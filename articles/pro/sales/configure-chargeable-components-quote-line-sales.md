---
title: Konfigurowanie odpłatnych składników wiersza oferty
description: Ten temat zawiera informacje na temat konfigurowania odpłatnych i nieodpłatnych składników w wierszu oferty opartej na projekcie.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec8a999142fd9960c79ef981e499ae840642e57b269c83d201d2db006179de09
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995999"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurowanie odpłatnych składników wiersza oferty 

_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_

Pozycja oferty oparta na projekcie zawiera składniki typu *dołączane* i *odpłatne*.

Dołączone składniki są poddawane:

  - Podlegają podziałom metody fakturowania i klienta
  - Nieprzekraczalne limity 
  - Ustawienia częstotliwości faktur zdefiniowane w pozycji oferty opartej na projekcie

Podzbiór dołączonych składników można oznaczyć jako odpłatny przy użyciu pola **Typ fakturowania**. Pole **Typ fakturowania** jest zestawem opcji, który zezwala na korzystanie z następujących wartości w kontekście pozycji oferty:

  - Odpłatne
  - Nieodpłatne

Składniki odpłatne mogą być definiowane w zadaniach, rolach i kategoriach transakcji.

Opłata jest definiowana w zadaniach dla pozycji oferty projektu i stosowana do wszystkich klas transakcji zawartych w tym wierszu. Jeśli pole **Dołącz zadania** w wierszu kontraktu jest puste lub ustawione na wartość **Cały projekt**, karta **Zadania odpłatne** nie będzie dostępna.

Opłata zdefiniowana w rolach pozycji oferty, która ma zastosowanie tylko do klasy transakcji **Czas**. Jeśli pole **Dołącz czas** w wierszu oferty jest puste lub ustawione na wartość **Nie**, karta **Role odpłatne** nie będzie dostępna.

Opłata zdefiniowana w kategoriach transakcji pozycji oferty projektu ma zastosowanie tylko do klasy transakcji **Wydatek**. Jeśli pole **Dołącz wydatki** w wierszu oferty jest puste lub ustawione na wartość **Nie**, karta **Kategorie odpłatne** nie będzie dostępna.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie zadania projektu w stan odpłatny lub nieodpłatny

Zadanie projektu może być odpłatne lub niepłatne w ramach określonej pozycji oferty opartej na projekcie, co powoduje, że dostępne są następujące ustawienia.

Jeśli wiersz oferty opartej na projekcie zawiera **Czas** i zadanie **T1**, zadanie jest skojarzone z wierszem oferty jako odpłatne. Jeśli istnieje drugi wiersz oferty zawierający **Wydatki**, można skojarzyć zadanie **T1** w pozycji oferty jako nieodpłatne. W efekcie cały czas zanotowany dla zadania jest odpłatny, a wydatki zapisane w zadaniu nie.

Typ fakturowania zadania można skonfigurować na karcie **Odpłatne zadania** w pozycji oferty opartej na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Zadania wiersza oferty**. Alternatywnie możesz zaktualizować typ rozliczenia dla zadania projektu w polu **Typ fakturowania** w podsiatce w konfiguracji rozliczenia zadania projektu, która pokazuje wiersze oferty skojarzone z zadaniem.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie ról projektu jako odpłatnego lub niepłatnego

W kontekście określonego wiersza oferty opartej na projekcie rola może być odpłatna lub nieodpłatna.

Typ fakturowania roli można skonfigurować na karcie **Odpłatne role** w pozycji oferty na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Odpłatne role**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizowanie kategorii transakcji jako odpłatnej lub nie

Kategoria transakcji w danej pozycji oferty może być płatna lub nieodpłatna.

Typ fakturowania tranzakcji można skonfigurować na karcie **Odpłatne kategorie** w pozycji oferty na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Odpłatne kategorie**.

### <a name="resolve-chargeability"></a>Rozwiązywanie odpłatności
Wartość szacunkowa lub faktycznie utworzona dla czasu będzie uznana za wymagalną tylko wtedy, gdy:

   - **Czas** jest zawarty w wierszu oferty.
   - **Rola** jest skonfigurowana jako płatna w wierszu oferty.
   - Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty. 

Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest też skonfigurowane jako opłata. 

Szacunek lub wartość rzeczywista utworzona dla wydatku jest uważana za naliczaną tylko wtedy, gdy: 

   - **Wydatek** jest zawarty w wierszu oferty.
   - **Kategoria transakcji** jest skonfigurowana jako płatna w wierszu oferty.
   - Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.

Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest też skonfigurowane jako opłata. 

Wartość szacunkowa lub faktycznie utworzona dla materiału będzie uznana za wymagalną tylko wtedy, gdy:

   - **Materiały** sa zawarte w wierszu oferty.
   - Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.

Jeśli te dwie rzeczy zostaną spełnione, **Zadanie** powinno też być skonfigurowane jako opłata. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Uwzględnia czas</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Uwzględnia wydatek</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Uwzględnij materiały</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Uwzględnione zadania</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rola</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategoria</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Zadanie</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Wpływ opłaty</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Cały projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="70" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="70" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="70" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: <strong>Nieodpłatny</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: <strong> Nieodpłatny</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Cały projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Odpłatne</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Cały projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Cały projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="70" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Tak </p>
            </td>
            <td width="75" valign="top">
                <p>
Cały projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: Odpłatny </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Cały projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="70" valign="top">
                <p>
Odpłatne </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: Odpłatny </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Tak </p>
            </td>
            <td width="78" valign="top">
                <p>
Tak </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Cały projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nieodpłatne</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie można ustawić </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatne</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
