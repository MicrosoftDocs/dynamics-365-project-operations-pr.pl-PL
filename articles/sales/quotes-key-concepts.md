---
title: Pojęcia unikalne dla ofert opartych na projekcie
description: W tym artykule przedstawiono informacje na temat ofert projektu w aplikacji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824341"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Pojęcia unikalne dla ofert opartych na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Przed rozpoczęciem użytkowania ofert projektu w Microsoft Dynamics 365 Project Operations należy pamiętać o następujących kluczowych pojęciach.

## <a name="owning-company"></a>Firma będąca właścicielem

Firma będąca właścicielem reprezentuje osobę prawną, która jest właścicielem dostawcy projektu. Klient w ofercie powinien być prawidłowym klientem w tej osobie prawnej w aplikacjach finansowych i operacyjnych. Waluta firmy, która jest właścicielem, i waluta jednostki kontraktu wybrana w ofercie opartej na projekcie musi być taka sama.

## <a name="contracting-unit"></a>Jednostka kontraktująca

Jednostka kontraktująca reprezentuje dział lub oddział, który jest właścicielem dostarczanego projektu. Koszty zasobów można zdefiniować dla każdej jednostki. Po określeniu kosztów zasobu dla zasobu w jednostce kontaktowej można skonfigurować różne stawki kosztów dla zasobów, które dana instytucja lub inne działy lub oddziały w ramach przedsiębiorstwa wykorzystują. Te stawki kosztów są określane jako ceny transferów, pożyczanie zasobów lub ceny wymiany. Podczas konfigurowania kosztów pożyczania zasobów od innych działów można skonfigurować stawki kosztów w walucie oddziału użyczającego.

## <a name="cost-currency"></a>Waluta kosztu

Waluta kosztów w Project Operations jest walutą, w której są raportowane koszty. Ta waluta jest pobierana z waluty dołączonej do pola **Jednostka zamawiająca** na ofercie, kontrakcie i projekcie. Koszty mogą być rejestrowane w dowolnej walucie w projekcie. Jednakże waluta zapisana na wydatku zostanie przekonwertowana na walutę w projekcie.

Ze względu na fakt, że kursy wymiany na platformie Dataverse nie dotyczą konkretnej daty, sumy na ekranie dotyczące wydatków mogą zmieniać się w czasie, jeśli zostaną zaktualizowane kursy wymiany walut. Natomiast koszty zarejestrowane w bazie danych pozostaną bez zmian, ponieważ kwoty są przechowywane w walutach, w których zostały poniesione.

## <a name="sales-currency"></a>Waluta sprzedaży

Waluta sprzedaży w Project Operations to waluta, w której są szacunkowe i rzeczywiste kwoty sprzedaży są rejestrowane i pokazywane. Jest to również waluta, w której klient będzie fakturowany. Z poziomu oferty projektu domyślna waluta sprzedaży jest określana na podstawie rekordu klienta lub konta i może zostać zmieniona podczas tworzenia oferty. Jednakże po zapisaniu oferty nie można już zmienić waluty sprzedaży. Domyślne cenniki produktów i projektów są tworzone na podstawie waluty sprzedaży w ofercie.

W odróżnieniu od kosztów, wartości sprzedaży można zapisać **tylko** w walucie sprzedaży.

## <a name="billing-method"></a>Metoda rozliczania

Zazwyczaj w projekcie istnieje stała opłata i modele kontraktowania oparte na zużyciu. W Project Operations model kontraktu projektu jest reprezentowany przez sposób rozliczania. Sposób rozliczania ma dwie wartości: czas i materiał oraz stałą cenę.

- **Czas i materiały** — model kontraktu oparty na zużyciu, gdzie każdy koszt poniesiony jest związany z odpowiednim przychodem. W miarę szacowania lub ponoszenia dodatkowych kosztów odpowiadające oszacowana i rzeczywista sprzedaż będzie również się zmieniać. W wierszach oferty, które mają taką metodę fakturowania, można podać limity nie do przekroczenia. W ten sposób można włączyć górny limit rzeczywistego przychodu. Szacunkowy przychód nie jest ograniczony limitami nie-do-przekroczenia.
- **Stała cena** — model kontraktowania z opłatą ustaloną, który oznacza, że wartości sprzedaży będą niezależne od poniesionych kosztów. Wartość sprzedaży jest stała i nie zmienia się w wyniku oszacowania lub ponoszenia dodatkowych kosztów.

## <a name="project-price-lists"></a>Cenniki projektu

