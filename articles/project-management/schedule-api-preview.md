---
title: Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania
description: To temat zawiera informacje i przykłady dotyczące korzystania z interfejsów API planowania.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868142"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="c02d2-103">Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania</span><span class="sxs-lookup"><span data-stu-id="c02d2-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="c02d2-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="c02d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="c02d2-105">Niektóre lub wszystkie funkcje wymienione w tym temacie są dostępne w wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="c02d2-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="c02d2-106">Zawartość i funkcjonalność mogą ulec zmianie.</span><span class="sxs-lookup"><span data-stu-id="c02d2-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="c02d2-107">Encje planowania</span><span class="sxs-lookup"><span data-stu-id="c02d2-107">Scheduling entities</span></span>

<span data-ttu-id="c02d2-108">Harmonogramy API zapewniają możliwość tworzenia, aktualizowania i usuwania operacji z **Encje planowania**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="c02d2-109">Te jednostki są zarządzane za pomocą aparatu planowania w Project dla sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c02d2-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="c02d2-110">We wcześniejszych wersjach Dynamics 365 Project Operations operacje tworzenia, aktualizowania i usuwania **Encji planowania** były ograniczone.</span><span class="sxs-lookup"><span data-stu-id="c02d2-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="c02d2-111">W poniższej tabeli przedstawiono pełną listę **Encje planowania**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="c02d2-112">Nazwa encji</span><span class="sxs-lookup"><span data-stu-id="c02d2-112">Entity name</span></span>  | <span data-ttu-id="c02d2-113">Logiczna nazwa encji</span><span class="sxs-lookup"><span data-stu-id="c02d2-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="c02d2-114">Project</span><span class="sxs-lookup"><span data-stu-id="c02d2-114">Project</span></span> | <span data-ttu-id="c02d2-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="c02d2-115">msdyn_project</span></span> |
| <span data-ttu-id="c02d2-116">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-116">Project Task</span></span>  | <span data-ttu-id="c02d2-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="c02d2-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="c02d2-118">Zależność zadania projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-118">Project Task Dependency</span></span>  | <span data-ttu-id="c02d2-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="c02d2-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="c02d2-120">Przypisanie zasobu</span><span class="sxs-lookup"><span data-stu-id="c02d2-120">Resource Assignment</span></span> | <span data-ttu-id="c02d2-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="c02d2-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="c02d2-122">Zasobnik projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-122">Project Bucket</span></span>  | <span data-ttu-id="c02d2-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="c02d2-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="c02d2-124">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-124">Project Team Member</span></span> | <span data-ttu-id="c02d2-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="c02d2-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="c02d2-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="c02d2-126">OperationSet</span></span>

<span data-ttu-id="c02d2-127">OperationSet to wzorzec jednostki pracy, którego można użyć, gdy w ramach transakcji musi zostać przetworzonych kilka żądań mających wpływ na harmonogram.</span><span class="sxs-lookup"><span data-stu-id="c02d2-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="c02d2-128">Planowanie interfejsów API</span><span class="sxs-lookup"><span data-stu-id="c02d2-128">Schedule APIs</span></span>

