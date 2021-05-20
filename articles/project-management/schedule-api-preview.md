---
title: Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania
description: To temat zawiera informacje i przykłady dotyczące korzystania z interfejsów API planowania.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950817"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="72e5e-103">Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania</span><span class="sxs-lookup"><span data-stu-id="72e5e-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="72e5e-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="72e5e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="72e5e-105">Niektóre lub wszystkie funkcje wymienione w tym temacie są dostępne w wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="72e5e-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="72e5e-106">Zawartość i funkcjonalność mogą ulec zmianie.</span><span class="sxs-lookup"><span data-stu-id="72e5e-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="72e5e-107">Encje planowania</span><span class="sxs-lookup"><span data-stu-id="72e5e-107">Scheduling entities</span></span>

<span data-ttu-id="72e5e-108">Harmonogramy API zapewniają możliwość tworzenia, aktualizowania i usuwania operacji z **Encje planowania**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="72e5e-109">Te jednostki są zarządzane za pomocą aparatu planowania w Project dla sieci Web.</span><span class="sxs-lookup"><span data-stu-id="72e5e-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="72e5e-110">We wcześniejszych wersjach Dynamics 365 Project Operations operacje tworzenia, aktualizowania i usuwania **Encji planowania** były ograniczone.</span><span class="sxs-lookup"><span data-stu-id="72e5e-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="72e5e-111">W poniższej tabeli przedstawiono pełną listę **Encje planowania**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="72e5e-112">Nazwa encji</span><span class="sxs-lookup"><span data-stu-id="72e5e-112">Entity name</span></span>  | <span data-ttu-id="72e5e-113">Logiczna nazwa encji</span><span class="sxs-lookup"><span data-stu-id="72e5e-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="72e5e-114">Project</span><span class="sxs-lookup"><span data-stu-id="72e5e-114">Project</span></span> | <span data-ttu-id="72e5e-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="72e5e-115">msdyn_project</span></span> |
| <span data-ttu-id="72e5e-116">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-116">Project Task</span></span>  | <span data-ttu-id="72e5e-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="72e5e-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="72e5e-118">Zależność zadania projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-118">Project Task Dependency</span></span>  | <span data-ttu-id="72e5e-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="72e5e-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="72e5e-120">Przypisanie zasobu</span><span class="sxs-lookup"><span data-stu-id="72e5e-120">Resource Assignment</span></span> | <span data-ttu-id="72e5e-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="72e5e-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="72e5e-122">Zasobnik projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-122">Project Bucket</span></span>  | <span data-ttu-id="72e5e-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="72e5e-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="72e5e-124">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-124">Project Team Member</span></span> | <span data-ttu-id="72e5e-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="72e5e-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="72e5e-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="72e5e-126">OperationSet</span></span>

<span data-ttu-id="72e5e-127">OperationSet to wzorzec jednostki pracy, którego można użyć, gdy w ramach transakcji musi zostać przetworzonych kilka żądań mających wpływ na harmonogram.</span><span class="sxs-lookup"><span data-stu-id="72e5e-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="72e5e-128">Planowanie interfejsów API</span><span class="sxs-lookup"><span data-stu-id="72e5e-128">Schedule APIs</span></span>

<span data-ttu-id="72e5e-129">Poniżej przedstawiono listę bieżących interfejsów API planowania.</span><span class="sxs-lookup"><span data-stu-id="72e5e-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="72e5e-130">**msdyn_CreateProjectV1**: tego interfejsu API można używać do tworzenia projektu.</span><span class="sxs-lookup"><span data-stu-id="72e5e-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="72e5e-131">Projekt i domyślny rozmiar projektu są tworzone natychmiast.</span><span class="sxs-lookup"><span data-stu-id="72e5e-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="72e5e-132">**msdyn_CreateTeamMemberV1**: tego interfejsu API można używać do tworzenia członka zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="72e5e-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="72e5e-133">Rekord członka zespołu jest tworzony natychmiast.</span><span class="sxs-lookup"><span data-stu-id="72e5e-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="72e5e-134">**msdyn_CreateOperationSetV1**: ten interfejs API może być używany do planowania kilku żądań, które muszą zostać wykonane w ramach transakcji.</span><span class="sxs-lookup"><span data-stu-id="72e5e-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="72e5e-135">**msdyn_PSSCreateV1**: tego interfejsu API można używać do tworzenia encji.</span><span class="sxs-lookup"><span data-stu-id="72e5e-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="72e5e-136">Może to być dowolny z obiektów planowania obsługujący operację tworzenia.</span><span class="sxs-lookup"><span data-stu-id="72e5e-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="72e5e-137">**msdyn_PSSUpdateV1**: tego interfejsu API można używać do aktualizacji encji.</span><span class="sxs-lookup"><span data-stu-id="72e5e-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="72e5e-138">Może to być dowolny z obiektów planowania obsługujący operację aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="72e5e-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="72e5e-139">**msdyn_PSSDeleteV1**: tego interfejsu API można używać do usuwania encji.</span><span class="sxs-lookup"><span data-stu-id="72e5e-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="72e5e-140">Może to być dowolny z obiektów planowania obsługujący operację usuwania.</span><span class="sxs-lookup"><span data-stu-id="72e5e-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="72e5e-141">**msdyn_ExecuteOperationSetV1**: ten interfejs API jest używany do wykonywania wszystkich operacji w ramach danego zestawu operacji.</span><span class="sxs-lookup"><span data-stu-id="72e5e-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="72e5e-142">Używanie interfejsów API harmonogramu z zestawem OperationSet</span><span class="sxs-lookup"><span data-stu-id="72e5e-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="72e5e-143">Ponieważ rekordy z zarówno **CreateProjectV1**, jak i **CreateTeamMemberV1** są tworzone natychmiast, tych interfejsów API nie można używać bezpośrednio w przy użyciu zestawu **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="72e5e-144">Interfejs API umożliwia jednak tworzenie potrzebnych rekordów, tworzenie zestawu **OperationSet**, a następnie używanie tych wstępnie utworzonych rekordów w zestawie **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="72e5e-145">Obsługiwane operacje</span><span class="sxs-lookup"><span data-stu-id="72e5e-145">Supported operations</span></span>

