---
title: Procesy sprzedaży
description: Ta temat zawiera informacje o podstawowych procesach sprzedaży.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 5f01ba14baa0a2378b0a230a46aed3a682342ce6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014219"
---
# <a name="sales-processes"></a>Procesy sprzedaży

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Procesy sprzedaży używane w organizacji opartej na projektach różnią się w zależności od procesów sprzedaży używanych w organizacji opartej na produkcie. Różnica wynika z tego, że cykle sprzedaży w organizacjach opartych na projektach są dłuższe i wymagają niestandardowych technik oceny, aby analizować i tworzyć oferty dla każdej transakcji. Dynamics 365 Project Service Automation używa części z tej samej funkcji, która jest używana w procesie sprzedaży dla Dynamics 365 Sales. Oto kilka przykładów:

- Encja potencjalny klient jest używana do śledzenia procesu sprzedaży.
- Kwalifikujący się potencjalni klienci są śledzeni jako szanse sprzedaży. Proces sprzedaży może również zaczynać się od szansy sprzedaży.
- Uzyskiwanie dostępu do wszystkich pokrewnych artefaktów szansy sprzedaży. Te artefakty to zespół ds. sprzedaży, udziałowcy, prawdopodobieństwo, ocena, etapy sprzedaży i procesy biznesowe.
- Dla szansy sprzedaży są tworzone różne oferty.
- Oferta jest oznaczona jako **Zamknięta jako wykorzystana** w celu utworzenia zamówienia sprzedaży. W programie PSA zamówienie sprzedaży jest dostosowywane i nazywane jest kontraktem dotyczącym projektu.

Na poniższym rysunku pokazano typowy proces sprzedaży w organizacji opartej na projektach.

