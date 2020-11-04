---
title: Używanie tablicy harmonogramu do rezerwowania zasobów projektu
description: W tym temacie zamieszczono informacje dotyczące rezerwowania zasobów.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: fa7e34b12f3767e89cc13ddde930e5c9f8ebc565
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082234"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="6d682-103">Używanie tablicy harmonogramu do rezerwowania zasobów projektu</span><span class="sxs-lookup"><span data-stu-id="6d682-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="6d682-104">Oprócz rezerwowania zasobów do projektu z poziomu projektu można też rezerwować zasoby ostatecznie lub wstępnie z poziomu tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="6d682-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="6d682-105">Zanim będzie można rezerwować z tablicy harmonogramu, należy utworzyć lub wygenerować wymagania zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d682-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="6d682-106">Wykonaj następujące kroki, aby utworzyć wymagania zasobów z tablicy harmonogramu:</span><span class="sxs-lookup"><span data-stu-id="6d682-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="6d682-107">Jeśli okienko **Wymagania dotyczące rezerwacji** umieszczone u dołu strony jest zwinięte, kliknij kontrolkę ekspandera, aby je rozwinąć.</span><span class="sxs-lookup"><span data-stu-id="6d682-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="6d682-108">W okienku **Wymagania dotyczące rezerwacji** na karcie **Projekt** zaznacz wymaganie, dla którego chcesz dokonać rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="6d682-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![Wymaganie zaznaczone na karcie Projekt](media/Resource-Management-image73.png)

3. <span data-ttu-id="6d682-110">Wybierz pozycję **Znajdź dostępność** w celu wyfiltrowania zasobów możliwych do zarezerwowania i wyświetlenia dostępnych zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d682-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="6d682-111">Zaznacz jeden lub więcej zasobów w tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="6d682-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="6d682-112">W okienku **Utwórz rezerwację zasobu** , które znajduje się przy prawej krawędzi strony, wprowadź informacje o rezerwacji, a następnie wybierz opcję **Zarezerwuj i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="6d682-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Okienko Utwórz rezerwację zasobu dla wybranego zasobu możliwego do zarezerwowania](media/Resource-Management-image74.png)

6. <span data-ttu-id="6d682-114">Kiedy wymaganie jest zaznaczone w okienku **Utwórz rezerwację zasobu** , kliknij jedną lub więcej komórek zasobów, aby utworzyć rezerwację.</span><span class="sxs-lookup"><span data-stu-id="6d682-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Zaznaczenie wielu komórek dla zasobu](media/Resource-Management-image75.png)

7. <span data-ttu-id="6d682-116">Kliknij opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="6d682-116">Select **Book**.</span></span>

<span data-ttu-id="6d682-117">Wymaganie zostanie zaspokojone przy użyciu wybranego zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d682-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="6d682-118">Zwróć uwagę, że w okienku **Wymagania dotyczące rezerwacji** wymaganie zostało zaktualizowane, a zasób jest wyświetlany jako zarezerwowany w projekcie.</span><span class="sxs-lookup"><span data-stu-id="6d682-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Zasób zarezerwowany w projekcie](media/Resource-Management-image76.png)