Cenniki projektów to cenniki, które są używane do korzystania z cen domyślnych, a nie stawki kosztów, czasu, wydatków i innych składników związanych z projektem. Istnieje wiele cenników, a każdy z nich może mieć własną datę wejścia w życie dla każdej oferty projektu. Project Operations nie obsługuje nakładania się dat dla cenników projektu.

## <a name="product-price-lists"></a>Cenniki produktu

Cenniki produktów to cenniki, które są używane do wprowadzania kalkulacji cen domyślnych, a nie stawki kosztów dla wierszy na podstawie produktu w ofercie. Dla każdej oferty istnieje tylko jeden cennik produktu.

## <a name="transaction-classes"></a>Klasy transakcji

W Project Operations są obsługiwane cztery typy klas transakcji:

- Czas
- Wydatek
- Materiał
- Opłata

Koszty i wartości sprzedaży można oszacować i ponieść w klasach transakcji **czasu**, **wydatków** i **materiału**. **Opłata** jest klasą transakcji typu przychód.

## <a name="work-entities-and-billing-entities"></a>Encje robocze i encje rozliczania

Projektu i zadania to encje reprezentujące pracę. Wiersze oferty i pozycje kontraktu to encje reprezentujące rozliczanie. Można połączyć różne encje robocze z opcjami rozliczenia, kojarząc je z wierszami oferty lub pozycjami kontraktu.

## <a name="multi-customer-deals"></a>Transakcje dotyczące wielu klientów

Transakcje dotyczące wielu klientów mają miejsce, gdy na fakturze znajduje się więcej niż jeden klient. Oto kilka typowych przykładów:

- **Oryginalne przedsiębiorstwa producenta sprzętu (OEM) i ich partnerzy** — partnerzy i odsprzedawcy sprzedają produkt dzięki usługom z wartościami dodanymi. W trakcie umowy z klientem, w której producent zazwyczaj OEM proponuje finansowanie części projektu.
- **Projekty sektora publicznego** — wiele działów administracji lokalnej zgadza się na finansowanie projektu i zafakturowanie zgodnie z uprzednio ustalonym podziałem. Na przykład okręg szkolny i urząd miasta oświadczają, że będą finansować budowę basenu.

## <a name="invoice-schedules"></a>Harmonogram fakturowania

Harmonogramy fakturowania są specyficzne dla każdego wiersza oferty i są także opcjonalne. Harmonogramy fakturowania są tworzone na podstawie określonych dat rozpoczęcia i zakończenia oraz częstotliwości faktur. Są one używane na etapie kontraktu podczas konfigurowania automatycznej operacji tworzenia faktur. Na etapie oferty harmonogramy faktur są opcjonalne. Po ich utworzeniu na etapie oferty są one kopiowane do kontraktu projektu tworzonego przy wykorzystaniu oferty projektu.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Różnice z ofert Dynamics 365 Sales

Oferty Project Operations są oparte na ofertach Dynamics 365 Sales. Należy jednak pamiętać o pewnych zasadniczych różnicach funkcjonalnych:

- Oferty w Project Operations mają dwa różne typy wierszy: jeden dla projektów i jeden dla produktów.
- Oferty Project Operations mają własne elementy strony i interfejsu użytkownika (UI), reguły biznesowe, logikę biznesową w dodatkach plug-in oraz skrypty po stronie klienta, które sprawiają, że różnią się od ofert Sales.
- W rozwiązaniu Sales istnieje możliwość dołączenia wielu zamówień do jednej oferty sprzedaży. W Project Operations do oferty projektu można dołączyć tylko jeden kontrakt dotyczący projektu.
- Po wygraniu oferty sprzedaży pozostała szansa sprzedaży może pozostać otwarta. Po wygraniu oferty projektu pokrewna szansa sprzedaży jest zamykana.
- Oferta sprzedaży nie zawiera żadnych pól i koncepcji zawartych w ofercie projektu. Pola obejmują **jednostkę kontraktującą**, **menedżera klienta** oraz **Imię i nazwisko kontaktu u płatnika**.
- Oferty sprzedaży i oferty projektu są również identyfikowane za pośrednictwem pola opartego na zestawie opcji pod nazwą **Typ**. W przypadku oferty sprzedaży wartość w tym polu jest określana wartość **na podstawie towaru**. W przypadku oferty projektu jest to wartość **na podstawie pracy**.

Ze względu na te różnice nie zalecamy zamiennego używania ofert Sales i ofert Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
