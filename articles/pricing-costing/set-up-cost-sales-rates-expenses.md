---
title: Konfigurowanie kosztów i stawek sprzedaży na potrzeby wydatku
description: Ten temat zawiera informacje na temat konfigurowania kosztów i stawek sprzedaży dla transakcji i kategorii wydatków.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee52daae18c5f9f0b630e54359021fffe1759274
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274921"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Konfigurowanie kosztów i stawek sprzedaży na potrzeby wydatku

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W rozwiązaniu Dynamics 365 Project Operations można skonfigurować ceny kosztów i sprzedaży dla kategorii transakcji. Ze względu na fakt, że koszty i ceny sprzedaży są projektowane z uwzględnieniem kosztów, każda kategoria transakcji zawierająca te elementy musi również zostać ustawiona jako kategoria wydatku. Dzięki tej konfiguracji jest zapewniana dokładność funkcji podrzędnych. Koszty i ceny sprzedaży dla kategorii transakcji można wystawiać tylko w jednej walucie, która musi być walutą w nagłówku cennika.

W celu skonfigurowania kosztów i stawek sprzedaży dla kategorii transakcji wykonaj poniższe kroki. 

1. Utwórz cennik na podstawie nagłówka cennika. 
2. Na **Ceny kategorii** w menu podsiatce wybierz pozycję **+ Nowa cena kategorii**. 
3. Na stronie **Szybkie tworzenie** wprowadź kategorię transakcji i jednostkę, dla której jest tworzona nowa cena.

W poniższej tabeli podano pola na karcie **Ogólne** oraz na stronie **Szybkie tworzenie** z wiersza cen z kategoriami, o których trzeba pamiętać, podczas tworzenia cen kategorii w cenniku sprzedaży lub kosztów:

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| Kategoria transakcji | Karta **Ogólne** i strony **Szybkie tworzenie** | Wybierz kategorię transakcji, dla której tworzysz cenę sprzedaży lub kosztu własnego. | Kategoria transakcji na oszacowaniu przychodzącym lub wartości rzeczywistej wydatku będzie dopasowana do tego wiersza domyślnej stawki kosztu lub sprzedaży za kategorię transakcji. |
| Harmonogram jednostek | Karta **Ogólne** i strony **Szybkie tworzenie** | Harmonogram jednostki jest pobierany domyślnie z harmonogramu w kategorii transakcji. | To pole nie ma wpływu na dalsze etapy. |
| Jednostka | Karta **Ogólne** i strony **Szybkie tworzenie** | Wybierz jednostkę, dla której są ustawiane stawki. | Jednostka w szacowaniu przychodzącej lub wartość rzeczywista jest dopasowana do jednostki w tym wierszu w celu ustawienia domyślnej stawki w szacowaniu wydatku lub wartości rzeczywistej. |
| Metoda kalkulacji cen | Karta **Ogólne** i strony **Szybkie tworzenie** | Dopuszczalne wartości pola **Metoda kalkulacji ceny** to **Cena jednostkowa**, **Po kosztach** i **Narzut po koszcie**. | Podczas konfigurowania cen wybranie opcji **Cena na jednostkę** zablokuje cenę w polu **Procent** w wierszu kategorii. W przypadku wyboru **Po kosztach**, pola **Cena** i **Procent** są blokowane w cenniku sprzedaży. Wybór opcji **Narzut po kosztach** powoduje zablokowanie pola **Cena** na liście cen sprzedaży. W przypadku przychodzącej linii kosztów rzeczywistych wydatku, metoda kalkulacji **Po kosztach** lub **Narzut po kosztach** skutkuje przypisaniem nierozliczonych wierszy sprzedaży do ceny, która jest równa cenie z rzeczywistego kosztu lub obliczonej jako narzut po kosztach. |
| Cena | Karta **Ogólne** i strony **Szybkie tworzenie** | W tym celu należy skonfigurować stawkę jednostkową dla każdej kategorii transakcji i jednostek. Na przykład stawka na odległość to 10 USD za milę i 8 USD za kilometr. | Stawka za przejechaną trasę jest stawką kosztową domyślną dla każdego kosztu jednostkowego lub ceny w szacowaniu przychodzącym lub wartości rzeczywistej dla klasy transakcji wydatek.|
| Procent | Karta **Ogólne** i strony **Szybkie tworzenie** | W tym celu należy skonfigurować wartość procentową ponad koszt dla każdej kategorii transakcji i jednostek. Na przykład współczynnik związany ze sprzedażą lotniczą być oznaczony 10 procentowym narzutem z powodu poniesionych kosztów transportu. | Procent narzutu na koszt ma zastosowanie tylko do cennika sprzedaży jeśli wybrana metoda kalkulacji ceny to **Narzut na koszt**. |
| Waluta | Karta **Ogólne** i strony **Szybkie tworzenie** | Domyślnie ta wartość pochodzi z waluty w nagłówku cennika. W przypadku cennika kategorii transakcji nie można zastąpić waluty. | Ta waluta to domyślna waluta każdego kosztu jednostkowego w transakcji wydatków dla kosztów i sprzedaży. |

## <a name="pricing-methods-for-expenses"></a>Metody kalkulacji kosztów dla wydatków

Podczas konfigurowania cen kategorii, które są istotne tylko w kontekście kalkulacji cen kosztów, można użyć jednej z następujących trzech metod kalkulacji cen:

- **Cena jednostkowa**
- **Po kosztach**
- **Narzut na koszt**

### <a name="price-per-unit"></a>Cena jednostkowa
W przypadku wybrania tej metody kalkulacji cen w cenniku powiązanym cena sprzedaży jest domyślnie określana przez kombinację kategoria i jednostka zarówno w szacowaniu, jak i wartości rzeczywistej. Szacowane wiersze odnoszą się do wierszy oszacowania projektu dla wydatki, wierszy szczegółów oferty i wierszy szczegółów kontraktu dla wydatków.

### <a name="at-cost"></a>Po kosztach
W przypadku wybrania tej metody kalkulacji cen w cenniku powiązanym cena sprzedaży jest domyślnie określana przez kombinację kategoria i jednostka tylko dla wartości rzeczywistej. Na przykład wartości rzeczywiste dotyczące nierozliczonej sprzedaży dla klasy transakcji wydatkowej. Cena jednostkowa jest ustalana na podstawie niepodlegającej sprzedaży wartości rzeczywistych z ceny jednostkowej na koszt rzeczywisty danego wydatku. Domyślne ustawianie cen przy użyciu kosztów nie jest wykonywane na podstawie oszacowań kosztów lub wierszy oferty oraz szczegółów pozycji kontraktu dla kosztów.

### <a name="markup-over-cost"></a>Narzut na koszt
W przypadku wybrania tej metody kalkulacji cen w cenniku powiązanym cena sprzedaży jest domyślnie określana przez kombinację kategoria i jednostka tylko dla wartości rzeczywistej. Na przykład wartości rzeczywiste dotyczące nierozliczonej sprzedaży dla klasy transakcji wydatkowej. Ta cena jednostkowa jest ustalana na podstawie ceny niepodlegającej sprzedaży w odniesieniu do wartości obliczonej, która jest wyznaczana na wartość ceny jednostkowej w koszcie rzeczywistym dla tego wydatku po zastosowaniu określonego procentu marży. Domyślne ustawianie cen przy użyciu kosztów nie jest wykonywane na podstawie oszacowań kosztów lub wierszy oferty oraz szczegółów pozycji kontraktu dla kosztów.


[!INCLUDE[footer-include](../includes/footer-banner.md)]