---
title: Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen
description: W tym temat przedstawiono informacje na temat tworzenia niestandardowych zestawów opcji lub encji.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898274"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="05963-103">Tworzenie pól niestandardowych i encji jako wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="05963-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="05963-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="05963-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="05963-105">Poniższe kroki można wykonać w dowolnym momencie, kiedy zechcesz utworzyć niestandardowy zestaw opcji lub encję.</span><span class="sxs-lookup"><span data-stu-id="05963-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05963-106">Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="05963-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="05963-107">Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="05963-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="05963-108">Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane**, a następnie je zaimportować do innych wystąpień i tam wykorzystywać.</span><span class="sxs-lookup"><span data-stu-id="05963-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="05963-109">Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="05963-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="05963-110">Wybierz kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie wybierz **Nowy**, aby utworzyć nowe rozwiązanie.</span><span class="sxs-lookup"><span data-stu-id="05963-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="05963-111">Nazwij rozwiązanie **\<your organization name>nazwa Twojej organizacji> — wymiary kalkulacji cen**, wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="05963-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="05963-112">Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="05963-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="05963-113">Wymiarem kalkulacji cen może być zestaw opcji lub encja.</span><span class="sxs-lookup"><span data-stu-id="05963-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="05963-114">Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen.</span><span class="sxs-lookup"><span data-stu-id="05963-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="05963-115">Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="05963-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="05963-116">Wymiary oparte na encjach</span><span class="sxs-lookup"><span data-stu-id="05963-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="05963-117">Przejdź kolejno do: **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="05963-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="05963-118">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.</span><span class="sxs-lookup"><span data-stu-id="05963-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="05963-119">Wybierz **Nowy**, aby utworzyć nową encję o nazwie **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="05963-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="05963-120">Wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="05963-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="05963-121">Wymiary oparte na zestawach opcji</span><span class="sxs-lookup"><span data-stu-id="05963-121">Option set-based dimensions</span></span> 
<span data-ttu-id="05963-122">Można utworzyć dwa wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="05963-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="05963-123">Wymiar **Lokalizacja pracy zasobu** umożliwia śledzenie pracy w lokalizacjach **Główna** i **Na miejscu**, a wymiar **Godziny pracy zasobu** z wartościami **Regularny** i **Nadgodziny** pozwala stosować narzut po zakończeniu pracy.</span><span class="sxs-lookup"><span data-stu-id="05963-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="05963-124">Przejdź kolejno do: **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="05963-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="05963-125">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Zestawy opcji**.</span><span class="sxs-lookup"><span data-stu-id="05963-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="05963-126">Wybierz **Nowy**, aby utworzyć nowy zestaw opcji, wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="05963-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="05963-127">Tworzenie danych dla wymiarów opartych na encjach</span><span class="sxs-lookup"><span data-stu-id="05963-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="05963-128">Dane wymiarów opartych na encjach można tworzyć ręcznie, poprzez import z programu Microsoft Excel lub za pomocą wywołań usług.</span><span class="sxs-lookup"><span data-stu-id="05963-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="05963-129">Czynności opisane w tej procedurze umożliwiają utworzenie dwóch standardowych stanowisk — **Inżynier systemów** i **Starszy inżynier systemów** — na podstawie wymiaru opartego na encji noszącego nazwę **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="05963-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="05963-130">Jeśli ilość danych, które mają zostać utworzone, jest niewielka, jak w poniższym przykładzie, można użyć standardowego formularza.</span><span class="sxs-lookup"><span data-stu-id="05963-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="05963-131">Wybierz pozycję **Szukanie zaawansowane**, wybierz **Tytuł standardowy** encji, a następnie wybierz pozycję **Wyniki**.</span><span class="sxs-lookup"><span data-stu-id="05963-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="05963-132">Zostaną wyświetlone wszystkie wiersze encji **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="05963-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="05963-133">Wybierz **Nowe**, w polu **Nazwa** wpisz treść „Inżynier systemów”, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="05963-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="05963-134">Zamknij formularz.</span><span class="sxs-lookup"><span data-stu-id="05963-134">Close the form.</span></span> 
4. <span data-ttu-id="05963-135">Powtórz kroki 1–3, aby utworzyć kolejne nowe stanowisko „Starszy inżynier systemów”.</span><span class="sxs-lookup"><span data-stu-id="05963-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="05963-136">Dodawanie wszystkich wymaganych encji i pokrewnych składników do rozwiązania do zarządzania wymiarami kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="05963-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="05963-137">Następujące encje usługi trzeba będzie dodać do rozwiązania do zarządzania wymiarami kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="05963-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="05963-138">Czynności opisane w tej procedurze umożliwiają wprowadzenie pewnych istotnych zmian w schemacie rozwiązania do zarządzania kalkulacjami cen, tak aby encje dowiedziały się o nowych wymiarach kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="05963-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="05963-139">Wybierz **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="05963-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="05963-140">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij kolejno opcje **Dodaj istniejący** > **Encje**.</span><span class="sxs-lookup"><span data-stu-id="05963-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="05963-141">W oknie dialogowym **Składniki rozwiązania** zaznacz następujące encje:</span><span class="sxs-lookup"><span data-stu-id="05963-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="05963-142">Wartość rzeczywista</span><span class="sxs-lookup"><span data-stu-id="05963-142">Actual</span></span>
  - <span data-ttu-id="05963-143">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="05963-143">Bookable Resource</span></span>
  - <span data-ttu-id="05963-144">Wiersz szacowania</span><span class="sxs-lookup"><span data-stu-id="05963-144">Estimate Line</span></span>
  - <span data-ttu-id="05963-145">Szczegóły wiersza faktury</span><span class="sxs-lookup"><span data-stu-id="05963-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="05963-146">Wiersz arkusza</span><span class="sxs-lookup"><span data-stu-id="05963-146">Journal Line</span></span>
  - <span data-ttu-id="05963-147">Szczegóły pozycji kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="05963-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="05963-148">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="05963-148">Project Team Member</span></span>
  - <span data-ttu-id="05963-149">Szczegóły wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="05963-149">Quote Line Detail</span></span>
  - <span data-ttu-id="05963-150">Narzut na cenę dla roli</span><span class="sxs-lookup"><span data-stu-id="05963-150">Role Price Markup</span></span>
  - <span data-ttu-id="05963-151">Cena roli</span><span class="sxs-lookup"><span data-stu-id="05963-151">Role Price</span></span> 
  - <span data-ttu-id="05963-152">Wpis czasu</span><span class="sxs-lookup"><span data-stu-id="05963-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="05963-153">Upewnić się, dla każdej wybranej encji dołączono wszystkie formularze i widoki.</span><span class="sxs-lookup"><span data-stu-id="05963-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="05963-154">Gdy zobaczysz monit o dodanie wszelkich encji zależnych od encji zaznaczonych powyżej, wybierz opcję **Nie**.</span><span class="sxs-lookup"><span data-stu-id="05963-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

