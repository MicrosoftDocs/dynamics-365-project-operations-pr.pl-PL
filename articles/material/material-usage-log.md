---
title: Rejestrowanie użycia materiałów w projektach i zadaniach projektów
description: Ten temat zawiera informacje na temat sposobu logowania użycia materiałów do projektów i zadań projektów.
author: rumant
manager: AnnBe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab431ce4c18a4283cd887de9afcba0dd556d2567
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852882"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a><span data-ttu-id="1e4c0-103">Rejestrowanie użycia materiałów w projektach i zadaniach projektów</span><span class="sxs-lookup"><span data-stu-id="1e4c0-103">Record material usage on projects and project tasks</span></span>

<span data-ttu-id="1e4c0-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="1e4c0-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1e4c0-105">Gdy zespół projektowy pracuje nad zadaniami w projekcie, konsumuje lub wykorzystuje materiały.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-105">As a project team works through tasks on a project, they consume or use materials.</span></span> <span data-ttu-id="1e4c0-106">Dziennik zużycia materiałów umożliwia rejestrowanie tego wykorzystania, tak aby mógł zostać zatwierdzony przez kierownika projektu i ostatecznie zafakturowany klientowi.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-106">A material usage log provides a way to record this usage so that it can be approved by the project manager and eventually invoiced to the customer.</span></span> 

<span data-ttu-id="1e4c0-107">Aby zarejestrować użycie katalogu lub materiałów do zapisu i przesłać je do osoby zatwierdzającej, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="1e4c0-107">To record the usage of catalog or write-in materials and submit them to the approver, follow these steps:</span></span> 

1. <span data-ttu-id="1e4c0-108">W okienku nawigacyjnym wybierz opcję **Użycie materiałów**, a następnie wybierz opcję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-108">In the navigation pane, select **Material Usage**, and then select **New**.</span></span>
2. <span data-ttu-id="1e4c0-109">Na stronie **Nowe użycie materiałów** wprowadź wymagane informacje dotyczące użycia materiałów, a następnie wybierz opcję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-109">On the **New Material Usage** page, enter the required material usage information, and then select **Save**.</span></span>

<span data-ttu-id="1e4c0-110">W poniższej tabeli przedstawiono informacje o polach na stronie **Dziennik użycia materiałów**.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-110">The following table provides information about the fields on the **Material Usage Log** page.</span></span> 

