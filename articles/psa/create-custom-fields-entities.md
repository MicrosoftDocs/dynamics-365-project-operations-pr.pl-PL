---
title: Tworzenie niestandardowych pól i encji
description: W tym temacie przedstawiono sposób tworzenia zestawów opcji i encji we własnym rozwiązaniu na platformie Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082081"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="c956c-103">Tworzenie niestandardowych pól i encji</span><span class="sxs-lookup"><span data-stu-id="c956c-103">Create custom fields and entities</span></span> 

<span data-ttu-id="c956c-104">Poniższe kroki można wykonać w dowolnym momencie, kiedy zechcesz utworzyć niestandardowy zestaw opcji lub encję na platformie Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c956c-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="c956c-105">Procedury w tym temacie należy wykonać przy użyciu interfejsu internetowego usługi Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="c956c-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c956c-106">Zalecamy, aby wszelkie niestandardowe modyfikacje wymiarów kalkulacji cen wykonywać w osobnym rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="c956c-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c956c-107">Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="c956c-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c956c-108">Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane** , a następnie je zaimportować do innych wystąpień i tam wykorzystywać.</span><span class="sxs-lookup"><span data-stu-id="c956c-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c956c-109">Tworzenie niestandardowych pól i zestawów opcji w rozwiązaniu do zarządzania wymiarami kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="c956c-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c956c-110">Wymiarem kalkulacji cen może być zestaw opcji lub encja.</span><span class="sxs-lookup"><span data-stu-id="c956c-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c956c-111">Oba rodzaje wymiarów muszą być utworzone w rozwiązaniu do zarządzania kalkulacjami cen.</span><span class="sxs-lookup"><span data-stu-id="c956c-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c956c-112">Etapy tej procedury pokazują, jak tworzyć wymiary oparte na encjach i wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="c956c-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c956c-113">Wymiary oparte na encjach</span><span class="sxs-lookup"><span data-stu-id="c956c-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="c956c-114">W programie PSA kliknij opcję **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="c956c-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c956c-115">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje**.</span><span class="sxs-lookup"><span data-stu-id="c956c-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c956c-116">Kliknij przycisk **Nowy** , aby utworzyć nową encję o nazwie **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="c956c-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="c956c-117">Wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c956c-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicja encji Standardowe stanowisko](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c956c-119">Wymiary oparte na zestawach opcji</span><span class="sxs-lookup"><span data-stu-id="c956c-119">Option set-based dimensions</span></span> 
<span data-ttu-id="c956c-120">Można utworzyć dwa wymiary oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="c956c-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c956c-121">Wymiar **Lokalizacja pracy zasobu** umożliwia śledzenie pracy w lokalizacjach **Główna** i **Na miejscu** , a wymiar **Godziny pracy zasobu** z wartościami **Regularny** i **Nadgodziny** pozwala stosować narzut po zakończeniu pracy.</span><span class="sxs-lookup"><span data-stu-id="c956c-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c956c-122">W programie PSA kliknij opcję **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="c956c-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c956c-123">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Zestawy opcji**.</span><span class="sxs-lookup"><span data-stu-id="c956c-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c956c-124">Kliknij przycisk **Nowy** , aby utworzyć nowy zestaw opcji, wprowadź pozostałe wymagane informacje, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c956c-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="c956c-125">Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Lokalizacja pracy zasobu</span><span class="sxs-lookup"><span data-stu-id="c956c-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="c956c-126">Wymiar kalkulacji cen oparty na zestawie opcji zatytułowany Godziny pracy zasobu</span><span class="sxs-lookup"><span data-stu-id="c956c-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c956c-127">Tworzenie danych dla wymiarów opartych na encjach</span><span class="sxs-lookup"><span data-stu-id="c956c-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c956c-128">Dane wymiarów opartych na encjach można tworzyć ręcznie, poprzez import z programu Microsoft Excel lub za pomocą wywołań usług.</span><span class="sxs-lookup"><span data-stu-id="c956c-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c956c-129">Czynności opisane w tej procedurze umożliwiają utworzenie dwóch standardowych stanowisk — **Inżynier systemów** i **Starszy inżynier systemów** — na podstawie wymiaru opartego na encji noszącego nazwę **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="c956c-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c956c-130">Jeśli ilość danych, które mają zostać utworzone, jest niewielka, jak w poniższym przykładzie, można użyć standardowego formularza.</span><span class="sxs-lookup"><span data-stu-id="c956c-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c956c-131">W programie PSA kliknij opcję **Szukanie zaawansowane**.</span><span class="sxs-lookup"><span data-stu-id="c956c-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="c956c-132">Zaznacz encję **Standardowe stanowisko** i kliknij przycisk **Wyniki**.</span><span class="sxs-lookup"><span data-stu-id="c956c-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="c956c-133">Zostaną wyświetlone wszystkie wiersze encji **Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="c956c-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c956c-134">Kliknij pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="c956c-134">Click **New**.</span></span> <span data-ttu-id="c956c-135">W polu **Nazwa** wpisz treść „Inżynier systemów”, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c956c-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="c956c-136">Zamknij formularz.</span><span class="sxs-lookup"><span data-stu-id="c956c-136">Close the form.</span></span> 
4. <span data-ttu-id="c956c-137">Powtórz kroki 1–3, aby utworzyć kolejne nowe stanowisko „Starszy inżynier systemów”.</span><span class="sxs-lookup"><span data-stu-id="c956c-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="c956c-138">Przykładowe dane encji Standardowe stanowisko</span><span class="sxs-lookup"><span data-stu-id="c956c-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