| <span data-ttu-id="72e5e-146">Encja planowania</span><span class="sxs-lookup"><span data-stu-id="72e5e-146">Scheduling entity</span></span> | <span data-ttu-id="72e5e-147">Utworzenie</span><span class="sxs-lookup"><span data-stu-id="72e5e-147">Create</span></span> | <span data-ttu-id="72e5e-148">Zaktualizuj</span><span class="sxs-lookup"><span data-stu-id="72e5e-148">Update</span></span> | <span data-ttu-id="72e5e-149">Delete</span><span class="sxs-lookup"><span data-stu-id="72e5e-149">Delete</span></span> | <span data-ttu-id="72e5e-150">Ważne uwagi</span><span class="sxs-lookup"><span data-stu-id="72e5e-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="72e5e-151">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-151">Project task</span></span> | <span data-ttu-id="72e5e-152">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-152">Yes</span></span> | <span data-ttu-id="72e5e-153">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-153">Yes</span></span> | <span data-ttu-id="72e5e-154">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-154">Yes</span></span> | <span data-ttu-id="72e5e-155">Brak</span><span class="sxs-lookup"><span data-stu-id="72e5e-155">None</span></span> |
| <span data-ttu-id="72e5e-156">Zależność zadania projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-156">Project task dependency</span></span> | <span data-ttu-id="72e5e-157">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-157">Yes</span></span> | <span data-ttu-id="72e5e-158">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-158">Yes</span></span> | | <span data-ttu-id="72e5e-159">Rekordy zależności zadań projektu nie są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="72e5e-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="72e5e-160">Zamiast tego można usunąć stary rekord i utworzyć nowy rekord.</span><span class="sxs-lookup"><span data-stu-id="72e5e-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="72e5e-161">Przypisanie zasobu</span><span class="sxs-lookup"><span data-stu-id="72e5e-161">Resource assignment</span></span> | <span data-ttu-id="72e5e-162">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-162">Yes</span></span> | <span data-ttu-id="72e5e-163">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-163">Yes</span></span> | | <span data-ttu-id="72e5e-164">Operacje z następującymi polami nie są obsługiwane: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="72e5e-165">Rekordy przypisania zasobów nie są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="72e5e-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="72e5e-166">Zamiast tego można usunąć stary rekord i utworzyć nowy rekord.</span><span class="sxs-lookup"><span data-stu-id="72e5e-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="72e5e-167">Zasobnik projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-167">Project bucket</span></span> | <span data-ttu-id="72e5e-168">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="72e5e-168">N/A</span></span> | <span data-ttu-id="72e5e-169">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="72e5e-169">N/A</span></span> | <span data-ttu-id="72e5e-170">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="72e5e-170">N/A</span></span> | <span data-ttu-id="72e5e-171">Domyślny domyślny rozmiar jest tworzony przy użyciu interfejsu **API CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="72e5e-172">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-172">Project team member</span></span> | <span data-ttu-id="72e5e-173">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-173">Yes</span></span> | <span data-ttu-id="72e5e-174">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-174">Yes</span></span> | <span data-ttu-id="72e5e-175">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-175">Yes</span></span> | <span data-ttu-id="72e5e-176">Aby utworzyć operację tworzenia, użyj interfejsu API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="72e5e-177">Project</span><span class="sxs-lookup"><span data-stu-id="72e5e-177">Project</span></span> | <span data-ttu-id="72e5e-178">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-178">Yes</span></span> | <span data-ttu-id="72e5e-179">Tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-179">Yes</span></span> | <span data-ttu-id="72e5e-180">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="72e5e-180">N/A</span></span> | <span data-ttu-id="72e5e-181">Operacje z następującymi polami nie są obsługiwane: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="72e5e-182">Te interfejsy API można nazwać obiektami encji, które zawierają pola niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="72e5e-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="72e5e-183">Właściwość numeru identyfikacyjnego jest opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="72e5e-183">The ID property is optional.</span></span> <span data-ttu-id="72e5e-184">Jeśli zostanie on podany, system próbuje go użyć i zgłasza wyjątek, jeśli nie może być używany.</span><span class="sxs-lookup"><span data-stu-id="72e5e-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="72e5e-185">Jeśli nie zostanie on dostarczony, system wygeneruje go.</span><span class="sxs-lookup"><span data-stu-id="72e5e-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="72e5e-186">Pola ograniczone</span><span class="sxs-lookup"><span data-stu-id="72e5e-186">Restricted fields</span></span>

<span data-ttu-id="72e5e-187">W poniższych tabelach przedstawiono pola, których nie można **tworzyć** i **edytować**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="72e5e-188">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-188">Project task</span></span>

