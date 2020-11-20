---
title: Omówienie wierszy oferty opartej na projekcie
description: Ten temat zawiera informacje o korzystaniu z wiersza oferty opartej na projekcie w pracy projektowej.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181870"
---
# <a name="project-based-quote-lines-overview"></a>Omówienie wierszy oferty opartej na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Wiersze oferty opartej na projekcie są utworzone w celu ułatwienia oceny pracy nad projektem w momencie zakontraktowania. Struktura wiersza oferty opartej na projekcie jest przedłużana na potrzeby oszacowań projektu z następującymi pojęciami:

- Metoda rozliczania
- Mapowanie projektu
- Dołączone klasy transakcji
- Nieprzekraczalny limit
- Konfiguracja odpłatności
- Szacowanie przy użyciu szczegółów wiersza oferty
- Klienci wierszy oferty

Poniższa tabela zawiera informacje o polach na karcie **Ogólne** w wierszu oferty opartej na projekcie. Te pola pomagają skonfigurować podstawę dla konkretnego szacunkowego oszacowania pracy projektowej.

| **Pole** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- |
| Nazwa/nazwisko | Nazwa wiersza oferty, która ułatwia identyfikację oddzielnego komponentu szacowanego w ramach danej oferty. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Metoda rozliczania | Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola w szansie sprzedaży. To pole zawiera dwa główne projekty, które są obsługiwane przez Dynamics 365 Project Operations:</br>- Stała cena</br>- Czas i materiał.| Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Project | Użyj tego opcjonalnego pola w celu zidentyfikowania projektu, który będzie używany do dostarczania pracy w ramach tego zakontraktowania. Podczas mapowania projektu na wiersz oferty pomocne jest konfigurowanie zadań odpłatnych, a także wprowadzenie oceny opartej na projekcie z wiersza oferty jako szczegółów wiersza oferty. Jeśli projekt nie jest mapowany na wiersz oferty opartej na projekcie, szacunek powinien zostać utworzony ręcznie, tworząc szczegóły poszczególnych wierszy oferty. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Uwzględnij czas | Flaga **Tak**/**Nie** wskazuje, czy transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Nie** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Tak** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Uwzględnij wydatek | Flaga **Tak**/**Nie** wskazuje, czy koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Nie** wskazuje, że koszty wydatków w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Tak** wskazuje, że koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Uwzględnij opłatę | Flaga **Tak**/**Nie** wskazuje, czy opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Nie** wskazuje, że opłaty w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Tak** wskazuje, że opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Oferowana kwota | Jest to kwota, która zostanie zaoferowana klientowi dla wszystkich prognozowanych prac w wierszu oferty opartej na projekcie. Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola **Budżet klienta** w szansie sprzedaży. Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej w wierszu oferty. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Szacowany podatek | Jest to pole, które można edytować, aby dodać szacowaną kwotę podatku w wierszu oferty. Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podatku podanej w wierszu oferty. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Oferowana kwota po opodatkowaniu | To pole stanowi kwotę wiersza oferty po zaliczeniu podatku i jest w trybie tylko do odczytu. Kwota w tym polu jest obliczana jako *Oferowana kwota z podatkiem*. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Nieprzekraczalny limit | To pole można edytować i jest dostępne tylko w wierszach oferty opartej na projekcie z metodą rozliczania **Czas i amteriał**. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Budżet klienta | Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Reguły sprawdzania poprawności dla pól na karcie Ogólne w wierszach oferty opartej na projektach

**Reguła 1**: dana klasa transakcji w wybranym projekcie może być uwzględniona tylko w jednym wierszu oferty opartej na projekcie oferty.

**Reguła 2**: Jeśli szansa sprzedaży zawiera wiele ofert, między różnymi ofertami można odwoływać się do tego samego projektu i zawierać tę samą klasę transakcji.

**Zasada 3**: Jeśli oferty nie należą do tej samej szansy sprzedaży, nie mogą zawierać tej samej klasy projektów i transakcji.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Szansa sprzedaży</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Oferta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Wiersz oferty</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
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
                    <strong>Dołącz</strong>
                </p>
                <p>
                    <strong>opłata</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Prawidłowe/nieprawidłowe</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Przyczyna</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 1. Czas, wydatek i opłaty w projekcie P1 są uwzględniane zarówno w wierszach oferty, QL1, jak i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 1. Czas i opłaty w projekcie P1 są uwzględniane zarówno w wierszach oferty, QL1, jak i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Prawidłowe </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Godziny i opłaty z projektu P1 są zawarte w QL1.
Wydatki projektowe w ramach P1 są zawarte w QL2.
W żadnym wierszu oferty nie ma nakładania się wartości, więc wszystko jest poprawne.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 1 powyżej </p>
                <p>
Q1 zawiera czas, koszty i opłaty dla całego projektu P1.
                </p>
                <p>
QL2 zawiera czas, wydatki i opłaty dla całego projektu P1 i pokrywa się ze składnikiem, który został zamieszczony w Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" valign="top">
                <p>
Prawidłowe </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na podstawie reguły nr 2, Q1 i Q2 to dwie oferty z tej samej szansy sprzedaży, przez co obydwa te elementy mogą szacować dla tych samych składników projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 do Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" valign="top">
                <p>
Prawidłowe </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na podstawie reguły nr 3, Q1 i Q2 to dwie oferty z różnych szans sprzedaży, przez co obydwa te elementy nie mogą szacować dla tych samych składników projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
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
            <td width="54" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
        </tr>
    </tbody>
</table>

