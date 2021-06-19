---
title: Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie
description: W tym temacie zamieszczono informacje dotyczące sposobu dodawania odpłatnych składników do pozycji kontraktu w Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003734"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="20f92-103">Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie</span><span class="sxs-lookup"><span data-stu-id="20f92-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="20f92-104">_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_</span><span class="sxs-lookup"><span data-stu-id="20f92-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="20f92-105">Pozycja kontraktu oparta na projekcie zawiera składniki typu *dołączane* i *odpłatne*.</span><span class="sxs-lookup"><span data-stu-id="20f92-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="20f92-106">Dołączone składniki to składniki, które:</span><span class="sxs-lookup"><span data-stu-id="20f92-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="20f92-107">Podlegają podziałom metody fakturowania i klienta</span><span class="sxs-lookup"><span data-stu-id="20f92-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="20f92-108">Nieprzekraczalne limity</span><span class="sxs-lookup"><span data-stu-id="20f92-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="20f92-109">Ustawienia częstotliwości faktur zdefiniowane w pozycji kontraktu opartego na projekcie</span><span class="sxs-lookup"><span data-stu-id="20f92-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="20f92-110">Podzbiór dołączonych składników można oznaczyć jako odpłatny przy użyciu pola **Typ fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="20f92-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="20f92-111">Pole **Typ fakturowania** jest zestawem opcji, który zezwala na korzystanie z następujących wartości w kontekście pozycji kontraktu:</span><span class="sxs-lookup"><span data-stu-id="20f92-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="20f92-112">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-112">Chargeable</span></span>
  - <span data-ttu-id="20f92-113">Nieodpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-113">Non-chargeable</span></span>

<span data-ttu-id="20f92-114">Składniki odpłatne mogą być definiowane w zadaniach, rolach i kategoriach transakcji.</span><span class="sxs-lookup"><span data-stu-id="20f92-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="20f92-115">Opłata jest definiowana w zadaniach dla pozycji kontraktu projektu i stosowana do wszystkich klas transakcji zawartych w wierszu.</span><span class="sxs-lookup"><span data-stu-id="20f92-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="20f92-116">Jeśli pole **Dołącz zadania** w wierszu kontraktu jest puste lub ustawione na wartość **Cały projekt**, karta **Zadania odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="20f92-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="20f92-117">Opłata zdefiniowana w rolach pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Czas**.</span><span class="sxs-lookup"><span data-stu-id="20f92-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="20f92-118">Jeśli pole **Dołącz czas** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Role odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="20f92-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="20f92-119">Opłata zdefiniowana w kategoriach transakcji pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Wydatek**.</span><span class="sxs-lookup"><span data-stu-id="20f92-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="20f92-120">Jeśli pole **Wydatek** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Kategorie odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="20f92-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="20f92-121">Aktualizowanie zadania projektu jako odpłatnego lub niepłatnego</span><span class="sxs-lookup"><span data-stu-id="20f92-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="20f92-122">Zadanie projektu może być odpłatne lub niepłatne w ramach określonej pozycji kontraktu, co powoduje, że dostępne są następujące ustawienia:</span><span class="sxs-lookup"><span data-stu-id="20f92-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="20f92-123">Jeśli pozycja kontraktu oparta na projekcie zawiera **Czas** i określone zadanie, **T1** jest z nim skojarzone jako odpłatne.</span><span class="sxs-lookup"><span data-stu-id="20f92-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="20f92-124">Jeśli istnieje drugi wiersz kontraktu zawierający **Wydatki**, można skojarzyć zadanie T1 w pozycji kontraktu z jako nieodpłatne.</span><span class="sxs-lookup"><span data-stu-id="20f92-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="20f92-125">W efekcie cały czas zanotowany dla zadania jest odpłatny, a wydatki nie.</span><span class="sxs-lookup"><span data-stu-id="20f92-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="20f92-126">Typ fakturowania zadania można skonfigurować na karcie **Odpłatne zadania** w pozycji kontraktu przez zaktualizowanie pola **Typ fakturowania** w podsiatce zadania związane z pozycjami kontraktu.</span><span class="sxs-lookup"><span data-stu-id="20f92-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="20f92-127">Można również zaktualizować pole **Typ fakturowania** w podsiatce ustawień fakturowania zadań projektu, który zawiera pozycje kontraktu skojarzone z zadaniem.</span><span class="sxs-lookup"><span data-stu-id="20f92-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="20f92-128">Aktualizowanie ról projektu jako odpłatnego lub niepłatnego</span><span class="sxs-lookup"><span data-stu-id="20f92-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="20f92-129">Rola w danej pozycji kontraktu może być płatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="20f92-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="20f92-130">Typ fakturowania roli można skonfigurować na karcie **Role płatne** w pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="20f92-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="20f92-131">W tym celu należy zaktualizować pole **Typ fakturowania** w podsiatce **Role płatne**.</span><span class="sxs-lookup"><span data-stu-id="20f92-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="20f92-132">Aktualizowanie kategorii transakcji jako odpłatnej lub nie</span><span class="sxs-lookup"><span data-stu-id="20f92-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="20f92-133">Kategoria transakcji w danej pozycji kontraktu może być płatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="20f92-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="20f92-134">Typ fakturowania transakcji można skonfigurować na karcie **Kategorie płatne** w pozycji kontraktu opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="20f92-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="20f92-135">W tym celu należy zaktualizować pole **Typ fakturowania** w podsiatce **Kategorie płatne**.</span><span class="sxs-lookup"><span data-stu-id="20f92-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="20f92-136">Rozwiązywanie odpłatności</span><span class="sxs-lookup"><span data-stu-id="20f92-136">Resolve chargeability</span></span>

