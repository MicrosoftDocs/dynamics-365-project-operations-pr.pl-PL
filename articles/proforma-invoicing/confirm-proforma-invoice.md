---
title: Potwierdzenie faktury proforma opartej na projekcie
description: Ten temat zawiera informacje na temat potwierdzania faktury opartej na projekcie proforma.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867144"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Potwierdzenie faktury proforma opartej na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Po potwierdzeniu faktury pro forma stan faktury projektu ustawiony zostanie na **Potwierdzenie**. Po potwierdzeniu faktura staje się dostępna tylko w trybie do odczytu. Odtąd fakturę można skorygować tylko wtedy, gdy występują jakiekolwiek korekty lub uznanie zainicjowane przez klienta.

Poniższa tabela zawiera listę wartości rzeczywistych tworzonych przez system. Te wartości rzeczywiste są tworzone przy wykonywaniu pewnych operacji na wersji roboczej faktury projektu przed jej potwierdzeniem.

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
Fakturowanie płatności opartej na zatrzymaniu lub zaliczce </p>
            </td>
            <td width="408" valign="top">
                <p>
Wartość rzeczywista sprzedaży fakturowanej typu <strong>Zatrzymanie</strong>, tworzony dla zaliczki lub zatrzymania.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Niezafakturowana sprzedaż rzeczywista z ujemną kwotą zaliczki lub zaliczki do wykorzystania w celu uzgodnienia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Po pełnym uzgodnieniu z zamówieniem lub zaliczką na fakturze.
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
Rzeczywista rozliczona wartość sprzedaży za ilość znajdującą się na tej fakturze.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Po częściowym uzgodnieniu z zamówieniem lub zaliczką na fakturze.
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
Rzeczywista rozliczona wartość sprzedaży za ilość znajdującą się na tej fakturze.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Kwota ujemna nierozliczonej sprzedaży pozostałej zaliczki lub zatrzymania, która zostanie użyta podczas uzgodnienia na przyszłych fakturach.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie transakcji czasowej bez żadnych zmian w stosunku do wersji roboczej faktury.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Wycofanie rozliczonej kwoty rzeczywistej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturowanie transakcji godzinowej, która została edytowana w celu zmniejszenia ilości.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu godzin i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa niezafakturowana rzeczywista sprzedaż, która nie podlega opłacie za pozostałe godziny i kwotę po odjęciu skorygowanych liczb w edytowanych szczegółach wiersza faktury, odwróceniu faktycznej sprzedaży i równoważnej fakturowanej sprzedaży.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie transakcji godzinowej, która została edytowana w celu zwiększenia ilości.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu godzin i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie transakcji wydatkowej bez żadnych zmian w stosunku do wersji roboczej faktury.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rozliczona wartość rzeczywista sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturowanie transakcji wydatkowej, która została edytowana w celu zmniejszenia ilości.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałej ilości i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie transakcji wydatkowej, która została edytowana w celu zwiększenia ilości.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie istotnej transakcji bez żadnych zmian w wersji roboczej faktury.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Niezafakturowane wycofanie sprzedaży dla ilości i kwoty w pierwotnym zatwierdzeniu wykorzystania materiału.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Faktyczna sprzedaż zafakturowana dla ilości i kwoty na pierwotnym zatwierdzeniu wykorzystania materiału.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturowanie transakcji materiałowej, która została edytowana w celu zmniejszenia ilości.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Niezafakturowane wycofanie sprzedaży dla ilości i kwoty w pierwotnym zatwierdzeniu czasu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałej ilości i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie transakcji materiałowej, która została edytowana w celu zwiększenia ilości.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Niezafakturowane wycofanie sprzedaży dla ilości i kwoty w pierwotnym zatwierdzeniu wykorzystania materiału.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturowanie opłaty.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Wycofanie nierozliczonej sprzedaży za kwotę opłaty w oryginalnym wierszu arkusza.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rozliczona wartość rzeczywista sprzedaży za ilość i kwotę w oryginalnym wierszu arkusza opłaty.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Wystawianie fakturowania punktów kontrolnych.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rozliczona rzeczywista sprzedaż dla kwoty punktów kontrolnych w oryginalnym punktach kontrolnych pozycji kontraktu projektu.
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
