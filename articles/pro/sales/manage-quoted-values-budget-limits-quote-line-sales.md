---
title: Omówienie wierszy oferty opartej na projekcie
description: Ten temat zawiera informacje o korzystaniu z wiersza oferty opartej na projekcie w pracy projektowej.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a9661d9b91ffeece4c66b129846632b30ebebc8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591095"
---
# <a name="project-based-quote-lines-overview"></a>Omówienie wierszy oferty opartej na projekcie 

_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_

Wiersze oferty opartej na projekcie są utworzone w celu ułatwienia oceny pracy nad projektem w momencie zakontraktowania. Struktura wiersza oferty opartej na projekcie jest przedłużana na potrzeby oszacowań projektu z następującymi pojęciami:

- Metoda rozliczania
- Mapowanie projektów i zadań
- Dołączone klasy transakcji
- Nieprzekraczalny limit
- Konfiguracja odpłatności
- Szacowanie przy użyciu szczegółów wiersza oferty
- Klienci wierszy oferty

Poniższa tabela zawiera informacje o polach na karcie **Ogólne** w wierszu oferty opartej na projekcie. Te pola pomagają skonfigurować podstawę dla konkretnego szacunkowego oszacowania pracy projektowej.

| **Pole** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- |
| Nazwa/nazwisko | Nazwa wiersza oferty, która pomaga zidentyfikować dyskretny składnik wyceny, która jest szacowana. | Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu. |
| Metoda rozliczania | Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola w szansie sprzedaży. To pole obejmuje dwa główne modele kontraktów obsługiwane przez Dynamics 365 Project Operations:</br>- Stała cena</br>- Czas i materiał.| Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Project | Użyj tego opcjonalnego pola w celu zidentyfikowania projektu, który będzie używany do dostarczania pracy w ramach tego zakontraktowania. Podczas mapowania projektu na wiersz oferty pomocne jest konfigurowanie zadań odpłatnych, a także wprowadzenie oceny opartej na projekcie z wiersza oferty jako szczegółów wiersza oferty. Jeśli projekt nie jest mapowany na wiersz oferty opartej na projekcie, szacunek powinien zostać utworzony ręcznie, tworząc szczegóły poszczególnych wierszy oferty. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.|
| Uwzględnione zadania | Wskazuje, czy dany wiersz oferty jest używany we wszystkich zadaniach wybranego projektu. To pole ma następujące wartości:</br>- Wszystkie zadania projektu</br>- Tylko wybrane zadania projektu</br>W tym polu jest wyświetlona pusta wartość, która jest równoznaczna z opcją **Wszystkie zadania projektu**. | Gdy wybrana jest opcja **Tylko wybrane zadania projektu** na stronie projektu, karta **Konfiguracja rozliczania zadań** umożliwia wybranie określonych zadań w celu skojarzenia ich z tym wierszem oferty. Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Uwzględnij czas | Wartość **Tak**/**Nie** wskazuje, czy transakcje czasowe lub koszty pracy w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty. Flaga **Nie** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Tak** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Uwzględnij wydatek | Wartość **Tak**/**Nie** wskazuje, czy wydatki w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty. Flaga **Nie** wskazuje, że koszty wydatków w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Flaga **Tak** wskazuje, że koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Uwzględnij materiał | Wartość **Tak**/**Nie** wskazuje, czy materiały w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty. Wartość **Nie** oznacza, że koszty materiałów nie zostaną uwzględnione w szacunkach w tym wierszu oferty. Wartość **Tak** oznacza, że koszty materiałów zostaną uwzględnione w szacunkach w tym wierszu oferty. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Uwzględnij opłatę | Wartość **Tak**/**Nie** wskazuje, czy opłaty w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty. Wartość **Nie** wskazuje, że opłaty w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty. Wartość **Tak** wskazuje, że opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Oferowana kwota | Jest to kwota, która zostanie podana klientowi za całą pracę prognozowaną w tym wierszu oferty opartym na projekcie. Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola **Budżet klienta** w szansie sprzedaży. Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej w wierszu oferty. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Szacowany podatek | Jest to pole, które można edytować, aby dodać szacowaną kwotę podatku w wierszu oferty. Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podatku podanej w wierszu oferty. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Oferowana kwota po opodatkowaniu | To pole stanowi kwotę wiersza oferty po zaliczeniu podatku i jest w trybie tylko do odczytu. Kwota w tym polu jest obliczana jako *Oferowana kwota z podatkiem*. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Nieprzekraczalny limit | To pole można edytować i jest dostępne tylko w wierszach oferty opartej na projekcie z metodą rozliczania **Czas i amteriał**. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |
| Budżet klienta | Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży. | Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Reguły sprawdzania poprawności dla pól na karcie Ogólne w wierszach oferty opartej na projektach

