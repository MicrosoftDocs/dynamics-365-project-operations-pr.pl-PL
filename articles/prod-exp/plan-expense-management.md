---
title: Konfiguracja zarządzania wydatkami
description: W tym artykule opisano kwestie i decyzje, które należy wziąć pod uwagę w procesie planowania, zanim użytkownik skonfiguruje Zarządzanie wydatkami w Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271366"
---
# <a name="configure-expense-management"></a><span data-ttu-id="3e72b-103">Konfiguracja zarządzania wydatkami</span><span class="sxs-lookup"><span data-stu-id="3e72b-103">Configure expense management</span></span>

<span data-ttu-id="3e72b-104">W tym temacie opisano kwestie i decyzje, które należy wziąć pod uwagę w procesie planowania, zanim użytkownik skonfiguruje Zarządzanie wydatkami.</span><span class="sxs-lookup"><span data-stu-id="3e72b-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="3e72b-105">W zarządzaniu wydatkami są przechowywane informacje o metodach płatności, zapotrzebowaniach na wyjazdy raportach o wydatkach, zasadach itp.</span><span class="sxs-lookup"><span data-stu-id="3e72b-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="3e72b-106">Z uwagi na fakt, że podczas planowania konfiguracji w celu zarządzania wydatkami wiele decyzji jest opartych na hierarchiach organizacji i strukturze finansowej, należy odwołać się do tych obszarów w dokumentach planowania.</span><span class="sxs-lookup"><span data-stu-id="3e72b-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="3e72b-107">Wydatki międzyfirmowe</span><span class="sxs-lookup"><span data-stu-id="3e72b-107">Intercompany expenses</span></span>

<span data-ttu-id="3e72b-108">W przypadku włączania kosztów międzyfirmowych można zezwolić firmom i pracownikom na otrzymywanie kosztów w imieniu innego podmiotu prawnego i gromadzenie płatności od podmiotu prawnego w ramach Twojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="3e72b-109">Na przykład pracownik w firmie A wykona projekt dla podmiotu prawnego B, a w projekcie poniesie koszty związane z podróżą.</span><span class="sxs-lookup"><span data-stu-id="3e72b-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="3e72b-110">Jeśli są włączone koszty międzyfirmowe, pracownik będzie mógł zaraportować koszty księgowania kosztów w firmie B, a koszty muszą zostać zapłacone przez firmę prawną. Jeśli organizacja nie ma wielu osób prawnych, nie trzeba włączać kosztów międzyfirmowych.</span><span class="sxs-lookup"><span data-stu-id="3e72b-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="3e72b-111">**Decyzja:** Czy chcesz włączyć koszty międzyfirmowe?</span><span class="sxs-lookup"><span data-stu-id="3e72b-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="3e72b-112">Zarządzanie finansami</span><span class="sxs-lookup"><span data-stu-id="3e72b-112">Financial management</span></span>

<span data-ttu-id="3e72b-113">Zarządzanie wydatkami jest ściśle zintegrowane z zarządzaniem finansami organizacji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="3e72b-114">Wiele konfiguracji w celu zarządzania wydatkami będzie oparte na decyzjach podjętych przez użytkownika o finansach organizacji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="3e72b-115">W poniższych sekcjach przedstawiono różne obszary, które wymagają planowania i podejmowania decyzji na podstawie decyzji finansowych i wytycznych zespołu kierowniczego.</span><span class="sxs-lookup"><span data-stu-id="3e72b-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="3e72b-116">Każdego dnia</span><span class="sxs-lookup"><span data-stu-id="3e72b-116">Per diems</span></span>

