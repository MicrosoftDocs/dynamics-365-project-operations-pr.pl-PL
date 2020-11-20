---
title: Śledź stan projektu
description: Śledzenie stanu projektu w Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 00b6d874b42a415fe567d17e49c0ea319d8952a0
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127846"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="089bc-103">Śledź stan projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="089bc-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="089bc-104">Użyj [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], aby śledzić postęp projektu klienta.</span><span class="sxs-lookup"><span data-stu-id="089bc-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="089bc-105">Wraz z postępem zaangażowania etapy projektu są aktualizowane, aby odzwierciedlić etap zaangażowania:</span><span class="sxs-lookup"><span data-stu-id="089bc-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="089bc-106">**Nowy**</span><span class="sxs-lookup"><span data-stu-id="089bc-106">**New**</span></span>    | <span data-ttu-id="089bc-107">Podczas tworzenia projektu etap jest określany jako **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="089bc-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="089bc-108">Jeżeli projekt został utworzony z szablonu, na tym etapie projekt może posiadać harmonogram, szacunki i dane zespołu.</span><span class="sxs-lookup"><span data-stu-id="089bc-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="089bc-109">W przeciwnym razie będzie to konspekt projektu i będziesz musiał ręcznie wprowadzić pozostałe elementy projektu.</span><span class="sxs-lookup"><span data-stu-id="089bc-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="089bc-110">**Oferta**</span><span class="sxs-lookup"><span data-stu-id="089bc-110">**Quote**</span></span>   |      <span data-ttu-id="089bc-111">Podczas kojarzenia projektu z ofertą lub tworzenia go z oferty, etap projektu jest określany jako **Oferta**, a szacunkowe daty rozpoczęcia i zakończenia są również aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="089bc-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="089bc-112">Gdy projekt jest w fazie oferty, szczegóły dotyczące ofert są wyświetlane na karcie **Sprzedaż** na stronie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="089bc-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="089bc-113">**Planowanie**</span><span class="sxs-lookup"><span data-stu-id="089bc-113">**Plan**</span></span>   |                                     <span data-ttu-id="089bc-114">Gdy wygrywasz ofertę związaną z projektem, i kiedy zaangażowanie przechodzi na etap umowy, etap projektu zostaje aktualizowany do **Plan**.</span><span class="sxs-lookup"><span data-stu-id="089bc-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="089bc-115">Szczegóły dotyczące umowy są wyświetlane na karcie **Sprzedaż** na stronie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="089bc-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="089bc-116">**Zakończony**</span><span class="sxs-lookup"><span data-stu-id="089bc-116">**Complete**</span></span> |                    <span data-ttu-id="089bc-117">Po zakończeniu pracy nad projektem można przełączyć etap na **Zakończ**.</span><span class="sxs-lookup"><span data-stu-id="089bc-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="089bc-118">Gdy etapu projektu jest określany jako zakończony, rozumiemy, że praca została wykonana w 100%, ale projekt pozostaje otwarty przez czas oczekiwania lub do czasu zarejestrowania wpisów dotyczących wydatków.</span><span class="sxs-lookup"><span data-stu-id="089bc-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="089bc-119">**Zamknij**</span><span class="sxs-lookup"><span data-stu-id="089bc-119">**Close**</span></span>   |           <span data-ttu-id="089bc-120">Gdy wszystkie transakcje zostały zarejestrowane w projekcie i nie spodziewasz rejestrowania żadnych innych, możesz ręcznie ustawić etap na **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="089bc-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="089bc-121">Gdy projekt jest na etapie **Zamknij**, nie możesz zarejestrować żadnych więcej transakcji w ramach tego projektu i projektu jest w trybie tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="089bc-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="089bc-122">Aby śledzić stan projektu</span><span class="sxs-lookup"><span data-stu-id="089bc-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="089bc-123">Przejdź do **Project Service > Projekty**.</span><span class="sxs-lookup"><span data-stu-id="089bc-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="089bc-124">Kliknij projekt, nad którym chcesz pracować.</span><span class="sxs-lookup"><span data-stu-id="089bc-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="089bc-125">Na pasku u góry ekranu, wybierz strzałkę w dół obok nazwy projektu, a następnie kliknij **Śledzenie projektu**.</span><span class="sxs-lookup"><span data-stu-id="089bc-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="089bc-126">Wybierz **Śledzenie nakładu pracy** lub **Śledzenie kosztów** na liście rozwijanej powyżej listy zadań.</span><span class="sxs-lookup"><span data-stu-id="089bc-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="089bc-127">Kliknij dwukrotnie dowolne zadanie, aby je edytować.</span><span class="sxs-lookup"><span data-stu-id="089bc-127">Double-click any task to edit it.</span></span> <span data-ttu-id="089bc-128">Możesz również przenieść lub zmienić rozmiar pasków na wykresie Gantta, aby zmienić godzinę i postęp zadania.</span><span class="sxs-lookup"><span data-stu-id="089bc-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="089bc-129">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="089bc-129">See Also</span></span>  
 [<span data-ttu-id="089bc-130">Przewodnik menedżera projektu</span><span class="sxs-lookup"><span data-stu-id="089bc-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)