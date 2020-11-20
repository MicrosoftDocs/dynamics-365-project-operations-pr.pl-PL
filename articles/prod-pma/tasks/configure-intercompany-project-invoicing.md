---
title: Konfigurowanie międzyfirmowego fakturowania projektu
description: W tym temat pokazano, jak skonfigurować sposób fakturowania projektów między dwiema firmami w organizacji.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082071"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="f19b4-103">Konfigurowanie międzyfirmowego fakturowania projektu</span><span class="sxs-lookup"><span data-stu-id="f19b4-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f19b4-104">W tym temat pokazano, jak skonfigurować sposób fakturowania projektów między dwiema firmami w organizacji.</span><span class="sxs-lookup"><span data-stu-id="f19b4-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="f19b4-105">W tym zadaniu jest używany zestaw danych USSI.</span><span class="sxs-lookup"><span data-stu-id="f19b4-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f19b4-106">W okienku nawigacji wybierz kolejno pozycje **Moduły > Rozrachunki z dostawcami > Sprzedawcy > Wszyscy sprzedawcy**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="f19b4-107">Na liście **Wszyscy sprzedawcy** znajdź i wybierz żądany rekord.</span><span class="sxs-lookup"><span data-stu-id="f19b4-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="f19b4-108">W okienku akcji wybierz pozycję **Ogólne**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="f19b4-109">Wybierz opcję **Międzyfirmowe**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="f19b4-110">Ustaw wartość **Aktywne** na **Tak** , aby włączyć handel międzyfirmowy.</span><span class="sxs-lookup"><span data-stu-id="f19b4-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="f19b4-111">W polu **Firma klienta** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="f19b4-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="f19b4-112">W polu **Moje konto** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="f19b4-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="f19b4-113">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-113">Select **Save**.</span></span>
9. <span data-ttu-id="f19b4-114">Zamknij strony, aby powrócić do strony głównej.</span><span class="sxs-lookup"><span data-stu-id="f19b4-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="f19b4-115">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Parametry Zarządzanie projektami i księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="f19b4-116">Wybierz kartę **Międzyfirmowe**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="f19b4-117">Przesuń suwak na **Tak** , aby włączyć Międzyfirmowe planowanie zasobów i grafiki.</span><span class="sxs-lookup"><span data-stu-id="f19b4-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="f19b4-118">Zaznacz wybrany wiersz na liście.</span><span class="sxs-lookup"><span data-stu-id="f19b4-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f19b4-119">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-119">Select **New**.</span></span>
15. <span data-ttu-id="f19b4-120">W polu **Firma pozyczająca** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="f19b4-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="f19b4-121">Zaznacz pole wyboru **Naliczony przychód**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="f19b4-122">W polu **Domyślna kategoria grafiku** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="f19b4-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="f19b4-123">W polu **Domyślna kategoria wydatku** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="f19b4-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="f19b4-124">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-124">Select **Save**.</span></span>
20. <span data-ttu-id="f19b4-125">Zamyknij stronę.</span><span class="sxs-lookup"><span data-stu-id="f19b4-125">Close the page.</span></span>
21. <span data-ttu-id="f19b4-126">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Księgowanie > Konfiguracja księgowania w rejestrze**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="f19b4-127">W polu **Typy kont księgowych** wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="f19b4-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="f19b4-128">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-128">Select **New**.</span></span>
24. <span data-ttu-id="f19b4-129">W polu **Konto główne** nowego wiersza określ wymagane wartości.</span><span class="sxs-lookup"><span data-stu-id="f19b4-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="f19b4-130">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-130">Select **Save**.</span></span>
26. <span data-ttu-id="f19b4-131">Zamyknij stronę.</span><span class="sxs-lookup"><span data-stu-id="f19b4-131">Close the page.</span></span>
27. <span data-ttu-id="f19b4-132">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Cena przelewu**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="f19b4-133">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-133">Select **New**.</span></span>
29. <span data-ttu-id="f19b4-134">W polu **Data wejścia w życie** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="f19b4-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="f19b4-135">W polu **Firma pozyczająca** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="f19b4-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="f19b4-136">W polu **Model ceny przeniesienia** wybierz jedną z opcji.</span><span class="sxs-lookup"><span data-stu-id="f19b4-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="f19b4-137">W polu **Ceny** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="f19b4-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="f19b4-138">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="f19b4-138">Select **Save**.</span></span>
