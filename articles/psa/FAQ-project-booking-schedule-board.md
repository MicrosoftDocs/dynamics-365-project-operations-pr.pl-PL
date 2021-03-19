---
title: Tworzenie rezerwacji projektu z tablicy harmonogramu
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia rezerwacji w projekcie z tablicy harmonogramu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286126"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="760f4-103">Tworzenie rezerwacji projektu z tablicy harmonogramu</span><span class="sxs-lookup"><span data-stu-id="760f4-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="760f4-104">Możesz zarezerwować zasób dla projektu bezpośrednio na karcie **Zespół** dla projektu lub wygenerować zapotrzebowanie na zasób z przydziału ogólnego członka zespołu, a następnie spełniając wygenerowane wymaganie dzięki członkowi zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="760f4-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="760f4-105">Możesz także zarezerwować zasób dla projektu bezpośrednio z tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="760f4-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="760f4-106">Możesz to zrobić na jeden z trzech sposobów:</span><span class="sxs-lookup"><span data-stu-id="760f4-106">There are three ways to do this:</span></span>

- <span data-ttu-id="760f4-107">**Przeprowadź rezerwację z wygenerowanego wymagania zasobu:** możesz wygenerować wymaganie zasobu po utworzeniu zasobu ogólnego i przypisaniu zadań w ramach projektu.</span><span class="sxs-lookup"><span data-stu-id="760f4-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="760f4-108">**Rezerwuj z wymagania podstawowego:** podstawowe wymagania są wyświetlane na tablicy harmonogramu na karcie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="760f4-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="760f4-109">**Przeprowadź rezerwację z nowego wymagania zasobu:** możesz utworzyć wymaganie zasobu od podstaw i skojarzyć je z projektem.</span><span class="sxs-lookup"><span data-stu-id="760f4-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="760f4-110">W tablicy harmonogramu wymaganie zasobu jest widoczne na karcie **Otwarte wymagania**.</span><span class="sxs-lookup"><span data-stu-id="760f4-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="760f4-111">Przeprowadź rezerwację z wygenerowanego wymagania zasobu</span><span class="sxs-lookup"><span data-stu-id="760f4-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="760f4-112">Możesz utworzyć zasób ogólny i przypisać go do jednego lub wielu zadań w ramach projektu.</span><span class="sxs-lookup"><span data-stu-id="760f4-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="760f4-113">Następnie można wygenerować wymaganie zasobu z ogólnego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="760f4-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="760f4-114">W tablicy harmonogramu ten zasób będzie widoczny na karcie **Otwarte wymagania**. Może zaistnieć konieczność użycia filtrów kolumny w siatce, jeśli masz wiele otwartych wymagań.</span><span class="sxs-lookup"><span data-stu-id="760f4-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="760f4-115">![Otwórz kartę wymagań na tablicy harmonogramu](media/FAQ-Project-Booking-Schedule-Board-1.png "Zrzut ekranu ukazujący tabelę z rezerwacjami i przypisaniami")</span><span class="sxs-lookup"><span data-stu-id="760f4-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="760f4-116">Wybierz wymaganie.</span><span class="sxs-lookup"><span data-stu-id="760f4-116">Select the requirement.</span></span> <span data-ttu-id="760f4-117">Karta **Znajdź dostępność** pojawi się w górnej części wybranego wiersza,</span><span class="sxs-lookup"><span data-stu-id="760f4-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="760f4-118">Po wybraniu karty uruchamia się tryb Asystent planowania w tablicy harmonogramu i filtruje on dostępne zasoby, które spełniają wymagania zasobu.</span><span class="sxs-lookup"><span data-stu-id="760f4-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="760f4-119">Następnie można zarezerwować zasób.</span><span class="sxs-lookup"><span data-stu-id="760f4-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="760f4-120">Można również przeciągnąć i upuścić wybrany wiersz z dołu tablicy harmonogramu do komórki zasobu w siatce powyżej.</span><span class="sxs-lookup"><span data-stu-id="760f4-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="760f4-121">Po upuszczeniu otworzy się panel **Utwórz rezerwację zasobu** po prawej stronie.</span><span class="sxs-lookup"><span data-stu-id="760f4-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="760f4-122">Wybranie **Rezerwuj** rezerwuje zasób dla zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="760f4-122">Selecting **Book** books the resource onto the project team.</span></span>

