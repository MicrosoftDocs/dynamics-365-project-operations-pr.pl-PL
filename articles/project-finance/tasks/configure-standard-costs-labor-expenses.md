---
title: Konfigurowanie kosztów standardowych na robociznę i koszty
description: W tym temat opisano sposób konfigurowania kosztów standardowych dla robocizny i kosztów projektu.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754417"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="1eb35-103">Konfigurowanie kosztów standardowych na robociznę i koszty</span><span class="sxs-lookup"><span data-stu-id="1eb35-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1eb35-104">W tym temat opisano sposób konfigurowania kosztów standardowych dla robocizny i kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="1eb35-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="1eb35-105">W tym zadaniu jest używany zestaw danych USSI.</span><span class="sxs-lookup"><span data-stu-id="1eb35-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1eb35-106">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Koszty własne (godziny)**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="1eb35-107">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-107">Select **New**.</span></span>
3. <span data-ttu-id="1eb35-108">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="1eb35-109">W polu **Koszt własny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="1eb35-110">Użytkownik może skonfigurować standardowy koszt własny dla danej kategorii projektu lub zdefiniować koszty własne według numeru pracownika, numeru projektu, kategorii, daty lub dowolnej kombinacji tych elementów.</span><span class="sxs-lookup"><span data-stu-id="1eb35-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="1eb35-111">Koszt własny jest kosztem własnym o najwyższym poziomie szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="1eb35-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="1eb35-112">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-112">Select **Save**.</span></span>
6. <span data-ttu-id="1eb35-113">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Cena sprzedaży (godziny)**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="1eb35-114">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-114">Select **New**.</span></span>
8. <span data-ttu-id="1eb35-115">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="1eb35-116">W polu **Ważne przez** wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="1eb35-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="1eb35-117">W polu **Ceny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="1eb35-118">Użytkownik może skonfigurować standardową cenę sprzedaży dla transakcji godzinowych lub dla kategorii projektu.</span><span class="sxs-lookup"><span data-stu-id="1eb35-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="1eb35-119">Można również skonfigurować ceny sprzedaży według numerów pracowników, numerów projektów, kategorii, dat transakcji lub dowolnej kombinacji tych elementów.</span><span class="sxs-lookup"><span data-stu-id="1eb35-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="1eb35-120">Rzeczywista cena sprzedaży stosowana w momencie, gdy pracownik wprowadza transakcję w arkuszu godzinowym, to cena sprzedaży zawierająca najwyższy poziom szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="1eb35-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="1eb35-121">Jeśli na przykład została ustawiona zarówno cena ogólna, jak i cena sprzedaży określona przez pracownika, jest używana cena sprzedaży właściwa dla danego procesu.</span><span class="sxs-lookup"><span data-stu-id="1eb35-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="1eb35-122">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-122">Select **Save**.</span></span>
12. <span data-ttu-id="1eb35-123">Zamyknij stronę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-123">Close the page.</span></span>
13. <span data-ttu-id="1eb35-124">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Koszty własne (wydatki)**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="1eb35-125">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-125">Select **New**.</span></span>
15. <span data-ttu-id="1eb35-126">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="1eb35-127">W polu **Koszt własny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="1eb35-128">W programie można wypełnić wiele pól, ale jest to minimalny format wymagany do zapisania rekordu.</span><span class="sxs-lookup"><span data-stu-id="1eb35-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="1eb35-129">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-129">Select **Save**.</span></span>
18. <span data-ttu-id="1eb35-130">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Cena sprzedaży (wydatki)**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="1eb35-131">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-131">Select **New**.</span></span>
20. <span data-ttu-id="1eb35-132">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="1eb35-133">W polu **Ważne przez** wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="1eb35-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="1eb35-134">W polu **Ceny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="1eb35-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="1eb35-135">Rzeczywista cena sprzedaży stosowana w momencie, gdy pracownik wprowadza transakcje w arkuszu wydatków, to cena sprzedaży zawierająca najwyższy poziom szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="1eb35-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="1eb35-136">Na przykład, jeśli skonfigurowano zarówno cenę sprzedaży ogólną, jak i cenę sprzedaży dla konkretnego pracownika, używana jest cena sprzedaży dla konkretnego pracownika.</span><span class="sxs-lookup"><span data-stu-id="1eb35-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="1eb35-137">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="1eb35-137">Select **Save**.</span></span>