<span data-ttu-id="20f92-137">Szacunek lub wartość rzeczywista utworzona dla czasu jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="20f92-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="20f92-138">**Czas** jest zawarty w wierszu kontraktu.</span><span class="sxs-lookup"><span data-stu-id="20f92-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="20f92-139">**Rola** jest skonfigurowana jako płatna w wierszu kontraktu.</span><span class="sxs-lookup"><span data-stu-id="20f92-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="20f92-140">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu kontraktu.</span><span class="sxs-lookup"><span data-stu-id="20f92-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="20f92-141">Jeśli te trzy rzeczy zostaną spełnione, zadanie jest skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="20f92-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="20f92-142">Szacunek lub wartość rzeczywista utworzona dla wydatku jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="20f92-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="20f92-143">**Wydatek** jest zawarty w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="20f92-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="20f92-144">**Kategoria transakcji** jest skonfigurowana jako płatna w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="20f92-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="20f92-145">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadanie** w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="20f92-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="20f92-146">Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="20f92-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="20f92-147">Szacunek lub wartość rzeczywista utworzona dla materiału jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="20f92-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="20f92-148">**Materiał** jest zawarty w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="20f92-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="20f92-149">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="20f92-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="20f92-150">Jeśli te dwie rzeczy zostaną spełnione, **Zadanie** jest skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="20f92-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-151">
                    <strong>Uwzględnia czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="20f92-152">
                    <strong>Uwzględnia wydatek</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="20f92-153">
                    <strong>Uwzględnij materiały</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="20f92-154">
                    <strong>Uwzględnione zadania</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-155">
                    <strong>Rola</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-156">
                    <strong>Kategoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-157">
                    <strong>Zadanie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="20f92-158">
                    <strong>Wpływ opłaty</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-159">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-160">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-161">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-162">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="20f92-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-163">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-164">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-165">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-166">Fakturowanie wartości rzeczywistej czas: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-167">Typ fakturowania wartości rzeczywistej wydatku: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-168">Typ fakturowania wartości rzeczywistej materiału: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-169">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-170">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-171">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-172">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="20f92-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-173">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-174">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-175">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-176">Fakturowanie wartości rzeczywistej czas: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-177">Typ fakturowania wartości rzeczywistej wydatku: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-178">Typ fakturowania wartości rzeczywistej materiału: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-179">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-180">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-181">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-182">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="20f92-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-183">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-184">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-185">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-186">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-187">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="20f92-188">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-189">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-190">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-191">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-192">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="20f92-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-193">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-194">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-195">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-196">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-197">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-198">Typ fakturowania wartości rzeczywistej materiału: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-199">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-200">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-201">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-202">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="20f92-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-203">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-204">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-205">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-206">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-207">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-208">Typ fakturowania wartości rzeczywistej materiału: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-209">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-210">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-211">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-212">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="20f92-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-213">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-214">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-215">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-216">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-217">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-218">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-220">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-221">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-222">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="20f92-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-223">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-224">
                    <strong>Odpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-225">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-226">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-227">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="20f92-228">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-230">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-231">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-232">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="20f92-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-233">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-234">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-235">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-236">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-237">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-238">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-239">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="20f92-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-241">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-242">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="20f92-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-243">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-244">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-245">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-246">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="20f92-247">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-248">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-249">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="20f92-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="20f92-251">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-252">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="20f92-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-253">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-254">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-255">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-256">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-257">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-258">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-259">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-260">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="20f92-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-262">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="20f92-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-263">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-264">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="20f92-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-265">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-266">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="20f92-267">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="20f92-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="20f92-268">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="20f92-269">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="20f92-270">Tak</span><span class="sxs-lookup"><span data-stu-id="20f92-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="20f92-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="20f92-272">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="20f92-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="20f92-273">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="20f92-274">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="20f92-275">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="20f92-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="20f92-276">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-277">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="20f92-278">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="20f92-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