<span data-ttu-id="3e72b-117">Należy zdefiniować dzienną dietę pracownika wykorzystywaną w danej organizacji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="3e72b-118">Z uwagi na fakt, że diety zwykle pokrywają koszty, takie jak posiłki, zakwaterowanie i inne koszty dodatkowe, można utworzyć reguły dotyczące diet w danej organizacji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="3e72b-119">stawki dzienne mogą być oparte na porze roku, miejscu podróży lub obydwu tych danych.</span><span class="sxs-lookup"><span data-stu-id="3e72b-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="3e72b-120">Podczas tworzenia reguły diety dziennej można określić, że procent stawki diety będzie wstrzymany, jeśli pracownik otrzymuje dodatkowe posiłki lub usługi.</span><span class="sxs-lookup"><span data-stu-id="3e72b-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="3e72b-121">Można również ustawić przedziały stawek dziennych oraz maksymalne i minimalne godziny, gdy może być zastosowana stawka dzienna do kosztów podróży pracownika.</span><span class="sxs-lookup"><span data-stu-id="3e72b-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="3e72b-122">**Decyzja:**</span><span class="sxs-lookup"><span data-stu-id="3e72b-122">**Decisions:**</span></span>

- <span data-ttu-id="3e72b-123">Domyślne reguły diety dla pierwszego i ostatniego dnia:</span><span class="sxs-lookup"><span data-stu-id="3e72b-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="3e72b-124">Jaka jest minimalna liczba godzin, jaką pracownik może zgłosić w ciągu dnia i czy wciąż otrzyma dietę?</span><span class="sxs-lookup"><span data-stu-id="3e72b-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="3e72b-125">Czy istnieje redukcja kwoty oferowanej za pierwszy lub ostatni dzień?</span><span class="sxs-lookup"><span data-stu-id="3e72b-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="3e72b-126">W przypadku zmniejszenia o ile procent jest zmniejszona dieta?</span><span class="sxs-lookup"><span data-stu-id="3e72b-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3e72b-127">Czy istnieje redukcja kwoty oferowanej za pierwszy lub ostatni dzień, jeśli chodzi o hotel?</span><span class="sxs-lookup"><span data-stu-id="3e72b-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="3e72b-128">W przypadku zmniejszenia o ile procent jest zmniejszona dieta?</span><span class="sxs-lookup"><span data-stu-id="3e72b-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3e72b-129">Czy istnieje redukcja kwoty oferowanej za pierwszy lub ostatni dzień, jeśli chodzi o inne wydatki?</span><span class="sxs-lookup"><span data-stu-id="3e72b-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="3e72b-130">W przypadku zmniejszenia o ile procent jest zmniejszona dieta?</span><span class="sxs-lookup"><span data-stu-id="3e72b-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="3e72b-131">Domyślne reguły diety:</span><span class="sxs-lookup"><span data-stu-id="3e72b-131">Default per diem rules:</span></span>

    - <span data-ttu-id="3e72b-132">Czy istnieje procentowa redukcja diety na posiłek, jeśli np. posiłek jest bezpłatny?</span><span class="sxs-lookup"><span data-stu-id="3e72b-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="3e72b-133">W przypadku zmniejszenia, o ile procent jest zmniejszona dieta za każdy posiłek?</span><span class="sxs-lookup"><span data-stu-id="3e72b-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="3e72b-134">Czy zmniejszenie posiłku jest obliczane na dzień, na podróż czy zależnie od liczby dań dziennie?</span><span class="sxs-lookup"><span data-stu-id="3e72b-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="3e72b-135">Czy kwoty diety powinny być zaokrąglane w zwykły sposób, czy zaokrąglane w górę?</span><span class="sxs-lookup"><span data-stu-id="3e72b-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="3e72b-136">Czy diety są obliczane w ramach okresu 24 godzin lub w ramach dnia kalendarzowego?</span><span class="sxs-lookup"><span data-stu-id="3e72b-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="3e72b-137">Reguły diety oparte na lokalizacji:</span><span class="sxs-lookup"><span data-stu-id="3e72b-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="3e72b-138">Czy stawki diety są różne, zależnie od lokalizacji?</span><span class="sxs-lookup"><span data-stu-id="3e72b-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="3e72b-139">Jakie lokalizacje są uwzględnione?</span><span class="sxs-lookup"><span data-stu-id="3e72b-139">What locations are included?</span></span>
    - <span data-ttu-id="3e72b-140">Jeśli stawki diety są różne w zależności od lokalizacji, dla każdej lokalizacji jest podawana procentowa kwota dla następujących typów kosztów:</span><span class="sxs-lookup"><span data-stu-id="3e72b-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="3e72b-141">Posiłki</span><span class="sxs-lookup"><span data-stu-id="3e72b-141">Meals</span></span>
        - <span data-ttu-id="3e72b-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="3e72b-142">Hotel</span></span>
        - <span data-ttu-id="3e72b-143">Inne wydatki</span><span class="sxs-lookup"><span data-stu-id="3e72b-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="3e72b-144">Dzienniki zarządzania wydatkami i konta</span><span class="sxs-lookup"><span data-stu-id="3e72b-144">Expense management journals and accounts</span></span>

