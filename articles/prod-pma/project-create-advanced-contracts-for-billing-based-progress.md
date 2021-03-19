---
title: Tworzenie zaawansowanych kontraktów dotyczących rozliczeń na podstawie postępu
description: W tym temacie wyjaśniono, jak tworzyć kontrakty projektów, tak aby można było generować faktury dla klientów na podstawie procentu wykonanej pracy.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289517"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="975dc-103">Tworzenie zaawansowanych kontraktów dotyczących rozliczeń na podstawie postępu</span><span class="sxs-lookup"><span data-stu-id="975dc-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="975dc-104">W tym temacie wyjaśniono, jak tworzyć kontrakty projektów, tak aby można było tworzyć faktury dla klientów na podstawie procentu wykonanej pracy.</span><span class="sxs-lookup"><span data-stu-id="975dc-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="975dc-105">Kwoty na fakturze są obliczane automatycznie w odniesieniu do kategorii budżetu pracy skonfigurowanej dla projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="975dc-106">Harmonogram faktury jest ustawiany podczas negocjowania kontraktu dotyczącego projektu z klientem.</span><span class="sxs-lookup"><span data-stu-id="975dc-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="975dc-107">Procedury opisane w tym temacie służą do konfigurowania kontraktu, skojarzonego projektu oraz reguł fakturowania, które obliczają kwoty faktur dla kategorii budżetów pracy skonfigurowanych dla danego projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="975dc-108">Po utworzeniu kontraktu i projektu można skonfigurować szczegółowe informacje o projekcie.</span><span class="sxs-lookup"><span data-stu-id="975dc-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="975dc-109">Na przykład można zdefiniować działania i przypisać pracowników do projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="975dc-110">Przykład</span><span class="sxs-lookup"><span data-stu-id="975dc-110">Example</span></span>

<span data-ttu-id="975dc-111">Twoja organizacja jest przedsiębiorstwem rozwijającym oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="975dc-111">Your organization is a software development firm.</span></span> <span data-ttu-id="975dc-112">Wyrażasz zgodę na opracowywanie pakietu obsługi kont płacy dla klienta z łączną opłatą na kwotę 20 000 USD.</span><span class="sxs-lookup"><span data-stu-id="975dc-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="975dc-113">Twoja organizacja wyraża zgodę na fakturowanie klienta w miarę wykonywania określonych wartości procentowych projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="975dc-114">Konfigurowanie poniższych kategorii projektu dla pracy jest możliwe w taki sposób, że można z nich korzystać w procesie fakturowania:</span><span class="sxs-lookup"><span data-stu-id="975dc-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="975dc-115">Doradztwo</span><span class="sxs-lookup"><span data-stu-id="975dc-115">Consulting</span></span>
- <span data-ttu-id="975dc-116">Zaprojektuj</span><span class="sxs-lookup"><span data-stu-id="975dc-116">Design</span></span>
- <span data-ttu-id="975dc-117">Instalacja</span><span class="sxs-lookup"><span data-stu-id="975dc-117">Installation</span></span>

<span data-ttu-id="975dc-118">Skonfigurujesz także reguły rozliczeniowe, które automatycznie obliczają kwoty faktur dla procentu pracy projektowej wykonanej dla każdej kategorii.</span><span class="sxs-lookup"><span data-stu-id="975dc-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="975dc-119">Menedżer budżetu tworzy budżet dla kategorii projektów.</span><span class="sxs-lookup"><span data-stu-id="975dc-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="975dc-120">Ilość pracy wykonanej jest automatycznie obliczana jako wartość procentowa pracy rzeczywistej w porównaniu z wartościami zabudżetowanymi.</span><span class="sxs-lookup"><span data-stu-id="975dc-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="975dc-121">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="975dc-121">Prerequisites</span></span>

