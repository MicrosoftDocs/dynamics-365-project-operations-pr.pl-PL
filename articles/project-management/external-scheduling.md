---
title: Planowanie zewnętrzne
description: Ten artykuł zawiera informacje o planowaniu zewnętrznym.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736970"
---
# <a name="external-scheduling"></a>Planowanie zewnętrzne

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Tryb planowania zewnętrznego pozwala na natywne tworzenie, aktualizowanie i usuwanie encji powiązanych ze strukturami podziału pracy (SPP), ale bez bieżących ograniczeń wymuszanych przez program Microsoft Project for the Web. Umożliwia również ograniczoną walidację. Ten tryb powinien być używany tylko przez następujących klientów:

- Klienci z narzędziami wymaganymi do definiowania SPP poza logiką planowania dostarczaną przez aplikację Project Operations
- Klienci, którzy muszą zarządzać hierarchią harmonogramu, zależnościami lub czasem trwania zadania

> [!IMPORTANT]
> Dane, które nie zostały poprawnie wprowadzone w encjach powiązanych z SPP, mogą nie być renderowane w siatce uzgadniania zasobów, siatce szacowania, siatce śledzenia lub siatce przypisania zasobów.

## <a name="configuration"></a>Configuration

Ten funkcjonalność jest włączona domyślnie. Jednak na gotowej stronie głównej projektów pole pokrewne nie jest domyślnie widoczne. Aby włączyć pole, w portalu Maker Portal otwórz stronę główną encji projektu, zaznacz pole **Aparat planowania**, a następnie zmień pole na **Domyślnie widoczne**. Jeśli nie używasz gotowej strony głównej projektu, edytuj istniejącą stronę i dodaj do niej pole **Aparat planowania**.

## <a name="settings"></a>Ustawienia

Aby korzystać z trybu planowania zewnętrznego, należy najpierw utworzyć nowy projekt i wybrać aparat planowania **Zaplanowane zewnętrznie** z listy rozwijanej na stronie głównej projektu. Po skonfigurowaniu tego trybu dla projektu nie można go już zmienić.

## <a name="viewing-the-wbs"></a>Wyświetlanie SPP

Jeśli projekt jest zaplanowany zewnętrznie, dostęp do programu Project for the Web dla tego projektu jest ograniczony. Aby wyświetlić SPP, należy przejść do siatki śledzenia, w której jest wyświetlana pełna struktura SPP.

## <a name="creating-and-editing-the-wbs"></a>Tworzenie i edytowanie SPP

Jeśli dla projektu jest włączone planowanie zewnętrzne, należy zdefiniować dane dla wszystkich encji powiązanych z SPP, w tym zadania, członków zespołu, przypisania zasobów i zależności.

Poniższa ilustracja przedstawia model danych dla planowania projektu.

![Model danych planowania projektu.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Ograniczenia funkcjonalne

Następujące operacje są niedozwolone w projektach zaplanowanych zewnętrznie.

### <a name="project-planning"></a>Planowanie projektu

- **Kopiuj projekt** — ta operacja nie jest obsługiwana w projektach zaplanowanych zewnętrznie.
- **Przenieś projekt** — zmiany daty rozpoczęcia projektu nie będą przenosić rozpoczęcia zadań lub przypisań zasobów w SPP.
- **Aktualizacja menedżera projektu** — zmiany menedżera projektu na stronie głównej projektu nie będą automatycznie tworzyć nowego członka zespołu projektowego, dopóki projekt nie zostanie przekonwertowany.
- **Aktualizacja szablonu godzin pracy dla projektu** — zmiany w szablonie godziny pracy dla projektu nie będą przeliczane na harmonogram projektu.
- **Rozkłady przypisań zasobów** — utworzenie przypisań zasobów nie będzie automatycznie aktualizować pola **mdyn\_PlannedWork**. To pole służy do przechowywania rozkładów dla nakładów pracy przy przypisywaniu zasobów. Jeśli pokazujesz okresowy nakład pracy w siatce przypisań zasobów lub siatce uzgadniania zasobów, należy zdefiniować prawidłowe rozkłady przypisań zasobów. Te rozkłady muszą być poprawnie sformatowane, tak aby wyzwalały obliczenia rozkładów kosztów, jak i rozkładów cen sprzedaży. Zaleca się utworzenie projektu testowego zaplanowanego przez program Project for the Web, a następnie przejrzenie skojarzonych danych w celu potwierdzenia wymagań i formatowania.

### <a name="resource-management"></a>Zarządzanie zasobami

- **Realizacja zasobu ogólnego** — realizacja zasobu ogólnego nie jest obsługiwana w projektach zaplanowanych zewnętrznie. Próba zrealizowania aktywnych otwartych wymagań spowoduje utworzenie nowych członków zespołu projektowego, ale nie spowoduje usunięcia członka zespołu ogólnego ani zastąpienia członka zespołu ogólnego w istniejących przypisaniach zasobów.
- **Usuń członka zespołu** — usunięcie członka zespołu nie powoduje automatycznie usunięcia przypisań zasobów.

### <a name="quoting-and-contracting"></a>Sporządzanie ofert i zawieranie kontraktów

- **Importowanie szczegółów pozycji oferty i pozycji kontraktu** — podczas importowania szczegółów pozycji oferty lub kontraktu z projektu aplikacja została przetestowana w celu obsługi maksymalnie 500 zadań w ramach umowy WBA na podstawie limitu 20 przypisań na zadanie.

### <a name="actuals-and-invoicing"></a>Wartości rzeczywiste i fakturowanie

- Chociaż nie ma żadnych zmian w istniejących walidacjach między SPP a transakcjami finansowymi, ważne jest, aby upewnić się, że wszystkie transakcje w dół działają zgodnie z oczekiwaniami w gotowym modelu danych.