<span data-ttu-id="3e72b-145">Do zarządzania wydatkami jest wymagane użycie wielu arkuszy i kont.</span><span class="sxs-lookup"><span data-stu-id="3e72b-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="3e72b-146">Należy zdecydować, na przykład, czy to same konto jest używane w przypadku zaliczek gotówkowych i sporów związanych z kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="3e72b-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="3e72b-147">**Decyzja:**</span><span class="sxs-lookup"><span data-stu-id="3e72b-147">**Decisions:**</span></span>

- <span data-ttu-id="3e72b-148">Które arkusze księgi otrzymują zaksięgowane arkusze z wydatków?</span><span class="sxs-lookup"><span data-stu-id="3e72b-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="3e72b-149">Które konto jest używane na potrzeby zaliczek?</span><span class="sxs-lookup"><span data-stu-id="3e72b-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="3e72b-150">Czy zaliczki gotówkowe mają być od razu księgowane?</span><span class="sxs-lookup"><span data-stu-id="3e72b-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="3e72b-151">Formy płatności</span><span class="sxs-lookup"><span data-stu-id="3e72b-151">Payment methods</span></span>

<span data-ttu-id="3e72b-152">W przypadku umożliwienia pracownikom ponoszenia kosztów w imieniu firmy należy zdefiniować metody płatności, które mogą być używane przez pracowników.</span><span class="sxs-lookup"><span data-stu-id="3e72b-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="3e72b-153">Użytkownik może na przykład zezwolić pracownikom na korzystanie z gotówki lub firmowej karty kredytowej.</span><span class="sxs-lookup"><span data-stu-id="3e72b-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="3e72b-154">Użytkownik może również zezwolić pracownikom na korzystanie z osobistych kart kredytowych, a następnie zwracać im koszty.</span><span class="sxs-lookup"><span data-stu-id="3e72b-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="3e72b-155">Konieczne jest podjęcie następujących decyzji dla każdej dozwolonej metody płatności.</span><span class="sxs-lookup"><span data-stu-id="3e72b-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="3e72b-156">**Decyzja:**</span><span class="sxs-lookup"><span data-stu-id="3e72b-156">**Decisions:**</span></span>

- <span data-ttu-id="3e72b-157">Jakie formy płatności są dozwolone?</span><span class="sxs-lookup"><span data-stu-id="3e72b-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="3e72b-158">Do kogo jest przypisana forma płatności?</span><span class="sxs-lookup"><span data-stu-id="3e72b-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="3e72b-159">Czy istnieje typ konta rozliczeniowego?</span><span class="sxs-lookup"><span data-stu-id="3e72b-159">Is there an offset account type?</span></span> <span data-ttu-id="3e72b-160">Jeśli istnieje typ konta rozliczeniowego, to jaki jest?</span><span class="sxs-lookup"><span data-stu-id="3e72b-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="3e72b-161">Jeśli istnieje typ konta rozliczeniowego, to co to za konto?</span><span class="sxs-lookup"><span data-stu-id="3e72b-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="3e72b-162">Jeśli forma płatności to karta kredytowa, czy metoda płatności ma być używana tylko wraz z importowanymi transakcjami?</span><span class="sxs-lookup"><span data-stu-id="3e72b-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="3e72b-163">Kategorie wydatków i dzielone kategorie</span><span class="sxs-lookup"><span data-stu-id="3e72b-163">Expense categories and shared categories</span></span>

