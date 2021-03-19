---
title: Wartości rzeczywiste
description: Ten temat zawiera informacje dotyczące pracy z wartościami rzeczywistymi w rozwiązaniu Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291812"
---
# <a name="actuals"></a><span data-ttu-id="94403-103">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="94403-103">Actuals</span></span> 

<span data-ttu-id="94403-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="94403-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="94403-105">Wartości rzeczywiste określają ilość pracy wykonanej w projekcie.</span><span class="sxs-lookup"><span data-stu-id="94403-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="94403-106">Są one tworzone w wyniku zapisów czasu i wydatku oraz pozycji dziennika i faktur.</span><span class="sxs-lookup"><span data-stu-id="94403-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="94403-107">Wiersze arkusza i przesyłanie czasu</span><span class="sxs-lookup"><span data-stu-id="94403-107">Journal lines and time submission</span></span>

<span data-ttu-id="94403-108">Aby uzyskać więcej informacji o wprowadzaniu godziny, zobacz temat [Przegląd wpisów czasu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="94403-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="94403-109">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="94403-109">Time and materials</span></span>

<span data-ttu-id="94403-110">W przypadku połączenia przesłanego wpisu czasu do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.</span><span class="sxs-lookup"><span data-stu-id="94403-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="94403-111">Stała cena</span><span class="sxs-lookup"><span data-stu-id="94403-111">Fixed price</span></span>

<span data-ttu-id="94403-112">Podczas przesyłania wpisu czasu dla projektu, który jest połączony z projektem zamapowanym do kontraktu o stałej cenie, system tworzy tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="94403-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="94403-113">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="94403-113">Default pricing</span></span>

<span data-ttu-id="94403-114">Logika tworzenia cen domyślnych jest przechowywana w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="94403-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="94403-115">Wartości pól z wpisu czasu są kopiowane do wiersza arkusza.</span><span class="sxs-lookup"><span data-stu-id="94403-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="94403-116">Te wartości zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.</span><span class="sxs-lookup"><span data-stu-id="94403-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="94403-117">Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka organizacyjna**, są wykorzystywane do domyślnego wprowadzenia właściwej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="94403-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="94403-118">We wpisie czasu można dodać pole niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="94403-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="94403-119">Chcąc przetworzyć wartość do wartości rzeczywistych, należy utworzyć pole w encji Wartości rzeczywiste, a następnie za pomocą mapowań pól skopiować pole z wpisu czasu do wartości rzeczywistej.</span><span class="sxs-lookup"><span data-stu-id="94403-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="94403-120">Wiersze arkusza i przesyłanie podstawowych kosztów</span><span class="sxs-lookup"><span data-stu-id="94403-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="94403-121">Aby uzyskać więcej informacji o wprowadzaniu wydatków, zobacz temat [Przegląd wydatków](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="94403-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="94403-122">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="94403-122">Time and materials</span></span>

<span data-ttu-id="94403-123">W przypadku połączenia przesłanego wpisu wydatku podstawowego do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.</span><span class="sxs-lookup"><span data-stu-id="94403-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="94403-124">Stała cena</span><span class="sxs-lookup"><span data-stu-id="94403-124">Fixed price</span></span>

<span data-ttu-id="94403-125">Podczas przesyłania wpisu podstawowego wydatku dla projektu, który jest połączony z projektem zamapowanym do kontraktu o stałej cenie, system tworzy tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="94403-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="94403-126">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="94403-126">Default pricing</span></span>

<span data-ttu-id="94403-127">Logika wprowadzania cen domyślnych wydatków jest oparta na kategorii wydatków.</span><span class="sxs-lookup"><span data-stu-id="94403-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="94403-128">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="94403-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="94403-129">Jednak domyślnie kwota wprowadzona przez użytkownika dla ceny jest ustawiana bezpośrednio w odpowiednich wierszach arkusza wydatków dla kosztów i sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="94403-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="94403-130">We wpisach wydatków nie można wprowadzać domyślnych cen jednostkowych opartych na kategoriach.</span><span class="sxs-lookup"><span data-stu-id="94403-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="94403-131">Używanie dzienników do rejestrowania kosztów</span><span class="sxs-lookup"><span data-stu-id="94403-131">Use entry journals to record costs</span></span>

<span data-ttu-id="94403-132">Arkusze umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="94403-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="94403-133">Arkusze mogą być używane w produkcji.</span><span class="sxs-lookup"><span data-stu-id="94403-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="94403-134">Rejestrowania rzeczywistych kosztów materiałów i wielkości sprzedaży w projekcie.</span><span class="sxs-lookup"><span data-stu-id="94403-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="94403-135">Przenieś wartości rzeczywiste transakcji z innego systemu do rozwiązaniu Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="94403-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="94403-136">Zarejestrowania kosztów, które wystąpiły w innym systemie.</span><span class="sxs-lookup"><span data-stu-id="94403-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="94403-137">Koszty te mogą zawierać koszty zakupu lub podwykonawców.</span><span class="sxs-lookup"><span data-stu-id="94403-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94403-138">Aplikacja nie sprawdza poprawności typu wiersza arkusza lub powiązanej kalkulacji cen wprowadzonych w wierszu dziennika.</span><span class="sxs-lookup"><span data-stu-id="94403-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="94403-139">Z tego powodu tylko użytkownik, który jest w pełni świadomi skutków związanych z księgowaniem w projekcie powinien używać dzienników wpisów do tworzenia wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="94403-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="94403-140">Ze względu na wpływ danego typu arkusza należy starannie wybrać osoby, które mają mieć dostęp do tworzenia arkuszy zapisu.</span><span class="sxs-lookup"><span data-stu-id="94403-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="94403-141">Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu</span><span class="sxs-lookup"><span data-stu-id="94403-141">Record actuals based on project events</span></span>

<span data-ttu-id="94403-142">Project Operations rejestruje transakcje finansowe zaistniałe w trakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="94403-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="94403-143">Te transakcje są zapisywane jako wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="94403-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="94403-144">W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="94403-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="94403-145">Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu</span><span class="sxs-lookup"><span data-stu-id="94403-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="94403-146">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="94403-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="94403-147">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="94403-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="94403-148">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="94403-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="94403-149">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="94403-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="94403-150">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="94403-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="94403-151">Stała cena</span><span class="sxs-lookup"><span data-stu-id="94403-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="94403-152">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="94403-152">Actuals</span></span></th>
<th><span data-ttu-id="94403-153">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="94403-153">Transaction currency</span></span></th>
<th><span data-ttu-id="94403-154">Stała cena</span><span class="sxs-lookup"><span data-stu-id="94403-154">Fixed price</span></span></th>
<th><span data-ttu-id="94403-155">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="94403-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94403-156">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="94403-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="94403-157">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="94403-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-158">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="94403-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="94403-159">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="94403-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94403-160">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94403-161">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-161">Cost actual</span></span></td>
<td><span data-ttu-id="94403-162">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-163">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-164">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="94403-165">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-166">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-167">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="94403-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="94403-168">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94403-169">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94403-170">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-170">Cost actual</span></span></td>
<td><span data-ttu-id="94403-171">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-172">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-173">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-174">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-175">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-176">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="94403-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94403-177">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-178">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="94403-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94403-179">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94403-180">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94403-181">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="94403-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94403-182">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-183">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="94403-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-184">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-185">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-186">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-187">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="94403-187">Billed sales</span></span></td>
<td><span data-ttu-id="94403-188">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94403-189">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94403-190">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="94403-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94403-191">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-192">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-193">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-194">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-195">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-196">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="94403-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94403-197">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-198">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="94403-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94403-199">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94403-200">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="94403-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94403-201">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="94403-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94403-202">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="94403-203">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="94403-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="94403-204">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="94403-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="94403-205">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-206">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-207">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-208">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="94403-208">Billed sales</span></span></td>
<td><span data-ttu-id="94403-209">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94403-210">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="94403-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94403-211">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="94403-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94403-212">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-213">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="94403-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="94403-214">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-215">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="94403-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="94403-216">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="94403-217">Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu</span><span class="sxs-lookup"><span data-stu-id="94403-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="94403-218">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="94403-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="94403-219">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="94403-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="94403-220">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="94403-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="94403-221">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="94403-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="94403-222">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="94403-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="94403-223">Stała cena</span><span class="sxs-lookup"><span data-stu-id="94403-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="94403-224">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="94403-224">Actuals</span></span></th>
<th><span data-ttu-id="94403-225">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="94403-225">Transaction currency</span></span></th>
<th><span data-ttu-id="94403-226">Stała cena</span><span class="sxs-lookup"><span data-stu-id="94403-226">Fixed price</span></span></th>
<th><span data-ttu-id="94403-227">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="94403-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94403-228">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="94403-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="94403-229">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="94403-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-230">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="94403-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="94403-231">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="94403-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="94403-232">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94403-233">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-233">Cost actual</span></span></td>
<td><span data-ttu-id="94403-234">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="94403-235">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="94403-236">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="94403-237">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="94403-238">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-239">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="94403-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="94403-240">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-241">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="94403-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="94403-242">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="94403-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-243">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="94403-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="94403-244">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="94403-245">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94403-246">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-246">Cost actual</span></span></td>
<td><span data-ttu-id="94403-247">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-248">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-249">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-250">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-251">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="94403-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-252">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="94403-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="94403-253">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="94403-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-254">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="94403-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="94403-255">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="94403-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-256">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="94403-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94403-257">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-258">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="94403-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94403-259">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94403-260">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94403-261">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="94403-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94403-262">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-263">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="94403-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-264">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-265">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="94403-266">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-267">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="94403-267">Billed sales</span></span></td>
<td><span data-ttu-id="94403-268">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94403-269">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="94403-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94403-270">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="94403-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94403-271">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-272">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-273">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-274">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94403-275">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-276">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="94403-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94403-277">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-278">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="94403-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94403-279">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94403-280">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="94403-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94403-281">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="94403-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94403-282">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="94403-283">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="94403-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="94403-284">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="94403-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="94403-285">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-286">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="94403-287">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="94403-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-288">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="94403-288">Billed sales</span></span></td>
<td><span data-ttu-id="94403-289">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94403-290">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="94403-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94403-291">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="94403-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94403-292">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-293">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="94403-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="94403-294">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94403-295">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="94403-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="94403-296">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="94403-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]