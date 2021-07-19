---
title: Wartości rzeczywiste
description: Ten temat zawiera informacje dotyczące pracy z wartościami rzeczywistymi w rozwiązaniu Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368624"
---
# <a name="actuals"></a><span data-ttu-id="4fe0a-103">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4fe0a-103">Actuals</span></span> 

<span data-ttu-id="4fe0a-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="4fe0a-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4fe0a-105">Dane rzeczywiste reprezentują sprawdzony i zatwierdzony postęp finansowy i harmonogram projektu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="4fe0a-106">Są one tworzone w wyniku zatwierdzania czasu, wydatków, wpisów użycia materiałów oraz wpisów i faktur.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="4fe0a-107">Wiersze arkusza i przesyłanie czasu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-107">Journal lines and time submission</span></span>

<span data-ttu-id="4fe0a-108">Aby uzyskać więcej informacji o wprowadzaniu godziny, zobacz temat [Przegląd wpisów czasu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4fe0a-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="4fe0a-109">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-109">Time and materials</span></span>

<span data-ttu-id="4fe0a-110">W przypadku połączenia przesłanego wpisu czasu do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="4fe0a-111">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4fe0a-111">Fixed price</span></span>

<span data-ttu-id="4fe0a-112">Podczas przesyłania wpisu czasu dla projektu, który jest połączony z projektem zamapowanym do kontraktu o stałej cenie, system tworzy tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="4fe0a-113">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="4fe0a-113">Default pricing</span></span>

<span data-ttu-id="4fe0a-114">Logika tworzenia cen domyślnych jest przechowywana w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="4fe0a-115">Wartości pól z wpisu czasu są kopiowane do wiersza arkusza.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="4fe0a-116">Te wartości zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="4fe0a-117">Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka zasobów**, służą do określenia odpowiedniej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="4fe0a-118">We wpisie czasu można dodać pole niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="4fe0a-119">Aby wartość pola była propagowana do wartości rzeczywistych, należy utworzyć pole w tabelach **Wartości rzeczywiste** i **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="4fe0a-120">Użyj kodu niestandardowego, aby propagować wybraną wartość pola od wpisu czasu do wartości rzeczywistych w wierszu arkusza przy użyciu źródeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="4fe0a-121">Aby uzyskać więcej informacji o pochodzenia transakcji i połączeniach, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="4fe0a-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="4fe0a-122">Wiersze arkusza i przesyłanie podstawowych kosztów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="4fe0a-123">Aby uzyskać więcej informacji o wprowadzaniu wydatków, zobacz temat [Przegląd wydatków](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4fe0a-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="4fe0a-124">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-124">Time and materials</span></span>

<span data-ttu-id="4fe0a-125">W przypadku połączenia przesłanego wpisu wydatku podstawowego do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="4fe0a-126">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4fe0a-126">Fixed price</span></span>

<span data-ttu-id="4fe0a-127">Gdy przesłany wpis podstawowego wydatku jest połączony z projektem, który jest mapowany do wiersza umowy o stałej cenie, system tworzy jeden wiersz arkusza dla kosztu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="4fe0a-128">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="4fe0a-128">Default pricing</span></span>

<span data-ttu-id="4fe0a-129">Logika wprowadzania cen domyślnych wydatków jest oparta na kategorii wydatków.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="4fe0a-130">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="4fe0a-131">Pola wpływające na domyślne ceny, takie jak **Kategoria transakcji** i **Jednostka**, służą do określenia odpowiedniej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="4fe0a-132">Działa to jednak tylko wtedy, gdy metoda kalkulacji cen w cenniku to **Cena jednostkowa**.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="4fe0a-133">Jeśli metoda kalkulacji cen to **Koszt** lub **Narzut na koszcie**, cena wprowadzona podczas tworzenia wpisu wydatku jest używana dla kosztu, a cena w wierszu sprzedaży jest obliczana na podstawie metody kalkulacji ceny.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="4fe0a-134">Niestandardowe pole można dodać do wpisu wydatków.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="4fe0a-135">Aby wartość pola była propagowana do wartości rzeczywistych, należy utworzyć pole w tabelach **Wartości rzeczywiste** i **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="4fe0a-136">Użyj kodu niestandardowego, aby propagować wybraną wartość pola od wpisu czasu do wartości rzeczywistych w wierszu arkusza przy użyciu źródeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="4fe0a-137">Aby uzyskać więcej informacji o pochodzenia transakcji i połączeniach, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="4fe0a-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="4fe0a-138">Wiersze dziennika i przesyłanie dziennika zużycia materiałów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="4fe0a-139">Aby uzyskać więcej informacji na temat wprowadzania wydatków, zobacz [Dziennik użycia materiałów](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="4fe0a-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="4fe0a-140">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-140">Time and materials</span></span>

<span data-ttu-id="4fe0a-141">Gdy przesłany wpis dziennika zużycia materiałów jest połączony z projektem, który jest mapowany do wiersza kontraktu dotyczącego czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów, a drugi dla niezafakturowanej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="4fe0a-142">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4fe0a-142">Fixed price</span></span>

<span data-ttu-id="4fe0a-143">Gdy przesłany wpis dziennika zużycia materiałów jest połączony z projektem, który jest mapowany do wiersza umowy o stałej cenie, system tworzy jeden wiersz arkusza dla kosztu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="4fe0a-144">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="4fe0a-144">Default pricing</span></span>

<span data-ttu-id="4fe0a-145">Logika wprowadzania domyślnych cen materiałów jest oparta na kombinacji produktu i jednostki.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="4fe0a-146">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="4fe0a-147">Pola wpływające na domyślne ceny, takie jak **Identyfikator produktu** i **Jednostka**, służą do określenia odpowiedniej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="4fe0a-148">Działa to jednak tylko w przypadku produktów z katalogu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-148">However, this only works for catalog products.</span></span> <span data-ttu-id="4fe0a-149">W przypadku produktów podlegających zapisowi cena wprowadzona podczas tworzenia wpisu dziennika zużycia materiału jest używana jako koszt i cena sprzedaży w wierszach arkusza.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="4fe0a-150">Niestandardowe pole można dodać do wpisu **Dziennik użycia materiałów**.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="4fe0a-151">Aby wartość pola była propagowana do wartości rzeczywistych, należy utworzyć pole w tabelach **Wartości rzeczywiste** i **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="4fe0a-152">Użyj kodu niestandardowego, aby propagować wybraną wartość pola od wpisu czasu do wartości rzeczywistych w wierszu arkusza przy użyciu źródeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="4fe0a-153">Aby uzyskać więcej informacji o pochodzenia transakcji i połączeniach, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="4fe0a-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="4fe0a-154">Używanie dzienników do rejestrowania kosztów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-154">Use entry journals to record costs</span></span>

<span data-ttu-id="4fe0a-155">Arkusze umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="4fe0a-156">Arkusze mogą być używane w produkcji.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="4fe0a-157">Przenieś wartości rzeczywiste transakcji z innego systemu do rozwiązaniu Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="4fe0a-158">Zarejestrowania kosztów, które wystąpiły w innym systemie.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="4fe0a-159">Koszty te mogą zawierać koszty zakupu lub podwykonawców.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fe0a-160">Aplikacja nie sprawdza poprawności typu wiersza arkusza lub powiązanej kalkulacji cen wprowadzonych w wierszu dziennika.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="4fe0a-161">Z tego powodu tylko użytkownik, który jest w pełni świadomi skutków związanych z księgowaniem w projekcie powinien używać dzienników wpisów do tworzenia wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="4fe0a-162">Ze względu na wpływ danego typu arkusza należy starannie wybrać osoby, które mają mieć dostęp do tworzenia arkuszy zapisu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="4fe0a-163">Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-163">Record actuals based on project events</span></span>

<span data-ttu-id="4fe0a-164">Project Operations rejestruje transakcje finansowe zaistniałe w trakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="4fe0a-165">Te transakcje są zapisywane jako wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="4fe0a-166">W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="4fe0a-167">Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4fe0a-168">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="4fe0a-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4fe0a-169">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="4fe0a-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4fe0a-170">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="4fe0a-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4fe0a-171">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="4fe0a-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4fe0a-172">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4fe0a-173">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4fe0a-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4fe0a-174">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4fe0a-174">Actuals</span></span></th>
<th><span data-ttu-id="4fe0a-175">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4fe0a-175">Transaction currency</span></span></th>
<th><span data-ttu-id="4fe0a-176">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4fe0a-176">Fixed price</span></span></th>
<th><span data-ttu-id="4fe0a-177">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4fe0a-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4fe0a-178">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4fe0a-179">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4fe0a-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-180">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4fe0a-181">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4fe0a-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4fe0a-182">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4fe0a-183">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-183">Cost actual</span></span></td>
<td><span data-ttu-id="4fe0a-184">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-185">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-186">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="4fe0a-187">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-188">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-189">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="4fe0a-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4fe0a-190">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4fe0a-191">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4fe0a-192">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-192">Cost actual</span></span></td>
<td><span data-ttu-id="4fe0a-193">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-194">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-195">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-196">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-197">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-198">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4fe0a-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4fe0a-199">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-200">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4fe0a-201">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4fe0a-202">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4fe0a-203">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4fe0a-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4fe0a-204">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-205">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4fe0a-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-206">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-207">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-208">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-209">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4fe0a-209">Billed sales</span></span></td>
<td><span data-ttu-id="4fe0a-210">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4fe0a-211">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4fe0a-212">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4fe0a-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4fe0a-213">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-214">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-215">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-216">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-217">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-218">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4fe0a-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4fe0a-219">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-220">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4fe0a-221">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4fe0a-222">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4fe0a-223">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4fe0a-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4fe0a-224">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4fe0a-225">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4fe0a-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4fe0a-226">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="4fe0a-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4fe0a-227">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-228">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-229">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-230">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4fe0a-230">Billed sales</span></span></td>
<td><span data-ttu-id="4fe0a-231">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4fe0a-232">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4fe0a-233">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4fe0a-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4fe0a-234">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-235">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4fe0a-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4fe0a-236">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-237">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4fe0a-238">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="4fe0a-239">Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4fe0a-240">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="4fe0a-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4fe0a-241">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="4fe0a-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4fe0a-242">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="4fe0a-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4fe0a-243">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="4fe0a-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4fe0a-244">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4fe0a-245">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4fe0a-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4fe0a-246">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4fe0a-246">Actuals</span></span></th>
<th><span data-ttu-id="4fe0a-247">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4fe0a-247">Transaction currency</span></span></th>
<th><span data-ttu-id="4fe0a-248">Stała cena</span><span class="sxs-lookup"><span data-stu-id="4fe0a-248">Fixed price</span></span></th>
<th><span data-ttu-id="4fe0a-249">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="4fe0a-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4fe0a-250">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4fe0a-251">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4fe0a-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-252">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4fe0a-253">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="4fe0a-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="4fe0a-254">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4fe0a-255">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-255">Cost actual</span></span></td>
<td><span data-ttu-id="4fe0a-256">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4fe0a-257">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4fe0a-258">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4fe0a-259">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4fe0a-260">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-261">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="4fe0a-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4fe0a-262">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-263">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4fe0a-264">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-265">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="4fe0a-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4fe0a-266">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="4fe0a-267">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4fe0a-268">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-268">Cost actual</span></span></td>
<td><span data-ttu-id="4fe0a-269">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-270">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-271">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-272">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-273">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-274">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4fe0a-275">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="4fe0a-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-276">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="4fe0a-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4fe0a-277">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="4fe0a-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-278">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4fe0a-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4fe0a-279">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-280">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4fe0a-281">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4fe0a-282">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4fe0a-283">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4fe0a-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4fe0a-284">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-285">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4fe0a-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-286">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-287">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4fe0a-288">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-289">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4fe0a-289">Billed sales</span></span></td>
<td><span data-ttu-id="4fe0a-290">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4fe0a-291">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4fe0a-292">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="4fe0a-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4fe0a-293">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-294">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-295">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-296">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4fe0a-297">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-298">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4fe0a-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4fe0a-299">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-300">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4fe0a-301">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4fe0a-302">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4fe0a-303">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4fe0a-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4fe0a-304">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4fe0a-305">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="4fe0a-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4fe0a-306">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="4fe0a-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4fe0a-307">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-308">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4fe0a-309">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-310">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="4fe0a-310">Billed sales</span></span></td>
<td><span data-ttu-id="4fe0a-311">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4fe0a-312">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="4fe0a-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4fe0a-313">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="4fe0a-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4fe0a-314">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-315">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="4fe0a-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4fe0a-316">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4fe0a-317">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="4fe0a-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4fe0a-318">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="4fe0a-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