<span data-ttu-id="3e72b-164">Kiedy pracownicy tworzą raport o wydatkach, każdy z tych rekordów musi być skojarzony z kategorią wydatku.</span><span class="sxs-lookup"><span data-stu-id="3e72b-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="3e72b-165">Kategorie wydatków są pobierane z kategorii udostępnionych, które mogą być współużytkowane przez osoby prawne należące do organizacji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="3e72b-166">Te kategorie mogą być również udostępniane w programie Project Management and Accounting w zależności od sposobu pracy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="3e72b-167">W zależności od definicji organizacji i wskazówek dotyczących zespołu implementacji należy określić, czy kategorie używane w zarządzaniu wydatkami będą używane tylko w zarządzaniu wydatkami, czy powinny być wspólne dla zarządzania projektem i księgowania oraz zarządzania wydatkami.</span><span class="sxs-lookup"><span data-stu-id="3e72b-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="3e72b-168">Należy pamiętać, że kategorie te mogą być współużytkowane przez zarządzanie projektami oraz zarządzanie wydatkami i kosztami, a także między zarządzaniem projektami oraz ich księgowaniem i produkcją, ale nie pomiędzy wydatkami a produkcją.</span><span class="sxs-lookup"><span data-stu-id="3e72b-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="3e72b-169">Konieczne jest podjęcie następujących decyzji dla każdej kategorii wydatku.</span><span class="sxs-lookup"><span data-stu-id="3e72b-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="3e72b-170">**Decyzja:**</span><span class="sxs-lookup"><span data-stu-id="3e72b-170">**Decisions:**</span></span>

