---
title: Omówienie wartości rzeczywistych
description: Ten temat zawiera informacje o wartościach rzeczywistych w projektach.
author: rumant
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
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014669"
---
# <a name="actuals-overview"></a><span data-ttu-id="ea3b0-103">Omówienie wartości rzeczywistych</span><span class="sxs-lookup"><span data-stu-id="ea3b0-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ea3b0-104">Wartości rzeczywiste określają ilość pracy wykonanej w projekcie.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="ea3b0-105">Wartości rzeczywiste projektu mogą być śledzone z powrotem do ich dokumentów źródłowych.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="ea3b0-106">Dokumentami mogą być wpisy czasu, wydatków i arkusza oraz faktury.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Śledzenie wartości rzeczywistych projektu do dokumentów źródłowych](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="ea3b0-108">Przesyłanie wpis czasu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-108">Submitting a time entry</span></span>

<span data-ttu-id="ea3b0-109">W rozwiązaniu PSA podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ea3b0-110">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ea3b0-111">Podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="ea3b0-112">Logika wprowadzania cen domyślnych jest przechowywana w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="ea3b0-113">Wszystkie wartości pól z wpisu czasu są kopiowane do wiersza arkusza.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="ea3b0-114">Te pola zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="ea3b0-115">Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka organizacyjna**, powodują domyślne wprowadzenie właściwej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="ea3b0-116">Chcąc dodać do wpisu niestandardowe pole, którego wartość ma zostać rozpowszechniona do wartości rzeczywistych, należy utworzyć pole w encji Wartości rzeczywiste, a następnie za pomocą mapowań pól skopiować pole z wpisu czasu do wartości rzeczywistej.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="ea3b0-117">Przesyłanie wpisu wydatku</span><span class="sxs-lookup"><span data-stu-id="ea3b0-117">Submitting an expense entry</span></span>

<span data-ttu-id="ea3b0-118">W rozwiązaniu PSA podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ea3b0-119">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ea3b0-120">Podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="ea3b0-121">Logika wprowadzania cen domyślnych dla wydatków bazuje na kategorii wydatków wybranej na stronie **Wpis wydatków**.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="ea3b0-122">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ea3b0-123">Jednak w samej cenie kwota wprowadzona przez użytkownika jest ustawiana bezpośrednio w odpowiednich wierszach arkusza wydatków domyślnie dla kosztów i sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="ea3b0-124">W obecnej wersji rozwiązania PSA we wpisach wydatków nie można wprowadzać domyślnych cen jednostkowych opartych na kategoriach.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="ea3b0-125">Używanie arkuszy wpisów do rejestrowania kosztów</span><span class="sxs-lookup"><span data-stu-id="ea3b0-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="ea3b0-126">W rozwiązaniu PSA arkusze wpisów umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ea3b0-127">Arkusz ma nagłówek, wiersze i akcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="ea3b0-128">Oto kilka scenariuszy, w których można korzystać z arkusza:</span><span class="sxs-lookup"><span data-stu-id="ea3b0-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="ea3b0-129">Trzeba zarejestrować rzeczywiste koszty materiałów i wielkości sprzedaży w projekcie.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="ea3b0-130">Trzeba przenieść wartości rzeczywiste transakcji z innego systemu do PSA.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="ea3b0-131">Trzeba zarejestrować koszty, które wystąpiły w innym systemie, na przykład koszty zaopatrzenia lub podwykonawstwa.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea3b0-132">Korzystając z arkuszów wpisów do tworzenia wartości rzeczywistych, należy wykonać tylko te osoby, które są w pełni świadomi oddziaływania danego projektu na wyniki księgowania.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="ea3b0-133">Wynika to z faktu, że aplikacja nie sprawdza poprawności typu wiersza arkusza ani pokrewnej kalkulacji cen wprowadzonej w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ea3b0-134">Ze względu na wpływ tego typu arkusza należy zachować ostrożność w przypadku osób mających dostęp do tworzenia arkuszy wpisów.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="ea3b0-135">Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-135">Recording actuals based on project events</span></span>

