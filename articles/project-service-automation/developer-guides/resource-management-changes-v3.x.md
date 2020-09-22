---
title: Zmiany w zarządzaniu zasobami (Project Service Automation wer. 3.x)
description: Ten temat zawiera informacje o zmianach w obszarze Zarządzanie zasobami.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754343"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="d8285-103">Zmiany w zarządzaniu zasobami (Project Service Automation wer. 3.x)</span><span class="sxs-lookup"><span data-stu-id="d8285-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="d8285-104">Sekcje tego tematu zawierają informacje o zmianach wprowadzonych w obszarze Zarządzanie zasobami w programie Dynamics 365 Project Service Automation w wersji 3.x.</span><span class="sxs-lookup"><span data-stu-id="d8285-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="d8285-105">Szacowania projektu</span><span class="sxs-lookup"><span data-stu-id="d8285-105">Project estimates</span></span>

<span data-ttu-id="d8285-106">Szacunki projektu już nie opierają się na encji **msdyn\_projecttask** (**Zadanie projektu**), ale na encji **msdyn\_resourceassignment** (**Przypisanie zasobu**).</span><span class="sxs-lookup"><span data-stu-id="d8285-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="d8285-107">Przypisania zasobów stały się „źródłem prawdziwych informacji” dla aparatów planowania zadań i kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="d8285-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="d8285-108">Zadania wierszy</span><span class="sxs-lookup"><span data-stu-id="d8285-108">Line tasks</span></span>

<span data-ttu-id="d8285-109">W programie PSA 3.x funkcjonalność zadań wierszy została wycofana.</span><span class="sxs-lookup"><span data-stu-id="d8285-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="d8285-110">Obecnie przypisania wskazują całe zadanie, a nie poszczególne wiersze zadania.</span><span class="sxs-lookup"><span data-stu-id="d8285-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="d8285-111">W poniższym przykładzie pokazano, jak zadanie o nazwie „Zadanie testowe” jest przypisywane członkom zespołu A i B w starszych wersjach programu PSA i w wersji PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="d8285-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="d8285-112">**Przed wersją PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="d8285-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="d8285-113">Zadanie testowe</span><span class="sxs-lookup"><span data-stu-id="d8285-113">Test task</span></span>

        - <span data-ttu-id="d8285-114">Zadanie testowe — zadanie wiersza 1</span><span class="sxs-lookup"><span data-stu-id="d8285-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="d8285-115">Przypisanie do osoby A</span><span class="sxs-lookup"><span data-stu-id="d8285-115">Assignment to A</span></span>

        - <span data-ttu-id="d8285-116">Zadanie testowe — zadanie wiersza 2</span><span class="sxs-lookup"><span data-stu-id="d8285-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="d8285-117">Przypisanie do osoby B</span><span class="sxs-lookup"><span data-stu-id="d8285-117">Assignment to B</span></span>

- <span data-ttu-id="d8285-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="d8285-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="d8285-119">Zadanie testowe</span><span class="sxs-lookup"><span data-stu-id="d8285-119">Test task</span></span>

        - <span data-ttu-id="d8285-120">Przypisanie do osoby A</span><span class="sxs-lookup"><span data-stu-id="d8285-120">Assignment to A</span></span>
        - <span data-ttu-id="d8285-121">Przypisanie do osoby B</span><span class="sxs-lookup"><span data-stu-id="d8285-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="d8285-122">Nieprzydzielone przypisanie</span><span class="sxs-lookup"><span data-stu-id="d8285-122">Unassigned assignment</span></span>

