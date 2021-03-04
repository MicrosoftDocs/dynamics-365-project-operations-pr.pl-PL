---
title: Omówienie procesu sprzedaży
description: Ten temat zawiera informacje o podstawowych procesach sprzedaży.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5da29d2959a6e49defa185630f45d280dba283c4
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177614"
---
# <a name="sales-process-overview"></a>Omówienie procesu sprzedaży

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Procesy sprzedaży używane w organizacji opartej na projektach różnią się w zależności od procesów sprzedaży używanych w organizacji opartej na produkcie. Różnica wynika z tego, że cykle sprzedaży w organizacjach opartych na projektach są dłuższe i wymagają niestandardowych technik szacunkowych, aby analizować i tworzyć oferty dla każdej transakcji. Dynamics 365 Project Operations używa części z poniższej funkcji, która jest używana w procesie sprzedaży:

- Rekord potencjalny klient jest używana do śledzenia procesu sprzedaży.
- Kwalifikujący się potencjalni klienci są śledzeni jako szanse sprzedaży.
- Wszystkie pokrewne artefakty szansy sprzedaży są dostępne. Te artefakty to zespół ds. sprzedaży, udziałowcy, prawdopodobieństwo, ocena, etapy sprzedaży i procesy biznesowe.
- Dla szansy sprzedaży są tworzone różne oferty.
- Oferta, która otrzymała oznaczenie **Zamknięta jako wykorzystana** w celu utworzenia zamówienia sprzedaży. W programie Project Operations zamówienie sprzedaży jest dostosowywane i nazywane jest kontraktem dotyczącym projektu.

## <a name="estimate-a-sale"></a>Szacowanie sprzedaży
Wartość sprzedaży może być oceniana na podstawie projektów, które zostały wcześniej dostarczone, oraz złożoności projektów. W przypadku projektów obejmujących rozszerzenia poprzednich projektów lub projektów, w których jest specjalistyczna wiedza i dobrze znane są szablony pracy, można użyć prostszego procesu szacowania. Bardziej złożone projekty mają zwykle dłuższy proces zakupu. W związku z tym w procesie szacowania sprzedaży występuje więcej etapów. Na początku procesu zespół ds. sprzedaży korzysta z pozostałej części menedżerów kont oraz specjalistów (ekspertów) w celu utworzenia oszacowania wysokiego poziomu dla każdego odrębnego składnika pracy, który jest w ofercie. Te składniki pracy są reprezentowane przez wiersze oferty. 

Istnieje możliwość utworzenia oszacowania wysokiego poziomu oferty. Ostatecznie to szacowane na wyższym poziomie zostanie zastąpione bardziej szczegółową wartością szacunkową, która jest oparta na planie projektu utworzonym przy użyciu standardowych szablonów projektów. Szablony te ułatwiają utworzenie harmonogramu i określenie wartości pieniężnych w ofercie i jej składnikach (wierszach oferty). 

Użytkownik może utworzyć wiele ofert dla projektu i pogrupować je w ramach jednego typu rekordu szansa sprzedaży. Ostatecznie jedna z tych ofert jest oznaczana jako **zamknięta jako wykorzystana** i zostaje utworzony kontrakt dotyczący projektu lub zestawienie prac. Kontrakt projektu zawiera wartość objętą umową dla każdego komponentu (pozycja kontraktu), która jest akceptowana przez klienta, aby była dostarczona. Zestawienie prac jest zwykle tworzone jako dokument Microsoft Word. Wszystkie faktury wysyłane do klienta w trakcie realizacji projektu odwołują się do kontraktu lub zestawienia prac.

Można również utworzyć alternatywne oferty pod jednym typem rekordu szansa sprzedaży lub konfigurację systemu w taki sposób, aby kontrakt projektu był tworzony w momencie wykorzystania oferty. W takim przypadku można dołączyć dokument programu Word reprezentujący zestawienie pracy do rekordu kontraktu projektu.

