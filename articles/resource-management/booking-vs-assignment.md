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
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896024"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="6db79-103">Rezerwacje i przypisania</span><span class="sxs-lookup"><span data-stu-id="6db79-103">Bookings vs assignments</span></span>

<span data-ttu-id="6db79-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="6db79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6db79-105">Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu.</span><span class="sxs-lookup"><span data-stu-id="6db79-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="6db79-106">Rezerwacje ostateczne zużywają dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="6db79-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="6db79-107">Przypisania to przydziały zasobów do zadań projektu w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="6db79-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="6db79-108">Zasoby mogą być rzeczywiste lub ogólne.</span><span class="sxs-lookup"><span data-stu-id="6db79-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="6db79-109">W przypadku zasobów rzeczywistych najlepiej, aby rezerwacje i przypisania były zgodne, ponieważ technicznie nie różnią się od siebie.</span><span class="sxs-lookup"><span data-stu-id="6db79-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="6db79-110">Jednak program Microsoft Dynamics Project Operations nie wymusza takiej zgodności.</span><span class="sxs-lookup"><span data-stu-id="6db79-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="6db79-111">Widok **Uzgadnianie** pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.</span><span class="sxs-lookup"><span data-stu-id="6db79-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