- <span data-ttu-id="3e72b-171">Jaka jest kategoria wydatków?</span><span class="sxs-lookup"><span data-stu-id="3e72b-171">What is the expense category?</span></span> <span data-ttu-id="3e72b-172">Mogą to być np. kategorie dla lotów, hotelu lub trasy.</span><span class="sxs-lookup"><span data-stu-id="3e72b-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="3e72b-173">Czy kategoria wydatków może być używana także w zarządzaniu projektami i księgowaniu?</span><span class="sxs-lookup"><span data-stu-id="3e72b-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="3e72b-174">Jaki jest typ wydatków?</span><span class="sxs-lookup"><span data-stu-id="3e72b-174">What is the expense type?</span></span>
- <span data-ttu-id="3e72b-175">Jaka jest domyślna metoda płatności dla tej kategorii wydatków?</span><span class="sxs-lookup"><span data-stu-id="3e72b-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="3e72b-176">Czy wydatki w tej kategorii muszą zostać wyszczególnione?</span><span class="sxs-lookup"><span data-stu-id="3e72b-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="3e72b-177">Jaka jest główne domyślne konto dla tej kategorii wydatków?</span><span class="sxs-lookup"><span data-stu-id="3e72b-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="3e72b-178">Jaka jest domyślna grupa podatków od sprzedaży w danej kategorii wydatku?</span><span class="sxs-lookup"><span data-stu-id="3e72b-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="3e72b-179">Czy dla kategorii wydatków są dozwolone dodatkowe formy płatności?</span><span class="sxs-lookup"><span data-stu-id="3e72b-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="3e72b-180">Czy jeśli są dozwolone dodatkowe formy płatności, to jakie?</span><span class="sxs-lookup"><span data-stu-id="3e72b-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="3e72b-181">Czy w tej kategorii wydatków znajdują się podkategorie?</span><span class="sxs-lookup"><span data-stu-id="3e72b-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="3e72b-182">Jeśli tak, to należy także podjąć następujące decyzje:</span><span class="sxs-lookup"><span data-stu-id="3e72b-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="3e72b-183">Czy któraś z podkategorii jest wykluczona ze zwrotu podatku?</span><span class="sxs-lookup"><span data-stu-id="3e72b-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="3e72b-184">Jaka jest grupa podatku od sprzedaży w tych podkategoriach?</span><span class="sxs-lookup"><span data-stu-id="3e72b-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="3e72b-185">Jeśli kategoria wydatków jest używana także w zarządzaniu projektami i księgowaniu, odpowiedz na pozostałe pytania.</span><span class="sxs-lookup"><span data-stu-id="3e72b-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="3e72b-186">W przeciwnym razie przejdź do następnej sekcji.</span><span class="sxs-lookup"><span data-stu-id="3e72b-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="3e72b-187">Które konta kosztów będą używane w następujących wydatkach?</span><span class="sxs-lookup"><span data-stu-id="3e72b-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="3e72b-188">Koszt</span><span class="sxs-lookup"><span data-stu-id="3e72b-188">Cost</span></span>
    - <span data-ttu-id="3e72b-189">Alokacja płac</span><span class="sxs-lookup"><span data-stu-id="3e72b-189">Payroll allocation</span></span>
    - <span data-ttu-id="3e72b-190">PWT-koszt wartość</span><span class="sxs-lookup"><span data-stu-id="3e72b-190">WIP-cost value</span></span>
    - <span data-ttu-id="3e72b-191">Koszt przedmiotu</span><span class="sxs-lookup"><span data-stu-id="3e72b-191">Cost-item</span></span>
    - <span data-ttu-id="3e72b-192">PWT-koszt wartość-przedmiotu</span><span class="sxs-lookup"><span data-stu-id="3e72b-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="3e72b-193">Naliczona strata</span><span class="sxs-lookup"><span data-stu-id="3e72b-193">Accrued loss</span></span>
    - <span data-ttu-id="3e72b-194">PWT-naliczona strata</span><span class="sxs-lookup"><span data-stu-id="3e72b-194">WIP-accrued loss</span></span>

- <span data-ttu-id="3e72b-195">Które konta przychodów będą używane w następujących kategoriach?</span><span class="sxs-lookup"><span data-stu-id="3e72b-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="3e72b-196">Zafakturowany przychód</span><span class="sxs-lookup"><span data-stu-id="3e72b-196">Invoiced revenue</span></span>
    - <span data-ttu-id="3e72b-197">Naliczony przychód — wartość sprzedaży</span><span class="sxs-lookup"><span data-stu-id="3e72b-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="3e72b-198">PWT — wartość sprzedaży</span><span class="sxs-lookup"><span data-stu-id="3e72b-198">WIP-sales value</span></span>
    - <span data-ttu-id="3e72b-199">Naliczony przychód — produkcja</span><span class="sxs-lookup"><span data-stu-id="3e72b-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="3e72b-200">PWT-produkcja</span><span class="sxs-lookup"><span data-stu-id="3e72b-200">WIP-production</span></span>
    - <span data-ttu-id="3e72b-201">Naliczony przychód — zysk</span><span class="sxs-lookup"><span data-stu-id="3e72b-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="3e72b-202">PWT-zysk</span><span class="sxs-lookup"><span data-stu-id="3e72b-202">WIP-profit</span></span>
    - <span data-ttu-id="3e72b-203">Naliczony przychód — subskrypcja</span><span class="sxs-lookup"><span data-stu-id="3e72b-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="3e72b-204">PWT-subskrypcja</span><span class="sxs-lookup"><span data-stu-id="3e72b-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="3e72b-205">Podatki</span><span class="sxs-lookup"><span data-stu-id="3e72b-205">Taxes</span></span>

