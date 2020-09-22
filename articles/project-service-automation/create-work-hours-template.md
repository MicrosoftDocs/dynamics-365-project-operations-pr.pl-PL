---
title: Utwórz szablon godzin pracy
description: Tworzenie szablonu godzin pracy w Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754353"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="88daa-103">Twórz szablon godzin pracy (Project Service)</span><span class="sxs-lookup"><span data-stu-id="88daa-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="88daa-104">Zanim będziesz mógł utworzyć harmonogramy projektów musisz skonfigurować kalendarz projektu, który definiuje liczbę godzin pracy w ciągu dnia w harmonogramie i wszystkie dni wolne od pracy.</span><span class="sxs-lookup"><span data-stu-id="88daa-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="88daa-105">Można to zrobić za pomocą szablonu godzin pracy, który zawiera szczegółowe informacje dotyczące godzin pracy w ciągu dnia, dni wolnych, a także wszelkich innych dni wolnych od pracy.</span><span class="sxs-lookup"><span data-stu-id="88daa-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="88daa-106">Podczas tworzenia projektu, kojarzysz szablon pracy z kalendarzem projektu, aby zastosować harmonogram dla projektu.</span><span class="sxs-lookup"><span data-stu-id="88daa-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="88daa-107">Istnieją dwa sposoby na utworzenie szablonu godzin pracy:</span><span class="sxs-lookup"><span data-stu-id="88daa-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="88daa-108">Utwórz szablon godzin pracy na podstawie kalendarza zasobu.</span><span class="sxs-lookup"><span data-stu-id="88daa-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="88daa-109">Utwórz nowy szablon godzin pracy.</span><span class="sxs-lookup"><span data-stu-id="88daa-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="88daa-110">Aby utworzyć szablon godzin pracy na podstawie kalendarza zasobu</span><span class="sxs-lookup"><span data-stu-id="88daa-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="88daa-111">Przejdź do **Project Service > Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="88daa-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="88daa-112">Wybierz zasób, dla którego chcesz wyznaczyć godziny pracy.</span><span class="sxs-lookup"><span data-stu-id="88daa-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="88daa-113">Kliknij **Zapisz kalendarz jako**, wprowadź nazwę szablonu godzin pracy, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="88daa-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="88daa-114">Po zakończeniu edycji opcji kliknij **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="88daa-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="88daa-115">Kliknij przycisk **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="88daa-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="88daa-116">Aby utworzyć nowy szablon godzin pracy</span><span class="sxs-lookup"><span data-stu-id="88daa-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="88daa-117">Przejdź do **Project Service > Szablony godzin pracy**.</span><span class="sxs-lookup"><span data-stu-id="88daa-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="88daa-118">Kliknij pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="88daa-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="88daa-119">Wprowadź nazwę dla szablonu godzin pracy.</span><span class="sxs-lookup"><span data-stu-id="88daa-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="88daa-120">Wybierz zasób, dla którego chcesz wyznaczyć godziny pracy, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="88daa-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="88daa-121">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="88daa-121">See Also</span></span>  
 [<span data-ttu-id="88daa-122">Konfigurowanie zasobów</span><span class="sxs-lookup"><span data-stu-id="88daa-122">Set up resources</span></span>](../project-service/set-up-resources.md)
