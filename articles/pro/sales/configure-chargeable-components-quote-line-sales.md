---
title: Konfigurowanie odpłatnych składników wiersza oferty
description: Ten temat zawiera informacje na temat konfigurowania odpłatnych i nieodpłatnych składników w wierszu oferty opartej na projekcie.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003779"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="26f5f-103">Konfigurowanie odpłatnych składników wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="26f5f-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="26f5f-104">_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_</span><span class="sxs-lookup"><span data-stu-id="26f5f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="26f5f-105">Pozycja oferty oparta na projekcie zawiera składniki typu *dołączane* i *odpłatne*.</span><span class="sxs-lookup"><span data-stu-id="26f5f-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="26f5f-106">Dołączone składniki są poddawane:</span><span class="sxs-lookup"><span data-stu-id="26f5f-106">Included components are subject to:</span></span>

  - <span data-ttu-id="26f5f-107">Podlegają podziałom metody fakturowania i klienta</span><span class="sxs-lookup"><span data-stu-id="26f5f-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="26f5f-108">Nieprzekraczalne limity</span><span class="sxs-lookup"><span data-stu-id="26f5f-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="26f5f-109">Ustawienia częstotliwości faktur zdefiniowane w pozycji oferty opartej na projekcie</span><span class="sxs-lookup"><span data-stu-id="26f5f-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="26f5f-110">Podzbiór dołączonych składników można oznaczyć jako odpłatny przy użyciu pola **Typ fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="26f5f-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="26f5f-111">Pole **Typ fakturowania** jest zestawem opcji, który zezwala na korzystanie z następujących wartości w kontekście pozycji oferty:</span><span class="sxs-lookup"><span data-stu-id="26f5f-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="26f5f-112">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-112">Chargeable</span></span>
  - <span data-ttu-id="26f5f-113">Nieodpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-113">Non-chargeable</span></span>

