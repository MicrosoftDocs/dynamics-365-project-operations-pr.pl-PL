---
title: Wartości rzeczywiste
description: Ten temat zawiera informacje o wartościach rzeczywistych w projektach.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754388"
---
# <a name="actuals"></a><span data-ttu-id="5af9e-103">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="5af9e-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5af9e-104">Wartości rzeczywiste określają ilość pracy wykonanej w projekcie.</span><span class="sxs-lookup"><span data-stu-id="5af9e-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="5af9e-105">Wartości rzeczywiste projektu mogą być śledzone z powrotem do ich dokumentów źródłowych.</span><span class="sxs-lookup"><span data-stu-id="5af9e-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="5af9e-106">Dokumentami mogą być wpisy czasu, wydatków i arkusza oraz faktury.</span><span class="sxs-lookup"><span data-stu-id="5af9e-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Śledzenie wartości rzeczywistych projektu do dokumentów źródłowych](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="5af9e-108">Przesyłanie wpis czasu</span><span class="sxs-lookup"><span data-stu-id="5af9e-108">Submitting a time entry</span></span>

<span data-ttu-id="5af9e-109">W rozwiązaniu PSA podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="5af9e-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5af9e-110">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="5af9e-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5af9e-111">Podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="5af9e-112">Logika wprowadzania cen domyślnych jest przechowywana w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="5af9e-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="5af9e-113">Wszystkie wartości pól z wpisu czasu są kopiowane do wiersza arkusza.</span><span class="sxs-lookup"><span data-stu-id="5af9e-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="5af9e-114">Te pola zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.</span><span class="sxs-lookup"><span data-stu-id="5af9e-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="5af9e-115">Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka organizacyjna**, powodują domyślne wprowadzenie właściwej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="5af9e-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="5af9e-116">Chcąc dodać do wpisu niestandardowe pole, którego wartość ma zostać rozpowszechniona do wartości rzeczywistych, należy utworzyć pole w encji Wartości rzeczywiste, a następnie za pomocą mapowań pól skopiować pole z wpisu czasu do wartości rzeczywistej.</span><span class="sxs-lookup"><span data-stu-id="5af9e-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="5af9e-117">Przesyłanie wpisu wydatku</span><span class="sxs-lookup"><span data-stu-id="5af9e-117">Submitting an expense entry</span></span>

<span data-ttu-id="5af9e-118">W rozwiązaniu PSA podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="5af9e-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5af9e-119">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="5af9e-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5af9e-120">Podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="5af9e-121">Logika wprowadzania cen domyślnych dla wydatków bazuje na kategorii wydatków wybranej na stronie **Wpis wydatków**.</span><span class="sxs-lookup"><span data-stu-id="5af9e-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="5af9e-122">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="5af9e-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5af9e-123">Jednak w samej cenie kwota wprowadzona przez użytkownika jest ustawiana bezpośrednio w odpowiednich wierszach arkusza wydatków domyślnie dla kosztów i sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="5af9e-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="5af9e-124">W obecnej wersji rozwiązania PSA we wpisach wydatków nie można wprowadzać domyślnych cen jednostkowych opartych na kategoriach.</span><span class="sxs-lookup"><span data-stu-id="5af9e-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="5af9e-125">Używanie dzienników do rejestrowania kosztów</span><span class="sxs-lookup"><span data-stu-id="5af9e-125">Using journals to record costs</span></span>

<span data-ttu-id="5af9e-126">W rozwiązaniu PSA arkusze umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="5af9e-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5af9e-127">Arkusz ma nagłówek, wiersze i akcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="5af9e-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="5af9e-128">Oto kilka scenariuszy, w których można korzystać z arkusza:</span><span class="sxs-lookup"><span data-stu-id="5af9e-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="5af9e-129">Trzeba zarejestrować rzeczywiste koszty materiałów i wielkości sprzedaży w projekcie.</span><span class="sxs-lookup"><span data-stu-id="5af9e-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="5af9e-130">Trzeba przenieść wartości rzeczywiste transakcji z innego systemu do PSA.</span><span class="sxs-lookup"><span data-stu-id="5af9e-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="5af9e-131">Trzeba zarejestrować koszty, które wystąpiły w innym systemie, na przykład koszty zaopatrzenia lub podwykonawstwa.</span><span class="sxs-lookup"><span data-stu-id="5af9e-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="5af9e-132">Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-132">Recording actuals based on project events</span></span>