![Panel Utwórz rezerwację zasobu](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="760f4-124">Rezerwuj z wymagania podstawowego</span><span class="sxs-lookup"><span data-stu-id="760f4-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="760f4-125">Tworzenie projektu w Project Service powoduje automatyczne tworzenie wymagania zasobu o nazwie Wymaganie podstawowe.</span><span class="sxs-lookup"><span data-stu-id="760f4-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="760f4-126">Jest to puste wymaganie służące do szybkiego rezerwowania zasobu z tablicy harmonogramu bez generowania wymagania czy tworzenia go od podstaw.</span><span class="sxs-lookup"><span data-stu-id="760f4-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="760f4-127">Ponieważ wymagane jest puste, należy określić daty, a także metodę alokacji oraz godziny, jeśli ma to zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="760f4-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="760f4-128">Aby zarezerwować zasób za pomocą wymagania podstawowego, na tablicy harmonogramu wybierz kartę **Projekt**. Jeśli masz wiele projektów, być może będzie trzeba skorzystać z filtru kolumny w kolumnie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="760f4-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="760f4-129">![Filtry kolumn na tablicy harmonogramu](media/FAQ-Project-Booking-Schedule-Board-2.png "Zrzut ekranu ukazujący tabelę z rezerwacjami i przypisaniami")</span><span class="sxs-lookup"><span data-stu-id="760f4-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="760f4-130">Wybierz wymaganie, które ma tylko nazwę projektu jako nazwę i czas trwania równy zero (0).</span><span class="sxs-lookup"><span data-stu-id="760f4-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="760f4-131">Wybierz kartę **Znajdź dostępność**, która pojawia się w wierszu.</span><span class="sxs-lookup"><span data-stu-id="760f4-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="760f4-132">To przenosi tablicę harmonogramu w tryb Asystent planowania i pokazuje dostępne zasoby, które mogą zostać zarezerwowane dla projektu.</span><span class="sxs-lookup"><span data-stu-id="760f4-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="760f4-133">Ponieważ **Wymaganie podstawowe** jest wymaganiem pustym o czasie trwania zero (0), trzeba będzie ustawić czas trwania na panelu **Utwórz rezerwację zasobu** podczas wybierania i rezerwacji zasobu.</span><span class="sxs-lookup"><span data-stu-id="760f4-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="760f4-134">Można również wybrać element **Podstawowe wymaganie projektu** w dolnej części tablicy harmonogramu i przeciągnąć oraz upuścić go na zasób, rezerwując go.</span><span class="sxs-lookup"><span data-stu-id="760f4-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="760f4-135">Ponieważ **Wymaganie podstawowe** jest wymaganiem pustym o czasie trwania zero (0), trzeba będzie ustawić czas trwania na panelu **Utwórz rezerwację zasobu** podczas wybierania i rezerwacji zasobu.</span><span class="sxs-lookup"><span data-stu-id="760f4-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="760f4-136">Gdy rezerwujesz zasób za pomocą elementu **Wymaganie podstawowe** na tablicy harmonogramu, dodajesz go do zespołu projektu bez żadnych przypisań.</span><span class="sxs-lookup"><span data-stu-id="760f4-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="760f4-137">Przeprowadź rezerwację z nowego wymagania zasobu</span><span class="sxs-lookup"><span data-stu-id="760f4-137">Book from a new resource requirement</span></span>
<span data-ttu-id="760f4-138">Wykonaj poniższe kroki, aby zarezerwować z nowego wymagania zasobu.</span><span class="sxs-lookup"><span data-stu-id="760f4-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="760f4-139">Przejdź do **Wymagania zasobów** i wybierz **Nowy**, aby utworzyć nowe wymaganie zasobu.</span><span class="sxs-lookup"><span data-stu-id="760f4-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="760f4-140">Na karcie **Projekt** wybierz projekt, aby skojarzyć wymaganie z projektem.</span><span class="sxs-lookup"><span data-stu-id="760f4-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="760f4-141">W tablicy harmonogramu to nowe wymaganie jest wyświetlane jako **Wymaganie otwarte**, które możesz zrealizować.</span><span class="sxs-lookup"><span data-stu-id="760f4-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="760f4-142">Zarezerwuj zasób, aby go dodać do zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="760f4-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="760f4-143">Teraz gdy zasób jest już zarezerwowany, należy ręcznie przypisać zadania.</span><span class="sxs-lookup"><span data-stu-id="760f4-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]