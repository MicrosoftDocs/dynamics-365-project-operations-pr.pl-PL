---
title: Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie
description: W tym temacie zamieszczono informacje dotyczące sposobu dodawania odpłatnych składników do pozycji kontraktu w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858486"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie

_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_

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

Szacunek lub wartość rzeczywista utworzona dla czasu jest uważana za naliczaną tylko wtedy, gdy:

   - **Czas** jest zawarty w wierszu kontraktu.
   - **Rola** jest skonfigurowana jako płatna w wierszu kontraktu.
   - Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu kontraktu.
 
 Jeśli te trzy rzeczy zostaną spełnione, zadanie jest skonfigurowane jako opłata. 

Szacunek lub wartość rzeczywista utworzona dla wydatku jest uważana za naliczaną tylko wtedy, gdy:

   - **Wydatek** jest zawarty w wierszu kontraktu
   - **Kategoria transakcji** jest skonfigurowana jako płatna w wierszu kontraktu
   - Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadanie** w wierszu kontraktu
  
 Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest skonfigurowane jako opłata. 

Szacunek lub wartość rzeczywista utworzona dla materiału jest uważana za naliczaną tylko wtedy, gdy:

   - **Materiał** jest zawarty w wierszu kontraktu
   - Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu kontraktu

Jeśli te dwie rzeczy zostaną spełnione, **Zadanie** jest skonfigurowane jako opłata. 

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
Fakturowanie wartości rzeczywistej czas: <strong>Odpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong>Odpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: <strong>Odpłatny</strong>
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
Fakturowanie wartości rzeczywistej czas: <strong>Odpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej wydatku: <strong>Odpłatny</strong>
                </p>
                <p>
Typ fakturowania wartości rzeczywistej materiału: <strong>Odpłatny</strong>
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