> ![Proces sprzedaży w organizacji opartej na projektach](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Szacowanie sprzedaży
Wartość sprzedaży może być oceniana na podstawie projektów, które zostały wcześniej dostarczone, oraz złożoności projektów. W przypadku projektów obejmujących rozszerzenia poprzednich projektów lub projektów, w których jest specjalistyczna wiedza i dobrze znane są szablony pracy, można użyć prostszego procesu szacowania. Bardziej złożone projekty mają zwykle dłuższy proces zakupu. W związku z tym w procesie szacowania sprzedaży występuje więcej etapów. Na początku procesu zespół ds. sprzedaży korzysta z pozostałej części menedżerów kont oraz specjalistów (msp) w celu utworzenia oszacowania wysokiego poziomu dla każdego odrębnego składnika pracy, który jest w ofercie. Te składniki pracy są reprezentowane przez wiersze oferty. 

Istnieje możliwość utworzenia oszacowania wysokiego poziomu oferty. Ostatecznie to szacowane na wyższym poziomie zostanie zastąpione bardziej szczegółową wartością szacunkową, która jest oparta na planie projektu utworzonym przy użyciu standardowych szablonów projektów. Szablony te ułatwiają utworzenie harmonogramu i określenie wartości pieniężnych w ofercie i jej składnikach (wierszach oferty). 

Użytkownik może utworzyć wiele ofert dla projektu i pogrupować je w ramach jednego typu encji szansa sprzedaży. Ostatecznie jedna z tych ofert jest oznaczana jako **zamknięta jako wykorzystana** i zostaje utworzony kontrakt dotyczący projektu lub zestawienie prac. Kontrakt projektu zawiera wartość objętą umową dla każdego komponentu (pozycja kontraktu), która jest akceptowana przez klienta, aby była dostarczona. Zestawienie prac jest zwykle tworzone jako dokument Microsoft Word. Wszystkie faktury wysyłane do klienta w trakcie realizacji projektu odwołują się do kontraktu lub zestawienia prac.

Można również utworzyć alternatywne oferty pod jednym typem encji szansa sprzedaży lub konfigurację systemu w taki sposób, aby kontrakt projektu był tworzony w momencie wykorzystania oferty. W takim przypadku można dołączyć dokument programu Word reprezentujący zestawienie pracy do rekordu kontraktu projektu.

![Zamykanie oferty w celu utworzenia kontraktu dotyczącego projektu](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfigurowanie procesu sprzedaży
Do skonfigurowania procesu sprzedaży można użyć przepływu procesów biznesowych (BPF) w Microsoft Dynamics 365. BPF dają pracownikom działu sprzedaży interfejs wizualny, za pomocą którego można przechodzić między etapami typowymi dla danej firmy.

Na przykład firma może w procesie sprzedaży mieć następujące sześć etapów:

1. Kwalifikuj
2. Szacowanie
3. Przegląd wewnętrzny
4. Contract
5. Dostarczenie
6. Zamknij

Te sześć etapów są reprezentowane przez cudzysłów ostrokątny (\>), który jest wybierany w celu rozwinięcia każdego typu tworzonych encji z szansą sprzedaży.

![Konfiguracja procesów biznesowych w Dynamics 365](media/basic-guide-3.png)
 
Organizacja może używać innych obiektów do reprezentowania tej samej transakcji. Na początku procesu sprzedaży transakcja jest reprezentowana przez obiekt szansa sprzedaży. W miarę upływu czasu i przybywania szczegółów można użyć oszacowań wysokiego poziomu w celu utworzenia jednej lub większej liczby ofert. Jeśli jedna z tych ofert jest analizowana przez udziałowców wewnętrznych i klienta, encja Oferta reprezentuje transakcję. Po zaakceptowaniu oferty przez klienta kontrakt lub jego zestawienie pracy stanowią informację o transakcji. Aby obsłużyć to zachowanie, BPF ma strukturę, dzięki czemu każdy etap procesu jest połączony z inną tabelą bazy danych.

Encja Szansa sprzedaży może tworzyć kopię zapasową etapu **kwalifikowania** w procesie sprzedaży. Encja Oferta może robić kopie zapasowe etapów **Szacunku** i **Oceny wewnętrznej**. Encja Kontrakt dotyczący projektu może robić kopie zapasowe etapów **Kontrakt**, **Dostarczenie** i **Zamknięcie**.

W miarę przechodzenia kolejnych etapów w umowach będą wyświetlane monity o utworzenie odpowiedniego rekordu encji w celu ułatwienia pomocy i przeprowadzenia procesu. Te etapy mogą być warunkowe. Na przykład jeśli jest wymagane wewnętrzne sprawdzenie oferty tylko wtedy, gdy oferta korzysta z niestandardowych cenników, można skonfigurować ten warunek w odpowiednim etapie procesu biznesowego. Etap **wewnętrznego przeglądu** jest widoczny tylko w przypadku ofert, w których jest używany niestandardowy cennik. W przypadku wszystkich pozostałych transakcji i ofert po etapie **Oszacowanie** następuje etap **Kontrakt**.

> [!NOTE]
> PSA zawiera konkretne strony encji szansy sprzedaży, oferty, zamówienia i faktury. Szanse sprzedaży, oferty, zamówienia i faktury dla usługi projektów należy utworzyć na podstawie tych encji na stronach z informacjami o projekcie. Jeśli do utworzenia rekordu jest używana inna strona, nie będzie można otworzyć rekordu na stronie z **informacjami o projekcie**. Aby otworzyć rekord z poziomu strony **informacji o projekcie**, należy usunąć rekord i utworzyć go ponownie na stronie **informacji o projekcie**. Na stronie **informacje o projekcie** logika biznesowa dla każdego z tych typów encji daje gwarancję, że pole **typu** rekordu będzie poprawnie ustawione, a wszystkie obowiązkowe pojęcia są poprawnie zainicjowane.

> ![Informacje o projekcie dla nowego zamówienia](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Różnice między rozwiązaniem Project Service Automation a sprzedażą
Mimo że proces sprzedaży w usłudze PSA korzysta z podstawowych funkcji procesu sprzedaży w sprzedaży, istnieją pewne zasadnicze różnice w zależności od metod postępowania w organizacjach opartych na projektach. Oto kilka przykładów:

- **Oferty projektu** — w programie Project Service Automation oferta jest zamykana po utworzeniu kontraktu projektu z poziomu oferty. W sprzedaży można zachować ofertę otwartą po jej wykorzystaniu. Ta różnica wynika z tego, że w organizacjach opartych na projektach lepiej dopasować umowę dotyczącą oferty i kontraktu dotyczącego projektu. 
- **Aktywacja i poprawki** — w programie PSA aktywacja i poprawki nie są obsługiwane w ofertach projektów. W przypadku sprzedaży oferta może zostać zablokowana w celu zapobiegania dodatkowym edycjom.
- **Zamknięcie ofert jako utraconych lub wygranych** — w usłudze PSA, kiedy oferta projektu jest zamykana jako wygrana lub utracona, szansa sprzedaży pozostaje otwarta. Wszystkie pozostałe oferty z szansy sprzedaży zostają zamknięte jako utracone. W przypadku sprzedaży, gdy oferta jest zamykana jako wygrana lub utracona, użytkownikowi jest wyświetlany monit o wykonanie akcji na szansie sprzedaży. W zależności od wartości wprowadzonej przez użytkownika szansa sprzedaży może być ZAMKNIĘTA lub pozostawiona otwarta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Śledzenie korekt ofert i planów projektów w cyklu sprzedaży
W PSA nie można śledzić poprawek wprowadzanych do oferty. Zamiast tego konieczne jest oznaczenie istniejącej oferty **zamkniętej jako utraconej**, a następnie utworzenie nowej oferty. Oferty oparte na projektach można skopiować lub sklonować, używając PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Śledzenie komentarzy i zatwierdzania ofert i kontraktów projektów
Użytkownik może zarządzać przeglądaniem i zatwierdzaniem ofert i kontraktów projektów przy użyciu tablicy rekordów i wpisów. Organizacja może tworzyć niestandardowe przepływy pracy i dodatki plug-in, aby przypisywać, przekierowywać, eskalować i zarządzać powiadomieniami o elementach pracy przeglądanie i zatwierdzenie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]