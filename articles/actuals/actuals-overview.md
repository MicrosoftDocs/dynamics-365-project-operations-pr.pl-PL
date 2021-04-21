---
title: Wartości rzeczywiste
description: Ten temat zawiera informacje dotyczące pracy z wartościami rzeczywistymi w rozwiązaniu Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852557"
---
# <a name="actuals"></a><span data-ttu-id="e43b8-103">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="e43b8-103">Actuals</span></span> 

<span data-ttu-id="e43b8-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="e43b8-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e43b8-105">Dane rzeczywiste reprezentują sprawdzony i zatwierdzony postęp finansowy i harmonogram projektu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="e43b8-106">Są one tworzone w wyniku zatwierdzania czasu, wydatków, wpisów użycia materiałów oraz wpisów i faktur.</span><span class="sxs-lookup"><span data-stu-id="e43b8-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="e43b8-107">Wiersze arkusza i przesyłanie czasu</span><span class="sxs-lookup"><span data-stu-id="e43b8-107">Journal lines and time submission</span></span>

<span data-ttu-id="e43b8-108">Aby uzyskać więcej informacji o wprowadzaniu godziny, zobacz temat [Przegląd wpisów czasu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e43b8-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e43b8-109">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="e43b8-109">Time and materials</span></span>

<span data-ttu-id="e43b8-110">W przypadku połączenia przesłanego wpisu czasu do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.</span><span class="sxs-lookup"><span data-stu-id="e43b8-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e43b8-111">Stała cena</span><span class="sxs-lookup"><span data-stu-id="e43b8-111">Fixed price</span></span>

<span data-ttu-id="e43b8-112">Podczas przesyłania wpisu czasu dla projektu, który jest połączony z projektem zamapowanym do kontraktu o stałej cenie, system tworzy tylko wiersz arkusza dotyczący kosztu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e43b8-113">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="e43b8-113">Default pricing</span></span>

<span data-ttu-id="e43b8-114">Logika tworzenia cen domyślnych jest przechowywana w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="e43b8-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="e43b8-115">Wartości pól z wpisu czasu są kopiowane do wiersza arkusza.</span><span class="sxs-lookup"><span data-stu-id="e43b8-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="e43b8-116">Te wartości zawierają datę transakcji, pozycję kontraktu, do której jest mapowany projekt, oraz wynik obliczania waluty z odpowiedniego cennika.</span><span class="sxs-lookup"><span data-stu-id="e43b8-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="e43b8-117">Pola wpływające na domyślne ceny, takie jak **Rola** i **Jednostka zasobów**, służą do określenia odpowiedniej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="e43b8-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="e43b8-118">We wpisie czasu można dodać pole niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="e43b8-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="e43b8-119">Aby wartość pola była propagowana do wartości rzeczywistych, należy utworzyć pole w tabelach **Wartości rzeczywiste** i **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="e43b8-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="e43b8-120">Użyj kodu niestandardowego, aby propagować wybraną wartość pola od wpisu czasu do wartości rzeczywistych w wierszu arkusza przy użyciu źródeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="e43b8-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="e43b8-121">Aby uzyskać więcej informacji o pochodzenia transakcji i połączeniach, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="e43b8-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="e43b8-122">Wiersze arkusza i przesyłanie podstawowych kosztów</span><span class="sxs-lookup"><span data-stu-id="e43b8-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="e43b8-123">Aby uzyskać więcej informacji o wprowadzaniu wydatków, zobacz temat [Przegląd wydatków](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e43b8-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e43b8-124">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="e43b8-124">Time and materials</span></span>

<span data-ttu-id="e43b8-125">W przypadku połączenia przesłanego wpisu wydatku podstawowego do projektu zamapowanego na pozycję dotyczącą czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów i drugi dla niezafakturowanych transakcji.</span><span class="sxs-lookup"><span data-stu-id="e43b8-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e43b8-126">Stała cena</span><span class="sxs-lookup"><span data-stu-id="e43b8-126">Fixed price</span></span>

<span data-ttu-id="e43b8-127">Gdy przesłany wpis podstawowego wydatku jest połączony z projektem, który jest mapowany do wiersza umowy o stałej cenie, system tworzy jeden wiersz arkusza dla kosztu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e43b8-128">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="e43b8-128">Default pricing</span></span>

<span data-ttu-id="e43b8-129">Logika wprowadzania cen domyślnych wydatków jest oparta na kategorii wydatków.</span><span class="sxs-lookup"><span data-stu-id="e43b8-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="e43b8-130">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="e43b8-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="e43b8-131">Pola wpływające na domyślne ceny, takie jak **Kategoria transakcji** i **Jednostka**, służą do określenia odpowiedniej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="e43b8-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="e43b8-132">Działa to jednak tylko wtedy, gdy metoda kalkulacji cen w cenniku to **Cena jednostkowa**.</span><span class="sxs-lookup"><span data-stu-id="e43b8-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="e43b8-133">Jeśli metoda kalkulacji cen to **Koszt** lub **Narzut na koszcie**, cena wprowadzona podczas tworzenia wpisu wydatku jest używana dla kosztu, a cena w wierszu sprzedaży jest obliczana na podstawie metody kalkulacji ceny.</span><span class="sxs-lookup"><span data-stu-id="e43b8-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="e43b8-134">Niestandardowe pole można dodać do wpisu wydatków.</span><span class="sxs-lookup"><span data-stu-id="e43b8-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="e43b8-135">Aby wartość pola była propagowana do wartości rzeczywistych, należy utworzyć pole w tabelach **Wartości rzeczywiste** i **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="e43b8-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="e43b8-136">Użyj kodu niestandardowego, aby propagować wybraną wartość pola od wpisu czasu do wartości rzeczywistych w wierszu arkusza przy użyciu źródeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="e43b8-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="e43b8-137">Aby uzyskać więcej informacji o pochodzenia transakcji i połączeniach, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="e43b8-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="e43b8-138">Wiersze dziennika i przesyłanie dziennika zużycia materiałów</span><span class="sxs-lookup"><span data-stu-id="e43b8-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="e43b8-139">Aby uzyskać więcej informacji na temat wprowadzania wydatków, zobacz [Dziennik użycia materiałów](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="e43b8-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e43b8-140">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="e43b8-140">Time and materials</span></span>

<span data-ttu-id="e43b8-141">Gdy przesłany wpis dziennika zużycia materiałów jest połączony z projektem, który jest mapowany do wiersza kontraktu dotyczącego czasu i materiałów, system tworzy dwa wiersze arkusza, jeden dla kosztów, a drugi dla niezafakturowanej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e43b8-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e43b8-142">Stała cena</span><span class="sxs-lookup"><span data-stu-id="e43b8-142">Fixed price</span></span>

<span data-ttu-id="e43b8-143">Gdy przesłany wpis dziennika zużycia materiałów jest połączony z projektem, który jest mapowany do wiersza umowy o stałej cenie, system tworzy jeden wiersz arkusza dla kosztu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e43b8-144">Cena domyślna</span><span class="sxs-lookup"><span data-stu-id="e43b8-144">Default pricing</span></span>

<span data-ttu-id="e43b8-145">Logika wprowadzania domyślnych cen materiałów jest oparta na kombinacji produktu i jednostki.</span><span class="sxs-lookup"><span data-stu-id="e43b8-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="e43b8-146">Do wyznaczenia odpowiedniego cennika są używane wartości daty transakcji, pozycji kontraktu, do której jest mapowany projekt, i waluty.</span><span class="sxs-lookup"><span data-stu-id="e43b8-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="e43b8-147">Pola wpływające na domyślne ceny, takie jak **Identyfikator produktu** i **Jednostka**, służą do określenia odpowiedniej ceny w wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="e43b8-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="e43b8-148">Działa to jednak tylko w przypadku produktów z katalogu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-148">However, this only works for catalog products.</span></span> <span data-ttu-id="e43b8-149">W przypadku produktów podlegających zapisowi cena wprowadzona podczas tworzenia wpisu dziennika zużycia materiału jest używana jako koszt i cena sprzedaży w wierszach arkusza.</span><span class="sxs-lookup"><span data-stu-id="e43b8-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="e43b8-150">Niestandardowe pole można dodać do wpisu **Dziennik użycia materiałów**.</span><span class="sxs-lookup"><span data-stu-id="e43b8-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="e43b8-151">Aby wartość pola była propagowana do wartości rzeczywistych, należy utworzyć pole w tabelach **Wartości rzeczywiste** i **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="e43b8-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="e43b8-152">Użyj kodu niestandardowego, aby propagować wybraną wartość pola od wpisu czasu do wartości rzeczywistych w wierszu arkusza przy użyciu źródeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="e43b8-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="e43b8-153">Aby uzyskać więcej informacji o pochodzenia transakcji i połączeniach, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="e43b8-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="e43b8-154">Używanie dzienników do rejestrowania kosztów</span><span class="sxs-lookup"><span data-stu-id="e43b8-154">Use entry journals to record costs</span></span>

<span data-ttu-id="e43b8-155">Arkusze umożliwiają rejestrowanie kosztów lub przychodów w klasach materiałów, opłat, czasu, wydatków lub transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="e43b8-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="e43b8-156">Arkusze mogą być używane w produkcji.</span><span class="sxs-lookup"><span data-stu-id="e43b8-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="e43b8-157">Przenieś wartości rzeczywiste transakcji z innego systemu do rozwiązaniu Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e43b8-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="e43b8-158">Zarejestrowania kosztów, które wystąpiły w innym systemie.</span><span class="sxs-lookup"><span data-stu-id="e43b8-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="e43b8-159">Koszty te mogą zawierać koszty zakupu lub podwykonawców.</span><span class="sxs-lookup"><span data-stu-id="e43b8-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e43b8-160">Aplikacja nie sprawdza poprawności typu wiersza arkusza lub powiązanej kalkulacji cen wprowadzonych w wierszu dziennika.</span><span class="sxs-lookup"><span data-stu-id="e43b8-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="e43b8-161">Z tego powodu tylko użytkownik, który jest w pełni świadomi skutków związanych z księgowaniem w projekcie powinien używać dzienników wpisów do tworzenia wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="e43b8-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="e43b8-162">Ze względu na wpływ danego typu arkusza należy starannie wybrać osoby, które mają mieć dostęp do tworzenia arkuszy zapisu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="e43b8-163">Rejestrowanie wartości rzeczywistych na podstawie zdarzeń projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-163">Record actuals based on project events</span></span>

<span data-ttu-id="e43b8-164">Project Operations rejestruje transakcje finansowe zaistniałe w trakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="e43b8-165">Te transakcje są zapisywane jako wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="e43b8-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="e43b8-166">W poniższych tabelach przedstawiono różne typy wartości rzeczywistych, które są tworzone w zależności od tego, czy projekt jest rozliczany według czasu i materiałów czy też jest projektem o stałej cenie, czy znajduje się na etapie przedsprzedaży lub czy jest projektem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="e43b8-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="e43b8-167">Zasób należy do tej samej jednostki organizacyjnej, co jednostka kontraktująca projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e43b8-168">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="e43b8-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e43b8-169">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="e43b8-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e43b8-170">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="e43b8-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e43b8-171">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="e43b8-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e43b8-172">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="e43b8-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e43b8-173">Stała cena</span><span class="sxs-lookup"><span data-stu-id="e43b8-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e43b8-174">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="e43b8-174">Actuals</span></span></th>
<th><span data-ttu-id="e43b8-175">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="e43b8-175">Transaction currency</span></span></th>
<th><span data-ttu-id="e43b8-176">Stała cena</span><span class="sxs-lookup"><span data-stu-id="e43b8-176">Fixed price</span></span></th>
<th><span data-ttu-id="e43b8-177">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="e43b8-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e43b8-178">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e43b8-179">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="e43b8-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-180">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e43b8-181">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="e43b8-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e43b8-182">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e43b8-183">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-183">Cost actual</span></span></td>
<td><span data-ttu-id="e43b8-184">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-185">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-186">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="e43b8-187">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-188">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-189">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="e43b8-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e43b8-190">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e43b8-191">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e43b8-192">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-192">Cost actual</span></span></td>
<td><span data-ttu-id="e43b8-193">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-194">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-195">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-196">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-197">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-198">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="e43b8-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e43b8-199">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-200">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="e43b8-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e43b8-201">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e43b8-202">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e43b8-203">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e43b8-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e43b8-204">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-205">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="e43b8-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-206">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-207">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-208">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-209">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="e43b8-209">Billed sales</span></span></td>
<td><span data-ttu-id="e43b8-210">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e43b8-211">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e43b8-212">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e43b8-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e43b8-213">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-214">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-215">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-216">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-217">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-218">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="e43b8-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e43b8-219">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-220">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="e43b8-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e43b8-221">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e43b8-222">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="e43b8-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e43b8-223">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="e43b8-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e43b8-224">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e43b8-225">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="e43b8-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e43b8-226">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="e43b8-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e43b8-227">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-228">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-229">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-230">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="e43b8-230">Billed sales</span></span></td>
<td><span data-ttu-id="e43b8-231">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e43b8-232">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="e43b8-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e43b8-233">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="e43b8-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e43b8-234">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-235">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="e43b8-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e43b8-236">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-237">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="e43b8-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e43b8-238">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="e43b8-239">Zasób należy do jednostki organizacyjnej innej niż jednostka kontraktująca projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e43b8-240">Zdarzenie</span><span class="sxs-lookup"><span data-stu-id="e43b8-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e43b8-241">Projekt do rozliczenia lub sprzedany</span><span class="sxs-lookup"><span data-stu-id="e43b8-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e43b8-242">Projekt na etapie przedsprzedaży</span><span class="sxs-lookup"><span data-stu-id="e43b8-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e43b8-243">Projekt wewnętrzny</span><span class="sxs-lookup"><span data-stu-id="e43b8-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e43b8-244">Rozliczanie według czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="e43b8-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e43b8-245">Stała cena</span><span class="sxs-lookup"><span data-stu-id="e43b8-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e43b8-246">Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="e43b8-246">Actuals</span></span></th>
<th><span data-ttu-id="e43b8-247">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="e43b8-247">Transaction currency</span></span></th>
<th><span data-ttu-id="e43b8-248">Stała cena</span><span class="sxs-lookup"><span data-stu-id="e43b8-248">Fixed price</span></span></th>
<th><span data-ttu-id="e43b8-249">Waluta transakcji</span><span class="sxs-lookup"><span data-stu-id="e43b8-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e43b8-250">Jest tworzony wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e43b8-251">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="e43b8-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-252">Jest przesyłany wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e43b8-253">Brak działania w encji Wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="e43b8-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="e43b8-254">Godzina jest zatwierdzana, a podczas zatwierdzania nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e43b8-255">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-255">Cost actual</span></span></td>
<td><span data-ttu-id="e43b8-256">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e43b8-257">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e43b8-258">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e43b8-259">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e43b8-260">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-261">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna</span><span class="sxs-lookup"><span data-stu-id="e43b8-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e43b8-262">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-263">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="e43b8-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e43b8-264">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="e43b8-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-265">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="e43b8-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e43b8-266">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="e43b8-267">Godzina jest zatwierdzana, a podczas zatwierdzania następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e43b8-268">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-268">Cost actual</span></span></td>
<td><span data-ttu-id="e43b8-269">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-270">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-271">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-272">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-273">Wartość rzeczywista kosztu</span><span class="sxs-lookup"><span data-stu-id="e43b8-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-274">Koszt jednostkowy zasobów</span><span class="sxs-lookup"><span data-stu-id="e43b8-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e43b8-275">Waluta jednostki zasobów</span><span class="sxs-lookup"><span data-stu-id="e43b8-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-276">Sprzedaż międzyorganizacyjna</span><span class="sxs-lookup"><span data-stu-id="e43b8-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e43b8-277">Waluta jednostki kontraktującej</span><span class="sxs-lookup"><span data-stu-id="e43b8-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-278">Wartość rzeczywista nierozliczonej sprzedaży — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="e43b8-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e43b8-279">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-280">Wartość rzeczywista nierozliczonej sprzedaży — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="e43b8-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e43b8-281">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e43b8-282">Faktura jest potwierdzania, nie ma żadnych zmian ani zwiększenia liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e43b8-283">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e43b8-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e43b8-284">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-285">Rozliczona sprzedaż w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="e43b8-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-286">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-287">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e43b8-288">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-289">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="e43b8-289">Billed sales</span></span></td>
<td><span data-ttu-id="e43b8-290">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e43b8-291">Faktura jest potwierdzania, następuje zmniejszenie liczby godzin podlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="e43b8-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e43b8-292">Wycofanie nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e43b8-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e43b8-293">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-294">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-295">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-296">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e43b8-297">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-298">Rozliczona sprzedaż — odpłatna w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="e43b8-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e43b8-299">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-300">Rozliczona sprzedaż — nieodpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="e43b8-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e43b8-301">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e43b8-302">Faktura jest korygowana w celu zwiększenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="e43b8-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e43b8-303">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="e43b8-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e43b8-304">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e43b8-305">Wycofanie rozliczonej sprzedaży w punkcie kontrolnym</span><span class="sxs-lookup"><span data-stu-id="e43b8-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e43b8-306">Zmiana stanu punktu kontrolnego z <strong>Zafakturowano</strong> na <strong>Gotowe do zafakturowania</strong></span><span class="sxs-lookup"><span data-stu-id="e43b8-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e43b8-307">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-308">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e43b8-309">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="e43b8-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-310">Rozliczona sprzedaż</span><span class="sxs-lookup"><span data-stu-id="e43b8-310">Billed sales</span></span></td>
<td><span data-ttu-id="e43b8-311">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e43b8-312">Faktura jest korygowana w celu zmniejszenia ilości odpłatnej.</span><span class="sxs-lookup"><span data-stu-id="e43b8-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e43b8-313">Rozliczona sprzedaż — wycofanie</span><span class="sxs-lookup"><span data-stu-id="e43b8-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e43b8-314">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-315">Rozliczona sprzedaż w zakresie nowej ilości</span><span class="sxs-lookup"><span data-stu-id="e43b8-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e43b8-316">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e43b8-317">Nierozliczona sprzedaż — odpłatna w zakresie różnicy</span><span class="sxs-lookup"><span data-stu-id="e43b8-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e43b8-318">Waluta kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="e43b8-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
