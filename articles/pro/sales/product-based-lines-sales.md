---
title: Wiesze szansy sprzedaży oparte na produkcie - wersja uproszczona
description: W tym temat zamieszczono informacje dotyczące wierszy szansy sprzedaży opartych na produkcie w Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949557"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="1f958-103">Wiesze szansy sprzedaży oparte na produkcie - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="1f958-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="1f958-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="1f958-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f958-105">Wiersze szans sprzedaży oparte na produkcie są pozycjami w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="1f958-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="1f958-106">Te odrębne pozycje znajdują się na ostatecznej fakturze dostarczanej klientowi.</span><span class="sxs-lookup"><span data-stu-id="1f958-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="1f958-107">Faktura nie obejmuje żadnych innych usług dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="1f958-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="1f958-108">Związane z tym wydatki i zużycie nie są śledzone na zadaniach związanych z żadnymi powiązanymi projektami.</span><span class="sxs-lookup"><span data-stu-id="1f958-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="1f958-109">Wiersze oparte na produkcie mogą mieć pozycje katalogowe i produkty dopisane.</span><span class="sxs-lookup"><span data-stu-id="1f958-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="1f958-110">Większość funkcji w wierszach opartych na produkcie szansy sprzedaży działa zgodnie z funkcjami oferowanymi przez aplikację Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="1f958-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="1f958-111">Aby uzyskać więcej informacji o wierszach szans sprzedaży utworzonych na podstawie produktów, zobacz [Dodawanie produktów do szansy sprzedaży](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="1f958-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="1f958-112">**Budżet klienta** to koncepcja, która jest specyficzna dla wierszy szansy sprzedaży opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="1f958-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="1f958-113">Pole **Budżet klienta** śledzi kwotę, jaką odbiorca jest gotów zapłacić za przedmiot.</span><span class="sxs-lookup"><span data-stu-id="1f958-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="1f958-114">Gdy metodą przychodów podsumowania szansy sprzedaży jest **Obliczony przez system**, wartości budżetu klienta w wierszach szansy sprzedaży są sumowane w celu obliczenia szacowanego przychodu.</span><span class="sxs-lookup"><span data-stu-id="1f958-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]