| <span data-ttu-id="1e4c0-111">**Pole**</span><span class="sxs-lookup"><span data-stu-id="1e4c0-111">**Field**</span></span> | <span data-ttu-id="1e4c0-112">**Opis**</span><span class="sxs-lookup"><span data-stu-id="1e4c0-112">**Description**</span></span> | <span data-ttu-id="1e4c0-113">**Wpływ zmian w dalszych etapach**</span><span class="sxs-lookup"><span data-stu-id="1e4c0-113">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1e4c0-114">Opis</span><span class="sxs-lookup"><span data-stu-id="1e4c0-114">Description</span></span> | <span data-ttu-id="1e4c0-115">Opis konkretnego zastosowania materiałów.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-115">A description of the specific material usage.</span></span> | <span data-ttu-id="1e4c0-116">W tym polu nie ma wpływu zmian na dalsze etapy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-116">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="1e4c0-117">Data</span><span class="sxs-lookup"><span data-stu-id="1e4c0-117">Date</span></span> | <span data-ttu-id="1e4c0-118">Data, w której materiał ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-118">The date on which the material is expected to be used.</span></span> | <span data-ttu-id="1e4c0-119">W tym polu nie ma wpływu zmian na dalsze etapy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-119">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="1e4c0-120">Project</span><span class="sxs-lookup"><span data-stu-id="1e4c0-120">Project</span></span> | <span data-ttu-id="1e4c0-121">Listy projektów, które są aktywne.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-121">A list projects that are active.</span></span> | <span data-ttu-id="1e4c0-122">Wybranie projektu do dziennika użycia materiałów wpływa na pole **Zadanie**, tak aby wyświetlane było tylko zadania związane z projektem.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-122">Selecting a project for a material usage log impacts the **Task** field to show only those tasks that are on the project.</span></span> |
| <span data-ttu-id="1e4c0-123">Zadanie</span><span class="sxs-lookup"><span data-stu-id="1e4c0-123">Task</span></span> | <span data-ttu-id="1e4c0-124">Lista zadań projektu łącznie z podsumowaniem i zadaniami węzła liścia.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-124">A list of tasks for the project including summary and leaf node tasks.</span></span> | <span data-ttu-id="1e4c0-125">Wybranie zadania do dziennika zużycia materiałów ma wpływ na rzeczywisty koszt materiałów i rzeczywistą sprzedaż materiałów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-125">Selecting a task for a material usage log impacts the actual material cost and actual material sales for a task.</span></span> <span data-ttu-id="1e4c0-126">Jeśli to pole jest puste, odpowiednie koszty zużycia materiałów i sprzedaży są śledzone i podsumowywane tylko na poziomie projektu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-126">If this field is empty, the corresponding material usage cost and sales is tracked and summarized only at the project level.</span></span> |
| <span data-ttu-id="1e4c0-127">Wybierz produkt</span><span class="sxs-lookup"><span data-stu-id="1e4c0-127">Select Product</span></span> | <span data-ttu-id="1e4c0-128">Należy określić, czy to użycie materiałów dotyczy **Istniejącego** produktu (katalogu), czy też **Dopisane** produktu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-128">Specify if this material usage is for an **Existing** (catalog) product or a **Write in** product.</span></span> | <span data-ttu-id="1e4c0-129">To pole określa typ produktu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-129">This field determines the type of product.</span></span> |
| <span data-ttu-id="1e4c0-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="1e4c0-130">Product</span></span> | <span data-ttu-id="1e4c0-131">Identyfikator produktu z katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-131">The ID of the product from product catalog.</span></span> <span data-ttu-id="1e4c0-132">Po wybraniu identyfikatora produktu pole **Wybierz produkt** automatycznie aktualizuje **Istniejący produkt**.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-132">When you select a product ID, the **Select Product** field automatically updates to **Existing product**.</span></span> <span data-ttu-id="1e4c0-133">Identyfikator jest używany do pobierania kosztów i cen sprzedaży z cennika.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-133">The ID is used to retrieve cost and sales prices from the price list.</span></span> | <span data-ttu-id="1e4c0-134">W tym polu nie ma wpływu zmian na dalsze etapy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-134">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="1e4c0-135">Opis produktu dopisanego</span><span class="sxs-lookup"><span data-stu-id="1e4c0-135">WriteIn Product Description</span></span> | <span data-ttu-id="1e4c0-136">Pole tekstowe dopisania nazwy produktu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-136">A text field to write in the name of the product.</span></span> <span data-ttu-id="1e4c0-137">To pole jest dostępne po wybraniu opcji **Dopisanie** w polu **Wybierz produkt**.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-137">This field is available when you select **Write In** product in the **Select product** field.</span></span>| <span data-ttu-id="1e4c0-138">W tym polu nie ma wpływu zmian na dalsze etapy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-138">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="1e4c0-139">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="1e4c0-139">Bookable Resource</span></span>| <span data-ttu-id="1e4c0-140">Zasób, który wykorzystać ten materiał do projektu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-140">Resource that used this material on the project.</span></span> <span data-ttu-id="1e4c0-141">Domyślną wartością tego pola jest zarezerwowany zasób zalogowanego użytkownika, ale można go zmienić na użycie rekordów w imieniu innych członków zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-141">The default for this field is the bookable resource of the logged in user, but can be changed to record usage on behalf of other members on the project team.</span></span> | <span data-ttu-id="1e4c0-142">W tym polu nie ma wpływu zmian na dalsze etapy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-142">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="1e4c0-143">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="1e4c0-143">Unit group</span></span> | <span data-ttu-id="1e4c0-144">Wartość domyślna w tym polu pochodzi z grupy jednostek ustawionej jako domyślna dla produktu katalogu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-144">The default value in this field comes from the unit group that's set up as the default on the catalog product.</span></span> <span data-ttu-id="1e4c0-145">Możesz zaktualizować to pole, aby wybrać inną grupę jednostek.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-145">You can update this field to select another unit group.</span></span> | <span data-ttu-id="1e4c0-146">W tym polu nie ma wpływu zmian na dalsze etapy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-146">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="1e4c0-147">Jednostka</span><span class="sxs-lookup"><span data-stu-id="1e4c0-147">Unit</span></span> | <span data-ttu-id="1e4c0-148">Domyślna wartość w tym polu jest jednostką domyślną wybranego produktu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-148">The default value in this field is the default unit of the selected product.</span></span> <span data-ttu-id="1e4c0-149">Możesz zaktualizować to pole, aby wybrać inną jednostkę.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-149">You can update this field to select another unit.</span></span> | <span data-ttu-id="1e4c0-150">Zmiana jednostki powoduje inną domyślną cenę jednostkową i koszt.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-150">Changing the unit results in a different default unit price and cost.</span></span> |
| <span data-ttu-id="1e4c0-151">Ilość</span><span class="sxs-lookup"><span data-stu-id="1e4c0-151">Quantity</span></span> | <span data-ttu-id="1e4c0-152">Ilość produktu użytego w projekcie lub zadaniu projektu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-152">The quantity of the product that has been used on the project or the project task.</span></span> | <span data-ttu-id="1e4c0-153">W tym polu nie ma wpływu zmian na dalsze etapy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-153">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="1e4c0-154">Koszt jednostkowy</span><span class="sxs-lookup"><span data-stu-id="1e4c0-154">Unit Cost</span></span> | <span data-ttu-id="1e4c0-155">Koszt jednostkowy wybranego produktu i kombinacji jednostek, zgodnie z obowiązującym cennikiem.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-155">The unit cost of the selected product and unit combination as set up in the applicable cost price list.</span></span> | <span data-ttu-id="1e4c0-156">Koszt jednostkowy jest zawsze wyświetlany w walucie kosztu projektu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-156">The unit cost is always shown in the project's cost currency.</span></span> <span data-ttu-id="1e4c0-157">Jeśli w cenniku nie ma kosztu jednostkowego produktu i jednostki, koszt jednostkowy zostanie domyślnie wartości 0,00.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-157">If there's no unit cost for the combination product and unit in the price list, the unit cost will default to 0.00.</span></span> |
| <span data-ttu-id="1e4c0-158">Łączny koszt</span><span class="sxs-lookup"><span data-stu-id="1e4c0-158">Total Cost</span></span> | <span data-ttu-id="1e4c0-159">Kwota kosztu obliczana jako ilość \* koszt jednostkowy.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-159">The cost amount that is calculated as quantity \* unit cost.</span></span>| <span data-ttu-id="1e4c0-160">Kwota kosztu jest zawsze wyświetlana w walucie kosztu projektu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-160">The cost amount is always shown in the project's cost currency.</span></span> |


