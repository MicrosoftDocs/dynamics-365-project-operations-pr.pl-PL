---
title: Wycena pozycji kontraktu opartego na produkcie - wersja uproszczona
description: Ten temat zawiera informacje o tworzeniu
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273706"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="8a09b-103">Wycena pozycji kontraktu opartego na produkcie - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="8a09b-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="8a09b-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="8a09b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8a09b-105">Wiersze kontraktu oparte na produkcie w Dynamics 365 Project Operations zawierają pole **Koszt własny**, w którym przechowywana jest cena własna produktu na potrzeby obliczeń rentowności na dalszych etapach.</span><span class="sxs-lookup"><span data-stu-id="8a09b-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="8a09b-106">Po utworzeniu pozycji umowy opartej na produktach dla produktu z katalogu, koszt wiersza jest ustawiany domyślnie w polu **Koszt normatywny** w katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="8a09b-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="8a09b-107">Pole **Koszt normatywny** w katalogu produktów jest podawane w walucie podstawowej organizacji.</span><span class="sxs-lookup"><span data-stu-id="8a09b-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="8a09b-108">Kiedy koszt jednostkowy jest domyślnie związany z pozycją kontraktu, jest konwertowany na walutę sprzedaży dotyczącą kontraktu.</span><span class="sxs-lookup"><span data-stu-id="8a09b-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="8a09b-109">Koszt jednostkowy w wierszu kontraktu opartej na produkcie</span><span class="sxs-lookup"><span data-stu-id="8a09b-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="8a09b-110">Dysponowanie kosztami jednostkowymi w wierszu kontraktu opartego na produkcie pozwala na zastosowanie różnych kosztów produktu w danej sprzedaży jednostki.</span><span class="sxs-lookup"><span data-stu-id="8a09b-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="8a09b-111">Choć nie zawsze jest to konieczne, istnieje kilka scenariuszy, w których koszt produktu może być zredukowany na rzecz klienta.</span><span class="sxs-lookup"><span data-stu-id="8a09b-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="8a09b-112">Rozważmy następujący scenariusz:</span><span class="sxs-lookup"><span data-stu-id="8a09b-112">Consider the following scenario:</span></span>

<span data-ttu-id="8a09b-113">Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="8a09b-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="8a09b-114">Firma Fabrikam świadczy usługi instalacyjne, ale ramiona robotów pochodzą z firmy Trey Research.</span><span class="sxs-lookup"><span data-stu-id="8a09b-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="8a09b-115">Jeśli instalacja ramion w Adatum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey Research, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki.</span><span class="sxs-lookup"><span data-stu-id="8a09b-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="8a09b-116">W takim przypadku firma Fabrikam tworzy linię kontraktową opartą na produktach dla ramion robotów.</span><span class="sxs-lookup"><span data-stu-id="8a09b-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="8a09b-117">W przypadku kontraktu jest wprowadzany koszt jednostkowy.</span><span class="sxs-lookup"><span data-stu-id="8a09b-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="8a09b-118">Koszt jest inny niż koszt zakupu od firmy Trey Research.</span><span class="sxs-lookup"><span data-stu-id="8a09b-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]