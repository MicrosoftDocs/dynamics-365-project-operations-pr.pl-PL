---
title: Nawigowanie po interfejsie użytkownika
description: W tym temacie zamieszczono informacje o Zarządzaniu projektem w Dynamics 365 Project operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 715a8bdb9a1f38f71b4c42f5307ed4a5c7170ef6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014264"
---
# <a name="navigating-the-user-interface"></a>Nawigowanie po interfejsie użytkownika

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

## <a name="overview"></a>Omówienie

Główny formularz projektu jest podzielony na kilka kart. Na każdej karcie znajduje się inny poziom szczegółów projektu.

- **Podsumowanie**: zawiera opis projektu i agreguje zarówno planowaną, jak i rzeczywistą wydajność projektu.

    ![Karta i pola podsumowania](media/navigation7.png)

- **Zadania**: zawiera szczegółowe informacje dotyczące struktury podziału pracy reprezentowane przez widok siatki, widok tablicy i wykres Gantta.

    ![Karta i pola zadania](media/navigation8.png)

- **Zespół**: zawiera szczegółowe informacje dotyczące uczestników projektu. Przydzielone nakłady pracy dla każdego członka zespołu są również podsumowane w tym widoku.

    ![Karta i pola zespół](media/navigation9.png)

- **Przydziały zasobów**: program dostarcza etapowy widok nakładu pracy dla każdego zasobu w projekcie.

    ![Karta i pola przydziałów zasobów](media/navigation10.png)

- **Uzgadnianie zasobu**: zawiera okresowy widok różnic między przydziałami poszczególnych nazwanych zasobów i ich rezerwacji.

    ![Karta i pola uzgadniania zasobów](media/navigation11.png)

- **Oszacowania**: zawiera okresowy widok szacunków kosztów i sprzedaży projektu.

    ![Karta i pola oszacowania](media/navigation12.png)

- **Śledzenie**: zawiera widok pokazujący postępy zadań w strukturze podziału prac w zakresie nakładów pracy, kosztów i sprzedaży.

    ![Karta i pola śledzenie](media/navigation13.png)

- **Sprzedaż**: zawiera głębokie łącza do ofert i kontraktów skojarzonych z projektem.

- **Oszacowania kosztów**: zawiera siatkę definiującą wydatki na projekt na podstawie kategorii wydatków organizacyjnych.

    ![Karta i pola oszacowania wydatków](media/navigation14.png)

## <a name="grid-controls"></a>Formanty siatki

Poniżej znajduje się zwięzły przegląd typowych formantów dostępnych na różnych kartach planowania projektów.

### <a name="refresh"></a>Refresh

**Odświeżenie**: pobiera najnowsze dane z serwera, jeśli wprowadzone zmiany wystąpiły po załadowaniu siatki.

![Przycisk Odśwież](media/navigation7.png)

### <a name="group-by"></a>Grupuj wg

**Grupuj według**: program aktualizuje pogrupowanie wierszy w siatce, aby odzwierciedlić zasoby, role lub kategorie zależnie od potrzeb użytkownika.

![Przycisk Grupuj według](media/navigation6.png)

### <a name="previousnext"></a>Poprzedni/Następny

**Poprzedni**/**Następny**: Uaktualnij wyświetlane okresy na siatce faz czasowych.

![Przyciski poprzedni i następny](media/navigation2.png)

### <a name="timescale"></a>Skala czasu

**Skala czasowa**: zmiana podsumowania danych faz czasowych: dni, tygodnie, miesiące i lata.

![Przycisk skali czasowej](media/navigation3.png)

### <a name="expand"></a>Rozwiń

**Rozwiń**: renderowanie widocznej siatki na pełnym ekranie dzięki większym możliwościom wyświetlenia dodatkowych ról.

![Przycisk Rozwiń](media/navigation4.png)

### <a name="time-phase-by"></a>Fazy czasowe według

**Fazy czasowe według**: aktualizacja pogrupowania wierszy w siatce w celu odzwierciedlenia oszacowań kosztów dotyczących oszacowań sprzedaży. Formant ma zastosowanie również do skryptu oszacowania i śledzenia.

![Przycisk fazy czasowe według](media/navigation0.png)

### <a name="add-column"></a>Dodaj kolumnę

**Dodaj kolumnę**: umożliwia użytkownikowi zdefiniowanie widocznych kolumn w siatce. Do siatek w formularzu **planowania projektu** można dodać tylko niektóre z gotowych kolumn.

![Przycisk dodawania kolumny](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]