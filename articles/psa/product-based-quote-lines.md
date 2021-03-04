---
title: Wiersze ofert oparte na produktach
description: Ta temat zawiera informacje o wierszach ofert opartych na produktach.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151266"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="d6003-103">Wiersze ofert oparte na produktach</span><span class="sxs-lookup"><span data-stu-id="d6003-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="d6003-104">W programie Dynamics 365 Project Service Automation można tworzyć wiersze ofert oparte na produktach.</span><span class="sxs-lookup"><span data-stu-id="d6003-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="d6003-105">Wiersze ofert oparte na produktach mogą być „dopisywane” albo dotyczyć pozycji z katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="d6003-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="d6003-106">Katalog produktów</span><span class="sxs-lookup"><span data-stu-id="d6003-106">Product catalog</span></span>

<span data-ttu-id="d6003-107">Produkty w katalogu produktów w rozwiązaniu Dynamics 365 mają domyślne jednostki i grupy jednostek.</span><span class="sxs-lookup"><span data-stu-id="d6003-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="d6003-108">Jeśli wiele produktów ma ten sam zestaw atrybutów, można utworzyć rodzinę produktów zawierających te wspólne atrybuty.</span><span class="sxs-lookup"><span data-stu-id="d6003-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="d6003-109">Wszystkie produkty w jednej rodzinie produktów dziedziczą ten sam zestaw atrybutów.</span><span class="sxs-lookup"><span data-stu-id="d6003-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="d6003-110">Na przykład firma sprzedaje licencje subskrypcyjne na różne oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="d6003-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="d6003-111">Każdy subskrybowany program ma dwa następujące atrybuty:</span><span class="sxs-lookup"><span data-stu-id="d6003-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="d6003-112">Liczba użytkowników</span><span class="sxs-lookup"><span data-stu-id="d6003-112">Number of users</span></span> 
- <span data-ttu-id="d6003-113">Czas trwania subskrypcji (w miesiącach)</span><span class="sxs-lookup"><span data-stu-id="d6003-113">Subscription duration (in months)</span></span>

<span data-ttu-id="d6003-114">Dobrym sposobem na prowadzenie tego typu katalogu jest utworzenie rodziny produktów o nazwie **Subskrypcja oprogramowania**, która ma atrybuty **Liczba użytkowników** i **Czas trwania subskrypcji**.</span><span class="sxs-lookup"><span data-stu-id="d6003-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="d6003-115">Następnie można dodać poszczególne produkty, takie jak **Dynamics 365 Sales** lub **Dynamics 365 Field Service**, do rodziny produktów **Subskrypcja oprogramowania**.</span><span class="sxs-lookup"><span data-stu-id="d6003-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="d6003-116">Dodawanie elementów katalogu produktów do oferty projektu</span><span class="sxs-lookup"><span data-stu-id="d6003-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="d6003-117">Strony Oferta projektu i Kontrakt projektu zawierają sekcje na dwa typy wierszy: wiersze oparte na projekcie i wiersze oparte na produktach.</span><span class="sxs-lookup"><span data-stu-id="d6003-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="d6003-118">W przypadku wierszy opartych na produktach program Dynamics 365 dodaje elementy z katalogu produktów do oferty.</span><span class="sxs-lookup"><span data-stu-id="d6003-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="d6003-119">Lista rozwijana w wierszu oferty lub pozycji kontraktu projektu zawiera wszystkie produkty i jednostki z cennika produktów dołączonego do oferty lub kontraktu na projekt.</span><span class="sxs-lookup"><span data-stu-id="d6003-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="d6003-120">Można również dodawać produkty, które nie są częścią cennika produktów dołączonego do oferty.</span><span class="sxs-lookup"><span data-stu-id="d6003-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="d6003-121">Oprócz tego można wybierać produkty z innych cenników lub albo bezpośrednio z katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="d6003-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="d6003-122">W przypadku wybierania produktów bezpośrednio z katalogu produktów do ustalania ceny sprzedaży produktu jest używany domyślny cennik tego produktu.</span><span class="sxs-lookup"><span data-stu-id="d6003-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="d6003-123">Jeśli cennik domyślny nie jest określony, system ustawia cenę 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d6003-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="d6003-124">Jeśli wiersz oferty jest oparty na katalogu produktów, można zastąpić cenę sprzedaży bezpośrednio w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="d6003-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="d6003-125">Należy zwrócić uwagę, że wiersz oferty w programie Dynamics 365 ma pole **Kalkulacja cen**.</span><span class="sxs-lookup"><span data-stu-id="d6003-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="d6003-126">Może ono przybierać dwie wartości:</span><span class="sxs-lookup"><span data-stu-id="d6003-126">Two values are available:</span></span>

- <span data-ttu-id="d6003-127">Zastąp kalkulację ceny</span><span class="sxs-lookup"><span data-stu-id="d6003-127">Override pricing</span></span>  
- <span data-ttu-id="d6003-128">Użyj domyślnego</span><span class="sxs-lookup"><span data-stu-id="d6003-128">Use default</span></span>