<span data-ttu-id="975dc-122">Przed utworzeniem projektu, który korzysta z reguł fakturowania, należy skonfigurować sekwencje numerów dla reguł fakturowania i arkusz opłat używany do księgowania postępu fakturowania.</span><span class="sxs-lookup"><span data-stu-id="975dc-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="975dc-123">Przejdź do **Zarządzanie projektami i księgowanie** \> **Ustawienia** \> **Parametry zarządzania projektami i księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="975dc-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="975dc-124">Na stronie **Zarządzanie projektami i parametry księgowania**, na karcie **Sekwencje numerów** skonfiguruj sekwencję numerów, która ma być używana podczas tworzenia reguł fakturowania.</span><span class="sxs-lookup"><span data-stu-id="975dc-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="975dc-125">Wybierz kolejno pozycje **Zarządzanie projektami i księgowanie** \> **Arkusze** \> **Opłaty**.</span><span class="sxs-lookup"><span data-stu-id="975dc-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="975dc-126">Na stronie **Arkusz opłat** wybierz opcję **Nowy** i wprowadź nazwę arkusza.</span><span class="sxs-lookup"><span data-stu-id="975dc-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="975dc-127">Tworzenie kontraktu dotyczącego fakturowania postępu</span><span class="sxs-lookup"><span data-stu-id="975dc-127">Create a contract for progress billings</span></span>

<span data-ttu-id="975dc-128">Ta procedura służy do tworzenia kontraktu projektu dotyczącego projektów o stałej cenie.</span><span class="sxs-lookup"><span data-stu-id="975dc-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="975dc-129">Faktura jest tworzona w momencie, gdy praca wykonana w projekcie osiągnie określoną wartość procentową.</span><span class="sxs-lookup"><span data-stu-id="975dc-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="975dc-130">Przejdź do **Zarządzanie projektami i księgowanie** \> **Wszystkie projekty** \> **Kontrakty projektu**.</span><span class="sxs-lookup"><span data-stu-id="975dc-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="975dc-131">Na stronie szczegółów **Kontraktu projektu** wybierz opcję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="975dc-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="975dc-132">W oknie dialogowym **Nowy kontrakt dotyczący projektu** ustaw następujące pola:</span><span class="sxs-lookup"><span data-stu-id="975dc-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="975dc-133">**Nazwa/nazwisko**</span><span class="sxs-lookup"><span data-stu-id="975dc-133">**Name**</span></span>
    - <span data-ttu-id="975dc-134">**Typ finansowania**</span><span class="sxs-lookup"><span data-stu-id="975dc-134">**Funding type**</span></span>
    - <span data-ttu-id="975dc-135">**Źródło finansowania**</span><span class="sxs-lookup"><span data-stu-id="975dc-135">**Funding source**</span></span>
    - <span data-ttu-id="975dc-136">**Waluta sprzedaży** — Domyślnie ta waluta jest używana na fakturach klienta skojarzonych z kontraktem dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="975dc-137">Można jednak zmienić walutę sprzedaży na określonej fakturze dla danego klienta.</span><span class="sxs-lookup"><span data-stu-id="975dc-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="975dc-138">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="975dc-138">Select **OK**.</span></span> <span data-ttu-id="975dc-139">Informacje zostaną skopiowane do nagłówka strony **Kontrakty projektów**.</span><span class="sxs-lookup"><span data-stu-id="975dc-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="975dc-140">Na stronie **Kontrakty projektu** wypełnij pozostałe informacje wymagane do projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="975dc-141">Tworzenie projektu dotyczącego fakturowania postępu</span><span class="sxs-lookup"><span data-stu-id="975dc-141">Create a project for progress billings</span></span>

<span data-ttu-id="975dc-142">Wykonaj te kroki, aby utworzyć projekt i wszystkie podprojekty skojarzone z kontraktem dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="975dc-143">Przejdź do **Zarządzanie projektami i księgowanie** \> **Projekty** \> **Wszystkie projekty**.</span><span class="sxs-lookup"><span data-stu-id="975dc-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="975dc-144">Na stronie **Wszystkie projekty** wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="975dc-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="975dc-145">W oknie dialogowym **Nowy projekt**, w polu **Typ projektu** wybierz opcję **Czas i materiały**.</span><span class="sxs-lookup"><span data-stu-id="975dc-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="975dc-146">Wybierz grupę projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-146">Select a project group.</span></span> <span data-ttu-id="975dc-147">Grupa projektu definiuje informacje dotyczące księgowania dla projektów przypisanych do grupy.</span><span class="sxs-lookup"><span data-stu-id="975dc-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="975dc-148">Wybierz pozycję **Utwórz projekt**.</span><span class="sxs-lookup"><span data-stu-id="975dc-148">Select **Create project**.</span></span>
6. <span data-ttu-id="975dc-149">Po utworzeniu projektu ustaw etap projektu na **W toku**.</span><span class="sxs-lookup"><span data-stu-id="975dc-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="975dc-150">Utwórz budżet dla projektu</span><span class="sxs-lookup"><span data-stu-id="975dc-150">Create a budget for a project</span></span>

