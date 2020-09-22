---
title: Śledź stan projektu
description: Śledzenie stanu projektu w Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754397"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="cf599-103">Śledź stan projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="cf599-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="cf599-104">Użyj [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], aby śledzić postęp projektu klienta.</span><span class="sxs-lookup"><span data-stu-id="cf599-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="cf599-105">Wraz z postępem zaangażowania etapy projektu są aktualizowane, aby odzwierciedlić etap zaangażowania:</span><span class="sxs-lookup"><span data-stu-id="cf599-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="cf599-106">**Nowy**</span><span class="sxs-lookup"><span data-stu-id="cf599-106">**New**</span></span>    | <span data-ttu-id="cf599-107">Podczas tworzenia projektu etap jest określany jako **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="cf599-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="cf599-108">Jeżeli projekt został utworzony z szablonu, na tym etapie projekt może posiadać harmonogram, szacunki i dane zespołu.</span><span class="sxs-lookup"><span data-stu-id="cf599-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="cf599-109">W przeciwnym razie będzie to konspekt projektu i będziesz musiał ręcznie wprowadzić pozostałe elementy projektu.</span><span class="sxs-lookup"><span data-stu-id="cf599-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="cf599-110">**Oferta**</span><span class="sxs-lookup"><span data-stu-id="cf599-110">**Quote**</span></span>   |      <span data-ttu-id="cf599-111">Podczas kojarzenia projektu z ofertą lub tworzenia go z oferty, etap projektu jest określany jako **Oferta**, a szacunkowe daty rozpoczęcia i zakończenia są również aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="cf599-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="cf599-112">Gdy projekt jest w fazie oferty, szczegóły dotyczące ofert są wyświetlane na karcie **Sprzedaż** na stronie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="cf599-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="cf599-113">**Planowanie**</span><span class="sxs-lookup"><span data-stu-id="cf599-113">**Plan**</span></span>   |                                     <span data-ttu-id="cf599-114">Gdy wygrywasz ofertę związaną z projektem, i kiedy zaangażowanie przechodzi na etap umowy, etap projektu zostaje aktualizowany do **Plan**.</span><span class="sxs-lookup"><span data-stu-id="cf599-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="cf599-115">Szczegóły dotyczące umowy są wyświetlane na karcie **Sprzedaż** na stronie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="cf599-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="cf599-116">**Zakończony**</span><span class="sxs-lookup"><span data-stu-id="cf599-116">**Complete**</span></span> |                    <span data-ttu-id="cf599-117">Po zakończeniu pracy nad projektem można przełączyć etap na **Zakończ**.</span><span class="sxs-lookup"><span data-stu-id="cf599-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="cf599-118">Gdy etapu projektu jest określany jako zakończony, rozumiemy, że praca została wykonana w 100%, ale projekt pozostaje otwarty przez czas oczekiwania lub do czasu zarejestrowania wpisów dotyczących wydatków.</span><span class="sxs-lookup"><span data-stu-id="cf599-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="cf599-119">**Zamknij**</span><span class="sxs-lookup"><span data-stu-id="cf599-119">**Close**</span></span>   |           <span data-ttu-id="cf599-120">Gdy wszystkie transakcje zostały zarejestrowane w projekcie i nie spodziewasz rejestrowania żadnych innych, możesz ręcznie ustawić etap na **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="cf599-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="cf599-121">Gdy projekt jest na etapie **Zamknij**, nie możesz zarejestrować żadnych więcej transakcji w ramach tego projektu i projektu jest w trybie tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="cf599-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="cf599-122">Aby śledzić stan projektu</span><span class="sxs-lookup"><span data-stu-id="cf599-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="cf599-123">Przejdź do **Project Service > Projekty**.</span><span class="sxs-lookup"><span data-stu-id="cf599-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="cf599-124">Kliknij projekt, nad którym chcesz pracować.</span><span class="sxs-lookup"><span data-stu-id="cf599-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="cf599-125">Na pasku u góry ekranu, wybierz strzałkę w dół obok nazwy projektu, a następnie kliknij **Śledzenie projektu**.</span><span class="sxs-lookup"><span data-stu-id="cf599-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="cf599-126">Wybierz **Śledzenie nakładu pracy** lub **Śledzenie kosztów** na liście rozwijanej powyżej listy zadań.</span><span class="sxs-lookup"><span data-stu-id="cf599-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="cf599-127">Kliknij dwukrotnie dowolne zadanie, aby je edytować.</span><span class="sxs-lookup"><span data-stu-id="cf599-127">Double-click any task to edit it.</span></span> <span data-ttu-id="cf599-128">Możesz również przenieść lub zmienić rozmiar pasków na wykresie Gantta, aby zmienić godzinę i postęp zadania.</span><span class="sxs-lookup"><span data-stu-id="cf599-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="cf599-129">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="cf599-129">See Also</span></span>  
 [<span data-ttu-id="cf599-130">Przewodnik menedżera projektu</span><span class="sxs-lookup"><span data-stu-id="cf599-130">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
