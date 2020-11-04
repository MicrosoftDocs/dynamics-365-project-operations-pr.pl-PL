---
title: Kredyty i korekty faktur
description: Ta temat zawiera informacje na temat pracy korekt faktur w Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082123"
---
# <a name="credits-and-corrected-invoices"></a>Kredyty i korekty faktur

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
> Szczegóły wierszy faktury, które są korektą do innych zafakturowanych opłat, mają w polu **Korektę** ustawioną wartość **Tak**. Na fakturach, dla których istnieją poprawione dane w wierszu faktury znajduje się pole **Wprowadzono korektę** , która ma również ustawioną wartość na **Tak**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Wartości rzeczywiste utworzone w potwierdzeniu faktury korygującej:

Poniżej znajdują się wartości rzeczywiste, które zostały utworzone przez aplikację na bazie korekty na podstawie operacji wykonywanych na wersji roboczej faktury korygującej przed jej potwierdzeniem.

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
Faktura punktu kontrolnego lub status fakturowania w pozycji kontraktu projektu są aktualizowane na **Gotowe do fakturowania**.
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
