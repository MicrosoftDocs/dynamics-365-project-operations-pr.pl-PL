---
title: Potwierdzenie faktury proforma - wersja uproszczona
description: Ten temat zawiera informacje na temat potwierdzania faktur proforma w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176534"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Potwierdzenie faktury proforma - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Po potwierdzeniu faktury pro forma stan faktury projektu ustawiony zostanie na **Potwierdzenie**. Po potwierdzeniu faktura staje się dostępna tylko w trybie do odczytu. Faktura może zostać skorygowana tylko wtedy, gdy istnieją zwroty lub kredytowanie zainicjowane przez klienta albo gdy faktura zostanie oznaczona jako zapłacona.

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
