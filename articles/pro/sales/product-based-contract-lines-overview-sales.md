---
title: Omówienie pozycji kontraktu opartego na produkcie - wersja uproszczona
description: Ta temat zawiera informacje o wierszach kontraktów opartych na produktach.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994554"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="aae8a-103">Omówienie pozycji kontraktu opartego na produkcie - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="aae8a-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="aae8a-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="aae8a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aae8a-105">W programie Dynamics 365 Project Operations można tworzyć pozycje kontraktu oparte na produktach.</span><span class="sxs-lookup"><span data-stu-id="aae8a-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="aae8a-106">Wiersze kontraktów oparte na produktach mogą być ręcznie tworzone albo dotyczyć pozycji z katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="aae8a-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="aae8a-107">Katalog produktów</span><span class="sxs-lookup"><span data-stu-id="aae8a-107">Product catalog</span></span>

<span data-ttu-id="aae8a-108">Produkty w katalogu produktów mają domyślne jednostki i grupy jednostek.</span><span class="sxs-lookup"><span data-stu-id="aae8a-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="aae8a-109">Jeśli wiele produktów ma ten sam zestaw atrybutów, można utworzyć rodzinę produktów zawierających te wspólne atrybuty.</span><span class="sxs-lookup"><span data-stu-id="aae8a-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="aae8a-110">Wszystkie produkty w jednej rodzinie produktów dziedziczą ten sam zestaw atrybutów.</span><span class="sxs-lookup"><span data-stu-id="aae8a-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="aae8a-111">Na przykład firma sprzedaje licencje subskrypcyjne na różne typy oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="aae8a-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="aae8a-112">Każdy subskrybowany program ma dwa następujące atrybuty:</span><span class="sxs-lookup"><span data-stu-id="aae8a-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="aae8a-113">Liczba użytkowników</span><span class="sxs-lookup"><span data-stu-id="aae8a-113">Number of users</span></span>
- <span data-ttu-id="aae8a-114">Czas trwania subskrypcji (w miesiącach)</span><span class="sxs-lookup"><span data-stu-id="aae8a-114">Subscription duration (in months)</span></span>

<span data-ttu-id="aae8a-115">Aby zachować katalog tego typu, należy utworzyć rodzinę produktów z nazwą **Oprogramowanie subskrypcyjne**.</span><span class="sxs-lookup"><span data-stu-id="aae8a-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="aae8a-116">Dodaj atrybuty, **liczbę użytkowników** i **Czas trwania subskrypcji** do rodziny produktów.</span><span class="sxs-lookup"><span data-stu-id="aae8a-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="aae8a-117">Następnie należy dodać poszczególne produkty do rodziny produktów **Oprogramowania subskrypcyjnego**.</span><span class="sxs-lookup"><span data-stu-id="aae8a-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="aae8a-118">Dodawanie elementów katalogu produktów do kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="aae8a-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="aae8a-119">Kontrakty projektu dwa typy wierszy: wiersze oparte na projekcie i wiersze oparte na produktach.</span><span class="sxs-lookup"><span data-stu-id="aae8a-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="aae8a-120">Wiersze oparte na produktach zawierają wszystkie produkty i jednostki z cennika produktów w kontrakcie.</span><span class="sxs-lookup"><span data-stu-id="aae8a-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="aae8a-121">Można również dodawać produkty, które nie są częścią cennika produktów dołączonego do kontraktu.</span><span class="sxs-lookup"><span data-stu-id="aae8a-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="aae8a-122">Użytkownik może wybrać produkty z innych cenników lub bezpośrednio z katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="aae8a-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="aae8a-123">W przypadku wybierania produktów bezpośrednio z katalogu produktów do ustalania ceny sprzedaży produktu jest używany domyślny cennik tego produktu.</span><span class="sxs-lookup"><span data-stu-id="aae8a-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="aae8a-124">Jeśli cennik domyślny nie jest określony, system ustawia cenę 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="aae8a-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="aae8a-125">Jeśli wiersz kontraktu jest oparty na katalogu produktów, można zastąpić cenę sprzedaży bezpośrednio w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="aae8a-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="aae8a-126">Pozycja kontraktu zawiera pole **Cennik** i dwie wartości:</span><span class="sxs-lookup"><span data-stu-id="aae8a-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="aae8a-127">**Zastąp kalkulację ceny**</span><span class="sxs-lookup"><span data-stu-id="aae8a-127">**Override pricing**</span></span>
- <span data-ttu-id="aae8a-128">**Użyj domyślnego**</span><span class="sxs-lookup"><span data-stu-id="aae8a-128">**Use default**</span></span>

<span data-ttu-id="aae8a-129">Jeśli w polu **Kalkulacja cen** zostanie ustawiona wartość **Zastąp kalkulację ceny**, nie jest ustawiana cena domyślna.</span><span class="sxs-lookup"><span data-stu-id="aae8a-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="aae8a-130">Wprowadź cenę produktu w pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="aae8a-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="aae8a-131">Jeśli pole ma **Używać wartości domyślnych**, jest używana domyślna cena sprzedaży i nie można edytować pola.</span><span class="sxs-lookup"><span data-stu-id="aae8a-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="aae8a-132">Po zainstalowaniu rozwiązania Project Operations domyślne ceny sprzedaży są wprowadzane w wierszach opartych na produktach w kontrakcie.</span><span class="sxs-lookup"><span data-stu-id="aae8a-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="aae8a-133">Następnie w polu **Kalkulacja cen** jest ustawiana wartość **Zastąp kalkulację ceny**, tak aby można było edytować domyślną cenę w wierszach kontraktu.</span><span class="sxs-lookup"><span data-stu-id="aae8a-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="aae8a-134">Jest to opcja zastąpienia dostępna w Project Operations dla wierszy opartych na produkcie w Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="aae8a-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]