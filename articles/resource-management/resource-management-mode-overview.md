---
title: Omówienie trybów zarządzania zasobami
description: W tym temacie zamieszczono informacje o funkcjach Zarządzania zasobami w Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081900"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="32d07-103">Omówienie trybów zarządzania zasobami</span><span class="sxs-lookup"><span data-stu-id="32d07-103">Resource management modes overview</span></span>

<span data-ttu-id="32d07-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="32d07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="32d07-105">Dynamics 365 Project Operations obsługuje dwa tryby w celu wykonania całościowego przepływu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="32d07-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="32d07-106">Tryb zarządzania jest definiowany jako parametr projektu i może zostać zmodyfikowany, jeśli wystąpi taka konieczność.</span><span class="sxs-lookup"><span data-stu-id="32d07-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="32d07-107">Tryb centralny</span><span class="sxs-lookup"><span data-stu-id="32d07-107">Central mode</span></span>
<span data-ttu-id="32d07-108">W przypadku organizacji, w których scentralizowano alokację zasobów do projektów, tryb centralny umożliwia zapewnienie menedżerom projektów możliwości definiowania wymagań dotyczących zasobów na poziomie projektu.</span><span class="sxs-lookup"><span data-stu-id="32d07-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="32d07-109">Realizacja zapotrzebowania na zasoby jest przekazywana do menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="32d07-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="32d07-110">Menedżerowie projektów mogą akceptować lub odrzucać zasoby, które zaproponował menedżer zasobów.</span><span class="sxs-lookup"><span data-stu-id="32d07-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Tryb centralny](./media/resource-management-central.png)

<span data-ttu-id="32d07-112">Aby zarządzać zasobami w trybie Centralnym, zobacz:</span><span class="sxs-lookup"><span data-stu-id="32d07-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="32d07-113">Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="32d07-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="32d07-114">Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="32d07-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="32d07-115">Przesyłanie żądania zasobów</span><span class="sxs-lookup"><span data-stu-id="32d07-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="32d07-116">Realizowanie żądania zasobów</span><span class="sxs-lookup"><span data-stu-id="32d07-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="32d07-117">Akceptowanie lub odrzucanie proponowanego zasobu projektu z poziomu żądania zasobu</span><span class="sxs-lookup"><span data-stu-id="32d07-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="32d07-118">Tryb hybrydowy</span><span class="sxs-lookup"><span data-stu-id="32d07-118">Hybrid mode</span></span>
<span data-ttu-id="32d07-119">W organizacjach, które potrzebują elastyczności w zakresie alokacji zasobów, tryb hybrydowy umożliwia menedżerom projektów i menedżerom zasobów możliwość tworzenia rezerwacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="32d07-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Tryb hybrydowy](./media/resource-management-hybrid.png)

<span data-ttu-id="32d07-121">Poza obsługiwanym procesem w trybie centralnym można także skorzystać z następujących tematów, aby zarządzać wszystkimi innymi obsługiwanymi przepływami rezerwacji w trybie hybrydowym:</span><span class="sxs-lookup"><span data-stu-id="32d07-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="32d07-122">Rezerwacja zasobu bezpośrednio do projektu:</span><span class="sxs-lookup"><span data-stu-id="32d07-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="32d07-123">Rezerwowanie nazwanych zasobów możliwych do zarezerwowania dla zespołu projektu i przypisywanie zadań</span><span class="sxs-lookup"><span data-stu-id="32d07-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="32d07-124">Rezerwowanie zasobów z poziomu wymagań zasobów:</span><span class="sxs-lookup"><span data-stu-id="32d07-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="32d07-125">Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="32d07-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="32d07-126">Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="32d07-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
