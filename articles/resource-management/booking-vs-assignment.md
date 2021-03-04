---
title: Rezerwacje i przypisania
description: Ten temat zawiera informacje o różnicach między księgami zasobów a przydziałami zasobów.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841185"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="4560e-103">Rezerwacje i przypisania</span><span class="sxs-lookup"><span data-stu-id="4560e-103">Bookings vs assignments</span></span>

<span data-ttu-id="4560e-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="4560e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4560e-105">Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu.</span><span class="sxs-lookup"><span data-stu-id="4560e-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4560e-106">Rezerwacje ostateczne zużywają dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="4560e-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="4560e-107">Rezerwacje reprezentują koncepcje organizacyjne dla zespołów, dzięki czemu mogą zrozumieć, w jaki sposób zasoby będą realizowane między różnymi projektami.</span><span class="sxs-lookup"><span data-stu-id="4560e-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="4560e-108">Dynamics 365 Project Operations traktuje rezerwacje jako koncepcję na poziomie projektu.</span><span class="sxs-lookup"><span data-stu-id="4560e-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="4560e-109">W przeciwieństwie do rezerwacji, przydziały to przydział zasobów do zadań projektu w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="4560e-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4560e-110">Zasoby mogą mieć nazwy lub ogólne.</span><span class="sxs-lookup"><span data-stu-id="4560e-110">The resources can be named or generic.</span></span>  <span data-ttu-id="4560e-111">Gdy zapotrzebowanie na zasoby pochodzi z przydziałów zadań projektu, Project Operations używają konturów nakładu pracy przydziału zasobów do tworzenia konturów szczegółów zapotrzebowania na zasoby.</span><span class="sxs-lookup"><span data-stu-id="4560e-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="4560e-112">Jednak czas, który przypisano do zasobów, nie jest zachowywany.</span><span class="sxs-lookup"><span data-stu-id="4560e-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="4560e-113">Aktualizacje rezerwacji wynikających z wymagania zasobu nie aktualizują żadnych przypisań zasobów.</span><span class="sxs-lookup"><span data-stu-id="4560e-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="4560e-114">Zazwyczaj suma księgowań zasobu jest równa sumie przydziałów zasobu w jednym lub wielu zadaniach.</span><span class="sxs-lookup"><span data-stu-id="4560e-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="4560e-115">Jednak Project Operations nie wymusza takiej zgodności.</span><span class="sxs-lookup"><span data-stu-id="4560e-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="4560e-116">Widok **Uzgadnianie** pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.</span><span class="sxs-lookup"><span data-stu-id="4560e-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


