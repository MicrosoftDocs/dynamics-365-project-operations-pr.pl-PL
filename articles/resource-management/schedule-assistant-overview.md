---
title: Omówienie asystenta planowania
description: W tym temacie zamieszczono informacje dotyczące pracy z asystentem planowania zasobów w celu ich rezerwowania.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279241"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="563da-103">Omówienie asystenta planowania</span><span class="sxs-lookup"><span data-stu-id="563da-103">Schedule assistant overview</span></span>

<span data-ttu-id="563da-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="563da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="563da-105">Asystent planowania jest używany do rezerwowania zasobów na podstawie wymagań określonych przez menedżera projektu.</span><span class="sxs-lookup"><span data-stu-id="563da-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="563da-106">Asystent planowania opiera się na parametrach zawartych w wymaganiu zasobu w celu wyszukania danego zasobu.</span><span class="sxs-lookup"><span data-stu-id="563da-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="563da-107">Asystent planowania rekomenduje zasoby spełniające odpowiednie wymagania, takie jak czas i potrzebne umiejętności.</span><span class="sxs-lookup"><span data-stu-id="563da-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="563da-108">Po zidentyfikowaniu odpowiednich zasobów, menedżer zasobów lub menedżer projektu może dokonać jego rezerwacji na zadania.</span><span class="sxs-lookup"><span data-stu-id="563da-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="563da-109">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="563da-109">Prerequisites</span></span>

<span data-ttu-id="563da-110">Asystent planowania jest częścią rozwiązania Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="563da-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="563da-111">To rozwiązanie jest dołączone i instalowane z rozwiązaniami Dynamics 365 Project Operations, Dynamics 365 Field Service oraz Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="563da-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="563da-112">Dopasowywanie wymagań i zasobów</span><span class="sxs-lookup"><span data-stu-id="563da-112">Matching requirements and resources</span></span>

<span data-ttu-id="563da-113">Zapotrzebowanie wygenerowanego zasobu jest oparte na szczegółach, takich jak:</span><span class="sxs-lookup"><span data-stu-id="563da-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="563da-114">Charakterystyki</span><span class="sxs-lookup"><span data-stu-id="563da-114">Characteristics</span></span>
-   <span data-ttu-id="563da-115">Role</span><span class="sxs-lookup"><span data-stu-id="563da-115">Roles</span></span>
-   <span data-ttu-id="563da-116">Jednostki biznesowe</span><span class="sxs-lookup"><span data-stu-id="563da-116">Business units</span></span>
-   <span data-ttu-id="563da-117">Preferencje dotyczące zasobu</span><span class="sxs-lookup"><span data-stu-id="563da-117">Resource preferences</span></span>
-   <span data-ttu-id="563da-118">Rozkłady nakładów</span><span class="sxs-lookup"><span data-stu-id="563da-118">Effort contours</span></span>
-   <span data-ttu-id="563da-119">Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="563da-119">Time zone</span></span>

<span data-ttu-id="563da-120">Asystent planowania używa tych szczegółów do filtrowania zasobów.</span><span class="sxs-lookup"><span data-stu-id="563da-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="563da-121">Uruchom asystenta planowania</span><span class="sxs-lookup"><span data-stu-id="563da-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="563da-122">Istnieją dwa sposoby uruchamiania asystenta planowania.</span><span class="sxs-lookup"><span data-stu-id="563da-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="563da-123">W przypadku korzystania z trybu hybrydowego w siatce członków zespołu można wybrać dowolnego członka zespołu z niezrealizowanym wymaganiem dotyczącym zasobów, a następnie wybrać opcję **Rezerwacja**.</span><span class="sxs-lookup"><span data-stu-id="563da-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="563da-124">W przypadku korzystania z trybu centralnego menedżer zasobów znajduje i wybiera zasób.</span><span class="sxs-lookup"><span data-stu-id="563da-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="563da-125">Filtr asystenta planowania</span><span class="sxs-lookup"><span data-stu-id="563da-125">Schedule assistant filters</span></span>

<span data-ttu-id="563da-126">Po uruchomieniu asystenta planowania szczegóły dotyczące wymagania zasobu są wyświetlane jako filtrowane wartości w lewym okienku.</span><span class="sxs-lookup"><span data-stu-id="563da-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="563da-127">Wyniki może dostosować menedżer zasobów lub menedżer projektu, dopasowując filtry w celu zaspokojenia potrzeb planowania.</span><span class="sxs-lookup"><span data-stu-id="563da-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="563da-128">W okienku filtru są wyświetlane opcje związane z pracą, w tym:</span><span class="sxs-lookup"><span data-stu-id="563da-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="563da-129">Data rozpoczęcia i zakończenia pracy</span><span class="sxs-lookup"><span data-stu-id="563da-129">Work start and end</span></span>
-   <span data-ttu-id="563da-130">Charakterystyki</span><span class="sxs-lookup"><span data-stu-id="563da-130">Characteristics</span></span>
-   <span data-ttu-id="563da-131">Role</span><span class="sxs-lookup"><span data-stu-id="563da-131">Roles</span></span>
-   <span data-ttu-id="563da-132">Jednostki organizacyjne</span><span class="sxs-lookup"><span data-stu-id="563da-132">Organizational units</span></span>
-   <span data-ttu-id="563da-133">Firma zasobów</span><span class="sxs-lookup"><span data-stu-id="563da-133">Resourcing company</span></span>
-   <span data-ttu-id="563da-134">Typy zasobów</span><span class="sxs-lookup"><span data-stu-id="563da-134">Resource types</span></span>
-   <span data-ttu-id="563da-135">Preferowane zasoby</span><span class="sxs-lookup"><span data-stu-id="563da-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]