---
title: Nawigowanie po interfejsie użytkownika
description: W tym temacie zamieszczono informacje o Zarządzaniu projektem w Dynamics 365 Project operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286756"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="3a940-103">Nawigowanie po interfejsie użytkownika</span><span class="sxs-lookup"><span data-stu-id="3a940-103">Navigating the user interface</span></span>

<span data-ttu-id="3a940-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="3a940-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="3a940-105">Omówienie</span><span class="sxs-lookup"><span data-stu-id="3a940-105">Overview</span></span>

<span data-ttu-id="3a940-106">Główny formularz projektu jest podzielony na kilka kart.</span><span class="sxs-lookup"><span data-stu-id="3a940-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="3a940-107">Na każdej karcie znajduje się inny poziom szczegółów projektu.</span><span class="sxs-lookup"><span data-stu-id="3a940-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="3a940-108">**Podsumowanie**: zawiera opis projektu i agreguje zarówno planowaną, jak i rzeczywistą wydajność projektu.</span><span class="sxs-lookup"><span data-stu-id="3a940-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Karta i pola podsumowania](media/navigation7.png)

- <span data-ttu-id="3a940-110">**Zadania**: zawiera szczegółowe informacje dotyczące struktury podziału pracy reprezentowane przez widok siatki, widok tablicy i wykres Gantta.</span><span class="sxs-lookup"><span data-stu-id="3a940-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Karta i pola zadania](media/navigation8.png)

- <span data-ttu-id="3a940-112">**Zespół**: zawiera szczegółowe informacje dotyczące uczestników projektu.</span><span class="sxs-lookup"><span data-stu-id="3a940-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="3a940-113">Przydzielone nakłady pracy dla każdego członka zespołu są również podsumowane w tym widoku.</span><span class="sxs-lookup"><span data-stu-id="3a940-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Karta i pola zespół](media/navigation9.png)

- <span data-ttu-id="3a940-115">**Przydziały zasobów**: program dostarcza etapowy widok nakładu pracy dla każdego zasobu w projekcie.</span><span class="sxs-lookup"><span data-stu-id="3a940-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Karta i pola przydziałów zasobów](media/navigation10.png)

- <span data-ttu-id="3a940-117">**Uzgadnianie zasobu**: zawiera okresowy widok różnic między przydziałami poszczególnych nazwanych zasobów i ich rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="3a940-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Karta i pola uzgadniania zasobów](media/navigation11.png)

- <span data-ttu-id="3a940-119">**Oszacowania**: zawiera okresowy widok szacunków kosztów i sprzedaży projektu.</span><span class="sxs-lookup"><span data-stu-id="3a940-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Karta i pola oszacowania](media/navigation12.png)

- <span data-ttu-id="3a940-121">**Śledzenie**: zawiera widok pokazujący postępy zadań w strukturze podziału prac w zakresie nakładów pracy, kosztów i sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="3a940-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Karta i pola śledzenie](media/navigation13.png)

- <span data-ttu-id="3a940-123">**Sprzedaż**: zawiera głębokie łącza do ofert i kontraktów skojarzonych z projektem.</span><span class="sxs-lookup"><span data-stu-id="3a940-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="3a940-124">**Oszacowania kosztów**: zawiera siatkę definiującą wydatki na projekt na podstawie kategorii wydatków organizacyjnych.</span><span class="sxs-lookup"><span data-stu-id="3a940-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Karta i pola oszacowania wydatków](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="3a940-126">Formanty siatki</span><span class="sxs-lookup"><span data-stu-id="3a940-126">Grid controls</span></span>

<span data-ttu-id="3a940-127">Poniżej znajduje się zwięzły przegląd typowych formantów dostępnych na różnych kartach planowania projektów.</span><span class="sxs-lookup"><span data-stu-id="3a940-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="3a940-128">Refresh</span><span class="sxs-lookup"><span data-stu-id="3a940-128">Refresh</span></span>

<span data-ttu-id="3a940-129">**Odświeżenie**: pobiera najnowsze dane z serwera, jeśli wprowadzone zmiany wystąpiły po załadowaniu siatki.</span><span class="sxs-lookup"><span data-stu-id="3a940-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Przycisk Odśwież](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="3a940-131">Grupuj wg</span><span class="sxs-lookup"><span data-stu-id="3a940-131">Group by</span></span>

<span data-ttu-id="3a940-132">**Grupuj według**: program aktualizuje pogrupowanie wierszy w siatce, aby odzwierciedlić zasoby, role lub kategorie zależnie od potrzeb użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a940-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Przycisk Grupuj według](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="3a940-134">Poprzedni/Następny</span><span class="sxs-lookup"><span data-stu-id="3a940-134">Previous/Next</span></span>

<span data-ttu-id="3a940-135">**Poprzedni**/**Następny**: Uaktualnij wyświetlane okresy na siatce faz czasowych.</span><span class="sxs-lookup"><span data-stu-id="3a940-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Przyciski poprzedni i następny](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="3a940-137">Skala czasu</span><span class="sxs-lookup"><span data-stu-id="3a940-137">Timescale</span></span>

<span data-ttu-id="3a940-138">**Skala czasowa**: zmiana podsumowania danych faz czasowych: dni, tygodnie, miesiące i lata.</span><span class="sxs-lookup"><span data-stu-id="3a940-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Przycisk skali czasowej](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="3a940-140">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="3a940-140">Expand</span></span>

<span data-ttu-id="3a940-141">**Rozwiń**: renderowanie widocznej siatki na pełnym ekranie dzięki większym możliwościom wyświetlenia dodatkowych ról.</span><span class="sxs-lookup"><span data-stu-id="3a940-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Przycisk Rozwiń](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="3a940-143">Fazy czasowe według</span><span class="sxs-lookup"><span data-stu-id="3a940-143">Time-phase by</span></span>

<span data-ttu-id="3a940-144">**Fazy czasowe według**: aktualizacja pogrupowania wierszy w siatce w celu odzwierciedlenia oszacowań kosztów dotyczących oszacowań sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="3a940-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="3a940-145">Formant ma zastosowanie również do skryptu oszacowania i śledzenia.</span><span class="sxs-lookup"><span data-stu-id="3a940-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Przycisk fazy czasowe według](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="3a940-147">Dodaj kolumnę</span><span class="sxs-lookup"><span data-stu-id="3a940-147">Add column</span></span>

<span data-ttu-id="3a940-148">**Dodaj kolumnę**: umożliwia użytkownikowi zdefiniowanie widocznych kolumn w siatce.</span><span class="sxs-lookup"><span data-stu-id="3a940-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="3a940-149">Do siatek w formularzu **planowania projektu** można dodać tylko niektóre z gotowych kolumn.</span><span class="sxs-lookup"><span data-stu-id="3a940-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Przycisk dodawania kolumny](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]