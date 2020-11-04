---
title: Zarządzanie zasobami — często zadawane pytania
description: Ta temat zawiera odpowiedzi na często zadawane pytania dotyczące zarządzania zasobami.
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082223"
---
# <a name="resource-management-faq"></a><span data-ttu-id="d8831-103">Zarządzanie zasobami — często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="d8831-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="d8831-104">Jaka jest różnica między członkiem zespołu a wymaganiem zasobu?</span><span class="sxs-lookup"><span data-stu-id="d8831-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="d8831-105">Członka zespołu projektu można przypisywać do zadań, rezerwować lub rezerwować nadmiarowo oraz ustawiać jako osobę zatwierdzającą.</span><span class="sxs-lookup"><span data-stu-id="d8831-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="d8831-106">Wymaganie zasobu może istnieć bez członka zespołu projektu, jako wersja robocza uwagi o wymaganiu.</span><span class="sxs-lookup"><span data-stu-id="d8831-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="d8831-107">Jaka jest różnica między godzinami proponowanymi a godzinami zarezerwowanymi wstępnie?</span><span class="sxs-lookup"><span data-stu-id="d8831-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="d8831-108">Godziny proponowane i godziny zarezerwowane wstępnie różnią się widocznością.</span><span class="sxs-lookup"><span data-stu-id="d8831-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="d8831-109">Godziny proponowane są widoczne tylko dla menedżerów zasobów i menedżera projektu, który zainicjował wymaganie za pomocą żądania zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8831-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="d8831-110">Godziny zarezerwowane wstępnie są widoczne dla każdego, kto ma dostęp do tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d8831-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="d8831-111">Jak wyświetlić wstępnie zarezerwowane godziny dla zasobów w zespole?</span><span class="sxs-lookup"><span data-stu-id="d8831-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="d8831-112">Wstępnej rezerwacji można dokonać podczas rezerwowania wymagania zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8831-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="d8831-113">Zasoby, które wstępnie zarezerwowano w zespole projektu, są wyświetlane jako członkowie zespołu mający wstępnie zarezerwowane godziny.</span><span class="sxs-lookup"><span data-stu-id="d8831-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="d8831-114">Są one również widoczne na tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d8831-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="d8831-115">Jak zmienić wymagane godziny oraz daty rozpoczęcia i zakończenia dla zasobu (ogólnego lub nazwanego) zarezerwowanego przeze mnie?</span><span class="sxs-lookup"><span data-stu-id="d8831-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="d8831-116">Po zarezerwowaniu zasobów wybierz opcję **Obsługa rezerwacji** , aby wprowadzić wszelkie wymagane zmiany.</span><span class="sxs-lookup"><span data-stu-id="d8831-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="d8831-117">Jakie typy zasobów obsługuje program Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="d8831-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="d8831-118">**Użytkownik** i **Kontakt** są jedynymi typami zasobów obsługiwanymi w programie Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d8831-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="d8831-119">Mimo iż można tworzyć inne typy zasobów (np. **Sprzęt** i **Grupa** ), nie są dla nich obsługiwane żadne kompleksowe przypadki użycia.</span><span class="sxs-lookup"><span data-stu-id="d8831-119">Although you can create other types of resources (for example, **Equipment** and **Group** ), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="d8831-120">Jaka jest różnica między przypisaniem a rezerwacją?</span><span class="sxs-lookup"><span data-stu-id="d8831-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="d8831-121">Przypisania to przydziały zasobów do zadań projektu w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="d8831-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="d8831-122">Zasoby mogą być rzeczywiste lub ogólne.</span><span class="sxs-lookup"><span data-stu-id="d8831-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="d8831-123">Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu.</span><span class="sxs-lookup"><span data-stu-id="d8831-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="d8831-124">Rezerwacje ostateczne zużywają dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8831-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="d8831-125">W przypadku zasobów rzeczywistych najlepiej, aby rezerwacje i przypisania były zgodne, ponieważ technicznie nie różnią się od siebie.</span><span class="sxs-lookup"><span data-stu-id="d8831-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="d8831-126">Jednak program PSA nie wymusza takiej zgodności.</span><span class="sxs-lookup"><span data-stu-id="d8831-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="d8831-127">Widok Uzgadnianie pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.</span><span class="sxs-lookup"><span data-stu-id="d8831-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
