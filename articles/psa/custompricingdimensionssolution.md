---
title: Tworzenie niestandardowych rozwiązań dla wymiarów kalkulacji cen
description: W tym temat wyjaśniono sposób tworzenia niestandardowego rozwiązania podczas tworzenia niestandardowych wymiarów kalkulacji cen.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082021"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="566d3-103">Tworzenie niestandardowych rozwiązań dla wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="566d3-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="566d3-104">Wszystkie zmiany wymiarów niestandardowych cen są dostępne w odrębnym rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="566d3-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="566d3-105">Ta ważna najlepsza praktyka zapewnia elastyczność umożliwiającą w przyszłości wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzone obiekty do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="566d3-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="566d3-106">Po wprowadzeniu wymaganych zmian należy wyeksportować rozwiązanie jako **Rozwiązanie zarządzane** , a następnie je zaimportować do innych wystąpień i tam wykorzystywać.</span><span class="sxs-lookup"><span data-stu-id="566d3-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="566d3-107">Wybierz przycisk **Ustawienia** > **Rozwiązania** , a następnie wybierz pozycję **Nowe**.</span><span class="sxs-lookup"><span data-stu-id="566d3-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="566d3-108">Nazwij rozwiązanie **\<your organization name>nazwa Twojej organizacji> — wymiary kalkulacji cen** , wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="566d3-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Tworzenie niestandardowego rozwiązania dla wymiarów kalkulacji cen](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="566d3-110">Dodawanie wszystkich wymaganych encji i pokrewnych składników do rozwiązania wymiarami cen</span><span class="sxs-lookup"><span data-stu-id="566d3-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="566d3-111">Następujące encje usługi Project Service trzeba będzie dodać do rozwiązania do zarządzania wymiarami kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="566d3-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="566d3-112">Czynności opisane w tej procedurze umożliwiają wprowadzenie pewnych istotnych zmian w schemacie rozwiązania do zarządzania kalkulacjami cen, tak aby encje dowiedziały się o nowych wymiarach kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="566d3-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="566d3-113">Wybierz **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="566d3-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="566d3-114">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij kolejno opcje **Dodaj istniejący** > **Encje**.</span><span class="sxs-lookup"><span data-stu-id="566d3-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="566d3-115">W oknie dialogowym **Składniki rozwiązania** zaznacz następujące encje:</span><span class="sxs-lookup"><span data-stu-id="566d3-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="566d3-116">Rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="566d3-116">Actual</span></span>
- <span data-ttu-id="566d3-117">Zasób, który można zarezerwować</span><span class="sxs-lookup"><span data-stu-id="566d3-117">Bookable Resource</span></span>
- <span data-ttu-id="566d3-118">Wiersz szacowania</span><span class="sxs-lookup"><span data-stu-id="566d3-118">Estimate Line</span></span>
- <span data-ttu-id="566d3-119">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="566d3-119">Project Task</span></span>
- <span data-ttu-id="566d3-120">Szczegóły wiersza faktury</span><span class="sxs-lookup"><span data-stu-id="566d3-120">Invoice Line Detail</span></span>
- <span data-ttu-id="566d3-121">Wiersz arkusza</span><span class="sxs-lookup"><span data-stu-id="566d3-121">Journal Line</span></span>
- <span data-ttu-id="566d3-122">Szczegóły pozycji kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="566d3-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="566d3-123">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="566d3-123">Project Team Member</span></span>
- <span data-ttu-id="566d3-124">Szczegóły wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="566d3-124">Quote Line Detail</span></span>
- <span data-ttu-id="566d3-125">Narzut na cenę dla roli</span><span class="sxs-lookup"><span data-stu-id="566d3-125">Role Price Markup</span></span>
- <span data-ttu-id="566d3-126">Cena roli</span><span class="sxs-lookup"><span data-stu-id="566d3-126">Role Price</span></span> 
- <span data-ttu-id="566d3-127">Wpis czasu</span><span class="sxs-lookup"><span data-stu-id="566d3-127">Time Entry</span></span> 

> ![Dodawanie istniejących encji do rozwiązania do zarządzania wymiarami kalkulacji cen](media/Existing-entities-to-PD-solution.png)

> ![Wybieranie składników rozwiązania](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="566d3-130">Upewnić się, dla każdej wybranej encji dołączono wszystkie formularze i widoki.</span><span class="sxs-lookup"><span data-stu-id="566d3-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="566d3-131">Gdy zobaczysz monit o dodanie wszelkich encji zależnych od zaznaczonych encji, wybierz opcję **Nie**.</span><span class="sxs-lookup"><span data-stu-id="566d3-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Opcja niedołączania pokrewnych składników](media/Do-not-include-required.png)


