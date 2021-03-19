---
title: Omówienie wierszy oferty opartej na produkcie - wersja uproszczona
description: Ten temat zawiera informacje dotyczące pracy z wierszami ofert opartymi na produktach.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272581"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="d1189-103">Omówienie wierszy oferty opartej na produkcie - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="d1189-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="d1189-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="d1189-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1189-105">W programie Dynamics 365 Project Operations można tworzyć wiersze ofert oparte na produktach.</span><span class="sxs-lookup"><span data-stu-id="d1189-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="d1189-106">Wiersze ofert oparte na produktach mogą być dodane ręcznie albo dotyczyć pozycji z katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="d1189-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="d1189-107">Katalog produktów</span><span class="sxs-lookup"><span data-stu-id="d1189-107">Product catalog</span></span>

<span data-ttu-id="d1189-108">Każdy produkt w katalogu produktów ma domyślną jednostkę i grupę jednostek.</span><span class="sxs-lookup"><span data-stu-id="d1189-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="d1189-109">Jeśli wiele produktów ma ten sam zestaw atrybutów, można utworzyć rodzinę produktów zawierających te wspólne atrybuty.</span><span class="sxs-lookup"><span data-stu-id="d1189-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="d1189-110">Na przykład firma sprzedaje licencje subskrypcyjne na różne typy oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="d1189-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="d1189-111">Każdy subskrybowany program ma dwa następujące atrybuty:</span><span class="sxs-lookup"><span data-stu-id="d1189-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="d1189-112">Liczba użytkowników</span><span class="sxs-lookup"><span data-stu-id="d1189-112">Number of users</span></span>
- <span data-ttu-id="d1189-113">Okres subskrypcji mierzony w miesiącach</span><span class="sxs-lookup"><span data-stu-id="d1189-113">A subscription duration measured in months</span></span>

<span data-ttu-id="d1189-114">Aby zachować ten typ katalogu, utwórz rodzinę produktów o nazwie **Subskrypcja oprogramowania** i dodaj liczbę użytkowników oraz czas trwania subskrypcji jako atrybuty.</span><span class="sxs-lookup"><span data-stu-id="d1189-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="d1189-115">Następnie możesz dodać poszczególne produkty do rodziny produktów **Oprogramowanie subskrypcyjne**.</span><span class="sxs-lookup"><span data-stu-id="d1189-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="d1189-116">Dodawanie elementów katalogu produktów do oferty projektu</span><span class="sxs-lookup"><span data-stu-id="d1189-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="d1189-117">Strony **Oferta projektu** i **Kontrakt projektu** zawierają sekcje: wiersze oparte na projekcie i wiersze oparte na produktach.</span><span class="sxs-lookup"><span data-stu-id="d1189-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="d1189-118">W przypadku linii opartych na produktach lista rozwijana w wierszu oferty lub wierszu umowy dotyczącej projektu zawiera wszystkie produkty i jednostki w cenniku produktów.</span><span class="sxs-lookup"><span data-stu-id="d1189-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="d1189-119">Można również dodawać produkty, które nie są częścią cennika produktów.</span><span class="sxs-lookup"><span data-stu-id="d1189-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="d1189-120">Oprócz tego można wybierać produkty z innych cenników lub bezpośrednio z katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="d1189-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="d1189-121">W przypadku wybierania produktów bezpośrednio z katalogu produktów do ustalania ceny sprzedaży produktu jest używany domyślny cennik tego produktu.</span><span class="sxs-lookup"><span data-stu-id="d1189-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="d1189-122">Jeśli cennik domyślny nie jest określony, system ustawia cenę zero (0).</span><span class="sxs-lookup"><span data-stu-id="d1189-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="d1189-123">Jeśli wiersz oferty jest oparty na katalogu produktów, można zastąpić cenę sprzedaży bezpośrednio w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="d1189-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="d1189-124">Wiersz oferty wpolu **Cennik** zawierający dwie dostępne wartości:</span><span class="sxs-lookup"><span data-stu-id="d1189-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="d1189-125">**Zastąp Cennik**</span><span class="sxs-lookup"><span data-stu-id="d1189-125">**Override Pricing**</span></span>
- <span data-ttu-id="d1189-126">**Użyj domyślnej**</span><span class="sxs-lookup"><span data-stu-id="d1189-126">**Use Default**</span></span>

<span data-ttu-id="d1189-127">W przypadku wybrania opcji **Zastąp cennik** cena domyślna nie jest ustawiona.</span><span class="sxs-lookup"><span data-stu-id="d1189-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="d1189-128">W zamian należy wprowadzić cenę produktu w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="d1189-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="d1189-129">W przypadku wybrania opcji **Użyj domyślnych** jest używana domyślna cena sprzedaży, a pole jest zablokowane do edycji.</span><span class="sxs-lookup"><span data-stu-id="d1189-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="d1189-130">Domyślne ceny sprzedaży są wprowadzana w wierszach opartych na produktach w ofercie.</span><span class="sxs-lookup"><span data-stu-id="d1189-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="d1189-131">Następnie w polu **Kalkulacja cen** jest ustawiana wartość **Zastąp Cennik**, tak aby można było edytować domyślną cenę w wierszach oferty.</span><span class="sxs-lookup"><span data-stu-id="d1189-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="d1189-132">Jest to zastąpienie specyficzne dla Project Operations dotyczące zachowania wierszy opartych na produkcie w rozwiązaniu Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d1189-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]