---
title: Wycena wierszy oferty opartej na produkcie
description: Ta temat zawiera informacje o stosowaniu kosztu własnego w wierszu oferty opartej na produktach.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081915"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="fff25-103">Wycena wierszy oferty opartej na produkcie</span><span class="sxs-lookup"><span data-stu-id="fff25-103">Costing product-based quote lines</span></span>

<span data-ttu-id="fff25-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="fff25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fff25-105">Wiersze oferty opartej na produkcie w Dynamics 365 Project Operations są również dostępne jako pole **Kosztu własnego**.</span><span class="sxs-lookup"><span data-stu-id="fff25-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="fff25-106">To pole jest używane do śledzenia kosztu własnego produktu w wierszu oferty oraz na potrzeby obliczeń opłacalności na niższych poziomach.</span><span class="sxs-lookup"><span data-stu-id="fff25-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="fff25-107">W przypadku tworzenia wiersza oferty opartej na produkcie dotyczącego produktu z katalogu, cena w wierszu oferty opartej na produkcie jest domyślnie określana na podstawie pola **Koszt normatywny** w katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="fff25-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="fff25-108">Pole Koszt normatywny w katalogu produktów jest podawane w walucie podstawowej organizacji.</span><span class="sxs-lookup"><span data-stu-id="fff25-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="fff25-109">Domyślny koszt jednostkowy w wierszu oferty opartej na produkcie jest konwertowany na walutę sprzedaży z oferty.</span><span class="sxs-lookup"><span data-stu-id="fff25-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="fff25-110">Koszt jednostkowy w wierszu oferty opartej na produkcie</span><span class="sxs-lookup"><span data-stu-id="fff25-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="fff25-111">Celem dysponowania kosztami jednostkowymi w wierszu oferty opartej na produkcie jest zezwolenie na zastosowanie różnych kosztów produktu w danej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="fff25-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="fff25-112">Nie jest to typowy scenariusz użycia, ale czasami koszt produktu może być obniżony przez dostawcę w zależności od klienta.</span><span class="sxs-lookup"><span data-stu-id="fff25-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="fff25-113">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="fff25-113">For example:</span></span>

<span data-ttu-id="fff25-114">Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="fff25-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="fff25-115">Firma Fabrikam oferuje usługi instalacyjne, ale ramiona są wytwarzane przez inną firmę — Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="fff25-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="fff25-116">Jeśli instalacja ramion w Datum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki.</span><span class="sxs-lookup"><span data-stu-id="fff25-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="fff25-117">W takiej sytuacji Fabrikam będzie tworzył wiersz oferty opartej na produkcie dla ramion robotycznych i skorzystać ze specjalnego kosztu jednostkowego dla takiej oferty.</span><span class="sxs-lookup"><span data-stu-id="fff25-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="fff25-118">Koszty różnią się od kosztów normatywnych ramion robotycznych Trey.</span><span class="sxs-lookup"><span data-stu-id="fff25-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
