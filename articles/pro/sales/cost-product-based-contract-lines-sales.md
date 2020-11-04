---
title: Wycena pozycji kontraktu opartej na produkcie
description: Ten temat zawiera informacje o tworzeniu
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/20/2020
ms.locfileid: "4082243"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="e113b-103">Wycena pozycji kontraktu opartej na produkcie</span><span class="sxs-lookup"><span data-stu-id="e113b-103">Costing product-based contract lines</span></span>

<span data-ttu-id="e113b-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="e113b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e113b-105">Pozycje kontraktu oparte na produktach dostępne w Dynamics 365 Project Operations to pole **Koszt własny** , w którym są przechowywane koszty własne produktu w celu realizacji obliczeń opłacalności podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="e113b-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="e113b-106">W przypadku tworzenia wiersza kontraktu opartego na produkcie dotyczącego produktu z katalogu, cena w wierszu kontraktu opartym na produkcie jest domyślnie określana na podstawie pola **Koszt normatywny** w katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="e113b-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="e113b-107">Pole **Koszt normatywny** w katalogu produktów jest podawane w walucie podstawowej organizacji.</span><span class="sxs-lookup"><span data-stu-id="e113b-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="e113b-108">Kiedy koszt jednostkowy jest domyślnie związany z pozycją kontraktu, jest konwertowany na walutę sprzedaży dotyczącą kontraktu.</span><span class="sxs-lookup"><span data-stu-id="e113b-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="e113b-109">Koszt jednostkowy w wierszu kontraktu opartej na produkcie</span><span class="sxs-lookup"><span data-stu-id="e113b-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="e113b-110">Dysponowanie kosztami jednostkowymi w wierszu kontraktu opartego na produkcie pozwala na zastosowanie różnych kosztów produktu w danej sprzedaży jednostki.</span><span class="sxs-lookup"><span data-stu-id="e113b-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="e113b-111">Choć nie zawsze jest to konieczne, istnieje kilka scenariuszy, w których koszt produktu może być zredukowany na rzecz klienta.</span><span class="sxs-lookup"><span data-stu-id="e113b-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="e113b-112">Rozważmy następujący scenariusz:</span><span class="sxs-lookup"><span data-stu-id="e113b-112">Consider the following scenario:</span></span>

<span data-ttu-id="e113b-113">Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="e113b-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="e113b-114">Firma Fabrikam oferuje usługi instalacyjne, ale ramiona są wytwarzane przez inną firmę — Trey Research.</span><span class="sxs-lookup"><span data-stu-id="e113b-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="e113b-115">Jeśli instalacja ramion w Adatum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey Research, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki.</span><span class="sxs-lookup"><span data-stu-id="e113b-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="e113b-116">W tym przypadku w firmie Fabrikam zostanie utworzona pozycja kontraktu oparta na produktach dla ramion robotycznych, w której podana jest cena jednostkowa dla tego kontraktu, różniąca się od standardowego kosztu ramion robotycznych od Trey Research.</span><span class="sxs-lookup"><span data-stu-id="e113b-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
