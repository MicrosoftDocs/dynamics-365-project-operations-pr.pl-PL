---
title: Omówienie pozycji kontraktu opartego na projekcie
description: Ten temat zawiera informacje o pracy z pozycjami kontraktów opartych na projektach.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003149"
---
# <a name="project-based-contract-lines-overview"></a>Omówienie pozycji kontraktu opartego na projekcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Linie umowy oparte na projekcie w rozwiązaniu Dynamics 365 Project Operations są przeznaczone do przechowywania szacunkowych i rozliczeniowych umów dla określonych komponentów pracy projektowej na zlecenie. Struktura pozycji kontraktu opartej na projekcie jest rozszerzana na oszacowania projektów i scenariusze fakturowania przy użyciu następujących koncepcji:

- Metoda rozliczania
- Mapowanie projektów i zadań
- Dołączone klasy transakcji
- Nieprzekraczalny limit
- Konfiguracja odpłatności
- Oszacowania przy użyciu szczegółów pozycji kontraktu
- Klient pozycji kontraktu

Poniższa tabela zawiera pola na karcie **Ogólne** w wierszach kontraktu opartego na projektach, które pomagają w konfigurowaniu podstawy do szczegółowego oszacowania kosztów i sposobu fakturowania dla pracy opartej na projektach.

| Pole | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- |
| **Nazwa/nazwisko** | Nazwa pozycji kontraktu. To identyfikuje dyskretny składnik szacowanego kontraktu. W przypadku kontraktu projektu utworzonego z oferty ta wartość jest kopiowana z odpowiedniej wartości wiersza oferty opartej na projekcie. | Nazwa skopiowana do wiersza faktury projektu, który jest tworzony na podstawie tej pozycji kontraktu podczas tworzenia faktury. |
| **Metoda rozliczania** | W umowie dotyczącej projektu utworzonej na podstawie oferty ta wartość jest kopiowana z odpowiedniego pola w wierszu oferty. Jest to zestaw opcji reprezentujący dwa główne modele zamawiające, które są obsługiwane przez Project Operations:</br>- **Stała cena**</br>- **Czas i materiał** | Na podstawie metody fakturowania przywoływanego wiersza kontraktu zostanie przetworzona transakcja rzeczywista. Jeśli dana pozycja kontraktu zawiera metodę fakturowania czasu i materiału, tworzone są rekordy kosztów i niezafakturowanego rekordów sprzedaży. Jeśli pozycja kontraktu, do której odwołuje się wartość rzeczywista, ma metodę fakturowania z ceną ustaloną, zostanie utworzona tylko wartość rzeczywista kosztu. |
| **Project** | To pole służy do identyfikowania projektu, który będzie używany do dostarczania pracy nad tym zakontraktowaniem. | Ta wartość będzie używana w połączeniu z **Uwzględnionymi zadaniami** i **Uwzględnionymi klasami transakcji** w celu rozstrzygnięcia odniesienia do wiersza umowy w rzeczywistym lub szacunkowym rekordzie wiersza. |
| **Uwzględnione zadania** | Wskazuje, czy dana pozycja kontraktu obejmuje wszystkie zadania projektu dla wybranego projektu, czy tylko podzestaw zadań. To zestaw opcji o następujących możliwych wartościach:</br>- **Wszystkie zadania projektu**</br>- **Tylko wybrane zadania projektu**. Pusta wartość w tym polu jest równa zaznaczeniu **Wszystkich zadań projektu**. | Jeśli wybrano opcję **Tylko wybrane zadania**, można wybrać określone zadania i skojarzyć je z tym wierszem umowy na karcie **Konfiguracja rozliczania zadań** na stronie **Projekt**. Wartość jest używana w połączeniu z **Projekt** i **Uwzględnione klasy transakcji** w celu ustalenia odwołania do pozycji kontraktu w rekordzie rzeczywistym lub w wierszu szacowania. |
| **Uwzględnij czas** | Wartość **Tak**/**Nie** wskazuje, czy w tej kolejce kontraktu zostaną uwzględnione transakcje czasu lub koszty pracy dla wybranego projektu. Wartość **Nie** oznacza, że transakcje godzinowe lub koszt robocizny nie zostaną uwzględnione w tej pozycji kontraktu. Wartość **Tak** oznacza, że będą. | Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza. |
| **Uwzględnij wydatek** | Wartość **Tak**/**Nie** wskazuje, czy koszty związane z wybranym projektem zostaną uwzględnione w tej linii kontraktu. Wartość **Nie** oznacza, że koszt wydatków nie zostanie uwzględniony w tej pozycji kontraktu. Wartość **Tak** oznacza, że będzie. | Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza. |
| **Uwzględnij materiały** | Wartość **Tak**/**Nie** wskazuje, czy materiały związane z wybranym projektem zostaną uwzględnione w tej linii kontraktu. Wartość **Nie** oznacza, że koszty materiałów nie zostaną uwzględnione w tej linii kontraktu. Wartość **Tak** oznacza, że będzie. | Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza. |
| **Uwzględnij opłatę** | Wartość **Tak**/**Nie** wskazuje, czy opłaty związane z wybranym projektem zostaną uwzględnione w tej linii kontraktu. Wartość **Nie** oznacza, że opłaty nie będą uwzględnione w tej pozycji kontraktu. Wartość **Tak** oznacza, że będą. | Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza. |
| **Zakontraktowana kwota** | W pozycji kontraktu o stałej cenie jest to wartość ustalona, która zostanie zafakturowana klientowi dla wszystkich składników pracy skojarzonych z daną pozycją kontraktu. W pozycji umowy dotyczącej czasu i materiałów kwota ta jest szacunkową wartością tego, co zostanie zafakturowane klientowi za wszystkie składniki pracy związane z tą pozycją kontraktu. W umowie dotyczącej projektu utworzonej na podstawie oferty ta wartość jest kopiowana z odpowiedniego pola w wierszu oferty. Kiedy pozycja kontraktu oparta na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej we wszystkich pozycjach kontraktu. | W przypadku, gdy pozycja kontraktu zawiera szczegółowe informacje o wierszach, ta wartość może zostać zmodyfikowana, zmieniając kwoty w szczegółach wiersza. W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania kwoty przed podatkami dotyczącymi okresowych punktów kontrolnych rozliczania. |
| **Szacowany podatek** | Użytkownik może edytować to pole, aby wprowadzić szacowaną kwotę podatku w pozycji kontraktu. Kiedy pozycja kontraktu oparta na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane podatku od kwoty podanej we wszystkich pozycjach kontraktu. | W przypadku, gdy pozycja kontraktu zawiera szczegółowe informacje o wierszach, ta wartość może zostać zmodyfikowana, zmieniając kwoty podatku w szczegółach wiersza. W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania podatków dotyczących okresowych punktów kontrolnych rozliczania. |
| **Zakontraktowana kwota po opodatkowaniu** | Zakontraktowana kwota pozycji kontraktu po opodatkowaniu. To pole jest tylko do odczytu i jest obliczane jako **Kwota w kontrakcie + podatek**. | W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania okresowych punktów kontrolnych fakturowania. |
| **Nieprzekraczalny limit** | Użytkownik może edytować to pole, ale jest dostępne tylko w wierszach kontraktów opartych na projektach, które mają metodę fakturowania typu czas i materiały. | Użytkownik może edytować to pole. Kiedy rzeczywiste dane dotyczące czasu i materiałów odnoszą się do tej pozycji umowy pod względem czasu i materiałów, kwota rzeczywista jest oceniana w odniesieniu do nieprzekraczalnego limitu w linii umowy. Ta ocena jest przeprowadzana po rozpoczęciu już zrealizowanych i zakontraktowanych kwot. |
| **Budżet klienta** | To pole jest edytowalne i jest kopiowane z odpowiedniego pola w wierszu oferty, jeśli umowa została utworzona na podstawie oferty. | To pole jest używane tylko do informowania i nie ma żadnych elementów podrzędnych. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Reguły sprawdzania poprawności opcji na karcie Ogólne w wierszach kontraktu opartego na projektach

