---
title: Rezerwacje i przypisania
description: Ten temat zawiera informacje o różnicach między księgami zasobów a przydziałami zasobów.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130231"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="5d227-103">Rezerwacje i przypisania</span><span class="sxs-lookup"><span data-stu-id="5d227-103">Bookings vs assignments</span></span>

<span data-ttu-id="5d227-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="5d227-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d227-105">Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu.</span><span class="sxs-lookup"><span data-stu-id="5d227-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="5d227-106">Rezerwacje ostateczne zużywają dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d227-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="5d227-107">Rezerwacje reprezentują koncepcje organizacyjne dla zespołów, dzięki czemu mogą zrozumieć, w jaki sposób zasoby będą realizowane między różnymi projektami.</span><span class="sxs-lookup"><span data-stu-id="5d227-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="5d227-108">Dynamics 365 Project Operations traktuje rezerwacje jako koncepcję na poziomie projektu.</span><span class="sxs-lookup"><span data-stu-id="5d227-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="5d227-109">W przeciwieństwie do rezerwacji, przydziały to przydział zasobów do zadań projektu w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="5d227-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="5d227-110">Zasoby mogą mieć nazwy lub ogólne.</span><span class="sxs-lookup"><span data-stu-id="5d227-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="5d227-111">Zazwyczaj suma księgowań zasobu jest równa sumie przydziałów zasobu w jednym lub wielu zadaniach.</span><span class="sxs-lookup"><span data-stu-id="5d227-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="5d227-112">Jednak Project Operations nie wymusza takiej zgodności.</span><span class="sxs-lookup"><span data-stu-id="5d227-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="5d227-113">Widok **Uzgadnianie** pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.</span><span class="sxs-lookup"><span data-stu-id="5d227-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
