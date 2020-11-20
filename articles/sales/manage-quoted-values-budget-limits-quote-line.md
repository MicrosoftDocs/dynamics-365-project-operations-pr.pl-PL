---
title: Omówienie wierszy oferty opartej na projekcie
description: Ten temat zawiera informacje o korzystaniu z wiersza oferty opartej na projekcie w pracy projektowej.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181870"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="5eeed-103">Omówienie wierszy oferty opartej na projekcie</span><span class="sxs-lookup"><span data-stu-id="5eeed-103">Project-based quote lines overview</span></span>

<span data-ttu-id="5eeed-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="5eeed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5eeed-105">Wiersze oferty opartej na projekcie są utworzone w celu ułatwienia oceny pracy nad projektem w momencie zakontraktowania.</span><span class="sxs-lookup"><span data-stu-id="5eeed-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="5eeed-106">Struktura wiersza oferty opartej na projekcie jest przedłużana na potrzeby oszacowań projektu z następującymi pojęciami:</span><span class="sxs-lookup"><span data-stu-id="5eeed-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="5eeed-107">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="5eeed-107">Billing Method</span></span>
- <span data-ttu-id="5eeed-108">Mapowanie projektu</span><span class="sxs-lookup"><span data-stu-id="5eeed-108">Project Mapping</span></span>
- <span data-ttu-id="5eeed-109">Dołączone klasy transakcji</span><span class="sxs-lookup"><span data-stu-id="5eeed-109">Included Transaction classes</span></span>
- <span data-ttu-id="5eeed-110">Nieprzekraczalny limit</span><span class="sxs-lookup"><span data-stu-id="5eeed-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="5eeed-111">Konfiguracja odpłatności</span><span class="sxs-lookup"><span data-stu-id="5eeed-111">Chargeability setup</span></span>
- <span data-ttu-id="5eeed-112">Szacowanie przy użyciu szczegółów wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="5eeed-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="5eeed-113">Klienci wierszy oferty</span><span class="sxs-lookup"><span data-stu-id="5eeed-113">Quote line Customers</span></span>

