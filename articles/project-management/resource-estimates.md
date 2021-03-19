---
title: Szacowania zasobu
description: W tym temat zamieszczono informacje dotyczące sposobu obliczania zasobów w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286531"
---
# <a name="resource-estimates"></a><span data-ttu-id="daa6c-103">Szacowania zasobu</span><span class="sxs-lookup"><span data-stu-id="daa6c-103">Resource estimates</span></span>

<span data-ttu-id="daa6c-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="daa6c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="daa6c-105">Oszacowania zasobów pochodzą z nakładu pracy faz czasowych, określonego w strukturze podziału pracy oraz w zakresie odpowiednich wymiarów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="daa6c-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="daa6c-106">Zazwyczaj obliczenia dokonywane są na podstawie następującego schematu: **współczynnik/h dla każdej roli x liczba godzin.**</span><span class="sxs-lookup"><span data-stu-id="daa6c-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="daa6c-107">Nakłady pracy faz czasowych na każdy zasób są przechowywane w rekordzie przydziału zasobu.</span><span class="sxs-lookup"><span data-stu-id="daa6c-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="daa6c-108">Cena jest przechowywana we wstępnie zdefiniowanym cenniku.</span><span class="sxs-lookup"><span data-stu-id="daa6c-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="daa6c-109">Przeliczanie jednostek jest stosowane na podstawie odpowiednich cenników.</span><span class="sxs-lookup"><span data-stu-id="daa6c-109">Unit conversion is applied based on the applicable price list.</span></span>

![Szacowania zasobu](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="daa6c-111">Wartości domyślne kosztów własnych i waluty kosztów</span><span class="sxs-lookup"><span data-stu-id="daa6c-111">Default cost price and cost currency</span></span>

<span data-ttu-id="daa6c-112">Koszty własne są domyślnie pobierane z jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="daa6c-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="daa6c-113">Domyślna stawka rozliczenia i waluta sprzedaży</span><span class="sxs-lookup"><span data-stu-id="daa6c-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="daa6c-114">Ceny sprzedaży są stosowane raz dla każdej transakcji.</span><span class="sxs-lookup"><span data-stu-id="daa6c-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="daa6c-115">Hierarchia domyślna dla cennika sprzedaży zawiera następujące dane:</span><span class="sxs-lookup"><span data-stu-id="daa6c-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="daa6c-116">Organizacja</span><span class="sxs-lookup"><span data-stu-id="daa6c-116">Organization</span></span>
2. <span data-ttu-id="daa6c-117">Klient</span><span class="sxs-lookup"><span data-stu-id="daa6c-117">Customer</span></span>
3. <span data-ttu-id="daa6c-118">Oferta / kontrakt</span><span class="sxs-lookup"><span data-stu-id="daa6c-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]