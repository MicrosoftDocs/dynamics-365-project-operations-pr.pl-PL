---
title: Omówienie wierszy oferty opartej na projekcie
description: Ten temat zawiera informacje o korzystaniu z wiersza oferty opartej na projekcie w pracy projektowej.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858711"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="83114-103">Omówienie wierszy oferty opartej na projekcie</span><span class="sxs-lookup"><span data-stu-id="83114-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="83114-104">_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_</span><span class="sxs-lookup"><span data-stu-id="83114-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="83114-105">Wiersze oferty opartej na projekcie są utworzone w celu ułatwienia oceny pracy nad projektem w momencie zakontraktowania.</span><span class="sxs-lookup"><span data-stu-id="83114-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="83114-106">Struktura wiersza oferty opartej na projekcie jest przedłużana na potrzeby oszacowań projektu z następującymi pojęciami:</span><span class="sxs-lookup"><span data-stu-id="83114-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="83114-107">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="83114-107">Billing Method</span></span>
- <span data-ttu-id="83114-108">Mapowanie projektów i zadań</span><span class="sxs-lookup"><span data-stu-id="83114-108">Project and Task Mapping</span></span>
- <span data-ttu-id="83114-109">Dołączone klasy transakcji</span><span class="sxs-lookup"><span data-stu-id="83114-109">Included Transaction classes</span></span>
- <span data-ttu-id="83114-110">Nieprzekraczalny limit</span><span class="sxs-lookup"><span data-stu-id="83114-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="83114-111">Konfiguracja odpłatności</span><span class="sxs-lookup"><span data-stu-id="83114-111">Chargeability setup</span></span>
- <span data-ttu-id="83114-112">Szacowanie przy użyciu szczegółów wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="83114-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="83114-113">Klienci wierszy oferty</span><span class="sxs-lookup"><span data-stu-id="83114-113">Quote line Customers</span></span>

