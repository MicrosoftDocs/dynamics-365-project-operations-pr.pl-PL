---
title: Faktury korygujące za projekty
description: Ten temat zawiera informacje o tym, jak tworzyć i potwierdzać faktury korygujące w Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cec77f22dd52e15c9fb61b7acc0bd3e633f119b96d7958af021e4dce977140a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009544"
---
# <a name="corrective-project-invoices"></a>Faktury korygujące za projekty

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Potwierdzona faktura projektu może być skorygowana w celu wprowadzenia zmian lub uznań, po uprzedniej zgodzie klienta i menedżera projektu.

Aby dokonać edycji potwierdzonej faktury, otwórz potwierdzoną fakturę i wybierz pozycję **Koryguj tę fakturę**. 

> [!NOTE]
> Ta opcja jest niedostępna, jeśli nie została potwierdzona faktura projektu.

Nowa wersja robocza faktury jest tworzona na podstawie potwierdzonej faktury. Wszystkie szczegóły wiersza faktury z uprzednio potwierdzonej faktury zostaną skopiowane do nowej wersji roboczej. Oto niektóre z najważniejszych informacji na temat nowych wierszy korygowanych faktur:

- Wszystkie ilości są aktualizowane na zero. Aplikacja zakłada, że wszystkie zafakturowane towary są całkowicie uznane. Jeśli jest to konieczne, można ręcznie zaktualizować te ilości, tak aby odpowiadały ilości zafakturowanej, a nie uznanej ilości. W zależności od wprowadzonej ilości program obliczy uznaną zaksięgowaną kwotę. Ta kwota jest odzwierciedlona w wartościach rzeczywistych tworzonych podczas potwierdzania faktury korygującej. W przypadku wprowadzania zmian do kwoty podatku należy wprowadzić prawidłową kwotę podatku, a nie kwotę podatku, która ma być uznana.
- Poprzednio potwierdzone pozycje kontraktu opartego na produktach nie są kopiowane. Przetwarzanie korekt na fakturze projektu opartej na produkcie nie jest obsługiwane.
- Korekta punktów kontrolnych jest zawsze przetwarzana jako pełne uznania.
- Jeśli klient został zafakturowany na nieprawidłową kwotę, można skorygować zatrzymanie lub zaliczkę.
- Uzgodnienia dotyczące zatrzymań i zaliczek można skorygować, jeśli do uzgodnienia została użyta nieprawidłowa kwota względem opłat na poprzednio potwierdzonej fakturze zastosowano nieprawidłową kwotę.

> [!IMPORTANT]
> Szczegóły wierszy faktury, które są korektą do innych zafakturowanych opłat, mają w polu **Korektę** ustawioną wartość **Tak**. Na fakturach, dla których istnieją poprawione dane w wierszu faktury znajduje się pole **Wprowadzono korektę**, która ma również ustawioną wartość na **Tak**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Wartości rzeczywiste tworzone po potwierdzeniu faktury korygującej

W poniższej tabeli przedstawiono wartości rzeczywiste, które są tworzone po potwierdzenia faktury korekcyjnej.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenariusz</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Wartości rzeczywiste utworzone przy potwierdzeniu</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potwierdź korektę zafakturowanego zatrzymania lub zaliczki.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia. Ta kwota jest dodatnia, ponieważ powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie zafakturowania zatrzymania lub zaliczki.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Wartość rzeczywista wycofanych wyliczonych sprzedaży jest tworzona dla kwoty zaliczki lub zatrzymania, w celu wycofania pierwotnej zafakturowanej sprzedaży.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Tworzona jest nowa wartość rzeczywista zafakturowanej sprzedaży w korygowanym wierszu faktury opartym na zaliczce lub zatrzymaniu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Niezafakturowana wartość sprzedaży negatywnej wartości rzeczywistej wiersza faktury opartego na zaliczce lub zatrzymaniu, która ma być używana do uzgadniania.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potwierdzenie korekty wcześniej uzgodnionej zaliczki lub zatrzymania.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia. Ta kwota jest dodatnia i powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie poprzedniego uzgodnienia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rzeczywiste rozliczone wycofanie wartości sprzedaży za ilość znajdującą się na poprzedniej fakturze.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stosowana jest nowa rozliczona wartość rzeczywista w korygowanym wierszu faktury opartym na zaliczce lub zatrzymaniu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Niezafakturowana wartość sprzedaży o negatywnej wartości rzeczywistej ze skorygowanych pozostałych zaliczek lub zatrzymań, która ma być używana na późniejszych fakturach.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji czasowej.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rozliczona sprzedaż za godziny i kwotę z oryginalnego wiersza faktury dla czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona wartość rzeczywista sprzedaży za godziny i kwotę z oryginalnego wiersza faktury dla czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturowanie częściowego uznania transakcji czasu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rozliczona sprzedaż za godziny i kwotę z oryginalnego fakturowanego wiersza faktury dla czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna względem godzin i kwoty w edytowanym wierszu faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą liczbę godzin i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji wydatkowej.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji wydatkowej.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rozliczone wycofanie sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z korygowanego wiersza faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą ilość i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie pełnego kredytu z poprzednio zafakturowanej transakcji materiałowej.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturowane wycofanie sprzedaży dla ilości i kwoty w szczegółach wiersza oryginalnej faktury dla materiału.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa niezafakturowana sprzedaż rzeczywista dla ilości i kwoty w szczegółach wiersza oryginalnej faktury dla materiału.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturowanie częściowego kredytu przy istotnej transakcji.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie sprzedaży zafakturowanej dla ilości i kwoty zafakturowanej dla szczegółów wiersza oryginalnej faktury dla materiału.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa niezafakturowana rzeczywista sprzedaż, która jest obciążana za ilość i kwotę w edytowanych szczegółach wiersza faktury, ich odwrócenie i równoważna faktyczna fakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą ilość i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji opłaty.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji opłaty.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury opłaty.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z wiersza faktury korygującej, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Zafakturowanie pełnego uznania uprzednio zafakturowanego punktu kontrolnego.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rozliczona sprzedaż za kwotę z oryginalnego wiersza faktury dla punktu kontrolnego.
                </p>
                <p>
Stan faktury w punktów kontrolnych jest aktualizowany z <b>Zaksięgowano fakturę dla klienta</b> do <b>Przygotowane do fakturowania</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Zafakturowanie częściowego uznania uprzednio zafakturowanego punktu kontrolnego.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nieobsługiwane </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Uznania i korekty poprzednio zafakturowanego wiersza kontraktu opartego na produkcie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nieobsługiwane </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
