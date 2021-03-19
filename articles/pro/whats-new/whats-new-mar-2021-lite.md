---
title: Co nowego w marcu 2021 r. — uproszczone wdrożenie Project Operations
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w uproszczonym wdrożeniu Project Operations z marca 2021 r.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500028"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="00dc5-103">Co nowego w marcu 2021 r. — uproszczone wdrożenie Project Operations</span><span class="sxs-lookup"><span data-stu-id="00dc5-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="00dc5-104">_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="00dc5-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="00dc5-105">Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="00dc5-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="00dc5-106">Project Operations w środowisku Dataverse w wersji 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="00dc5-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="00dc5-107">Aktualizacje dotyczące jakości</span><span class="sxs-lookup"><span data-stu-id="00dc5-107">Quality updates</span></span>

| <span data-ttu-id="00dc5-108">**Obszar funkcji**</span><span class="sxs-lookup"><span data-stu-id="00dc5-108">**Feature area**</span></span> | <span data-ttu-id="00dc5-109">**Numer referencyjny**</span><span class="sxs-lookup"><span data-stu-id="00dc5-109">**Reference number**</span></span> | <span data-ttu-id="00dc5-110">**Aktualizacja dotycząca jakości**</span><span class="sxs-lookup"><span data-stu-id="00dc5-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="00dc5-111">Rozliczenia i ceny</span><span class="sxs-lookup"><span data-stu-id="00dc5-111">Billing and pricing</span></span> | <span data-ttu-id="00dc5-112">2133873</span><span class="sxs-lookup"><span data-stu-id="00dc5-112">2133873</span></span> | <span data-ttu-id="00dc5-113">Poprawiono wyświetlanie symbolu waluty **Ceny sprzedaży jednostkowej** w siatce **Szacowania wydatków**.</span><span class="sxs-lookup"><span data-stu-id="00dc5-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="00dc5-114">Rozliczenia i ceny</span><span class="sxs-lookup"><span data-stu-id="00dc5-114">Billing and pricing</span></span> | <span data-ttu-id="00dc5-115">2174616</span><span class="sxs-lookup"><span data-stu-id="00dc5-115">2174616</span></span> | <span data-ttu-id="00dc5-116">Po wygraniu oferty do niestandardowy cennik kontraktu odwołuje się do szczegółów pozycji kontraktu, które są kopiowane z oferty.</span><span class="sxs-lookup"><span data-stu-id="00dc5-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="00dc5-117">Zarządzanie szansami sprzedaży</span><span class="sxs-lookup"><span data-stu-id="00dc5-117">Opportunity Management</span></span> | <span data-ttu-id="00dc5-118">2167475</span><span class="sxs-lookup"><span data-stu-id="00dc5-118">2167475</span></span> | <span data-ttu-id="00dc5-119">Stała kwota podatku na fakturze korygującej, która pochodzi z nierozliczonych wpisów rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="00dc5-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="00dc5-120">Zarządzanie szansami sprzedaży</span><span class="sxs-lookup"><span data-stu-id="00dc5-120">Opportunity Management</span></span> | <span data-ttu-id="00dc5-121">2176285</span><span class="sxs-lookup"><span data-stu-id="00dc5-121">2176285</span></span> | <span data-ttu-id="00dc5-122">Kwota podatku nie może być kopiowana ze szczegółów umowy sprzedaży/wiersza oferty do szczegółów wiersza umowy/wiersza oferty kosztów.</span><span class="sxs-lookup"><span data-stu-id="00dc5-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="00dc5-123">Zarządzanie szansami sprzedaży</span><span class="sxs-lookup"><span data-stu-id="00dc5-123">Opportunity Management</span></span> | <span data-ttu-id="00dc5-124">2188079</span><span class="sxs-lookup"><span data-stu-id="00dc5-124">2188079</span></span> | <span data-ttu-id="00dc5-125">Reguła podzielonego fakturowania nie może być tworzona dla umów, które nie są oparte na pracy.</span><span class="sxs-lookup"><span data-stu-id="00dc5-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="00dc5-126">Planowanie i śledzenie</span><span class="sxs-lookup"><span data-stu-id="00dc5-126">Planning and Tracking</span></span> | <span data-ttu-id="00dc5-127">2138853</span><span class="sxs-lookup"><span data-stu-id="00dc5-127">2138853</span></span> | <span data-ttu-id="00dc5-128">Funkcja kopiowania projektu zaktualizowana w celu zapewnienia, że wiersze szacowania wydatków, które odwołują się do zadań, są kopiowane do projektu docelowego.</span><span class="sxs-lookup"><span data-stu-id="00dc5-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="00dc5-129">Planowanie i śledzenie</span><span class="sxs-lookup"><span data-stu-id="00dc5-129">Planning and Tracking</span></span> | <span data-ttu-id="00dc5-130">2173259</span><span class="sxs-lookup"><span data-stu-id="00dc5-130">2173259</span></span> | <span data-ttu-id="00dc5-131">Funkcja kopiowania projektu została zaktualizowana, aby upewnić się, że nie wyświetla komunikatu o błędzie **Kopiowanie SPP** w niektórych scenariuszach.</span><span class="sxs-lookup"><span data-stu-id="00dc5-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="00dc5-132">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="00dc5-132">Time and Expense</span></span> | <span data-ttu-id="00dc5-133">2148910</span><span class="sxs-lookup"><span data-stu-id="00dc5-133">2148910</span></span> | <span data-ttu-id="00dc5-134">Naprawiono problem z wyświetlaniem strony **Edytuj wpis** w siatce **Wpis czasu**.</span><span class="sxs-lookup"><span data-stu-id="00dc5-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="00dc5-135">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="00dc5-135">Time and Expense</span></span> | <span data-ttu-id="00dc5-136">2159798</span><span class="sxs-lookup"><span data-stu-id="00dc5-136">2159798</span></span> | <span data-ttu-id="00dc5-137">Zaostrzona kontrola w celu zapewnienia, że zatwierdzone wpisy wydatków nie mogą być edytowane.</span><span class="sxs-lookup"><span data-stu-id="00dc5-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