<span data-ttu-id="d6003-129">Jeśli w tym polu zostanie ustawiona wartość **Zastąp kalkulację ceny**, w usłudze Dynamics 365 nie jest ustawiana cena domyślna.</span><span class="sxs-lookup"><span data-stu-id="d6003-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="d6003-130">Należy wprowadzić cenę produktu w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="d6003-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="d6003-131">Jeśli w tym polu zostanie ustawiona wartość **Użyj domyślnego**, w usłudze Dynamics 365 zostanie użyta domyślna cena sprzedaży, a pole zostanie zablokowane, aby zapobiec edytowaniu.</span><span class="sxs-lookup"><span data-stu-id="d6003-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="d6003-132">Po zainstalowaniu rozwiązania PSA domyślne ceny sprzedaży są wprowadzana w wierszach opartych na produktach w ofercie.</span><span class="sxs-lookup"><span data-stu-id="d6003-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="d6003-133">Następnie w polu **Kalkulacja cen** jest ustawiana wartość **Zastąp kalkulację ceny**, tak aby można było edytować domyślną cenę w wierszach oferty.</span><span class="sxs-lookup"><span data-stu-id="d6003-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Konfigurowanie zastępowania kalkulacji ceny](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="d6003-135">Współczynniki ilościowe dla produktów</span><span class="sxs-lookup"><span data-stu-id="d6003-135">Quantity factors for products</span></span>

<span data-ttu-id="d6003-136">Do obsługi sprzedaży produktów opartych na subskrypcji program PSA używa współczynników ilościowych.</span><span class="sxs-lookup"><span data-stu-id="d6003-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="d6003-137">W przypadku produktów opartych na subskrypcji liczba w ofercie lub pozycji kontraktu projektu jest wyrażona liczbą użytkowników w miesiącu.</span><span class="sxs-lookup"><span data-stu-id="d6003-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="d6003-138">Zazwyczaj cena subskrybowanego oprogramowania jest przechowywana w katalogu jako cena za jednego użytkownika za jeden miesiąc.</span><span class="sxs-lookup"><span data-stu-id="d6003-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="d6003-139">Można jednak używać również innych opisów czasu.</span><span class="sxs-lookup"><span data-stu-id="d6003-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="d6003-140">W trakcie procesu sprzedaży cena w wierszu oferty to zazwyczaj cena na użytkownika na miesiąc, która została wynegocjowana i uzupełniona o rabat przez przedstawiciela handlowego z działu IT.</span><span class="sxs-lookup"><span data-stu-id="d6003-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="d6003-141">Każda transakcja ma inną liczbę użytkowników i inną liczbę miesięcy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d6003-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="d6003-142">Ilość użyta do obliczenia kwoty w wierszu oferty jest iloczynem liczby użytkowników i liczby miesięcy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d6003-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="d6003-143">W celu zapewnienia obsługi tego typu sprzedaży w rozwiązaniu PSA wprowadzono koncepcję współczynników ilościowych.</span><span class="sxs-lookup"><span data-stu-id="d6003-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="d6003-144">Współczynniki ilościowe opierają się na atrybutach produktów w systemie Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d6003-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="d6003-145">Podczas konfigurowania konkretnych właściwości produktu program PSA umożliwia oflagowanie podzbioru tych właściwości albo wszystkich właściwości jako współczynników ilościowych.</span><span class="sxs-lookup"><span data-stu-id="d6003-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="d6003-146">System PSA weryfikuje, czy tylko właściwości liczbowe lub właściwości produktu mające liczbowy typ danych są flagowane jako współczynniki ilościowe.</span><span class="sxs-lookup"><span data-stu-id="d6003-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="d6003-147">Gdy produkt, dla którego są konfigurowane współczynniki ilościowe, zostanie dodany do wiersza produktu, pole **Ilość** w wierszu oferty staje się polem tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="d6003-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="d6003-148">Po wprowadzeniu wartości właściwości produktu będących współczynnikami ilościowymi rozwiązanie PSA obliczy ilość w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="d6003-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="d6003-149">Na przykład system Dynamics 365 może mieć następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="d6003-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="d6003-150">**Liczba użytkowników** — liczba użytkowników</span><span class="sxs-lookup"><span data-stu-id="d6003-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="d6003-151">**Liczba miesięcy** — liczba miesięcy subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d6003-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="d6003-152">**Kod SKU produktu**</span><span class="sxs-lookup"><span data-stu-id="d6003-152">**Product SKU**</span></span> 

<span data-ttu-id="d6003-153">Właściwości **Liczba użytkowników** i **Liczba miesięcy** można oflagować jako współczynniki ilościowe, odpowiednio modyfikując właściwości wiersza produktu.</span><span class="sxs-lookup"><span data-stu-id="d6003-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Flagowanie atrybutów Liczba użytkowników i Liczba miesięcy jako współczynników ilościowych](media/basic-guide-11.png)
 
