---
title: Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie
description: Ten temat zawiera informacje na temat dołączonych, odpłatnych i nieodpłatnych składników w wierszu oferty.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081949"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Pozycja kontraktu oparta na projekcie zawiera składniki typu dołączane, nieodpłatne i odpłatne.

Dołączone składniki podlegają metodom fakturowania, rozdzieleniu klientów, limitom nie do przekroczenia i ustawieniom częstotliwości fakturowania, które zdefiniowano w pozycji kontraktu opartej na projektach.

Podzbiór dołączonych składników można oznaczyć jako odpłatny korzystając z pola **Typ fakturowania**.

Składniki odpłatne mogą być definiowane w rolach i kategoriach transakcji.

Opłata zdefiniowana w rolach w ramach pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Czas**. Jeśli pole **Dołącz czas** w wierszu kontraktu jest puste lub ustawione na wartość **Nie** , karta **Role odpłatne** nie będzie dostępna.

Opłata zdefiniowana w kategoriach transakcji pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Wydatek**. Jeśli pole **Dołącz wydatki** w wierszu kontraktu jest puste lub ustawione na wartość **Nie** , karta **Kategorie odpłatne** nie będzie dostępna.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie ról projektu jako odpłatnego lub niepłatnego

Rola w danej pozycji kontraktu opartego na projekcie może być płatna lub nieodpłatna.

Typ fakturowania w ramach danej roli można skonfigurować na karcie **Role płatne** w pozycji oferty opartej na projekcie, poprzez zaktualizowanie pola **Typ fakturowania** w podsiatce **Role odpłatne**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie kategorii transakcji jako odpłatnej lub nie

Kategoria transakcji w danej pozycji kontraktu opartej na projekcie może być płatna lub nieodpłatna.

Typ fakturowania w ramach danej transakcji można skonfigurować na karcie **Role płatne** w pozycji kontraktu opartej na projekcie, poprzez zaktualizowanie pola **Typ fakturowania** w podsiatce **Role odpłatne**.

### <a name="resolve-chargeability"></a>Rozwiązywanie odpłatności

Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli czas zostanie uwzględniony w pozycji kontraktu, a w przypadku, gdy zadanie i rola zostaną skonfigurowane jako odpłatne w pozycji kontraktu.

Utworzony czas szacowany lub rzeczywisty będzie uważany za odpłatny, jeśli wydatek zostanie uwzględniony w pozycji kontraktu, a w przypadku, gdy kategorie transakcja zostanie skonfigurowana jako odpłatna w pozycji kontraktu.

| Uwzględnia czas | Uwzględnia wydatek | Rola | Kategoria | Zadanie |
| --- | --- | --- | --- | --- |
| Tak | Tak | Odpłatne | Odpłatne | Fakturowanie wartości rzeczywistej czas: Odpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Tak | Tak | Nieodpłatne | Odpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| Tak | Tak | Nieodpłatne | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: Nieodpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| No | Tak | Nie można ustawić | Odpłatne | Fakturowanie wartości rzeczywistej czas: Niedostępne </br>Typ fakturowania wartości rzeczywistej wydatku: Odpłatny |
| No | Tak | Nie można ustawić | Nieodpłatne | Fakturowanie wartości rzeczywistej czas: Niedostępne </br>Typ fakturowania wartości rzeczywistej wydatku: Nieodpłatny |
| Tak | No | Odpłatne | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Odpłatny </br>Typ fakturowania wartości rzeczywistej wydatku: Niedostępne |
| Tak | No | Nieodpłatne | Nie można ustawić | Fakturowanie wartości rzeczywistej czas: Nieodpłatny </br> Typ fakturowania wartości rzeczywistej wydatku: Niedostępne |
