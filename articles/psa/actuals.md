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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146136"
---
# <a name="actuals-overview"></a><span data-ttu-id="4d8f2-103">Omówienie wartości rzeczywistych</span><span class="sxs-lookup"><span data-stu-id="4d8f2-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4d8f2-104">Wartości rzeczywiste określają ilość pracy wykonanej w projekcie.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="4d8f2-105">Wartości rzeczywiste projektu mogą być śledzone z powrotem do ich dokumentów źródłowych.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="4d8f2-106">Dokumentami mogą być wpisy czasu, wydatków i arkusza oraz faktury.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Śledzenie wartości rzeczywistych projektu do dokumentów źródłowych](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="4d8f2-108">Przesyłanie wpis czasu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-108">Submitting a time entry</span></span>

<span data-ttu-id="4d8f2-109">W rozwiązaniu PSA podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="4d8f2-110">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="4d8f2-111">Podczas przesyłania wpisu czasu dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="4d8f2-112">Logika wprowadzania cen domyślnych jest przechowywana w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="4d8f2-113">Wszystkie wartości pól z wpisu czasu są kopiowane do wiersza arkusza.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="4d8f2-114">Te pola zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="4d8f2-115">Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka organizacyjna**, powodują domyślne wprowadzenie właściwej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="4d8f2-116">Chcąc dodać do wpisu niestandardowe pole, którego wartość ma zostać rozpowszechniona do wartości rzeczywistych, należy utworzyć pole w encji Wartości rzeczywiste, a następnie za pomocą mapowań pól skopiować pole z wpisu czasu do wartości rzeczywistej.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="4d8f2-117">Przesyłanie wpisu wydatku</span><span class="sxs-lookup"><span data-stu-id="4d8f2-117">Submitting an expense entry</span></span>

<span data-ttu-id="4d8f2-118">W rozwiązaniu PSA podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu rozliczanego według czasu i materiałów, są tworzone dwa wiersze arkusza.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="4d8f2-119">Jeden wiersz jest przeznaczony dla kosztu, a drugi dla nierozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="4d8f2-120">Podczas przesyłania wpisu wydatku dla projektu, który jest zamapowany na wiersz kontraktu o stałej cenie, jest tworzony tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="4d8f2-121">Logika wprowadzania cen domyślnych dla wydatków bazuje na kategorii wydatków wybranej na stronie **Wpis wydatków**.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="4d8f2-122">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="4d8f2-123">Jednak w samej cenie kwota wprowadzona przez użytkownika jest ustawiana bezpośrednio w odpowiednich wierszach arkusza wydatków domyślnie dla kosztów i sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="4d8f2-124">W obecnej wersji rozwiązania PSA we wpisach wydatków nie można wprowadzać domyślnych cen jednostkowych opartych na kategoriach.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="4d8f2-125">Używanie arkuszy wpisów do rejestrowania kosztów</span><span class="sxs-lookup"><span data-stu-id="4d8f2-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="4d8f2-126">W rozwiązaniu PSA arkusze wpisów umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="4d8f2-127">Arkusz ma nagłówek, wiersze i akcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="4d8f2-128">Oto kilka scenariuszy, w których można korzystać z arkusza:</span><span class="sxs-lookup"><span data-stu-id="4d8f2-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="4d8f2-129">Trzeba zarejestrować rzeczywiste koszty materiałów i wielkości sprzedaży w projekcie.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="4d8f2-130">Trzeba przenieść wartości rzeczywiste transakcji z innego systemu do PSA.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="4d8f2-131">Trzeba zarejestrować koszty, które wystąpiły w innym systemie, na przykład koszty zaopatrzenia lub podwykonawstwa.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d8f2-132">Korzystając z arkuszów wpisów do tworzenia wartości rzeczywistych, należy wykonać tylko te osoby, które są w pełni świadomi oddziaływania danego projektu na wyniki księgowania.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="4d8f2-133">Wynika to z faktu, że aplikacja nie sprawdza poprawności typu wiersza arkusza ani pokrewnej kalkulacji cen wprowadzonej w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="4d8f2-134">Ze względu na wpływ tego typu arkusza należy zachować ostrożność w przypadku osób mających dostęp do tworzenia arkuszy wpisów.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="4d8f2-135">Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-135">Recording actuals based on project events</span></span>

