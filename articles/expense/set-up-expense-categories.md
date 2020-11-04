---
title: Konfiguracja kategorii wydatków
description: Ten temat zawiera informacje na temat konfigurowania kategorii wydatków i udostępnionych kategorii raportów z wydatków.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081902"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="6f760-103">Konfiguracja kategorii wydatków</span><span class="sxs-lookup"><span data-stu-id="6f760-103">Set up expense categories</span></span>

<span data-ttu-id="6f760-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="6f760-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6f760-105">Kiedy pracownicy tworzą raporty o wydatkach, każdy z tych rekordów musi być skojarzony z kategorią wydatku.</span><span class="sxs-lookup"><span data-stu-id="6f760-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="6f760-106">Kategorie wydatków są pobierane z kategorii udostępnionych, które mogą być współużytkowane przez osoby prawne należące do organizacji.</span><span class="sxs-lookup"><span data-stu-id="6f760-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="6f760-107">W zależności od sposobu definiowania organizacji te kategorie kosztów mogą być również udostępniane w innych obszarach.</span><span class="sxs-lookup"><span data-stu-id="6f760-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="6f760-108">W zależności od definicji organizacji i wskazówek dotyczących zespołu implementacji należy określić, czy kategorie używane w zarządzaniu wydatkami będą używane tylko w zarządzaniu wydatkami, czy powinny być wspólne dla innych obszarów.</span><span class="sxs-lookup"><span data-stu-id="6f760-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="6f760-109">Kategorie te mogą być współużytkowane przez zarządzanie projektami oraz zarządzanie wydatkami i kosztami, a także między zarządzaniem projektami oraz ich księgowaniem i produkcją.</span><span class="sxs-lookup"><span data-stu-id="6f760-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="6f760-110">Nie można ich jednak udostępniać pomiędzy zarządzaniem wydatkami i produkcją.</span><span class="sxs-lookup"><span data-stu-id="6f760-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="6f760-111">Przed rozpoczęciem procesu instalacji należy wykonać następujące decyzje dotyczące każdej kategorii wydatków:</span><span class="sxs-lookup"><span data-stu-id="6f760-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="6f760-112">Jaka jest kategoria wydatków?</span><span class="sxs-lookup"><span data-stu-id="6f760-112">What is the expense category?</span></span> <span data-ttu-id="6f760-113">Mogą to być np. kategorie dla lotów, hotelu lub trasy.</span><span class="sxs-lookup"><span data-stu-id="6f760-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="6f760-114">Czy kategoria wydatków może być używana także w zarządzaniu projektami i księgowaniu?</span><span class="sxs-lookup"><span data-stu-id="6f760-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="6f760-115">Jeśli tak, to należy także podjąć następujące decyzje:</span><span class="sxs-lookup"><span data-stu-id="6f760-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6f760-116">Które konta kosztów będą używane w następujących wydatkach?</span><span class="sxs-lookup"><span data-stu-id="6f760-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="6f760-117">Koszt</span><span class="sxs-lookup"><span data-stu-id="6f760-117">Cost</span></span>
        - <span data-ttu-id="6f760-118">Alokacja płac</span><span class="sxs-lookup"><span data-stu-id="6f760-118">Payroll allocation</span></span>
        - <span data-ttu-id="6f760-119">PWT-koszt wartość</span><span class="sxs-lookup"><span data-stu-id="6f760-119">WIP-cost value</span></span>
        - <span data-ttu-id="6f760-120">Koszt przedmiotu</span><span class="sxs-lookup"><span data-stu-id="6f760-120">Cost-item</span></span>
        - <span data-ttu-id="6f760-121">PWT-koszt wartość-przedmiotu</span><span class="sxs-lookup"><span data-stu-id="6f760-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="6f760-122">Naliczona strata</span><span class="sxs-lookup"><span data-stu-id="6f760-122">Accrued loss</span></span>
        - <span data-ttu-id="6f760-123">PWT-naliczona strata</span><span class="sxs-lookup"><span data-stu-id="6f760-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="6f760-124">Które konta przychodu będą używane dla następujących źródeł przychodów?</span><span class="sxs-lookup"><span data-stu-id="6f760-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="6f760-125">Zafakturowany przychód</span><span class="sxs-lookup"><span data-stu-id="6f760-125">Invoiced revenue</span></span>
        - <span data-ttu-id="6f760-126">Naliczony przychód — wartość sprzedaży</span><span class="sxs-lookup"><span data-stu-id="6f760-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="6f760-127">PWT — wartość sprzedaży</span><span class="sxs-lookup"><span data-stu-id="6f760-127">WIP-sales value</span></span>
        - <span data-ttu-id="6f760-128">Naliczony przychód — produkcja</span><span class="sxs-lookup"><span data-stu-id="6f760-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="6f760-129">PWT-produkcja</span><span class="sxs-lookup"><span data-stu-id="6f760-129">WIP-production</span></span>
        - <span data-ttu-id="6f760-130">Naliczony przychód — zysk</span><span class="sxs-lookup"><span data-stu-id="6f760-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="6f760-131">PWT-zysk</span><span class="sxs-lookup"><span data-stu-id="6f760-131">WIP-profit</span></span>
        - <span data-ttu-id="6f760-132">Naliczony przychód — subskrypcja</span><span class="sxs-lookup"><span data-stu-id="6f760-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="6f760-133">PWT-subskrypcja</span><span class="sxs-lookup"><span data-stu-id="6f760-133">WIP-subscription</span></span>

- <span data-ttu-id="6f760-134">Jaki jest typ wydatków?</span><span class="sxs-lookup"><span data-stu-id="6f760-134">What is the expense type?</span></span>
- <span data-ttu-id="6f760-135">Jaka jest domyślna metoda płatności dla tej kategorii wydatków?</span><span class="sxs-lookup"><span data-stu-id="6f760-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="6f760-136">Czy wydatki w tej kategorii muszą zostać wyszczególnione?</span><span class="sxs-lookup"><span data-stu-id="6f760-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="6f760-137">Jaka jest główne domyślne konto dla tej kategorii wydatków?</span><span class="sxs-lookup"><span data-stu-id="6f760-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="6f760-138">Jaka jest domyślna grupa podatków od sprzedaży w danej kategorii wydatku?</span><span class="sxs-lookup"><span data-stu-id="6f760-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="6f760-139">Czy dla kategorii wydatków są dozwolone dodatkowe formy płatności?</span><span class="sxs-lookup"><span data-stu-id="6f760-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="6f760-140">Jeśli tak, to jakie?</span><span class="sxs-lookup"><span data-stu-id="6f760-140">If so, what are they?</span></span>
- <span data-ttu-id="6f760-141">Czy w tej kategorii wydatków znajdują się podkategorie?</span><span class="sxs-lookup"><span data-stu-id="6f760-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="6f760-142">Jeśli tak, to należy także podjąć następujące decyzje:</span><span class="sxs-lookup"><span data-stu-id="6f760-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6f760-143">Czy któraś z podkategorii jest wykluczona ze zwrotu podatku?</span><span class="sxs-lookup"><span data-stu-id="6f760-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="6f760-144">Jaka jest grupa podatku od sprzedaży w tych podkategoriach?</span><span class="sxs-lookup"><span data-stu-id="6f760-144">What is the item sales tax group of the subcategories?</span></span>
