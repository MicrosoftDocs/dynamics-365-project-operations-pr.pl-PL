---
title: Rezerwacje i przypisania
description: Ten temat zawiera informacje o różnicach między księgami zasobów a przydziałami zasobów.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081861"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="182cd-103">Rezerwacje i przypisania</span><span class="sxs-lookup"><span data-stu-id="182cd-103">Bookings vs assignments</span></span>

<span data-ttu-id="182cd-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="182cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="182cd-105">Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu.</span><span class="sxs-lookup"><span data-stu-id="182cd-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="182cd-106">Rezerwacje ostateczne zużywają dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="182cd-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="182cd-107">Przypisania to przydziały zasobów do zadań projektu w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="182cd-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="182cd-108">Zasoby mogą być rzeczywiste lub ogólne.</span><span class="sxs-lookup"><span data-stu-id="182cd-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="182cd-109">W przypadku zasobów rzeczywistych najlepiej, aby rezerwacje i przypisania były zgodne, ponieważ technicznie nie różnią się od siebie.</span><span class="sxs-lookup"><span data-stu-id="182cd-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="182cd-110">Jednak program Microsoft Dynamics Project Operations nie wymusza takiej zgodności.</span><span class="sxs-lookup"><span data-stu-id="182cd-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="182cd-111">Widok **Uzgadnianie** pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.</span><span class="sxs-lookup"><span data-stu-id="182cd-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