<span data-ttu-id="3e72b-206">W przypadku podatków powiązanych z wydatkami należy określić, co ma zostać uwzględnione lub włączone w raportach o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="3e72b-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="3e72b-207">**Decyzja:**</span><span class="sxs-lookup"><span data-stu-id="3e72b-207">**Decisions:**</span></span>

- <span data-ttu-id="3e72b-208">Czy kwoty wydatków uwzględniają podatki?</span><span class="sxs-lookup"><span data-stu-id="3e72b-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="3e72b-209">Czy ma być włączone odzyskiwanie podatku z wydatków?</span><span class="sxs-lookup"><span data-stu-id="3e72b-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e72b-210">Po zaplanowaniu księgi głównej, jeśli postanowiono stosować amerykańskie stawki podatku i używajać reguł podatkowych, nie można włączyć zwrotu podatku na pokrycie kosztów.</span><span class="sxs-lookup"><span data-stu-id="3e72b-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="3e72b-211">(Aby zastosować amerykańskie reguły podatkowe i podatek amerykański, należy ustawić opcję **Stosowanie reguł opodatkowania podatku** na **Tak**.)</span><span class="sxs-lookup"><span data-stu-id="3e72b-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="3e72b-212">Zasady</span><span class="sxs-lookup"><span data-stu-id="3e72b-212">Policies</span></span>

<span data-ttu-id="3e72b-213">Tworząc zasady raportów o wydatkach, można pomóc organizacji w zaoszczędzeniu czasu i pieniędzy w momencie, gdy pracownicy ponoszą koszty w jej imieniu.</span><span class="sxs-lookup"><span data-stu-id="3e72b-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="3e72b-214">Zasady pomagają zagwarantować, że pracownicy nie przekroczą budżetu, pomagają udostępniać wszystkie wymagane informacje i wydawać pieniądze wyłącznie wtedy, gdy rzeczywiście trzeba.</span><span class="sxs-lookup"><span data-stu-id="3e72b-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="3e72b-215">Konieczne jest podjęcie następujących decyzji dla każdej zasady raportu dotyczącego wydatków oraz wszystkich utworzonych przez użytkownika zasad zatwierdzania raportów o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="3e72b-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="3e72b-216">**Decyzja:**</span><span class="sxs-lookup"><span data-stu-id="3e72b-216">**Decisions:**</span></span>

- <span data-ttu-id="3e72b-217">Jaka jest nazwa zasady?</span><span class="sxs-lookup"><span data-stu-id="3e72b-217">What is the name of the policy?</span></span>
- <span data-ttu-id="3e72b-218">Czego dotyczy zasada wydatków?</span><span class="sxs-lookup"><span data-stu-id="3e72b-218">What is the expense policy for?</span></span>
- <span data-ttu-id="3e72b-219">Jeśli zdecydowano się na włączenie kosztów międzyfirmowych, które firmy z organizacji będą stosować te zasady?</span><span class="sxs-lookup"><span data-stu-id="3e72b-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="3e72b-220">Kiedy zasady wejdą w życie?</span><span class="sxs-lookup"><span data-stu-id="3e72b-220">When does the policy become effective?</span></span>
- <span data-ttu-id="3e72b-221">Kiedy zasady wygasną?</span><span class="sxs-lookup"><span data-stu-id="3e72b-221">When does the policy expire?</span></span>
- <span data-ttu-id="3e72b-222">Czym jest reguła zasad?</span><span class="sxs-lookup"><span data-stu-id="3e72b-222">What is the policy rule?</span></span>
- <span data-ttu-id="3e72b-223">Jaki jest wynik reguły zasad?</span><span class="sxs-lookup"><span data-stu-id="3e72b-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]