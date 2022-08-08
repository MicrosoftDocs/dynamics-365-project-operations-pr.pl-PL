---
title: Przeglądanie proponowanych zasobów
description: W tym artykule zamieszczono informacje dotyczące sposobu proponowania zasobów do projektu.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183988"
---
# <a name="review-proposed-resources"></a>Przeglądanie proponowanych zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Menedżerowie zasobów mogą proponować zasób menedżerowi projektu za pomocą żądania zasobu.

Aby przejrzeć proponowane zasoby, wykonaj następujące kroki:

1. W siatce **żądań** lub w oknie samego żądania wybierz pozycję **Znajdź zasoby**.
2. Na stronie **Asystent planowania** wybierz zasób i potwierdź, że wszystkie proponowane godziny są uwzględnione w proponowanej rezerwacji.
3. W okienku **Tworzenie rezerwacji zasobu** ustaw pole **Stan rezerwacji** na **Proponowana**, a następnie wybierz opcję **Zarezerwuj**.

    > [!NOTE]
    > Ustawienie **stanu rezerwacji** na **Proponowana** nie powoduje rezerwacji ostatecznej zasobu i nie zastępuje zasobu ogólnego nazwanym członkiem zespołu.

    Dojdzie do następujących aktualizacji stanu:

    - Na stronie **Asystent planowania** wskaźniki stanu zostaną zaktualizowane i będą wskazywać, że rezerwacja została zaproponowana, a nie dokonana ostatecznie.
    - W żądaniu zasobu recenzent żądania powinien zmienić stan na **Wymaga przeglądu**.
    - W ustawieniach projektu na karcie **Zespół** wartość w polu **Stan żądania** dla ogólnego członka zespołu automatycznie zmieni się na **Wymaga weryfikacji**.

Menedżer projektu może zaakceptować lub odrzucić propozycję.

Gdy menedżerowie zasobów przetwarzają żądania zasobów, mogą używać następujących metod:

- Zaproponowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób na wszystkie wymagane godziny. Proponowane godziny są następnie dzielone między wszystkie zasoby mogące zaspokoić zapotrzebowanie na godziny. W tym scenariuszu godziny nie mogą się pokrywać.
- Zaproponowanie mniejszej ilości zasobów niż potrzeba. W tym scenariuszu proponowana dyspozycyjność zasobów jest mniejsza niż wymagana liczba godzin określona przez wnioskodawcę. Gdy wnioskodawca zaakceptuje zaproponowane zasoby, jest tworzone niezrealizowane wymaganie zasobu w celu odnotowania pozostałego zapotrzebowania.
- Zarezerwowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób do wykonania całej pracy.
- Zarezerwowanie mniejszej ilości zasobów niż potrzeba. W tym scenariuszu zarezerwowana liczba godzin jest mniejsza niż wymagana liczba godzin. System poprowadzi użytkownika do zaproponowania zasobów zamiast ich rezerwowania, dzięki czemu wnioskodawca może zweryfikować i śledzić pozostałe zapotrzebowania.

## <a name="resource-availability"></a>Dostępność zasobów

Menedżerowie zasobów muszą być w stanie przeglądać dostępne zasoby i aktualizować rezerwacje. W niektórych przypadkach nie jest to formalne żądanie (żądanie dotyczące zasobu). Menedżer zasobów musi jednak odpowiadać na nieplanowane zapotrzebowanie, które jest wysyłane za pośrednictwem innych kanałów, takich jak wiadomości e-mail, rozmowy telefoniczne lub wiadomości błyskawiczne. Menedżerowie zasobów używają **tablicy harmonogramu** do aktualizowania zasobów i rezerwacji.

Godziny pracy zasobu są używane jako podstawa do obliczania dostępności zasobu. Rezerwacje zasobów powodują zużywanie dyspozycyjności zasobów.

**Tablica harmonogramu** korzysta z kolorów i cieniowania w celu pokazania rezerwacji, dostępności, nakładania się rezerwacji oraz stanu rezerwacji. Ustawienie na **tablicy harmonogramu** pozwala na wyświetlenie legendy.

Jeśli na **tablicy harmonogramu** obok konkretnego zasobu możliwego do zarezerwowania widać znak strzałki w prawo, można rozwinąć zasób, aby wyświetlić szczegółowe informacje o pracy, dla której zasób został zarezerwowany.

Program Dynamics 365 Project Operations korzysta z aparatu Universal Resource Scheduling, dlatego jeśli zainstalowano również aplikację Dynamics 365 Field Service, można wyświetlić szczegółowe informacje o rezerwacjach zasobów dla projektów, zleceń pracy i innych encji, na które rozszerzono planowanie.

Aby wyświetlić dalsze szczegóły konkretnego zasobu, kliknij go prawym przyciskiem myszy, a zostanie otwarta karta zasobu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
