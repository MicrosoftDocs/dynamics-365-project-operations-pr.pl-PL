---
title: Szacowania zasobu
description: W tym temat zamieszczono informacje dotyczące sposobu obliczania zasobów w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081932"
---
# <a name="resource-estimates"></a><span data-ttu-id="c78e9-103">Szacowania zasobu</span><span class="sxs-lookup"><span data-stu-id="c78e9-103">Resource estimates</span></span>

<span data-ttu-id="c78e9-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="c78e9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c78e9-105">Oszacowania zasobów pochodzą z nakładu pracy faz czasowych, określonego w strukturze podziału pracy oraz w zakresie odpowiednich wymiarów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="c78e9-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="c78e9-106">Zazwyczaj obliczenia dokonywane są na podstawie następującego schematu: **współczynnik/h dla każdej roli x liczba godzin.**</span><span class="sxs-lookup"><span data-stu-id="c78e9-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="c78e9-107">Nakłady pracy faz czasowych na każdy zasób są przechowywane w rekordzie przydziału zasobu.</span><span class="sxs-lookup"><span data-stu-id="c78e9-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="c78e9-108">Cena jest przechowywana we wstępnie zdefiniowanym cenniku.</span><span class="sxs-lookup"><span data-stu-id="c78e9-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="c78e9-109">Przeliczanie jednostek jest stosowane na podstawie odpowiednich cenników.</span><span class="sxs-lookup"><span data-stu-id="c78e9-109">Unit conversion is applied based on the applicable price list.</span></span>

![Szacowania zasobu](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="c78e9-111">Wartości domyślne kosztów własnych i waluty kosztów</span><span class="sxs-lookup"><span data-stu-id="c78e9-111">Default cost price and cost currency</span></span>

<span data-ttu-id="c78e9-112">Koszty własne są domyślnie pobierane z jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="c78e9-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="c78e9-113">Domyślna stawka rozliczenia i waluta sprzedaży</span><span class="sxs-lookup"><span data-stu-id="c78e9-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="c78e9-114">Ceny sprzedaży są stosowane raz dla każdej transakcji.</span><span class="sxs-lookup"><span data-stu-id="c78e9-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="c78e9-115">Hierarchia domyślna dla cennika sprzedaży zawiera następujące dane:</span><span class="sxs-lookup"><span data-stu-id="c78e9-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="c78e9-116">Organizacja</span><span class="sxs-lookup"><span data-stu-id="c78e9-116">Organization</span></span>
2. <span data-ttu-id="c78e9-117">Klient</span><span class="sxs-lookup"><span data-stu-id="c78e9-117">Customer</span></span>
3. <span data-ttu-id="c78e9-118">Oferta / kontrakt</span><span class="sxs-lookup"><span data-stu-id="c78e9-118">Quote/contract</span></span>
