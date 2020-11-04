---
title: Kluczowe pojęcia dotyczące oferty projektu
description: Ta temat zawiera informacje na temat używania ofert w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081936"
---
# <a name="project-quote-key-concepts"></a>Kluczowe pojęcia dotyczące oferty projektu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Należy zapoznać się z poniższymi podstawowymi pojęciami przed rozpoczęciem korzystania z ofert projektów w ramach Dynamics 365 Project Operations.

## <a name="contracting-unit"></a>Jednostka kontraktująca

Jednostka kontraktująca reprezentuje dział lub oddział, który jest właścicielem dostarczanego projektu. Koszty zasobów można zdefiniować dla każdej jednostki. Po określeniu kosztu zasobu w jednostce zamawianej można również skonfigurować różne stawki kosztów dla zasobów, które dana instytucja lub inne działy lub oddziały w ramach przedsiębiorstwa wykorzystują. Te koszty są określane jako ceny transferów, pożyczanie zasobów lub ceny wymiany. Podczas konfigurowania kosztów pożyczania zasobów od innych działów można również wybrać opcję konfigurowania stawek kosztów w walucie oddziału użyczającego.

## <a name="cost-currency"></a>Waluta kosztu

Waluta kosztów w Project Operations jest walutą, w której są raportowane koszty. Ta waluta jest pobierana z waluty dołączonej do pola **Jednostka zamawiająca** na ofercie, kontrakcie i projekcie. Koszty mogą być rejestrowane w dowolnej walucie w projekcie. Jednakże waluta zapisana na wydatku zostanie przekonwertowana na walutę w projekcie.

Ze względu na fakt, że kursy wymiany na platformie CDS nie dotyczą konkretnej daty, sumy na ekranie dotyczące wydatków mogą zmieniać się w czasie, jeśli zostaną zaktualizowane kursy wymiany walut. Natomiast koszty zarejestrowane w bazie danych pozostaną bez zmian, ponieważ kwoty są przechowywane w walutach, w których zostały poniesione.

## <a name="sales-currency"></a>Waluta sprzedaży

Waluta sprzedaży w Project Operations to waluta, w której są szacunkowe i rzeczywiste kwoty sprzedaży są rejestrowane i pokazywane. Jest to również waluta, w której klient będzie fakturowany. Z poziomu oferty projektu domyślna waluta sprzedaży jest określana na podstawie rekordu klienta lub konta i może zostać zmieniona podczas tworzenia oferty. Po zapisaniu oferty nie można już zmienić waluty sprzedaży. Cenniki produktów i projektów tworzą wartości domyślne na podstawie waluty sprzedaży w ofercie.

W odróżnieniu od kosztów wartości sprzedaży można zapisać tylko w walucie sprzedaży.

## <a name="billing-method"></a>Metoda rozliczania

Zazwyczaj w projekcie istnieje stała opłata i modele kontraktowania oparte na zużyciu. W Project Operations jest to przedstawione jako **Metoda rozliczenia** i zawiera dwie wartości, czas i materiały oraz ustaloną cenę.

- **Czas i materiały:** jest to model kontraktu bazujący na zużyciu, gdzie każdy koszt poniesiony jest związany z odpowiednim przychodem. W miarę szacowania lub ponoszenia dodatkowych kosztów odpowiadające oszacowana i rzeczywista sprzedaż będzie również się zmieniać. W wierszach oferty, które mają taką metodę fakturowania, można podać limity nie do przekroczenia. Spowoduje to ustawienie limitu rzeczywiście uzyskanego przychodu. Szacunkowy przychód nie jest ograniczony limitami nie-do-przekroczenia.
- **Stałą cena:** jest to model kontraktu z opłatą ustaloną, który oznacza, że wartości sprzedaży będą niezależne od poniesionych kosztów. Wartość sprzedaży jest stała i nie zmienia się w wyniku oszacowania lub ponoszenia dodatkowych kosztów.

## <a name="project-price-lists"></a>Cenniki projektu

Cenniki projektów to cenniki, które są używane do korzystania z cen domyślnych, a nie stawki kosztów, czasu, wydatków i innych składników związanych z projektem. Istnieje wiele cenników, a każdy z nich może mieć własną datę wejścia w życie dla każdej oferty projektu. Project Operations nie obsługuje nachodzących na siebie efektywnych dat cenników projektu.

## <a name="product-price-lists"></a>Cenniki produktu

Cenniki produktów to cenniki, które są używane do kalkulacji cen domyślnych, a nie stawki kosztów dla wierszy na podstawie produktu w ofercie. Dla każdej oferty istnieje tylko jeden cennik produktu.

## <a name="transaction-classes"></a>Klasy transakcji

W Project Operations są obsługiwane cztery typy klas transakcji:

- Czas
- Wydatek
- Materiał
- Opłata

Koszty i wartości sprzedaży można oszacować i ponieść w klasach transakcji czasu, wydatków i materiału. Opłata jest klasą transakcji typu przychód.

## <a name="work-entities-and-billing-entities"></a>Encje robocze i encje rozliczania

Encje reprezentujące prace są projektami i zadaniami. Encje reprezentujące rozliczenia są wierszami oferty i pozycjami kontraktu. Można połączyć różne encje robocze z opcjami rozliczenia, kojarząc je z ofertami lub pozycjami kontraktu.

## <a name="multi-customer-deals"></a>Transakcje dotyczące wielu klientów

Transakcje dotyczące wielu klientów mają miejsce, gdy na fakturze znajduje się więcej niż jeden klient. Typowe przykłady to:

- **Przedsiębiorstwa OEM i ich partnerzy:** partnerzy i odsprzedawcy sprzedają produkt dzięki usługom z wartościami dodanymi. Zazwyczaj jest to scenariusz, w którym producent OEM proponuje finansowanie części projektu przy użyciu określonej transakcji. 

- **Projekty sektora publicznego:** wiele działów administracji lokalnej zgadza się na finansowanie projektu i zafakturowanie zgodnie z uprzednio ustalonym podziałem. Na przykład okręg szkolny i urząd miasta oświadczają, że będą finansować budowę basenu.

## <a name="invoice-schedules"></a>Harmonogram fakturowania

Harmonogramy fakturowania są specyficzne dla każdego wiersza oferty i są również opcjonalne. Harmonogramy fakturowania są tworzone na podstawie określonych dat rozpoczęcia i zakończenia oraz częstotliwości faktur. Harmonogramy fakturowania są używane na etapie kontraktu podczas konfigurowania automatycznej operacji tworzenia faktur. Na etapie oferty harmonogramy są opcjonalne. Kiedy harmonogramy faktur są tworzone na etapie **Oferty** , są one kopiowane do kontraktu projektu tworzonego przy wykorzystaniu oferty projektu.

## <a name="changes-from-dynamics-365-sales-quote"></a>Zmiany z oferty Dynamics 365 Sales:

Oferty Project Operations są oparte na ofertach Dynamics 365 Sales. Należy jednak pamiętać o pewnych zasadniczych różnicach funkcjonalnych:

- Działania **Popraw** i **Aktywuj** nie są obsługiwane.
- Oferty Project Operations są dwoma różnymi typami wierszy. Jedna dla projektów, a drugi produktów.
- Oferty Project Operations mają własne elementy formularzy i UI, reguły biznesowe, logikę biznesową w dodatkach plug-in oraz skrypty po stronie klienta, które sprawiają, że różnią się od ofert Sales.

Z tych powodów nie jest zalecane korzystanie z oferty Sales i Project Operations wymiennie.
