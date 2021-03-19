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
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279916"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="4ebe2-103">Rezerwacje i przypisania</span><span class="sxs-lookup"><span data-stu-id="4ebe2-103">Bookings vs assignments</span></span>

<span data-ttu-id="4ebe2-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="4ebe2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ebe2-105">Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4ebe2-106">Rezerwacje ostateczne zużywają dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="4ebe2-107">Rezerwacje reprezentują koncepcje organizacyjne dla zespołów, dzięki czemu mogą zrozumieć, w jaki sposób zasoby będą realizowane między różnymi projektami.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="4ebe2-108">Dynamics 365 Project Operations traktuje rezerwacje jako koncepcję na poziomie projektu.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="4ebe2-109">W przeciwieństwie do rezerwacji, przydziały to przydział zasobów do zadań projektu w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4ebe2-110">Zasoby mogą mieć nazwy lub ogólne.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-110">The resources can be named or generic.</span></span>  <span data-ttu-id="4ebe2-111">Gdy zapotrzebowanie na zasoby pochodzi z przydziałów zadań projektu, Project Operations używają konturów nakładu pracy przydziału zasobów do tworzenia konturów szczegółów zapotrzebowania na zasoby.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="4ebe2-112">Jednak czas, który przypisano do zasobów, nie jest zachowywany.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="4ebe2-113">Aktualizacje rezerwacji wynikających z wymagania zasobu nie aktualizują żadnych przypisań zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="4ebe2-114">Zazwyczaj suma księgowań zasobu jest równa sumie przydziałów zasobu w jednym lub wielu zadaniach.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="4ebe2-115">Jednak Project Operations nie wymusza takiej zgodności.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="4ebe2-116">Widok **Uzgadnianie** pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.</span><span class="sxs-lookup"><span data-stu-id="4ebe2-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]