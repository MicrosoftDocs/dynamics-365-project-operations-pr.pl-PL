---
title: Zagadnienia dotyczące uaktualniania struktury podziału pracy
description: W tym temacie zamieszczono informacje dotyczące uaktualniania struktury podziału pracy w programie Project Service Automation z wersji 2.x do 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951357"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="63c79-103">Zagadnienia dotyczące uaktualniania struktury podziału pracy</span><span class="sxs-lookup"><span data-stu-id="63c79-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="63c79-104">W tym temacie zamieszczono informacje dotyczące uaktualniania struktury podziału pracy w programie Project Service Automation z wersji 2.x do 3.x.</span><span class="sxs-lookup"><span data-stu-id="63c79-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="63c79-105">Ten temat określa dobrą kondycję projektu w rozwiązaniu Project Service Automation (PSA), która jest niezbędna do pomyślnego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="63c79-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="63c79-106">Są tu również informacje o typowych sytuacjach blokowania, które spowodują niepowodzenie uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="63c79-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="63c79-107">Aby uzyskać więcej informacji na temat definiowania zadań w projektach i ich funkcjach w harmonogramie projektu, zobacz [Harmonogramy projektów](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="63c79-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="63c79-108">Kluczowe encje</span><span class="sxs-lookup"><span data-stu-id="63c79-108">Key entities</span></span>
<span data-ttu-id="63c79-109">Dokładna struktura podziału pracy, do której już załadowano zasoby, musi mieć następujące encje:</span><span class="sxs-lookup"><span data-stu-id="63c79-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="63c79-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="63c79-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="63c79-111">Zespół projektu</span><span class="sxs-lookup"><span data-stu-id="63c79-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="63c79-112">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="63c79-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="63c79-113">Przypisania zasobów</span><span class="sxs-lookup"><span data-stu-id="63c79-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="63c79-114">Zależność zadania projektu</span><span class="sxs-lookup"><span data-stu-id="63c79-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="63c79-115">Zasoby, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="63c79-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="63c79-116">W celu zdefiniowania struktury podziału pracy z załadowanymi zasobami należy wykonać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="63c79-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="63c79-117">Utwórz nowy projekt.</span><span class="sxs-lookup"><span data-stu-id="63c79-117">Create a new project.</span></span> <span data-ttu-id="63c79-118">Aby uzyskać więcej informacji na temat tworzenia nowego projektu, zobacz [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="63c79-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="63c79-119">Utwórz jedno lub więcej zadań.</span><span class="sxs-lookup"><span data-stu-id="63c79-119">Create one or more tasks.</span></span> <span data-ttu-id="63c79-120">Aby uzyskać więcej informacji na temat tworzenia zadania, zobacz [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="63c79-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="63c79-121">Zdefiniuj zależności zadań.</span><span class="sxs-lookup"><span data-stu-id="63c79-121">Define the task dependencies.</span></span> <span data-ttu-id="63c79-122">Aby uzyskać więcej informacji, zobacz [Zależność zadań projektu](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="63c79-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="63c79-123">Przypisz członków zespołu projektu do projektu.</span><span class="sxs-lookup"><span data-stu-id="63c79-123">Assign project team members to the project.</span></span> <span data-ttu-id="63c79-124">Aby uzyskać więcej informacji, zobacz [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="63c79-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="63c79-125">Przypisz członków zespołu projektu do zadań.</span><span class="sxs-lookup"><span data-stu-id="63c79-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="63c79-126">Aby uzyskać więcej informacji, zobacz [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="63c79-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="63c79-127">Relacje w zespole projektu</span><span class="sxs-lookup"><span data-stu-id="63c79-127">Project team relationships</span></span>

<span data-ttu-id="63c79-128">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="63c79-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="63c79-129">Wszyscy członkowie zespołu projektu muszą być skojarzeni z zasobami możliwymi do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="63c79-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="63c79-130">Wszyscy członkowie zespołu projektu muszą być skojarzeni z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="63c79-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="63c79-131">Relacje zadań projektu</span><span class="sxs-lookup"><span data-stu-id="63c79-131">Project task relationships</span></span>
<span data-ttu-id="63c79-132">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="63c79-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="63c79-133">Wszystkie powiązane zadania muszą być skojarzone z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="63c79-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="63c79-134">Każde zadanie wiersza musi mieć zadanie nadrzędne.</span><span class="sxs-lookup"><span data-stu-id="63c79-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="63c79-135">Każde zadanie musi mieć projekt nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="63c79-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="63c79-136">Obowiązujące warunki</span><span class="sxs-lookup"><span data-stu-id="63c79-136">Valid conditions</span></span>

- <span data-ttu-id="63c79-137">Wszystkie czasy trwania zadań muszą być większe lub równe (>=) jednej godzinie, a krótsze niż 1 800 000 minut (1250 dni).\*</span><span class="sxs-lookup"><span data-stu-id="63c79-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="63c79-138">Wszystkie zadania muszą mieć datę rozpoczęcia nie wcześniejszą niż 1 stycznia 2000 r.\*</span><span class="sxs-lookup"><span data-stu-id="63c79-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="63c79-139">Wszystkie zadania muszą mieć datę rozpoczęcia nie późniejszą niż 17 lat od bieżącego dnia.\*</span><span class="sxs-lookup"><span data-stu-id="63c79-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="63c79-140">Wszystkie zadania muszą mieć datę rozpoczęcia wcześniejszą niż data zakończenia lub jej równą.</span><span class="sxs-lookup"><span data-stu-id="63c79-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="63c79-141">Wszystkie typy transakcji w klasyfikacjach (Wydatek, Materiał, Podatek i Czas) muszą mieć wartości w ustawieniach **Jednostka domyślna** i **Grupa jednostek**.</span><span class="sxs-lookup"><span data-stu-id="63c79-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="63c79-142">Należy unikać używania formatów daty z literami.</span><span class="sxs-lookup"><span data-stu-id="63c79-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="63c79-143">Potencjalne kroki ograniczenia ryzyka</span><span class="sxs-lookup"><span data-stu-id="63c79-143">Potential mitigation steps</span></span>
- <span data-ttu-id="63c79-144">Użycie funkcji szukania zaawansowanego w celu zidentyfikowania zadań projektu, które nie zawierają identyfikatora projektu.</span><span class="sxs-lookup"><span data-stu-id="63c79-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="63c79-145">Przy użyciu funkcji Szukanie zaawansowane można identyfikować zadania projektu, w których zaplanowany czas trwania jest większy niż > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="63c79-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="63c79-146">Przed wprowadzeniem jakichkolwiek zmian w danych należy przeanalizować wszystkie dostosowania skojarzone z encją, które mogły doprowadzić do nieprawidłowego stanu danych.</span><span class="sxs-lookup"><span data-stu-id="63c79-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="63c79-147">Te dostosowania należy rozwiązać przed kontynuowaniem jakichkolwiek aktualizacji dotyczących danych.</span><span class="sxs-lookup"><span data-stu-id="63c79-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="63c79-148">W przypadku zidentyfikowanych oddzielonych zadań warto rozważyć ich usunięcie, jeśli nie są one potrzebne lub które powinny być skojarzone z poprawnym projektem nadrzędnym.</span><span class="sxs-lookup"><span data-stu-id="63c79-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="63c79-149">W przypadku każdego zadania, w którym czas trwania wynosi więcej niż 1250 dni, warto rozważyć dodanie wielu zadań w celu przedstawienia łącznego czasu trwania, o ile jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="63c79-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="63c79-150">Elementy oznaczone gwiazdką (\*) mają ograniczenia wynikające z faktu, że system zarządzania relacjami z klientami (CRM) obsługuje tylko 7320 rozszerzeń cyklu.</span><span class="sxs-lookup"><span data-stu-id="63c79-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="63c79-151">Należy pozostać poniżej tego limitu.</span><span class="sxs-lookup"><span data-stu-id="63c79-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="63c79-152">Relacje przypisania zasobów</span><span class="sxs-lookup"><span data-stu-id="63c79-152">Resource Assignment relationships</span></span>
<span data-ttu-id="63c79-153">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="63c79-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="63c79-154">Wszystkie przypisania zasobów w strukturze podziału pracy muszą być powiązane z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="63c79-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="63c79-155">Wszystkie przypisania zasobów w strukturze podziału pracy muszą być skojarzone z członkami zespołu projektu w tym samym projekcie.</span><span class="sxs-lookup"><span data-stu-id="63c79-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="63c79-156">Potencjalne kroki ograniczenia ryzyka</span><span class="sxs-lookup"><span data-stu-id="63c79-156">Potential mitigation steps</span></span>
- <span data-ttu-id="63c79-157">Zidentyfikuj wszystkie zadania, które nie mieszczą się poza powyższymi warunkami.</span><span class="sxs-lookup"><span data-stu-id="63c79-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="63c79-158">Wszystkie przydziały zasobów, które nie są już ważne, powinny zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="63c79-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="63c79-159">Relacje zależność zadań projektu</span><span class="sxs-lookup"><span data-stu-id="63c79-159">Project task dependency relationships</span></span>
<span data-ttu-id="63c79-160">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="63c79-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="63c79-161">Wszystkie zależności zadań projektu muszą być powiązane z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="63c79-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="63c79-162">Zadanie może się odwoływać tylko raz do każdego elementu stanowiącego zależność.</span><span class="sxs-lookup"><span data-stu-id="63c79-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]