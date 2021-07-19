---
title: Omówienie pozycji kontraktu opartego na projekcie
description: Ten temat zawiera informacje o pracy z pozycjami kontraktów opartych na projektach.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369929"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="0468d-103">Omówienie pozycji kontraktu opartego na projekcie</span><span class="sxs-lookup"><span data-stu-id="0468d-103">Project-based contract lines overview</span></span>

<span data-ttu-id="0468d-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="0468d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0468d-105">Linie umowy oparte na projekcie w rozwiązaniu Dynamics 365 Project Operations są przeznaczone do przechowywania szacunkowych i rozliczeniowych umów dla określonych komponentów pracy projektowej na zlecenie.</span><span class="sxs-lookup"><span data-stu-id="0468d-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="0468d-106">Struktura pozycji kontraktu opartej na projekcie jest rozszerzana na oszacowania projektów i scenariusze fakturowania przy użyciu następujących koncepcji:</span><span class="sxs-lookup"><span data-stu-id="0468d-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="0468d-107">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="0468d-107">Billing method</span></span>
- <span data-ttu-id="0468d-108">Mapowanie projektów i zadań</span><span class="sxs-lookup"><span data-stu-id="0468d-108">Project and task mapping</span></span>
- <span data-ttu-id="0468d-109">Dołączone klasy transakcji</span><span class="sxs-lookup"><span data-stu-id="0468d-109">Included transaction classes</span></span>
- <span data-ttu-id="0468d-110">Nieprzekraczalny limit</span><span class="sxs-lookup"><span data-stu-id="0468d-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="0468d-111">Konfiguracja odpłatności</span><span class="sxs-lookup"><span data-stu-id="0468d-111">Chargeability setup</span></span>
- <span data-ttu-id="0468d-112">Oszacowania przy użyciu szczegółów pozycji kontraktu</span><span class="sxs-lookup"><span data-stu-id="0468d-112">Estimates using contract line details</span></span>
- <span data-ttu-id="0468d-113">Klient pozycji kontraktu</span><span class="sxs-lookup"><span data-stu-id="0468d-113">Contract line customers</span></span>