<span data-ttu-id="ea3b0-136">Rozwiązanie PSA rejestruje transakcje finansowe zaistniałe w trakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ea3b0-137">Te transakcje są zapisywane jako **wartości rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="ea3b0-138">W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="ea3b0-139">**Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="ea3b0-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ea3b0-140">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="ea3b0-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ea3b0-141">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="ea3b0-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ea3b0-142">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="ea3b0-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ea3b0-143">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="ea3b0-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ea3b0-144">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="ea3b0-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ea3b0-145">Stała cena</span><span class="sxs-lookup"><span data-stu-id="ea3b0-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ea3b0-146">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="ea3b0-146">Actuals</span></span></th>
<th><span data-ttu-id="ea3b0-147">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="ea3b0-147">Transaction currency</span></span></th>
<th><span data-ttu-id="ea3b0-148">Stała cena</span><span class="sxs-lookup"><span data-stu-id="ea3b0-148">Fixed price</span></span></th>
<th><span data-ttu-id="ea3b0-149">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="ea3b0-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ea3b0-150">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ea3b0-151">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="ea3b0-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-152">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ea3b0-153">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="ea3b0-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ea3b0-154">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ea3b0-155">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-155">Cost actual</span></span></td>
<td><span data-ttu-id="ea3b0-156">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-157">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-158">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ea3b0-159">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-160">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-161">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="ea3b0-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ea3b0-162">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ea3b0-163">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ea3b0-164">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-164">Cost actual</span></span></td>
<td><span data-ttu-id="ea3b0-165">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-166">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-167">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-168">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-169">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-170">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="ea3b0-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ea3b0-171">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-172">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ea3b0-173">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ea3b0-174">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ea3b0-175">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="ea3b0-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ea3b0-176">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-177">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="ea3b0-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-178">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-179">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-180">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-181">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="ea3b0-181">Billed sales</span></span></td>
<td><span data-ttu-id="ea3b0-182">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ea3b0-183">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ea3b0-184">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="ea3b0-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ea3b0-185">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-186">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-187">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-188">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-189">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-190">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="ea3b0-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ea3b0-191">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-192">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ea3b0-193">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ea3b0-194">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ea3b0-195">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="ea3b0-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ea3b0-196">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ea3b0-197">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="ea3b0-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ea3b0-198">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="ea3b0-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ea3b0-199">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-200">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-201">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-202">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="ea3b0-202">Billed sales</span></span></td>
<td><span data-ttu-id="ea3b0-203">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ea3b0-204">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ea3b0-205">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="ea3b0-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ea3b0-206">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-207">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="ea3b0-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ea3b0-208">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-209">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ea3b0-210">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ea3b0-211">**Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="ea3b0-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ea3b0-212">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="ea3b0-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ea3b0-213">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="ea3b0-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ea3b0-214">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="ea3b0-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ea3b0-215">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="ea3b0-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ea3b0-216">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="ea3b0-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ea3b0-217">Stała cena</span><span class="sxs-lookup"><span data-stu-id="ea3b0-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ea3b0-218">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="ea3b0-218">Actuals</span></span></th>
<th><span data-ttu-id="ea3b0-219">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="ea3b0-219">Transaction currency</span></span></th>
<th><span data-ttu-id="ea3b0-220">Stała cena</span><span class="sxs-lookup"><span data-stu-id="ea3b0-220">Fixed price</span></span></th>
<th><span data-ttu-id="ea3b0-221">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="ea3b0-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ea3b0-222">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ea3b0-223">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="ea3b0-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-224">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ea3b0-225">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="ea3b0-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ea3b0-226">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ea3b0-227">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-227">Cost actual</span></span></td>
<td><span data-ttu-id="ea3b0-228">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ea3b0-229">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ea3b0-230">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ea3b0-231">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ea3b0-232">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-233">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="ea3b0-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ea3b0-234">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-235">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="ea3b0-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ea3b0-236">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="ea3b0-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-237">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="ea3b0-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ea3b0-238">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ea3b0-239">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ea3b0-240">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-240">Cost actual</span></span></td>
<td><span data-ttu-id="ea3b0-241">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-242">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-243">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-244">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-245">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-246">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="ea3b0-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ea3b0-247">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="ea3b0-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-248">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="ea3b0-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ea3b0-249">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="ea3b0-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-250">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="ea3b0-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ea3b0-251">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-252">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ea3b0-253">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ea3b0-254">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ea3b0-255">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="ea3b0-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ea3b0-256">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-257">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="ea3b0-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-258">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-259">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ea3b0-260">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-261">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="ea3b0-261">Billed sales</span></span></td>
<td><span data-ttu-id="ea3b0-262">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ea3b0-263">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ea3b0-264">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="ea3b0-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ea3b0-265">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-266">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-267">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-268">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ea3b0-269">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-270">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="ea3b0-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ea3b0-271">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-272">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ea3b0-273">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ea3b0-274">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ea3b0-275">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="ea3b0-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ea3b0-276">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ea3b0-277">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="ea3b0-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ea3b0-278">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="ea3b0-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ea3b0-279">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-280">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ea3b0-281">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-282">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="ea3b0-282">Billed sales</span></span></td>
<td><span data-ttu-id="ea3b0-283">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ea3b0-284">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ea3b0-285">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="ea3b0-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ea3b0-286">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-287">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="ea3b0-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ea3b0-288">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ea3b0-289">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="ea3b0-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ea3b0-290">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="ea3b0-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]