## <a name="configure-the-sales-process"></a>Konfigurowanie procesu sprzedaży
Do skonfigurowania procesu sprzedaży można użyć przepływu procesów biznesowych. Te przepływy stanowią interfejs wizualny ukierunkowany na przechodzenie przez etapy procesu sprzedaży.

Na przykład firma może w procesie sprzedaży mieć następujące sześć etapów:

1. Kwalifikuj
2. Szacowanie
3. Przegląd wewnętrzny
4. Kontrakt
5. Dostarczenie
6. Zamykanie
 
Organizacja może używać innych obiektów do reprezentowania tej samej transakcji. Na początku procesu sprzedaży transakcja jest reprezentowana przez obiekt szansa sprzedaży. W miarę upływu czasu i przybywania szczegółów można użyć oszacowań wysokiego poziomu w celu utworzenia jednej lub większej liczby ofert. Jeśli jedna z tych ofert jest analizowana przez udziałowców wewnętrznych i klienta, encja Oferta reprezentuje transakcję. Po zaakceptowaniu oferty przez klienta kontrakt lub jego zestawienie pracy stanowią informację o transakcji. Aby obsłużyć to zachowanie, BPF ma strukturę, dzięki czemu każdy etap procesu jest połączony z inną tabelą bazy danych.

Encja Szansa sprzedaży może tworzyć kopię zapasową etapu **kwalifikowania** w procesie sprzedaży. Encja Oferta może robić kopie zapasowe etapów **Szacunku** i **Oceny wewnętrznej**. Encja Kontrakt dotyczący projektu może robić kopie zapasowe etapów **Kontrakt**, **Dostarczenie** i **Zamknięcie**.

W miarę przechodzenia kolejnych etapów w umowach będą wyświetlane monity o utworzenie odpowiedniego rekordu encji w celu ułatwienia pomocy i przeprowadzenia procesu. Te etapy mogą być warunkowe. Na przykład jeśli jest wymagane wewnętrzne sprawdzenie oferty tylko wtedy, gdy oferta korzysta z niestandardowych cenników, można skonfigurować ten warunek w odpowiednim etapie procesu biznesowego. Etap **wewnętrznego przeglądu** jest widoczny tylko w przypadku ofert, w których jest używany niestandardowy cennik. W przypadku wszystkich pozostałych transakcji i ofert po etapie **Oszacowanie** następuje etap **Kontrakt**.

> [!NOTE]
> Project Operations mają konkretne strony rekordów szansy sprzedaży, oferty, zamówienia i faktury. Te rekordy muszą zostać utworzone przy użyciu stron informacji o projekcie dla tych encji. W przeciwnym razie nie będzie możliwe otwieranie rekordów na stronie z **informacjami o projekcie**. Aby otworzyć rekord z poziomu strony z **informacjami o projekcie** należy usunąć rekord i utworzyć go ponownie, korzystając ze strony z **informacjami o projekcie**, gdzie logika biznesowa dla każdego z tych typów encji gwarantuje, że pole **Typ** rekordu będzie poprawnie ustawione, a wszystkie obowiązkowe pojęcia poprawnie zainicjowane.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Śledź korekty ofert i planów projektów w cyklu sprzedaży
W Project Operations nie można śledzić poprawek wprowadzanych do oferty. Zamiast tego konieczne jest oznaczenie istniejącej oferty **zamkniętej jako utraconej**, a następnie utworzenie nowej oferty. Oferty oparte na projektach można skopiować lub sklonować.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Śledź komentarze i zatwierdzenia ofert i kontraktów projektów
Użytkownik może zarządzać przeglądaniem i zatwierdzaniem ofert i kontraktów projektów przy użyciu tablicy rekordów i wpisów. Organizacja może tworzyć niestandardowe przepływy pracy i dodatki plug-in, aby przypisywać, przekierowywać, eskalować i zarządzać powiadomieniami o elementach pracy przeglądanie i zatwierdzenie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]