| <span data-ttu-id="72e5e-189">**Nazwa logiczna**</span><span class="sxs-lookup"><span data-stu-id="72e5e-189">**Logical name**</span></span>                       | <span data-ttu-id="72e5e-190">**Można tworzyć**</span><span class="sxs-lookup"><span data-stu-id="72e5e-190">**Can create**</span></span> | <span data-ttu-id="72e5e-191">**Może edytować**</span><span class="sxs-lookup"><span data-stu-id="72e5e-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="72e5e-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="72e5e-193">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-193">no</span></span>             | <span data-ttu-id="72e5e-194">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-194">no</span></span>               |
| <span data-ttu-id="72e5e-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="72e5e-196">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-196">no</span></span>             | <span data-ttu-id="72e5e-197">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-197">no</span></span>               |
| <span data-ttu-id="72e5e-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="72e5e-198">msdyn_actualend</span></span>                        | <span data-ttu-id="72e5e-199">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-199">no</span></span>             | <span data-ttu-id="72e5e-200">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-200">no</span></span>               |
| <span data-ttu-id="72e5e-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="72e5e-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="72e5e-202">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-202">no</span></span>             | <span data-ttu-id="72e5e-203">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-203">no</span></span>               |
| <span data-ttu-id="72e5e-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="72e5e-205">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-205">no</span></span>             | <span data-ttu-id="72e5e-206">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-206">no</span></span>               |
| <span data-ttu-id="72e5e-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="72e5e-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="72e5e-208">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-208">no</span></span>             | <span data-ttu-id="72e5e-209">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-209">no</span></span>               |
| <span data-ttu-id="72e5e-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="72e5e-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="72e5e-211">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-211">no</span></span>             | <span data-ttu-id="72e5e-212">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-212">no</span></span>               |
| <span data-ttu-id="72e5e-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="72e5e-214">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-214">no</span></span>             | <span data-ttu-id="72e5e-215">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-215">no</span></span>               |
| <span data-ttu-id="72e5e-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="72e5e-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="72e5e-217">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-217">no</span></span>             | <span data-ttu-id="72e5e-218">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-218">no</span></span>               |
| <span data-ttu-id="72e5e-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="72e5e-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="72e5e-220">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-220">no</span></span>             | <span data-ttu-id="72e5e-221">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-221">no</span></span>               |
| <span data-ttu-id="72e5e-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="72e5e-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="72e5e-223">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-223">no</span></span>             | <span data-ttu-id="72e5e-224">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-224">no</span></span>               |
| <span data-ttu-id="72e5e-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="72e5e-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="72e5e-226">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-226">no</span></span>             | <span data-ttu-id="72e5e-227">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-227">no</span></span>               |
| <span data-ttu-id="72e5e-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="72e5e-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="72e5e-229">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-229">no</span></span>             | <span data-ttu-id="72e5e-230">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-230">no</span></span>               |
| <span data-ttu-id="72e5e-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="72e5e-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="72e5e-232">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-232">no</span></span>             | <span data-ttu-id="72e5e-233">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-233">no</span></span>               |
| <span data-ttu-id="72e5e-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="72e5e-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="72e5e-235">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-235">no</span></span>             | <span data-ttu-id="72e5e-236">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-236">no</span></span>               |
| <span data-ttu-id="72e5e-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="72e5e-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="72e5e-238">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-238">no</span></span>             | <span data-ttu-id="72e5e-239">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-239">no</span></span>               |
| <span data-ttu-id="72e5e-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="72e5e-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="72e5e-241">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-241">no</span></span>             | <span data-ttu-id="72e5e-242">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-242">no</span></span>               |
| <span data-ttu-id="72e5e-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="72e5e-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="72e5e-244">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-244">no</span></span>             | <span data-ttu-id="72e5e-245">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-245">no</span></span>               |
| <span data-ttu-id="72e5e-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="72e5e-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="72e5e-247">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-247">no</span></span>             | <span data-ttu-id="72e5e-248">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-248">no</span></span>               |
| <span data-ttu-id="72e5e-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="72e5e-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="72e5e-250">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-250">no</span></span>             | <span data-ttu-id="72e5e-251">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-251">no</span></span>               |
| <span data-ttu-id="72e5e-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="72e5e-253">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-253">no</span></span>             | <span data-ttu-id="72e5e-254">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-254">no</span></span>               |
| <span data-ttu-id="72e5e-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="72e5e-256">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-256">no</span></span>             | <span data-ttu-id="72e5e-257">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-257">no</span></span>               |
| <span data-ttu-id="72e5e-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="72e5e-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="72e5e-259">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-259">no</span></span>             | <span data-ttu-id="72e5e-260">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-260">no</span></span>               |
| <span data-ttu-id="72e5e-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="72e5e-262">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-262">no</span></span>             | <span data-ttu-id="72e5e-263">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-263">no</span></span>               |
| <span data-ttu-id="72e5e-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="72e5e-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="72e5e-265">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-265">no</span></span>             | <span data-ttu-id="72e5e-266">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-266">no</span></span>               |
| <span data-ttu-id="72e5e-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="72e5e-267">msdyn_progress</span></span>                         | <span data-ttu-id="72e5e-268">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-268">no</span></span>             | <span data-ttu-id="72e5e-269">nie (tak dla P4W)</span><span class="sxs-lookup"><span data-stu-id="72e5e-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="72e5e-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="72e5e-271">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-271">no</span></span>             | <span data-ttu-id="72e5e-272">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-272">no</span></span>               |
| <span data-ttu-id="72e5e-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="72e5e-274">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-274">no</span></span>             | <span data-ttu-id="72e5e-275">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-275">no</span></span>               |
| <span data-ttu-id="72e5e-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="72e5e-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="72e5e-277">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-277">no</span></span>             | <span data-ttu-id="72e5e-278">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-278">no</span></span>               |
| <span data-ttu-id="72e5e-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="72e5e-280">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-280">no</span></span>             | <span data-ttu-id="72e5e-281">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-281">no</span></span>               |
| <span data-ttu-id="72e5e-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="72e5e-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="72e5e-283">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-283">no</span></span>             | <span data-ttu-id="72e5e-284">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-284">no</span></span>               |
| <span data-ttu-id="72e5e-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="72e5e-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="72e5e-286">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-286">no</span></span>             | <span data-ttu-id="72e5e-287">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-287">no</span></span>               |
| <span data-ttu-id="72e5e-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="72e5e-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="72e5e-289">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-289">no</span></span>             | <span data-ttu-id="72e5e-290">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-290">no</span></span>               |
| <span data-ttu-id="72e5e-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="72e5e-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="72e5e-292">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-292">no</span></span>             | <span data-ttu-id="72e5e-293">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-293">no</span></span>               |
| <span data-ttu-id="72e5e-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="72e5e-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="72e5e-295">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-295">no</span></span>             | <span data-ttu-id="72e5e-296">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-296">no</span></span>               |
| <span data-ttu-id="72e5e-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="72e5e-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="72e5e-298">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-298">no</span></span>             | <span data-ttu-id="72e5e-299">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-299">no</span></span>               |
| <span data-ttu-id="72e5e-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="72e5e-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="72e5e-301">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-301">no</span></span>             | <span data-ttu-id="72e5e-302">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-302">no</span></span>               |
| <span data-ttu-id="72e5e-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="72e5e-304">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-304">no</span></span>             | <span data-ttu-id="72e5e-305">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-305">no</span></span>               |
| <span data-ttu-id="72e5e-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="72e5e-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="72e5e-307">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-307">no</span></span>             | <span data-ttu-id="72e5e-308">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-308">no</span></span>               |
| <span data-ttu-id="72e5e-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="72e5e-310">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-310">no</span></span>             | <span data-ttu-id="72e5e-311">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-311">no</span></span>               |
| <span data-ttu-id="72e5e-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="72e5e-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="72e5e-313">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-313">no</span></span>             | <span data-ttu-id="72e5e-314">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-314">no</span></span>               |
| <span data-ttu-id="72e5e-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="72e5e-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="72e5e-316">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-316">no</span></span>             | <span data-ttu-id="72e5e-317">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-317">no</span></span>               |
| <span data-ttu-id="72e5e-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="72e5e-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="72e5e-319">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-319">no</span></span>             | <span data-ttu-id="72e5e-320">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-320">no</span></span>               |
| <span data-ttu-id="72e5e-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="72e5e-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="72e5e-322">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-322">no</span></span>             | <span data-ttu-id="72e5e-323">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-323">no</span></span>               |
| <span data-ttu-id="72e5e-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="72e5e-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="72e5e-325">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-325">no</span></span>             | <span data-ttu-id="72e5e-326">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-326">no</span></span>               |
| <span data-ttu-id="72e5e-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="72e5e-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="72e5e-328">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-328">no</span></span>             | <span data-ttu-id="72e5e-329">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-329">no</span></span>               |
| <span data-ttu-id="72e5e-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="72e5e-330">msdyn_summary</span></span>                          | <span data-ttu-id="72e5e-331">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-331">no</span></span>             | <span data-ttu-id="72e5e-332">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-332">no</span></span>               |
| <span data-ttu-id="72e5e-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="72e5e-334">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-334">no</span></span>             | <span data-ttu-id="72e5e-335">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-335">no</span></span>               |
| <span data-ttu-id="72e5e-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="72e5e-337">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-337">no</span></span>             | <span data-ttu-id="72e5e-338">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="72e5e-339">Zależność zadania projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-339">Project task dependency</span></span>

