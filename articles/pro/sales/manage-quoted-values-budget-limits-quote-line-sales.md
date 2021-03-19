---
title: Omówienie wierszy oferty opartej na projekcie - wersja uproszczona
description: Ten temat zawiera informacje o korzystaniu z wiersza oferty opartej na projekcie w pracy projektowej. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272986"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="13e4e-104">Omówienie wierszy oferty opartej na projekcie - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="13e4e-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="13e4e-105">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="13e4e-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="13e4e-106">Wiersze oferty opartej na projekcie są utworzone w celu ułatwienia oceny pracy nad projektem w momencie zakontraktowania.</span><span class="sxs-lookup"><span data-stu-id="13e4e-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="13e4e-107">Struktura wiersza oferty opartej na projekcie jest przedłużana na potrzeby oszacowań projektu z następującymi pojęciami:</span><span class="sxs-lookup"><span data-stu-id="13e4e-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="13e4e-108">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="13e4e-108">Billing Method</span></span>
- <span data-ttu-id="13e4e-109">Mapowanie projektów i zadań</span><span class="sxs-lookup"><span data-stu-id="13e4e-109">Project and Task Mapping</span></span>
- <span data-ttu-id="13e4e-110">Dołączone klasy transakcji</span><span class="sxs-lookup"><span data-stu-id="13e4e-110">Included Transaction classes</span></span>
- <span data-ttu-id="13e4e-111">Nieprzekraczalny limit</span><span class="sxs-lookup"><span data-stu-id="13e4e-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="13e4e-112">Konfiguracja odpłatności</span><span class="sxs-lookup"><span data-stu-id="13e4e-112">Chargeability setup</span></span>
- <span data-ttu-id="13e4e-113">Szacowanie przy użyciu szczegółów wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="13e4e-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="13e4e-114">Klienci wierszy oferty</span><span class="sxs-lookup"><span data-stu-id="13e4e-114">Quote line Customers</span></span>