<span data-ttu-id="d8285-123">W programie PSA 3.x nieprzydzielone przypisanie to takie, które zostało przypisane do członka zespołu **NULL** i zasobu **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d8285-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="d8285-124">Nieprzydzielone przypisania mogą występować w różnych scenariuszach:</span><span class="sxs-lookup"><span data-stu-id="d8285-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="d8285-125">Jeśli zadanie zostało utworzone, ale nie zostało jeszcze przypisane żadnemu członkowi zespołu, zawsze jest tworzone nieprzydzielone przypisanie.</span><span class="sxs-lookup"><span data-stu-id="d8285-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="d8285-126">Jeśli wszystkie osoby przypisane do zadania zostaną usunięte, dla tego zadania zostanie ponownie utworzone nieprzydzielone przypisanie.</span><span class="sxs-lookup"><span data-stu-id="d8285-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="d8285-127">Pola planowania w encji Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="d8285-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="d8285-128">Pola w encji **msdyn\_projecttask** zostały wycofane lub przeniesione do encji **msdyn\_resourceassignment** albo są obecnie przywoływane przez encję **msdyn\_projectteam** (**Członek zespołu projektu**).</span><span class="sxs-lookup"><span data-stu-id="d8285-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="d8285-129">Wycofane pole w encji msdyn\_projecttask (Zadanie projektu)</span><span class="sxs-lookup"><span data-stu-id="d8285-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d8285-130">Nowe pole w encji msdyn\_resourceassignment (Przypisanie zasobu)</span><span class="sxs-lookup"><span data-stu-id="d8285-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="d8285-131">Komentarz</span><span class="sxs-lookup"><span data-stu-id="d8285-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="d8285-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="d8285-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="d8285-133">Brak</span><span class="sxs-lookup"><span data-stu-id="d8285-133">None</span></span> | |
| <span data-ttu-id="d8285-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="d8285-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="d8285-135">Brak</span><span class="sxs-lookup"><span data-stu-id="d8285-135">None</span></span> | |
| <span data-ttu-id="d8285-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="d8285-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="d8285-137">Brak</span><span class="sxs-lookup"><span data-stu-id="d8285-137">None</span></span> | |
| <span data-ttu-id="d8285-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="d8285-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="d8285-139">Brak</span><span class="sxs-lookup"><span data-stu-id="d8285-139">None</span></span> | |
| <span data-ttu-id="d8285-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="d8285-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="d8285-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="d8285-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="d8285-142">Zmieniła się struktura danych formatu JavaScript Object Notation (JSON) przechowywana w polu.</span><span class="sxs-lookup"><span data-stu-id="d8285-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="d8285-143">Rozkład harmonogramu</span><span class="sxs-lookup"><span data-stu-id="d8285-143">Schedule contour</span></span>

<span data-ttu-id="d8285-144">Rozkład harmonogramu jest przechowywany w polu **Zaplanowana praca** (**msdyn\_plannedwork**) każdej encji **Przypisanie zasobu** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="d8285-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="d8285-145">Struktura</span><span class="sxs-lookup"><span data-stu-id="d8285-145">Structure</span></span>

<span data-ttu-id="d8285-146">Nowa struktura rozkładu harmonogramu składa się z elastycznych fragmentów czasu, które są definiowane dla każdego dnia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d8285-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="d8285-147">Każdy fragment czasu ma następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="d8285-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="d8285-148">**Początek** — początek godzin pracy w dniu, zgodnie z kalendarzem projektu.</span><span class="sxs-lookup"><span data-stu-id="d8285-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="d8285-149">**Koniec** — koniec godzin pracy w dniu, zgodnie z kalendarzem projektu.</span><span class="sxs-lookup"><span data-stu-id="d8285-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="d8285-150">**Godziny** — liczba godzin przypisana do dnia.</span><span class="sxs-lookup"><span data-stu-id="d8285-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="d8285-151">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="d8285-151">**Example**</span></span>

<span data-ttu-id="d8285-152">W tym przykładzie jest używany kalendarz projektu, w którym dzień roboczy trwa od 9.00 do 17.00 w strefie czasowej UTC-8.</span><span class="sxs-lookup"><span data-stu-id="d8285-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="d8285-153">Planowanie automatyczne i ręczne</span><span class="sxs-lookup"><span data-stu-id="d8285-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="d8285-154">Jeśli zadanie jest planowane automatycznie, system stara się zmieścić jak najwięcej godzin na początku i czas trwania zadania może wtedy zostać skrócony.</span><span class="sxs-lookup"><span data-stu-id="d8285-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="d8285-155">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="d8285-155">**Example**</span></span>

<span data-ttu-id="d8285-156">Poniższe zadanie zostało zaplanowane automatycznie na 18 godzin w ciągu trzech dni (od 3 grudnia 2018 r. do 5 grudnia 2018 r.).</span><span class="sxs-lookup"><span data-stu-id="d8285-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="d8285-157">Jeśli zadanie jest planowane ręcznie, godziny są rozmieszczane równo między wszystkie dni.</span><span class="sxs-lookup"><span data-stu-id="d8285-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="d8285-158">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="d8285-158">**Example**</span></span>