Reguła 1: Jeśli pole **Uwzględnione zadania** jest puste lub ustawione na **Wszystkie zadania projektu**, wszystkie zadania projektu są uwzględniane w wierszu umowy.

Reguła 2. Gdy pole **Uwzględnione zadania** jest puste lub jawnie ustawione na **Wszystkie zadania projektu**, projekt i określona klasa transakcji mogą być uwzględnione tylko w jednym wierszu kontraktu opartym na projekcie.

Reguła 3. Gdy pole **Uwzględnione zadania** ustawione na **Tylko wybrane zadania projektu**, projekt i określona klasa transakcji mogą być uwzględnione tylko w wielu wierszach kontraktu opartego na projekcie.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Kontrakt</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Pozycja kontraktu</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Uwzględnione zadania</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Uwzględnij czas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Uwzględnij wydatek</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>IUwzględnij materiały</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Uwzględnij</strong>
                </p>
                <p>
                    <strong>Opłata</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Prawidłowe/nieprawidłowe</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Przyczyna</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 2. Czas, koszt, materiały i opłaty w projekcie P1 są uwzględnione zarówno w wierszach kontraktu CL1, jak i w CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 2. Czas, materiały i opłaty w projekcie P1 są uwzględnione zarówno w wierszach kontraktu CL1, jak i w cl2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Prawidłowy </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Czas, materiały i opłaty w projekcie P1 są uwzględnione w CL1.
                </p>
                <ul>
                    <li>
Wydatki projektowe w ramach P1 są zawarte w CL2.
                    </li>
                </ul>
                <p>
Nie pokrywają się w tym, co jest zawarte w każdym wierszu kontraktu, a zatem jest ważne.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 2 </p>
                <p>
C1 obejmuje czas, materiały, wydatki i opłaty dla podzbioru zadań w projekcie P1.
                </p>
                <p>
CL2 obejmuje czas, materiały, wydatki i opłaty za cały projekt P1 i dlatego pokrywa się z tym, co jest zawarte w C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Prawidłowy </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Na regułę #3 </p>
                <p>
C1 obejmuje czas, wydatki, materiały i opłaty dla podzbioru zadań w projekcie P1.
                </p>
                <p>
CL2 obejmuje czas, wydatki, materiały i opłaty dla podzbioru zadań w projekcie P1.
                </p>
                <p>
Jedyna dodatkowa weryfikacja dotyczy podzbioru zadań w CL1 różni się od podzbioru zadań w CL2, aby upewnić się, że nie ma tam nakładania się. Jest to wykonywane przez system podczas kojarzenia zadań.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="48" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
            <td width="42" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