| <span data-ttu-id="72e5e-340">**Nazwa logiczna**</span><span class="sxs-lookup"><span data-stu-id="72e5e-340">**Logical name**</span></span>              | <span data-ttu-id="72e5e-341">**Można tworzyć**</span><span class="sxs-lookup"><span data-stu-id="72e5e-341">**Can create**</span></span> | <span data-ttu-id="72e5e-342">**Może edytować**</span><span class="sxs-lookup"><span data-stu-id="72e5e-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="72e5e-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="72e5e-343">msdyn_linktype</span></span>                | <span data-ttu-id="72e5e-344">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-344">no</span></span>             | <span data-ttu-id="72e5e-345">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-345">no</span></span>           |
| <span data-ttu-id="72e5e-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="72e5e-346">msdyn_linktypename</span></span>            | <span data-ttu-id="72e5e-347">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-347">no</span></span>             | <span data-ttu-id="72e5e-348">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-348">no</span></span>           |
| <span data-ttu-id="72e5e-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="72e5e-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="72e5e-350">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-350">yes</span></span>            | <span data-ttu-id="72e5e-351">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-351">no</span></span>           |
| <span data-ttu-id="72e5e-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="72e5e-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="72e5e-353">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-353">yes</span></span>            | <span data-ttu-id="72e5e-354">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-354">no</span></span>           |
| <span data-ttu-id="72e5e-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="72e5e-355">msdyn_project</span></span>                 | <span data-ttu-id="72e5e-356">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-356">yes</span></span>            | <span data-ttu-id="72e5e-357">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-357">no</span></span>           |
| <span data-ttu-id="72e5e-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="72e5e-358">msdyn_projectname</span></span>             | <span data-ttu-id="72e5e-359">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-359">yes</span></span>            | <span data-ttu-id="72e5e-360">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-360">no</span></span>           |
| <span data-ttu-id="72e5e-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="72e5e-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="72e5e-362">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-362">yes</span></span>            | <span data-ttu-id="72e5e-363">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-363">no</span></span>           |
| <span data-ttu-id="72e5e-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="72e5e-364">msdyn_successortask</span></span>           | <span data-ttu-id="72e5e-365">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-365">yes</span></span>            | <span data-ttu-id="72e5e-366">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-366">no</span></span>           |
| <span data-ttu-id="72e5e-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="72e5e-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="72e5e-368">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-368">yes</span></span>            | <span data-ttu-id="72e5e-369">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="72e5e-370">Przypisanie zasobu</span><span class="sxs-lookup"><span data-stu-id="72e5e-370">Resource assignment</span></span>