<span data-ttu-id="26f5f-114">Składniki odpłatne mogą być definiowane w zadaniach, rolach i kategoriach transakcji.</span><span class="sxs-lookup"><span data-stu-id="26f5f-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="26f5f-115">Opłata jest definiowana w zadaniach dla pozycji oferty projektu i stosowana do wszystkich klas transakcji zawartych w tym wierszu.</span><span class="sxs-lookup"><span data-stu-id="26f5f-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="26f5f-116">Jeśli pole **Dołącz zadania** w wierszu kontraktu jest puste lub ustawione na wartość **Cały projekt**, karta **Zadania odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="26f5f-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="26f5f-117">Opłata zdefiniowana w rolach pozycji oferty, która ma zastosowanie tylko do klasy transakcji **Czas**.</span><span class="sxs-lookup"><span data-stu-id="26f5f-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="26f5f-118">Jeśli pole **Dołącz czas** w wierszu oferty jest puste lub ustawione na wartość **Nie**, karta **Role odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="26f5f-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="26f5f-119">Opłata zdefiniowana w kategoriach transakcji pozycji oferty projektu ma zastosowanie tylko do klasy transakcji **Wydatek**.</span><span class="sxs-lookup"><span data-stu-id="26f5f-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="26f5f-120">Jeśli pole **Dołącz wydatki** w wierszu oferty jest puste lub ustawione na wartość **Nie**, karta **Kategorie odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="26f5f-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="26f5f-121">Aktualizowanie zadania projektu w stan odpłatny lub nieodpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="26f5f-122">Zadanie projektu może być odpłatne lub niepłatne w ramach określonej pozycji oferty opartej na projekcie, co powoduje, że dostępne są następujące ustawienia.</span><span class="sxs-lookup"><span data-stu-id="26f5f-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="26f5f-123">Jeśli wiersz oferty opartej na projekcie zawiera **Czas** i zadanie **T1**, zadanie jest skojarzone z wierszem oferty jako odpłatne.</span><span class="sxs-lookup"><span data-stu-id="26f5f-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="26f5f-124">Jeśli istnieje drugi wiersz oferty zawierający **Wydatki**, można skojarzyć zadanie **T1** w pozycji oferty jako nieodpłatne.</span><span class="sxs-lookup"><span data-stu-id="26f5f-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="26f5f-125">W efekcie cały czas zanotowany dla zadania jest odpłatny, a wydatki zapisane w zadaniu nie.</span><span class="sxs-lookup"><span data-stu-id="26f5f-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="26f5f-126">Typ fakturowania zadania można skonfigurować na karcie **Odpłatne zadania** w pozycji oferty opartej na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Zadania wiersza oferty**.</span><span class="sxs-lookup"><span data-stu-id="26f5f-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="26f5f-127">Alternatywnie możesz zaktualizować typ rozliczenia dla zadania projektu w polu **Typ fakturowania** w podsiatce w konfiguracji rozliczenia zadania projektu, która pokazuje wiersze oferty skojarzone z zadaniem.</span><span class="sxs-lookup"><span data-stu-id="26f5f-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="26f5f-128">Aktualizowanie ról projektu jako odpłatnego lub niepłatnego</span><span class="sxs-lookup"><span data-stu-id="26f5f-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="26f5f-129">W kontekście określonego wiersza oferty opartej na projekcie rola może być odpłatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="26f5f-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="26f5f-130">Typ fakturowania roli można skonfigurować na karcie **Odpłatne role** w pozycji oferty na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Odpłatne role**.</span><span class="sxs-lookup"><span data-stu-id="26f5f-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="26f5f-131">Aktualizowanie kategorii transakcji jako odpłatnej lub nie</span><span class="sxs-lookup"><span data-stu-id="26f5f-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="26f5f-132">Kategoria transakcji w danej pozycji oferty może być płatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="26f5f-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="26f5f-133">Typ fakturowania tranzakcji można skonfigurować na karcie **Odpłatne kategorie** w pozycji oferty na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Odpłatne kategorie**.</span><span class="sxs-lookup"><span data-stu-id="26f5f-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="26f5f-134">Rozwiązywanie odpłatności</span><span class="sxs-lookup"><span data-stu-id="26f5f-134">Resolve chargeability</span></span>
<span data-ttu-id="26f5f-135">Wartość szacunkowa lub faktycznie utworzona dla czasu będzie uznana za wymagalną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="26f5f-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="26f5f-136">**Czas** jest zawarty w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="26f5f-137">**Rola** jest skonfigurowana jako płatna w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="26f5f-138">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="26f5f-139">Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest też skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="26f5f-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="26f5f-140">Szacunek lub wartość rzeczywista utworzona dla wydatku jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="26f5f-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="26f5f-141">**Wydatek** jest zawarty w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="26f5f-142">**Kategoria transakcji** jest skonfigurowana jako płatna w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="26f5f-143">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="26f5f-144">Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest też skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="26f5f-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="26f5f-145">Wartość szacunkowa lub faktycznie utworzona dla materiału będzie uznana za wymagalną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="26f5f-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="26f5f-146">**Materiały** sa zawarte w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="26f5f-147">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="26f5f-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="26f5f-148">Jeśli te dwie rzeczy zostaną spełnione, **Zadanie** powinno też być skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="26f5f-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-149">
                    <strong>Uwzględnia czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="26f5f-150">
                    <strong>Uwzględnia wydatek</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="26f5f-151">
                    <strong>Uwzględnij materiały</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="26f5f-152">
                    <strong>Uwzględnione zadania</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-153">
                    <strong>Rola</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-154">
                    <strong>Kategoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-155">
                    <strong>Zadanie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="26f5f-156">
                    <strong>Wpływ opłaty</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-157">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-158">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-159">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-160">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="26f5f-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-161">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-162">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-163">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-164">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-165">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-166">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-167">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-168">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-169">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-170">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="26f5f-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-171">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-172">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-173">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-174">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-175">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-176">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-177">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-178">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-179">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-180">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="26f5f-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-181">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-182">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-183">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-184">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-185">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-186">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-187">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-188">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-189">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-190">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="26f5f-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-191">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-192">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-193">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-194">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-195">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-196">Typ fakturowania wartości rzeczywistej materiału: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-197">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-198">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-199">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-200">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="26f5f-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-201">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-202">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-203">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-204">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-205">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-206">Typ fakturowania wartości rzeczywistej materiału: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-207">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-208">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-209">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-210">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="26f5f-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-211">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-212">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-213">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-214">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-215">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-216">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-218">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-219">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-220">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="26f5f-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-221">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-222">
                    <strong>Odpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-223">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-224">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-225">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-226">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-228">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-229">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-230">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="26f5f-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-231">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-232">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-233">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-234">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-235">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-236">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-237">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="26f5f-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-239">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-240">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="26f5f-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-241">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-242">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-243">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-244">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-245">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-246">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-247">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="26f5f-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26f5f-249">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-250">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="26f5f-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-251">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-252">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-253">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-254">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-255">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-256">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-257">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-258">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="26f5f-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-260">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="26f5f-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-261">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-262">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="26f5f-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-263">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-264">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-265">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="26f5f-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26f5f-266">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26f5f-267">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26f5f-268">Tak</span><span class="sxs-lookup"><span data-stu-id="26f5f-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="26f5f-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26f5f-270">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="26f5f-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26f5f-271">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26f5f-272">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26f5f-273">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="26f5f-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26f5f-274">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-275">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="26f5f-276">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26f5f-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
