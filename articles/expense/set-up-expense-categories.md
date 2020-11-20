---
title: Konfiguracja kategorii wydatków
description: Ten temat zawiera informacje na temat konfigurowania kategorii wydatków i udostępnionych kategorii raportów z wydatków.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123796"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="eed10-103">Konfiguracja kategorii wydatków</span><span class="sxs-lookup"><span data-stu-id="eed10-103">Set up expense categories</span></span>

<span data-ttu-id="eed10-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="eed10-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eed10-105">Kiedy pracownicy tworzą raporty o wydatkach, każdy z tych rekordów musi być skojarzony z kategorią wydatku.</span><span class="sxs-lookup"><span data-stu-id="eed10-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="eed10-106">Kategorie wydatków są pobierane z kategorii udostępnionych, które mogą być współużytkowane przez osoby prawne należące do organizacji.</span><span class="sxs-lookup"><span data-stu-id="eed10-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="eed10-107">W zależności od sposobu definiowania organizacji te kategorie kosztów mogą być również udostępniane w innych obszarach.</span><span class="sxs-lookup"><span data-stu-id="eed10-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="eed10-108">W zależności od definicji organizacji i wskazówek dotyczących zespołu implementacji należy określić, czy kategorie używane w zarządzaniu wydatkami będą używane tylko w zarządzaniu wydatkami, czy powinny być wspólne dla innych obszarów.</span><span class="sxs-lookup"><span data-stu-id="eed10-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="eed10-109">Kategorie te mogą być współużytkowane przez zarządzanie projektami oraz zarządzanie wydatkami i kosztami, a także między zarządzaniem projektami oraz ich księgowaniem i produkcją.</span><span class="sxs-lookup"><span data-stu-id="eed10-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="eed10-110">Nie można ich jednak udostępniać pomiędzy zarządzaniem wydatkami i produkcją.</span><span class="sxs-lookup"><span data-stu-id="eed10-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="eed10-111">Przed rozpoczęciem procesu instalacji należy wykonać następujące decyzje dotyczące każdej kategorii wydatków:</span><span class="sxs-lookup"><span data-stu-id="eed10-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="eed10-112">Jaka jest kategoria wydatków?</span><span class="sxs-lookup"><span data-stu-id="eed10-112">What is the expense category?</span></span> <span data-ttu-id="eed10-113">Mogą to być np. kategorie dla lotów, hotelu lub trasy.</span><span class="sxs-lookup"><span data-stu-id="eed10-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="eed10-114">Czy kategoria wydatków może być używana także w zarządzaniu projektami i księgowaniu?</span><span class="sxs-lookup"><span data-stu-id="eed10-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="eed10-115">Jeśli tak, to należy także podjąć następujące decyzje:</span><span class="sxs-lookup"><span data-stu-id="eed10-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="eed10-116">Które konta kosztów będą używane w następujących wydatkach?</span><span class="sxs-lookup"><span data-stu-id="eed10-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="eed10-117">Koszt</span><span class="sxs-lookup"><span data-stu-id="eed10-117">Cost</span></span>
        - <span data-ttu-id="eed10-118">Alokacja płac</span><span class="sxs-lookup"><span data-stu-id="eed10-118">Payroll allocation</span></span>
        - <span data-ttu-id="eed10-119">PWT-koszt wartość</span><span class="sxs-lookup"><span data-stu-id="eed10-119">WIP-cost value</span></span>
        - <span data-ttu-id="eed10-120">Koszt przedmiotu</span><span class="sxs-lookup"><span data-stu-id="eed10-120">Cost-item</span></span>
        - <span data-ttu-id="eed10-121">PWT-koszt wartość-przedmiotu</span><span class="sxs-lookup"><span data-stu-id="eed10-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="eed10-122">Naliczona strata</span><span class="sxs-lookup"><span data-stu-id="eed10-122">Accrued loss</span></span>
        - <span data-ttu-id="eed10-123">PWT-naliczona strata</span><span class="sxs-lookup"><span data-stu-id="eed10-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="eed10-124">Które konta przychodu będą używane dla następujących źródeł przychodów?</span><span class="sxs-lookup"><span data-stu-id="eed10-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="eed10-125">Zafakturowany przychód</span><span class="sxs-lookup"><span data-stu-id="eed10-125">Invoiced revenue</span></span>
        - <span data-ttu-id="eed10-126">Naliczony przychód — wartość sprzedaży</span><span class="sxs-lookup"><span data-stu-id="eed10-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="eed10-127">PWT — wartość sprzedaży</span><span class="sxs-lookup"><span data-stu-id="eed10-127">WIP-sales value</span></span>
        - <span data-ttu-id="eed10-128">Naliczony przychód — produkcja</span><span class="sxs-lookup"><span data-stu-id="eed10-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="eed10-129">PWT-produkcja</span><span class="sxs-lookup"><span data-stu-id="eed10-129">WIP-production</span></span>
        - <span data-ttu-id="eed10-130">Naliczony przychód — zysk</span><span class="sxs-lookup"><span data-stu-id="eed10-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="eed10-131">PWT-zysk</span><span class="sxs-lookup"><span data-stu-id="eed10-131">WIP-profit</span></span>
        - <span data-ttu-id="eed10-132">Naliczony przychód — subskrypcja</span><span class="sxs-lookup"><span data-stu-id="eed10-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="eed10-133">PWT-subskrypcja</span><span class="sxs-lookup"><span data-stu-id="eed10-133">WIP-subscription</span></span>

- <span data-ttu-id="eed10-134">Jaki jest typ wydatków?</span><span class="sxs-lookup"><span data-stu-id="eed10-134">What is the expense type?</span></span>
- <span data-ttu-id="eed10-135">Jaka jest domyślna metoda płatności dla tej kategorii wydatków?</span><span class="sxs-lookup"><span data-stu-id="eed10-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="eed10-136">Czy wydatki w tej kategorii muszą zostać wyszczególnione?</span><span class="sxs-lookup"><span data-stu-id="eed10-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="eed10-137">Jaka jest główne domyślne konto dla tej kategorii wydatków?</span><span class="sxs-lookup"><span data-stu-id="eed10-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="eed10-138">Jaka jest domyślna grupa podatków od sprzedaży w danej kategorii wydatku?</span><span class="sxs-lookup"><span data-stu-id="eed10-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="eed10-139">Czy dla kategorii wydatków są dozwolone dodatkowe formy płatności?</span><span class="sxs-lookup"><span data-stu-id="eed10-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="eed10-140">Jeśli tak, to jakie?</span><span class="sxs-lookup"><span data-stu-id="eed10-140">If so, what are they?</span></span>
- <span data-ttu-id="eed10-141">Czy w tej kategorii wydatków znajdują się podkategorie?</span><span class="sxs-lookup"><span data-stu-id="eed10-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="eed10-142">Jeśli tak, to należy także podjąć następujące decyzje:</span><span class="sxs-lookup"><span data-stu-id="eed10-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="eed10-143">Czy któraś z podkategorii jest wykluczona ze zwrotu podatku?</span><span class="sxs-lookup"><span data-stu-id="eed10-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="eed10-144">Jaka jest grupa podatku od sprzedaży w tych podkategoriach?</span><span class="sxs-lookup"><span data-stu-id="eed10-144">What is the item sales tax group of the subcategories?</span></span>
