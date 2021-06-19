---
title: Cenniki produktu
description: Ta temat zawiera informacje o cennikach związanych z używanych w cenach katalogowych w ofertach i kontraktach projektów.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004949"
---
# <a name="product-price-lists"></a><span data-ttu-id="c82da-103">Cenniki produktu</span><span class="sxs-lookup"><span data-stu-id="c82da-103">Product price lists</span></span>

<span data-ttu-id="c82da-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="c82da-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="c82da-105">W Project Operations **Cenniki produktów** i powiązane jednostki pozycji cennika obsługują funkcje wyceny produktów na podstawie oferty opartej na produkcie i wierszy umowy.</span><span class="sxs-lookup"><span data-stu-id="c82da-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="c82da-106">W przypadku produktów używanych w projektach używane są rekordy pozycji cennika dla cenników projektów.</span><span class="sxs-lookup"><span data-stu-id="c82da-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="c82da-107">Produkty należy skonfigurować w taki sposób, aby miały domyślne listy kosztów i cenniki w katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="c82da-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="c82da-108">W celu skonfigurowania domyślnych list kosztów i cenników należy użyć ceny katalogowej, kosztu standardowego i kosztu bieżącego.</span><span class="sxs-lookup"><span data-stu-id="c82da-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="c82da-109">Domyślne ceny katalogowe są używane w wierszu oferty lub w pozycji kontraktu projektu tylko wtedy, gdy system nie może znaleźć wiersza cennika dla tego produktu w cenniku produktu ustawionym dla oferty lub kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="c82da-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="c82da-110">Koszty własne w wierszach katalogu produktów można zmieniać miedzy ofertami.</span><span class="sxs-lookup"><span data-stu-id="c82da-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="c82da-111">Ta funkcja jest ważna, ponieważ w przypadku niedokładnego śledzenia kosztów nie można ustalić zysku operacyjnego z wykonywanych projektów.</span><span class="sxs-lookup"><span data-stu-id="c82da-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="c82da-112">Domyślnie kosztem własnym jest standardowy koszt produktu.</span><span class="sxs-lookup"><span data-stu-id="c82da-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="c82da-113">Jednak domyślny koszt własny można aktualizować w wierszu oferty, jeśli w konkretnej ofercie istnieje inny koszt własny.</span><span class="sxs-lookup"><span data-stu-id="c82da-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="c82da-114">Pozycje cennika</span><span class="sxs-lookup"><span data-stu-id="c82da-114">Price list items</span></span>

<span data-ttu-id="c82da-115">Produkty z katalogu produktów można dodawać do różnych cenników.</span><span class="sxs-lookup"><span data-stu-id="c82da-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="c82da-116">Pozycje cennika dla produktów zawsze odwołują się do określonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="c82da-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="c82da-117">Wycenę produktów figurujących na pozycjach cennika można skonfigurować jako kwotę w walucie.</span><span class="sxs-lookup"><span data-stu-id="c82da-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="c82da-118">Alternatywnie kalkulacja ceny może być funkcją ceny katalogowej, kosztu bieżącego lub kosztu standardowego.</span><span class="sxs-lookup"><span data-stu-id="c82da-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="c82da-119">Funkcja wyceny obsługuje różne opcje zaokrąglania, gdy ceny produktów są skonfigurowane jako funkcja ceny katalogowej, kosztu standardowego lub kosztu bieżącego.</span><span class="sxs-lookup"><span data-stu-id="c82da-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="c82da-120">W odniesieniu do pozycji cenników można nie tylko stosować wiele metod kalkulacji cen i opcji zaokrąglania, ale również łączyć z nimi listy rabatów.</span><span class="sxs-lookup"><span data-stu-id="c82da-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="c82da-121">Domyślny cennik produktów</span><span class="sxs-lookup"><span data-stu-id="c82da-121">Default product price list</span></span>
<span data-ttu-id="c82da-122">Każdy rekord odbiorcy zawiera pole **Cennik domyślny**, w którym można określić cennik odpowiadający walucie klienta.</span><span class="sxs-lookup"><span data-stu-id="c82da-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="c82da-123">Wartość domyślna nie jest automatycznie wprowadzana w tym polu.</span><span class="sxs-lookup"><span data-stu-id="c82da-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="c82da-124">Jeśli istnieje umowa z konkretnym odbiorcą określająca niestandardową kalkulację cen, można użyć tego pola w celu skojarzenia cennika z tym odbiorcą.</span><span class="sxs-lookup"><span data-stu-id="c82da-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="c82da-125">Encje Szansa sprzedaży, Oferta i Kontrakt projektu używają następującej kolejności wprowadzania domyślnych cenników produktów.</span><span class="sxs-lookup"><span data-stu-id="c82da-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="c82da-126">Ta sama kolejność jest stosowana w cennikach projektów.</span><span class="sxs-lookup"><span data-stu-id="c82da-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="c82da-127">Oferta</span><span class="sxs-lookup"><span data-stu-id="c82da-127">Quote</span></span>
2.  <span data-ttu-id="c82da-128">Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="c82da-128">Opportunity</span></span>
3.  <span data-ttu-id="c82da-129">Klient</span><span class="sxs-lookup"><span data-stu-id="c82da-129">Customer</span></span>
4.  <span data-ttu-id="c82da-130">Ustawienia globalne</span><span class="sxs-lookup"><span data-stu-id="c82da-130">Global settings</span></span> 

<span data-ttu-id="c82da-131">Domyślnie w polu **Produkt** w wierszu oferty znajduje się lista wszystkich aktywnych produktów z cennika produktów w ofercie.</span><span class="sxs-lookup"><span data-stu-id="c82da-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="c82da-132">Jeśli produkt został zdezaktywowany lub jest wersją roboczą, nie jest on wymieniony na tej liście, nawet jeśli znajduje się w cenniku.</span><span class="sxs-lookup"><span data-stu-id="c82da-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="c82da-133">Wiersze katalogu produktów są dodawane jako wiersze faktury w pierwszej fakturze tworzonej dla kontraktu na projekt.</span><span class="sxs-lookup"><span data-stu-id="c82da-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="c82da-134">W fakturze w wersji roboczej te wiersze faktury można usuwać.</span><span class="sxs-lookup"><span data-stu-id="c82da-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="c82da-135">W takim przypadku wiersze będą wyświetlane na kolejnej fakturze do momentu ich zafakturowania lub do chwili wysłania faktury do klienta.</span><span class="sxs-lookup"><span data-stu-id="c82da-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="c82da-136">Nie można zafakturować częściowej ilości w wierszu faktury za produkt.</span><span class="sxs-lookup"><span data-stu-id="c82da-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="c82da-137">Podczas fakturowania wierszy produktów z kontraktu na projekt są tworzone wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="c82da-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="c82da-138">Jednak te wartości rzeczywiste nie są łączone z pokrewną encją projektu.</span><span class="sxs-lookup"><span data-stu-id="c82da-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="c82da-139">Innymi słowy pozycje kontraktu projektu oparte na produktach są niezależne od jakiegokolwiek użycia opartego na projekcie.</span><span class="sxs-lookup"><span data-stu-id="c82da-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
