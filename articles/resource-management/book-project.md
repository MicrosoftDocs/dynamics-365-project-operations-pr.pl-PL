---
title: Rezerwacja do projektu
description: W tym temacie zamieszczono informacje dotyczące sposobu rezerwowania zasobów do projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c87b0c32ef081f601ed79c11687f008bb454dd45
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131086"
---
# <a name="book-to-a-project"></a><span data-ttu-id="5c576-103">Rezerwacja do projektu</span><span class="sxs-lookup"><span data-stu-id="5c576-103">Book to a project</span></span>

<span data-ttu-id="5c576-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="5c576-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c576-105">Istnieją też sytuacje, w których menedżer projektu lub menedżer zasobów musi zaalokować zasób do projektu bez konieczności definiowania określonego wymagania od ogólnego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="5c576-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="5c576-106">Można to osiągnąć na trzy sposoby.</span><span class="sxs-lookup"><span data-stu-id="5c576-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="5c576-107">Rezerwacja na siatce członków zespołu</span><span class="sxs-lookup"><span data-stu-id="5c576-107">Book from the team member grid</span></span>
- <span data-ttu-id="5c576-108">Rezerwacja z tablicy harmonogramu</span><span class="sxs-lookup"><span data-stu-id="5c576-108">Book from the schedule board</span></span>
- <span data-ttu-id="5c576-109">Rezerwacja z poziomu formularza **Projekt**</span><span class="sxs-lookup"><span data-stu-id="5c576-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="5c576-110">Rezerwacja na siatce członków zespołu</span><span class="sxs-lookup"><span data-stu-id="5c576-110">Book from the team member grid</span></span>

<span data-ttu-id="5c576-111">Jeśli organizacja działa w trybie hybrydowego przydziału zasobów, menedżer projektu może zarezerwować zasób bezpośrednio do projektu, wykonując następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="5c576-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="5c576-112">W projekcie przejdź do siatki członka zespołu i wybierz pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="5c576-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="5c576-113">Określ nazwę stanowiska i rolę zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c576-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="5c576-114">W widoku menu wybierz odpowiedni zasób do zaksięgowania.</span><span class="sxs-lookup"><span data-stu-id="5c576-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="5c576-115">Po wybraniu zasobu należy zdefiniować w nim następujące informacje dotyczące zaksięgowania zasobu:</span><span class="sxs-lookup"><span data-stu-id="5c576-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="5c576-116">Data rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="5c576-116">Start date</span></span>
    - <span data-ttu-id="5c576-117">Data zakończenia</span><span class="sxs-lookup"><span data-stu-id="5c576-117">Finish date</span></span>
    - <span data-ttu-id="5c576-118">Metoda alokacji</span><span class="sxs-lookup"><span data-stu-id="5c576-118">Allocation method</span></span>
    - <span data-ttu-id="5c576-119">Liczba godzin, jeśli ma to zastosowanie</span><span class="sxs-lookup"><span data-stu-id="5c576-119">Hours, if applicable</span></span>
    - <span data-ttu-id="5c576-120">Osoba zatwierdzająca w projekcie</span><span class="sxs-lookup"><span data-stu-id="5c576-120">Project approver</span></span>

6. <span data-ttu-id="5c576-121">Wybierz pozycję **Zapisz i zamknij**</span><span class="sxs-lookup"><span data-stu-id="5c576-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="5c576-122">Rezerwacja z tablicy harmonogramu</span><span class="sxs-lookup"><span data-stu-id="5c576-122">Book from the schedule board</span></span>

<span data-ttu-id="5c576-123">Gdy menedżer zasobów musi zarezerwować zasób bezpośrednio do projektu, może użyć tablicy harmonogramu i wymagania projektu.</span><span class="sxs-lookup"><span data-stu-id="5c576-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="5c576-124">Wymaganie projektu to zapotrzebowanie na zasoby, które jest zawsze dostępne do rezerwacji w programie.</span><span class="sxs-lookup"><span data-stu-id="5c576-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="5c576-125">Wykonaj poniższe kroki, aby zarezerwować zasób z tablicy harmonogramu do projektu.</span><span class="sxs-lookup"><span data-stu-id="5c576-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="5c576-126">Przejdź do tablicy harmonogramu i na lewej stronie odfiltruj zasoby uwzględniane w zależności od wymagania.</span><span class="sxs-lookup"><span data-stu-id="5c576-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="5c576-127">W dolnym okienku wybierz kartę **Projekt**, aby wyświetlić listę zapotrzebowań na projekt.</span><span class="sxs-lookup"><span data-stu-id="5c576-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="5c576-128">Przeciągnij zapotrzebowanie na dany zasób i określ następujące informacje:</span><span class="sxs-lookup"><span data-stu-id="5c576-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="5c576-129">Data rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="5c576-129">Start date</span></span>
    - <span data-ttu-id="5c576-130">Data zakończenia</span><span class="sxs-lookup"><span data-stu-id="5c576-130">Finish date</span></span>
    - <span data-ttu-id="5c576-131">Stan rezerwacji</span><span class="sxs-lookup"><span data-stu-id="5c576-131">Booking status</span></span>
    - <span data-ttu-id="5c576-132">Metoda rezerwacji</span><span class="sxs-lookup"><span data-stu-id="5c576-132">Booking method</span></span>
    - <span data-ttu-id="5c576-133">Czas trwania</span><span class="sxs-lookup"><span data-stu-id="5c576-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="5c576-134">Rezerwacja z poziomu formularza Projekt</span><span class="sxs-lookup"><span data-stu-id="5c576-134">Book from the Project form</span></span>

<span data-ttu-id="5c576-135">Jako menedżer projektu być może będziesz musiał zarezerwować zasób do projektu, ale znać będziesz tylko kryteria a nie nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c576-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="5c576-136">Wykonaj poniższe kroki, aby za pomocą asystenta planowania znaleźć zasób na podstawie różnych dostępnych atrybutów zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c576-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="5c576-137">Przejdź do projektu i wybierz pozycję **Rezerwuj**, aby otworzyć Asystenta planowania.</span><span class="sxs-lookup"><span data-stu-id="5c576-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="5c576-138">Korzystając z filtrów po lewej stronie Asystenta planowania, zawęź kryteria i wybierz opcję **Wyszukaj.**</span><span class="sxs-lookup"><span data-stu-id="5c576-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="5c576-139">W ramach zasobów zwracanych w wyniku można przeprowadzić rezerwację.</span><span class="sxs-lookup"><span data-stu-id="5c576-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="5c576-140">W tej metodzie nie są tworzone żadne rezerwacje danego zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c576-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="5c576-141">Zamiast tego, rezerwacja dodaje go po prostu do zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="5c576-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="5c576-142">Po dodaniu członka zespołu do projektu menedżer projektu może użyć funkcji utrzymania rezerwacji lub przedłużenia rezerwacji, aby dodać wymagane rezerwacje do zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c576-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
