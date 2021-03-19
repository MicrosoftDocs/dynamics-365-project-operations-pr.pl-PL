---
title: Zarządzanie jednostkami złożonymi, takimi jak na użytkownika, na miesiąc dla wierszy oferty opartej na produktach - wersja uproszczona
description: Ten temat zawiera informacje o zarządzaniu jednostkami złożonymi w wierszu oferty opartej na produktach.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272896"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="e50ee-103">Zarządzanie jednostkami złożonymi, takimi jak na użytkownika, na miesiąc dla wierszy oferty opartej na produktach - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="e50ee-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="e50ee-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="e50ee-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e50ee-105">Do obsługi sprzedaży produktów opartych na subskrypcji program Dynamics 365 Project Operations używa współczynników ilościowych.</span><span class="sxs-lookup"><span data-stu-id="e50ee-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="e50ee-106">W przypadku produktów opartych na subskrypcji liczba w ofercie lub pozycji kontraktu projektu jest wyrażona liczbą użytkowników w miesiącu.</span><span class="sxs-lookup"><span data-stu-id="e50ee-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="e50ee-107">Zazwyczaj cena subskrybowanego oprogramowania jest przechowywana w katalogu jako cena za jednego użytkownika za jeden miesiąc.</span><span class="sxs-lookup"><span data-stu-id="e50ee-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="e50ee-108">W trakcie procesu sprzedaży cena w wierszu oferty to zazwyczaj cena na użytkownika na miesiąc, która została wynegocjowana i uzupełniona o rabat przez przedstawiciela handlowego z działu IT.</span><span class="sxs-lookup"><span data-stu-id="e50ee-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="e50ee-109">Każda transakcja ma inną liczbę użytkowników i inną liczbę miesięcy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e50ee-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="e50ee-110">Ilość użyta do obliczenia kwoty w wierszu oferty jest iloczynem liczby użytkowników i liczby miesięcy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e50ee-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="e50ee-111">W celu zapewnienia obsługi tego typu sprzedaży w rozwiązaniu Project Operations wprowadzono koncepcję współczynników ilościowych.</span><span class="sxs-lookup"><span data-stu-id="e50ee-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="e50ee-112">Współczynniki ilościowe opierają się na atrybutach produktów w systemie Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e50ee-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="e50ee-113">Podczas konfigurowania konkretnych właściwości produktu program Project Operations umożliwia oflagowanie podzbioru tych właściwości albo wszystkich właściwości jako współczynników ilościowych.</span><span class="sxs-lookup"><span data-stu-id="e50ee-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="e50ee-114">Project Operations weryfikuje, czy tylko właściwości liczbowe lub właściwości produktu mające liczbowy typ danych są flagowane jako współczynniki ilościowe.</span><span class="sxs-lookup"><span data-stu-id="e50ee-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="e50ee-115">W przypadku dodawania do wiersza oferty towaru z współczynnikami ilościowymi, pole **Ilość** staje się polem tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="e50ee-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="e50ee-116">Po wprowadzeniu wartości właściwości produktu będących współczynnikami ilościowymi Project Operations obliczy ilość w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="e50ee-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="e50ee-117">Na przykład system Dynamics 365 Sales może mieć następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="e50ee-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="e50ee-118">**Liczba użytkowników**: liczba użytkowników</span><span class="sxs-lookup"><span data-stu-id="e50ee-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="e50ee-119">**Liczba miesięcy**: liczba miesięcy subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e50ee-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="e50ee-120">**Kod SKU produktu**</span><span class="sxs-lookup"><span data-stu-id="e50ee-120">**Product SKU**</span></span>

<span data-ttu-id="e50ee-121">Właściwości **Liczba użytkowników** i **Liczba miesięcy** można oflagować jako współczynniki ilościowe, odpowiednio modyfikując właściwości wiersza produktu.</span><span class="sxs-lookup"><span data-stu-id="e50ee-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="e50ee-122">Aby utworzyć współczynnik ilościowy na podstawie właściwości produktu, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="e50ee-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="e50ee-123">W lewym panelu nawigacyjnym Project Operations przejdź do **Sprzedaż** > **Produkty**.</span><span class="sxs-lookup"><span data-stu-id="e50ee-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="e50ee-124">Otwórz produkt, dla którego chcesz skonfigurować czynniki ilościowe.</span><span class="sxs-lookup"><span data-stu-id="e50ee-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="e50ee-125">Upewnij się, że właściwości produktu zostały już skonfigurowane.</span><span class="sxs-lookup"><span data-stu-id="e50ee-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="e50ee-126">Na stronie **Informacje o projekcie** danego produktu wybierz kartę **Czynniki ilościowe**.</span><span class="sxs-lookup"><span data-stu-id="e50ee-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="e50ee-127">W podsiatce wybierz **+ Nowe obliczanie pola**.</span><span class="sxs-lookup"><span data-stu-id="e50ee-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="e50ee-128">Wprowadź nazwę współczynnika ilościowego i wybierz wartość właściwości, która ma być mapowana na obliczenia pola.</span><span class="sxs-lookup"><span data-stu-id="e50ee-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="e50ee-129">Zapisz i zamknij formularz.</span><span class="sxs-lookup"><span data-stu-id="e50ee-129">Save and close the form.</span></span> <span data-ttu-id="e50ee-130">Powtórz te kroki dla wszystkich właściwości, które mają być używane do obliczania ilości wiersza oferty opartej na produkcie.</span><span class="sxs-lookup"><span data-stu-id="e50ee-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="e50ee-131">W przypadku utworzenia wiersza oferty opartej na produkcie dla danego produktu, ilość w wierszu oferty zostanie zablokowana.</span><span class="sxs-lookup"><span data-stu-id="e50ee-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="e50ee-132">Ilość będzie obliczana jako iloczyn wartości właściwości wprowadzonych w danym wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="e50ee-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]