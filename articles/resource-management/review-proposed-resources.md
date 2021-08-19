---
title: Przeglądanie proponowanych zasobów
description: W tym temacie zamieszczono informacje dotyczące sposobu proponowania zasobów do projektu.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a9d3f7b9194b29859ee1479fea8158067e22e819e8f190ef1659e14b7c0cd6b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998024"
---
# <a name="review-proposed-resources"></a>Przeglądanie proponowanych zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Menedżerowie zasobów mogą proponować zasób menedżerowi projektu za pomocą żądania zasobu.

1. W siatce żądań lub w oknie samego żądania wybierz pozycję **Znajdź zasoby**.
2. Na stronie **Asystent planowania** wybierz zasób, a następnie w okienku **Utwórz rezerwację zasobu** w polu **Stan rezerwacji** wybierz opcję **Zarezerwuj**.

Dojdzie do następujących aktualizacji stanu:

- Na stronie **Asystent planowania** wskaźniki stanu zostaną zaktualizowane i będą wskazywać, że rezerwacja została zaproponowana, a nie dokonana ostatecznie.
- W oknie żądania zasobu stan zmieni się na **Wymaga weryfikacji**.
- W ustawieniach projektu na karcie **Zespół** wartość w polu **Stan żądania** dla ogólnego członka zespołu zmieni się na **Wymaga weryfikacji**.

Menedżer projektu może zaakceptować lub odrzucić propozycję.

Gdy menedżerowie zasobów przetwarzają żądania zasobów, mogą używać następujących metod:

- Zaproponowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób na wszystkie wymagane godziny. Proponowane godziny są następnie dzielone między wszystkie zasoby mogące zaspokoić zapotrzebowanie na godziny. W tym scenariuszu godziny nie mogą się pokrywać.
- Zaproponowanie mniejszej ilości zasobów niż potrzeba. W tym scenariuszu proponowana dyspozycyjność zasobów jest mniejsza niż wymagana liczba godzin określona przez wnioskodawcę. W związku z tym kiedy wnioskodawca zaakceptuje zaproponowane zasoby, jest tworzone niezrealizowane wymaganie zasobu w celu odnotowania pozostałego zapotrzebowania.
- Zarezerwowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób do wykonania całej pracy.
- Zarezerwowanie mniejszej ilości zasobów niż potrzeba. W tym scenariuszu zarezerwowana liczba godzin jest mniejsza niż wymagana liczba godzin. System poprowadzi użytkownika do zaproponowania zasobów zamiast ich rezerwowania, dzięki czemu wnioskodawca może zweryfikować i śledzić pozostałe zapotrzebowania.

## <a name="resource-availability"></a>Dostępność zasobów

Bardzo ważne jest, aby menedżerowie zasobów mogli przeglądać dostępne zasoby i aktualizować rezerwacje. Czasami nie ma formalnego wymogu (żądania zasobu), ale menedżer zasobów musi reagować na nieplanowane zapotrzebowanie pochodzące z kanału takiego jak poczta e-mail, rozmowa telefoniczna lub wiadomość błyskawiczna. Menedżerowie zasobów używają tablicy harmonogramu do aktualizowania zasobów i rezerwacji.

Godziny pracy zasobu są używane jako podstawa do obliczenia dostępności zasobu. Rezerwacje zasobów powodują zużywanie dyspozycyjności zasobów.

Tablica harmonogramu korzysta z kolorów i cieniowania w celu pokazania rezerwacji, dostępności i nakładania się rezerwacji, a także stanu rezerwacji. Opcja w ustawieniach tablicy harmonogramu umożliwia wyświetlenie legendy.

Jeśli w tablicy harmonogramu obok konkretnego zasobu możliwego do zarezerwowania widać znak strzałki w prawo, można rozwinąć zasób, aby wyświetlić szczegółowe informacje o pracy, dla której zasób został zarezerwowany.

Program Dynamics 365 Project Operations korzysta z aparatu Universal Resource Scheduling, dlatego jeśli zainstalowano również aplikację Dynamics 365 Field Service, można wyświetlić szczegółowe informacje o rezerwacjach zasobów dla projektów, zleceń pracy i innych encji, na które rozszerzono planowanie.

Aby wyświetlić więcej informacji na temat konkretnego zasobu, kliknij go prawym przyciskiem myszy, a zostanie otwarta karta zasobu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]