<span data-ttu-id="5af9e-133">Rozwiązanie PSA rejestruje transakcje finansowe zaistniałe w trakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5af9e-134">Te transakcje są zapisywane jako **wartości rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="5af9e-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="5af9e-135">W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="5af9e-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="5af9e-136">**Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="5af9e-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5af9e-137">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="5af9e-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5af9e-138">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="5af9e-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5af9e-139">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="5af9e-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5af9e-140">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="5af9e-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5af9e-141">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="5af9e-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5af9e-142">Stała cena</span><span class="sxs-lookup"><span data-stu-id="5af9e-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5af9e-143">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="5af9e-143">Actuals</span></span></th>
<th><span data-ttu-id="5af9e-144">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="5af9e-144">Transaction currency</span></span></th>
<th><span data-ttu-id="5af9e-145">Stała cena</span><span class="sxs-lookup"><span data-stu-id="5af9e-145">Fixed price</span></span></th>
<th><span data-ttu-id="5af9e-146">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="5af9e-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5af9e-147">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5af9e-148">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="5af9e-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-149">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5af9e-150">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="5af9e-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5af9e-151">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5af9e-152">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-152">Cost actual</span></span></td>
<td><span data-ttu-id="5af9e-153">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-154">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-155">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5af9e-156">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-157">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-158">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="5af9e-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5af9e-159">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5af9e-160">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5af9e-161">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-161">Cost actual</span></span></td>
<td><span data-ttu-id="5af9e-162">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-163">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-164">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-165">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-166">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-167">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="5af9e-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5af9e-168">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-169">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="5af9e-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5af9e-170">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5af9e-171">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5af9e-172">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="5af9e-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5af9e-173">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-174">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="5af9e-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-175">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-176">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-177">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-178">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="5af9e-178">Billed sales</span></span></td>
<td><span data-ttu-id="5af9e-179">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5af9e-180">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5af9e-181">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="5af9e-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5af9e-182">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-183">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-184">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-185">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-186">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-187">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="5af9e-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5af9e-188">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-189">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="5af9e-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5af9e-190">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5af9e-191">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="5af9e-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5af9e-192">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="5af9e-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5af9e-193">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5af9e-194">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="5af9e-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5af9e-195">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="5af9e-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5af9e-196">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-197">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-198">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-199">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="5af9e-199">Billed sales</span></span></td>
<td><span data-ttu-id="5af9e-200">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5af9e-201">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="5af9e-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5af9e-202">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="5af9e-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5af9e-203">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-204">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="5af9e-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5af9e-205">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-206">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="5af9e-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5af9e-207">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5af9e-208">**Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="5af9e-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5af9e-209">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="5af9e-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5af9e-210">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="5af9e-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5af9e-211">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="5af9e-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5af9e-212">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="5af9e-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5af9e-213">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="5af9e-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5af9e-214">Stała cena</span><span class="sxs-lookup"><span data-stu-id="5af9e-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5af9e-215">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="5af9e-215">Actuals</span></span></th>
<th><span data-ttu-id="5af9e-216">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="5af9e-216">Transaction currency</span></span></th>
<th><span data-ttu-id="5af9e-217">Stała cena</span><span class="sxs-lookup"><span data-stu-id="5af9e-217">Fixed price</span></span></th>
<th><span data-ttu-id="5af9e-218">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="5af9e-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5af9e-219">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5af9e-220">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="5af9e-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-221">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5af9e-222">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="5af9e-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5af9e-223">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5af9e-224">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-224">Cost actual</span></span></td>
<td><span data-ttu-id="5af9e-225">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5af9e-226">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5af9e-227">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5af9e-228">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5af9e-229">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-230">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="5af9e-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5af9e-231">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-232">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="5af9e-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5af9e-233">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="5af9e-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-234">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="5af9e-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5af9e-235">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5af9e-236">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5af9e-237">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-237">Cost actual</span></span></td>
<td><span data-ttu-id="5af9e-238">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-239">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-240">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-241">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-242">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="5af9e-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-243">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="5af9e-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5af9e-244">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="5af9e-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-245">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="5af9e-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5af9e-246">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="5af9e-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-247">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="5af9e-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5af9e-248">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-249">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="5af9e-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5af9e-250">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5af9e-251">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5af9e-252">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="5af9e-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5af9e-253">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-254">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="5af9e-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-255">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-256">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5af9e-257">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-258">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="5af9e-258">Billed sales</span></span></td>
<td><span data-ttu-id="5af9e-259">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5af9e-260">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="5af9e-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5af9e-261">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="5af9e-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5af9e-262">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-263">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-264">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-265">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5af9e-266">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-267">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="5af9e-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5af9e-268">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-269">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="5af9e-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5af9e-270">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5af9e-271">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="5af9e-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5af9e-272">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="5af9e-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5af9e-273">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5af9e-274">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="5af9e-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5af9e-275">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="5af9e-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5af9e-276">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-277">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5af9e-278">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5af9e-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-279">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="5af9e-279">Billed sales</span></span></td>
<td><span data-ttu-id="5af9e-280">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5af9e-281">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="5af9e-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5af9e-282">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="5af9e-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5af9e-283">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-284">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="5af9e-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5af9e-285">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5af9e-286">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="5af9e-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5af9e-287">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="5af9e-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
