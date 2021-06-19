---
title: Konfigurowanie kosztów standardowych na robociznę i koszty
description: W tym temat opisano sposób konfigurowania kosztów standardowych dla robocizny i kosztów projektu.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011024"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="87d1e-103">Konfigurowanie kosztów standardowych na robociznę i koszty</span><span class="sxs-lookup"><span data-stu-id="87d1e-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87d1e-104">W tym temat opisano sposób konfigurowania kosztów standardowych dla robocizny i kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="87d1e-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="87d1e-105">W tym zadaniu jest używany zestaw danych USSI.</span><span class="sxs-lookup"><span data-stu-id="87d1e-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="87d1e-106">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Koszty własne (godziny)**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="87d1e-107">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-107">Select **New**.</span></span>
3. <span data-ttu-id="87d1e-108">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="87d1e-109">W polu **Koszt własny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="87d1e-110">Użytkownik może skonfigurować standardowy koszt własny dla danej kategorii projektu lub zdefiniować koszty własne według numeru pracownika, numeru projektu, kategorii, daty lub dowolnej kombinacji tych elementów.</span><span class="sxs-lookup"><span data-stu-id="87d1e-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="87d1e-111">Koszt własny jest kosztem własnym o najwyższym poziomie szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="87d1e-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="87d1e-112">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-112">Select **Save**.</span></span>
6. <span data-ttu-id="87d1e-113">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Cena sprzedaży (godziny)**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="87d1e-114">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-114">Select **New**.</span></span>
8. <span data-ttu-id="87d1e-115">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="87d1e-116">W polu **Ważne przez** wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="87d1e-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="87d1e-117">W polu **Ceny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="87d1e-118">Użytkownik może skonfigurować standardową cenę sprzedaży dla transakcji godzinowych lub dla kategorii projektu.</span><span class="sxs-lookup"><span data-stu-id="87d1e-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="87d1e-119">Można również skonfigurować ceny sprzedaży według numerów pracowników, numerów projektów, kategorii, dat transakcji lub dowolnej kombinacji tych elementów.</span><span class="sxs-lookup"><span data-stu-id="87d1e-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="87d1e-120">Rzeczywista cena sprzedaży stosowana w momencie, gdy pracownik wprowadza transakcję w arkuszu godzinowym, to cena sprzedaży zawierająca najwyższy poziom szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="87d1e-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="87d1e-121">Jeśli na przykład została ustawiona zarówno cena ogólna, jak i cena sprzedaży określona przez pracownika, jest używana cena sprzedaży właściwa dla danego procesu.</span><span class="sxs-lookup"><span data-stu-id="87d1e-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="87d1e-122">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-122">Select **Save**.</span></span>
12. <span data-ttu-id="87d1e-123">Zamyknij stronę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-123">Close the page.</span></span>
13. <span data-ttu-id="87d1e-124">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Koszty własne (wydatki)**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="87d1e-125">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-125">Select **New**.</span></span>
15. <span data-ttu-id="87d1e-126">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="87d1e-127">W polu **Koszt własny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="87d1e-128">W programie można wypełnić wiele pól, ale jest to minimalny format wymagany do zapisania rekordu.</span><span class="sxs-lookup"><span data-stu-id="87d1e-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="87d1e-129">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-129">Select **Save**.</span></span>
18. <span data-ttu-id="87d1e-130">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Cena sprzedaży (wydatki)**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="87d1e-131">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-131">Select **New**.</span></span>
20. <span data-ttu-id="87d1e-132">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="87d1e-133">W polu **Ważne przez** wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="87d1e-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="87d1e-134">W polu **Ceny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="87d1e-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="87d1e-135">Rzeczywista cena sprzedaży stosowana w momencie, gdy pracownik wprowadza transakcje w arkuszu wydatków, to cena sprzedaży zawierająca najwyższy poziom szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="87d1e-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="87d1e-136">Na przykład, jeśli skonfigurowano zarówno cenę sprzedaży ogólną, jak i cenę sprzedaży dla konkretnego pracownika, używana jest cena sprzedaży dla konkretnego pracownika.</span><span class="sxs-lookup"><span data-stu-id="87d1e-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="87d1e-137">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="87d1e-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]