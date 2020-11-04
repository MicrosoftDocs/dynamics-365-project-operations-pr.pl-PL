---
title: Metody rezerwowania alokacji
description: Ta temat zawiera informacje na temat sposobu działania metod alokacji zaliczania w Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c2a964c18c7eae61c5a0239da3b18da31b6ad574
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081962"
---
# <a name="booking-allocation-methods"></a>Metody rezerwowania alokacji

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Niezależnie, czy dodajesz członka zespołu bezpośrednio do projektu na karcie **Zespół** , czy rezerwujesz zasób dla projektu lub wymaganie z tablicy harmonogramu, istnieje kilka metod rezerwacji przydziału, które mogą zostać użyte. W tym temacie wyjaśniono, jak działa każda z tych metod, i które z tych metod mogą spowodować nałożenie się rezerwacji zasobów.

## <a name="booking-allocation-methods"></a>Metody rezerwowania alokacji

Istnieje sześć metod przydziału rezerwacji, których można użyć:

- [Pełna dyspozycyjność](#full)
- [Pozostała dyspozycyjność](#remaining)
- [Dyspozycyjność procentowa](#percentage)
- [Godziny — rozłóż równomiernie](#evenly)
- [Godziny — najwięcej na początku](#front)
- [Brak](#none)

### <a name="full-capacity"></a><a name="full"></a>Pełna dyspozycyjność 
Metoda Pełna dyspozycyjność rezerwuje pełną dyspozycyjność zasobu dla określonych dat Od/Do. Na przykład jeśli zasób ma kalendarz skonfigurowany dla pracy osiem godzin dziennie, pięć dni w tygodniu, ustawienie dat rozpoczęcia i zakończenia, które obejmują pięć dni roboczych, zarezerwuje zasób na 40 godzin. Rezerwacja odbywa się bez wzięcia pod uwagę pozostałej dyspozycyjności zasobu. Jeśli zasób jest już zarezerwowany w tym samym okresie dla innych projektów, 40 godzin zostanie zarezerwowane jako dodatkowe godziny, potencjalnie prowadząc do nakładania się rezerwacji.

### <a name="remaining-capacity"></a><a name="remaining"></a>Pozostała dyspozycyjność
Metoda Pozostała dyspozycyjność jest dostępna tylko w przypadku, gdy przeprowadzasz rezerwację bezpośrednio dla projektu przy użyciu tablicy harmonogramu. Ta metoda rezerwuje dostępną dyspozycyjności zasobu w określonym zakresie dat. Na przykład jeśli zasób ma dyspozycyjność równą 40 godzin w tygodniu i został już zarezerwowany na 10 godzin, rezerwacja na ten sam tydzień spowoduje rezerwację na pozostałe 30 godzin dyspozycyjności w tygodniu.

### <a name="percentage-capacity"></a><a name="percentage"></a>Dyspozycyjność procentowa
Metoda Dyspozycyjność procentowa rezerwuje procent dyspozycyjności zasobu dla określonych dat Od/Do. Na przykład jeśli zasób ma kalendarz skonfigurowany dla pracy osiem godzin dziennie, pięć dni w tygodniu, ustawienie dat rozpoczęcia i zakończenia, które obejmują pięć dni roboczych z 50-procentową dyspozycyjnością, zarezerwuje zasób na 20 godzin. Poszczególne rezerwacje na dzień są rozkładane po równo na cały ten okres, w tym przykładzie na cztery godziny w ciągu dnia. Rezerwacja odbywa się bez wzięcia pod uwagę pozostałej dyspozycyjności zasobu. Jeśli zasób jest już zarezerwowany w tym samym okresie dla innych projektów, 20 godzin zostanie zarezerwowane jako dodatkowe godziny, potencjalnie prowadząc do nakładania się rezerwacji.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Godziny — rozłóż równomiernie
Metoda Godziny — rozłóż równomiernie rezerwuje zasób na określoną liczbą godzin, rozkładając czas równomiernie w ciągu dnia dla określonych dat Od i Do. Na przykład jeśli rezerwujesz zasób na 20 godzin przez okres pięciu dni, ta metoda rozkłada 20 godzin równomiernie na cztery godziny w ciągu dnia. Rezerwacja odbywa się bez wzięcia pod uwagę pozostałej dyspozycyjności zasobu. Jeśli zasób jest już zarezerwowany w tym samym okresie dla innych projektów, 20 godzin zostanie zarezerwowane jako dodatkowe godziny, potencjalnie prowadząc do nakładania się rezerwacji.

### <a name="front-load-hours"></a><a name="front"></a>Godziny — najwięcej na początku
Metoda Godziny — najwięcej na początku rezerwuje zasób na określoną liczbą godzin, kładąc nacisk na godziny początkowe w ciągu dnia dla określonych dat Od/Do. Położenie nacisku na godziny początkowe zużywa dostępną dyspozycyjność zasobu w kolejności "pierwszy wchodzi - pierwszy schodzi". Na przykład jeśli harmonogram pracy zasobu obejmuje osiem godzin na dobę przez pięć dni w tygodniu, i nie ma żadnych bieżących rezerwacji, zarezerwowanie zasobu na 20 godzin w okresie pięciu dni roboczych daje następujący wzorzec dzienny rezerwacji: 

|                           |    Dzień 1    |    Dzień 2    |    Dzień 3    |    Dzień 4    |    Dzień 5    |    Razem    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Istniejące rezerwacje**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nowa rezerwacja**          |    8        |    8        |    4        |    0        |    0        |    20       |

Metoda Najwięcej na początku bierze pod uwagę istniejące rezerwacje i dostępną dyspozycyjność. Na przykład jeśli ten sam zasób ma już 20 godzin rezerwacji na dany tydzień roboczy, nowe rezerwacje zużywają pozostałą dyspozycyjność w poniższy sposób:

|                     | Dzień 1 | Dzień 2 | Dzień 3 | Dzień 4 | Dzień 5 | Razem |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Istniejące rezerwacje** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Nowa rezerwacja**       | 0     | 0     | 4     | 8     | 8     | 20    |

Ponieważ dostępna dyspozycyjność jest brana pod uwagę, możesz otrzymać komunikat o błędzie, jeśli zasób nie ma już dyspozycyjności, która może zostać pobrana przez rezerwację. W przypadku tej metody nie można doprowadzić do nakładania się rezerwacji.

### <a name="none"></a><a name="none"></a>Brak
Metoda Brak jest dostępna tylko w przypadku, gdy rezerwację przeprowadzasz z karty **Zespół** w ramach projektu. Ta metoda dodaje zasób jako członka zespołu projektu, ale nie tworzy żadnych rezerwacji, które absorbują dyspozycyjność zasobu. Ta metoda jest używana gdy domyślny członek zespołu Menedżer projektu jest dodawany podczas tworzenia projektu. Użytkownik Menedżer projektu, który utworzył projekt jest domyślnie dodawany do projektu, tak aby rekordu encji projektu miał właściciela i istnieje jedna osoba zatwierdzająca projekt. Ponieważ ten użytkownik nie ma żadnych rezerwacji, jeśli chcesz zarezerwować zasób, możesz albo usunąć i ponownie je dodać przy użyciu innej metody alokacji, albo dodać zasób do zadań, a następnie użyć **Rozszerz rezerwacje** na karcie **Uzgadnianie** , aby utworzyć rezerwacje dla przypisań.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Metody alokacji prowadzące do nakładania się rezerwacji
Podsumowując, poniższe metody alokacji prowadzą do nakładania się rezerwacji, jeśli zasób zajmuje się już innymi projektami (lub innymi zleceniami pracy lub encjami, które można objąć harmonogramem):

- Pełna dyspozycyjność
- Dyspozycyjność procentowa
- Godziny — rozłóż równomiernie

Korzystając z jednej z tych trzech metod alokacji nie zostaniesz powiadomiony, że zasób został nadmiarowo zarezerwowany. Aby rozwiązać problem nakładania się rezerwacji, należy użyć tablicy harmonogramu.
