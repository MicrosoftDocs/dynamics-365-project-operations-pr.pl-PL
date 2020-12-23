---
title: Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen
description: W tym temat przedstawiono informacje na temat tworzenia niestandardowych zestawów opcji lub encji.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642826"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="77207-103">Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="77207-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="77207-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="77207-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="77207-105">Poniższe kroki można wykonać, gdy zechcesz utworzyć niestandardowy zestaw opcji lub encję do użycia jako wymiaru kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="77207-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="77207-106">Aby uzyskać więcej informacji, zobacz [Omówienie wymiarów kalkulacji cen](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="77207-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="77207-107">Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="77207-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="77207-108">Ta ważna najlepsza praktyka zapewni w przyszłości elastyczność aktualizowania lub usuwania wybranych zmian.</span><span class="sxs-lookup"><span data-stu-id="77207-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="77207-109">Ułatwi ona również ponowne użycie pracy oraz przenoszenie tych zmian do innego wystąpienia. Po wprowadzeniu wszystkich wymaganych zmian wyeksportuj to rozwiązanie jako **rozwiązanie zarządzane** i zaimportuj je do innych wystąpień, aby ponownie użyć ustawień kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="77207-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="77207-110">Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="77207-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="77207-111">Wymiarem kalkulacji cen może być zestaw opcji lub encja.</span><span class="sxs-lookup"><span data-stu-id="77207-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="77207-112">Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen.</span><span class="sxs-lookup"><span data-stu-id="77207-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="77207-113">Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="77207-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="77207-114">Wymiary oparte na encjach</span><span class="sxs-lookup"><span data-stu-id="77207-114">Entity-based dimensions</span></span>
<span data-ttu-id="77207-115">Aby utworzyć wymiary oparte na encjach, należy wykonać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="77207-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="77207-116">Przejdź kolejno do: **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="77207-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="77207-117">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.</span><span class="sxs-lookup"><span data-stu-id="77207-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="77207-118">Wybierz **Nowy**, aby utworzyć nową encję o nazwie **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="77207-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="77207-119">Wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="77207-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definicja encji Standardowe stanowisko](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="77207-121">Wymiary oparte na zestawach opcji</span><span class="sxs-lookup"><span data-stu-id="77207-121">Option set-based dimensions</span></span> 
<span data-ttu-id="77207-122">Można utworzyć dwa wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="77207-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="77207-123">Użyj **lokalizacji pracy zasobu** do śledzenia ceny pracy w lokalizacji **Główna** i **Na miejscu**.</span><span class="sxs-lookup"><span data-stu-id="77207-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="77207-124">Użyj **godzin pracy zasobu** z wartościami **Regularne** i **Nadgodziny**, aby zastosować narzut po zakończeniu pracy.</span><span class="sxs-lookup"><span data-stu-id="77207-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="77207-125">Poniższa ilustracja zawiera widok wymiaru **Lokalizacja pracy zasobu**.</span><span class="sxs-lookup"><span data-stu-id="77207-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Lokalizacja pracy zasobu](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="77207-127">Poniższa ilustracja zawiera widok wymiaru **Godziny pracy zasobu**.</span><span class="sxs-lookup"><span data-stu-id="77207-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Godziny pracy zasobu](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="77207-129">Przejdź kolejno do: **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="77207-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="77207-130">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Zestawy opcji**.</span><span class="sxs-lookup"><span data-stu-id="77207-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="77207-131">Wybierz **Nowy**, aby utworzyć nowy zestaw opcji, wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="77207-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="77207-132">Tworzenie danych dla wymiarów opartych na encjach</span><span class="sxs-lookup"><span data-stu-id="77207-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="77207-133">Dane wymiarów opartych na encjach można tworzyć ręcznie, poprzez import z programu Microsoft Excel lub za pomocą wywołań usług.</span><span class="sxs-lookup"><span data-stu-id="77207-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="77207-134">Czynności opisane w tej procedurze umożliwiają utworzenie dwóch standardowych stanowisk — **Inżynier systemów** i **Starszy inżynier systemów** — na podstawie wymiaru opartego na encji noszącego nazwę **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="77207-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="77207-135">Jeśli ilość danych, które mają zostać utworzone, jest niewielka, jak w poniższym przykładzie, można użyć standardowego formularza.</span><span class="sxs-lookup"><span data-stu-id="77207-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="77207-136">Wybierz pozycję **Szukanie zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="77207-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="77207-137">Wybierz encję **Standardowe stanowisko** i wybierz pozycję **Wyniki**.</span><span class="sxs-lookup"><span data-stu-id="77207-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="77207-138">Zostaną wyświetlone wszystkie wiersze encji **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="77207-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="77207-139">Wybierz **Nowe**, w polu **Nazwa** wpisz treść „Inżynier systemów”, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="77207-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="77207-140">Zamyknij stronę.</span><span class="sxs-lookup"><span data-stu-id="77207-140">Close the page.</span></span> 
5. <span data-ttu-id="77207-141">Powtórz kroki 1–3, aby utworzyć kolejne nowe stanowisko „Starszy inżynier systemów”.</span><span class="sxs-lookup"><span data-stu-id="77207-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Przykładowe dane encji Standardowe stanowisko](media/ST-data.png)