<span data-ttu-id="c02d2-129">Poniżej przedstawiono listę bieżących interfejsów API planowania.</span><span class="sxs-lookup"><span data-stu-id="c02d2-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="c02d2-130">**msdyn_CreateProjectV1**: tego interfejsu API można używać do tworzenia projektu.</span><span class="sxs-lookup"><span data-stu-id="c02d2-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="c02d2-131">Projekt i domyślny rozmiar projektu są tworzone natychmiast.</span><span class="sxs-lookup"><span data-stu-id="c02d2-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="c02d2-132">**msdyn_CreateTeamMemberV1**: tego interfejsu API można używać do tworzenia członka zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="c02d2-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="c02d2-133">Rekord członka zespołu jest tworzony natychmiast.</span><span class="sxs-lookup"><span data-stu-id="c02d2-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="c02d2-134">**msdyn_CreateOperationSetV1**: ten interfejs API może być używany do planowania kilku żądań, które muszą zostać wykonane w ramach transakcji.</span><span class="sxs-lookup"><span data-stu-id="c02d2-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="c02d2-135">**msdyn_PSSCreateV1**: tego interfejsu API można używać do tworzenia encji.</span><span class="sxs-lookup"><span data-stu-id="c02d2-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="c02d2-136">Może to być dowolny z obiektów planowania obsługujący operację tworzenia.</span><span class="sxs-lookup"><span data-stu-id="c02d2-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="c02d2-137">**msdyn_PSSUpdateV1**: tego interfejsu API można używać do aktualizacji encji.</span><span class="sxs-lookup"><span data-stu-id="c02d2-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="c02d2-138">Może to być dowolny z obiektów planowania obsługujący operację aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c02d2-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="c02d2-139">**msdyn_PSSDeleteV1**: tego interfejsu API można używać do usuwania encji.</span><span class="sxs-lookup"><span data-stu-id="c02d2-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="c02d2-140">Może to być dowolny z obiektów planowania obsługujący operację usuwania.</span><span class="sxs-lookup"><span data-stu-id="c02d2-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="c02d2-141">**msdyn_ExecuteOperationSetV1**: ten interfejs API jest używany do wykonywania wszystkich operacji w ramach danego zestawu operacji.</span><span class="sxs-lookup"><span data-stu-id="c02d2-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="c02d2-142">Używanie interfejsów API harmonogramu z zestawem OperationSet</span><span class="sxs-lookup"><span data-stu-id="c02d2-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="c02d2-143">Ponieważ rekordy z zarówno **CreateProjectV1**, jak i **CreateTeamMemberV1** są tworzone natychmiast, tych interfejsów API nie można używać bezpośrednio w przy użyciu zestawu **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="c02d2-144">Interfejs API umożliwia jednak tworzenie potrzebnych rekordów, tworzenie zestawu **OperationSet**, a następnie używanie tych wstępnie utworzonych rekordów w zestawie **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="c02d2-145">Obsługiwane operacje</span><span class="sxs-lookup"><span data-stu-id="c02d2-145">Supported operations</span></span>