| <span data-ttu-id="72e5e-371">**Nazwa logiczna**</span><span class="sxs-lookup"><span data-stu-id="72e5e-371">**Logical name**</span></span>             | <span data-ttu-id="72e5e-372">**Można tworzyć**</span><span class="sxs-lookup"><span data-stu-id="72e5e-372">**Can create**</span></span> | <span data-ttu-id="72e5e-373">**Może edytować**</span><span class="sxs-lookup"><span data-stu-id="72e5e-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="72e5e-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="72e5e-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="72e5e-375">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-375">yes</span></span>            | <span data-ttu-id="72e5e-376">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-376">no</span></span>           |
| <span data-ttu-id="72e5e-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="72e5e-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="72e5e-378">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-378">yes</span></span>            | <span data-ttu-id="72e5e-379">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-379">no</span></span>           |
| <span data-ttu-id="72e5e-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="72e5e-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="72e5e-381">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-381">no</span></span>             | <span data-ttu-id="72e5e-382">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-382">no</span></span>           |
| <span data-ttu-id="72e5e-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="72e5e-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="72e5e-384">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-384">no</span></span>             | <span data-ttu-id="72e5e-385">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-385">no</span></span>           |
| <span data-ttu-id="72e5e-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="72e5e-386">msdyn_committype</span></span>             | <span data-ttu-id="72e5e-387">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-387">no</span></span>             | <span data-ttu-id="72e5e-388">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-388">no</span></span>           |
| <span data-ttu-id="72e5e-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="72e5e-389">msdyn_committypename</span></span>         | <span data-ttu-id="72e5e-390">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-390">no</span></span>             | <span data-ttu-id="72e5e-391">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-391">no</span></span>           |
| <span data-ttu-id="72e5e-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="72e5e-392">msdyn_effort</span></span>                 | <span data-ttu-id="72e5e-393">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-393">no</span></span>             | <span data-ttu-id="72e5e-394">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-394">no</span></span>           |
| <span data-ttu-id="72e5e-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="72e5e-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="72e5e-396">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-396">no</span></span>             | <span data-ttu-id="72e5e-397">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-397">no</span></span>           |
| <span data-ttu-id="72e5e-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="72e5e-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="72e5e-399">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-399">no</span></span>             | <span data-ttu-id="72e5e-400">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-400">no</span></span>           |
| <span data-ttu-id="72e5e-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="72e5e-401">msdyn_finish</span></span>                 | <span data-ttu-id="72e5e-402">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-402">no</span></span>             | <span data-ttu-id="72e5e-403">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-403">no</span></span>           |
| <span data-ttu-id="72e5e-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="72e5e-405">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-405">no</span></span>             | <span data-ttu-id="72e5e-406">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-406">no</span></span>           |
| <span data-ttu-id="72e5e-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="72e5e-408">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-408">no</span></span>             | <span data-ttu-id="72e5e-409">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-409">no</span></span>           |
| <span data-ttu-id="72e5e-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="72e5e-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="72e5e-411">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-411">no</span></span>             | <span data-ttu-id="72e5e-412">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-412">no</span></span>           |
| <span data-ttu-id="72e5e-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="72e5e-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="72e5e-414">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-414">no</span></span>             | <span data-ttu-id="72e5e-415">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-415">no</span></span>           |
| <span data-ttu-id="72e5e-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="72e5e-417">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-417">no</span></span>             | <span data-ttu-id="72e5e-418">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-418">no</span></span>           |
| <span data-ttu-id="72e5e-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="72e5e-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="72e5e-420">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-420">no</span></span>             | <span data-ttu-id="72e5e-421">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-421">no</span></span>           |
| <span data-ttu-id="72e5e-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="72e5e-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="72e5e-423">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-423">no</span></span>             | <span data-ttu-id="72e5e-424">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-424">no</span></span>           |
| <span data-ttu-id="72e5e-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="72e5e-425">msdyn_projectid</span></span>              | <span data-ttu-id="72e5e-426">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-426">yes</span></span>            | <span data-ttu-id="72e5e-427">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-427">no</span></span>           |
| <span data-ttu-id="72e5e-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="72e5e-428">msdyn_projectidname</span></span>          | <span data-ttu-id="72e5e-429">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-429">no</span></span>             | <span data-ttu-id="72e5e-430">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-430">no</span></span>           |
| <span data-ttu-id="72e5e-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="72e5e-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="72e5e-432">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-432">no</span></span>             | <span data-ttu-id="72e5e-433">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-433">no</span></span>           |
| <span data-ttu-id="72e5e-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="72e5e-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="72e5e-435">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-435">no</span></span>             | <span data-ttu-id="72e5e-436">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-436">no</span></span>           |
| <span data-ttu-id="72e5e-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="72e5e-437">msdyn_start</span></span>                  | <span data-ttu-id="72e5e-438">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-438">no</span></span>             | <span data-ttu-id="72e5e-439">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-439">no</span></span>           |
| <span data-ttu-id="72e5e-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="72e5e-440">msdyn_taskid</span></span>                 | <span data-ttu-id="72e5e-441">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-441">no</span></span>             | <span data-ttu-id="72e5e-442">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-442">no</span></span>           |
| <span data-ttu-id="72e5e-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="72e5e-443">msdyn_taskidname</span></span>             | <span data-ttu-id="72e5e-444">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-444">no</span></span>             | <span data-ttu-id="72e5e-445">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-445">no</span></span>           |
| <span data-ttu-id="72e5e-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="72e5e-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="72e5e-447">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-447">no</span></span>             | <span data-ttu-id="72e5e-448">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="72e5e-449">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="72e5e-449">Project team member</span></span>

