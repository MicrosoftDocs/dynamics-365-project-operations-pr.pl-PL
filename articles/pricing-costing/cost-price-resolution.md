---
title: Określanie stawek kosztów dla oszacowań i wartości rzeczywistych projektu
description: W tym artykule przedstawiono informacje na temat sposobu określania stawek kosztów w przypadku wartości szacowanych i rzeczywistych projektu.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475292"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Określanie stawek kosztów dla oszacowań i wartości rzeczywistych projektu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Aby określić koszt własny w wartościach szacunkowych i wartościach rzeczywistych w aplikacji Microsoft Dynamics 365 Project Operations, platforma najpierw używa daty i waluty w przychodzącym kontekście szacowania lub wartości rzeczywistych do określania cennika sprzedaży. W szczególności w kontekście wartości rzeczywistych platforma używa pola **Data transakcji** do określenia obowiązującego cennika. Wartość **daty transakcji** przychodzącego szacowania lub wartości rzeczywistej jest porównywana z wartościami **Effective Start (independent)** i **Effective End (Timezone independent)** w cenniku. Po określeniu listy kosztów system określa stawkę kosztów.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Określanie stawek kosztów w kontekstach wartości szacowanych i rzeczywistych dla wiersza Czas

Kontekst szacowania dla wiersza **Czas** odnosi się do następujących elementów:

- Szczegóły wierszy ofert dla elementu **Czas**.
- Szczegóły pozycji kontraktu dla elementu **Czas**.
- Przypisania zasobu do projektu.

Kontekst wartości rzeczywistych dla wiersza **Czas** odnosi się do następujących elementów:

- Wprowadzanie i poprawianie wpisów w arkuszu dla elementu **Czas**.
- Wpisy w arkuszy utworzone podczas przesyłania wpisów czasu.

Po określeniu listy kosztów własnych platforma wykonuje poniższe kroki, aby wprowadzić domyślną stawkę kosztu.

1. Platforma dopasowuje kombinację pól **Rola**, **Firma zasobów** i **Jednostka zasobów** w kontekście wartości szacowanych lub rzeczywistych z wiersza **Czas** względem wierszy cen dla roli w cenniku. To dopasowanie zakłada, że używasz standardowych wymiarów cenowych dla kosztów pracy. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał polom **Rola**, **Firma zasobów** i **Jednostka zasobów** lub odpowiadał także tym polom, w celu pobrania pasującego cennika ról zostanie wykorzystana inna kombinacja.
1. Jeśli system znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola**, **Firma zasobów** oraz **Jednostką zasobów**, to będzie to koszt będzie użyty domyślny.
1. Jeśli w systemie nie można dopasować wartości **Rola**, **Firma zasobów** i **Jednostka zasobów**, system odrzuca wymiar o najniższym priorytecie, wyszukuje w wierszach cen ról pasujących do pozostałych dwóch wartości rozmiarów i dalej stopniowo odrzuca wymiary, dopóki nie zostanie znaleziony wiersz ceny pasującej roli. Koszt z tego rekordu będzie używana jako domyślny koszt. Jeśli system nie znajdzie pasującego wiersza ceny roli, cena zostanie domyślnie ustawiona na **0** (zero).

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji pól **Rola** i **Jednostka zasobów** lub jeśli istnieją inne wymiary mające wyższy priorytet, poprzednie zachowanie odpowiednio się zmieni. Platforma pobiera rekordy cen ról o wartościach, które pasują do każdej wartości wymiaru cen w kolejności priorytetów. Wiersze o wartościach null dla tych wymiarów są ostatnie.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Określanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek

Kontekst szacowania dla wiersza **Wydatek** odnosi się do następujących elementów:

- Szczegóły wierszy ofert dla elementu **Wydatek**.
- Szczegóły pozycji kontraktu dla elementu **Wydatek**.
- Szacowania wydatków w projekcie.

Rzeczywisty kontekst dla wiersza **Wydatek** odnosi się do następujących elementów:

- Wprowadzanie i poprawianie wpisów w arkuszu dla elementu **Wydatek**.
- Wpisy w arkuszy utworzone podczas przesyłania wpisów wydatków.

Po określeniu listy kosztów własnych platforma wykonuje poniższe kroki, aby wprowadzić domyślną stawkę kosztu.

1. Platforma dopasowuje kombinację pól **Kategoria** i **Jednostka** w kontekście wartości szacowanych lub rzeczywistych z wiersza **Wydatek** względem wierszy kategorii w cenniku.
1. Jeśli platforma znajdzie wiersz ceny kategorii, który ma stawkę kosztu dla połączenia pól **Kategoria** i **Jednostka**, ta stawka kosztu będzie używana jako domyślna.
1. Jeśli platforma nie może dopasować wartości **Kategoria** i **Jednostka**, cena jest domyślnie ustawiona na **0** (zero).
1. W kontekście szacowania jeśli platforma nie może dopasować wiersza ceny kategorii, ale metoda cen jest inna niż **Cena jednostkowa**, stawka kosztu jest domyślnie ustawiana na **0** (zero).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Określanie stawek kosztów w wierszach rzeczywistych i szacowanych dla elementu Materiały

Kontekst szacowania dla wiersza **Materiały** odnosi się do następujących elementów:

- Szczegóły wierszy ofert dla elementu **Materiały**.
- Szczegóły pozycji kontraktu dla elementu **Materiały**.
- Szacowania materiałów w projekcie.

Rzeczywisty kontekst dla wiersza **Materiały** odnosi się do następujących elementów:

- Wprowadzanie i poprawianie wpisów w arkuszu dla elementu **Materiały**.
- Wpisy w arkuszy utworzone podczas przesyłania dziennika użycia materiałów.

Po określeniu listy kosztów własnych platforma wykonuje poniższe kroki, aby wprowadzić domyślną stawkę kosztu.

1. Platforma używa kombinacji pól **Produkt** i **Jednostka** w kontekście wartości szacowanych lub rzeczywistych z wiersza **Materiały** względem wierszy pozycji cennika w cenniku.
1. Jeśli platforma znajdzie wiersz pozycji cennika, który ma stawkę kosztu dla połączenia pól **Produkt** i **Jednostka**, ta stawka kosztu będzie używana jako domyślna.
1. Jeśli platforma nie może dopasować wartości **Produkt** i **Jednostka**, koszt jednostki jest domyślnie ustawiany na **0** (zero).
1. W kontekście szacowania lub wartości rzeczywistych jeśli platforma nie może dopasować wiersza pozycji cennika, ale metoda cen jest inna niż **Kwota w walucie**, koszt jednostki jest domyślnie ustawiany na **0**. Dzieje się tak, ponieważ aplikacja Project Operations obsługuje tylko metodę cen **Kwota w walucie** dla materiałów używanych w projekcie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
