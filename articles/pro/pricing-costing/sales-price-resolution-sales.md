---
title: Określanie cen sprzedaży dla szacowań i wartości rzeczywistych projektu
description: W tym artykule przedstawiono informacje na temat sposobu określania cen sprzedaży w przypadku wartości szacowanych i rzeczywistych projektu.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410132"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Określanie cen sprzedaży dla szacowań i wartości rzeczywistych projektu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Aby określić ceny sprzedaży w wartościach szacunkowych i wartościach rzeczywistych w aplikacji Microsoft Dynamics 365 Project Operations, platforma najpierw używa daty i waluty w przychodzącym kontekście szacowania lub wartości rzeczywistych do określania cennika sprzedaży. W szczególności w kontekście wartości rzeczywistych platforma używa pola **Data transakcji** do określenia obowiązującego cennika. Po określeniu cennika sprzedaży platforma definiuje stawkę sprzedaży lub rozliczania.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Określanie stawek sprzedaży w wartościach rzeczywistych i oszacowaniach dla wiersza Czas

Kontekst szacowania dla wiersza **Czas** odnosi się do następujących elementów:

- Szczegóły wierszy ofert dla elementu **Czas**.
- Szczegóły pozycji kontraktu dla elementu **Czas**.
- Przypisania zasobu do projektu.

Kontekst wartości rzeczywistych dla wiersza **Czas** odnosi się do następujących elementów:

- Wprowadzanie i poprawianie wpisów w arkuszu dla elementu **Czas**.
- Wpisy w arkuszy utworzone podczas przesyłania wpisów czasu.
- Szczegóły wiersza faktury dla elementu **Czas**. 

Po określeniu cennika na potrzeby sprzedaży platforma wykonuje poniższe kroki, aby wprowadzić domyślną stawkę rozliczania.

1. Platforma dopasowuje kombinację pól **Rola** i **Jednostka zasobów** w kontekście wartości szacowanych lub rzeczywistych z wiersza **Czas** względem wierszy cen dla roli w cenniku. To dopasowanie zakłada, że używasz gotowych wymiarów cen dla stawek rozliczania. Jeśli ceny skonfigurowano tak, aby opierały się na polach innych niż lub dodatkowo do pól **Rola** oraz **Jednostka zasobów**, do pobierania pasującego wiersza ceny dla roli, jest używana kombinacja tych pól.
1. Jeśli platforma znajdzie wiersz ceny dla roli, który ma stawkę rozliczania dla kombinacji pól **Rola** i **Jednostką zasobów**, ta stawka rozliczania będzie używana jako domyślna.
1. Jeśli platforma nie może dopasować wartości pól **Rola**, **Jednostka zasobów**, pobiera wiersze ceny dla roli, które mają pasujące wartości dla pola **Rola** oraz wartości null dla pola **Jednostka zasobów**. Gdy platforma zajdzie pasujący rekord ceny dla roli, stawka rozliczania z tego rekordu będzie używana jako domyślna. To dopasowanie zakłada użycie gotowej konfiguracji dla względnego priorytetu pola **Rola** w porównaniu z polem **Jednostka zasobów** jako wymiaru ceny sprzedaży.

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji pól **Rola** i **Jednostka zasobów** lub jeśli istnieją inne wymiary mające wyższy priorytet, poprzednie zachowanie odpowiednio się zmieni. Platforma pobiera rekordy cen ról o wartościach, które pasują do każdej wartości wymiaru cen w kolejności priorytetów. Wiersze o wartościach null dla tych wymiarów są ostatnie.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Określanie stawek sprzedaży w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek

Kontekst szacowania dla wiersza **Wydatek** odnosi się do następujących elementów:

- Szczegóły wierszy ofert dla elementu **Wydatek**.
- Szczegóły pozycji kontraktu dla elementu **Wydatek**.
- Wiersze szacowań wydatków w projekcie.

Rzeczywisty kontekst dla wiersza **Wydatek** odnosi się do następujących elementów:

- Wprowadzanie i poprawianie wpisów w arkuszu dla elementu **Wydatek**.
- Wpisy w arkuszy utworzone podczas przesyłania wpisów wydatków.
- Szczegóły wiersza faktury dla elementu **Wydatek**. 

Po określeniu cennika na potrzeby sprzedaży platforma wykonuje poniższe kroki, aby wprowadzić domyślną cenę jednostkową sprzedaży.

1. Platforma dopasowuje kombinację pól **Kategoria** oraz **Jednostka** z wiersza szacowania dla wiersza **Wydatek** w celu dopasowania do wiersza ceny kategorii w cenniku.
1. Jeśli platforma znajdzie wiersz ceny kategorii, który ma stawkę sprzedaży dla połączenia pól **Kategoria** i **Jednostka**, ta stawka sprzedaży będzie używana jako domyślna.
1. Jeśli platforma znajdzie pasujący wiersz cena kategorii, może użyć metody cen do wprowadzenia domyślnej ceny sprzedaży. W poniższej tabeli podano domyślne zachowanie cen dla wydatków w aplikacji Project Operations.

    | Kontekst | Metoda kalkulacji cen | Cena domyślna |
    | --- | --- | --- |
    | Szacowanie | Cena jednostkowa | Na podstawie wiersza cena kategorii. |
    |        | Po kosztach | 0.00 |
    |        | Narzut na koszt | 0.00 |
    | Rzeczywiste | Cena jednostkowa | Na podstawie wiersza cena kategorii. |
    |        | Po kosztach | Na podstawie wartości rzeczywistych powiązanych z kosztem. |
    |        | Narzut na koszt | Narzut zdefiniowany w wierszu kategorii cena jest stosowany do stawki kosztu jednostkowego dla wartości rzeczywistej pokrewnego kosztu. |

1. Jeśli platforma nie może dopasować wartości **Kategoria** i **Jednostka**, stawka sprzedaży jest domyślnie ustawiona na **0** (zero).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Określanie stawek sprzedaży w wierszach rzeczywistych i szacowanych dla wiersza Materiały

Kontekst szacowania dla wiersza **Materiały** odnosi się do następujących elementów:

- Szczegóły wierszy ofert dla elementu **Materiały**.
- Szczegóły pozycji kontraktu dla elementu **Materiały**.
- Wiersze szacowań materiałów w projekcie.

Rzeczywisty kontekst dla wiersza **Materiały** odnosi się do następujących elementów:

- Wprowadzanie i poprawianie wpisów w arkuszu dla elementu **Materiały**.
- Wpisy w arkuszy utworzone podczas przesyłania dziennika użycia materiałów.
- Szczegóły wiersza faktury dla elementu **Materiały**. 

Po określeniu cennika na potrzeby sprzedaży platforma wykonuje poniższe kroki, aby wprowadzić domyślną cenę jednostkową sprzedaży.

1. Platforma dopasowuje kombinację pól **Produkt** i **Jednostka** w wierszu szacowania dla wiersza **Materiały** w celu dopasowania do wierszy pozycji cennika w cenniku.
1. Jeśli platforma znajdzie wiersz pozycji cennika, który ma stawkę sprzedaży dla kombinacji pól **Produkt** i **Jednostka**, a metoda cen to **Kwota w walucie**, używana jest cena sprzedaży określona w wierszu cennika. 
1. Jeśli wartości pól **Produkt** i **Jednostka** nie są zgodne lub jeśli metoda cen jest inna niż **Kwota w walucie**, stawka sprzedązy jest domyślnie ustawiana na **0** (zero). Dzieje się tak, ponieważ aplikacja Project Operations obsługuje tylko metodę cen **Kwota w walucie** dla materiałów używanych w projekcie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
