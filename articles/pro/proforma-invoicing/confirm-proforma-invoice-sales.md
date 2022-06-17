---
title: Potwierdzenie faktury proforma projektu
description: W tym artykule przedstawiono informacje na temat potwierdzania faktur proforma dla projektu w aplikacji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 101e4564fcf57cbbfc713773ed760291b9d28410
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922235"
---
# <a name="confirm-a-proforma-project-invoice"></a>Potwierdzenie faktury proforma projektu 

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


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
Niewykorzystana wartość sprzedaży niepodlegającej kwocie ujemnej zatrzymania lub wcześniejszej, która ma być używana do uzgadniania.
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
Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałych godzin i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.
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
Rozliczona wartość rzeczywista sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Fakturowanie pozycji kontraktu opartych na produkcie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rozliczona wartość rzeczywista za wiersz produktu wraz z ilością i kwotą przychodzącą z pozycji kontraktu opartej na produkcie.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