## <a name="submit-material-usage-for-review-and-approval"></a><span data-ttu-id="1e4c0-161">Przesyłanie materiałów do przeglądu i zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="1e4c0-161">Submit material usage for review and approval</span></span> 
<span data-ttu-id="1e4c0-162">Po przechwytywaniu wszystkich materiałów i przygotowaniu się do zatwierdzenia należy przesłać informacje o użyciu do przeglądu.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-162">After you capture all your material usage, and you're ready to have it approved, you must submit the usage information for review.</span></span>

1. <span data-ttu-id="1e4c0-163">Należy przejść do **Dziennik użycia materiałów** i wybrać jeden lub więcej wpisów.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-163">Go to **Material Usage Log** and select one or more entries.</span></span> <span data-ttu-id="1e4c0-164">Można również zaznaczyć wszystkie rekordy użycia materiałów przy użyciu pola wyboru w nagłówku.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-164">Or, select all the material usage records by using the check box on the header.</span></span>
2. <span data-ttu-id="1e4c0-165">Wybierz **Prześlij**.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-165">Select **Submit**.</span></span> <span data-ttu-id="1e4c0-166">System przetwarza wybrane pozycje, a następnie tworzy żądania zatwierdzenia użycia materiałów.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-166">The system processes the selected entries and then creates material usage approval requests.</span></span>

## <a name="recall-a-material-usage-log"></a><span data-ttu-id="1e4c0-167">Odwołaj dany wpis zużycia materiałów</span><span class="sxs-lookup"><span data-stu-id="1e4c0-167">Recall a material usage log</span></span>

<span data-ttu-id="1e4c0-168">W razie potrzeby można sprawdzić, czy został przekazany materiał.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-168">When necessary, you can recall a submitted material usage.</span></span> <span data-ttu-id="1e4c0-169">Czas potrzebny na wycofanie wpisu dotyczącego wykorzystania materiału zależy od etapu zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-169">The time required to recall a material usage entry depends on the approval stage.</span></span>  <span data-ttu-id="1e4c0-170">Jeśli osoba zatwierdzająca jeszcze nie zatwierdziła wpisu, odwołanie może nastąpić natychmiast.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-170">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="1e4c0-171">Jeśli jednak wpis został już zatwierdzony, należy poprosić osobę zatwierdzającą o zatwierdzenie wycofania i odwrócenie transakcji.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-171">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="1e4c0-172">Wybierz opcję **Użycie materiałów** i z listy dzienników użycia materiałów wybierz użycie materiałów, które chcesz przechować.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-172">Go to **Material Usage**, and in the list of material usage logs, select the material usage to recall.</span></span>
2. <span data-ttu-id="1e4c0-173">Wybierz pozycję **Odwołaj**.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-173">Select **Recall**.</span></span> <span data-ttu-id="1e4c0-174">Jeśli wpis o zużyciu materiału nie został jeszcze zatwierdzony, system natychmiast go wycofuje.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-174">If the material usage entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="1e4c0-175">Jeśli pozycja materiału została już zatwierdzona, tworzone jest żądanie wycofania w celu powiadomienia osoby zatwierdzającej, że chcesz wycofać użycie materiału.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-175">If the material entry has already been approved, a recall request is created to notify the approver that you want to recall the material usage.</span></span> <span data-ttu-id="1e4c0-176">Osoba zatwierdzająca potwierdzi również, że można dokonać odwrócenia, a wpis zostanie cofnięty.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-176">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-material-usage-log"></a><span data-ttu-id="1e4c0-177">Usuń dany wpis zużycia materiałów</span><span class="sxs-lookup"><span data-stu-id="1e4c0-177">Delete a material usage log</span></span>

<span data-ttu-id="1e4c0-178">Nie można usuwać dzienników użycia materiałów, które nie zostały przesłane.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-178">You can delete material usage logs that haven't been submitted.</span></span> <span data-ttu-id="1e4c0-179">Aby usunąć przesłany wcześniej dziennik użycia materiałów, należy najpierw go usunąć.</span><span class="sxs-lookup"><span data-stu-id="1e4c0-179">To delete a material usage log that has already been submitted, you must first recall it.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]