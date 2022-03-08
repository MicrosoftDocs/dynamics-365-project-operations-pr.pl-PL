---
title: Konfigurowanie odpłatnych składników w pozycji kontraktu projektu
description: Ten temat zawiera informacje na temat dołączonych, odpłatnych i nieodpłatnych składników w wierszu oferty.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 51151089df67e2d164fc6315c1291f880917f43f1fba189304cb305ea973cecb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004054"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Konfigurowanie odpłatnych składników w pozycji kontraktu projektu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Pozycja kontraktu oparta na projekcie zawiera składniki typu dołączane, nieodpłatne i odpłatne.

Dołączone składniki podlegają metodom fakturowania, rozdzieleniu klientów, limitom nie do przekroczenia i ustawieniom częstotliwości fakturowania, które zdefiniowano w pozycji kontraktu opartej na projektach.

Podzbiór dołączonych składników można oznaczyć jako odpłatny korzystając z pola **Typ fakturowania**.

Składniki odpłatne mogą być definiowane w rolach i kategoriach transakcji.

Opłata zdefiniowana w rolach w ramach pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Czas**. Jeśli pole **Dołącz czas** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Role odpłatne** nie będzie dostępna.

Opłata zdefiniowana w kategoriach transakcji pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Wydatek**. Jeśli pole **Dołącz wydatki** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Kategorie odpłatne** nie będzie dostępna.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie ról projektu jako odpłatnego lub niepłatnego

Rola w danej pozycji kontraktu opartego na projekcie może być płatna lub nieodpłatna.

Na karcie **Role odpłatne** w pozycji kontraktu opartego na projekcie w podsiatce **Kategorie odpłatne** w polu **Typ fakturowania** zaktualizuj typ fakturowania dla danej roli.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie kategorii transakcji jako odpłatnej lub nie

Kategoria transakcji w danej pozycji kontraktu opartej na projekcie może być płatna lub nieodpłatna.

Na karcie **Kategorie odpłatne** w pozycji kontraktu opartej na projekcie w podsiatce **Kategorie odpłatne** w polu **Typ fakturowania** zaktualizuj typ fakturowania dla transakcji.

### <a name="resolve-chargeability"></a>Rozwiązywanie odpłatności

Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli czas zostanie uwzględniony w pozycji kontraktu, a w przypadku, gdy zadanie i rola zostaną skonfigurowane jako odpłatne w pozycji kontraktu.

Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli wydatek zostanie uwzględniony w pozycji kontraktu, a w przypadku, gdy kategorie transakcja zostanie skonfigurowana jako odpłatna w pozycji kontraktu.

| Uwzględnia czas | Uwzględnia wydatek | Rola | Kategoria | Zadanie |
| --- | --- | --- | --- | --- |
| Tak | Tak | Odpłatne | Odpłatne | Fakturowanie wartości rzeczywistej czas: Odpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Tak | Tak | Nieodpłatne | Odpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Tak | Tak | Nieodpłatne | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| Brak | Tak | Nie można ustawić | Odpłatne | Fakturowanie wartości rzeczywistej czas: Niedostępne </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Brak | Tak | Nie można ustawić | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: Niedostępne </br>Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| Tak | Brak | Odpłatne | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Odpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Niedostępne |
| Tak | Brak | Nieodpłatne | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Nieodpłatny </br> Typ fakturowania wartości rzeczywistej wydatku: Niedostępne |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
