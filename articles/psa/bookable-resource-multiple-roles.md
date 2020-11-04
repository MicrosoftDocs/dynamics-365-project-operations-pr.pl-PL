---
title: Szacowanie sprzedaży projektu i kosztów, gdy zasób udostępniany wypełnia wiele ról w projekcie
description: W tym temat przedstawiono informacje na temat sposobu, w jaki można użyć wymiarów kalkulacji cen do obsługi kalkulacji cen i wycen zasobu, który wypełnia wiele ról w projekcie.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082064"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="cecd4-103">Szacowanie sprzedaży projektu i kosztów, gdy zasób udostępniany wypełnia wiele ról w projekcie</span><span class="sxs-lookup"><span data-stu-id="cecd4-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="cecd4-104">Przedsiębiorstwa oparte na projektach często muszą dysponować jednym zasobem, aby wykonywać wiele ról w projekcie.</span><span class="sxs-lookup"><span data-stu-id="cecd4-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="cecd4-105">Każda z tych ról może mieć odmienną cenę i różny koszt, co oznacza, że czas zasobu w projekcie może mieć różny szacunek finansowy w zależności od stawek za fakturę i stawki kosztów dla poszczególnych ról.</span><span class="sxs-lookup"><span data-stu-id="cecd4-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="cecd4-106">Rozwiązanie Project Service Automation zezwala na konfigurowanie wartości w rekordach członków zespołu dla nazwanego zasobu i zezwala na różne zastąpienia dla każdego zadania, do którego jest przypisany członek zespołu.</span><span class="sxs-lookup"><span data-stu-id="cecd4-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="cecd4-107">W poniższym przykładzie wyjaśniono, jak to proste zastąpienie tej wartości umożliwia zasobowi korzystanie z wielu ról w projekcie z różnymi stawkami kosztów i fakturowania.</span><span class="sxs-lookup"><span data-stu-id="cecd4-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="cecd4-108">Tworzenie zadań</span><span class="sxs-lookup"><span data-stu-id="cecd4-108">Create tasks</span></span>
<span data-ttu-id="cecd4-109">Utwórz dwa zadania projektu, każde dla 40 godzin, zadanie a i zadanie B. Wybierz zadanie A jako poprzednik zadania B.</span><span class="sxs-lookup"><span data-stu-id="cecd4-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="cecd4-110">Skonfiguruj rolę i jednostkę organizacyjną dla ogólnego członka zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="cecd4-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="cecd4-111">Na stronie **harmonogram** wybierz wiersz **zadania** dla zadania A.</span><span class="sxs-lookup"><span data-stu-id="cecd4-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="cecd4-112">W polu **zasoby** listy rozwijanej wybierz pozycję **Utwórz**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="cecd4-113">Na stronie **Szybkie tworzenie członków zespołu** określ atrybuty ogólnego członka zespołu, który będzie mógł wykonać to zadanie.</span><span class="sxs-lookup"><span data-stu-id="cecd4-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="cecd4-114">Wybierz odpowiednią rolę i jednostkę organizacyjną, a następnie wybierz pozycję **Zapisz i zamknij**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="cecd4-115">Ogólny członek zespołu zostaje utworzony i przypisany do tego zadania.</span><span class="sxs-lookup"><span data-stu-id="cecd4-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="cecd4-116">Powtórz te kroki dla zadania B i upewnij się, że rola i jednostka organizacyjna w ogólnym członku zespołu utworzonym dla zadania B są inna niż dla zadania A.</span><span class="sxs-lookup"><span data-stu-id="cecd4-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="cecd4-117">Skonfiguruj rolę i jednostkę organizacyjną dla zadania projektu</span><span class="sxs-lookup"><span data-stu-id="cecd4-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="cecd4-118">Po utworzeniu zadania A wybierz zadanie, a następnie wybierz pozycję **Edytuj zadanie**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="cecd4-119">Na stronie **Szczegóły zadania** znajdź pola **Rola** i **Jednostka organizacyjna** , dodaj wartości wymagane dla zasobu, który wykona to zadanie.</span><span class="sxs-lookup"><span data-stu-id="cecd4-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="cecd4-120">W przypadku wykonywania tych scenariuszy przy użyciu danych demonstracyjnych w programie Project Service Automation wybierz opcję **Potencjalny klient konsultingowy** dla roli oraz **Fabrikam US** jako jednostkę organizacyjną.</span><span class="sxs-lookup"><span data-stu-id="cecd4-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="cecd4-121">Wybierz zadanie B, a następnie wybierz **Edytuj zadanie**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="cecd4-122">Na stronie **Szczegóły zadania** znajdź pola **Rola** i **Jednostka organizacyjna** , dodaj wartości wymagane dla zasobu, który wykona to zadanie.</span><span class="sxs-lookup"><span data-stu-id="cecd4-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="cecd4-123">Upewnij się, że wartości pól **Rola** i **Jednostka organizacyjna** różnią się między zadaniem B i zadaniem A.</span><span class="sxs-lookup"><span data-stu-id="cecd4-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="cecd4-124">W przypadku wykonywania tych scenariuszy przy użyciu danych demonstracyjnych w programie Project Service Automation wybierz opcję **Technik sieciowy** dla roli oraz **Fabrikam US** jako jednostkę organizacyjną.</span><span class="sxs-lookup"><span data-stu-id="cecd4-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="cecd4-125">Zapisz i zamknij stronę **Szczegóły zadania**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="cecd4-126">Członek zespołu i oszacowania zachowania</span><span class="sxs-lookup"><span data-stu-id="cecd4-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="cecd4-127">Na stronie **Szczegóły zadania** w **Członek zespołu** wybierz dwóch ogólnych członków zespołu, a następnie wybierz opcję **Generuj wymagania**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="cecd4-128">Wygeneruje to wymagania zasobu.</span><span class="sxs-lookup"><span data-stu-id="cecd4-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="cecd4-129">Wybierz wiersz członka zespołu do **Potencjalny klient konsultingowy** i wybierz pozycję **Rezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="cecd4-130">Tablica harmonogramu zostanie otwarta i zostanie zarezerwowany zasób dla tego wymagania.</span><span class="sxs-lookup"><span data-stu-id="cecd4-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="cecd4-131">Wybierz wiersz członka zespołu do **Technik sieciowy** i wybierz pozycję **Rezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="cecd4-132">Tablica harmonogramu zostanie otwarta i zostanie zarezerwowany ten sam zasób dla tego wymagania.</span><span class="sxs-lookup"><span data-stu-id="cecd4-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="cecd4-133">Siatka członka zespołu</span><span class="sxs-lookup"><span data-stu-id="cecd4-133">Team Member grid</span></span> 
<span data-ttu-id="cecd4-134">Zwróć uwagę, że w siatce **członków zespołu** są usuwane dwa podstawowe rekordy członków zespołu i są one zastąpione jednym zasobem.</span><span class="sxs-lookup"><span data-stu-id="cecd4-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="cecd4-135">Dla tego zasobu istnieje jeden zestaw wartości, który zawiera domyślny zestaw wartości dla **Roli** i **Jednostki organizacyjnej**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="cecd4-136">Po rozwinięciu wiersza rekordu tego członka zespołu można wyraźnie zobaczyć przypisania da obu tych zadań w rekordzie członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="cecd4-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="cecd4-137">Każdy wiersz przypisania zawiera specyficzne wartości zadania dla **Roli** i **Jednostki organizacyjnej**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="cecd4-138">Siatka szacowań</span><span class="sxs-lookup"><span data-stu-id="cecd4-138">Estimates grid</span></span> 
<span data-ttu-id="cecd4-139">Kiedy przechodzisz do siatki **Szacowań** , zauważysz, że oba przypisania dotyczące tego samego zasobu będą w różny sposób wycenione.</span><span class="sxs-lookup"><span data-stu-id="cecd4-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="cecd4-140">Przypisanie zasobu w zadaniu A ma cenę ustaloną za pomocą wartości atrybutu **Rola** **Potencjalnego klienta konsultingowego**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="cecd4-141">Przypisanie tego samego zasobu w zadaniu B ma cenę ustaloną za pomocą wartości atrybutu **Rola** **Technika sieciowego**.</span><span class="sxs-lookup"><span data-stu-id="cecd4-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





