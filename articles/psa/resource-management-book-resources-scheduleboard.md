---
title: Używanie tablicy harmonogramu do rezerwowania zasobów projektu
description: W tym temacie zamieszczono informacje dotyczące rezerwowania zasobów.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 89eac463fd80378a6cfdb53741afbbd1444d5662
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283201"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="fc518-103">Używanie tablicy harmonogramu do rezerwowania zasobów projektu</span><span class="sxs-lookup"><span data-stu-id="fc518-103">Use the Schedule Board to book project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fc518-104">Oprócz rezerwowania zasobów do projektu z poziomu projektu można też rezerwować zasoby ostatecznie lub wstępnie z poziomu tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fc518-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="fc518-105">Zanim będzie można rezerwować z tablicy harmonogramu, należy utworzyć lub wygenerować wymagania zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc518-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="fc518-106">Wykonaj następujące kroki, aby utworzyć wymagania zasobów z tablicy harmonogramu:</span><span class="sxs-lookup"><span data-stu-id="fc518-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="fc518-107">Jeśli okienko **Wymagania dotyczące rezerwacji** umieszczone u dołu strony jest zwinięte, kliknij kontrolkę ekspandera, aby je rozwinąć.</span><span class="sxs-lookup"><span data-stu-id="fc518-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="fc518-108">W okienku **Wymagania dotyczące rezerwacji** na karcie **Projekt** zaznacz wymaganie, dla którego chcesz dokonać rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="fc518-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![Wymaganie zaznaczone na karcie Projekt](media/Resource-Management-image73.png)

3. <span data-ttu-id="fc518-110">Wybierz pozycję **Znajdź dostępność** w celu wyfiltrowania zasobów możliwych do zarezerwowania i wyświetlenia dostępnych zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc518-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="fc518-111">Zaznacz jeden lub więcej zasobów w tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fc518-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="fc518-112">W okienku **Utwórz rezerwację zasobu**, które znajduje się przy prawej krawędzi strony, wprowadź informacje o rezerwacji, a następnie wybierz opcję **Zarezerwuj i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="fc518-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Okienko Utwórz rezerwację zasobu dla wybranego zasobu możliwego do zarezerwowania](media/Resource-Management-image74.png)

6. <span data-ttu-id="fc518-114">Kiedy wymaganie jest zaznaczone w okienku **Utwórz rezerwację zasobu**, kliknij jedną lub więcej komórek zasobów, aby utworzyć rezerwację.</span><span class="sxs-lookup"><span data-stu-id="fc518-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Zaznaczenie wielu komórek dla zasobu](media/Resource-Management-image75.png)

7. <span data-ttu-id="fc518-116">Kliknij opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="fc518-116">Select **Book**.</span></span>

<span data-ttu-id="fc518-117">Wymaganie zostanie zaspokojone przy użyciu wybranego zasobu.</span><span class="sxs-lookup"><span data-stu-id="fc518-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="fc518-118">Zwróć uwagę, że w okienku **Wymagania dotyczące rezerwacji** wymaganie zostało zaktualizowane, a zasób jest wyświetlany jako zarezerwowany w projekcie.</span><span class="sxs-lookup"><span data-stu-id="fc518-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Zasób zarezerwowany w projekcie](media/Resource-Management-image76.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]