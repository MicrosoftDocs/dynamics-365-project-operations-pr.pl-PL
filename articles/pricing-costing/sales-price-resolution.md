---
title: Określanie kosztów sprzedaży dla oszacowań i wartości rzeczywistych projektu
description: W tym artykule przedstawiono informacje na temat sposobu określania cen sprzedaży w przypadku wartości szacowanych i rzeczywistych projektu.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475383"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Określanie kosztów sprzedaży dla oszacowań i wartości rzeczywistych projektu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Aby określić ceny sprzedaży w wartościach szacunkowych i wartościach rzeczywistych w aplikacji Microsoft Dynamics 365 Project Operations, platforma najpierw używa daty i waluty w przychodzącym kontekście szacowania lub wartości rzeczywistych do określania cennika sprzedaży. W szczególności w kontekście wartości rzeczywistych platforma używa pola **Data transakcji** do określenia obowiązującego cennika. Wartość **daty transakcji** przychodzącego szacowania lub wartości rzeczywistej jest porównywana z wartościami **Effective Start (independent)** i **Effective End (Timezone independent)** w cenniku. Po określeniu cennika sprzedaży platforma definiuje stawkę sprzedaży lub rozliczania.

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

1. Platforma dopasowuje kombinację pól **Rola**, **Firma zasobów** i **Jednostka zasobów** w kontekście wartości szacowanych lub rzeczywistych z wiersza **Czas** względem wierszy cen dla roli w cenniku. To dopasowanie zakłada, że używasz gotowych wymiarów cen dla stawek rozliczania. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał innym polom niż **Rola**, **Firma zasobów** i **Jednostka zasobów**, to nastąpi połączenie, które będzie pobierało pasującą cena kategorii roli.
1. Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola**, **Firma zasobów** oraz **Jednostką zasobów**, to będzie to domyślna stawka rozliczeniowa.

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji **Roli**, **Firmy zasobów** i **Jednostki zasobów** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie cen odpowiednio się zmieni. Platforma pobiera rekordy cen ról o wartościach, które pasują do każdej wartości wymiaru cen w kolejności priorytetów. Wiersze o wartościach null dla tych wymiarów są ostatnie.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