| <span data-ttu-id="c02d2-146">Encja planowania</span><span class="sxs-lookup"><span data-stu-id="c02d2-146">Scheduling entity</span></span> | <span data-ttu-id="c02d2-147">Utworzenie</span><span class="sxs-lookup"><span data-stu-id="c02d2-147">Create</span></span> | <span data-ttu-id="c02d2-148">Zaktualizuj</span><span class="sxs-lookup"><span data-stu-id="c02d2-148">Update</span></span> | <span data-ttu-id="c02d2-149">Delete</span><span class="sxs-lookup"><span data-stu-id="c02d2-149">Delete</span></span> | <span data-ttu-id="c02d2-150">Ważne uwagi</span><span class="sxs-lookup"><span data-stu-id="c02d2-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="c02d2-151">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-151">Project task</span></span> | <span data-ttu-id="c02d2-152">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-152">Yes</span></span> | <span data-ttu-id="c02d2-153">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-153">Yes</span></span> | <span data-ttu-id="c02d2-154">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-154">Yes</span></span> | <span data-ttu-id="c02d2-155">Brak</span><span class="sxs-lookup"><span data-stu-id="c02d2-155">None</span></span> |
| <span data-ttu-id="c02d2-156">Zależność zadania projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-156">Project task dependency</span></span> | <span data-ttu-id="c02d2-157">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-157">Yes</span></span> | <span data-ttu-id="c02d2-158">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-158">Yes</span></span> | | <span data-ttu-id="c02d2-159">Rekordy zależności zadań projektu nie są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="c02d2-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="c02d2-160">Zamiast tego można usunąć stary rekord i utworzyć nowy rekord.</span><span class="sxs-lookup"><span data-stu-id="c02d2-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c02d2-161">Przypisanie zasobu</span><span class="sxs-lookup"><span data-stu-id="c02d2-161">Resource assignment</span></span> | <span data-ttu-id="c02d2-162">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-162">Yes</span></span> | <span data-ttu-id="c02d2-163">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-163">Yes</span></span> | | <span data-ttu-id="c02d2-164">Operacje z następującymi polami nie są obsługiwane: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="c02d2-165">Rekordy przypisania zasobów nie są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="c02d2-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="c02d2-166">Zamiast tego można usunąć stary rekord i utworzyć nowy rekord.</span><span class="sxs-lookup"><span data-stu-id="c02d2-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c02d2-167">Zasobnik projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-167">Project bucket</span></span> | <span data-ttu-id="c02d2-168">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="c02d2-168">N/A</span></span> | <span data-ttu-id="c02d2-169">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="c02d2-169">N/A</span></span> | <span data-ttu-id="c02d2-170">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="c02d2-170">N/A</span></span> | <span data-ttu-id="c02d2-171">Domyślny domyślny rozmiar jest tworzony przy użyciu interfejsu **API CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="c02d2-172">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="c02d2-172">Project team member</span></span> | <span data-ttu-id="c02d2-173">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-173">Yes</span></span> | <span data-ttu-id="c02d2-174">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-174">Yes</span></span> | <span data-ttu-id="c02d2-175">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-175">Yes</span></span> | <span data-ttu-id="c02d2-176">Aby utworzyć operację tworzenia, użyj interfejsu API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="c02d2-177">Project</span><span class="sxs-lookup"><span data-stu-id="c02d2-177">Project</span></span> | <span data-ttu-id="c02d2-178">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-178">Yes</span></span> | <span data-ttu-id="c02d2-179">Tak</span><span class="sxs-lookup"><span data-stu-id="c02d2-179">Yes</span></span> | <span data-ttu-id="c02d2-180">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="c02d2-180">N/A</span></span> | <span data-ttu-id="c02d2-181">Operacje z następującymi polami nie są obsługiwane: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="c02d2-182">Te interfejsy API można nazwać obiektami encji, które zawierają pola niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="c02d2-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="c02d2-183">Właściwość numeru identyfikacyjnego jest opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="c02d2-183">The ID property is optional.</span></span> <span data-ttu-id="c02d2-184">Jeśli zostanie on podany, system próbuje go użyć i zgłasza wyjątek, jeśli nie może być używany.</span><span class="sxs-lookup"><span data-stu-id="c02d2-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="c02d2-185">Jeśli nie zostanie on dostarczony, system wygeneruje go.</span><span class="sxs-lookup"><span data-stu-id="c02d2-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="c02d2-186">Ograniczenia i znane problemy</span><span class="sxs-lookup"><span data-stu-id="c02d2-186">Limitations and known issues</span></span>
<span data-ttu-id="c02d2-187">Oto lista ograniczeń i znanych problemów:</span><span class="sxs-lookup"><span data-stu-id="c02d2-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="c02d2-188">Interfejsy API planowania mogą być używane tylko przez **Użytkowników z licencją programu Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="c02d2-189">Nie mogą z nich korzystać:</span><span class="sxs-lookup"><span data-stu-id="c02d2-189">They can't be used by:</span></span>
    - <span data-ttu-id="c02d2-190">Użytkownicy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c02d2-190">Application users</span></span>
    - <span data-ttu-id="c02d2-191">Użytkownicy systemowi</span><span class="sxs-lookup"><span data-stu-id="c02d2-191">System users</span></span>
    - <span data-ttu-id="c02d2-192">Użytkownicy integracyjni</span><span class="sxs-lookup"><span data-stu-id="c02d2-192">Integration users</span></span>
    - <span data-ttu-id="c02d2-193">Inni użytkownicy, którzy nie mają wymaganej licencji</span><span class="sxs-lookup"><span data-stu-id="c02d2-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="c02d2-194">Każdy **OperationSet** może mieć maksymalnie 100 operacji.</span><span class="sxs-lookup"><span data-stu-id="c02d2-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="c02d2-195">Każdy użytkownik może mieć otwartych maksymalnie 10 **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="c02d2-196">Project Operations obsługuje obecnie maksymalnie 500 wszystkich zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="c02d2-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="c02d2-197">Obecnie nie są dostępne dzienniki błędów i stanu niepowodzenia **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="c02d2-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="c02d2-198">Harmonogram interfejsów API jest w publicznej wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="c02d2-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="c02d2-199">Używanie tych interfejsów API w środowisku produkcyjnym nie jest obsługiwane przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c02d2-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="c02d2-200">Przykładowy scenariusz</span><span class="sxs-lookup"><span data-stu-id="c02d2-200">Sample scenario</span></span>

<span data-ttu-id="c02d2-201">W tym scenariuszu zostanie utworzyć projekt, członka zespołu, cztery zadania i dwa przypisania zasobów.</span><span class="sxs-lookup"><span data-stu-id="c02d2-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="c02d2-202">Następnie należy zaktualizować jedno zadanie, zaktualizować projekt, usunąć jedno zadanie, usunąć jedno przypisanie zasobów i utworzyć zależność zadania.</span><span class="sxs-lookup"><span data-stu-id="c02d2-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="c02d2-203">Więcej przykładów</span><span class="sxs-lookup"><span data-stu-id="c02d2-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
