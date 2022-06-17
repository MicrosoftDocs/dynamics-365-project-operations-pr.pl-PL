---
title: Konfigurowanie odpłatnych składników wiersza oferty opartej na projekcie
description: W tym artykule przedstawiono informacje na temat konfigurowania składników uwzględnionych, odpłatnych i nieodpłatnych w wierszach oferty opartych na projekcie.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff409132ef9103641578f9c94f8ea1ff56738a71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915565"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurowanie odpłatnych składników wiersza oferty opartej na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Wiersz oferty opartej na projekcie może mieć składniki dołączone i składniki odpłatne.

Składniki dołączone podlegają ustawieniom metody fakturowania, podziałów klientów, nieprzekraczalnych limitów i częstotliwości faktur, które zdefiniowano w wierszu oferty opartej na projekcie.
Podzestaw składników dołączonych można oznaczyć jako odpłatny, korzystając z opcji **Typ fakturowania**. W polu **Typ fakturowania** można wybrać jedną z następujących opcji w kontekście wiersza oferty:

   - Odpłatne
   - Nieodpłatne

Składniki odpłatne mogą być definiowane w rolach i kategoriach transakcji.

Odpłatność definiowana w rolach w wierszu oferty projektu ma zastosowanie tylko do klasy transakcji **Czas**. Jeśli wiersz oferty projektu ma ustawienie **Uwzględnij czas** = **Nie**, karta **Odpłatne role** jest niedostępna.

Odpłatność definiowana w kategoriach transakcji w wierszu oferty projektu ma zastosowanie tylko do klasy transakcji **Wydatek**. Jeśli wiersz oferty projektu ma ustawienie **Uwzględnij wydatki** = **Nie**, karta **Odpłatne kategorie** jest niedostępna.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie ról projektu jako odpłatnego lub niepłatnego
Rola może być odpłatna lub nieodpłatna w wierszy oferty opartej na projekcie. Typ fakturowania dla roli można skonfigurować na karcie **Odpłatne role** wiersza oferty opartej na projekcie. W tym celu należy zaktualizować **typ fakturowania** w podsiatce **Odpłatne role**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie kategorii transakcji jako odpłatnej lub nie
Kategoria transakcji może być odpłatna lub nieodpłatna w wierszy oferty opartej na projekcie. Typ fakturowania dla transakcji można skonfigurować na karcie **Odpłatne kategorie** wiersza oferty opartej na projekcie. W tym celu należy zaktualizować pole **Typ fakturowania** w podsiatce **Kategorie płatne**. 

## <a name="resolve-chargeability"></a>Rozwiązywanie odpłatności

Wartość szacowana lub rzeczywista utworzona dla czasu będzie traktowana jako odpłatna wyłącznie w sytuacji, gdy czas jest uwzględniany w wierszu oferty, a rola jest konfigurowana jako odpłatna.
Wartość szacowana lub rzeczywista utworzona dla wydatku będzie traktowana jako odpłatna wyłącznie w sytuacji, gdy wydatek jest uwzględniany w wierszu oferty, a kategoria transakcji jest konfigurowana jako odpłatna w wierszu oferty. W poniższej tabeli pokazano ustawienia domyślne odpłatności dla poszczególnych wartości rzeczywistych. Wartości domyślne opierają się na składnikach dołączonych i typie fakturowania skonfigurowanym w wierszu oferty.

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