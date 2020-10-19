---
title: Tworzenie ofert projektu na podstawie szans sprzedaży
description: Ta temat zawiera informacje na temat tworzenia ofert z poziomu szans sprzedaży.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898545"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="e7569-103">Tworzenie ofert projektu na podstawie szans sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e7569-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="e7569-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="e7569-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e7569-105">Oferty mogą być tworzone na podstawie szans sprzedaży projektów w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="e7569-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="e7569-106">Z poziomu karty **Oferty** na stronie **Szansa sprzedaży**</span><span class="sxs-lookup"><span data-stu-id="e7569-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="e7569-107">Z poziomu procesu przepływu szansy sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e7569-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="e7569-108">Aktualizując odwołanie do szansy sprzedaży na istniejącej ofercie</span><span class="sxs-lookup"><span data-stu-id="e7569-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="e7569-109">Z poziomu karty Oferty na stronie Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e7569-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="e7569-110">Aby utworzyć ofertę projektu z szansy sprzedaży, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="e7569-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="e7569-111">Otworzyć stronę **Szansa sprzedaży** na karcie **Oferty**.</span><span class="sxs-lookup"><span data-stu-id="e7569-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="e7569-112">W podsiatce **Oferty** wybrać opcję **+** w celu utworzenia nowej oferty projektu na podstawie szansy sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e7569-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="e7569-113">Wszystkie wiersze szans sprzedaży i powiązane z nimi cenniki projektu są kopiowane do nowej oferty z szansy sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e7569-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="e7569-114">Z poziomu procesu przepływu szansy sprzedaży</span><span class="sxs-lookup"><span data-stu-id="e7569-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="e7569-115">Aby utworzyć ofertę projektu z procesu przepływu szansy sprzedaży, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="e7569-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="e7569-116">Otwórz szansę sprzedaży z poziomu przepływu procesu.</span><span class="sxs-lookup"><span data-stu-id="e7569-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="e7569-117">Wybierz etap **Kwalifikacja**.</span><span class="sxs-lookup"><span data-stu-id="e7569-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="e7569-118">Wybierz opcję **Dalej**, a następnie wybierz pozycję **+ Utwórz**, aby utworzyć nową ofertę.</span><span class="sxs-lookup"><span data-stu-id="e7569-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="e7569-119">Większość informacji znajdujących się na karcie **Podsumowanie** tej nowej oferty będzie domyślnie wybierana na podstawie szansy sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e7569-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="e7569-120">Wprowadź wymagane brakujące informacje lub zaktualizuj wartości domyślne zgodnie z wymaganiami na **karcie Podsumowanie**.</span><span class="sxs-lookup"><span data-stu-id="e7569-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="e7569-121">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="e7569-121">Select **Save**.</span></span> <span data-ttu-id="e7569-122">Nowa oferta zostanie utworzona i skojarzona z szansą sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e7569-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="e7569-123">Można teraz wyświetlić informacje o ofercie na karcie **Oferty** na stronie **Szansa sprzedaży**.</span><span class="sxs-lookup"><span data-stu-id="e7569-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="e7569-124">Proces sprzedaży dla szansy sprzedaży zostanie przesunięty do kolejnego etapu i **Zaproponowany**.</span><span class="sxs-lookup"><span data-stu-id="e7569-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="e7569-125">Aktualizując odwołanie do szansy sprzedaży na istniejącej ofercie</span><span class="sxs-lookup"><span data-stu-id="e7569-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="e7569-126">Istniejącą ofertę można połączyć z szansą sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e7569-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="e7569-127">Wykonaj poniższe kroki, aby zaktualizować informacje o szansie sprzedaży dla istniejącej oferty.</span><span class="sxs-lookup"><span data-stu-id="e7569-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="e7569-128">Otwórz stronę **Oferta** na karcie **Podsumowanie**.</span><span class="sxs-lookup"><span data-stu-id="e7569-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="e7569-129">W polu **Szansa sprzedaży** wybierz szansę sprzedaży, która ma zostać połączona z ofertą.</span><span class="sxs-lookup"><span data-stu-id="e7569-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="e7569-130">Oferta jest widoczna w siatce **Ofert** w szansie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e7569-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="e7569-131">Korzystając z procesu sprzedaży szansy sprzedaży, szansa sprzedaży może zostać przeniesiona do kolejnego etapu i **Zaproponowana**.</span><span class="sxs-lookup"><span data-stu-id="e7569-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="e7569-132">Po przeniesieniu szansy sprzedaży do danego etapu można wybrać tę ofertę z listy ofert skojarzonych z daną szansą sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e7569-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="e7569-133">Zaznaczenie tej oferty oznacza, że jest ona wybrana do dalszego przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="e7569-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="e7569-134">Wszystkie pozostałe oferty skojarzone z szansą sprzedaży będą nadal dostępne i aktywne do chwili wygrania jednej z nich.</span><span class="sxs-lookup"><span data-stu-id="e7569-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="e7569-135">Użytkownik może przenieść proces sprzedaży z powrotem na poprzedni etap **Kwalifikowanie** i wybrać inną ofertę.</span><span class="sxs-lookup"><span data-stu-id="e7569-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
