---
title: Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie
description: W tym temacie zamieszczono informacje dotyczące sposobu dodawania odpłatnych składników do pozycji kontraktu w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858486"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="379e8-103">Konfigurowanie odpłatnych składników pozycji kontraktu opartego na projekcie</span><span class="sxs-lookup"><span data-stu-id="379e8-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="379e8-104">_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_</span><span class="sxs-lookup"><span data-stu-id="379e8-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="379e8-105">Pozycja kontraktu oparta na projekcie zawiera składniki typu *dołączane* i *odpłatne*.</span><span class="sxs-lookup"><span data-stu-id="379e8-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="379e8-106">Dołączone składniki to składniki, które:</span><span class="sxs-lookup"><span data-stu-id="379e8-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="379e8-107">Podlegają podziałom metody fakturowania i klienta</span><span class="sxs-lookup"><span data-stu-id="379e8-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="379e8-108">Nieprzekraczalne limity</span><span class="sxs-lookup"><span data-stu-id="379e8-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="379e8-109">Ustawienia częstotliwości faktur zdefiniowane w pozycji kontraktu opartego na projekcie</span><span class="sxs-lookup"><span data-stu-id="379e8-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="379e8-110">Podzbiór dołączonych składników można oznaczyć jako odpłatny przy użyciu pola **Typ fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="379e8-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="379e8-111">Pole **Typ fakturowania** jest zestawem opcji, który zezwala na korzystanie z następujących wartości w kontekście pozycji kontraktu:</span><span class="sxs-lookup"><span data-stu-id="379e8-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="379e8-112">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-112">Chargeable</span></span>
  - <span data-ttu-id="379e8-113">Nieodpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-113">Non-chargeable</span></span>

<span data-ttu-id="379e8-114">Składniki odpłatne mogą być definiowane w zadaniach, rolach i kategoriach transakcji.</span><span class="sxs-lookup"><span data-stu-id="379e8-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="379e8-115">Opłata jest definiowana w zadaniach dla pozycji kontraktu projektu i stosowana do wszystkich klas transakcji zawartych w wierszu.</span><span class="sxs-lookup"><span data-stu-id="379e8-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="379e8-116">Jeśli pole **Dołącz zadania** w wierszu kontraktu jest puste lub ustawione na wartość **Cały projekt**, karta **Zadania odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="379e8-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="379e8-117">Opłata zdefiniowana w rolach pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Czas**.</span><span class="sxs-lookup"><span data-stu-id="379e8-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="379e8-118">Jeśli pole **Dołącz czas** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Role odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="379e8-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="379e8-119">Opłata zdefiniowana w kategoriach transakcji pozycji kontraktu projektu ma zastosowanie tylko do klasy transakcji **Wydatek**.</span><span class="sxs-lookup"><span data-stu-id="379e8-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="379e8-120">Jeśli pole **Wydatek** w wierszu kontraktu jest puste lub ustawione na wartość **Nie**, karta **Kategorie odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="379e8-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="379e8-121">Aktualizowanie zadania projektu jako odpłatnego lub niepłatnego</span><span class="sxs-lookup"><span data-stu-id="379e8-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="379e8-122">Zadanie projektu może być odpłatne lub niepłatne w ramach określonej pozycji kontraktu, co powoduje, że dostępne są następujące ustawienia:</span><span class="sxs-lookup"><span data-stu-id="379e8-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="379e8-123">Jeśli pozycja kontraktu oparta na projekcie zawiera **Czas** i określone zadanie, **T1** jest z nim skojarzone jako odpłatne.</span><span class="sxs-lookup"><span data-stu-id="379e8-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="379e8-124">Jeśli istnieje drugi wiersz kontraktu zawierający **Wydatki**, można skojarzyć zadanie T1 w pozycji kontraktu z jako nieodpłatne.</span><span class="sxs-lookup"><span data-stu-id="379e8-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="379e8-125">W efekcie cały czas zanotowany dla zadania jest odpłatny, a wydatki nie.</span><span class="sxs-lookup"><span data-stu-id="379e8-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="379e8-126">Typ fakturowania zadania można skonfigurować na karcie **Odpłatne zadania** w pozycji kontraktu przez zaktualizowanie pola **Typ fakturowania** w podsiatce zadania związane z pozycjami kontraktu.</span><span class="sxs-lookup"><span data-stu-id="379e8-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="379e8-127">Można również zaktualizować pole **Typ fakturowania** w podsiatce ustawień fakturowania zadań projektu, który zawiera pozycje kontraktu skojarzone z zadaniem.</span><span class="sxs-lookup"><span data-stu-id="379e8-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="379e8-128">Aktualizowanie ról projektu jako odpłatnego lub niepłatnego</span><span class="sxs-lookup"><span data-stu-id="379e8-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="379e8-129">Rola w danej pozycji kontraktu może być płatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="379e8-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="379e8-130">Typ fakturowania roli można skonfigurować na karcie **Role płatne** w pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="379e8-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="379e8-131">W tym celu należy zaktualizować pole **Typ fakturowania** w podsiatce **Role płatne**.</span><span class="sxs-lookup"><span data-stu-id="379e8-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="379e8-132">Aktualizowanie kategorii transakcji jako odpłatnej lub nie</span><span class="sxs-lookup"><span data-stu-id="379e8-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="379e8-133">Kategoria transakcji w danej pozycji kontraktu może być płatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="379e8-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="379e8-134">Typ fakturowania transakcji można skonfigurować na karcie **Kategorie płatne** w pozycji kontraktu opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="379e8-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="379e8-135">W tym celu należy zaktualizować pole **Typ fakturowania** w podsiatce **Kategorie płatne**.</span><span class="sxs-lookup"><span data-stu-id="379e8-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="379e8-136">Rozwiązywanie odpłatności</span><span class="sxs-lookup"><span data-stu-id="379e8-136">Resolve chargeability</span></span>