| <span data-ttu-id="72e5e-450">**Nazwa logiczna**</span><span class="sxs-lookup"><span data-stu-id="72e5e-450">**Logical name**</span></span>                                 | <span data-ttu-id="72e5e-451">**Można tworzyć**</span><span class="sxs-lookup"><span data-stu-id="72e5e-451">**Can create**</span></span> | <span data-ttu-id="72e5e-452">**Może edytować**</span><span class="sxs-lookup"><span data-stu-id="72e5e-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="72e5e-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="72e5e-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="72e5e-454">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-454">no</span></span>             | <span data-ttu-id="72e5e-455">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-455">no</span></span>           |
| <span data-ttu-id="72e5e-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="72e5e-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="72e5e-457">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-457">no</span></span>             | <span data-ttu-id="72e5e-458">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-458">no</span></span>           |
| <span data-ttu-id="72e5e-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="72e5e-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="72e5e-460">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-460">no</span></span>             | <span data-ttu-id="72e5e-461">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-461">no</span></span>           |
| <span data-ttu-id="72e5e-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="72e5e-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="72e5e-463">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-463">no</span></span>             | <span data-ttu-id="72e5e-464">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-464">no</span></span>           |
| <span data-ttu-id="72e5e-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="72e5e-465">msdyn_effort</span></span>                                     | <span data-ttu-id="72e5e-466">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-466">no</span></span>             | <span data-ttu-id="72e5e-467">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-467">no</span></span>           |
| <span data-ttu-id="72e5e-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="72e5e-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="72e5e-469">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-469">no</span></span>             | <span data-ttu-id="72e5e-470">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-470">no</span></span>           |
| <span data-ttu-id="72e5e-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="72e5e-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="72e5e-472">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-472">no</span></span>             | <span data-ttu-id="72e5e-473">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-473">no</span></span>           |
| <span data-ttu-id="72e5e-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="72e5e-474">msdyn_finish</span></span>                                     | <span data-ttu-id="72e5e-475">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-475">no</span></span>             | <span data-ttu-id="72e5e-476">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-476">no</span></span>           |
| <span data-ttu-id="72e5e-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="72e5e-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="72e5e-478">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-478">no</span></span>             | <span data-ttu-id="72e5e-479">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-479">no</span></span>           |
| <span data-ttu-id="72e5e-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="72e5e-480">msdyn_hours</span></span>                                      | <span data-ttu-id="72e5e-481">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-481">no</span></span>             | <span data-ttu-id="72e5e-482">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-482">no</span></span>           |
| <span data-ttu-id="72e5e-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="72e5e-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="72e5e-484">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-484">no</span></span>             | <span data-ttu-id="72e5e-485">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-485">no</span></span>           |
| <span data-ttu-id="72e5e-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="72e5e-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="72e5e-487">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-487">no</span></span>             | <span data-ttu-id="72e5e-488">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-488">no</span></span>           |
| <span data-ttu-id="72e5e-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="72e5e-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="72e5e-490">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-490">no</span></span>             | <span data-ttu-id="72e5e-491">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-491">no</span></span>           |
| <span data-ttu-id="72e5e-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="72e5e-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="72e5e-493">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-493">no</span></span>             | <span data-ttu-id="72e5e-494">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-494">no</span></span>           |
| <span data-ttu-id="72e5e-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="72e5e-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="72e5e-496">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-496">no</span></span>             | <span data-ttu-id="72e5e-497">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-497">no</span></span>           |
| <span data-ttu-id="72e5e-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="72e5e-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="72e5e-499">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-499">no</span></span>             | <span data-ttu-id="72e5e-500">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-500">no</span></span>           |
| <span data-ttu-id="72e5e-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="72e5e-501">msdyn_start</span></span>                                      | <span data-ttu-id="72e5e-502">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-502">no</span></span>             | <span data-ttu-id="72e5e-503">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="72e5e-504">Project</span><span class="sxs-lookup"><span data-stu-id="72e5e-504">Project</span></span>

