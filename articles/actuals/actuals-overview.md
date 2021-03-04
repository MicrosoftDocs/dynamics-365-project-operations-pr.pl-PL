---
title: Wartości rzeczywiste
description: Ten temat zawiera informacje na temat pracy z wartościami rzeczywistymi w Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126326"
---
# <a name="actuals"></a>Wartości rzeczywiste 

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Wartości rzeczywiste określają ilość pracy wykonanej w projekcie. Są one tworzone w wyniku zapisów czasu i wydatku oraz pozycji dziennika i faktur.

## <a name="journal-lines-and-time-submission"></a>Wiersze arkusza i przesyłanie czasu

Aby uzyskać więcej informacji o wprowadzaniu godziny, zobacz temat [Przegląd wpisów czasu](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Rozliczanie według czasu i materiałów

W przypadku połączenia przesłanego wpisu czasu do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.

### <a name="fixed-price"></a>Stała cena

Podczas przesyłania wpisu czasu dla projektu, który jest połączony z projektem zamapowanym do kontraktu o stałej cenie, system tworzy tylko wiersz arkusza dotyczący kosztu.

### <a name="default-pricing"></a>Cena domyślna

Logika tworzenia cen domyślnych jest przechowywana w wierszu arkusza. Wartości pól z wpisu czasu są kopiowane do wiersza arkusza. Te wartości zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.

Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka organizacyjna**, są wykorzystywane do domyślnego wprowadzenia właściwej ceny w wierszu arkusza. We wpisie czasu można dodać pole niestandardowe. Chcąc przetworzyć wartość do wartości rzeczywistych, należy utworzyć pole w encji Wartości rzeczywiste, a następnie za pomocą mapowań pól skopiować pole z wpisu czasu do wartości rzeczywistej.

## <a name="journal-lines-and-basic-expense-submission"></a>Wiersze arkusza i przesyłanie podstawowych kosztów

Aby uzyskać więcej informacji o wprowadzaniu wydatków, zobacz temat [Przegląd wydatków](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Rozliczanie według czasu i materiałów

W przypadku połączenia przesłanego wpisu wydatku podstawowego do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.

### <a name="fixed-price"></a>Stała cena

Podczas przesyłania wpisu podstawowego wydatku dla projektu, który jest połączony z projektem zamapowanym do kontraktu o stałej cenie, system tworzy tylko wiersz arkusza dotyczący kosztu.

### <a name="default-pricing"></a>Cena domyślna

Logika wprowadzania cen domyślnych wydatków jest oparta na kategorii wydatków. Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty. Jednak domyślnie kwota wprowadzona przez użytkownika dla ceny jest ustawiana bezpośrednio w odpowiednich wierszach arkusza wydatków dla kosztów i sprzedaży.

We wpisach wydatków nie można wprowadzać domyślnych cen jednostkowych opartych na kategoriach.

## <a name="use-entry-journals-to-record-costs"></a>Używanie dzienników do rejestrowania kosztów

Arkusze umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych. Arkusze mogą być używane w produkcji.

- Rejestrowania rzeczywistych kosztów materiałów i wielkości sprzedaży w projekcie.
- Przeniesienia wartości rzeczywistych transakcji z innego systemu do Microsoft Dynamics 365 Project Operations.
- Zarejestrowania kosztów, które wystąpiły w innym systemie. Koszty te mogą zawierać koszty zakupu lub podwykonawców.

> [!IMPORTANT]
> Aplikacja nie sprawdza poprawności typu wiersza arkusza lub powiązanej kalkulacji cen wprowadzonych w wierszu dziennika. Z tego powodu tylko użytkownik, który jest w pełni świadomi skutków związanych z księgowaniem w projekcie powinien używać dzienników wpisów do tworzenia wartości rzeczywistych. Ze względu na wpływ danego typu arkusza należy starannie wybrać osoby, które mają mieć dostęp do tworzenia arkuszy zapisu.
## <a name="record-actuals-based-on-project-events"></a>Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu

Project Operations rejestruje transakcje finansowe zaistniałe w trakcie projektu. Te transakcje są zapisywane jako wartości rzeczywiste. W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu

<table>
<thead>
<tr>
<th rowspan="3">Zdarzenie</th>
<th colspan="4">Projekt do rozliczenia lub sprzedany</th>
<th rowspan="3">Projekt na etapie przedsprzedaży</th>
<th rowspan="3">Projekt wewnętrzny</th>
</tr>
<tr>
<th colspan="2">Rozliczanie według czasu i materiałów</th>
<th colspan="2">Stała cena</th>
</tr>
<tr>
<th>Wartości rzeczywiste</th>
<th>Waluta transakcji</th>
<th>Stała cena</th>
<th>Waluta transakcji</th>
</tr>
</thead>
<tbody>
<tr>
<td>Jest tworzony wpis czasu.</td>
<td colspan="6">Brak działania w encji Wartości rzeczywiste</td>
</tr>
<tr>
<td>Jest przesyłany wpis czasu.</td>
<td colspan="6">Brak działania w encji Wartości rzeczywiste</td>
</tr>
<tr>
<td rowspan="2">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</td>
<td>Wartość rzeczywista kosztu</td>
<td>Waluta jednostki kontraktującej</td>
<td rowspan="2">Wartość rzeczywista kosztu</td>
<td rowspan="2">Waluta jednostki kontraktującej
<td rowspan="2">Wartość rzeczywista kosztu</td>
<td rowspan="2">Wartość rzeczywista kosztu</td>
</tr>
<tr>
<td>Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="3">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</td>
<td>Wartość rzeczywista kosztu</td>
<td>Waluta jednostki kontraktującej</td>
<td rowspan="3">Wartość rzeczywista kosztu</td>
<td rowspan="3">Waluta jednostki kontraktującej</td>
<td rowspan="3">Wartość rzeczywista kosztu</td>
<td rowspan="3">Wartość rzeczywista kosztu</td>
</tr>
<tr>
<td>Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="2">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</td>
<td>Wycofanie nierozliczonej sprzedaży</td>
<td>Waluta kontraktu projektu</td>
<td rowspan="2">Rozliczona sprzedaż w punkcie kontrolnym</td>
<td rowspan="2">Waluta kontraktu projektu</td>
<td rowspan="2">Nie dotyczy</td>
<td rowspan="2">Nie dotyczy</td>
</tr>
<tr>
<td>Rozliczona sprzedaż</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="3">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</td>
<td>Wycofanie nierozliczonej sprzedaży</td>
<td>Waluta kontraktu projektu</td>
<td rowspan="3">Nie dotyczy</td>
<td rowspan="3">Nie dotyczy</td>
<td rowspan="3">Nie dotyczy</td>
<td rowspan="3">Nie dotyczy</td>
</tr>
<tr>
<td>Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="2">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</td>
<td>Rozliczona sprzedaż — wycofanie</td>
<td>Waluta kontraktu projektu</td>
<td rowspan="5">
<ul>
<li>Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</li>
<li>Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></li>
</ul>
</td>
<td rowspan="5">Waluta kontraktu projektu</td>
<td rowspan="5">Nie dotyczy</td>
<td rowspan="5">Nie dotyczy</td>
</tr>
<tr>
<td>Rozliczona sprzedaż</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="3">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</td>
<td>Rozliczona sprzedaż — wycofanie</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Rozliczona sprzedaż w zakresie nowej ilości</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Nierozliczona sprzedaż — odpłatna w zakresie różnicy</td>
<td>Waluta kontraktu projektu</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu

<table>
<thead>
<tr>
<th rowspan="3">Zdarzenie</th>
<th colspan="4">Projekt do rozliczenia lub sprzedany</th>
<th rowspan="3">Projekt na etapie przedsprzedaży</th>
<th rowspan="3">Projekt wewnętrzny</th>
</tr>
<tr>
<th colspan="2">Rozliczanie według czasu i materiałów</th>
<th colspan="2">Stała cena</th>
</tr>
<tr>
<th>Wartości rzeczywiste</th>
<th>Waluta transakcji</th>
<th>Stała cena</th>
<th>Waluta transakcji</th>
</tr>
</thead>
<tbody>
<tr>
<td>Jest tworzony wpis czasu.</td>
<td colspan="6">Brak działania w encji Wartości rzeczywiste</td>
</tr>
<tr>
<td>Jest przesyłany wpis czasu.</td>
<td colspan="6">Brak działania w encji Wartości rzeczywiste</td>
</tr>
<tr>
<td rowspan="4">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</td>
<td>Wartość rzeczywista kosztu</td>
<td>Waluta jednostki kontraktującej</td>
<td rowspan="4">Wartość rzeczywista kosztu</td>
<td rowspan="4">Waluta jednostki kontraktującej</td>
<td rowspan="4">Wartość rzeczywista kosztu</td>
<td rowspan="4">Wartość rzeczywista kosztu</td>
</tr>
<tr>
<td>Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Koszt jednostkowy zasobów</td>
<td>Waluta jednostki zasobów</td>
</tr>
<tr>
<td>Sprzedaż międzyorganizacyjna</td>
<td>Waluta jednostki kontraktującej</td>
</tr>
<tr>
<td rowspan="5">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</td>
<td>Wartość rzeczywista kosztu</td>
<td>Waluta jednostki kontraktującej</td>
<td rowspan="5">Wartość rzeczywista kosztu</td>
<td rowspan="5">Waluta jednostki kontraktującej</td>
<td rowspan="5">Wartość rzeczywista kosztu</td>
<td rowspan="5">Wartość rzeczywista kosztu</td>
</tr>
<tr>
<td>Koszt jednostkowy zasobów</td>
<td>Waluta jednostki zasobów</td>
</tr>
<tr>
<td>Sprzedaż międzyorganizacyjna</td>
<td>Waluta jednostki kontraktującej</td>
</tr>
<tr>
<td>Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="2">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</td>
<td>Wycofanie nierozliczonej sprzedaży</td>
<td>Waluta kontraktu projektu</td>
<td rowspan="2">Rozliczona sprzedaż w punkcie kontrolnym</td>
<td rowspan="2">Waluta kontraktu projektu</td>
<td rowspan="2">Nie dotyczy</td>
<td rowspan="2">Nie dotyczy</td>
</tr>
<tr>
<td>Rozliczona sprzedaż</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="3">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</td>
<td>Wycofanie nierozliczonej sprzedaży</td>
<td>Waluta kontraktu projektu</td>
<td rowspan="3">Nie dotyczy</td>
<td rowspan="3">Nie dotyczy</td>
<td rowspan="3">Nie dotyczy</td>
<td rowspan="3">Nie dotyczy</td>
</tr>
<tr>
<td>Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="2">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</td>
<td>Rozliczona sprzedaż — wycofanie</td>
<td>Waluta kontraktu projektu</td>
<td rowspan="5">
<ul>
<li>Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</li>
<li>Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></li>
</ul>
</td>
<td rowspan="5">Waluta kontraktu projektu</td>
<td rowspan="5">Nie dotyczy</td>
<td rowspan="5">Nie dotyczy</td>
</tr>
<tr>
<td>Rozliczona sprzedaż</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td rowspan="3">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</td>
<td>Rozliczona sprzedaż — wycofanie</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Rozliczona sprzedaż w zakresie nowej ilości</td>
<td>Waluta kontraktu projektu</td>
</tr>
<tr>
<td>Nierozliczona sprzedaż — odpłatna w zakresie różnicy</td>
<td>Waluta kontraktu projektu</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]