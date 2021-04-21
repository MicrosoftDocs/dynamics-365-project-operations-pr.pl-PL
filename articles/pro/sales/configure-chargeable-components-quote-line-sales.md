---
title: Konfigurowanie odpłatnych składników wiersza oferty
description: Ten temat zawiera informacje na temat konfigurowania odpłatnych i nieodpłatnych składników w wierszu oferty opartej na projekcie.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858306"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="a2400-103">Konfigurowanie odpłatnych składników wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="a2400-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="a2400-104">_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_</span><span class="sxs-lookup"><span data-stu-id="a2400-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a2400-105">Pozycja oferty oparta na projekcie zawiera składniki typu *dołączane* i *odpłatne*.</span><span class="sxs-lookup"><span data-stu-id="a2400-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="a2400-106">Dołączone składniki są poddawane:</span><span class="sxs-lookup"><span data-stu-id="a2400-106">Included components are subject to:</span></span>

  - <span data-ttu-id="a2400-107">Podlegają podziałom metody fakturowania i klienta</span><span class="sxs-lookup"><span data-stu-id="a2400-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="a2400-108">Nieprzekraczalne limity</span><span class="sxs-lookup"><span data-stu-id="a2400-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="a2400-109">Ustawienia częstotliwości faktur zdefiniowane w pozycji oferty opartej na projekcie</span><span class="sxs-lookup"><span data-stu-id="a2400-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="a2400-110">Podzbiór dołączonych składników można oznaczyć jako odpłatny przy użyciu pola **Typ fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="a2400-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="a2400-111">Pole **Typ fakturowania** jest zestawem opcji, który zezwala na korzystanie z następujących wartości w kontekście pozycji oferty:</span><span class="sxs-lookup"><span data-stu-id="a2400-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="a2400-112">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-112">Chargeable</span></span>
  - <span data-ttu-id="a2400-113">Nieodpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-113">Non-chargeable</span></span>

