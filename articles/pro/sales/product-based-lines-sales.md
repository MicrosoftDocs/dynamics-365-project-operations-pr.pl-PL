---
title: Wiesze szansy sprzedaży oparte na produkcie - wersja uproszczona
description: W tym temat zamieszczono informacje dotyczące wierszy szansy sprzedaży opartych na produkcie w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176352"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="b8032-103">Wiesze szansy sprzedaży oparte na produkcie - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="b8032-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="b8032-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="b8032-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b8032-105">Wiersze szans sprzedaży oparte na produkcie są pozycjami w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b8032-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="b8032-106">Te wiersze są dostarczane do klienta jako odrębne pozycje na ewentualnej fakturze bez żadnych innych usług wartości dodanych.</span><span class="sxs-lookup"><span data-stu-id="b8032-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="b8032-107">Związane z tym wydatki i zużycie nie są śledzone na zadaniach związanych z żadnymi powiązanymi projektami.</span><span class="sxs-lookup"><span data-stu-id="b8032-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="b8032-108">Wiersze oparte na produkcie mogą mieć pozycje katalogowe i produkty dopisane.</span><span class="sxs-lookup"><span data-stu-id="b8032-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="b8032-109">Większość funkcji w wierszach opartych na produkcie szansy sprzedaży działa zgodnie z funkcjami oferowanymi przez aplikację Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b8032-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="b8032-110">Aby uzyskać więcej informacji o wierszach szans sprzedaży utworzonych na podstawie produktów, zobacz [Dodawanie produktów do szansy sprzedaży](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="b8032-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="b8032-111">Jedną z koncepcji dotyczących szans sprzedaży opartych na produkcie, które są specyficzne dla szans sprzedaży opartych na projektach, jest **budżet klienta**.</span><span class="sxs-lookup"><span data-stu-id="b8032-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="b8032-112">To pole służy do śledzenia kwoty, która może być zapłacona za dany wiersz przez klienta.</span><span class="sxs-lookup"><span data-stu-id="b8032-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="b8032-113">Jeśli dla metody przychodu z podsumowania szansy sprzedaży ustawiono wartość **Obliczone przez system**, wartości budżetu klienta pomiędzy wierszami opartymi na projekcie i produkcie są sumowane w celu obliczenia szacowanego przychodu.</span><span class="sxs-lookup"><span data-stu-id="b8032-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
