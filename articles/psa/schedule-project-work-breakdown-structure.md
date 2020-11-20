---
title: Zaplanuj projekt ze strukturą podziału pracy
description: Planowanie projektu ze strukturą podziału pracy w Project Service
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127891"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="084c3-103">Zaplanuj projekt ze strukturą podziału pracy (Project Service)</span><span class="sxs-lookup"><span data-stu-id="084c3-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="084c3-104">Harmonogram projektu komunikuje, co jest niezbędne do wykonania pracy, które zasoby będą za to odpowiedzialne, i w jakich ramach czasowych praca musi zostać zrealizowana.</span><span class="sxs-lookup"><span data-stu-id="084c3-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="084c3-105">Harmonogram projektu odzwierciedla wszystkie prace związane z dostarczeniem projektu na czas.</span><span class="sxs-lookup"><span data-stu-id="084c3-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="084c3-106">Jednym z pierwszych kroków w początkowej fazie projektu jest opracowanie harmonogramu projektu.</span><span class="sxs-lookup"><span data-stu-id="084c3-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="084c3-107">Aby opracować harmonogram projektu musisz utworzyć strukturę podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="084c3-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="084c3-108">Utwórz strukturę projektu ze strukturą podziału pracy, co pomoże w:</span><span class="sxs-lookup"><span data-stu-id="084c3-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="084c3-109">Dokonaniu podziału pracy na zadania, którymi można zarządzać</span><span class="sxs-lookup"><span data-stu-id="084c3-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="084c3-110">Szacowaniu czasu wymaganego do wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="084c3-111">Ustawieniu czasu trwania zadania i współzależności między zadaniami</span><span class="sxs-lookup"><span data-stu-id="084c3-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="084c3-112">Określeniu ról wymaganych do wykonania każdego zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="084c3-113">Harmonogram projektu w strukturze podziału pracy ma znany wygląd i styl i jest uzupełniany interaktywnym wykresem Gantta.</span><span class="sxs-lookup"><span data-stu-id="084c3-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="084c3-114">Utwórz strukturę podziału pracy dla projektu</span><span class="sxs-lookup"><span data-stu-id="084c3-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="084c3-115">Utwórz strukturę podziału pracy, aby ukazać sekwencję zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="084c3-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="084c3-116">Struktura podziału pracy obejmuje zadania, wymogi dla każdego zadania i informacje o przychodach i kosztach.</span><span class="sxs-lookup"><span data-stu-id="084c3-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="084c3-117">W swojej strukturze podziału pracy możesz dodać poniższe informacje:</span><span class="sxs-lookup"><span data-stu-id="084c3-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="084c3-118">Sekwencja zadań w hierarchii</span><span class="sxs-lookup"><span data-stu-id="084c3-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="084c3-119">Inne zadania, jeśli istnieją takie, które należy wykonać przed rozpoczęciem zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="084c3-120">Data rozpoczęcia, data zakończenia i czas trwania zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="084c3-121">Liczba godzin wymagana do wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="084c3-122">Wymagane kwalifikacje pracownika i jego wykształcenie</span><span class="sxs-lookup"><span data-stu-id="084c3-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="084c3-123">Nazwiska pracowników przypisanych do zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="084c3-124">Szacowany przychód i koszty</span><span class="sxs-lookup"><span data-stu-id="084c3-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="084c3-125">Typy zadań</span><span class="sxs-lookup"><span data-stu-id="084c3-125">Task types</span></span>  
<span data-ttu-id="084c3-126">Tworząc swoje struktury podziału pracy, będziesz używać następujących typów zadań:</span><span class="sxs-lookup"><span data-stu-id="084c3-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="084c3-127">**Węzeł główny projektu**</span><span class="sxs-lookup"><span data-stu-id="084c3-127">**Project root node**</span></span> | <span data-ttu-id="084c3-128">Najwyższy poziom podsumowania dla projektu.</span><span class="sxs-lookup"><span data-stu-id="084c3-128">The top-level summary task for the project.</span></span> <span data-ttu-id="084c3-129">Wszystkie inne zadania projektu są tworzone na jego podstawie.</span><span class="sxs-lookup"><span data-stu-id="084c3-129">All other project tasks are created under it.</span></span> <span data-ttu-id="084c3-130">Nazwa zadania głównego jest nazwą projektu.</span><span class="sxs-lookup"><span data-stu-id="084c3-130">The name of the root task is the project name.</span></span> <span data-ttu-id="084c3-131">Nakład pracy, daty i czas trwania węzła głównego wynikają z wartości w hierarchii znajdującej się pod nim.</span><span class="sxs-lookup"><span data-stu-id="084c3-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="084c3-132">Nie możesz edytować właściwości węzła głównego ani go usunąć.</span><span class="sxs-lookup"><span data-stu-id="084c3-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="084c3-133">**Zadania sumaryczne lub zadania typu kontener**</span><span class="sxs-lookup"><span data-stu-id="084c3-133">**Summary or container tasks**</span></span> | <span data-ttu-id="084c3-134">Zadanie sumaryczne to zadanie, które składa się z podzadań.</span><span class="sxs-lookup"><span data-stu-id="084c3-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="084c3-135">Zadanie sumaryczne nie wiąże się z żadnym nakładem pracy, ani nie posiada kosztów własnych.</span><span class="sxs-lookup"><span data-stu-id="084c3-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="084c3-136">Jego nakład pracy i koszt są podsumowaniem jego podzadań.</span><span class="sxs-lookup"><span data-stu-id="084c3-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="084c3-137">Można zmienić nazwę zadania sumarycznego, ale nie można zmienić nakładu pracy, dat ani czasu trwania, ponieważ te są obliczane automatycznie.</span><span class="sxs-lookup"><span data-stu-id="084c3-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="084c3-138">Usunięcie zadania sumarycznego usuwa zadanie i wszystkie jego podzadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="084c3-139">**Zadania węzła liścia**</span><span class="sxs-lookup"><span data-stu-id="084c3-139">**Leaf node tasks**</span></span> | <span data-ttu-id="084c3-140">Zadanie węzła liścia reprezentuje najbardziej szczegółowe prace związane z projektem.</span><span class="sxs-lookup"><span data-stu-id="084c3-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="084c3-141">Ma szacunkowe nakłady pracy, planowaną liczbę zasobów, planowaną datę rozpoczęcia i zakończenia oraz czas trwania.</span><span class="sxs-lookup"><span data-stu-id="084c3-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="084c3-142">Hierarchia zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-142">Task hierarchy</span></span>  
 <span data-ttu-id="084c3-143">Podczas tworzenia hierarchii zadania masz dostępne następujące opcje:</span><span class="sxs-lookup"><span data-stu-id="084c3-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="084c3-144">**Dodaj zadanie**.</span><span class="sxs-lookup"><span data-stu-id="084c3-144">**Add task**.</span></span>   <span data-ttu-id="084c3-145">W wybranym miejscu w hierarchii zadania możesz dodać zadanie.</span><span class="sxs-lookup"><span data-stu-id="084c3-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="084c3-146">Jeśli nie wybierzesz miejsca, nowe zadanie pojawi się na końcu.</span><span class="sxs-lookup"><span data-stu-id="084c3-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="084c3-147">**Zwiększ wcięcie zadania**.</span><span class="sxs-lookup"><span data-stu-id="084c3-147">**Indent task**.</span></span>   <span data-ttu-id="084c3-148">Utwórz wcięcie zadania, aby stało się ono elementem podrzędnym zadania znajdującego się bezpośrednio nad nim.</span><span class="sxs-lookup"><span data-stu-id="084c3-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="084c3-149">**Zmniejsz wcięcie zadania**.</span><span class="sxs-lookup"><span data-stu-id="084c3-149">**Outdent task**.</span></span>   <span data-ttu-id="084c3-150">Zmniejsz wcięcie zadania, aby nie było już ono podzadaniem oryginalnego zadania nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="084c3-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="084c3-151">**Przenieś w górę i w dół**.</span><span class="sxs-lookup"><span data-stu-id="084c3-151">**Move up and Move down**.</span></span>   <span data-ttu-id="084c3-152">Przenoszenie zadań w górę i w dół w hierarchii jego zadania nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="084c3-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="084c3-153">Przenoszenie zadania w górę lub w dół nie wpływa na związany z nim nakład pracy, koszt, daty i czas trwania.</span><span class="sxs-lookup"><span data-stu-id="084c3-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="084c3-154">Atrybuty zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-154">Task attributes</span></span>  
 <span data-ttu-id="084c3-155">Nazwa zadania opisuje czynności, które należy wykonać.</span><span class="sxs-lookup"><span data-stu-id="084c3-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="084c3-156">Różne atrybuty zadań służą do opisywania harmonogramu i wymagań dotyczących personelu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="084c3-157">Zaplanuj atrybuty</span><span class="sxs-lookup"><span data-stu-id="084c3-157">Schedule attributes</span></span>

 - <span data-ttu-id="084c3-158">Przypisz wartości do **Nakład pracy w godzinach**, **Liczba zasobów**, **Data rozpoczęcia**, **Data zakończenia**, i **Czas trwania**, aby ustalić harmonogram dla zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="084c3-159">**Nakład pracy** to przybliżona liczba godzin potrzebnych do wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="084c3-160">**Liczba zasobów** to oszacowanie, które menedżer projektu umieszcza w zadaniu, aby pomóc opracować najlepszy możliwy harmonogram.</span><span class="sxs-lookup"><span data-stu-id="084c3-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="084c3-161">**Czas trwania** (w dniach) wskazuje liczbę dni pracy niezbędnych do ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="084c3-162">Atrybuty personelu</span><span class="sxs-lookup"><span data-stu-id="084c3-162">Staffing attributes</span></span>

 - <span data-ttu-id="084c3-163">**Rola**, **Jednostka organizacyjna zasobu**, **Liczba zasobów**, i **Zasoby** opisują wymagania dotyczące personelu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="084c3-164">**Rola** opisuje typ zasobu potrzebnego do wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="084c3-165">**Jednostka organizacyjna zasobu** wskazuje jednostkę organizacyjną, z której ma pochodzić zasób dla tego zadania; wpływa to również na koszt i prognozy sprzedaży dla zadania, ponieważ jest uwzględniane przy określaniu jednostkowej ceny sprzedaży dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="084c3-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="084c3-166">**Zasoby** to zasób rodzajowy lub zasób posiadający nazwę, jeśli taki zostanie znaleziony.</span><span class="sxs-lookup"><span data-stu-id="084c3-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="084c3-167">Zależności między zadaniami</span><span class="sxs-lookup"><span data-stu-id="084c3-167">Task dependencies</span></span>  
 <span data-ttu-id="084c3-168">Możesz tworzyć relacje poprzednika między jednym lub kilkoma zadaniami w strukturze podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="084c3-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="084c3-169">Możesz ustawić jedną lub więcej wartości dla pola poprzednika dla zadań, aby wskazać zadania, od których będzie to zależne.</span><span class="sxs-lookup"><span data-stu-id="084c3-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="084c3-170">Podczas przypisywania wartości poprzednika do zadania, zadanie może się rozpocząć po zakończeniu wszystkich zadań poprzedników.</span><span class="sxs-lookup"><span data-stu-id="084c3-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="084c3-171">Ustawienie tej współzależności dla zadania spowoduje ponowne obliczenie planowanej daty rozpoczęcia zadania jako najnowszego zakończenia wszystkich poprzedników.</span><span class="sxs-lookup"><span data-stu-id="084c3-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="084c3-172">Wpływy na harmonogram związane z poprzednikiem nie są ograniczone przez tryb zadania zdefiniowany dla zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="084c3-173">Tryb zadania</span><span class="sxs-lookup"><span data-stu-id="084c3-173">Task mode</span></span>  
 <span data-ttu-id="084c3-174">Tryb zadania jest jednym z najważniejszych czynników określających planowanie zadań węzła liścia.</span><span class="sxs-lookup"><span data-stu-id="084c3-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="084c3-175">Istnieją dwa tryby zadania dla każdego zadania: tryb planowania automatycznego i tryb planowania ręcznego.</span><span class="sxs-lookup"><span data-stu-id="084c3-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="084c3-176">**Automatyczne planowanie**.</span><span class="sxs-lookup"><span data-stu-id="084c3-176">**Auto scheduling**.</span></span>   <span data-ttu-id="084c3-177">Po ustawieniu trybu zadania na Automatyczne planowanie aparat planowania zadania używa reguł planowania na poniższych atrybutach zadania, aby ustalić harmonogram dla zadania:</span><span class="sxs-lookup"><span data-stu-id="084c3-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="084c3-178">Elementy poprzedzające</span><span class="sxs-lookup"><span data-stu-id="084c3-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="084c3-179">Nakład pracy</span><span class="sxs-lookup"><span data-stu-id="084c3-179">Effort</span></span>  
  
    -   <span data-ttu-id="084c3-180">Liczba zasobów</span><span class="sxs-lookup"><span data-stu-id="084c3-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="084c3-181">daty rozpoczęcia i zakończenia;</span><span class="sxs-lookup"><span data-stu-id="084c3-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="084c3-182">**Reguły planowania**.</span><span class="sxs-lookup"><span data-stu-id="084c3-182">**Scheduling rules**.</span></span>   <span data-ttu-id="084c3-183">Data rozpoczęcia zadania węzła liścia, które nie ma poprzedników daje domyślnie zaplanowaną datę rozpoczęcia projektu.</span><span class="sxs-lookup"><span data-stu-id="084c3-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="084c3-184">Czas trwania zadania węzła liścia jest zawsze obliczany jako liczba dni roboczych pomiędzy datą rozpoczęcia a datą zakończenia.</span><span class="sxs-lookup"><span data-stu-id="084c3-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="084c3-185">Gdy zadanie jest planowane automatycznie, aparat planowania kieruje się poniższymi regułami:</span><span class="sxs-lookup"><span data-stu-id="084c3-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="084c3-186">Daty rozpoczęcia i zakończenia zadania muszą być zawsze dniami roboczymi w kalendarzu planowania projektu</span><span class="sxs-lookup"><span data-stu-id="084c3-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="084c3-187">Data rozpoczęcia zadania, które ma poprzedników, staje się domyślnie najpóźniejszą datą zakończenia poprzedników</span><span class="sxs-lookup"><span data-stu-id="084c3-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="084c3-188">Nakład pracy = Liczba osób \* Czas trwania \* godziny w standardowym dniu pracy kalendarza projektu</span><span class="sxs-lookup"><span data-stu-id="084c3-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="084c3-189">**Planowanie ręczne**.</span><span class="sxs-lookup"><span data-stu-id="084c3-189">**Manual scheduling**.</span></span>   <span data-ttu-id="084c3-190">W niektórych przypadkach możesz chcieć odstąpić od tych zasad.</span><span class="sxs-lookup"><span data-stu-id="084c3-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="084c3-191">W takich przypadkach możesz ustawić, aby tryb zadania dla zadania był planowany ręcznie.</span><span class="sxs-lookup"><span data-stu-id="084c3-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="084c3-192">Zatrzymuje to aparat planowania przed obliczaniem wartości dla innych atrybutów planowania.</span><span class="sxs-lookup"><span data-stu-id="084c3-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="084c3-193">Ustawienie poprzedników zadań zawsze wpływa na datę rozpoczęcia zadania zależnego.</span><span class="sxs-lookup"><span data-stu-id="084c3-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="084c3-194">Utwórz strukturę podziału pracy</span><span class="sxs-lookup"><span data-stu-id="084c3-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="084c3-195">Przejdź do **Project Service > Projekty**.</span><span class="sxs-lookup"><span data-stu-id="084c3-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="084c3-196">Kliknij projekt, nad którym chcesz pracować.</span><span class="sxs-lookup"><span data-stu-id="084c3-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="084c3-197">Na pasku u góry ekranu, wybierz strzałkę w dół obok nazwy projektu, a następnie kliknij Struktura podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="084c3-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="084c3-198">Aby dodać zadanie, kliknij **Dodaj zadanie**.</span><span class="sxs-lookup"><span data-stu-id="084c3-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="084c3-199">Wypełnij pola dla zadania, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="084c3-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="084c3-200">Kontynuuj dodawanie zadań do momentu ukończenia struktury podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="084c3-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="084c3-201">Podczas tworzenia struktury podziału pracy, możesz wykonać następujące czynności w celu uporządkowania zadań:</span><span class="sxs-lookup"><span data-stu-id="084c3-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="084c3-202">Zaznacz zadanie, a następnie kliknij **Wcięcie**, aby przesunąć je pod inne zadanie lub kliknij Zmniejsz wcięcie, aby wyprowadzić je spod innego zadania.</span><span class="sxs-lookup"><span data-stu-id="084c3-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="084c3-203">Zaznacz zadanie, a następnie kliknij **Przenieś w górę** lub **Przenieś w dół**, aby przenieść je w górę lub w dół na liście.</span><span class="sxs-lookup"><span data-stu-id="084c3-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="084c3-204">Kliknij **Ukryj wykres Gantta**, aby ukryć wykres Gantta, a następnie kliknij **Pokaż wykres Gantta**, aby wyświetlić go ponownie.</span><span class="sxs-lookup"><span data-stu-id="084c3-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="084c3-205">Wybierz inny okres czasu dla wykresu Gantta w **Skala czasu**.</span><span class="sxs-lookup"><span data-stu-id="084c3-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="084c3-206">Aby dodać role określone w strukturze podziału pracy do członków zespołu projektu, kliknij **Generuj zespół projektu**.</span><span class="sxs-lookup"><span data-stu-id="084c3-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="084c3-207">Po zakończeniu wprowadzania zmian kliknij **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="084c3-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="084c3-208">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="084c3-208">See Also</span></span>  
 [<span data-ttu-id="084c3-209">Przewodnik menedżera projektu</span><span class="sxs-lookup"><span data-stu-id="084c3-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