<span data-ttu-id="83114-114">Poniższa tabela zawiera informacje o polach na karcie **Ogólne** w wierszu oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="83114-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="83114-115">Te pola pomagają skonfigurować podstawę dla konkretnego szacunkowego oszacowania pracy projektowej.</span><span class="sxs-lookup"><span data-stu-id="83114-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="83114-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="83114-116">**Field**</span></span> | <span data-ttu-id="83114-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="83114-117">**Description**</span></span> | <span data-ttu-id="83114-118">**Wpływ zmian w dalszych etapach**</span><span class="sxs-lookup"><span data-stu-id="83114-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="83114-119">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="83114-119">Name</span></span> | <span data-ttu-id="83114-120">Nazwa wiersza oferty, która pomaga zidentyfikować dyskretny składnik wyceny, która jest szacowana.</span><span class="sxs-lookup"><span data-stu-id="83114-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="83114-121">Po wykorzystaniu oferty wartość pola jest kopiowana do tworzonego kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="83114-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-122">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="83114-122">Billing Method</span></span> | <span data-ttu-id="83114-123">Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="83114-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="83114-124">To pole obejmuje dwa główne modele kontraktów obsługiwane przez Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="83114-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="83114-125">- Stała cena</span><span class="sxs-lookup"><span data-stu-id="83114-125">- Fixed price</span></span></br><span data-ttu-id="83114-126">- Czas i materiał.</span><span class="sxs-lookup"><span data-stu-id="83114-126">- Time and material.</span></span>| <span data-ttu-id="83114-127">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-128">Project</span><span class="sxs-lookup"><span data-stu-id="83114-128">Project</span></span> | <span data-ttu-id="83114-129">Użyj tego opcjonalnego pola w celu zidentyfikowania projektu, który będzie używany do dostarczania pracy w ramach tego zakontraktowania.</span><span class="sxs-lookup"><span data-stu-id="83114-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="83114-130">Podczas mapowania projektu na wiersz oferty pomocne jest konfigurowanie zadań odpłatnych, a także wprowadzenie oceny opartej na projekcie z wiersza oferty jako szczegółów wiersza oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="83114-131">Jeśli projekt nie jest mapowany na wiersz oferty opartej na projekcie, szacunek powinien zostać utworzony ręcznie, tworząc szczegóły poszczególnych wierszy oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="83114-132">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="83114-133">Uwzględnione zadania</span><span class="sxs-lookup"><span data-stu-id="83114-133">Included Tasks</span></span> | <span data-ttu-id="83114-134">Wskazuje, czy dany wiersz oferty jest używany we wszystkich zadaniach wybranego projektu.</span><span class="sxs-lookup"><span data-stu-id="83114-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="83114-135">To pole ma następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="83114-135">This field has the following possible values:</span></span></br><span data-ttu-id="83114-136">- Wszystkie zadania projektu</span><span class="sxs-lookup"><span data-stu-id="83114-136">- All project tasks</span></span></br><span data-ttu-id="83114-137">- Tylko wybrane zadania projektu</span><span class="sxs-lookup"><span data-stu-id="83114-137">- Selected project tasks only</span></span></br><span data-ttu-id="83114-138">W tym polu jest wyświetlona pusta wartość, która jest równoznaczna z opcją **Wszystkie zadania projektu**.</span><span class="sxs-lookup"><span data-stu-id="83114-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="83114-139">Gdy wybrana jest opcja **Tylko wybrane zadania projektu** na stronie projektu, karta **Konfiguracja rozliczania zadań** umożliwia wybranie określonych zadań w celu skojarzenia ich z tym wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="83114-140">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-141">Uwzględnij czas</span><span class="sxs-lookup"><span data-stu-id="83114-141">Include Time</span></span> | <span data-ttu-id="83114-142">Wartość **Tak**/**Nie** wskazuje, czy transakcje czasowe lub koszty pracy w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-143">Flaga **Nie** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-144">Flaga **Tak** wskazuje, że transakcje czasu lub koszty pracy w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="83114-145">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-146">Uwzględnij wydatek</span><span class="sxs-lookup"><span data-stu-id="83114-146">Include Expense</span></span> | <span data-ttu-id="83114-147">Wartość **Tak**/**Nie** wskazuje, czy wydatki w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-148">Flaga **Nie** wskazuje, że koszty wydatków w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-149">Flaga **Tak** wskazuje, że koszty wydatków w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="83114-150">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-151">Uwzględnij materiał</span><span class="sxs-lookup"><span data-stu-id="83114-151">Include Material</span></span> | <span data-ttu-id="83114-152">Wartość **Tak**/**Nie** wskazuje, czy materiały w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-153">Wartość **Nie** oznacza, że koszty materiałów nie zostaną uwzględnione w szacunkach w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-154">Wartość **Tak** oznacza, że koszty materiałów zostaną uwzględnione w szacunkach w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="83114-155">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-156">Uwzględnij opłatę</span><span class="sxs-lookup"><span data-stu-id="83114-156">Include Fee</span></span> | <span data-ttu-id="83114-157">Wartość **Tak**/**Nie** wskazuje, czy opłaty w wybranym projekcie zostaną uwzględnione w oszacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-158">Wartość **Nie** wskazuje, że opłaty w wybranym projekcie nie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="83114-159">Wartość **Tak** wskazuje, że opłaty w wybranym projekcie zostaną uwzględnione w szacowaniu w tym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="83114-160">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-161">Oferowana kwota</span><span class="sxs-lookup"><span data-stu-id="83114-161">Quoted Amount</span></span> | <span data-ttu-id="83114-162">Jest to kwota, która zostanie podana klientowi za całą pracę prognozowaną w tym wierszu oferty opartym na projekcie.</span><span class="sxs-lookup"><span data-stu-id="83114-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="83114-163">Gdy oferta jest tworzona z szansy sprzedaży, ta wartość jest kopiowana z odpowiedniego pola **Budżet klienta** w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="83114-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="83114-164">Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="83114-165">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-166">Szacowany podatek</span><span class="sxs-lookup"><span data-stu-id="83114-166">Estimated Tax</span></span> | <span data-ttu-id="83114-167">Jest to pole, które można edytować, aby dodać szacowaną kwotę podatku w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="83114-168">Kiedy wiersz oferty opartej na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podatku podanej w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="83114-169">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-170">Oferowana kwota po opodatkowaniu</span><span class="sxs-lookup"><span data-stu-id="83114-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="83114-171">To pole stanowi kwotę wiersza oferty po zaliczeniu podatku i jest w trybie tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="83114-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="83114-172">Kwota w tym polu jest obliczana jako *Oferowana kwota z podatkiem*.</span><span class="sxs-lookup"><span data-stu-id="83114-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="83114-173">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-174">Nieprzekraczalny limit</span><span class="sxs-lookup"><span data-stu-id="83114-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="83114-175">To pole można edytować i jest dostępne tylko w wierszach oferty opartej na projekcie z metodą rozliczania **Czas i amteriał**.</span><span class="sxs-lookup"><span data-stu-id="83114-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="83114-176">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="83114-177">Budżet klienta</span><span class="sxs-lookup"><span data-stu-id="83114-177">Customer Budget</span></span> | <span data-ttu-id="83114-178">Gdy oferta jest tworzona z szansy sprzedaży, to pole jest kopiowane z odpowiedniego pola w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="83114-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="83114-179">Ta wartość jest kopiowana do wiersza umowy dotyczącej projektu, który jest tworzony na podstawie tego wiersza oferty, gdy oferta jest wygrywana.</span><span class="sxs-lookup"><span data-stu-id="83114-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="83114-180">Reguły sprawdzania poprawności dla pól na karcie Ogólne w wierszach oferty opartej na projektach</span><span class="sxs-lookup"><span data-stu-id="83114-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="83114-181">**Reguła 1**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli jest ustawione na **Wszystkie zadania projektu**, projekt jest uwzględniany w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="83114-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="83114-182">**Reguła 2**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli ustawiono je na **Wszystkie zadania projektu**, projekt i dana klasa transakcji mogą być uwzględnione tylko w jednym wierszu oferty opartej na projekcie w ofercie.</span><span class="sxs-lookup"><span data-stu-id="83114-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="83114-183">**Reguła 3**: Jeśli pole **Uwzględnione zadania** jest puste lub jeśli ustawiono je na **Tylko wybrane zadania projektu**, projekt i dana klasa transakcji mogą być uwzględnione w wielu wierszach oferty opartej na projekcie w ofercie.</span><span class="sxs-lookup"><span data-stu-id="83114-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="83114-184">**Reguła 4**: Jeśli szansa sprzedaży zawiera wiele ofert, między różnymi ofertami można odwoływać się do tego samego projektu i zawierać tę samą klasę transakcji.</span><span class="sxs-lookup"><span data-stu-id="83114-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="83114-185">**Zasada 5**: Jeśli oferty nie należą do tej samej szansy sprzedaży, nie mogą zawierać tej samej klasy projektów i transakcji.</span><span class="sxs-lookup"><span data-stu-id="83114-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="83114-186">
                    <strong>Szansa sprzedaży</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="83114-187">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="83114-188">
                    <strong>Wiersz oferty</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="83114-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="83114-190">
                    <strong>Uwzględnione zadania</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="83114-191">
                    <strong>Uwzględnij czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="83114-192">
                    <strong>Uwzględnij wydatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="83114-193">
                    <strong>Uwzględnij materiał</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="83114-194">
                    <strong>Uwzględnij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="83114-195">
                    <strong>Opłata</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="83114-196">
                    <strong>Prawidłowe/nieprawidłowe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="83114-197">
                    <strong>Przyczyna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83114-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-198">O1</span><span class="sxs-lookup"><span data-stu-id="83114-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-199">K1</span><span class="sxs-lookup"><span data-stu-id="83114-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-200">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-201">O1</span><span class="sxs-lookup"><span data-stu-id="83114-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-202">Pusty</span><span class="sxs-lookup"><span data-stu-id="83114-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-203">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-204">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-205">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-206">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-207">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="83114-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-208">Naruszenie reguły nr 2.</span><span class="sxs-lookup"><span data-stu-id="83114-208">Violation of Rule #2.</span></span> <span data-ttu-id="83114-209">Czas, wydatek i opłaty w projekcie P1 są uwzględniane w wierszach oferty QL1, jak i QL2</span><span class="sxs-lookup"><span data-stu-id="83114-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-210">O1</span><span class="sxs-lookup"><span data-stu-id="83114-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-211">K1</span><span class="sxs-lookup"><span data-stu-id="83114-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-212">QL2</span><span class="sxs-lookup"><span data-stu-id="83114-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-213">O1</span><span class="sxs-lookup"><span data-stu-id="83114-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-214">Pusty</span><span class="sxs-lookup"><span data-stu-id="83114-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-215">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-216">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-217">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-218">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-219">O1</span><span class="sxs-lookup"><span data-stu-id="83114-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-220">K1</span><span class="sxs-lookup"><span data-stu-id="83114-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-221">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-222">O1</span><span class="sxs-lookup"><span data-stu-id="83114-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-223">Pusty</span><span class="sxs-lookup"><span data-stu-id="83114-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-224">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-225">No</span><span class="sxs-lookup"><span data-stu-id="83114-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-226">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-227">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-228">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="83114-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-229">Naruszenie reguły nr 2.</span><span class="sxs-lookup"><span data-stu-id="83114-229">Violation of Rule #2.</span></span> <span data-ttu-id="83114-230">Czas, materiał i opłaty w projekcie P1 są uwzględniane w wierszach oferty QL1, jak i QL2</span><span class="sxs-lookup"><span data-stu-id="83114-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-231">O1</span><span class="sxs-lookup"><span data-stu-id="83114-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-232">K1</span><span class="sxs-lookup"><span data-stu-id="83114-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-233">QL2</span><span class="sxs-lookup"><span data-stu-id="83114-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-234">O1</span><span class="sxs-lookup"><span data-stu-id="83114-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-235">Pusty</span><span class="sxs-lookup"><span data-stu-id="83114-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-236">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-237">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-238">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-239">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-240">O1</span><span class="sxs-lookup"><span data-stu-id="83114-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-241">K1</span><span class="sxs-lookup"><span data-stu-id="83114-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-242">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-243">O1</span><span class="sxs-lookup"><span data-stu-id="83114-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-244">Pusty</span><span class="sxs-lookup"><span data-stu-id="83114-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-245">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-246">No</span><span class="sxs-lookup"><span data-stu-id="83114-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-247">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-248">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-249">Prawidłowy</span><span class="sxs-lookup"><span data-stu-id="83114-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-250">Czas, materiał i opłaty w projekcie P1 są uwzględnione w QL1</span><span class="sxs-lookup"><span data-stu-id="83114-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="83114-251">Wydatki projektowe w ramach P1 są zawarte w QL2</span><span class="sxs-lookup"><span data-stu-id="83114-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="83114-252">Nie pokrywają się w tym, co jest zawarte w każdym wierszu oferty, a zatem jest ważne.</span><span class="sxs-lookup"><span data-stu-id="83114-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-253">O1</span><span class="sxs-lookup"><span data-stu-id="83114-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-254">K1</span><span class="sxs-lookup"><span data-stu-id="83114-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-255">QL2</span><span class="sxs-lookup"><span data-stu-id="83114-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-256">O1</span><span class="sxs-lookup"><span data-stu-id="83114-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-257">Pusty</span><span class="sxs-lookup"><span data-stu-id="83114-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-258">No</span><span class="sxs-lookup"><span data-stu-id="83114-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-259">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-260">No</span><span class="sxs-lookup"><span data-stu-id="83114-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-261">No</span><span class="sxs-lookup"><span data-stu-id="83114-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-262">O1</span><span class="sxs-lookup"><span data-stu-id="83114-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-263">K1</span><span class="sxs-lookup"><span data-stu-id="83114-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-264">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-265">O1</span><span class="sxs-lookup"><span data-stu-id="83114-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-266">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="83114-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-267">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-268">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-269">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-270">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-271">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="83114-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-272">Naruszenie reguły nr 2</span><span class="sxs-lookup"><span data-stu-id="83114-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="83114-273">Q1 obejmuje czas, materiał, wydatki i opłaty dla podzbioru zadań w projekcie P1</span><span class="sxs-lookup"><span data-stu-id="83114-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="83114-274">QL2 obejmuje czas, wydatki i opłaty za cały projekt P1, a zatem pokrywa się z tym, co jest uwzględnione w pierwszym kwartale.</span><span class="sxs-lookup"><span data-stu-id="83114-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-275">O1</span><span class="sxs-lookup"><span data-stu-id="83114-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-276">K1</span><span class="sxs-lookup"><span data-stu-id="83114-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-277">QL2</span><span class="sxs-lookup"><span data-stu-id="83114-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-278">O1</span><span class="sxs-lookup"><span data-stu-id="83114-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-279">Pusty</span><span class="sxs-lookup"><span data-stu-id="83114-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-280">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-281">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-282">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-283">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-284">O1</span><span class="sxs-lookup"><span data-stu-id="83114-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-285">K1</span><span class="sxs-lookup"><span data-stu-id="83114-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-286">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-287">O1</span><span class="sxs-lookup"><span data-stu-id="83114-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-288">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="83114-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-289">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-290">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-291">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-292">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-293">Prawidłowy</span><span class="sxs-lookup"><span data-stu-id="83114-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-294">Na regułę #3,</span><span class="sxs-lookup"><span data-stu-id="83114-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="83114-295">Q1 obejmuje czas, materiał, wydatki i opłaty dla podzbioru zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="83114-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="83114-296">QL2 obejmuje czas, materiały, wydatki i opłaty dla podzbioru zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="83114-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="83114-297">Jedyna dodatkowa walidacja dotyczy podzbioru zadań na QL1, który różni się od podzbioru zadań na QL2, aby upewnić się, że nie nakładają się na siebie.</span><span class="sxs-lookup"><span data-stu-id="83114-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="83114-298">Jest to wykonywane przez system podczas kojarzenia zadań.</span><span class="sxs-lookup"><span data-stu-id="83114-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-299">O1</span><span class="sxs-lookup"><span data-stu-id="83114-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-300">K1</span><span class="sxs-lookup"><span data-stu-id="83114-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-301">QL2</span><span class="sxs-lookup"><span data-stu-id="83114-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-302">O1</span><span class="sxs-lookup"><span data-stu-id="83114-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-303">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="83114-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-304">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-305">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-306">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-307">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-308">O1</span><span class="sxs-lookup"><span data-stu-id="83114-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-309">K1</span><span class="sxs-lookup"><span data-stu-id="83114-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-310">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-311">O1</span><span class="sxs-lookup"><span data-stu-id="83114-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-312">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="83114-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-313">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-314">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-315">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-316">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-317">Prawidłowy</span><span class="sxs-lookup"><span data-stu-id="83114-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-318">Zgodnie z regułą # 5, Q1 i Q2 to dwie oferty dotyczące tej samej możliwości, więc obie mogą szacować te same komponenty projektu.</span><span class="sxs-lookup"><span data-stu-id="83114-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-319">O1</span><span class="sxs-lookup"><span data-stu-id="83114-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-320">K2</span><span class="sxs-lookup"><span data-stu-id="83114-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-321">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-322">O1</span><span class="sxs-lookup"><span data-stu-id="83114-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-323">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="83114-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-324">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-325">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-326">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-327">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-328">O1</span><span class="sxs-lookup"><span data-stu-id="83114-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-329">K1</span><span class="sxs-lookup"><span data-stu-id="83114-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-330">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-331">O1</span><span class="sxs-lookup"><span data-stu-id="83114-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-332">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="83114-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-333">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-334">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-335">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-336">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-337">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="83114-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83114-338">Zgodnie z regułą # 4, Q1 i Q2 to dwie wyceny różnych możliwości, więc nie mogą oszacować tych samych komponentów tego samego projektu.</span><span class="sxs-lookup"><span data-stu-id="83114-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="83114-339">O2</span><span class="sxs-lookup"><span data-stu-id="83114-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="83114-340">K1</span><span class="sxs-lookup"><span data-stu-id="83114-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="83114-341">QL1</span><span class="sxs-lookup"><span data-stu-id="83114-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-342">O1</span><span class="sxs-lookup"><span data-stu-id="83114-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="83114-343">Wszystkie zadania projektu lub puste</span><span class="sxs-lookup"><span data-stu-id="83114-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="83114-344">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="83114-345">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="83114-346">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="83114-347">Tak</span><span class="sxs-lookup"><span data-stu-id="83114-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
