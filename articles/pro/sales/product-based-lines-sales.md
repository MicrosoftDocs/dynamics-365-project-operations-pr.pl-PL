---
title: Wiersze szansy sprzedaży oparte na produkcie
description: W tym temat zamieszczono informacje dotyczące wierszy szansy sprzedaży opartych na produkcie w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081938"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="ba652-103">Wiersze szansy sprzedaży oparte na produkcie</span><span class="sxs-lookup"><span data-stu-id="ba652-103">Product-based opportunity lines</span></span>

<span data-ttu-id="ba652-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="ba652-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba652-105">Wiersze szans sprzedaży oparte na produkcie są pozycjami w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="ba652-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="ba652-106">Te wiersze są dostarczane do klienta jako odrębne pozycje na ewentualnej fakturze bez żadnych innych usług wartości dodanych.</span><span class="sxs-lookup"><span data-stu-id="ba652-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="ba652-107">Związane z tym wydatki i zużycie nie są śledzone na zadaniach związanych z żadnymi powiązanymi projektami.</span><span class="sxs-lookup"><span data-stu-id="ba652-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="ba652-108">Wiersze oparte na produkcie mogą mieć pozycje katalogowe i produkty dopisane.</span><span class="sxs-lookup"><span data-stu-id="ba652-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="ba652-109">Większość funkcji w wierszach opartych na produkcie szansy sprzedaży działa zgodnie z funkcjami oferowanymi przez aplikację Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ba652-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="ba652-110">Aby uzyskać więcej informacji o wierszach szans sprzedaży utworzonych na podstawie produktów, zobacz [Dodawanie produktów do szansy sprzedaży](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="ba652-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="ba652-111">Jedną z koncepcji dotyczących szans sprzedaży opartych na produkcie, które są specyficzne dla szans sprzedaży opartych na projektach, jest **budżet klienta**.</span><span class="sxs-lookup"><span data-stu-id="ba652-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="ba652-112">To pole służy do śledzenia kwoty, która może być zapłacona za dany wiersz przez klienta.</span><span class="sxs-lookup"><span data-stu-id="ba652-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="ba652-113">Jeśli dla metody przychodu z podsumowania szansy sprzedaży ustawiono wartość **Obliczone przez system** , wartości budżetu klienta pomiędzy wierszami opartymi na projekcie i produkcie są sumowane w celu obliczenia szacowanego przychodu.</span><span class="sxs-lookup"><span data-stu-id="ba652-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
