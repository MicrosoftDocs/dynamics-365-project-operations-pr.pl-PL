---
title: Zagadnienia dotyczące uaktualniania struktury podziału pracy
description: W tym temacie zamieszczono informacje dotyczące uaktualniania struktury podziału pracy w programie Project Service Automation z wersji 2.x do 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754362"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="d7ff6-103">Zagadnienia dotyczące uaktualniania struktury podziału pracy</span><span class="sxs-lookup"><span data-stu-id="d7ff6-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="d7ff6-104">W tym temacie zamieszczono informacje dotyczące uaktualniania struktury podziału pracy w programie Project Service Automation z wersji 2.x do 3.x.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="d7ff6-105">Ten temat określa dobrą kondycję projektu w rozwiązaniu Project Service Automation (PSA), która jest niezbędna do pomyślnego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="d7ff6-106">Są tu również informacje o typowych sytuacjach blokowania, które spowodują niepowodzenie uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="d7ff6-107">Aby uzyskać więcej informacji na temat definiowania zadań w projektach i ich funkcjach w harmonogramie projektu, zobacz [Harmonogramy projektów](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="d7ff6-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="d7ff6-108">Kluczowe encje</span><span class="sxs-lookup"><span data-stu-id="d7ff6-108">Key entities</span></span>
<span data-ttu-id="d7ff6-109">Dokładna struktura podziału pracy, do której już załadowano zasoby, musi mieć następujące encje:</span><span class="sxs-lookup"><span data-stu-id="d7ff6-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="d7ff6-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="d7ff6-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="d7ff6-111">Zespół projektu</span><span class="sxs-lookup"><span data-stu-id="d7ff6-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="d7ff6-112">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="d7ff6-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="d7ff6-113">Przypisania zasobów</span><span class="sxs-lookup"><span data-stu-id="d7ff6-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="d7ff6-114">Zależność zadania projektu</span><span class="sxs-lookup"><span data-stu-id="d7ff6-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="d7ff6-115">Zasoby, które można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="d7ff6-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="d7ff6-116">W celu zdefiniowania struktury podziału pracy z załadowanymi zasobami należy wykonać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="d7ff6-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="d7ff6-117">Utwórz nowy projekt.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-117">Create a new project.</span></span> <span data-ttu-id="d7ff6-118">Aby uzyskać więcej informacji na temat tworzenia nowego projektu, zobacz [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="d7ff6-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="d7ff6-119">Utwórz jedno lub więcej zadań.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-119">Create one or more tasks.</span></span> <span data-ttu-id="d7ff6-120">Aby uzyskać więcej informacji na temat tworzenia zadania, zobacz [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="d7ff6-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="d7ff6-121">Zdefiniuj zależności zadań.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-121">Define the task dependencies.</span></span> <span data-ttu-id="d7ff6-122">Aby uzyskać więcej informacji, zobacz [Zależność zadań projektu](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="d7ff6-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="d7ff6-123">Przypisz członków zespołu projektu do projektu.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-123">Assign project team members to the project.</span></span> <span data-ttu-id="d7ff6-124">Aby uzyskać więcej informacji, zobacz [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="d7ff6-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="d7ff6-125">Przypisz członków zespołu projektu do zadań.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="d7ff6-126">Aby uzyskać więcej informacji, zobacz [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d7ff6-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="d7ff6-127">Relacje w zespole projektu</span><span class="sxs-lookup"><span data-stu-id="d7ff6-127">Project team relationships</span></span>

<span data-ttu-id="d7ff6-128">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="d7ff6-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="d7ff6-129">Wszyscy członkowie zespołu projektu muszą być skojarzeni z zasobami możliwymi do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="d7ff6-130">Wszyscy członkowie zespołu projektu muszą być skojarzeni z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="d7ff6-131">Relacje zadań projektu</span><span class="sxs-lookup"><span data-stu-id="d7ff6-131">Project task relationships</span></span>
<span data-ttu-id="d7ff6-132">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="d7ff6-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="d7ff6-133">Wszystkie powiązane zadania muszą być skojarzone z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="d7ff6-134">Każde zadanie wiersza musi mieć zadanie nadrzędne.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="d7ff6-135">Każde zadanie musi mieć projekt nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="d7ff6-136">Obowiązujące warunki</span><span class="sxs-lookup"><span data-stu-id="d7ff6-136">Valid conditions</span></span>

- <span data-ttu-id="d7ff6-137">Wszystkie czasy trwania zadań muszą być większe lub równe (>=) jednej godzinie, a krótsze niż 1 800 000 minut (1250 dni).\*</span><span class="sxs-lookup"><span data-stu-id="d7ff6-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="d7ff6-138">Wszystkie zadania muszą mieć datę rozpoczęcia nie wcześniejszą niż 1 stycznia 2000 r.\*</span><span class="sxs-lookup"><span data-stu-id="d7ff6-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="d7ff6-139">Wszystkie zadania muszą mieć datę rozpoczęcia nie późniejszą niż 17 lat od bieżącego dnia.\*</span><span class="sxs-lookup"><span data-stu-id="d7ff6-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="d7ff6-140">Wszystkie zadania muszą mieć datę rozpoczęcia wcześniejszą niż data zakończenia lub jej równą.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="d7ff6-141">Wszystkie typy transakcji w klasyfikacjach (Wydatek, Materiał, Podatek i Czas) muszą mieć wartości w ustawieniach **Jednostka domyślna** i **Grupa jednostek**.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="d7ff6-142">Należy unikać używania formatów daty z literami.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="d7ff6-143">Potencjalne kroki ograniczenia ryzyka</span><span class="sxs-lookup"><span data-stu-id="d7ff6-143">Potential mitigation steps</span></span>
- <span data-ttu-id="d7ff6-144">Użycie funkcji szukania zaawansowanego w celu zidentyfikowania zadań projektu, które nie zawierają identyfikatora projektu.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="d7ff6-145">Przy użyciu funkcji Szukanie zaawansowane można identyfikować zadania projektu, w których zaplanowany czas trwania jest większy niż > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="d7ff6-146">Przed wprowadzeniem jakichkolwiek zmian w danych należy przeanalizować wszystkie dostosowania skojarzone z encją, które mogły doprowadzić do nieprawidłowego stanu danych.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="d7ff6-147">Te dostosowania należy rozwiązać przed kontynuowaniem jakichkolwiek aktualizacji dotyczących danych.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="d7ff6-148">W przypadku zidentyfikowanych oddzielonych zadań warto rozważyć ich usunięcie, jeśli nie są one potrzebne lub które powinny być skojarzone z poprawnym projektem nadrzędnym.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="d7ff6-149">W przypadku każdego zadania, w którym czas trwania wynosi więcej niż 1250 dni, warto rozważyć dodanie wielu zadań w celu przedstawienia łącznego czasu trwania, o ile jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="d7ff6-150">Elementy oznaczone gwiazdką (\*) mają ograniczenia wynikające z faktu, że system zarządzania relacjami z klientami (CRM) obsługuje tylko 7320 rozszerzeń cyklu.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="d7ff6-151">Należy pozostać poniżej tego limitu.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="d7ff6-152">Relacje przypisania zasobów</span><span class="sxs-lookup"><span data-stu-id="d7ff6-152">Resource Assignment relationships</span></span>
<span data-ttu-id="d7ff6-153">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="d7ff6-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="d7ff6-154">Wszystkie przypisania zasobów w strukturze podziału pracy muszą być powiązane z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="d7ff6-155">Wszystkie przypisania zasobów w strukturze podziału pracy muszą być skojarzone z członkami zespołu projektu w tym samym projekcie.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="d7ff6-156">Potencjalne kroki ograniczenia ryzyka</span><span class="sxs-lookup"><span data-stu-id="d7ff6-156">Potential mitigation steps</span></span>
- <span data-ttu-id="d7ff6-157">Zidentyfikuj wszystkie zadania, które nie mieszczą się poza powyższymi warunkami.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="d7ff6-158">Wszystkie przydziały zasobów, które nie są już ważne, powinny zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="d7ff6-159">Relacje zależność zadań projektu</span><span class="sxs-lookup"><span data-stu-id="d7ff6-159">Project task dependency relationships</span></span>
<span data-ttu-id="d7ff6-160">W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:</span><span class="sxs-lookup"><span data-stu-id="d7ff6-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="d7ff6-161">Wszystkie zależności zadań projektu muszą być powiązane z tym samym projektem.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="d7ff6-162">Zadanie może się odwoływać tylko raz do każdego elementu stanowiącego zależność.</span><span class="sxs-lookup"><span data-stu-id="d7ff6-162">A task can't have the same dependency referenced more than once.</span></span>
