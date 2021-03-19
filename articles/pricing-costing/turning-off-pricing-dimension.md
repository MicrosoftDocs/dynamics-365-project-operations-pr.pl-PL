---
title: Wyłączanie wymiaru kalkulacji cen
description: Ten temat zawiera informacje na temat wyłączenia niestandardowych wymiarów kalkulacji cen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274741"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="6dc03-103">Wyłączanie wymiaru kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="6dc03-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="6dc03-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="6dc03-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6dc03-105">Co kilka lat może zaistnieć konieczność przejrzenia i zaktualizowania strategii kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="6dc03-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="6dc03-106">Wszelkie aktualizacje wprowadzone przez użytkownika mogą wymagać wyłączenia istniejącego wymiaru kalkulacji cen i utworzenia nowego.</span><span class="sxs-lookup"><span data-stu-id="6dc03-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="6dc03-107">Na przykład uprzednio cena mogła być ustalana według kryterium **Rola**, ale obecnie użytkownik zdecydował się wyceniać według kryterium **Doświadczenie zawodowe**.</span><span class="sxs-lookup"><span data-stu-id="6dc03-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="6dc03-108">Może to wymagać wyłączenia encji **Rola** jako wymiaru kalkulacji cen i utworzenia encji **Doświadczenie zawodowe** jako nowego wymiaru kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="6dc03-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="6dc03-109">Wyłączenia wymiaru kalkulacji cen, bez względu na to, czy jest on gotowy czy niestandardowy, można dokonać, ustawiając w wymiarze kalkulacji cen w polach **Ma zastosowanie do kosztu** i **Ma zastosowanie do sprzedaży** wartość **Nie**.</span><span class="sxs-lookup"><span data-stu-id="6dc03-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="6dc03-110">Po wykonaniu tej czynności może jednak zostać wyświetlony komunikat o błędzie pt. **Wymiar kalkulacji cen nie może być aktualizowany ani usuwany, jeśli istnieją rekordy skojarzonych rekordów cen**.</span><span class="sxs-lookup"><span data-stu-id="6dc03-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Błąd procesu biznesowego prawdopodobny podczas wyłączania wymiaru kalkulacji cen](media/Business-Process-Error.png)

<span data-ttu-id="6dc03-112">Ten komunikat o błędzie oznacza, że istnieją rekordy cen, które uprzednio skonfigurowano dla wyłączanego wymiaru.</span><span class="sxs-lookup"><span data-stu-id="6dc03-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="6dc03-113">Wszystkie rekordy **Cena roli** i **Narzut na cenę dla roli** odwołujące się do wymiaru muszą zostać usunięte, zanim dla wymiaru będzie można ustawić stosowalność **Nie**.</span><span class="sxs-lookup"><span data-stu-id="6dc03-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="6dc03-114">Ta reguła ma zastosowanie zarówno do gotowych wymiarów kalkulacji cen, jak i wszelkich niestandardowych wymiarów kalkulacji cen utworzonych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6dc03-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="6dc03-115">To sprawdzanie poprawności wynika z faktu, że każdy rekord **Cena roli** musi mieć unikatową kombinację wymiarów.</span><span class="sxs-lookup"><span data-stu-id="6dc03-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="6dc03-116">Na przykład w cenniku zatytułowanym **Stawki kosztów US 2018** istnieją poniższe wiersze **Cena roli**.</span><span class="sxs-lookup"><span data-stu-id="6dc03-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="6dc03-117">Standardowe stanowisko</span><span class="sxs-lookup"><span data-stu-id="6dc03-117">Standard Title</span></span>         | <span data-ttu-id="6dc03-118">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="6dc03-118">Org Unit</span></span>    |<span data-ttu-id="6dc03-119">Jednostka</span><span class="sxs-lookup"><span data-stu-id="6dc03-119">Unit</span></span>   |<span data-ttu-id="6dc03-120">Cena</span><span class="sxs-lookup"><span data-stu-id="6dc03-120">Price</span></span>  |<span data-ttu-id="6dc03-121">Waluta</span><span class="sxs-lookup"><span data-stu-id="6dc03-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="6dc03-122">Inżynier systemów</span><span class="sxs-lookup"><span data-stu-id="6dc03-122">Systems Engineer</span></span>|<span data-ttu-id="6dc03-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="6dc03-123">Contoso US</span></span>|<span data-ttu-id="6dc03-124">Hour</span><span class="sxs-lookup"><span data-stu-id="6dc03-124">Hour</span></span>| <span data-ttu-id="6dc03-125">100</span><span class="sxs-lookup"><span data-stu-id="6dc03-125">100</span></span>|<span data-ttu-id="6dc03-126">USD</span><span class="sxs-lookup"><span data-stu-id="6dc03-126">USD</span></span>|
| <span data-ttu-id="6dc03-127">Starszy inżynier systemów</span><span class="sxs-lookup"><span data-stu-id="6dc03-127">Senior Systems Engineer</span></span>|<span data-ttu-id="6dc03-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="6dc03-128">Contoso US</span></span>|<span data-ttu-id="6dc03-129">Hour</span><span class="sxs-lookup"><span data-stu-id="6dc03-129">Hour</span></span>| <span data-ttu-id="6dc03-130">150</span><span class="sxs-lookup"><span data-stu-id="6dc03-130">150</span></span>| <span data-ttu-id="6dc03-131">USD</span><span class="sxs-lookup"><span data-stu-id="6dc03-131">USD</span></span>|


<span data-ttu-id="6dc03-132">Gdy wyłączysz encję **Standardowe stanowisko** jako wymiar kalkulacji, aparat kalkulacji cen podczas wyszukiwania ceny będzie z kontekstu wejściowego używał tylko wartości **Jednostka organizacyjna**.</span><span class="sxs-lookup"><span data-stu-id="6dc03-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="6dc03-133">Jeśli element **Jednostka organizacyjna** w kontekście wejściowym ma wartość „Contoso US”, wynik będzie niedeterministyczny, ponieważ oba wiersze będą pasowały.</span><span class="sxs-lookup"><span data-stu-id="6dc03-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="6dc03-134">Aby uniknąć tego scenariusza, podczas tworzenia rekordów **Cena roli** program sprawdza, czy kombinacja wymiarów jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="6dc03-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="6dc03-135">Jeśli wymiar zostanie wyłączony po utworzeniu rekordów **Cena roli**, może nastąpić naruszenie tego ograniczenia.</span><span class="sxs-lookup"><span data-stu-id="6dc03-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="6dc03-136">Z tego powodu przed wyłączeniem wymiaru trzeba koniecznie usunąć wszystkie wiersze **Cena roli** i **Narzut na cenę dla roli**, które mają wypełnioną tę wartość wymiaru.</span><span class="sxs-lookup"><span data-stu-id="6dc03-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]