<span data-ttu-id="5eeed-114">Poniższa tabela zawiera informacje o polach na karcie **Ogólne** w wierszu oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="5eeed-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="5eeed-115">Te pola pomagają skonfigurować podstawę dla konkretnego szacunkowego oszacowania pracy projektowej.</span><span class="sxs-lookup"><span data-stu-id="5eeed-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="5eeed-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="5eeed-116">**Field**</span></span> | <span data-ttu-id="5eeed-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="5eeed-117">**Description**</span></span> | <span data-ttu-id="5eeed-118">**Wpływ zmian w dalszych etapach**</span><span class="sxs-lookup"><span data-stu-id="5eeed-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5eeed-119">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="5eeed-119">Name</span></span> | <span data-ttu-id="5eeed-120">Nazwa wiersza oferty, która ułatwia identyfikację oddzielnego komponentu szacowanego w ramach danej oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="5eeed-121">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-122">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="5eeed-122">Billing Method</span></span> | <span data-ttu-id="5eeed-123">Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="5eeed-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="5eeed-124">To pole zawiera dwa główne projekty, które są obsługiwane przez Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="5eeed-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="5eeed-125">- Stała cena</span><span class="sxs-lookup"><span data-stu-id="5eeed-125">- Fixed price</span></span></br><span data-ttu-id="5eeed-126">- Czas i materiał.</span><span class="sxs-lookup"><span data-stu-id="5eeed-126">- Time and material.</span></span>| <span data-ttu-id="5eeed-127">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-128">Project</span><span class="sxs-lookup"><span data-stu-id="5eeed-128">Project</span></span> | <span data-ttu-id="5eeed-129">Użyj tego opcjonalnego pola w celu zidentyfikowania projektu, który będzie używany do dostarczania pracy w ramach tego zakontraktowania.</span><span class="sxs-lookup"><span data-stu-id="5eeed-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="5eeed-130">Podczas mapowania projektu na wiersz oferty pomocne jest konfigurowanie zadań odpłatnych, a także wprowadzenie oceny opartej na projekcie z wiersza oferty jako szczegółów wiersza oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="5eeed-131">Jeśli projekt nie jest mapowany na wiersz oferty opartej na projekcie, szacunek powinien zostać utworzony ręcznie, tworząc szczegóły poszczególnych wierszy oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="5eeed-132">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-133">Uwzględnij czas</span><span class="sxs-lookup"><span data-stu-id="5eeed-133">Include Time</span></span> | <span data-ttu-id="5eeed-134">Flaga **Tak**/**Nie** wskazuje, czy transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5eeed-135">Flaga **Nie** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5eeed-136">Flaga **Tak** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5eeed-137">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-138">Uwzględnij wydatek</span><span class="sxs-lookup"><span data-stu-id="5eeed-138">Include Expense</span></span> | <span data-ttu-id="5eeed-139">Flaga **Tak**/**Nie** wskazuje, czy koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5eeed-140">Flaga **Nie** wskazuje, że koszty wydatków w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5eeed-141">Flaga **Tak** wskazuje, że koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5eeed-142">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-143">Uwzględnij opłatę</span><span class="sxs-lookup"><span data-stu-id="5eeed-143">Include Fee</span></span> | <span data-ttu-id="5eeed-144">Flaga **Tak**/**Nie** wskazuje, czy opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5eeed-145">Flaga **Nie** wskazuje, że opłaty w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5eeed-146">Flaga **Tak** wskazuje, że opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5eeed-147">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-148">Oferowana kwota</span><span class="sxs-lookup"><span data-stu-id="5eeed-148">Quoted Amount</span></span> | <span data-ttu-id="5eeed-149">Jest to kwota, która zostanie zaoferowana klientowi dla wszystkich prognozowanych prac w wierszu oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="5eeed-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="5eeed-150">Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola **Budżet klienta** w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="5eeed-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="5eeed-151">Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="5eeed-152">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-153">Szacowany podatek</span><span class="sxs-lookup"><span data-stu-id="5eeed-153">Estimated Tax</span></span> | <span data-ttu-id="5eeed-154">Jest to pole, które można edytować, aby dodać szacowaną kwotę podatku w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="5eeed-155">Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podatku podanej w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="5eeed-156">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-157">Oferowana kwota po opodatkowaniu</span><span class="sxs-lookup"><span data-stu-id="5eeed-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="5eeed-158">To pole stanowi kwotę wiersza oferty po zaliczeniu podatku i jest w trybie tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="5eeed-159">Kwota w tym polu jest obliczana jako *Oferowana kwota z podatkiem*.</span><span class="sxs-lookup"><span data-stu-id="5eeed-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="5eeed-160">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-161">Nieprzekraczalny limit</span><span class="sxs-lookup"><span data-stu-id="5eeed-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="5eeed-162">To pole można edytować i jest dostępne tylko w wierszach oferty opartej na projekcie z metodą rozliczania **Czas i amteriał**.</span><span class="sxs-lookup"><span data-stu-id="5eeed-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="5eeed-163">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5eeed-164">Budżet klienta</span><span class="sxs-lookup"><span data-stu-id="5eeed-164">Customer Budget</span></span> | <span data-ttu-id="5eeed-165">Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="5eeed-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="5eeed-166">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="5eeed-167">Reguły sprawdzania poprawności dla pól na karcie Ogólne w wierszach oferty opartej na projektach</span><span class="sxs-lookup"><span data-stu-id="5eeed-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="5eeed-168">**Reguła 1**: dana klasa transakcji w wybranym projekcie może być uwzględniona tylko w jednym wierszu oferty opartej na projekcie oferty.</span><span class="sxs-lookup"><span data-stu-id="5eeed-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="5eeed-169">**Reguła 2**: Jeśli szansa sprzedaży zawiera wiele ofert, między różnymi ofertami można odwoływać się do tego samego projektu i zawierać tę samą klasę transakcji.</span><span class="sxs-lookup"><span data-stu-id="5eeed-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="5eeed-170">**Zasada 3**: Jeśli oferty nie należą do tej samej szansy sprzedaży, nie mogą zawierać tej samej klasy projektów i transakcji.</span><span class="sxs-lookup"><span data-stu-id="5eeed-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="5eeed-171">
                    <strong>Szansa sprzedaży</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5eeed-172">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5eeed-173">
                    <strong>Wiersz oferty</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5eeed-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5eeed-175">
                    <strong>Uwzględnij czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5eeed-176">
                    <strong>Uwzględnij wydatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5eeed-177">
                    <strong>Dołącz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="5eeed-178">
                    <strong>opłata</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="5eeed-179">
                    <strong>Prawidłowe/nieprawidłowe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="5eeed-180">
                    <strong>Przyczyna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5eeed-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-181">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-182">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-183">QL1</span><span class="sxs-lookup"><span data-stu-id="5eeed-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-184">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-185">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-186">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-187">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-188">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="5eeed-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-189">Naruszenie reguły nr 1.</span><span class="sxs-lookup"><span data-stu-id="5eeed-189">Violation of Rule #1.</span></span> <span data-ttu-id="5eeed-190">Czas, wydatek i opłaty w projekcie P1 są uwzględniane zarówno w wierszach oferty, QL1, jak i QL2.</span><span class="sxs-lookup"><span data-stu-id="5eeed-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-191">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-192">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-193">QL2</span><span class="sxs-lookup"><span data-stu-id="5eeed-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-194">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-195">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-196">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-197">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-198">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-199">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-200">QL1</span><span class="sxs-lookup"><span data-stu-id="5eeed-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-201">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-202">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-203">No</span><span class="sxs-lookup"><span data-stu-id="5eeed-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-204">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-205">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="5eeed-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-206">Naruszenie reguły nr 1.</span><span class="sxs-lookup"><span data-stu-id="5eeed-206">Violation of Rule #1.</span></span> <span data-ttu-id="5eeed-207">Czas i opłaty w projekcie P1 są uwzględniane zarówno w wierszach oferty, QL1, jak i QL2.</span><span class="sxs-lookup"><span data-stu-id="5eeed-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-208">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-209">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-210">QL2</span><span class="sxs-lookup"><span data-stu-id="5eeed-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-211">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-212">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-213">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-214">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-215">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-216">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-217">QL1</span><span class="sxs-lookup"><span data-stu-id="5eeed-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-218">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-219">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-220">No</span><span class="sxs-lookup"><span data-stu-id="5eeed-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-221">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-222">Prawidłowe</span><span class="sxs-lookup"><span data-stu-id="5eeed-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="5eeed-223">Godziny i opłaty z projektu P1 są zawarte w QL1.</span><span class="sxs-lookup"><span data-stu-id="5eeed-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="5eeed-224">Wydatki projektowe w ramach P1 są zawarte w QL2.</span><span class="sxs-lookup"><span data-stu-id="5eeed-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="5eeed-225">W żadnym wierszu oferty nie ma nakładania się wartości, więc wszystko jest poprawne.</span><span class="sxs-lookup"><span data-stu-id="5eeed-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-226">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-227">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-228">QL2</span><span class="sxs-lookup"><span data-stu-id="5eeed-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-229">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-230">No</span><span class="sxs-lookup"><span data-stu-id="5eeed-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-231">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-232">No</span><span class="sxs-lookup"><span data-stu-id="5eeed-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-233">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-234">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-235">QL1</span><span class="sxs-lookup"><span data-stu-id="5eeed-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-236">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-237">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-238">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-239">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-240">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="5eeed-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-241">Naruszenie reguły nr 1 powyżej</span><span class="sxs-lookup"><span data-stu-id="5eeed-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="5eeed-242">Q1 zawiera czas, koszty i opłaty dla całego projektu P1.</span><span class="sxs-lookup"><span data-stu-id="5eeed-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5eeed-243">QL2 zawiera czas, wydatki i opłaty dla całego projektu P1 i pokrywa się ze składnikiem, który został zamieszczony w Q1.</span><span class="sxs-lookup"><span data-stu-id="5eeed-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-244">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-245">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-246">QL2</span><span class="sxs-lookup"><span data-stu-id="5eeed-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-247">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-248">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-249">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-250">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-251">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-252">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-253">QL1</span><span class="sxs-lookup"><span data-stu-id="5eeed-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-254">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-255">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-256">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-257">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5eeed-258">Prawidłowe</span><span class="sxs-lookup"><span data-stu-id="5eeed-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-259">Na podstawie reguły nr 2, Q1 i Q2 to dwie oferty z tej samej szansy sprzedaży, przez co obydwa te elementy mogą szacować dla tych samych składników projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-260">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-261">K2</span><span class="sxs-lookup"><span data-stu-id="5eeed-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-262">QL1 do Q2</span><span class="sxs-lookup"><span data-stu-id="5eeed-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-263">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-264">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-265">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-266">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-267">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-268">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-269">QL1</span><span class="sxs-lookup"><span data-stu-id="5eeed-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-270">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-271">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-272">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-273">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5eeed-274">Prawidłowe</span><span class="sxs-lookup"><span data-stu-id="5eeed-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5eeed-275">Na podstawie reguły nr 3, Q1 i Q2 to dwie oferty z różnych szans sprzedaży, przez co obydwa te elementy nie mogą szacować dla tych samych składników projektu.</span><span class="sxs-lookup"><span data-stu-id="5eeed-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5eeed-276">O2</span><span class="sxs-lookup"><span data-stu-id="5eeed-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5eeed-277">K1</span><span class="sxs-lookup"><span data-stu-id="5eeed-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-278">QL1</span><span class="sxs-lookup"><span data-stu-id="5eeed-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-279">O1</span><span class="sxs-lookup"><span data-stu-id="5eeed-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-280">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5eeed-281">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5eeed-282">Tak</span><span class="sxs-lookup"><span data-stu-id="5eeed-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5eeed-283">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="5eeed-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

