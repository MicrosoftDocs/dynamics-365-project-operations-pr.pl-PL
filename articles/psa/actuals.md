---
title: Omówienie wartości rzeczywistych
description: Ten temat zawiera informacje o wartościach rzeczywistych w projektach.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285631"
---
# <a name="actuals-overview"></a>Omówienie wartości rzeczywistych

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Wartości rzeczywiste określają ilość pracy wykonanej w projekcie. Wartości rzeczywiste projektu mogą być śledzone z powrotem do ich dokumentów źródłowych. Dokumentami mogą być wpisy czasu, wydatków i arkusza oraz faktury.

![Śledzenie wartości rzeczywistych projektu do dokumentów źródłowych](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Przesyłanie wpis czasu

W rozwiązaniu PSA podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza. Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży. Podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu. 

Logika wprowadzania cen domyślnych jest przechowywana w wierszu arkusza. Wszystkie wartości pól z wpisu czasu są kopiowane do wiersza arkusza. Te pola zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika. 

Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka organizacyjna**, powodują domyślne wprowadzenie właściwej ceny w wierszu arkusza. Chcąc dodać do wpisu niestandardowe pole, którego wartość ma zostać rozpowszechniona do wartości rzeczywistych, należy utworzyć pole w encji Wartości rzeczywiste, a następnie za pomocą mapowań pól skopiować pole z wpisu czasu do wartości rzeczywistej.

## <a name="submitting-an-expense-entry"></a>Przesyłanie wpisu wydatku

W rozwiązaniu PSA podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza. Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży. Podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.

Logika wprowadzania cen domyślnych dla wydatków bazuje na kategorii wydatków wybranej na stronie **Wpis wydatków**. Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty. Jednak w samej cenie kwota wprowadzona przez użytkownika jest ustawiana bezpośrednio w odpowiednich wierszach arkusza wydatków domyślnie dla kosztów i sprzedaży.

W obecnej wersji rozwiązania PSA we wpisach wydatków nie można wprowadzać domyślnych cen jednostkowych opartych na kategoriach.

## <a name="using-entry-journals-to-record-costs"></a>Używanie arkuszy wpisów do rejestrowania kosztów

W rozwiązaniu PSA arkusze wpisów umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych. Arkusz ma nagłówek, wiersze i akcję **Potwierdź**. Oto kilka scenariuszy, w których można korzystać z arkusza:

- Trzeba zarejestrować rzeczywiste koszty materiałów i wielkości sprzedaży w projekcie.
- Trzeba przenieść wartości rzeczywiste transakcji z innego systemu do PSA.
- Trzeba zarejestrować koszty, które wystąpiły w innym systemie, na przykład koszty zaopatrzenia lub podwykonawstwa.

> [!IMPORTANT]
> Korzystając z arkuszów wpisów do tworzenia wartości rzeczywistych, należy wykonać tylko te osoby, które są w pełni świadomi oddziaływania danego projektu na wyniki księgowania. Wynika to z faktu, że aplikacja nie sprawdza poprawności typu wiersza arkusza ani pokrewnej kalkulacji cen wprowadzonej w wierszu arkusza. Ze względu na wpływ tego typu arkusza należy zachować ostrożność w przypadku osób mających dostęp do tworzenia arkuszy wpisów.     


## <a name="recording-actuals-based-on-project-events"></a>Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu

Rozwiązanie PSA rejestruje transakcje finansowe zaistniałe w trakcie projektu. Te transakcje są zapisywane jako **wartości rzeczywiste**. W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.

**Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu**

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

**Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu**

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