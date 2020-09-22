---
title: Tworzenie niestandardowych pól i encji
description: W tym temacie przedstawiono sposób tworzenia zestawów opcji i encji we własnym rozwiązaniu na platformie Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754391"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="8a864-103">Tworzenie niestandardowych pól i encji</span><span class="sxs-lookup"><span data-stu-id="8a864-103">Create custom fields and entities</span></span> 

<span data-ttu-id="8a864-104">Poniższe kroki można wykonać w dowolnym momencie, kiedy zechcesz utworzyć niestandardowy zestaw opcji lub encję na platformie Power Apps.</span><span class="sxs-lookup"><span data-stu-id="8a864-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="8a864-105">Procedury w tym temacie należy wykonać przy użyciu interfejsu internetowego usługi Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="8a864-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a864-106">Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="8a864-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8a864-107">Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="8a864-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="8a864-108">Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane**, a następnie je zaimportować do innych wystąpień i tam wykorzystywać.</span><span class="sxs-lookup"><span data-stu-id="8a864-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="8a864-109">Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="8a864-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="8a864-110">W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij przycisk **Nowy**, aby utworzyć nowe rozwiązanie.</span><span class="sxs-lookup"><span data-stu-id="8a864-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="8a864-111">Nazwij rozwiązanie **\<nazwa Twojej organizacji> — wymiary kalkulacji cen**, wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="8a864-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8a864-113">Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="8a864-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8a864-114">Wymiarem kalkulacji cen może być zestaw opcji lub encja.</span><span class="sxs-lookup"><span data-stu-id="8a864-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8a864-115">Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen.</span><span class="sxs-lookup"><span data-stu-id="8a864-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8a864-116">Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="8a864-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8a864-117">Wymiary oparte na encjach</span><span class="sxs-lookup"><span data-stu-id="8a864-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="8a864-118">W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **\<nazwa Twojej organizacji> — wymiary finansowe**.</span><span class="sxs-lookup"><span data-stu-id="8a864-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8a864-119">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.</span><span class="sxs-lookup"><span data-stu-id="8a864-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8a864-120">Kliknij przycisk **Nowy**, aby utworzyć nową encję o nazwie **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="8a864-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="8a864-121">Wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="8a864-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicja encji Standardowe stanowisko](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="8a864-123">Wymiary oparte na zestawach opcji</span><span class="sxs-lookup"><span data-stu-id="8a864-123">Option set-based dimensions</span></span> 
<span data-ttu-id="8a864-124">Można utworzyć dwa wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="8a864-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="8a864-125">Wymiar **Lokalizacja pracy zasobu** umożliwia śledzenie pracy w lokalizacjach **Główna** i **Na miejscu**, a wymiar **Godziny pracy zasobu** z wartościami **Regularny** i **Nadgodziny** pozwala stosować narzut po zakończeniu pracy.</span><span class="sxs-lookup"><span data-stu-id="8a864-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="8a864-126">W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **\<nazwa Twojej organizacji> — wymiary kalkulacji cen**.</span><span class="sxs-lookup"><span data-stu-id="8a864-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8a864-127">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Zestawy opcji**.</span><span class="sxs-lookup"><span data-stu-id="8a864-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8a864-128">Kliknij przycisk **Nowy**, aby utworzyć nowy zestaw opcji, wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="8a864-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="8a864-129">Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Lokalizacja pracy zasobu</span><span class="sxs-lookup"><span data-stu-id="8a864-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="8a864-130">Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Godziny pracy zasobu</span><span class="sxs-lookup"><span data-stu-id="8a864-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8a864-131">Tworzenie danych dla wymiarów opartych na encjach</span><span class="sxs-lookup"><span data-stu-id="8a864-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8a864-132">Dane wymiarów opartych na encjach można tworzyć ręcznie, poprzez import z programu Microsoft Excel lub za pomocą wywołań usług.</span><span class="sxs-lookup"><span data-stu-id="8a864-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8a864-133">Czynności opisane w tej procedurze umożliwiają utworzenie dwóch standardowych stanowisk — **Inżynier systemów** i **Starszy inżynier systemów** — na podstawie wymiaru opartego na encji noszącego nazwę **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="8a864-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8a864-134">Jeśli ilość danych, które mają zostać utworzone, jest niewielka, jak w poniższym przykładzie, można użyć standardowego formularza.</span><span class="sxs-lookup"><span data-stu-id="8a864-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8a864-135">W programie PSA kliknij opcję **Szukanie zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="8a864-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="8a864-136">Zaznacz encję **Standardowe stanowisko** i kliknij przycisk **Wyniki**.</span><span class="sxs-lookup"><span data-stu-id="8a864-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="8a864-137">Zostaną wyświetlone wszystkie wiersze encji **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="8a864-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="8a864-138">Kliknij pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="8a864-138">Click **New**.</span></span> <span data-ttu-id="8a864-139">W polu **Nazwa** wpisz treść „Inżynier systemów”, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="8a864-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="8a864-140">Zamknij formularz.</span><span class="sxs-lookup"><span data-stu-id="8a864-140">Close the form.</span></span> 
4. <span data-ttu-id="8a864-141">Powtórz kroki 1–3, aby utworzyć kolejne nowe stanowisko „Starszy inżynier systemów”.</span><span class="sxs-lookup"><span data-stu-id="8a864-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="8a864-142">Przykładowe dane encji Standardowe stanowisko</span><span class="sxs-lookup"><span data-stu-id="8a864-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="8a864-143">Dodawanie wszystkich wymaganych encji i pokrewnych składników programu PSA do rozwiązania do zarządzania wymiarami kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="8a864-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="8a864-144">Następujące encje usługi Project Service trzeba będzie dodać do rozwiązania do zarządzania wymiarami kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="8a864-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="8a864-145">Czynności opisane w tej procedurze umożliwiają wprowadzenie pewnych istotnych zmian w schemacie rozwiązania do zarządzania kalkulacjami cen, tak aby encje dowiedziały się o nowych wymiarach kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="8a864-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="8a864-146">W programie PSA kliknij kolejno opcje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **\<nazwa Twojej organizacji> — wymiary finansowe**.</span><span class="sxs-lookup"><span data-stu-id="8a864-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8a864-147">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij kolejno opcje **Dodaj istniejący** > **Encje**.</span><span class="sxs-lookup"><span data-stu-id="8a864-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="8a864-148">W oknie dialogowym **Składniki rozwiązania** zaznacz następujące encje:</span><span class="sxs-lookup"><span data-stu-id="8a864-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="8a864-149">Wartość rzeczywista</span><span class="sxs-lookup"><span data-stu-id="8a864-149">Actual</span></span>
- <span data-ttu-id="8a864-150">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="8a864-150">Bookable Resource</span></span>
- <span data-ttu-id="8a864-151">Wiersz szacowania</span><span class="sxs-lookup"><span data-stu-id="8a864-151">Estimate Line</span></span>
- <span data-ttu-id="8a864-152">Szczegóły wiersza faktury</span><span class="sxs-lookup"><span data-stu-id="8a864-152">Invoice Line Detail</span></span>
- <span data-ttu-id="8a864-153">Wiersz arkusza</span><span class="sxs-lookup"><span data-stu-id="8a864-153">Journal Line</span></span>
- <span data-ttu-id="8a864-154">Szczegóły pozycji kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="8a864-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="8a864-155">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="8a864-155">Project Team Member</span></span>
- <span data-ttu-id="8a864-156">Szczegóły wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="8a864-156">Quote Line Detail</span></span>
- <span data-ttu-id="8a864-157">Narzut na cenę dla roli</span><span class="sxs-lookup"><span data-stu-id="8a864-157">Role Price Markup</span></span>
- <span data-ttu-id="8a864-158">Cena roli</span><span class="sxs-lookup"><span data-stu-id="8a864-158">Role Price</span></span> 
- <span data-ttu-id="8a864-159">Wpis czasu</span><span class="sxs-lookup"><span data-stu-id="8a864-159">Time Entry</span></span> 

> ![Dodawanie istniejących encji do rozwiązania do zarządzania wymiarami kalkulacji cen](media/Existing-entities-to-PD-solution.png)

> ![Wybieranie składników rozwiązania](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="8a864-162">Upewnić się, dla każdej wybranej encji dołączono wszystkie formularze i widoki.</span><span class="sxs-lookup"><span data-stu-id="8a864-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="8a864-163">Gdy zobaczysz monit o dodanie wszelkich encji zależnych od encji zaznaczonych powyżej, kliknij opcję **Nie**.</span><span class="sxs-lookup"><span data-stu-id="8a864-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Opcja niedołączania pokrewnych składników](media/Do-not-include-required.png)


