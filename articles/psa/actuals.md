---
title: Omówienie wartości rzeczywistych
description: Ten temat zawiera informacje o wartościach rzeczywistych w projektach.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129781"
---
# <a name="actuals-overview"></a><span data-ttu-id="cfea4-103">Omówienie wartości rzeczywistych</span><span class="sxs-lookup"><span data-stu-id="cfea4-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cfea4-104">Wartości rzeczywiste określają ilość pracy wykonanej w projekcie.</span><span class="sxs-lookup"><span data-stu-id="cfea4-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="cfea4-105">Wartości rzeczywiste projektu mogą być śledzone z powrotem do ich dokumentów źródłowych.</span><span class="sxs-lookup"><span data-stu-id="cfea4-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="cfea4-106">Dokumentami mogą być wpisy czasu, wydatków i arkusza oraz faktury.</span><span class="sxs-lookup"><span data-stu-id="cfea4-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Śledzenie wartości rzeczywistych projektu do dokumentów źródłowych](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="cfea4-108">Przesyłanie wpis czasu</span><span class="sxs-lookup"><span data-stu-id="cfea4-108">Submitting a time entry</span></span>

<span data-ttu-id="cfea4-109">W rozwiązaniu PSA podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="cfea4-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cfea4-110">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="cfea4-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cfea4-111">Podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="cfea4-112">Logika wprowadzania cen domyślnych jest przechowywana w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="cfea4-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="cfea4-113">Wszystkie wartości pól z wpisu czasu są kopiowane do wiersza arkusza.</span><span class="sxs-lookup"><span data-stu-id="cfea4-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="cfea4-114">Te pola zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.</span><span class="sxs-lookup"><span data-stu-id="cfea4-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="cfea4-115">Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka organizacyjna**, powodują domyślne wprowadzenie właściwej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="cfea4-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="cfea4-116">Chcąc dodać do wpisu niestandardowe pole, którego wartość ma zostać rozpowszechniona do wartości rzeczywistych, należy utworzyć pole w encji Wartości rzeczywiste, a następnie za pomocą mapowań pól skopiować pole z wpisu czasu do wartości rzeczywistej.</span><span class="sxs-lookup"><span data-stu-id="cfea4-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="cfea4-117">Przesyłanie wpisu wydatku</span><span class="sxs-lookup"><span data-stu-id="cfea4-117">Submitting an expense entry</span></span>

<span data-ttu-id="cfea4-118">W rozwiązaniu PSA podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="cfea4-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cfea4-119">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="cfea4-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cfea4-120">Podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="cfea4-121">Logika wprowadzania cen domyślnych dla wydatków bazuje na kategorii wydatków wybranej na stronie **Wpis wydatków**.</span><span class="sxs-lookup"><span data-stu-id="cfea4-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="cfea4-122">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="cfea4-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="cfea4-123">Jednak w samej cenie kwota wprowadzona przez użytkownika jest ustawiana bezpośrednio w odpowiednich wierszach arkusza wydatków domyślnie dla kosztów i sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="cfea4-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="cfea4-124">W obecnej wersji rozwiązania PSA we wpisach wydatków nie można wprowadzać domyślnych cen jednostkowych opartych na kategoriach.</span><span class="sxs-lookup"><span data-stu-id="cfea4-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="cfea4-125">Używanie arkuszy wpisów do rejestrowania kosztów</span><span class="sxs-lookup"><span data-stu-id="cfea4-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="cfea4-126">W rozwiązaniu PSA arkusze wpisów umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="cfea4-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="cfea4-127">Arkusz ma nagłówek, wiersze i akcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="cfea4-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="cfea4-128">Oto kilka scenariuszy, w których można korzystać z arkusza:</span><span class="sxs-lookup"><span data-stu-id="cfea4-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="cfea4-129">Trzeba zarejestrować rzeczywiste koszty materiałów i wielkości sprzedaży w projekcie.</span><span class="sxs-lookup"><span data-stu-id="cfea4-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="cfea4-130">Trzeba przenieść wartości rzeczywiste transakcji z innego systemu do PSA.</span><span class="sxs-lookup"><span data-stu-id="cfea4-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="cfea4-131">Trzeba zarejestrować koszty, które wystąpiły w innym systemie, na przykład koszty zaopatrzenia lub podwykonawstwa.</span><span class="sxs-lookup"><span data-stu-id="cfea4-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfea4-132">Korzystając z arkuszów wpisów do tworzenia wartości rzeczywistych, należy wykonać tylko te osoby, które są w pełni świadomi oddziaływania danego projektu na wyniki księgowania.</span><span class="sxs-lookup"><span data-stu-id="cfea4-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="cfea4-133">Wynika to z faktu, że aplikacja nie sprawdza poprawności typu wiersza arkusza ani pokrewnej kalkulacji cen wprowadzonej w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="cfea4-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="cfea4-134">Ze względu na wpływ tego typu arkusza należy zachować ostrożność w przypadku osób mających dostęp do tworzenia arkuszy wpisów.</span><span class="sxs-lookup"><span data-stu-id="cfea4-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="cfea4-135">Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-135">Recording actuals based on project events</span></span>

