---
title: Faktury korygujące oparte na projektach
description: W tym artykule przedstawiono informacje na temat sposobu tworzenia i potwierdzania faktur opartych na projekcie w aplikacji Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931113"
---
# <a name="corrective-project-based-invoices"></a>Faktury korygujące oparte na projektach

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Potwierdzona faktura projektu może być skorygowana w celu wprowadzenia zmian lub uznań, po uprzedniej zgodzie klienta i menedżera projektu.

Aby dokonać edycji potwierdzonej faktury, otwórz potwierdzoną fakturę i wybierz pozycję **Koryguj tę fakturę**. 

> [!NOTE]
> Ten wybór nie jest dostępny, chyba że faktura za projekt zostanie potwierdzona lub faktura oparta na projekcie zawiera zaliczki lub zaliczki lub uzgodnienia zaliczek lub zaliczek.

Nowa wersja robocza faktury jest tworzona na podstawie potwierdzonej faktury. Wszystkie szczegóły wiersza faktury z uprzednio potwierdzonej faktury zostaną skopiowane do nowej wersji roboczej. Oto niektóre z najważniejszych informacji na temat nowych wierszy korygowanych faktur:

- Wszystkie ilości są aktualizowane na zero. Dynamics 365 Project Operations zakłada, że wszystkie zafakturowane pozycje są w pełni zaksięgowane. Jeśli jest to konieczne, można ręcznie zaktualizować te ilości, tak aby odpowiadały ilości zafakturowanej, a nie uznanej ilości. W zależności od wprowadzonej ilości program obliczy uznaną zaksięgowaną kwotę. Ta kwota jest odzwierciedlona w wartościach rzeczywistych tworzonych podczas potwierdzania faktury korygującej. W przypadku wprowadzania zmian do kwoty podatku należy wprowadzić prawidłową kwotę podatku, a nie kwotę podatku, która ma być uznana.
- Korekta punktów kontrolnych jest zawsze przetwarzana jako pełne uznania.


> [!IMPORTANT]
> W przypadku szczegółów wiersza faktury, które są korektami innych już zafakturowanych opłat, pole **Korekta** ma ustawioną wartość **Tak**. W przypadku faktur, które mają skorygowane szczegóły wiersza faktury, pole **Ma korekty** ma ustawioną wartość **Tak**.

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
Ten scenariusz nie jest obsługiwany.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