<span data-ttu-id="a2400-114">Składniki odpłatne mogą być definiowane w zadaniach, rolach i kategoriach transakcji.</span><span class="sxs-lookup"><span data-stu-id="a2400-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="a2400-115">Opłata jest definiowana w zadaniach dla pozycji oferty projektu i stosowana do wszystkich klas transakcji zawartych w tym wierszu.</span><span class="sxs-lookup"><span data-stu-id="a2400-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="a2400-116">Jeśli pole **Dołącz zadania** w wierszu kontraktu jest puste lub ustawione na wartość **Cały projekt**, karta **Zadania odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="a2400-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="a2400-117">Opłata zdefiniowana w rolach pozycji oferty, która ma zastosowanie tylko do klasy transakcji **Czas**.</span><span class="sxs-lookup"><span data-stu-id="a2400-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="a2400-118">Jeśli pole **Dołącz czas** w wierszu oferty jest puste lub ustawione na wartość **Nie**, karta **Role odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="a2400-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="a2400-119">Opłata zdefiniowana w kategoriach transakcji pozycji oferty projektu ma zastosowanie tylko do klasy transakcji **Wydatek**.</span><span class="sxs-lookup"><span data-stu-id="a2400-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="a2400-120">Jeśli pole **Dołącz wydatki** w wierszu oferty jest puste lub ustawione na wartość **Nie**, karta **Kategorie odpłatne** nie będzie dostępna.</span><span class="sxs-lookup"><span data-stu-id="a2400-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="a2400-121">Aktualizowanie zadania projektu w stan odpłatny lub nieodpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="a2400-122">Zadanie projektu może być odpłatne lub niepłatne w ramach określonej pozycji oferty opartej na projekcie, co powoduje, że dostępne są następujące ustawienia.</span><span class="sxs-lookup"><span data-stu-id="a2400-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="a2400-123">Jeśli wiersz oferty opartej na projekcie zawiera **Czas** i zadanie **T1**, zadanie jest skojarzone z wierszem oferty jako odpłatne.</span><span class="sxs-lookup"><span data-stu-id="a2400-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="a2400-124">Jeśli istnieje drugi wiersz oferty zawierający **Wydatki**, można skojarzyć zadanie **T1** w pozycji oferty jako nieodpłatne.</span><span class="sxs-lookup"><span data-stu-id="a2400-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="a2400-125">W efekcie cały czas zanotowany dla zadania jest odpłatny, a wydatki zapisane w zadaniu nie.</span><span class="sxs-lookup"><span data-stu-id="a2400-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="a2400-126">Typ fakturowania zadania można skonfigurować na karcie **Odpłatne zadania** w pozycji oferty opartej na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Zadania wiersza oferty**.</span><span class="sxs-lookup"><span data-stu-id="a2400-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="a2400-127">Alternatywnie możesz zaktualizować typ rozliczenia dla zadania projektu w polu **Typ fakturowania** w podsiatce w konfiguracji rozliczenia zadania projektu, która pokazuje wiersze oferty skojarzone z zadaniem.</span><span class="sxs-lookup"><span data-stu-id="a2400-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="a2400-128">Aktualizowanie ról projektu jako odpłatnego lub niepłatnego</span><span class="sxs-lookup"><span data-stu-id="a2400-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="a2400-129">W kontekście określonego wiersza oferty opartej na projekcie rola może być odpłatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="a2400-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="a2400-130">Typ fakturowania roli można skonfigurować na karcie **Odpłatne role** w pozycji oferty na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Odpłatne role**.</span><span class="sxs-lookup"><span data-stu-id="a2400-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="a2400-131">Aktualizowanie kategorii transakcji jako odpłatnej lub nie</span><span class="sxs-lookup"><span data-stu-id="a2400-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="a2400-132">Kategoria transakcji w danej pozycji oferty może być płatna lub nieodpłatna.</span><span class="sxs-lookup"><span data-stu-id="a2400-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="a2400-133">Typ fakturowania tranzakcji można skonfigurować na karcie **Odpłatne kategorie** w pozycji oferty na projekcie przez zaktualizowanie pola **Typ fakturowania** w podsiatce **Odpłatne kategorie**.</span><span class="sxs-lookup"><span data-stu-id="a2400-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="a2400-134">Rozwiązywanie odpłatności</span><span class="sxs-lookup"><span data-stu-id="a2400-134">Resolve chargeability</span></span>
<span data-ttu-id="a2400-135">Wartość szacunkowa lub faktycznie utworzona dla czasu będzie uznana za wymagalną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="a2400-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="a2400-136">**Czas** jest zawarty w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="a2400-137">**Rola** jest skonfigurowana jako płatna w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="a2400-138">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="a2400-139">Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest też skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="a2400-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="a2400-140">Szacunek lub wartość rzeczywista utworzona dla wydatku jest uważana za naliczaną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="a2400-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="a2400-141">**Wydatek** jest zawarty w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="a2400-142">**Kategoria transakcji** jest skonfigurowana jako płatna w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="a2400-143">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="a2400-144">Jeśli te trzy rzeczy zostaną spełnione, **Zadanie** jest też skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="a2400-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="a2400-145">Wartość szacunkowa lub faktycznie utworzona dla materiału będzie uznana za wymagalną tylko wtedy, gdy:</span><span class="sxs-lookup"><span data-stu-id="a2400-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="a2400-146">**Materiały** sa zawarte w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="a2400-147">Dla opcji **Zadania uwzględnione** ustawiono wartość **Wybrane zadania** w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="a2400-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="a2400-148">Jeśli te dwie rzeczy zostaną spełnione, **Zadanie** powinno też być skonfigurowane jako opłata.</span><span class="sxs-lookup"><span data-stu-id="a2400-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-149">
                    <strong>Uwzględnia czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="a2400-150">
                    <strong>Uwzględnia wydatek</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="a2400-151">
                    <strong>Uwzględnij materiały</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="a2400-152">
                    <strong>Uwzględnione zadania</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-153">
                    <strong>Rola</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-154">
                    <strong>Kategoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-155">
                    <strong>Zadanie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="a2400-156">
                    <strong>Wpływ opłaty</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-157">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-158">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-159">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-160">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="a2400-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-161">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-162">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-163">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-164">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-165">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-166">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-167">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-168">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-169">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-170">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="a2400-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-171">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-172">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-173">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-174">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-175">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-176">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-177">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-178">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-179">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-180">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="a2400-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-181">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-182">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-183">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-184">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-185">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-186">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-187">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-188">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-189">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-190">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="a2400-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-191">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-192">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-193">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-194">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-195">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-196">Typ fakturowania wartości rzeczywistej materiału: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-197">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-198">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-199">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-200">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="a2400-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-201">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-202">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-203">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-204">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-205">Typ fakturowania wartości rzeczywistej wydatku: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-206">Typ fakturowania wartości rzeczywistej materiału: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-207">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-208">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-209">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-210">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="a2400-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-211">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-212">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-213">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-214">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-215">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-216">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-218">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-219">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-220">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="a2400-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-221">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-222">
                    <strong>Odpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-223">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-224">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-225">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-226">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-228">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-229">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-230">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="a2400-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-231">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-232">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-233">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-234">Fakturowanie wartości rzeczywistej czas: <strong>Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-235">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatny</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-236">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-237">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="a2400-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-239">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-240">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="a2400-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-241">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-242">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-243">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-244">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-245">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-246">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-247">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="a2400-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a2400-249">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-250">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="a2400-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-251">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-252">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-253">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-254">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-255">Typ fakturowania wartości rzeczywistej wydatku: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-256">Typ fakturowania wartości rzeczywistej materiału: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-257">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-258">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="a2400-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-260">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="a2400-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-261">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-262">Odpłatne</span><span class="sxs-lookup"><span data-stu-id="a2400-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-263">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-264">Fakturowanie wartości rzeczywistej czas: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-265">Typ fakturowania wartości rzeczywistej wydatku: Odpłatny</span><span class="sxs-lookup"><span data-stu-id="a2400-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a2400-266">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a2400-267">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a2400-268">Tak</span><span class="sxs-lookup"><span data-stu-id="a2400-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="a2400-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a2400-270">Cały projekt</span><span class="sxs-lookup"><span data-stu-id="a2400-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a2400-271">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a2400-272">
                    <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a2400-273">Nie można ustawić</span><span class="sxs-lookup"><span data-stu-id="a2400-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a2400-274">Fakturowanie wartości rzeczywistej czas: <strong>Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-275">Typ fakturowania wartości rzeczywistej wydatku: <strong> Nieodpłatne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="a2400-276">Typ fakturowania wartości rzeczywistej materiału: <strong> Niedostępne</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a2400-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
