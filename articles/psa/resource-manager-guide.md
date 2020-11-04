---
title: Przewodnik menedżera zasobów
description: Przewodnik zarządzania zasobami w Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 4a26a384dfaf6b974ed35105434152e655ff6444
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082220"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="ef30d-103">Przewodnik menedżera zasobów (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ef30d-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ef30d-104">Funkcje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] w [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pomagają znaleźć odpowiednie zasoby w odpowiednim czasie do odpowiedniego projektu i upewnić się, czy wszystkie zasoby są wykorzystywane efektywnie.</span><span class="sxs-lookup"><span data-stu-id="ef30d-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="ef30d-105">Wdrażaj konsultantów skutecznie dzięki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ef30d-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="ef30d-106">Zapewniają one narzędzia potrzebne do planowania zasobów na podstawie wymagań i harmonogramów projektów doradczych oraz umiejętności i dostępności konsultantów.</span><span class="sxs-lookup"><span data-stu-id="ef30d-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="ef30d-107">Możesz szybko znaleźć najbardziej wykwalifikowanych konsultantów, którzy są dostępni do pracy nad projektami, i możesz łatwo zobaczyć jak lepiej zaplanować ich prace dla każdego projektu.</span><span class="sxs-lookup"><span data-stu-id="ef30d-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="ef30d-108">Planowanie zasobów pomoże Ci:</span><span class="sxs-lookup"><span data-stu-id="ef30d-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="ef30d-109">Dopasować zasoby do projektów, w oparciu o to, jak dobrze umiejętności i poziomy zaawansowania są dopasowane do wymagań zasobów projektu.</span><span class="sxs-lookup"><span data-stu-id="ef30d-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="ef30d-110">Dopasować harmonogram zasobu do kalendarza projektu, w oparciu o dostępność i zaplanowany czas wolny.</span><span class="sxs-lookup"><span data-stu-id="ef30d-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="ef30d-111">Kalendarz kodowany kolorami zapewnia wizualne wskazówki informujące o dostępności zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef30d-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="ef30d-112">Przejrzyj zdolności produkcyjne każdego konsultant i określ, w jakim stopniu te zdolności są aktualnie używane.</span><span class="sxs-lookup"><span data-stu-id="ef30d-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="ef30d-113">Może Ci to się dowiedzieć, gdzie Konsultant jest zbyt mało lub nadmiernie wykorzystywany, lub czy pracujemy zgodnie ze zdolnościami produkcyjnymi.</span><span class="sxs-lookup"><span data-stu-id="ef30d-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="ef30d-114">Przypisz wartość procentową lub określoną liczbę godzin dla zdolności produkcyjnych pracownika do projektu.</span><span class="sxs-lookup"><span data-stu-id="ef30d-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="ef30d-115">Dokonaj grupowych rezerwacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef30d-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="ef30d-116">Przeprowadź wstępną bądź ostateczną rezerwację zasobów, i w jednym kroku konwertuj zarezerwowane wstępnie godziny na godziny zarezerwowane ostatecznie.</span><span class="sxs-lookup"><span data-stu-id="ef30d-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="ef30d-117">Automatycznie twórz zespół projektu bazujący na zasobach określonych w strukturze podziału pracy dla projektu.</span><span class="sxs-lookup"><span data-stu-id="ef30d-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="ef30d-118">Spełniaj żądania zasobów (rezerwuj, proponuj, znajduj zasoby zastępcze).</span><span class="sxs-lookup"><span data-stu-id="ef30d-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="ef30d-119">Przypisuj zasoby zgodnie z modelem centralnym (przypisania dokonuje menedżer zasobów) lub hybrydowym (przypisania może dokonać menedżer zasobów oraz inni menedżerowie).</span><span class="sxs-lookup"><span data-stu-id="ef30d-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="ef30d-120">Aby uzyskać więcej informacji na temat ustawiania centralnego i hybrydowego modelu zarządzania zasobami, zobacz [Skonfiguruj ustawienia dodatkowych parametrów (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ef30d-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="ef30d-121">Możesz efektywnie zarządzać zasobami w projektach i upewnić się, że projekty są odpowiednio obsadzone.</span><span class="sxs-lookup"><span data-stu-id="ef30d-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="ef30d-122">Będziesz musiał przeprowadzić następujące zadania:</span><span class="sxs-lookup"><span data-stu-id="ef30d-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="ef30d-123">[Zarządzaj żądaniami zasobów](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="ef30d-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="ef30d-124">Dopasuj umiejętności i biegłości konsultantów do odpowiednich projektów.</span><span class="sxs-lookup"><span data-stu-id="ef30d-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="ef30d-125">[Wyświetl dostępność zasobów](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="ef30d-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="ef30d-126">Sprawdź dostępność konsultantów w widoku kalendarza.</span><span class="sxs-lookup"><span data-stu-id="ef30d-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="ef30d-127">[Wyświetl wykorzystanie zasobów](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="ef30d-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="ef30d-128">Zobacz wartość procentową czasu, w którym konsultanci są aktualnie zarezerwowani.</span><span class="sxs-lookup"><span data-stu-id="ef30d-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="ef30d-129">[Zaplanuj zasoby dla projektu](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="ef30d-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="ef30d-130">Zaplanuj konsultantów dla projektu.</span><span class="sxs-lookup"><span data-stu-id="ef30d-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="ef30d-131">Aby uzyskać więcej informacji na temat przesyłania żądania zasobu dla poszczególnych projektów, zobacz [Prześlij żądania zasobów](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="ef30d-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ef30d-132">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="ef30d-132">See Also</span></span>  
 <span data-ttu-id="ef30d-133">[Przewodnik po rozwiązaniu Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="ef30d-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="ef30d-134">[Przewodnik administratora](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="ef30d-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="ef30d-135">[Przewodnik menedżera kont](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="ef30d-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="ef30d-136">[Przewodnik menedżera projektów](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="ef30d-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="ef30d-137">Przewodnik dotyczący czasu, wydatków i współpracy</span><span class="sxs-lookup"><span data-stu-id="ef30d-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