**Reguła 1**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli jest ustawione na **Wszystkie zadania projektu**, projekt jest uwzględniany w wierszu oferty.

**Reguła 2**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli ustawiono je na **Wszystkie zadania projektu**, projekt i dana klasa transakcji mogą być uwzględnione tylko w jednym wierszu oferty opartej na projekcie w ofercie.

**Reguła 3**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli ustawiono je na **Tylko wybrane zadania projektu**, projekt i dana klasa transakcji mogą być uwzględnione w wielu wierszach oferty opartej na projekcie w ofercie.

**Reguła 4**: Jeśli szansa sprzedaży zawiera wiele ofert, między różnymi ofertami można odwoływać się do tego samego projektu i zawierać tę samą klasę transakcji.

**Zasada 5**: Jeśli oferty nie należą do tej samej szansy sprzedaży, nie mogą zawierać tej samej klasy projektów i transakcji.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Szansa sprzedaży</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Oferta</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Wiersz oferty</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Uwzględnione zadania</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Uwzględnij czas</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Uwzględnij wydatek</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Uwzględnij materiał</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Uwzględnij</strong>
                </p>
                <p>
                    <strong>Opłata</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Prawidłowe/nieprawidłowe</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Przyczyna</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 2. Czas, wydatek i opłaty w projekcie P1 są uwzględniane w wierszach oferty QL1, jak i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Nie. </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 2. Czas, materiał i opłaty w projekcie P1 są uwzględniane w wierszach oferty QL1, jak i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Nie. </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Prawidłowy </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Czas, materiał i opłaty w projekcie P1 są uwzględnione w QL1 <br>
Wydatki projektowe w ramach P1 są zawarte w QL2 <br>
Nie pokrywają się w tym, co jest zawarte w każdym wierszu oferty, a zatem jest ważne.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="45" valign="top">
                <p>
Nie. </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Nie. </p>
            </td>
            <td width="41" valign="top">
                <p>
Nie. </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Naruszenie reguły nr 2 </p>
                <p>
Q1 obejmuje czas, materiał, wydatki i opłaty dla podzbioru zadań w projekcie P1 </p>
                <p>
QL2 obejmuje czas, wydatki i opłaty za cały projekt P1, a zatem pokrywa się z tym, co jest uwzględnione w pierwszym kwartale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pusty </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Prawidłowy </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Na regułę #3, </p>
                <p>
Q1 obejmuje czas, materiał, wydatki i opłaty dla podzbioru zadań w projekcie P1.
                </p>
                <p>
QL2 obejmuje czas, materiały, wydatki i opłaty dla podzbioru zadań w projekcie P1.
                </p>
                <p>
Jedyna dodatkowa walidacja dotyczy podzbioru zadań na QL1, który różni się od podzbioru zadań na QL2, aby upewnić się, że nie nakładają się na siebie. Jest to wykonywane przez system podczas kojarzenia zadań.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tylko wybrane zadania </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Wszystkie zadania projektu lub puste </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Prawidłowy </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Zgodnie z regułą # 5, Q1 i Q2 to dwie oferty dotyczące tej samej możliwości, więc obie mogą szacować te same komponenty projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Wszystkie zadania projektu lub puste </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Wszystkie zadania projektu lub puste </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nieprawidłowe </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Zgodnie z regułą # 4, Q1 i Q2 to dwie wyceny różnych możliwości, więc nie mogą oszacować tych samych komponentów tego samego projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Wszystkie zadania projektu lub puste </p>
            </td>
            <td width="45" valign="top">
                <p>
Tak </p>
            </td>
            <td width="46" valign="top">
                <p>
Tak </p>
            </td>
            <td width="43" valign="top">
                <p>
Tak </p>
            </td>
            <td width="41" valign="top">
                <p>
Tak </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
