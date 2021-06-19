---
title: Wyłączanie wymiaru kalkulacji cen
description: Ten temat zawiera informacje na temat konfigurowania wymiarów kalkulacji cen w rozwiązaniu Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014309"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="e1791-103">Wyłączanie wymiaru kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="e1791-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e1791-104">Co kilka lat może zaistnieć konieczność przejrzenia i zaktualizowania strategii kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="e1791-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="e1791-105">Wszelkie aktualizacje wprowadzone przez użytkownika mogą wymagać wyłączenia istniejącego wymiaru kalkulacji cen i utworzenia nowego.</span><span class="sxs-lookup"><span data-stu-id="e1791-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="e1791-106">Na przykład uprzednio cena mogła być ustalana według kryterium **Rola**, ale obecnie użytkownik zdecydował się wyceniać według kryterium **Doświadczenie zawodowe**.</span><span class="sxs-lookup"><span data-stu-id="e1791-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="e1791-107">Może to wymagać wyłączenia encji **Rola** jako wymiaru kalkulacji cen i utworzenia encji **Doświadczenie zawodowe** jako nowego wymiaru kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="e1791-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="e1791-108">Wyłączenia wymiaru kalkulacji cen, bez względu na to, czy jest on gotowy czy niestandardowy, można dokonać, ustawiając w wymiarze kalkulacji cen w polach **Ma zastosowanie do kosztu** i **Ma zastosowanie do sprzedaży** wartość **Nie**.</span><span class="sxs-lookup"><span data-stu-id="e1791-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="e1791-109">Podczas wykonywania tej czynności może jednak zostać wyświetlony następujący komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="e1791-109">However, when you do this, you might receive the following error message.</span></span>

![Błąd procesu biznesowego prawdopodobny podczas wyłączania wymiaru kalkulacji cen](media/Business-Process-Error.png)


<span data-ttu-id="e1791-111">Ten komunikat o błędzie oznacza, że istnieją rekordy cen, które uprzednio skonfigurowano dla wyłączanego wymiaru.</span><span class="sxs-lookup"><span data-stu-id="e1791-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="e1791-112">Wszystkie rekordy **Cena roli** i **Narzut na cenę dla roli** odwołujące się do wymiaru muszą zostać usunięte, zanim dla wymiaru będzie można ustawić stosowalność **Nie**.</span><span class="sxs-lookup"><span data-stu-id="e1791-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="e1791-113">Ta reguła ma zastosowanie zarówno do gotowych wymiarów kalkulacji cen, jak i wszelkich niestandardowych wymiarów kalkulacji cen utworzonych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e1791-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="e1791-114">To sprawdzanie poprawności wynika z faktu, że usługa Project Service ma ograniczenie, że każdy rekord **Cena roli** musi mieć unikatową kombinację wymiarów.</span><span class="sxs-lookup"><span data-stu-id="e1791-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="e1791-115">Na przykład w cenniku zatytułowanym **Stawki kosztów US 2018** istnieją poniższe wiersze **Cena roli**.</span><span class="sxs-lookup"><span data-stu-id="e1791-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="e1791-116">Standardowe stanowisko</span><span class="sxs-lookup"><span data-stu-id="e1791-116">Standard Title</span></span>         | <span data-ttu-id="e1791-117">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="e1791-117">Org Unit</span></span>    |<span data-ttu-id="e1791-118">Jednostka</span><span class="sxs-lookup"><span data-stu-id="e1791-118">Unit</span></span>   |<span data-ttu-id="e1791-119">Cena</span><span class="sxs-lookup"><span data-stu-id="e1791-119">Price</span></span>  |<span data-ttu-id="e1791-120">Waluta</span><span class="sxs-lookup"><span data-stu-id="e1791-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="e1791-121">Inżynier systemów</span><span class="sxs-lookup"><span data-stu-id="e1791-121">Systems Engineer</span></span>|<span data-ttu-id="e1791-122">Contoso — USA</span><span class="sxs-lookup"><span data-stu-id="e1791-122">Contoso US</span></span>|<span data-ttu-id="e1791-123">godzina</span><span class="sxs-lookup"><span data-stu-id="e1791-123">Hour</span></span>| <span data-ttu-id="e1791-124">100</span><span class="sxs-lookup"><span data-stu-id="e1791-124">100</span></span>|<span data-ttu-id="e1791-125">USD</span><span class="sxs-lookup"><span data-stu-id="e1791-125">USD</span></span>|
| <span data-ttu-id="e1791-126">Starszy inżynier systemów</span><span class="sxs-lookup"><span data-stu-id="e1791-126">Senior Systems Engineer</span></span>|<span data-ttu-id="e1791-127">Contoso — USA</span><span class="sxs-lookup"><span data-stu-id="e1791-127">Contoso US</span></span>|<span data-ttu-id="e1791-128">godzina</span><span class="sxs-lookup"><span data-stu-id="e1791-128">Hour</span></span>| <span data-ttu-id="e1791-129">150</span><span class="sxs-lookup"><span data-stu-id="e1791-129">150</span></span>| <span data-ttu-id="e1791-130">USD</span><span class="sxs-lookup"><span data-stu-id="e1791-130">USD</span></span>|


<span data-ttu-id="e1791-131">Gdy wyłączysz encję **Standardowe stanowisko** jako wymiar kalkulacji, aparat kalkulacji cen w usłudze Project Service podczas wyszukiwania ceny będzie z kontekstu wejściowego używał tylko wartości **Jednostka organizacyjna**.</span><span class="sxs-lookup"><span data-stu-id="e1791-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="e1791-132">Jeśli **Jednostka organizacyjna** kontekstu wejściowego to „Contoso US”, wynik będzie nieokreślony, ponieważ oba wiersze będą pasować.</span><span class="sxs-lookup"><span data-stu-id="e1791-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="e1791-133">Aby uniknąć tego scenariusza, podczas tworzenia rekordów **Cena roli** program Project Service sprawdza, czy kombinacja wymiarów jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="e1791-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="e1791-134">Jeśli wymiar zostanie wyłączony po utworzeniu rekordów **Cena roli**, może nastąpić naruszenie tego ograniczenia.</span><span class="sxs-lookup"><span data-stu-id="e1791-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="e1791-135">Z tego powodu przed wyłączeniem wymiaru trzeba koniecznie usunąć wszystkie wiersze **Cena roli** i **Narzut na cenę dla roli**, które mają wypełnioną tę wartość wymiaru.</span><span class="sxs-lookup"><span data-stu-id="e1791-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]