<span data-ttu-id="d8285-159">Poniższe zadanie zostało zaplanowane ręcznie na 18 godzin w ciągu trzech dni (od 3 grudnia 2018 r. do 5 grudnia 2018 r.).</span><span class="sxs-lookup"><span data-stu-id="d8285-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="d8285-160">Jednostka przypisania</span><span class="sxs-lookup"><span data-stu-id="d8285-160">Assignment unit</span></span>

<span data-ttu-id="d8285-161">Funkcjonalność jednostki przypisania została wycofana w programie PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="d8285-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="d8285-162">Godziny nakładu pracy zadania są obecnie równo dzielone w ciągu dnia między wszystkie przypisane zasoby.</span><span class="sxs-lookup"><span data-stu-id="d8285-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="d8285-163">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="d8285-163">**Example**</span></span>

<span data-ttu-id="d8285-164">W tym przykładzie zadanie zostało przypisane do dwóch zasobów i automatycznie zaplanowane na 36 godzin w ciągu trzech dni (od 3 grudnia 2018 r. do 5 grudnia 2018 r.).</span><span class="sxs-lookup"><span data-stu-id="d8285-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="d8285-165">Przypisanie 1:</span><span class="sxs-lookup"><span data-stu-id="d8285-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="d8285-166">Przypisanie 2:</span><span class="sxs-lookup"><span data-stu-id="d8285-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="d8285-167">Wymiary kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="d8285-167">Pricing dimensions</span></span>

<span data-ttu-id="d8285-168">W programie PSA 3.x pola wymiaru kalkulacji cen specyficzne dla zasobów (takie jak **Rola** i **Jednostka organizacyjna**) zostały usunięte z encji **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="d8285-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="d8285-169">Te pola można teraz pobrać od odpowiedniego członka zespołu projektu (**msdyn\_projectteam**) w przypisaniu zasobu (**msdyn\_resourceassignment**) podczas generowania oszacowań projektu.</span><span class="sxs-lookup"><span data-stu-id="d8285-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="d8285-170">Do encji **msdyn\_projectteam** dodano nowe pole **msdyn\_organizationalunit**.</span><span class="sxs-lookup"><span data-stu-id="d8285-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="d8285-171">Wycofane pole w encji msdyn\_projecttask (Zadanie projektu)</span><span class="sxs-lookup"><span data-stu-id="d8285-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d8285-172">Pola z encji msdyn\_projectteam (Członek zespołu projektu) używane w zamian</span><span class="sxs-lookup"><span data-stu-id="d8285-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="d8285-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d8285-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="d8285-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d8285-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="d8285-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="d8285-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="d8285-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="d8285-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="d8285-177">Rozkłady</span><span class="sxs-lookup"><span data-stu-id="d8285-177">Contours</span></span>

<span data-ttu-id="d8285-178">Pola rozkładu kalkulacji cen i szacowania zostały wycofane z encji **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="d8285-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="d8285-179">Zostały przeniesione do encji **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="d8285-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="d8285-180">Wycofane pole w encji msdyn\_projecttask (Zadanie projektu)</span><span class="sxs-lookup"><span data-stu-id="d8285-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d8285-181">Nowe pole w encji msdyn\_resourceassignment (Przypisanie zasobu)</span><span class="sxs-lookup"><span data-stu-id="d8285-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="d8285-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="d8285-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="d8285-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="d8285-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="d8285-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="d8285-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="d8285-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="d8285-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="d8285-186">Następujące pola zostały dodane do encji **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="d8285-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="d8285-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d8285-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="d8285-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d8285-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="d8285-189">W encji **msdyn\_projecttask** nie zmieniono następujących pól kosztu ani sprzedaży planowanych, rzeczywistych i pozostałych:</span><span class="sxs-lookup"><span data-stu-id="d8285-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="d8285-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d8285-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="d8285-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d8285-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="d8285-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="d8285-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="d8285-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="d8285-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="d8285-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d8285-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="d8285-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d8285-195">msdyn\_remainingsales</span></span>
