---
title: Tworzenie rozwiązania dla niestandardowych wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia rozwiązań obsługujących niestandardowe wymiary kalkulacji cen.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514011"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="6f047-103">Tworzenie rozwiązania dla niestandardowych wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="6f047-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="6f047-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="6f047-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="6f047-105">Wszystkie zmiany wymiarów niestandardowych cen są dostępne w odrębnym rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="6f047-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="6f047-106">Ta ważna najlepsza praktyka umożliwia elastyczne wprowadzanie aktualizacji lub usuwanie zmian w razie potrzeby, pomaga wykorzystywać utworzoną pracę do innych celów oraz ułatwia przenoszenie zmian do innych wystąpień.</span><span class="sxs-lookup"><span data-stu-id="6f047-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="6f047-107">Po wprowadzeniu wszystkich wymaganych zmian należy wyeksportować to rozwiązanie jako rozwiązanie **zarządzane**, a następnie je zaimportować do innych wystąpień w celu ponownego używania.</span><span class="sxs-lookup"><span data-stu-id="6f047-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="6f047-108">Tworzenie rozwiązania dla niestandardowych wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="6f047-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="6f047-109">Wybierz przycisk **Ustawienia** > **Rozwiązania**, a następnie wybierz pozycję **Nowe**.</span><span class="sxs-lookup"><span data-stu-id="6f047-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="6f047-110">Nazwij rozwiązanie *Wymiary kalkulacji cen organizacji <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="6f047-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="6f047-111">Wprowadź pozostałe wymagane informacje, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="6f047-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Tworzenie rozwiązania do obsługi niestandardowych wymiarów kalkulacji cen](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="6f047-113">Dodawanie wszystkich wymaganych encji i pokrewnych składników do rozwiązania wymiarami cen</span><span class="sxs-lookup"><span data-stu-id="6f047-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="6f047-114">Dodaj następujące encje aplikacji Project Service do rozwiązania obsługującego kalkulację cen, aby wprowadzić ważne zmiany schematu w rozwiązaniu obsługującym kalkulację cen.</span><span class="sxs-lookup"><span data-stu-id="6f047-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="6f047-115">Po zakończeniu tej procedury encje będą rozpoznawać nowe wymiary kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="6f047-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="6f047-116">Wybierz pozycje **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie pozycję **<*nazwa Twojej organizacji*> — wymiary kalkulacji cen**.</span><span class="sxs-lookup"><span data-stu-id="6f047-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="6f047-117">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij kolejno opcje **Dodaj istniejący** > **Encje**.</span><span class="sxs-lookup"><span data-stu-id="6f047-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="6f047-118">W oknie dialogowym **Składniki rozwiązania** zaznacz następujące encje:</span><span class="sxs-lookup"><span data-stu-id="6f047-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="6f047-119">**Rzeczywiste**</span><span class="sxs-lookup"><span data-stu-id="6f047-119">**Actual**</span></span>
   - <span data-ttu-id="6f047-120">**Zasób, który można zarezerwować**</span><span class="sxs-lookup"><span data-stu-id="6f047-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="6f047-121">**Wiersz szacowania**</span><span class="sxs-lookup"><span data-stu-id="6f047-121">**Estimate Line**</span></span>
   - <span data-ttu-id="6f047-122">**Zadanie projektu**</span><span class="sxs-lookup"><span data-stu-id="6f047-122">**Project Task**</span></span>
   - <span data-ttu-id="6f047-123">**Szczegóły wiersza faktury**</span><span class="sxs-lookup"><span data-stu-id="6f047-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="6f047-124">**Wiersz arkusza**</span><span class="sxs-lookup"><span data-stu-id="6f047-124">**Journal Line**</span></span>
   - <span data-ttu-id="6f047-125">**Szczegóły pozycji kontraktu projektu**</span><span class="sxs-lookup"><span data-stu-id="6f047-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="6f047-126">**Członek zespołu projektu**</span><span class="sxs-lookup"><span data-stu-id="6f047-126">**Project Team Member**</span></span>
   - <span data-ttu-id="6f047-127">**Szczegóły wiersza oferty**</span><span class="sxs-lookup"><span data-stu-id="6f047-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="6f047-128">**Narzut na cenę dla roli**</span><span class="sxs-lookup"><span data-stu-id="6f047-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="6f047-129">**Cena roli**</span><span class="sxs-lookup"><span data-stu-id="6f047-129">**Role Price**</span></span>
   - <span data-ttu-id="6f047-130">**Wpis czasu**</span><span class="sxs-lookup"><span data-stu-id="6f047-130">**Time Entry**</span></span>
 
   ![Dodawanie istniejących encji do rozwiązania do obsługi niestandardowych wymiarów kalkulacji cen](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="6f047-132">Dla każdej encji przejrzyj dodawane składniki i ostateczną listę zasobów dla każdej encji.</span><span class="sxs-lookup"><span data-stu-id="6f047-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="6f047-133">Uwzględnij wszystkie formularze i widoki dla każdej wybranej encji.</span><span class="sxs-lookup"><span data-stu-id="6f047-133">Include all forms and views for each of the selected entities.</span></span>

  ![Dodano encje](./media/solution-component-selection.png)


5.  <span data-ttu-id="6f047-135">Po wyświetleniu monitu o uwzględnienie dowolnych encji zależnych dla wybranych encji wybierz opcję **Nie, nie należy dołączać składników wymaganych.**</span><span class="sxs-lookup"><span data-stu-id="6f047-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Z uwzględnieniem encji zależnych](./media/Do-not-include-required.png)