| <span data-ttu-id="72e5e-505">**Nazwa logiczna**</span><span class="sxs-lookup"><span data-stu-id="72e5e-505">**Logical name**</span></span>                       | <span data-ttu-id="72e5e-506">**Można tworzyć**</span><span class="sxs-lookup"><span data-stu-id="72e5e-506">**Can create**</span></span> | <span data-ttu-id="72e5e-507">**Może edytować**</span><span class="sxs-lookup"><span data-stu-id="72e5e-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="72e5e-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="72e5e-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="72e5e-509">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-509">no</span></span>             | <span data-ttu-id="72e5e-510">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-510">no</span></span>           |
| <span data-ttu-id="72e5e-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="72e5e-512">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-512">no</span></span>             | <span data-ttu-id="72e5e-513">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-513">no</span></span>           |
| <span data-ttu-id="72e5e-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="72e5e-515">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-515">no</span></span>             | <span data-ttu-id="72e5e-516">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-516">no</span></span>           |
| <span data-ttu-id="72e5e-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="72e5e-518">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-518">no</span></span>             | <span data-ttu-id="72e5e-519">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-519">no</span></span>           |
| <span data-ttu-id="72e5e-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="72e5e-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="72e5e-521">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-521">no</span></span>             | <span data-ttu-id="72e5e-522">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-522">no</span></span>           |
| <span data-ttu-id="72e5e-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="72e5e-524">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-524">no</span></span>             | <span data-ttu-id="72e5e-525">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-525">no</span></span>           |
| <span data-ttu-id="72e5e-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="72e5e-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="72e5e-527">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-527">yes</span></span>            | <span data-ttu-id="72e5e-528">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-528">no</span></span>           |
| <span data-ttu-id="72e5e-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="72e5e-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="72e5e-530">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-530">yes</span></span>            | <span data-ttu-id="72e5e-531">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-531">no</span></span>           |
| <span data-ttu-id="72e5e-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="72e5e-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="72e5e-533">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-533">yes</span></span>            | <span data-ttu-id="72e5e-534">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-534">no</span></span>           |
| <span data-ttu-id="72e5e-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="72e5e-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="72e5e-536">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-536">no</span></span>             | <span data-ttu-id="72e5e-537">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-537">no</span></span>           |
| <span data-ttu-id="72e5e-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="72e5e-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="72e5e-539">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-539">no</span></span>             | <span data-ttu-id="72e5e-540">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-540">no</span></span>           |
| <span data-ttu-id="72e5e-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="72e5e-542">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-542">no</span></span>             | <span data-ttu-id="72e5e-543">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-543">no</span></span>           |
| <span data-ttu-id="72e5e-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="72e5e-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="72e5e-545">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-545">no</span></span>             | <span data-ttu-id="72e5e-546">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-546">no</span></span>           |
| <span data-ttu-id="72e5e-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="72e5e-548">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-548">no</span></span>             | <span data-ttu-id="72e5e-549">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-549">no</span></span>           |
| <span data-ttu-id="72e5e-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="72e5e-550">msdyn_duration</span></span>                         | <span data-ttu-id="72e5e-551">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-551">no</span></span>             | <span data-ttu-id="72e5e-552">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-552">no</span></span>           |
| <span data-ttu-id="72e5e-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="72e5e-553">msdyn_effort</span></span>                           | <span data-ttu-id="72e5e-554">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-554">no</span></span>             | <span data-ttu-id="72e5e-555">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-555">no</span></span>           |
| <span data-ttu-id="72e5e-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="72e5e-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="72e5e-557">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-557">no</span></span>             | <span data-ttu-id="72e5e-558">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-558">no</span></span>           |
| <span data-ttu-id="72e5e-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="72e5e-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="72e5e-560">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-560">no</span></span>             | <span data-ttu-id="72e5e-561">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-561">no</span></span>           |
| <span data-ttu-id="72e5e-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="72e5e-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="72e5e-563">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-563">no</span></span>             | <span data-ttu-id="72e5e-564">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-564">no</span></span>           |
| <span data-ttu-id="72e5e-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="72e5e-565">msdyn_finish</span></span>                           | <span data-ttu-id="72e5e-566">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-566">yes</span></span>            | <span data-ttu-id="72e5e-567">tak</span><span class="sxs-lookup"><span data-stu-id="72e5e-567">yes</span></span>          |
| <span data-ttu-id="72e5e-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="72e5e-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="72e5e-569">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-569">no</span></span>             | <span data-ttu-id="72e5e-570">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-570">no</span></span>           |
| <span data-ttu-id="72e5e-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="72e5e-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="72e5e-572">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-572">no</span></span>             | <span data-ttu-id="72e5e-573">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-573">no</span></span>           |
| <span data-ttu-id="72e5e-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="72e5e-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="72e5e-575">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-575">no</span></span>             | <span data-ttu-id="72e5e-576">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-576">no</span></span>           |
| <span data-ttu-id="72e5e-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="72e5e-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="72e5e-578">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-578">no</span></span>             | <span data-ttu-id="72e5e-579">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-579">no</span></span>           |
| <span data-ttu-id="72e5e-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="72e5e-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="72e5e-581">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-581">no</span></span>             | <span data-ttu-id="72e5e-582">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-582">no</span></span>           |
| <span data-ttu-id="72e5e-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="72e5e-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="72e5e-584">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-584">no</span></span>             | <span data-ttu-id="72e5e-585">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-585">no</span></span>           |
| <span data-ttu-id="72e5e-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="72e5e-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="72e5e-587">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-587">no</span></span>             | <span data-ttu-id="72e5e-588">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-588">no</span></span>           |
| <span data-ttu-id="72e5e-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="72e5e-590">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-590">no</span></span>             | <span data-ttu-id="72e5e-591">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-591">no</span></span>           |
| <span data-ttu-id="72e5e-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="72e5e-593">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-593">no</span></span>             | <span data-ttu-id="72e5e-594">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-594">no</span></span>           |
| <span data-ttu-id="72e5e-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="72e5e-596">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-596">no</span></span>             | <span data-ttu-id="72e5e-597">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-597">no</span></span>           |
| <span data-ttu-id="72e5e-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="72e5e-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="72e5e-599">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-599">no</span></span>             | <span data-ttu-id="72e5e-600">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-600">no</span></span>           |
| <span data-ttu-id="72e5e-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="72e5e-602">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-602">no</span></span>             | <span data-ttu-id="72e5e-603">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-603">no</span></span>           |
| <span data-ttu-id="72e5e-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="72e5e-604">msdyn_progress</span></span>                         | <span data-ttu-id="72e5e-605">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-605">no</span></span>             | <span data-ttu-id="72e5e-606">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-606">no</span></span>           |
| <span data-ttu-id="72e5e-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="72e5e-608">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-608">no</span></span>             | <span data-ttu-id="72e5e-609">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-609">no</span></span>           |
| <span data-ttu-id="72e5e-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="72e5e-611">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-611">no</span></span>             | <span data-ttu-id="72e5e-612">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-612">no</span></span>           |
| <span data-ttu-id="72e5e-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="72e5e-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="72e5e-614">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-614">no</span></span>             | <span data-ttu-id="72e5e-615">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-615">no</span></span>           |
| <span data-ttu-id="72e5e-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="72e5e-617">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-617">no</span></span>             | <span data-ttu-id="72e5e-618">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-618">no</span></span>           |
| <span data-ttu-id="72e5e-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="72e5e-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="72e5e-620">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-620">no</span></span>             | <span data-ttu-id="72e5e-621">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-621">no</span></span>           |
| <span data-ttu-id="72e5e-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="72e5e-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="72e5e-623">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-623">no</span></span>             | <span data-ttu-id="72e5e-624">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-624">no</span></span>           |
| <span data-ttu-id="72e5e-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="72e5e-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="72e5e-626">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-626">no</span></span>             | <span data-ttu-id="72e5e-627">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-627">no</span></span>           |
| <span data-ttu-id="72e5e-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="72e5e-629">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-629">no</span></span>             | <span data-ttu-id="72e5e-630">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-630">no</span></span>           |
| <span data-ttu-id="72e5e-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="72e5e-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="72e5e-632">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-632">no</span></span>             | <span data-ttu-id="72e5e-633">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-633">no</span></span>           |
| <span data-ttu-id="72e5e-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="72e5e-635">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-635">no</span></span>             | <span data-ttu-id="72e5e-636">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-636">no</span></span>           |
| <span data-ttu-id="72e5e-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="72e5e-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="72e5e-638">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-638">no</span></span>             | <span data-ttu-id="72e5e-639">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-639">no</span></span>           |
| <span data-ttu-id="72e5e-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="72e5e-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="72e5e-641">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-641">no</span></span>             | <span data-ttu-id="72e5e-642">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-642">no</span></span>           |
| <span data-ttu-id="72e5e-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="72e5e-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="72e5e-644">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-644">no</span></span>             | <span data-ttu-id="72e5e-645">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-645">no</span></span>           |
| <span data-ttu-id="72e5e-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="72e5e-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="72e5e-647">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-647">no</span></span>             | <span data-ttu-id="72e5e-648">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-648">no</span></span>           |
| <span data-ttu-id="72e5e-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="72e5e-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="72e5e-650">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-650">no</span></span>             | <span data-ttu-id="72e5e-651">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-651">no</span></span>           |
| <span data-ttu-id="72e5e-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="72e5e-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="72e5e-653">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-653">no</span></span>             | <span data-ttu-id="72e5e-654">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-654">no</span></span>           |
| <span data-ttu-id="72e5e-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="72e5e-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="72e5e-656">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-656">no</span></span>             | <span data-ttu-id="72e5e-657">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-657">no</span></span>           |
| <span data-ttu-id="72e5e-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="72e5e-659">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-659">no</span></span>             | <span data-ttu-id="72e5e-660">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-660">no</span></span>           |
| <span data-ttu-id="72e5e-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="72e5e-662">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-662">no</span></span>             | <span data-ttu-id="72e5e-663">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-663">no</span></span>           |
| <span data-ttu-id="72e5e-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="72e5e-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="72e5e-665">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-665">no</span></span>             | <span data-ttu-id="72e5e-666">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-666">no</span></span>           |
| <span data-ttu-id="72e5e-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="72e5e-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="72e5e-668">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-668">no</span></span>             | <span data-ttu-id="72e5e-669">nie</span><span class="sxs-lookup"><span data-stu-id="72e5e-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="72e5e-670">Ograniczenia i znane problemy</span><span class="sxs-lookup"><span data-stu-id="72e5e-670">Limitations and known issues</span></span>
<span data-ttu-id="72e5e-671">Oto lista ograniczeń i znanych problemów:</span><span class="sxs-lookup"><span data-stu-id="72e5e-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="72e5e-672">Interfejsy API planowania mogą być używane tylko przez **Użytkowników z licencją programu Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="72e5e-673">Nie mogą z nich korzystać:</span><span class="sxs-lookup"><span data-stu-id="72e5e-673">They can't be used by:</span></span>
    - <span data-ttu-id="72e5e-674">Użytkownicy aplikacji</span><span class="sxs-lookup"><span data-stu-id="72e5e-674">Application users</span></span>
    - <span data-ttu-id="72e5e-675">Użytkownicy systemowi</span><span class="sxs-lookup"><span data-stu-id="72e5e-675">System users</span></span>
    - <span data-ttu-id="72e5e-676">Użytkownicy integracyjni</span><span class="sxs-lookup"><span data-stu-id="72e5e-676">Integration users</span></span>
    - <span data-ttu-id="72e5e-677">Inni użytkownicy, którzy nie mają wymaganej licencji</span><span class="sxs-lookup"><span data-stu-id="72e5e-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="72e5e-678">Każdy **OperationSet** może mieć maksymalnie 100 operacji.</span><span class="sxs-lookup"><span data-stu-id="72e5e-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="72e5e-679">Każdy użytkownik może mieć otwartych maksymalnie 10 **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="72e5e-680">Project Operations obsługuje obecnie maksymalnie 500 wszystkich zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="72e5e-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="72e5e-681">Obecnie nie są dostępne dzienniki błędów i stanu niepowodzenia **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="72e5e-682">Harmonogram interfejsów API jest w publicznej wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="72e5e-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="72e5e-683">Używanie tych interfejsów API w środowisku produkcyjnym nie jest obsługiwane przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="72e5e-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="72e5e-684">Limity i ograniczenia projektów i zadań</span><span class="sxs-lookup"><span data-stu-id="72e5e-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="72e5e-685">Obsługa błędów</span><span class="sxs-lookup"><span data-stu-id="72e5e-685">Error handling</span></span>

   - <span data-ttu-id="72e5e-686">Aby przejrzeć błędy wygenerowane z zestawów operacji, przejdź do strony **Ustawienia** \> **Harmonogram integracji** \> **Zestawy operacji**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="72e5e-687">Aby przejrzeć błędy wygenerowane w usłudze planowania projektów, przejdź do menu **Ustawienia** \> **Harmonogram integracji** \> **Dziennik błędów PSS**.</span><span class="sxs-lookup"><span data-stu-id="72e5e-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="72e5e-688">Przykładowy scenariusz</span><span class="sxs-lookup"><span data-stu-id="72e5e-688">Sample scenario</span></span>

<span data-ttu-id="72e5e-689">W tym scenariuszu zostanie utworzyć projekt, członka zespołu, cztery zadania i dwa przypisania zasobów.</span><span class="sxs-lookup"><span data-stu-id="72e5e-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="72e5e-690">Następnie należy zaktualizować jedno zadanie, zaktualizować projekt, usunąć jedno zadanie, usunąć jedno przypisanie zasobów i utworzyć zależność zadania.</span><span class="sxs-lookup"><span data-stu-id="72e5e-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="72e5e-691">Więcej przykładów</span><span class="sxs-lookup"><span data-stu-id="72e5e-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