<span data-ttu-id="cfea4-136">Rozwiązanie PSA rejestruje transakcje finansowe zaistniałe w trakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="cfea4-137">Te transakcje są zapisywane jako **wartości rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="cfea4-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="cfea4-138">W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="cfea4-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="cfea4-139">**Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="cfea4-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cfea4-140">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="cfea4-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cfea4-141">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="cfea4-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cfea4-142">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="cfea4-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cfea4-143">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="cfea4-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cfea4-144">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="cfea4-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cfea4-145">Stała cena</span><span class="sxs-lookup"><span data-stu-id="cfea4-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cfea4-146">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="cfea4-146">Actuals</span></span></th>
<th><span data-ttu-id="cfea4-147">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="cfea4-147">Transaction currency</span></span></th>
<th><span data-ttu-id="cfea4-148">Stała cena</span><span class="sxs-lookup"><span data-stu-id="cfea4-148">Fixed price</span></span></th>
<th><span data-ttu-id="cfea4-149">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="cfea4-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cfea4-150">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cfea4-151">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="cfea4-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-152">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cfea4-153">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="cfea4-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cfea4-154">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cfea4-155">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-155">Cost actual</span></span></td>
<td><span data-ttu-id="cfea4-156">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-157">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-158">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="cfea4-159">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-160">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-161">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="cfea4-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cfea4-162">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cfea4-163">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cfea4-164">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-164">Cost actual</span></span></td>
<td><span data-ttu-id="cfea4-165">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-166">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-167">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-168">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-169">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-170">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="cfea4-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cfea4-171">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-172">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="cfea4-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cfea4-173">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cfea4-174">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cfea4-175">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="cfea4-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cfea4-176">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-177">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="cfea4-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-178">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-179">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-180">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-181">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="cfea4-181">Billed sales</span></span></td>
<td><span data-ttu-id="cfea4-182">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cfea4-183">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cfea4-184">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="cfea4-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cfea4-185">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-186">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-187">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-188">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-189">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-190">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="cfea4-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cfea4-191">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-192">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="cfea4-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cfea4-193">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cfea4-194">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="cfea4-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cfea4-195">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="cfea4-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cfea4-196">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cfea4-197">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="cfea4-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cfea4-198">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="cfea4-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cfea4-199">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-200">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-201">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-202">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="cfea4-202">Billed sales</span></span></td>
<td><span data-ttu-id="cfea4-203">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cfea4-204">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="cfea4-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cfea4-205">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="cfea4-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cfea4-206">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-207">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="cfea4-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cfea4-208">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-209">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="cfea4-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cfea4-210">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cfea4-211">**Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="cfea4-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cfea4-212">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="cfea4-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cfea4-213">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="cfea4-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cfea4-214">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="cfea4-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cfea4-215">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="cfea4-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cfea4-216">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="cfea4-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cfea4-217">Stała cena</span><span class="sxs-lookup"><span data-stu-id="cfea4-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cfea4-218">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="cfea4-218">Actuals</span></span></th>
<th><span data-ttu-id="cfea4-219">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="cfea4-219">Transaction currency</span></span></th>
<th><span data-ttu-id="cfea4-220">Stała cena</span><span class="sxs-lookup"><span data-stu-id="cfea4-220">Fixed price</span></span></th>
<th><span data-ttu-id="cfea4-221">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="cfea4-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cfea4-222">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cfea4-223">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="cfea4-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-224">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cfea4-225">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="cfea4-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cfea4-226">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cfea4-227">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-227">Cost actual</span></span></td>
<td><span data-ttu-id="cfea4-228">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cfea4-229">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cfea4-230">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cfea4-231">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cfea4-232">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-233">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="cfea4-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cfea4-234">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-235">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="cfea4-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cfea4-236">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="cfea4-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-237">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="cfea4-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cfea4-238">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cfea4-239">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cfea4-240">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-240">Cost actual</span></span></td>
<td><span data-ttu-id="cfea4-241">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-242">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-243">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-244">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-245">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="cfea4-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-246">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="cfea4-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cfea4-247">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="cfea4-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-248">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="cfea4-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cfea4-249">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="cfea4-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-250">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="cfea4-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cfea4-251">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-252">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="cfea4-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cfea4-253">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cfea4-254">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cfea4-255">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="cfea4-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cfea4-256">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-257">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="cfea4-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-258">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-259">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cfea4-260">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-261">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="cfea4-261">Billed sales</span></span></td>
<td><span data-ttu-id="cfea4-262">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cfea4-263">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="cfea4-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cfea4-264">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="cfea4-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cfea4-265">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-266">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-267">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-268">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cfea4-269">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-270">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="cfea4-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cfea4-271">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-272">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="cfea4-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cfea4-273">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cfea4-274">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="cfea4-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cfea4-275">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="cfea4-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cfea4-276">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cfea4-277">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="cfea4-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cfea4-278">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="cfea4-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cfea4-279">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-280">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cfea4-281">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="cfea4-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-282">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="cfea4-282">Billed sales</span></span></td>
<td><span data-ttu-id="cfea4-283">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cfea4-284">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="cfea4-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cfea4-285">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="cfea4-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cfea4-286">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-287">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="cfea4-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cfea4-288">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cfea4-289">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="cfea4-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cfea4-290">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="cfea4-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
