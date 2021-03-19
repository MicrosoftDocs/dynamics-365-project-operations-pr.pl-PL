---
title: Omówienie trybów zarządzania zasobami
description: Ta temat zawiera informacje o funkcji Zarządzania zasobami w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279466"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="10733-103">Omówienie trybów zarządzania zasobami</span><span class="sxs-lookup"><span data-stu-id="10733-103">Resource management modes overview</span></span>

<span data-ttu-id="10733-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="10733-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="10733-105">Rozwiązaniu Dynamics 365 Project Operations obsługuje dwa tryby, aby umożliwić wykonywanie całego przepływu księgowania.</span><span class="sxs-lookup"><span data-stu-id="10733-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="10733-106">Tryb zarządzania jest definiowany jako parametr projektu i może zostać zmodyfikowany, jeśli wystąpi taka konieczność.</span><span class="sxs-lookup"><span data-stu-id="10733-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="10733-107">Tryb centralny</span><span class="sxs-lookup"><span data-stu-id="10733-107">Central mode</span></span>
<span data-ttu-id="10733-108">W przypadku organizacji, w których scentralizowano alokację zasobów do projektów, tryb centralny umożliwia zapewnienie menedżerom projektów możliwości definiowania wymagań dotyczących zasobów na poziomie projektu.</span><span class="sxs-lookup"><span data-stu-id="10733-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="10733-109">Realizacja zapotrzebowania na zasoby jest przekazywana do menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="10733-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="10733-110">Menedżerowie projektów mogą akceptować lub odrzucać zasoby, które zaproponował menedżer zasobów.</span><span class="sxs-lookup"><span data-stu-id="10733-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Tryb centralny](./media/resource-management-central.png)

<span data-ttu-id="10733-112">Aby zarządzać zasobami w trybie Centralnym, zobacz:</span><span class="sxs-lookup"><span data-stu-id="10733-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="10733-113">Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="10733-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="10733-114">Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="10733-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="10733-115">Przesyłanie żądania zasobów</span><span class="sxs-lookup"><span data-stu-id="10733-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="10733-116">Realizowanie żądania zasobów</span><span class="sxs-lookup"><span data-stu-id="10733-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="10733-117">Akceptowanie lub odrzucanie proponowanego zasobu projektu z poziomu żądania zasobu</span><span class="sxs-lookup"><span data-stu-id="10733-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="10733-118">Tryb hybrydowy</span><span class="sxs-lookup"><span data-stu-id="10733-118">Hybrid mode</span></span>
<span data-ttu-id="10733-119">W organizacjach, które potrzebują elastyczności w zakresie alokacji zasobów, tryb hybrydowy umożliwia menedżerom projektów i menedżerom zasobów możliwość tworzenia rezerwacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="10733-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Tryb hybrydowy](./media/resource-management-hybrid.png)

<span data-ttu-id="10733-121">Poza obsługiwanym procesem w trybie centralnym można także skorzystać z następujących tematów, aby zarządzać wszystkimi innymi obsługiwanymi przepływami rezerwacji w trybie hybrydowym:</span><span class="sxs-lookup"><span data-stu-id="10733-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="10733-122">Rezerwacja zasobu bezpośrednio do projektu:</span><span class="sxs-lookup"><span data-stu-id="10733-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="10733-123">Rezerwowanie nazwanych zasobów możliwych do zarezerwowania dla zespołu projektu i przypisywanie zadań</span><span class="sxs-lookup"><span data-stu-id="10733-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="10733-124">Rezerwowanie zasobów z poziomu wymagań zasobów:</span><span class="sxs-lookup"><span data-stu-id="10733-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="10733-125">Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="10733-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="10733-126">Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="10733-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]