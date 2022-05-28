---
title: Kontrakty projektu - Kluczowe pojęcia
description: W tym temat zamieszczono informacje dotyczące podstawowych pojęć w kontraktach projektu w Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f87a29893ca3d9bec6fbd07dded66a282ff597c3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582953"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Pojęcia unikalne dla Kontraktów opartych na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_



W tym temacie przedstawiono kluczowe pojęcia dotyczące korzystania z kontraktów projektów w aplikacji Dynamics 365 Project Operations:

## <a name="owning-company"></a>Firma będąca właścicielem

Firma jest prawnie encjami z modułem **zarządzania projektami i księgowym** dla Project Operations z usługi Dynamics 365 Finance. Firma reprezentuje podmiot prawny, który będzie rozliczał koszty i przychody wynikające z transakcji.

## <a name="contracting-unit"></a>Jednostka kontraktująca

Jednostka kontraktująca reprezentuje dział lub oddział, który jest właścicielem projektu. Koszty zasobów można zdefiniować dla każdej jednostki. Po określeniu kosztu dla zasobu można również skonfigurować różne stawki kosztów dla zasobów. Kontraktująca jednostka pożycza zasoby z innego działu lub części przedsiębiorstwa. Te koszty stawki kosztów zasobów są określane jako ceny transferów, pożyczanie zasobów lub ceny wymiany. Podczas konfigurowania kosztów pożyczania zasobów od innych działów wykorzystywana jest waluta oddziału użyczającego.

## <a name="cost-currency"></a>Waluta kosztu

Waluta kosztów jest walutą, w której są raportowane koszty na ekranie. Ta waluta jest pobierana z waluty dołączonej do pola **Jednostka zamawiająca** na ofercie, kontrakcie i projekcie. Koszty mogą być rejestrowane w dowolnej walucie w projekcie. Jednakże waluta zapisana na wydatku zostanie przekonwertowana na walutę w projekcie.

Ze względu na fakt, że kursy wymiany na platformie Common Data Service (CDS) nie dotyczą konkretnej daty, sumy na ekranie dotyczące wydatków mogą zmieniać się w czasie, jeśli zostaną zaktualizowane kursy wymiany walut. Natomiast koszty zarejestrowane w bazie danych pozostaną bez zmian, ponieważ kwoty są przechowywane w walutach, w których zostały poniesione.

## <a name="sales-currency"></a>Waluta sprzedaży

Waluta sprzedaży w Project Operations to waluta, w której są szacunkowe i rzeczywiste kwoty sprzedaży są rejestrowane i pokazywane. Waluta sprzedaży to waluta, w której klient będzie fakturowany. Z poziomu oferty projektu domyślna waluta sprzedaży jest określana na podstawie rekordu klienta lub konta i może zostać zmieniona podczas tworzenia kontraktu. Kiedy kontrakt jest tworzony przez zamknięcie oferty jako wykorzystanej, waluta w kontrakcie jest domyślnie bazowana na walucie w ofercie.

Podczas tworzenia kontraktu projektu od nowa, pola **Waluta sprzedaży** nie można edytować. Cenniki produktów i projektów tworzą wartości domyślne na podstawie waluty w kontrakcie.

W odróżnieniu od kosztów, wartości sprzedaży można zapisać tylko w walucie sprzedaży.

## <a name="billing-method"></a>Metoda rozliczania

Zazwyczaj w projekcie istnieją dwa typy modeli kontraktowania: stała opłata i modele kontraktowania oparte na zużyciu. Te modele są przedstawione w Project Operations jako metody fakturowania z dwiema możliwymi wartościami:

- Czas i materiały: model kontraktowania bazujący na zużyciu, gdzie każdy koszt poniesiony jest związany z odpowiednim przychodem. W miarę szacowania lub ponoszenia dodatkowych kosztów odpowiadające oszacowana i rzeczywista sprzedaż będzie również się zmieniać. Określ limity nie do przekroczenia dla pozycji kontraktu, które zawierają tę metodę fakturowania. Powoduje to ograniczenie rzeczywistego przychodu. Szacunkowy przychód nie jest ograniczony limitami nie-do-przekroczenia.
- Stała cena: model kontraktowania z opłatą ustaloną, który oznacza, że wartości sprzedaży będą niezależne od poniesionych kosztów. Wartość sprzedaży jest stała i nie zmienia się w wyniku oszacowania lub ponoszenia dodatkowych kosztów.

## <a name="project-price-lists"></a>Cenniki projektu

Cenniki projektów są używane do korzystania z cen domyślnych, a nie stawki kosztów, czasu, wydatków i innych składników związanych z projektem. Może istnieć wiele cenników. Każdy cennik ma własny czas obowiązywania dla każdego kontraktu dotyczącego projektu. Project Operations nie obsługuje nachodzących na siebie dat obowiązywania różnych cenników projektu.

Kiedy kontrakt projektu jest tworzony przez wygranie oferty projektu, cenniki projektu są kopiowane z nazwą kontraktu i datą uwzględnioną w tym kontrakcie. Skopiowanie tych informacji stanowi niestandardową kalkulację cen dla składników projektów zawartych w tym kontrakcie.

## <a name="transaction-classes"></a>Klasy transakcji

W Project Operations są obsługiwane cztery typy klas transakcji:

- Czas
- Wydatek
- Materiał
- Opłata

Koszty i wartości sprzedaży można oszacować i ponieść w klasach transakcji czasu, wydatków i materiału. Opłata jest klasą transakcji typu przychód.

## <a name="work-entities-and-billing-entities"></a>Encje robocze i encje rozliczania

Encje reprezentujące prace są projektami i zadaniami. Encje reprezentujące rozliczenia są wierszami kontraktu i pozycjami kontraktu. Można połączyć różne encje robocze z opcjami rozliczenia, kojarząc je z pozycjami kontraktu.

## <a name="multi-customer-deals"></a>Transakcje dotyczące wielu klientów

Transakcje dotyczące wielu klientów oznaczają, że na fakturze transakcji jest więcej niż jeden klient. Typowe przykłady to:

- Przedsiębiorstwa OEM i ich partnerzy: Partnerzy i odsprzedający sprzedają produkt z pewną wartością dodaną, zazwyczaj w ramach określonej umowy z klientem. Producenci OEM oferują finansowanie części projektu. 

- Projekty sektora publicznego: wiele działów administracji lokalnej zgadza się na finansowanie projektu i zafakturowanie zgodnie z uprzednio ustalonym podziałem. Na przykład okręg szkolny i urząd miasta oświadczają, że będą finansować budowę basenu.

## <a name="invoice-schedules"></a>Harmonogram fakturowania

Harmonogramy fakturowania są specyficzne dla poszczególnych pozycji kontraktu i są wymagane do funkcjonowania automatycznego zafakturowania. Harmonogramy fakturowania są tworzone na podstawie określonych dat rozpoczęcia i zakończenia oraz częstotliwości faktur. Te harmonogramy są używane na etapie kontraktu podczas konfigurowania automatycznej operacji tworzenia faktur. Po utworzeniu kontraktu projektu z poziomu oferty harmonogram fakturowania jest kopiowany do kontraktu dotyczącego projektu z oferty.

## <a name="changes-from-dynamics-365-sales-orders"></a>Zmiany z zamówień w Dynamics 365 Sales

Kontrakty w Project Operations są oparte na zamówieniach w Dynamics 365 Sales. Istnieją jednak poważne różnice w działaniu tych funkcji. Kontrakty mają własne elementy formularzy i UI, reguły biznesowe, logikę biznesową w dodatkach plug-in oraz skrypty po stronie klienta, które sprawiają, że różnią się od ofert Orders. Z tych powodów nie należy używać zamiennych zamówień typu Sales i Project Operations wymiennie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
