---
title: Zaplanuj zasoby dla projektu
description: Planowanie zasobów dla projektu w Project Service
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082218"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="10e06-103">Planuj zasoby dla projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="10e06-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="10e06-104">Możesz sprawdzić dostępność zasobów, aby uzyskać ogólny pogląd stopnia zarezerwowania zasobów, lub możesz filtrować widok według umiejętności, zespołu, lokalizacji i innych opcji.</span><span class="sxs-lookup"><span data-stu-id="10e06-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="10e06-105">Tablica harmonogramu zawiera listę zasobów i ich dostępności.</span><span class="sxs-lookup"><span data-stu-id="10e06-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="10e06-106">Wybierz tryb wyświetlania dostępności dla **Godziny** , **Dzień** , **Tydzień** , lub **Miesiąc**.</span><span class="sxs-lookup"><span data-stu-id="10e06-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="10e06-107">Przed skorzystaniem z tablicy harmonogramu, należy ją skonfigurować.</span><span class="sxs-lookup"><span data-stu-id="10e06-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="10e06-108">Aby uzyskać więcej informacji, zobacz [Konfiguruj tablicę harmonogramu (Field Service lub Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="10e06-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="10e06-109">Jeśli używasz starszej wersji, dla dostępności zasobów sprawdź [Przeglądanie dostępności zasobów](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="10e06-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="10e06-110">Aby użyć funkcji rezerwacji tablicy harmonogramu, geokodowania i usług lokalizacji, należy włączyć mapy.</span><span class="sxs-lookup"><span data-stu-id="10e06-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="10e06-111">W menu głównym zaznacz **Planowanie zasobów** > **Administracja**.</span><span class="sxs-lookup"><span data-stu-id="10e06-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="10e06-112">Kliknij **Parametry planowania**.</span><span class="sxs-lookup"><span data-stu-id="10e06-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="10e06-113">Otwórz rekord i przewiń w dół do sekcji **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="10e06-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="10e06-114">W polu **Połącz z Mapy** , wybierz **Tak**.</span><span class="sxs-lookup"><span data-stu-id="10e06-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="10e06-115">Zaakceptuj warunki i zapisz rekord.</span><span class="sxs-lookup"><span data-stu-id="10e06-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="10e06-116">W menu głównym wybierz **Project Service** > **Tablica harmonogramu**.</span><span class="sxs-lookup"><span data-stu-id="10e06-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="10e06-117">Istnieje kilka sposobów ręcznego planowania wymogu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="10e06-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="10e06-118">Wybierz metodę, którą preferujesz.</span><span class="sxs-lookup"><span data-stu-id="10e06-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="10e06-119">Znajdź dostępne zasoby</span><span class="sxs-lookup"><span data-stu-id="10e06-119">Find available resources</span></span>

1.  <span data-ttu-id="10e06-120">Na liście **Wymóg rezerwacji** , kliknij prawym przyciskiem myszy na niezaplanowanej rezerwacji i wybierz jedną z następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="10e06-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="10e06-121">Wybierz **Znajdź dostępność - Bieżące zasoby** , aby znaleźć dostępny zasób na liście na tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="10e06-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="10e06-122">Wybierz **Znajdź dostępność - Wszystkie zasoby** , aby znaleźć zasób dostępny pośród zasobów w systemie</span><span class="sxs-lookup"><span data-stu-id="10e06-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="10e06-123">Gdy to zrobisz, filtry ukażą opcje wybranego wymogu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="10e06-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="10e06-124">Po pojawieniu się dostępnego przedziału czasu kliknij na nim prawym przyciskiem myszy na tablicy harmonogramu i wybierz **Zarezerwuj tutaj**.</span><span class="sxs-lookup"><span data-stu-id="10e06-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="10e06-125">Lub przeciągnij i upuść wymóg rezerwacji na dostępny przedział czasu.</span><span class="sxs-lookup"><span data-stu-id="10e06-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="10e06-126">Dokonaj rezerwacji zasobu w widoku dziennym i dowiedzieć się, który z zasobów wciąż można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="10e06-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="10e06-127">Na tablicy harmonogramu, wybierz **Tryb widoku** i wybierz **Dni**.</span><span class="sxs-lookup"><span data-stu-id="10e06-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="10e06-128">Pokazuje widok siatki mówiący o tym, ile godzin zasobu zostało zarezerwowane na dobę i w które dni zasób ten jest wolny.</span><span class="sxs-lookup"><span data-stu-id="10e06-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="10e06-129">Kliknij nazwę zasobu, który chcesz zerezerwować, a następnie wybierz **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="10e06-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="10e06-130">W oknie dialogowym **Rezerwacja zasobu (utwórz)** wybierz projekt, dla którego chcesz zarezerwować zasób, wraz z metodą rezerwacji oraz czasem rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="10e06-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="10e06-131">Kiedy skończysz, wybierz **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="10e06-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="10e06-132">Wyświetl tablicę harmonogramu</span><span class="sxs-lookup"><span data-stu-id="10e06-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="10e06-133">Wybierz niezaplanowany wymóg rezerwacji z listy u dołu.</span><span class="sxs-lookup"><span data-stu-id="10e06-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="10e06-134">Przeciągnij wymóg rezerwacji do dostępnego zasobu/przedziału czasu na tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="10e06-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="10e06-135">Kiedy skończysz, wybierz **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="10e06-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="10e06-136">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="10e06-136">Additional resources</span></span>  
 [<span data-ttu-id="10e06-137">Przewodnik menedżera zasobów</span><span class="sxs-lookup"><span data-stu-id="10e06-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)