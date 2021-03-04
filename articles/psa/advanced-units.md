---
title: Grupy jednostek i jednostki
description: Ten temat zawiera informacje o grupach jednostek i jednostkach.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145596"
---
# <a name="unit-groups-and-units"></a>Grupy jednostek i jednostki

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Grupy jednostek i jednostki są encjami podstawowymi w systemie Microsoft Dynamics 365. Jednostka jest pojedynczą jednostką miary, a wiele jednostek można połączyć w grupy jednostek. W interfejsie użytkownika (UI) programu Dynamics 365 grupa jednostek jest czasem określana mianem wykazu (harmonogramu) jednostek. 

Oto kilka przykładów jednostek i grup jednostek:
 
- **Grupa jednostek**: Odległość 
    - **Jednostki**: Mila, Kilometr itd.
- **Grupa jednostek**: Czas
    - **Jednostki**: Godzina, Dzień, Tydzień itd. 

Podczas konfigurowania wielu jednostek w grupie jednostek należy też zdefiniować współczynnik konwersji między nimi, wyznaczając pierwszą konfigurowaną jednostkę jako domyślną lub podstawową w grupie jednostek. 

Jeśli na przykład w grupie jednostek **Czas** jednostka **Godzina** zostanie ustawiona jako pierwsza, system wyznacza jednostkę **Godzina** jako domyślną. Jeśli następną konfigurowaną jednostką jest **Dzień**, należy skonfigurować współczynnik konwersji z **Dzień** na **Godzina**. Jeśli następnie dodasz **Tydzień** jako trzecią jednostkę, należy skonfigurować współczynnik konwersji jednostki **Tydzień** na jednostkę **Dzień** lub **Godzina**. 

Na poniższej ilustracji przedstawiono przykładową konfigurację jednostki **Dzień**, gdzie w polu **Ilość** jest wyświetlana liczba dni istniejących w dniu, oraz jednostki **Tydzień**, gdzie pole **Ilość** zawiera liczbę dni w tygodniu.

> ![Grupa jednostek: strona Informacje](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Używanie jednostek i grup jednostek

Program Dynamics 365 Project Service Automation używa jednostek i grup jednostek do przetwarzania oszacowań i wpisów dla kosztów i czasu. 

W przypadku kosztów każda kategoria wydatku ma domyślną grupę jednostek i jednostkę. Te wartości są wprowadzane jako wartości domyślne w pozycjach cennika dla kategorii wydatków. 

Na przykład masz kategorię wydatków o nazwie **Przebieg**. Ma ona grupę jednostek o nazwie **Odległość** oraz jednostkę domyślną o nazwie **Mila**. Jeśli skonfigurujesz grupę jednostek **Odległość** tak, aby zawierała dwie jednostki (**Mila** i **Kilometr**), można w jednym cenniku ustawić dwie ceny dla kategorii **Przebieg**: cenę za milę i cenę za kilometr.

| Kategoria wydatków  | Grupa jednostek  | Jednostka      | Metoda kalkulacji cen  | Cena jednostkowa  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Przebieg           | Odległość      | Mila      | Cena jednostkowa    | 10 USD            |
| Przebieg           | Odległość      | Kilometr | Cena jednostkowa    |  6 USD            |

Po wprowadzeniu wydatku w projekcie system oblicza mu cenę na podstawie kombinacji kategorii i jednostki. 

| Opis wydatku        | Kategoria wydatków  | Jednostka  | Ilość  | Cena jednostkowa   |
|----------------------------|---------------------|-------|-----------|----------------|
| Przejazd do lokalizacji klienta | Przebieg             | Mila  | 10        | 10 USD         |

Dla czasu każdy nagłówek cennika ma pole **Domyślna jednostka czasu**. Wartość jest ustawiana podczas tworzenia nagłówka cennika. Ta jednostka jest następnie używana do ustawiania wszystkich cen opartych na rolach w cenniku.

Wiersze szacowania dla pola **Czas w ofercie** mogą być wyrażone w dowolnej jednostce czasu. Natomiast wiersze szacowane w projektach oraz wpisy czasu dla projektów mogą używać tylko jednostki czasu **Godzina**. Jeśli jednostka we wpisie czasu lub wierszu szacowania nie pasuje do jednostki w wierszu cennika dla danej roli, system przelicza cenę na jednostki zdefiniowane w oszacowaniu projektu lub w transakcji z wartościami rzeczywistymi projektu.

W poniższym przykładzie pokazano, jak system PSA używa grupy jednostek, jednostek i współczynników konwersji.
- Units

   - **Grupa jednostek**: Czas 
   - **Jednostki**: Godzina 
    
    - **Dzień** — Współczynnik konwersji: 8 godzin       
    - **Tydzień** — Współczynnik konwersji: 40 godzin  
        
- Konfiguracja cennika w projekcie A:

    - **Nazwa**: Ceny sprzedaży na rynek brytyjski 2016 
    - **Domyślna jednostka czasu**: Dzień 
    - **Waluta**: GBP

| Rola      | Grupa jednostek | Jednostka | Jednostka organizacyjna | Cena   |
|-----------|------------|------|---------------------|---------|
| Dla deweloperów | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Wpis czasu

W poniższej tabeli przedstawiono wynikowe transakcje po stronie sprzedaży utworzone przez rozwiązanie PSA dla 3-godzinnego projektu.


| Projekt   | Zadanie    | Rola      | Ilość | Jednostka  | Cena jednostkowa | Kwota nierozliczonej sprzedaży |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Projekt  | Dla deweloperów | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Jednostka czasu — często zadawane pytania

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Czy program PSA przekształca na inne jednostki w przypadku kosztów?
Nr Przeliczanie jednostek działa tylko dla czasu. W przypadku kosztów — jeśli system nie może znaleźć ceny dla kombinacji kategorii wydatków i jednostki, cena jest domyślnie ustawiana na 0,00.

### <a name="why-does-psa-convert-time-units"></a>Dlaczego rozwiązanie PSA konwertuje jednostki czasu?
W niektórych krajach lub regionach istnieje prawny wymóg, aby stawki rozliczania były konfigurowane w dniach. Negocjowanie cen i przyznawanie rabatów w procesie ofertowym odbywa się przy użyciu stawek dziennych dla każdej roli podlegającej rozliczeniu. Szacowanie harmonogramów i wprowadzanie czasu odbywa się w godzinach. Aby uwzględnić tę różnicę w jednostkach czasu, program PSA konwertuje jednostki czasu.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Czy w oszacowaniach projektów można zmieniać jednostki czasu?
Nr Szacowanie harmonogramów można obecnie wykonywać tylko w godzinach.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Czy jednostki i grupy jednostek można edytować, usuwać i dodawać?
Tak. Z wyjątkiem grupy jednostek **Czasu** i jednostki **Godzina** można usuwać i edytować wszystkie jednostki, a także dodawać nowe jednostki. W usłudze PSA nie można usuwać grupy jednostek **Czas** ani jednostki **Godzina**. Można je jednak aktualizować o przetłumaczony tekst w polu **Nazwa**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]