<span data-ttu-id="13e4e-115">Poniższa tabela zawiera informacje o polach na karcie **Ogólne** w wierszu oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="13e4e-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="13e4e-116">Te pola pomagają skonfigurować podstawę dla konkretnego szacunkowego oszacowania pracy projektowej.</span><span class="sxs-lookup"><span data-stu-id="13e4e-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="13e4e-117">**Pole**</span><span class="sxs-lookup"><span data-stu-id="13e4e-117">**Field**</span></span> | <span data-ttu-id="13e4e-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="13e4e-118">**Description**</span></span> | <span data-ttu-id="13e4e-119">**Wpływ zmian w dalszych etapach**</span><span class="sxs-lookup"><span data-stu-id="13e4e-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="13e4e-120">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="13e4e-120">Name</span></span> | <span data-ttu-id="13e4e-121">Nazwa wiersza oferty, która ułatwia identyfikację oddzielnego komponentu szacowanego w ramach danej oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="13e4e-122">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-123">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="13e4e-123">Billing Method</span></span> | <span data-ttu-id="13e4e-124">Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="13e4e-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="13e4e-125">To pole obejmuje dwa główne modele kontraktów obsługiwane przez Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="13e4e-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="13e4e-126">- Stała cena</span><span class="sxs-lookup"><span data-stu-id="13e4e-126">- Fixed price</span></span></br><span data-ttu-id="13e4e-127">- Czas i materiał.</span><span class="sxs-lookup"><span data-stu-id="13e4e-127">- Time and material.</span></span>| <span data-ttu-id="13e4e-128">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-129">Project</span><span class="sxs-lookup"><span data-stu-id="13e4e-129">Project</span></span> | <span data-ttu-id="13e4e-130">Użyj tego opcjonalnego pola w celu zidentyfikowania projektu, który będzie używany do dostarczania pracy w ramach tego zakontraktowania.</span><span class="sxs-lookup"><span data-stu-id="13e4e-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="13e4e-131">Podczas mapowania projektu na wiersz oferty pomocne jest konfigurowanie zadań odpłatnych, a także wprowadzenie oceny opartej na projekcie z wiersza oferty jako szczegółów wiersza oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="13e4e-132">Jeśli projekt nie jest mapowany na wiersz oferty opartej na projekcie, szacunek powinien zostać utworzony ręcznie, tworząc szczegóły poszczególnych wierszy oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="13e4e-133">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="13e4e-134">Uwzględnione zadania</span><span class="sxs-lookup"><span data-stu-id="13e4e-134">Included Tasks</span></span> | <span data-ttu-id="13e4e-135">Wskazuje, czy dany wiersz oferty jest używany we wszystkich zadaniach wybranego projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="13e4e-136">To pole ma następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="13e4e-136">This field has the following possible values:</span></span></br><span data-ttu-id="13e4e-137">- Wszystkie zadania projektu</span><span class="sxs-lookup"><span data-stu-id="13e4e-137">- All project tasks</span></span></br><span data-ttu-id="13e4e-138">- Tylko wybrane zadania projektu</span><span class="sxs-lookup"><span data-stu-id="13e4e-138">- Selected project tasks only</span></span></br><span data-ttu-id="13e4e-139">W tym polu jest wyświetlona pusta wartość, która jest równoznaczna z opcją **Wszystkie zadania projektu**.</span><span class="sxs-lookup"><span data-stu-id="13e4e-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="13e4e-140">Po wybraniu opcji **Tylko zaznaczone zadania projektu** na stronie projekt, na karcie **Ustawienie rozliczeń zadań** można wybrać określone zadania, które mają zostać skojarzone z danym wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="13e4e-141">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-142">Uwzględnij czas</span><span class="sxs-lookup"><span data-stu-id="13e4e-142">Include Time</span></span> | <span data-ttu-id="13e4e-143">Flaga **Tak**/**Nie** wskazuje, czy transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="13e4e-144">Flaga **Nie** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="13e4e-145">Flaga **Tak** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="13e4e-146">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-147">Uwzględnij wydatek</span><span class="sxs-lookup"><span data-stu-id="13e4e-147">Include Expense</span></span> | <span data-ttu-id="13e4e-148">Flaga **Tak**/**Nie** wskazuje, czy koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="13e4e-149">Flaga **Nie** wskazuje, że koszty wydatków w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="13e4e-150">Flaga **Tak** wskazuje, że koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="13e4e-151">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-152">Uwzględnij opłatę</span><span class="sxs-lookup"><span data-stu-id="13e4e-152">Include Fee</span></span> | <span data-ttu-id="13e4e-153">Flaga **Tak**/**Nie** wskazuje, czy opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="13e4e-154">Flaga **Nie** wskazuje, że opłaty w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="13e4e-155">Flaga **Tak** wskazuje, że opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="13e4e-156">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-157">Oferowana kwota</span><span class="sxs-lookup"><span data-stu-id="13e4e-157">Quoted Amount</span></span> | <span data-ttu-id="13e4e-158">Jest to kwota, która zostanie zaoferowana klientowi dla wszystkich prognozowanych prac w wierszu oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="13e4e-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="13e4e-159">Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola **Budżet klienta** w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="13e4e-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="13e4e-160">Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="13e4e-161">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-162">Szacowany podatek</span><span class="sxs-lookup"><span data-stu-id="13e4e-162">Estimated Tax</span></span> | <span data-ttu-id="13e4e-163">Jest to pole, które można edytować, aby dodać szacowaną kwotę podatku w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="13e4e-164">Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podatku podanej w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="13e4e-165">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-166">Oferowana kwota po opodatkowaniu</span><span class="sxs-lookup"><span data-stu-id="13e4e-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="13e4e-167">To pole stanowi kwotę wiersza oferty po zaliczeniu podatku i jest w trybie tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="13e4e-168">Kwota w tym polu jest obliczana jako *Oferowana kwota z podatkiem*.</span><span class="sxs-lookup"><span data-stu-id="13e4e-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="13e4e-169">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-170">Nieprzekraczalny limit</span><span class="sxs-lookup"><span data-stu-id="13e4e-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="13e4e-171">To pole można edytować i jest dostępne tylko w wierszach oferty opartej na projekcie z metodą rozliczania **Czas i amteriał**.</span><span class="sxs-lookup"><span data-stu-id="13e4e-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="13e4e-172">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13e4e-173">Budżet klienta</span><span class="sxs-lookup"><span data-stu-id="13e4e-173">Customer Budget</span></span> | <span data-ttu-id="13e4e-174">Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="13e4e-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="13e4e-175">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="13e4e-176">Reguły sprawdzania poprawności dla pól na karcie Ogólne w wierszach oferty opartej na projektach</span><span class="sxs-lookup"><span data-stu-id="13e4e-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="13e4e-177">**Reguła 1**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli jest ustawione na **Wszystkie zadania projektu**, projekt jest uwzględniany w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="13e4e-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="13e4e-178">**Reguła 2**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli ustawiono je na **Wszystkie zadania projektu**, projekt i dana klasa transakcji mogą być uwzględnione tylko w jednym wierszu oferty opartej na projekcie w ofercie.</span><span class="sxs-lookup"><span data-stu-id="13e4e-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="13e4e-179">**Reguła 3**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli ustawiono je na **Tylko wybrane zadania projektu**, projekt i dana klasa transakcji mogą być uwzględnione w wielu wierszach oferty opartej na projekcie w ofercie.</span><span class="sxs-lookup"><span data-stu-id="13e4e-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="13e4e-180">**Reguła 4**: Jeśli szansa sprzedaży zawiera wiele ofert, między różnymi ofertami można odwoływać się do tego samego projektu i zawierać tę samą klasę transakcji.</span><span class="sxs-lookup"><span data-stu-id="13e4e-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="13e4e-181">**Zasada 5**: Jeśli oferty nie należą do tej samej szansy sprzedaży, nie mogą zawierać tej samej klasy projektów i transakcji.</span><span class="sxs-lookup"><span data-stu-id="13e4e-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="13e4e-182">
                    <strong>Szansa sprzedaży</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="13e4e-183">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="13e4e-184">
                    <strong>Wiersz oferty</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="13e4e-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="13e4e-186">
                    <strong>Uwzględnione zadania</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="13e4e-187">
                    <strong>Uwzględnij czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="13e4e-188">
                    <strong>Uwzględnij wydatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="13e4e-189">
                    <strong>Dołącz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="13e4e-190">
                    <strong>Opłata</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="13e4e-191">
                    <strong>Prawidłowe/nieprawidłowe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="13e4e-192">
                    <strong>Przyczyna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13e4e-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-193">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-194">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-195">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-196">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-197">Pusty</span><span class="sxs-lookup"><span data-stu-id="13e4e-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-198">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-199">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-200">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-201">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-202">Naruszenie reguły nr 2.</span><span class="sxs-lookup"><span data-stu-id="13e4e-202">Violation of Rule #2.</span></span> <span data-ttu-id="13e4e-203">Czas, wydatek i opłaty w projekcie P1 są uwzględniane w wierszach oferty QL1, jak i QL2.</span><span class="sxs-lookup"><span data-stu-id="13e4e-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-204">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-205">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-206">QL2</span><span class="sxs-lookup"><span data-stu-id="13e4e-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-207">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-208">Pusty</span><span class="sxs-lookup"><span data-stu-id="13e4e-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-209">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-210">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-211">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="13e4e-212">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-213">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-214">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-215">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-216">Pusty</span><span class="sxs-lookup"><span data-stu-id="13e4e-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-217">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-218">No</span><span class="sxs-lookup"><span data-stu-id="13e4e-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-219">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-220">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-221">Naruszenie reguły nr 2.</span><span class="sxs-lookup"><span data-stu-id="13e4e-221">Violation of Rule #2.</span></span> <span data-ttu-id="13e4e-222">Czas i opłaty w projekcie P1 są uwzględniane w wierszach oferty QL1, jak i QL2.</span><span class="sxs-lookup"><span data-stu-id="13e4e-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-223">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-224">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-225">QL2</span><span class="sxs-lookup"><span data-stu-id="13e4e-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-226">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-227">Pusty</span><span class="sxs-lookup"><span data-stu-id="13e4e-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-228">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-229">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-230">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-231">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-232">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-233">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-234">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-235">Pusty</span><span class="sxs-lookup"><span data-stu-id="13e4e-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-236">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-237">No</span><span class="sxs-lookup"><span data-stu-id="13e4e-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-238">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-239">Prawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="13e4e-240">Godziny i opłaty z projektu P1 są zawarte w QL1.</span><span class="sxs-lookup"><span data-stu-id="13e4e-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="13e4e-241">Wydatki projektowe w ramach P1 są zawarte w QL2.</span><span class="sxs-lookup"><span data-stu-id="13e4e-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="13e4e-242">W żadnym wierszu oferty nie ma nakładania się wartości i wszystko jest poprawne.</span><span class="sxs-lookup"><span data-stu-id="13e4e-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-243">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-244">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-245">QL2</span><span class="sxs-lookup"><span data-stu-id="13e4e-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-246">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-247">Pusty</span><span class="sxs-lookup"><span data-stu-id="13e4e-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-248">No</span><span class="sxs-lookup"><span data-stu-id="13e4e-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-249">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-250">No</span><span class="sxs-lookup"><span data-stu-id="13e4e-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="13e4e-251">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-252">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-253">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-254">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-255">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="13e4e-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-256">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-257">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-258">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-259">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-260">Naruszenie reguły nr 2 powyżej</span><span class="sxs-lookup"><span data-stu-id="13e4e-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="13e4e-261">Q1 zawiera czas, koszty i opłaty w podzbiorze zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="13e4e-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="13e4e-262">QL2 zawiera czas, wydatki i opłaty dla całego projektu P1 i pokrywa się ze składnikiem, który został zamieszczony w Q1.</span><span class="sxs-lookup"><span data-stu-id="13e4e-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-263">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-264">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-265">QL2</span><span class="sxs-lookup"><span data-stu-id="13e4e-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-266">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-267">Pusty</span><span class="sxs-lookup"><span data-stu-id="13e4e-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-268">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-269">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-270">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-271">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-272">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-273">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-274">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-275">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="13e4e-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-276">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-277">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-278">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-279">Prawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-280">Zgodnie z reguła nr 3 powyżej,</span><span class="sxs-lookup"><span data-stu-id="13e4e-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="13e4e-281">Q1 zawiera czas, koszty i opłaty w podzbiorze zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="13e4e-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="13e4e-282">QL2 zawiera czas, koszty i opłaty dla podzbioru zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="13e4e-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="13e4e-283">Jedyne dodatkowe sprawdzanie poprawności w tym podzbiorze zadań na QL1, który różni się od podzbioru w QL2.</span><span class="sxs-lookup"><span data-stu-id="13e4e-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="13e4e-284">Dzięki temu nie występuje nakładanie się.</span><span class="sxs-lookup"><span data-stu-id="13e4e-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="13e4e-285">Jest to wykonywane przez system podczas kojarzenia zadań.</span><span class="sxs-lookup"><span data-stu-id="13e4e-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-286">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-287">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-288">QL2</span><span class="sxs-lookup"><span data-stu-id="13e4e-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-289">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-290">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="13e4e-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-291">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-292">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-293">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="13e4e-294">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-295">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-296">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-297">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-298">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="13e4e-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-299">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-300">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-301">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="13e4e-302">Prawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-303">Na podstawie reguły nr 5, Q1 i Q2 to dwie oferty z tej samej szansy sprzedaży, przez co obydwa te elementy mogą szacować dla tych samych składników projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-304">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-305">K2</span><span class="sxs-lookup"><span data-stu-id="13e4e-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-306">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-307">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-308">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="13e4e-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-309">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-310">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-311">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="13e4e-312">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-313">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-314">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-315">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-316">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="13e4e-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-317">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-318">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-319">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="13e4e-320">Prawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13e4e-321">Na podstawie reguły nr 4, Q1 i Q2 to dwie oferty z różnych szans sprzedaży, przez co obydwa te elementy nie mogą szacować dla tych samych składników projektu.</span><span class="sxs-lookup"><span data-stu-id="13e4e-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="13e4e-322">O2</span><span class="sxs-lookup"><span data-stu-id="13e4e-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13e4e-323">K1</span><span class="sxs-lookup"><span data-stu-id="13e4e-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-324">QL1</span><span class="sxs-lookup"><span data-stu-id="13e4e-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-325">O1</span><span class="sxs-lookup"><span data-stu-id="13e4e-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="13e4e-326">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="13e4e-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-327">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="13e4e-328">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="13e4e-329">Tak</span><span class="sxs-lookup"><span data-stu-id="13e4e-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="13e4e-330">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="13e4e-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]