---
title: Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie - wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu dodawania odpłatnych składników do pozycji kontraktu w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513892"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Pozycja kontraktu oparta na projekcie zawiera składniki typu *dołączane* i *odpłatne*.

Dołączone składniki to składniki, które:

  - Podlegają podziałom metody fakturowania i klienta
  - Nieprzekraczalne limity 
  - Ustawienia częstotliwości faktur zdefiniowane w pozycji kontraktu opartego na projekcie

Podzbiór dołączonych składników można oznaczyć jako odpłatny przy użyciu pola **Typ fakturowania**. Pole **Typ fakturowania** jest zestawem opcji, który zezwala na korzystanie z następujących wartości w kontekście pozycji kontraktu:

  - Odpłatne
  - Nieodpłatne

Składniki odpłatne mogą być definiowane w zadaniach, rolach i kategoriach transakcji.

Opłata jest definiowana w zadaniach dla pozycji kontraktu projektu i stosowana do wszystkich klas transakcji zawartych w wierszu. Jeśli pole **Dołącz zadania** w wierszu kontraktu jest puste lub ustawione na wartość **Cały projekt**, karta **Zadania odpłatne** nie będzie dostępna.

Opłata zdefiniowana w rolach pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Czas**. Jeśli pole **Dołącz czas** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Role odpłatne** nie będzie dostępna.

Opłata zdefiniowana w kategoriach transakcji pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Wydatek**. Jeśli pole **Wydatek** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Kategorie odpłatne** nie będzie dostępna.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Aktualizowanie zadania projektu jako odpłatnego lub niepłatnego

Zadanie projektu może być odpłatne lub niepłatne w ramach określonej pozycji kontraktu, co powoduje, że dostępne są następujące ustawienia:

Jeśli pozycja kontraktu oparta na projekcie zawiera **Czas** i określone zadanie, **T1** jest z nim skojarzone jako odpłatne. Jeśli istnieje drugi wiersz kontraktu zawierający **Wydatki**, można skojarzyć zadanie T1 w pozycji kontraktu z jako nieodpłatne. W efekcie cały czas zanotowany dla zadania jest odpłatny, a wydatki nie.

Typ fakturowania zadania można skonfigurować na karcie **Odpłatne zadania** w pozycji kontraktu przez zaktualizowanie pola **Typ fakturowania** w podsiatce zadania związane z pozycjami kontraktu. Można również zaktualizować pole **Typ fakturowania** w podsiatce ustawień fakturowania zadań projektu, który zawiera pozycje kontraktu skojarzone z zadaniem.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Aktualizowanie ról projektu jako odpłatnego lub niepłatnego

Rola w danej pozycji kontraktu może być płatna lub nieodpłatna.

Typ fakturowania roli można skonfigurować na karcie **Role płatne** w pozycji kontraktu. W tym celu należy zaktualizować pole **Typ fakturowania** w podsiatce **Role płatne**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Aktualizowanie kategorii transakcji jako odpłatnej lub nie

Kategoria transakcji w danej pozycji kontraktu może być płatna lub nieodpłatna.

Typ fakturowania transakcji można skonfigurować na karcie **Kategorie płatne** w pozycji kontraktu opartej na projekcie. W tym celu należy zaktualizować pole **Typ fakturowania** w podsiatce **Kategorie płatne**.

### <a name="resolve-chargeability"></a>Rozwiązywanie odpłatności

Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli **Czas** zostanie uwzględniony w pozycji kontraktu, a w przypadku, gdy **Zadanie** i **Rola** zostaną skonfigurowane jako odpłatne w pozycji kontraktu.

Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli **Wydatek** zostanie uwzględniony w pozycji kontraktu, a w przypadku, gdy kategorie **Zadanie** i **Transakcja** zostaną skonfigurowane jako odpłatne w pozycji kontraktu.


| Uwzględnia czas | Uwzględnia wydatek | Uwzględnia zadania | Rola           | Kategoria       | Zadanie                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Tak           | Tak              | Cały projekt | Odpłatne     | Odpłatne     | Fakturowanie wartości rzeczywistej czas: **Odpłatny** </br> Typ fakturowania wartości rzeczywistej wydatku: **Odpłatny**           |
| Tak           | Tak              | Tylko wybrane zadania | Odpłatne     | Odpłatne     | Fakturowanie wartości rzeczywistej czas: **Odpłatny** </br> Typ fakturowania wartości rzeczywistej wydatku: **Odpłatny**           |
| Tak           | Tak              | Tylko wybrane zadania | Nieodpłatne | Odpłatne     | Fakturowanie wartości rzeczywistej czas: **Nieodpłatny** </br> Typ fakturowania wartości rzeczywistej wydatku: **Odpłatny**       |
| Tak           | Tak              | Tylko wybrane zadania | Odpłatne     | Odpłatne     | Fakturowanie wartości rzeczywistej czas: **Nieodpłatny** </br> Typ fakturowania wartości rzeczywistej wydatku: **Nieodpłatny** |
| Tak           | Tak              | Tylko wybrane zadania | Nieodpłatne | Odpłatne     | Fakturowanie wartości rzeczywistej czas: **Nieodpłatny** </br> Typ fakturowania wartości rzeczywistej wydatku: **Nieodpłatny** |
| Tak           | Tak              | Tylko wybrane zadania | Nieodpłatne | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: **Nieodpłatny** </br> Typ fakturowania wartości rzeczywistej wydatku: **Nieodpłatny** |
| No            | Tak              | Cały projekt | Nie można ustawić   | Odpłatne     | Fakturowanie wartości rzeczywistej czas: **Niedostępne**</br>Typ fakturowania wartości rzeczywistej wydatku: **Odpłatny**          |
| No            | Tak              | Cały projekt | Nie można ustawić   | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: **Niedostępne**</br> Typ fakturowania wartości rzeczywistej wydatku: **Nieodpłatny**     |
| Tak           | No               | Cały projekt | Odpłatne     | Nie można ustawić   | Fakturowanie wartości rzeczywistej czas: **Odpłatny** </br> Typ fakturowania wartości rzeczywistej wydatku: **Niedostępne**        |
| Tak           | No               | Cały projekt | Nieodpłatne | Nie można ustawić   | Fakturowanie wartości rzeczywistej czas: **Nieodpłatny** </br>Typ fakturowania wartości rzeczywistej wydatku: **Niedostępne**   |