<span data-ttu-id="4d8f2-136">Rozwiązanie PSA rejestruje transakcje finansowe zaistniałe w trakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="4d8f2-137">Te transakcje są zapisywane jako **wartości rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="4d8f2-138">W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="4d8f2-139">**Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="4d8f2-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4d8f2-140">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="4d8f2-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4d8f2-141">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="4d8f2-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4d8f2-142">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="4d8f2-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4d8f2-143">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="4d8f2-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4d8f2-144">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="4d8f2-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4d8f2-145">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4d8f2-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4d8f2-146">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4d8f2-146">Actuals</span></span></th>
<th><span data-ttu-id="4d8f2-147">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4d8f2-147">Transaction currency</span></span></th>
<th><span data-ttu-id="4d8f2-148">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4d8f2-148">Fixed price</span></span></th>
<th><span data-ttu-id="4d8f2-149">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4d8f2-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4d8f2-150">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4d8f2-151">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4d8f2-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-152">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4d8f2-153">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4d8f2-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4d8f2-154">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4d8f2-155">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-155">Cost actual</span></span></td>
<td><span data-ttu-id="4d8f2-156">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-157">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-158">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="4d8f2-159">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-160">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-161">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="4d8f2-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4d8f2-162">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4d8f2-163">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4d8f2-164">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-164">Cost actual</span></span></td>
<td><span data-ttu-id="4d8f2-165">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-166">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-167">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-168">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-169">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-170">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4d8f2-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4d8f2-171">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-172">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4d8f2-173">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4d8f2-174">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4d8f2-175">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4d8f2-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4d8f2-176">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-177">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4d8f2-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-178">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-179">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-180">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-181">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4d8f2-181">Billed sales</span></span></td>
<td><span data-ttu-id="4d8f2-182">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4d8f2-183">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4d8f2-184">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4d8f2-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4d8f2-185">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-186">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-187">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-188">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-189">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-190">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4d8f2-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4d8f2-191">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-192">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4d8f2-193">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4d8f2-194">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4d8f2-195">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4d8f2-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4d8f2-196">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4d8f2-197">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4d8f2-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4d8f2-198">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="4d8f2-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4d8f2-199">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-200">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-201">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-202">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4d8f2-202">Billed sales</span></span></td>
<td><span data-ttu-id="4d8f2-203">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4d8f2-204">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4d8f2-205">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4d8f2-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4d8f2-206">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-207">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4d8f2-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4d8f2-208">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-209">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4d8f2-210">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4d8f2-211">**Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu**</span><span class="sxs-lookup"><span data-stu-id="4d8f2-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4d8f2-212">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="4d8f2-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4d8f2-213">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="4d8f2-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4d8f2-214">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="4d8f2-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4d8f2-215">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="4d8f2-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4d8f2-216">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="4d8f2-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4d8f2-217">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4d8f2-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4d8f2-218">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4d8f2-218">Actuals</span></span></th>
<th><span data-ttu-id="4d8f2-219">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4d8f2-219">Transaction currency</span></span></th>
<th><span data-ttu-id="4d8f2-220">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4d8f2-220">Fixed price</span></span></th>
<th><span data-ttu-id="4d8f2-221">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4d8f2-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4d8f2-222">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4d8f2-223">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4d8f2-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-224">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4d8f2-225">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4d8f2-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="4d8f2-226">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4d8f2-227">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-227">Cost actual</span></span></td>
<td><span data-ttu-id="4d8f2-228">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4d8f2-229">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4d8f2-230">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4d8f2-231">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4d8f2-232">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-233">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="4d8f2-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4d8f2-234">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-235">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="4d8f2-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4d8f2-236">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="4d8f2-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-237">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="4d8f2-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4d8f2-238">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="4d8f2-239">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4d8f2-240">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-240">Cost actual</span></span></td>
<td><span data-ttu-id="4d8f2-241">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-242">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-243">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-244">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-245">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-246">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="4d8f2-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4d8f2-247">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="4d8f2-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-248">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="4d8f2-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4d8f2-249">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4d8f2-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-250">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4d8f2-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4d8f2-251">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-252">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4d8f2-253">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4d8f2-254">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4d8f2-255">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4d8f2-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4d8f2-256">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-257">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4d8f2-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-258">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-259">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4d8f2-260">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-261">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4d8f2-261">Billed sales</span></span></td>
<td><span data-ttu-id="4d8f2-262">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4d8f2-263">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4d8f2-264">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4d8f2-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4d8f2-265">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-266">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-267">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-268">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4d8f2-269">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-270">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4d8f2-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4d8f2-271">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-272">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4d8f2-273">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4d8f2-274">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4d8f2-275">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4d8f2-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4d8f2-276">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4d8f2-277">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4d8f2-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4d8f2-278">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="4d8f2-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4d8f2-279">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-280">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4d8f2-281">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-282">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4d8f2-282">Billed sales</span></span></td>
<td><span data-ttu-id="4d8f2-283">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4d8f2-284">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4d8f2-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4d8f2-285">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4d8f2-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4d8f2-286">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-287">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4d8f2-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4d8f2-288">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8f2-289">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4d8f2-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4d8f2-290">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4d8f2-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
