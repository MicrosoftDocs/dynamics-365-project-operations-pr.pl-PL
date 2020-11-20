---
title: Przypisywanie zasobu do zadania
description: W tym temacie zamieszczono informacje dotyczące sposobu przypisywania zasobów do zadań.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b7aef799ec4b90d602a6f3641cbac06264664f00
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125146"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="6eb74-103">Przypisywanie zasobu do zadania</span><span class="sxs-lookup"><span data-stu-id="6eb74-103">Assign a resource to a task</span></span>

<span data-ttu-id="6eb74-104">Istnieją trzy sposoby przypisywania zasobu do zadania w programie Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6eb74-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="6eb74-105">Zarezerwuj zasób jako członek zespołu, a następnie przypisz zasób do zadania</span><span class="sxs-lookup"><span data-stu-id="6eb74-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="6eb74-106">Możesz dodać zasób do zespołu projektu, a następnie przypisać zasób do zadań w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="6eb74-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="6eb74-107">Na karcie **Członek zespołu** dodaj nowego członka zespołu, wybierając **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="6eb74-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="6eb74-108">Otworzy się panel **Szybkie tworzenie członków zespołu**, gdzie można wybrać nazwę zasobu, który można zarezerwować, i ustawić rolę.</span><span class="sxs-lookup"><span data-stu-id="6eb74-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="6eb74-109">Wybierz jedną z następujących metod alokacji, aby zarezerwować zasób:</span><span class="sxs-lookup"><span data-stu-id="6eb74-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="6eb74-110">**Pełna dyspozycyjność** rezerwuje pełną dyspozycyjność zasobu dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="6eb74-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="6eb74-111">**Dyspozycyjność procentowa** rezerwuje zasób procentowo dla dyspozycyjności zasobu dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="6eb74-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="6eb74-112">**Według godzin — rozłóż równomiernie** rezerwuje zasób na określoną liczbą godzin, rozkładając je równomiernie w ciągu dnia dla określonych dat Od i Do.</span><span class="sxs-lookup"><span data-stu-id="6eb74-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="6eb74-113">**Według godzin — Najwięcej na początku** rezerwuje zasób na określoną liczbą godzin, kładąc nacisk na godziny początkowe w ciągu dnia dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="6eb74-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="6eb74-114">**Brak** dodaje zasób do zespołu, ale nie tworzy żadnych rezerwacji, które absorbują ich dyspozycyjność.</span><span class="sxs-lookup"><span data-stu-id="6eb74-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="6eb74-115">W siatce **Harmonogram** dla zadania wybierz ikonę **Zasób** w komórce zasobu, a następnie w obszarze **Członkowie zespołu** wybierz członka zespołu, który został właśnie dodany.</span><span class="sxs-lookup"><span data-stu-id="6eb74-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="6eb74-116">Na kartach **Członek zespołu** i **Uzgadnianie** zasób ukazuje zarezerwowane i przypisane godziny.</span><span class="sxs-lookup"><span data-stu-id="6eb74-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="6eb74-117">Godziny powinny, ale nie muszą być takie same, ponieważ rezerwacje i przypisania nie są ściśle powiązane.</span><span class="sxs-lookup"><span data-stu-id="6eb74-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="6eb74-118">Karta **Uzgadnianie** przedstawia szczegóły, gdy są one inne, np. jeśli przypiszesz do zasobu więcej godzin, niż zarezerwowano.</span><span class="sxs-lookup"><span data-stu-id="6eb74-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="6eb74-119">W razie potrzeby można skorygować informacje, rozszerzając rezerwacje zasobu albo zmieniając przypisanie.</span><span class="sxs-lookup"><span data-stu-id="6eb74-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="6eb74-120">Tworzenie ogólnego członka zespołu za pośrednictwem przypisania zadania</span><span class="sxs-lookup"><span data-stu-id="6eb74-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="6eb74-121">Podczas tworzenia ogólnego członka zespołu poprzez przypisanie zadania tworzysz zasób zastępczy lub zasób ogólny, który opisuje cechy zasobu nazwanego, który ma ostatecznie pracować nad zadaniami.</span><span class="sxs-lookup"><span data-stu-id="6eb74-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="6eb74-122">Następnie generujesz wymaganie (lub przesyłasz zgłoszenie korzystające z tego wymagania), które jest używane do wyszukiwania i rezerwowania nazwanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="6eb74-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="6eb74-123">W siatce **Harmonogram** dla zadania wybierz ikonę **Zasób** w komórce zasobu.</span><span class="sxs-lookup"><span data-stu-id="6eb74-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="6eb74-124">Wpisz nazwę, jaka ma stać się nazwą zasobu zastępczego.</span><span class="sxs-lookup"><span data-stu-id="6eb74-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="6eb74-125">Na przykład Menedżer programu.</span><span class="sxs-lookup"><span data-stu-id="6eb74-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="6eb74-126">Kliknij przycisk **Utwórz**, a następnie w polu **Szybkie tworzenie członka zespołu projektu** ustaw rolę zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="6eb74-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="6eb74-127">Możesz nadal przypisywać zadania do tego zasobu zastępczego, wybierając zasób w oknie **Selektor zasobów** dla zadania.</span><span class="sxs-lookup"><span data-stu-id="6eb74-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="6eb74-128">Są one wyświetlane w obszarze **Członkowie zespołu**.</span><span class="sxs-lookup"><span data-stu-id="6eb74-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="6eb74-129">Po zakończeniu przypisywania zasobu ogólnego wybierz zasób ogólny na karcie **Zespół**, a następnie wybierz opcję **Generuj wymaganie**, aby utworzyć wymaganie zasobu dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="6eb74-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="6eb74-130">Wybierz **Zarezerwuj** dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="6eb74-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="6eb74-131">Następnie możesz użyć tablicy harmonogramu, aby wyszukać i zarezerwować zasób.</span><span class="sxs-lookup"><span data-stu-id="6eb74-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="6eb74-132">Można również przesłać wymagań do spełnienia przez Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="6eb74-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="6eb74-133">Gdy zasób ogólny jest zrealizowany przez zasób nazwany, zasób ogólny jest usuwany z zespołu a przypisania zadań dla zasobu ogólnego są przypisywane do zasobu nazwanego, który zrealizował wymaganie zasobu dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="6eb74-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="6eb74-134">Przypisywanie nazwanego zasobu z listy wszystkich zasobów, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="6eb74-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="6eb74-135">Możesz użyć pola wyszukiwania w oknie **Selektor zasobów**, aby wyszukać wszystkie zasoby możliwe do zarezerwowania i przypisać je do zadania.</span><span class="sxs-lookup"><span data-stu-id="6eb74-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="6eb74-136">Zasoby przypisane w ten sposób zostaną dodane do zespołu bez żadnych rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="6eb74-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="6eb74-137">Jest to sposób podobny do dodawania członka zespołu i wybierania opcji Brak jako metody alokacji.</span><span class="sxs-lookup"><span data-stu-id="6eb74-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="6eb74-138">Zasoby będą wyświetlane na kartach **Zespół** i **Uzgadnianie** jako zasoby z przydziałami i deficytem rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="6eb74-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="6eb74-139">Zarezerwuj je, jeśli chcesz użyć ich dostępności.</span><span class="sxs-lookup"><span data-stu-id="6eb74-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="6eb74-140">W siatce **Harmonogram** dla zadania wybierz ikonę **Zasób** w komórce zasobu.</span><span class="sxs-lookup"><span data-stu-id="6eb74-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="6eb74-141">Zacznij wpisywać nazwę.</span><span class="sxs-lookup"><span data-stu-id="6eb74-141">Start typing a name.</span></span> <span data-ttu-id="6eb74-142">Wyniki wyszukiwania nazwy są wyświetlane w oknie **Selektor zasobów** w obszarze **Inne zasoby**.</span><span class="sxs-lookup"><span data-stu-id="6eb74-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="6eb74-143">Zaznacz zasób, który chcesz przypisać do zadania.</span><span class="sxs-lookup"><span data-stu-id="6eb74-143">Select the resource that you want to assign to the task.</span></span>