<span data-ttu-id="379e8-137">Szacunek lub wartość rzeczywista utworzona dla czasu jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="379e8-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="379e8-138">**Czas** jest zawarty w wierszu kontraktu.</span><span class="sxs-lookup"><span data-stu-id="379e8-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="379e8-139">**Rola** jest skonfigurowana jako płatna w wierszu kontraktu.</span><span class="sxs-lookup"><span data-stu-id="379e8-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="379e8-140">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu kontraktu.</span><span class="sxs-lookup"><span data-stu-id="379e8-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="379e8-141">Jeśli te trzy rzeczy zostaną spełnione, zadanie jest skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="379e8-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="379e8-142">Szacunek lub wartość rzeczywista utworzona dla wydatku jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="379e8-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="379e8-143">**Wydatek** jest zawarty w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="379e8-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="379e8-144">**Kategoria transakcji** jest skonfigurowana jako płatna w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="379e8-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="379e8-145">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadanie** w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="379e8-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="379e8-146">Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="379e8-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="379e8-147">Szacunek lub wartość rzeczywista utworzona dla materiału jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="379e8-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="379e8-148">**Materiał** jest zawarty w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="379e8-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="379e8-149">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu kontraktu</span><span class="sxs-lookup"><span data-stu-id="379e8-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="379e8-150">Jeśli te dwie rzeczy zostaną spełnione, **Zadanie** jest skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="379e8-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-151">
                    <strong>Uwzględnia czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="379e8-152">
                    <strong>Uwzględnia wydatek</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="379e8-153">
                    <strong>Uwzględnij materiały</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="379e8-154">
                    <strong>Uwzględnione zadania</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-155">
                    <strong>Rola</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-156">
                    <strong>Kategoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-157">
                    <strong>Zadanie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="379e8-158">
                    <strong>Wpływ opłaty</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-159">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-160">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-161">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-162">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="379e8-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-163">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-164">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-165">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-166">Fakturowanie wartości rzeczywistej czas: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-167">Typ fakturowania wartości rzeczywistej wydatku: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-168">Typ fakturowania wartości rzeczywistej materiału: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-169">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-170">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-171">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-172">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="379e8-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-173">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-174">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-175">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-176">Fakturowanie wartości rzeczywistej czas: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-177">Typ fakturowania wartości rzeczywistej wydatku: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-178">Typ fakturowania wartości rzeczywistej materiału: <strong>Odpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-179">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-180">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-181">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-182">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="379e8-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-183">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-184">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-185">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-186">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-187">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="379e8-188">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-189">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-190">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-191">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-192">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="379e8-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-193">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-194">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-195">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-196">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-197">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-198">Typ fakturowania wartości rzeczywistej materiału: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-199">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-200">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-201">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-202">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="379e8-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-203">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-204">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-205">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-206">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-207">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-208">Typ fakturowania wartości rzeczywistej materiału: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-209">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-210">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-211">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-212">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="379e8-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-213">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-214">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-215">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-216">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-217">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-218">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-220">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-221">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-222">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="379e8-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-223">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-224">
                    <strong>Odpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-225">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-226">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-227">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="379e8-228">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-230">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-231">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-232">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="379e8-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-233">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-234">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-235">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-236">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-237">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-238">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-239">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="379e8-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-241">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-242">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="379e8-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-243">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-244">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-245">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-246">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="379e8-247">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-248">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-249">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="379e8-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="379e8-251">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-252">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="379e8-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-253">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-254">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-255">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-256">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-257">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-258">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-259">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-260">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="379e8-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-262">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="379e8-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-263">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-264">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="379e8-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-265">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-266">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="379e8-267">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="379e8-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="379e8-268">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="379e8-269">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="379e8-270">Tak</span><span class="sxs-lookup"><span data-stu-id="379e8-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="379e8-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="379e8-272">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="379e8-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="379e8-273">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="379e8-274">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="379e8-275">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="379e8-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="379e8-276">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-277">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="379e8-278">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="379e8-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