<span data-ttu-id="975dc-151">kategorie budżetowe automatycznie obliczają kwoty faktur dla procentu pracy wykonanej dla każdej kategorii.</span><span class="sxs-lookup"><span data-stu-id="975dc-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="975dc-152">Wykonaj te kroki, aby utworzyć kategorie budżetu dla kosztów szacunkowych.</span><span class="sxs-lookup"><span data-stu-id="975dc-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="975dc-153">Przejdź do **Zarządzanie projektami i księgowanie** \> **Projekty** \> **Wszystkie projekty**.</span><span class="sxs-lookup"><span data-stu-id="975dc-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="975dc-154">Na stronie **Wszystkie projekty** wybierz odpowiedni projekt i otwórz go.</span><span class="sxs-lookup"><span data-stu-id="975dc-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="975dc-155">Na stronie **Projekty** w okienku akcji na karcie **Plan**, w grupie **Budżet** wybierz pozycję **Budżet projektu**.</span><span class="sxs-lookup"><span data-stu-id="975dc-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="975dc-156">Na stronie **Budżet projektu** wprowadź szacowany koszt dla każdej kategorii w projekcie.</span><span class="sxs-lookup"><span data-stu-id="975dc-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="975dc-157">Tworzenie reguł fakturowania dla fakturowania postępu</span><span class="sxs-lookup"><span data-stu-id="975dc-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="975dc-158">Przejdź do **Zarządzanie projektami i księgowanie** \> **Wszystkie projekty** \> **Kontrakty projektu**.</span><span class="sxs-lookup"><span data-stu-id="975dc-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="975dc-159">Na stronie listy **Kontrakty projektów** wybierz i otwórz kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="975dc-160">Na stronie kontrakt projektu na skróconej karcie **Reguły fakturowania** wybierz pozycję **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="975dc-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="975dc-161">Na stronie **Reguła fakturowania** w polu **Typ wiersza** wybierz pozycję **Postęp**.</span><span class="sxs-lookup"><span data-stu-id="975dc-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="975dc-162">Na skróconej karcie **Szczegóły wiersza reguły fakturowania**, w polu **Wartość kontraktu** wprowadź łączną wartość kontraktu.</span><span class="sxs-lookup"><span data-stu-id="975dc-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="975dc-163">W polu **Kategoria** wybierz kategorię, w której ma zostać zaksięgowana transakcja opłat.</span><span class="sxs-lookup"><span data-stu-id="975dc-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="975dc-164">W polu **Projekt** wybierz projekt korzystający z reguły fakturowania.</span><span class="sxs-lookup"><span data-stu-id="975dc-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="975dc-165">Opcjonalnie: Przypisz regułę fakturowania do dodatkowych projektów.</span><span class="sxs-lookup"><span data-stu-id="975dc-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="975dc-166">Na skróconej karcie **Projekt**, w sekcji **Dostępne projekty** wybierz projekt, a następnie wybierz przycisk strzałki w prawo, aby dodać projekt do sekcji **Wybrane projekty**.</span><span class="sxs-lookup"><span data-stu-id="975dc-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="975dc-167">Opcjonalnie: należy obliczyć kwotę procentową zatrzymania przez klienta na fakturze.</span><span class="sxs-lookup"><span data-stu-id="975dc-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="975dc-168">Na skróconej karcie **Warunki zatrzymania płatności** wybierz źródło finansowania, a następnie w polu **Procent zatrzymania** wprowadź wartość procentową zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="975dc-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="975dc-169">Powtórz te kroki, aby utworzyć dodatkowe reguły fakturowania dla kontraktu dotyczącego projektu.</span><span class="sxs-lookup"><span data-stu-id="975dc-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]