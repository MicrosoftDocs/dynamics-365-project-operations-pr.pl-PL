---
title: Przeglądanie proponowanych zasobów
description: W tym temacie zamieszczono informacje dotyczące sposobu proponowania zasobów do projektu.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897374"
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

## <a name="billable-utilization"></a>Wykorzystanie podlegające rozliczeniu

Zasoby mogą mieć docelowe wykorzystanie podlegające rozliczeniu. To docelowe wykorzystanie jest zdefiniowane jako atrybut w domyślnej roli zasobu albo ustawione w rekordzie konkretnego zasobu możliwego do zarezerwowania. Obliczenia wykorzystania bazują na rzeczywistej liczbie godzin zaraportowanej przez zasoby przy użyciu zatwierdzonych wpisów czasu.

Poniższe wzory służą do obliczania wykorzystania:

- Wykorzystanie podlegające rozliczeniu = odpłatne rzeczywiste godziny pracy ÷ dyspozycyjność zasobu
- Wykorzystanie niepodlegające rozliczeniu = rzeczywisty czas o identyfikatorze typu rozliczania = nieodpłatne, uzupełniające lub niedostępne ÷ dyspozycyjność zasobu
- Wewnętrzne = rzeczywisty czas bez kontraktu sprzedaży ÷ dyspozycyjności zasobu
- Dyspozycyjności zasobu = godziny pracy zasobu – poza biurem — dni wolne od pracy

Widok **Wykorzystanie zasobów** jest dostępny z poziomu okienka **Zasoby**.

Każda komórka w siatce reprezentuje procent wykorzystania zasobu podlegający rozliczeniu w okresie, takim jak dzień, tydzień lub miesiąc. Poniższe wzory służą do kolorowania komórek:

- **Zielony:** wykorzystanie podlegające rozliczeniu \>= docelowe wykorzystanie zasobu
- **Żółty:** docelowe wykorzystanie – 20 \<= wykorzystanie podlegające rozliczeniu \< docelowe wykorzystanie
- **Czerwony:** wykorzystanie podlegające rozliczeniu \< docelowe wykorzystanie – 20

Ponieważ widok **Wykorzystanie zasobów** jest oparty na tablicy harmonogramu, można używać funkcji filtrowania dostępnych w tablicy harmonogramu do filtrowania wyników.

Siatka wymaga skonfigurowania docelowego wykorzystania dla roli lub konkretnego zasobu. Aby wykonać te czynności konfiguracyjne, wybierz kolejno opcje **Zasoby** \> **Role zasobu**.

Ponadto każdemu zasobowi możliwemu do zarezerwowania musi być przypisana rola domyślna. Wybierz kolejno opcje **Zasoby** \> **Zasoby**. Na karcie **Project Service** sprawdź, czy została zdefiniowana rola zasobu, a pole **Jest domyślna** ma ustawioną wartość **Tak**. Można dodać kolejne role, w których **Jest domyślna = Nie**. Rola z atrybutem **Jest domyślna = Tak** jest używana do oceny wykorzystania zasobu w stosunku do wartości docelowej dla tej roli.

Na karcie **Project Service** można również skonfigurować konkretne docelowe wykorzystanie zasobu. Następnie aparat obliczania wykorzystania na podstawie docelowego wykorzystania ocenia wartość docelową dla zasobu, a nie dla jego domyślnej roli.

Wykorzystanie jest pokazywane dla zasobu tylko w przypadku, gdy zasób ma zatwierdzony czas odpłatny w okresie wyświetlanym w siatce.

## <a name="resource-availability"></a>Dostępność zasobów

Bardzo ważne jest, aby menedżerowie zasobów mogli przeglądać dostępne zasoby i aktualizować rezerwacje. Czasami nie ma formalnego wymogu (żądania zasobu), ale menedżer zasobów musi reagować na nieplanowane zapotrzebowanie pochodzące z kanału takiego jak poczta e-mail, rozmowa telefoniczna lub wiadomość błyskawiczna. Menedżerowie zasobów używają tablicy harmonogramu do aktualizowania zasobów i rezerwacji.

Godziny pracy zasobu są używane jako podstawa do obliczenia dostępności zasobu. Rezerwacje zasobów powodują zużywanie dyspozycyjności zasobów.

Tablica harmonogramu korzysta z kolorów i cieniowania w celu pokazania rezerwacji, dostępności i nakładania się rezerwacji, a także stanu rezerwacji. Opcja w ustawieniach tablicy harmonogramu umożliwia wyświetlenie legendy.

Jeśli w tablicy harmonogramu obok konkretnego zasobu możliwego do zarezerwowania widać znak strzałki w prawo, można rozwinąć zasób, aby wyświetlić szczegółowe informacje o pracy, dla której zasób został zarezerwowany.

Program Dynamics 365 Project Operations korzysta z aparatu Universal Resource Scheduling, dlatego jeśli zainstalowano również aplikację Dynamics 365 Field Service, można wyświetlić szczegółowe informacje o rezerwacjach zasobów dla projektów, zleceń pracy i innych encji, na które rozszerzono planowanie.

Aby wyświetlić więcej informacji na temat konkretnego zasobu, kliknij go prawym przyciskiem myszy, a zostanie otwarta karta zasobu.