<span data-ttu-id="0468d-114">Poniższa tabela zawiera pola na karcie **Ogólne** w wierszach kontraktu opartego na projektach, które pomagają w konfigurowaniu podstawy do szczegółowego oszacowania kosztów i sposobu fakturowania dla pracy opartej na projektach.</span><span class="sxs-lookup"><span data-stu-id="0468d-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="0468d-115">Pole</span><span class="sxs-lookup"><span data-stu-id="0468d-115">Field</span></span> | <span data-ttu-id="0468d-116">Opis</span><span class="sxs-lookup"><span data-stu-id="0468d-116">Description</span></span> | <span data-ttu-id="0468d-117">Wpływ zmian w dalszych etapach</span><span class="sxs-lookup"><span data-stu-id="0468d-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0468d-118">**Nazwa/nazwisko**</span><span class="sxs-lookup"><span data-stu-id="0468d-118">**Name**</span></span> | <span data-ttu-id="0468d-119">Nazwa pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-119">Name of the contract line.</span></span> <span data-ttu-id="0468d-120">To identyfikuje dyskretny składnik szacowanego kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="0468d-121">W przypadku kontraktu projektu utworzonego z oferty ta wartość jest kopiowana z odpowiedniej wartości wiersza oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="0468d-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="0468d-122">Nazwa skopiowana do wiersza faktury projektu, który jest tworzony na podstawie tej pozycji kontraktu podczas tworzenia faktury.</span><span class="sxs-lookup"><span data-stu-id="0468d-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="0468d-123">**Metoda rozliczania**</span><span class="sxs-lookup"><span data-stu-id="0468d-123">**Billing Method**</span></span> | <span data-ttu-id="0468d-124">W umowie dotyczącej projektu utworzonej na podstawie oferty ta wartość jest kopiowana z odpowiedniego pola w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="0468d-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="0468d-125">Jest to zestaw opcji reprezentujący dwa główne modele zamawiające, które są obsługiwane przez Project Operations:</span><span class="sxs-lookup"><span data-stu-id="0468d-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="0468d-126">- **Stała cena**</span><span class="sxs-lookup"><span data-stu-id="0468d-126">- **Fixed Price**</span></span></br><span data-ttu-id="0468d-127">- **Czas i materiał**</span><span class="sxs-lookup"><span data-stu-id="0468d-127">- **Time and Material**</span></span> | <span data-ttu-id="0468d-128">Na podstawie metody fakturowania przywoływanego wiersza kontraktu zostanie przetworzona transakcja rzeczywista.</span><span class="sxs-lookup"><span data-stu-id="0468d-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="0468d-129">Jeśli dana pozycja kontraktu zawiera metodę fakturowania czasu i materiału, tworzone są rekordy kosztów i niezafakturowanego rekordów sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="0468d-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="0468d-130">Jeśli pozycja kontraktu, do której odwołuje się wartość rzeczywista, ma metodę fakturowania z ceną ustaloną, zostanie utworzona tylko wartość rzeczywista kosztu.</span><span class="sxs-lookup"><span data-stu-id="0468d-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="0468d-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="0468d-131">**Project**</span></span> | <span data-ttu-id="0468d-132">To pole służy do identyfikowania projektu, który będzie używany do dostarczania pracy nad tym zakontraktowaniem.</span><span class="sxs-lookup"><span data-stu-id="0468d-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="0468d-133">Ta wartość będzie używana w połączeniu z **Uwzględnionymi zadaniami** i **Uwzględnionymi klasami transakcji** w celu rozstrzygnięcia odniesienia do wiersza umowy w rzeczywistym lub szacunkowym rekordzie wiersza.</span><span class="sxs-lookup"><span data-stu-id="0468d-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="0468d-134">**Uwzględnione zadania**</span><span class="sxs-lookup"><span data-stu-id="0468d-134">**Included Tasks**</span></span> | <span data-ttu-id="0468d-135">Wskazuje, czy dana pozycja kontraktu obejmuje wszystkie zadania projektu dla wybranego projektu, czy tylko podzestaw zadań.</span><span class="sxs-lookup"><span data-stu-id="0468d-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="0468d-136">To zestaw opcji o następujących możliwych wartościach:</span><span class="sxs-lookup"><span data-stu-id="0468d-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="0468d-137">- **Wszystkie zadania projektu**</span><span class="sxs-lookup"><span data-stu-id="0468d-137">- **All Project Tasks**</span></span></br><span data-ttu-id="0468d-138">- **Tylko wybrane zadania projektu**.</span><span class="sxs-lookup"><span data-stu-id="0468d-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="0468d-139">Pusta wartość w tym polu jest równa zaznaczeniu **Wszystkich zadań projektu**.</span><span class="sxs-lookup"><span data-stu-id="0468d-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="0468d-140">Jeśli wybrano opcję **Tylko wybrane zadania**, można wybrać określone zadania i skojarzyć je z tym wierszem umowy na karcie **Konfiguracja rozliczania zadań** na stronie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="0468d-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="0468d-141">Wartość jest używana w połączeniu z **Projekt** i **Uwzględnione klasy transakcji** w celu ustalenia odwołania do pozycji kontraktu w rekordzie rzeczywistym lub w wierszu szacowania.</span><span class="sxs-lookup"><span data-stu-id="0468d-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0468d-142">**Uwzględnij czas**</span><span class="sxs-lookup"><span data-stu-id="0468d-142">**Include Time**</span></span> | <span data-ttu-id="0468d-143">Wartość **Tak**/**Nie** wskazuje, czy w tej kolejce kontraktu zostaną uwzględnione transakcje czasu lub koszty pracy dla wybranego projektu.</span><span class="sxs-lookup"><span data-stu-id="0468d-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0468d-144">Wartość **Nie** oznacza, że transakcje godzinowe lub koszt robocizny nie zostaną uwzględnione w tej pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="0468d-145">Wartość **Tak** oznacza, że będą.</span><span class="sxs-lookup"><span data-stu-id="0468d-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="0468d-146">Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza.</span><span class="sxs-lookup"><span data-stu-id="0468d-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0468d-147">**Uwzględnij wydatek**</span><span class="sxs-lookup"><span data-stu-id="0468d-147">**Include Expense**</span></span> | <span data-ttu-id="0468d-148">Wartość **Tak**/**Nie** wskazuje, czy koszty związane z wybranym projektem zostaną uwzględnione w tej linii kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0468d-149">Wartość **Nie** oznacza, że koszt wydatków nie zostanie uwzględniony w tej pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="0468d-150">Wartość **Tak** oznacza, że będzie.</span><span class="sxs-lookup"><span data-stu-id="0468d-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="0468d-151">Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza.</span><span class="sxs-lookup"><span data-stu-id="0468d-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0468d-152">**Uwzględnij materiały**</span><span class="sxs-lookup"><span data-stu-id="0468d-152">**Include Materials**</span></span> | <span data-ttu-id="0468d-153">Wartość **Tak**/**Nie** wskazuje, czy materiały związane z wybranym projektem zostaną uwzględnione w tej linii kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0468d-154">Wartość **Nie** oznacza, że koszty materiałów nie zostaną uwzględnione w tej linii kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="0468d-155">Wartość **Tak** oznacza, że będzie.</span><span class="sxs-lookup"><span data-stu-id="0468d-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="0468d-156">Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza.</span><span class="sxs-lookup"><span data-stu-id="0468d-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0468d-157">**Uwzględnij opłatę**</span><span class="sxs-lookup"><span data-stu-id="0468d-157">**Include Fee**</span></span> | <span data-ttu-id="0468d-158">Wartość **Tak**/**Nie** wskazuje, czy opłaty związane z wybranym projektem zostaną uwzględnione w tej linii kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0468d-159">Wartość **Nie** oznacza, że opłaty nie będą uwzględnione w tej pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="0468d-160">Wartość **Tak** oznacza, że będą.</span><span class="sxs-lookup"><span data-stu-id="0468d-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="0468d-161">Ta wartość jest używana w połączeniu z projektem w celu rozwiązania odniesienia do wiersza kontraktu w rzeczywistym lub szacunkowym rekordzie wiersza.</span><span class="sxs-lookup"><span data-stu-id="0468d-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0468d-162">**Zakontraktowana kwota**</span><span class="sxs-lookup"><span data-stu-id="0468d-162">**Contracted Amount**</span></span> | <span data-ttu-id="0468d-163">W pozycji kontraktu o stałej cenie jest to wartość ustalona, która zostanie zafakturowana klientowi dla wszystkich składników pracy skojarzonych z daną pozycją kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="0468d-164">W pozycji umowy dotyczącej czasu i materiałów kwota ta jest szacunkową wartością tego, co zostanie zafakturowane klientowi za wszystkie składniki pracy związane z tą pozycją kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="0468d-165">W umowie dotyczącej projektu utworzonej na podstawie oferty ta wartość jest kopiowana z odpowiedniego pola w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="0468d-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="0468d-166">Kiedy pozycja kontraktu oparta na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane od kwoty podanej we wszystkich pozycjach kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="0468d-167">W przypadku, gdy pozycja kontraktu zawiera szczegółowe informacje o wierszach, ta wartość może zostać zmodyfikowana, zmieniając kwoty w szczegółach wiersza.</span><span class="sxs-lookup"><span data-stu-id="0468d-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="0468d-168">W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania kwoty przed podatkami dotyczącymi okresowych punktów kontrolnych rozliczania.</span><span class="sxs-lookup"><span data-stu-id="0468d-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="0468d-169">**Szacowany podatek**</span><span class="sxs-lookup"><span data-stu-id="0468d-169">**Estimated Tax**</span></span> | <span data-ttu-id="0468d-170">Użytkownik może edytować to pole, aby wprowadzić szacowaną kwotę podatku w pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="0468d-171">Kiedy pozycja kontraktu oparta na projekcie zawiera szczegółowe informacje o wierszach, to pole jest zablokowane do edycji i jest sumowane podatku od kwoty podanej we wszystkich pozycjach kontraktu.</span><span class="sxs-lookup"><span data-stu-id="0468d-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="0468d-172">W przypadku, gdy pozycja kontraktu zawiera szczegółowe informacje o wierszach, ta wartość może zostać zmodyfikowana, zmieniając kwoty podatku w szczegółach wiersza.</span><span class="sxs-lookup"><span data-stu-id="0468d-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="0468d-173">W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania podatków dotyczących okresowych punktów kontrolnych rozliczania.</span><span class="sxs-lookup"><span data-stu-id="0468d-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="0468d-174">**Zakontraktowana kwota po opodatkowaniu**</span><span class="sxs-lookup"><span data-stu-id="0468d-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="0468d-175">Zakontraktowana kwota pozycji kontraktu po opodatkowaniu.</span><span class="sxs-lookup"><span data-stu-id="0468d-175">The contract line amount after tax.</span></span> <span data-ttu-id="0468d-176">To pole jest tylko do odczytu i jest obliczane jako **Kwota w kontrakcie + podatek**.</span><span class="sxs-lookup"><span data-stu-id="0468d-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="0468d-177">W pozycji kontraktu o stałej cenie ta wartość jest używana do generowania okresowych punktów kontrolnych fakturowania.</span><span class="sxs-lookup"><span data-stu-id="0468d-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="0468d-178">**Nieprzekraczalny limit**</span><span class="sxs-lookup"><span data-stu-id="0468d-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="0468d-179">Użytkownik może edytować to pole, ale jest dostępne tylko w wierszach kontraktów opartych na projektach, które mają metodę fakturowania typu czas i materiały.</span><span class="sxs-lookup"><span data-stu-id="0468d-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="0468d-180">Użytkownik może edytować to pole.</span><span class="sxs-lookup"><span data-stu-id="0468d-180">The user can edit this field.</span></span> <span data-ttu-id="0468d-181">Kiedy rzeczywiste dane dotyczące czasu i materiałów odnoszą się do tej pozycji umowy pod względem czasu i materiałów, kwota rzeczywista jest oceniana w odniesieniu do nieprzekraczalnego limitu w linii umowy.</span><span class="sxs-lookup"><span data-stu-id="0468d-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="0468d-182">Ta ocena jest przeprowadzana po rozpoczęciu już zrealizowanych i zakontraktowanych kwot.</span><span class="sxs-lookup"><span data-stu-id="0468d-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="0468d-183">**Budżet klienta**</span><span class="sxs-lookup"><span data-stu-id="0468d-183">**Customer Budget**</span></span> | <span data-ttu-id="0468d-184">To pole jest edytowalne i jest kopiowane z odpowiedniego pola w wierszu oferty, jeśli umowa została utworzona na podstawie oferty.</span><span class="sxs-lookup"><span data-stu-id="0468d-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="0468d-185">To pole jest używane tylko do informowania i nie ma żadnych elementów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="0468d-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="0468d-186">Reguły sprawdzania poprawności opcji na karcie Ogólne w wierszach kontraktu opartego na projektach</span><span class="sxs-lookup"><span data-stu-id="0468d-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="0468d-187">Reguła 1: Jeśli pole **Uwzględnione zadania** jest puste lub ustawione na **Wszystkie zadania projektu**, wszystkie zadania projektu są uwzględniane w wierszu umowy.</span><span class="sxs-lookup"><span data-stu-id="0468d-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="0468d-188">Reguła 2. Gdy pole **Uwzględnione zadania** jest puste lub jawnie ustawione na **Wszystkie zadania projektu**, projekt i określona klasa transakcji mogą być uwzględnione tylko w jednym wierszu kontraktu opartym na projekcie.</span><span class="sxs-lookup"><span data-stu-id="0468d-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="0468d-189">Reguła 3. Gdy pole **Uwzględnione zadania** ustawione na **Tylko wybrane zadania projektu**, projekt i określona klasa transakcji mogą być uwzględnione tylko w wielu wierszach kontraktu opartego na projekcie.</span><span class="sxs-lookup"><span data-stu-id="0468d-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="0468d-190">
                    <strong>Kontrakt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0468d-191">
                    <strong>Pozycja kontraktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0468d-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="0468d-193">
                    <strong>Uwzględnione zadania</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0468d-194">
                    <strong>Uwzględnij czas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0468d-195">
                    <strong>Uwzględnij wydatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0468d-196">
                    <strong>IUwzględnij materiały</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0468d-197">
                    <strong>Uwzględnij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0468d-198">
                    <strong>Opłata</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="0468d-199">
                    <strong>Prawidłowe/nieprawidłowe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="0468d-200">
                    <strong>Przyczyna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0468d-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-201">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-202">CL1</span><span class="sxs-lookup"><span data-stu-id="0468d-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-203">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-204">Pusty</span><span class="sxs-lookup"><span data-stu-id="0468d-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-205">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-206">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-207">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-208">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-209">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="0468d-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-210">Naruszenie reguły nr 2.</span><span class="sxs-lookup"><span data-stu-id="0468d-210">Violation of Rule #2.</span></span> <span data-ttu-id="0468d-211">Czas, koszt, materiały i opłaty w projekcie P1 są uwzględnione zarówno w wierszach kontraktu CL1, jak i w CL2.</span><span class="sxs-lookup"><span data-stu-id="0468d-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-212">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-213">CL2</span><span class="sxs-lookup"><span data-stu-id="0468d-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-214">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-215">Pusty</span><span class="sxs-lookup"><span data-stu-id="0468d-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-216">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-217">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-218">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-219">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-220">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-221">CL1</span><span class="sxs-lookup"><span data-stu-id="0468d-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-222">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-223">Pusty</span><span class="sxs-lookup"><span data-stu-id="0468d-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-224">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-225">No</span><span class="sxs-lookup"><span data-stu-id="0468d-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-226">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-227">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-228">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="0468d-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-229">Naruszenie reguły nr 2.</span><span class="sxs-lookup"><span data-stu-id="0468d-229">Violation of Rule #2.</span></span> <span data-ttu-id="0468d-230">Czas, materiały i opłaty w projekcie P1 są uwzględnione zarówno w wierszach kontraktu CL1, jak i w cl2.</span><span class="sxs-lookup"><span data-stu-id="0468d-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-231">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-232">CL2</span><span class="sxs-lookup"><span data-stu-id="0468d-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-233">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-234">Pusty</span><span class="sxs-lookup"><span data-stu-id="0468d-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-235">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-236">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-237">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-238">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-239">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-240">CL1</span><span class="sxs-lookup"><span data-stu-id="0468d-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-241">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-242">Pusty</span><span class="sxs-lookup"><span data-stu-id="0468d-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-243">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-244">No</span><span class="sxs-lookup"><span data-stu-id="0468d-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-245">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-246">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-247">Prawidłowy</span><span class="sxs-lookup"><span data-stu-id="0468d-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-248">Czas, materiały i opłaty w projekcie P1 są uwzględnione w CL1.</span><span class="sxs-lookup"><span data-stu-id="0468d-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="0468d-249">Wydatki projektowe w ramach P1 są zawarte w CL2.</span><span class="sxs-lookup"><span data-stu-id="0468d-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="0468d-250">Nie pokrywają się w tym, co jest zawarte w każdym wierszu kontraktu, a zatem jest ważne.</span><span class="sxs-lookup"><span data-stu-id="0468d-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-251">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-252">CL2</span><span class="sxs-lookup"><span data-stu-id="0468d-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-253">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-254">Pusty</span><span class="sxs-lookup"><span data-stu-id="0468d-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-255">No</span><span class="sxs-lookup"><span data-stu-id="0468d-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-256">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-257">No</span><span class="sxs-lookup"><span data-stu-id="0468d-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-258">No</span><span class="sxs-lookup"><span data-stu-id="0468d-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-259">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-260">CL1</span><span class="sxs-lookup"><span data-stu-id="0468d-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-261">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-262">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="0468d-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-263">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-264">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-265">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-266">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-267">Nieprawidłowe</span><span class="sxs-lookup"><span data-stu-id="0468d-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-268">Naruszenie reguły nr 2</span><span class="sxs-lookup"><span data-stu-id="0468d-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="0468d-269">C1 obejmuje czas, materiały, wydatki i opłaty dla podzbioru zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="0468d-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0468d-270">CL2 obejmuje czas, materiały, wydatki i opłaty za cały projekt P1 i dlatego pokrywa się z tym, co jest zawarte w C1.</span><span class="sxs-lookup"><span data-stu-id="0468d-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-271">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-272">CL2</span><span class="sxs-lookup"><span data-stu-id="0468d-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-273">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-274">Pusty</span><span class="sxs-lookup"><span data-stu-id="0468d-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-275">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-276">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-277">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-278">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-279">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-280">CL1</span><span class="sxs-lookup"><span data-stu-id="0468d-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-281">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-282">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="0468d-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-283">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-284">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-285">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-286">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-287">Prawidłowy</span><span class="sxs-lookup"><span data-stu-id="0468d-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0468d-288">Na regułę #3</span><span class="sxs-lookup"><span data-stu-id="0468d-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="0468d-289">C1 obejmuje czas, wydatki, materiały i opłaty dla podzbioru zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="0468d-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0468d-290">CL2 obejmuje czas, wydatki, materiały i opłaty dla podzbioru zadań w projekcie P1.</span><span class="sxs-lookup"><span data-stu-id="0468d-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0468d-291">Jedyna dodatkowa weryfikacja dotyczy podzbioru zadań w CL1 różni się od podzbioru zadań w CL2, aby upewnić się, że nie ma tam nakładania się.</span><span class="sxs-lookup"><span data-stu-id="0468d-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="0468d-292">Jest to wykonywane przez system podczas kojarzenia zadań.</span><span class="sxs-lookup"><span data-stu-id="0468d-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0468d-293">C1</span><span class="sxs-lookup"><span data-stu-id="0468d-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0468d-294">CL2</span><span class="sxs-lookup"><span data-stu-id="0468d-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-295">O1</span><span class="sxs-lookup"><span data-stu-id="0468d-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0468d-296">Tylko wybrane zadania</span><span class="sxs-lookup"><span data-stu-id="0468d-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-297">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0468d-298">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-299">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0468d-300">Tak</span><span class="sxs-lookup"><span data-stu-id="0468d-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
