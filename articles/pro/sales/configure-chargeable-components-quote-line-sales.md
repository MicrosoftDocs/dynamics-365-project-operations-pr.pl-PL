---
title: Konfigurowanie odpłatnych składników wiersza oferty
description: Ten temat zawiera informacje na temat konfigurowania odpłatnych i nieodpłatnych składników w wierszu oferty opartej na projekcie.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082133"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurowanie odpłatnych składników wiersza oferty

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Pozycja oferty oparta na projekcie zawiera składniki typu *dołączane* i *odpłatne*.

Dołączone składniki są poddawane:

  - Podlegają podziałom metody fakturowania i klienta
  - Nieprzekraczalne limity 
  - Ustawienia częstotliwości faktur zdefiniowane w pozycji oferty opartej na projekcie

Podzbiór dołączonych składników można oznaczyć jako odpłatny przy użyciu pola **Typ fakturowania**. Pole **Typ fakturowania** jest zestawem opcji, który zezwala na korzystanie z następujących wartości w kontekście pozycji oferty:

  - Odpłatne
  - Nieodpłatne

Składniki odpłatne mogą być definiowane w zadaniach, rolach i kategoriach transakcji.

Opłata jest definiowana w zadaniach dla pozycji oferty projektu i stosowana do wszystkich klas transakcji zawartych w tym wierszu. Jeśli pole **Dołącz zadania** w wierszu kontraktu jest puste lub ustawione na wartość **Cały projekt** , karta **Zadania odpłatne** nie będzie dostępna.

Opłata zdefiniowana w rolach pozycji oferty, która ma zastosowanie tylko do klasy transakcji **Czas**. Jeśli pole **Dołącz czas** w wierszu oferty jest puste lub ustawione na wartość **Nie** , karta **Role odpłatne** nie będzie dostępna.

Opłata zdefiniowana w kategoriach transakcji pozycji oferty projektu ma zastosowanie tylko do klasy transakcji **Wydatek**. Jeśli pole **Dołącz wydatki** w wierszu oferty jest puste lub ustawione na wartość **Nie** , karta **Kategorie odpłatne** nie będzie dostępna.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie zadania projektu w stan odpłatny lub nieodpłatny

Zadanie projektu może być odpłatne lub niepłatne w ramach określonej pozycji oferty opartej na projekcie, co powoduje, że dostępne są następujące ustawienia:

Jeśli wiersz oferty opartej na projekcie zawiera **Czas** i zadanie **T1** , zadanie jest skojarzone z wierszem oferty jako odpłatne. Jeśli istnieje drugi wiersz oferty zawierający **Wydatki** , można skojarzyć zadanie **T1** w pozycji oferty jako nieodpłatne. W efekcie cały czas zanotowany dla zadania jest odpłatny, a wydatki zapisane w zadaniu nie.

Typ fakturowania zadania można skonfigurować na karcie **Zadania płatne** w pozycji oferty opartej na projekcie, poprzez zaktualizowanie pola **Typ fakturowania** w podsiatce **Zadania związanego z pozycjami oferty**. Można również zaktualizować pole **Typ fakturowania** , aby zaktualizować typ fakturowania w zadaniu projektu w podsiatce ustawienia fakturowania zadań projektu, która zawiera pozycje oferty przypisane do zadania.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie ról projektu jako odpłatnego lub niepłatnego

W kontekście określonego wiersza oferty opartej na projekcie rola może być odpłatna lub nieodpłatna.

Typ fakturowania zadania można skonfigurować na karcie **Role płatne** w pozycji oferty opartej na projekcie, poprzez zaktualizowanie pola **Typ fakturowania** w podsiatce **Role odpłatne**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie kategorii transakcji jako odpłatnej lub nie

Kategoria transakcji w danej pozycji oferty może być płatna lub nieodpłatna.

Typ fakturowania transakcji można skonfigurować na karcie **Kategorie płatne** w pozycji oferty opartej na projekcie, poprzez zaktualizowanie pola **Typ fakturowania** w podsiatce **Kategorie odpłatne**.

### <a name="resolve-chargeability"></a>Rozwiązywanie odpłatności
Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli **Czas** zostanie uwzględniony w pozycji oferty, a w przypadku, gdy **Zadanie** i **Rola** zostaną skonfigurowane jako odpłatne w pozycji oferty.

Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli **Wydatek** zostanie uwzględniony w pozycji oferty, a w przypadku, gdy kategorie **Zadanie** i **Kategoria transakcji** zostaną skonfigurowane jako odpłatne w pozycji oferty.

| Uwzględnia czas | Uwzględnia wydatek | Uwzględnione zadania | Rola | Kategoria | Zadanie | Rozliczenia |
| --- | --- | --- | --- | --- | --- | --- |
| Tak | Tak | Cały projekt | Odpłatne | Odpłatne | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Odpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Tak | Tak | Tylko wybrane zadania | Odpłatne | Odpłatne | Odpłatne | Fakturowanie wartości rzeczywistej czas: Odpłatny</br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Tak | Tak | Tylko wybrane zadania | Nieodpłatne | Odpłatne | Odpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny</br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Tak | Tak | Tylko wybrane zadania | Odpłatne | Odpłatne | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny</br> Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| Tak | Tak | Tylko wybrane zadania | Nieodpłatne | Odpłatne | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny</br> Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| Tak | Tak | Tylko wybrane zadania | Nieodpłatne | Nieodpłatne | Odpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny</br> Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| No | Tak | Cały projekt | Nie można ustawić | Odpłatne | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Niedostępne </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| No | Tak | Cały projekt | Nie można ustawić | Nieodpłatne | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Niedostępne </br>Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| Tak | No | Cały projekt | Odpłatne | Nie można ustawić | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Odpłatny</br>Typ fakturowania wartości rzeczywistej wydatku: Niedostępne |
| Tak | No | Cały projekt | Nieodpłatne | Nie można ustawić | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Nieodpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Niedostępne |
