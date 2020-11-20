---
title: Dodawanie pól niestandardowych do ustawień cen i encji transakcyjnych
description: W tym temacie znajdują się informacje o dodawaniu pól niestandardowych do encji konfiguracji cen i transakcji.
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
ms.openlocfilehash: 32d0dbc3a69d713dcae8d27e52f2a0c6fc296127
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082118"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a><span data-ttu-id="83ae2-103">Dodawanie pól niestandardowych do ustawień cen i encji transakcyjnych</span><span class="sxs-lookup"><span data-stu-id="83ae2-103">Add custom fields to price setup and transactional entities</span></span> 
<span data-ttu-id="83ae2-104">W tym temat założono, że wykonano procedury opisane w temacie [Tworzenie niestandardowych pól i encji](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="83ae2-104">This topic assumes that you have completed the procedures in the topic, [Create custom fields and entities](create-custom-fields-entities.md).</span></span> <span data-ttu-id="83ae2-105">Jeśli tych procedur jeszcze nie wykonano, wróć, wykonaj je, a następnie wróć do tego tematu.</span><span class="sxs-lookup"><span data-stu-id="83ae2-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="83ae2-106">W tym temacie procedury pokazują, jak dodawać do encji i do elementów interfejsu użytkownika wymagane odwołania do pól niestandardowych, np. formularze i widoki.</span><span class="sxs-lookup"><span data-stu-id="83ae2-106">In this topic, the procedures will show you how to add the required custom field references to entities and to the user interface (UI) elements such as forms and views.</span></span>

## <a name="add-custom-pricing-dimension-fields"></a><span data-ttu-id="83ae2-107">Dodawanie pól wymiarów niestandardowej kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="83ae2-107">Add custom pricing dimension fields</span></span> 
<span data-ttu-id="83ae2-108">Po utworzeniu niestandardowych pól i encji kolejnym krokiem jest ustawienie w konfiguracji cen i encji transakcyjnych wszelkich niestandardowych encji lub zestawów opcji przez utworzenie pól referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="83ae2-108">After custom fields and entities have been created, the next step is to make price setup and transactional entities aware of any custom entities or option sets by creating reference fields.</span></span> <span data-ttu-id="83ae2-109">W zależności od tego, czy lista wymiarów kalkulacji cen zawiera zestaw opcji wymiarów lub wymiarów encji lub jedno i drugie, należy wykonać tylko kroki opisane w sekcji **Niestandardowe wymiary kalkulacji cen oparte na zestawie opcji** lub **Niestandardowe wymiary kalkulacji cen oparte na encji** lub jedno i drugie, odpowiednio.</span><span class="sxs-lookup"><span data-stu-id="83ae2-109">Depending on whether your pricing dimensions list includes option set dimensions or entity dimensions or both, follow only the steps in **Option set-based custom pricing dimensions** or **Entity-based custom pricing dimensions** , or both, respectively.</span></span>

### <a name="option-set-based-custom-pricing-dimensions"></a><span data-ttu-id="83ae2-110">Niestandardowe wymiary kalkulacji cen oparte na zestawie opcji</span><span class="sxs-lookup"><span data-stu-id="83ae2-110">Option set-based custom pricing dimensions</span></span>
<span data-ttu-id="83ae2-111">Kiedy niestandardowy wymiar kalkulacji cen jest oparty na zestawie opcji, należy dodać go jako pole do kluczowych encji Project Service.</span><span class="sxs-lookup"><span data-stu-id="83ae2-111">When a custom pricing dimension is option set-based, add it as a field to key Project Service entities.</span></span> <span data-ttu-id="83ae2-112">W poniższej procedurze **Lokalizacja pracy zasobu** i **Godziny pracy zasobu** są używane jako wymiary kalkulacji cen oparte na zestawach opcji.</span><span class="sxs-lookup"><span data-stu-id="83ae2-112">In the following procedure, **Resource Work Location** and **Resource Work Hours** are used as the option set-based pricing dimensions.</span></span> <span data-ttu-id="83ae2-113">Najpierw muszą zostać dodane jako pola do encji kalkulacji cen, **Cena roli** i **Narzut na cenę dla roli**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-113">These must first be added as fields to the pricing entities, **Role Price** and **Role Price Markup**.</span></span>

1. <span data-ttu-id="83ae2-114">W Project Service Automation (PSA) kliknij kolejno opcje **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie pozycję **Wymiary finansowe \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-114">In Project Service Automation (PSA), click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="83ae2-115">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Cena roli**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-115">In Solution Explorer, on the left navigation pane, select **Entities > Role Price**.</span></span>
3. <span data-ttu-id="83ae2-116">Rozwiń encję **Cena roli** i wybierz **Pola**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-116">Expand the entity **Role Price** and select **Fields**.</span></span>
4. <span data-ttu-id="83ae2-117">Kliknij **Nowe** , aby utworzyć nowe pole o nazwie **Lokalizacja pracy zasobu** i wybierz **Zestaw opcji** jako typ pola.</span><span class="sxs-lookup"><span data-stu-id="83ae2-117">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="83ae2-118">Wybierz opcję **Użyj istniejącego zestaw opcji** , wybierz zostaw opcji **Lokalizacja pracy zasobu** i kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-118">Select **Use an existing Option set** , select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="83ae2-119">Powtórz kroki 1-5, aby dodać to pole do encji **Narzut na cenę dla roli**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-119">Repeat steps 1 - 5 to add this field to the **Role Price Markup** entity.</span></span> 
7. <span data-ttu-id="83ae2-120">Powtórz kroki 1-5 dla zestaw opcji **Godziny pracy zasobu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-120">Repeat steps 1 - 5 for the **Resource Work Hours** option set.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83ae2-121">W przypadku dodawania pola do więcej niż jednej encji należy użyć tej samej nazwy pola we wszystkich encjach.</span><span class="sxs-lookup"><span data-stu-id="83ae2-121">When you add a field to more than one entity, use the same field name across all of the entities.</span></span> 

> ![Dodawanie lokalizacji pracy zasobu do ceny roli](media/RWL-Field.png)

<span data-ttu-id="83ae2-123">W fazach sprzedaży i szacunkowej projektu prognozy nakładu pracy wymagane do ukończenia pracy **lokalnej** i **na miejscu** w **zwykłych godzinach** i **nadgodzinach** są używane w celu oszacowania wartość oferty/projektu.</span><span class="sxs-lookup"><span data-stu-id="83ae2-123">In the sales and estimation phases for a project, estimates of the work effort that is required to complete **Local** and **Onsite** work, in **Regular hours** and **Overtime hours**  are used to estimate the value of the Quote/Project.</span></span> <span data-ttu-id="83ae2-124">Pola **Lokalizacje pracy zasobu** i **Godziny pracy zasobu** zostaną dodane do encji oszacowania, **Szczegóły wiersza oferty** , **Szczegóły wiersza umowy** , **Zadanie projektu** , **Członek zespołu projektu** oraz **Wiersz szacowania**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-124">The fields **Resource Work Location** and **Resource Work Hours** will be added to the estimation entities, **Quote Line Detail** , **Contract Line detail** , **Project Task** , **Project Team Member** , and **Estimate Line**.</span></span>

1. <span data-ttu-id="83ae2-125">W programie PSA kliknij opcję **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-125">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="83ae2-126">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Szczegóły wiersza oferty**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-126">In Solution Explorer, on the left navigation pane, select **Entities > Quote Line Detail**.</span></span>
3. <span data-ttu-id="83ae2-127">Rozwiń encję **Szczegóły wiersza oferty** i wybierz **Pola**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-127">Expand the **Quote Line Detail** entity, and select **Fields**.</span></span>
4. <span data-ttu-id="83ae2-128">Kliknij **Nowe** , aby utworzyć nowe pole o nazwie **Lokalizacja pracy zasobu** i wybierz **Zestaw opcji** jako typ pola.</span><span class="sxs-lookup"><span data-stu-id="83ae2-128">Click **New** to create a new field called **Resource Work Location** and select the field type, **Option set**.</span></span> 
5. <span data-ttu-id="83ae2-129">Wybierz opcję **Użyj istniejącego zestaw opcji** , wybierz **Lokalizacja pracy zasobu** i kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-129">Select **Use an existing Option set** and **Resource Work Location** , and then click **Save**.</span></span>
6. <span data-ttu-id="83ae2-130">Powtórz kroki 1-5, aby dodać to pole do encji **Szczegóły pozycji kontraktu projektu** , **Zadanie projektu** , **Członek zespołu projektu** i **Wiersz szacowania**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-130">Repeat steps 1 - 5 to add this field to the **Project Contract line detail** , **Project Task** , **Project Team Member** , and **Estimate Line** entities.</span></span>
7. <span data-ttu-id="83ae2-131">Powtórz kroki 1-6 dla zestaw opcji **Godziny pracy zasobu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-131">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Dodawanie lokalizacji pracy zasobu do Wiersza szacowania](media/RWL-Default-Value.png)


<span data-ttu-id="83ae2-133">W celu dostarczenia i fakturowania ukończona praca powinna być dokładnie wyceniona, aby wybrać czy została wykonana **Lokalnie** lub **Na miejscu** i czy została ukończona w **godzinach pracy** czy w **nadgodzinach** w wartościach rzeczywistych projektu.</span><span class="sxs-lookup"><span data-stu-id="83ae2-133">For delivery and invoicing, completed work needs to be accurately priced to select whether it was performed **Local** or **Onsite** , and whether it was completed during **Regular hours** or **Overtime** on the Project Actuals.</span></span> <span data-ttu-id="83ae2-134">Pola **Lokalizacja pracy zasobu** i **Godziny pracy zasobu** zostaną dodane do encji **Wpis czasu** , **Rzeczywiste** , **Szczegóły wiersza faktury** oraz **Wiersz dziennika**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-134">The **Resource Work Location** and **Resource Work hours** fields should be added to the **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line** entities.</span></span>

1. <span data-ttu-id="83ae2-135">W programie PSA kliknij opcję **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-135">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="83ae2-136">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Wpisz czasu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-136">In Solution Explorer, on the left navigation pane, select  **Entities > Time Entry**.</span></span>
3. <span data-ttu-id="83ae2-137">Rozwiń encję **Szczegóły wiersza oferty** , a następnie wybierz **Pola**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-137">Expand the **Quote Line Detail** entity, and then select **Fields**.</span></span>
4. <span data-ttu-id="83ae2-138">Kliknij **Nowe** , aby utworzyć nowe pole o nazwie **Lokalizacja pracy zasobu** i wybierz **Zestaw opcji** jako typ pola.</span><span class="sxs-lookup"><span data-stu-id="83ae2-138">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="83ae2-139">Wybierz opcję **Użyj istniejącego zestaw opcji** , wybierz zostaw opcji **Lokalizacja pracy zasobu** i kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-139">Select **Use an existing Option set** , select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="83ae2-140">Powtórz kroki 1-5 w celu dodania tego pola do encji **Rzeczywiste** , **Szczegóły wiersza faktury** i **Wiersz dziennika**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-140">Repeat steps 1 - 5 to add this field to the **Actual** , **Invoice Line Detail** , and **Journal Line** entities.</span></span>
7. <span data-ttu-id="83ae2-141">Powtórz kroki 1-6 dla zestaw opcji **Godziny pracy zasobu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-141">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Dodawanie lokalizacji pracy zasobu do Wpisu czasu](media/RWL-time-entry.png)

<span data-ttu-id="83ae2-143">Spowoduje to ukończenie zmian schematu wymaganych dla niestandardowych wymiarów opartych na zestawie opcji.</span><span class="sxs-lookup"><span data-stu-id="83ae2-143">This completes the schema changes required for option set-based custom dimensions.</span></span>

## <a name="entity-based-custom-pricing-dimensions"></a><span data-ttu-id="83ae2-144">Niestandardowe wymiary kalkulacji cen oparte na encji</span><span class="sxs-lookup"><span data-stu-id="83ae2-144">Entity-based custom pricing dimensions</span></span>

<span data-ttu-id="83ae2-145">Kiedy niestandardowym wymiarem kalkulacji cen jest encja, dodasz relację 1:N między encją wymiarową i kluczowymi encjami Project Service.</span><span class="sxs-lookup"><span data-stu-id="83ae2-145">When the custom pricing dimension is an entity, you will add 1:N relationships between the dimension entity and key Project Service entities.</span></span> <span data-ttu-id="83ae2-146">Kiedy użyjemy przykładu Standardowe stanowisko z góry, należy oczekiwać, że każdy pracownik będzie miał przypisany standardowe stanowisko.</span><span class="sxs-lookup"><span data-stu-id="83ae2-146">Using the Standard Title example from above, it is reasonable to expect that each employee is assigned a standard title.</span></span> <span data-ttu-id="83ae2-147">To będzie wymagało relacji 1:N między standardowym stanowiskiem a zasobem, który można zaksięgować albo relacji N:1, jeśli utworzono z zasobu, który można zaksięgować do standardowego stanowiska.</span><span class="sxs-lookup"><span data-stu-id="83ae2-147">SAs a result, you will need a 1:N relationship from Standard Title to Bookable Resource, or a N:1 relationship if it were created from Bookable Resource to Standard Title.</span></span>

1. <span data-ttu-id="83ae2-148">W programie PSA kliknij opcję **Ustawienia** > **Rozwiązania** , a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-148">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="83ae2-149">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-149">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
3. <span data-ttu-id="83ae2-150">Rozwiń encję **Standardowe stanowisko** i wybierz **Relacje 1:N**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-150">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
4. <span data-ttu-id="83ae2-151">Kliknij pozycję **Nowa** , aby utworzyć nową relację 1:N o nazwie **Standardowe stanowisko do Zasobu, który można zaksięgować**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-151">Click **New** to create a new 1:N relationship called **Standard Title to Bookable Resource**.</span></span> <span data-ttu-id="83ae2-152">Wprowadź wymagane informacje, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-152">Enter the required information, and then click **Save**.</span></span>

> ![Dodawanie standardowego stanowiska jako pola odwołania do zasobu, który można zarezerwować](media/ST-BR.png)

<span data-ttu-id="83ae2-154">Standardowe stanowisko musi również zostać dodane do encji kalkulacji cen Project Service, **Cena roli** oraz **Narzut na cenę dla roli**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-154">The Standard Title will also need to be added to Project Service Pricing entities, **Role Price** and **Role Price Markup**.</span></span> <span data-ttu-id="83ae2-155">Te dane są również uzupełniane przy użyciu relacji 1:N między encjami **Standardowe stanowisko** a **Cena roli** i encjami **Standardowe stanowisko** i **Narzut na cenę dla roli**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-155">This is also completed using 1:N relationships between the **Standard Title** and **Role Price** entities and **Standard Title** and **Role Price Markup** entities.</span></span>

1. <span data-ttu-id="83ae2-156">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-156">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="83ae2-157">Rozwiń encję **Standardowe stanowisko** i wybierz **Relacje 1:N**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-157">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="83ae2-158">Kliknij pozycję **Nowa** , aby utworzyć nową relację 1:N o nazwie **Standardowe stanowisko do Ceny roli**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-158">Click **New** to create a new 1:N relationship called **Standard Title to Role Price**.</span></span> <span data-ttu-id="83ae2-159">Wprowadź wymagane informacje, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-159">Enter the required information, and then click **Save**.</span></span>
4. <span data-ttu-id="83ae2-160">Powtórz kroki 1–4, aby utworzyć relacje 1:N między encjami **Standardowe stanowisko** i **Narzut na cenę dla roli** ,</span><span class="sxs-lookup"><span data-stu-id="83ae2-160">Repeat steps 1 - 4 to create 1:N relationships between the **Standard Title** and **Role Price Markup** entities,</span></span>

<span data-ttu-id="83ae2-161">W fazach sprzedaży i oszacowania projektu, do kalkulacji cen oferty/projektu konieczne są szacowania nakładu pracy dotyczące poszczególnych standardowych stanowisk.</span><span class="sxs-lookup"><span data-stu-id="83ae2-161">In the sales and estimation phases for the project, to price the Quote/Project, estimates of the work effort are required for each standard title.</span></span> <span data-ttu-id="83ae2-162">Oznacza to, że potrzebne są relacje 1:N ze Standardowego stanowiska do poszczególnych encji szacowania w Project Service:</span><span class="sxs-lookup"><span data-stu-id="83ae2-162">This means that 1:N relationships from Standard Title to each of these estimation entities in Project Service are needed:</span></span> 

- <span data-ttu-id="83ae2-163">**zczegóły wiersza oferty**</span><span class="sxs-lookup"><span data-stu-id="83ae2-163">**Quote line Detail**</span></span>
- <span data-ttu-id="83ae2-164">**Szczegóły pozycji kontraktu projektu**</span><span class="sxs-lookup"><span data-stu-id="83ae2-164">**Project Contract Line Detail**</span></span>
- <span data-ttu-id="83ae2-165">**Zadanie projektu**</span><span class="sxs-lookup"><span data-stu-id="83ae2-165">**Project Task**</span></span>
- <span data-ttu-id="83ae2-166">**Członek zespołu projektu**</span><span class="sxs-lookup"><span data-stu-id="83ae2-166">**Project Team Member**</span></span>
- <span data-ttu-id="83ae2-167">**Wiersz szacowania**</span><span class="sxs-lookup"><span data-stu-id="83ae2-167">**Estimate Line**</span></span>

5. <span data-ttu-id="83ae2-168">Powtórz kroki 1-5, aby utworzyć relacje 1:N z encji **Standardowe stanowisko** do encji **Szczegóły wiersza oferty** , **Szczegóły pozycji kontraktu projektu** , **Zadanie projektu** , **Członek zespołu projektu** oraz **Wiersz szacowania**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-168">Repeat steps 1 - 5 to create 1:N relationships from **Standard Title** to **Quote line Detail** , **Project Contract Line Detail** , **Project Task** , **Project Team Member** , and **Estimate Line**.</span></span>

> ![Dodawanie standardowego stanowiska jako pola odwołania do wiersza szacowania](media/ST-Estimate-Line.png)

<span data-ttu-id="83ae2-170">W fazach dostarczania i fakturowania praca wykonana przez każde standardowe stanowisko musi być dokładnie wyceniona w wartościach rzeczywistych projektu.</span><span class="sxs-lookup"><span data-stu-id="83ae2-170">In the Delivery and Invoicing phases, the work completed by each standard title must be accurately priced on the Project Actuals.</span></span> <span data-ttu-id="83ae2-171">To oznacza, że musi być relacja 1:N z encji **Standardowe stanowisko** do encji **Wpis czasu** , **Rzeczywiste** , **Szczegóły wiersza faktury** oraz **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-171">This means that there needs to be 1:N relationships from **Standard Title** to **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line entities**.</span></span>

6. <span data-ttu-id="83ae2-172">Powtórz kroki 1-6, aby utworzyć relacje 1:N z encji **Standardowe stanowisko** do encji **Wpis czasu** , **Rzeczywiste** , **Szczegóły wiersza faktury** oraz **Wiersz arkusza**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-172">Repeat steps 1 - 6 to create 1:N relationships from **Standard Title** to **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line entities**.</span></span>

> ![Dodawanie standardowego stanowiska jako pola odwołania do wpisu czasu](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a><span data-ttu-id="83ae2-174">Konfigurowanie ustawiania domyślnych wartości wymiaru przy użyciu funkcji mapowania platformy</span><span class="sxs-lookup"><span data-stu-id="83ae2-174">Set up Dimension value defaulting using the mappings features of the platform</span></span>
<span data-ttu-id="83ae2-175">W przypadku encji Wpis czasu pomocne jest, kiedy system domyślnie ustawia ustawienie standardowe stanowisko na Wpis czas z Zasobu, który można zarezerwować, który rejestruje wpis czasu.</span><span class="sxs-lookup"><span data-stu-id="83ae2-175">For Time Entry, it would be helpful to have the system default the standard title on the Time Entry from the Bookable Resource that is recording the time entry.</span></span> <span data-ttu-id="83ae2-176">Wykonaj poniższe kroki, aby dodać mapowania do relacji 1:N z encji **Zasób, który można zarezerwować** do encji **Wpis czasu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-176">Use the following steps to add field mappings on the 1:N relationship from **Bookable Resource** to **Time Entry**.</span></span>

1. <span data-ttu-id="83ae2-177">W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Standardowe stanowisko**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-177">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="83ae2-178">Rozwiń encję **Standardowe stanowisko** i wybierz **Relacje 1:N**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-178">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="83ae2-179">Kliknij dwukrotnie pozycję **zasób z możliwością rezerwacji do wpisu czasu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-179">Double-click **Bookable Resource to Time Entry**.</span></span> <span data-ttu-id="83ae2-180">Na stronie **Relacja** kliknij opcję **Użyj mapowań pól**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-180">On the **Relationship** page, click **Use Field mappings**.</span></span> 
4. <span data-ttu-id="83ae2-181">Kliknij pozycję **Nowy** , aby utworzyć nowe mapowanie między polem **Standardowe stanowisko** w encji **Zasób, który można zarezerwować** a polem odwołania **Standardowe stanowisko** w encji **Wpis czasu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-181">Click **New** to create a new field mapping between the **Standard Title** field on the **Bookable Resource** entity to the **Standard Title** reference field on **Time Entry** entity.</span></span> 

> ![Skonfiguruj mapowanie pól, aby zezwolić na domyślne używanie wpisu czasu jako standardowego tytułu w zasobie, który można zarezerwować.](media/ST-Mapping2.png)


<span data-ttu-id="83ae2-183">Spowoduje to ukończenie zmian schematu wymaganych dla niestandardowych wymiarów opartych na encji.</span><span class="sxs-lookup"><span data-stu-id="83ae2-183">This completes the schema changes required for entity-based custom dimensions.</span></span>

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a><span data-ttu-id="83ae2-184">Dodawanie niestandardowych pól do formularzy, widoków i reguł biznesowych</span><span class="sxs-lookup"><span data-stu-id="83ae2-184">Add custom fields to forms, views, and business rules</span></span>

<span data-ttu-id="83ae2-185">Po wprowadzeniu wszystkich wymaganych zmian schematu kolejne kroki polegają na ustawieniu, aby pola były widoczne w interfejsie użytkownika przez dodanie pól do formularzy i widoków.</span><span class="sxs-lookup"><span data-stu-id="83ae2-185">After you have made all of the required schema changes, the next step is to make the fields visible in the UI by adding the fields to the forms and views.</span></span>

1. <span data-ttu-id="83ae2-186">Otwórz formularz lub widok.</span><span class="sxs-lookup"><span data-stu-id="83ae2-186">Open the form or the view.</span></span> <span data-ttu-id="83ae2-187">W prawym okienku nawigacji zaznacz pole i przeciągnij je na kanwę formularza.</span><span class="sxs-lookup"><span data-stu-id="83ae2-187">On the right navigation pane, select the field and drag it on to the form canvas.</span></span> 
2. <span data-ttu-id="83ae2-188">W przypadku edytowania widoku użyj prawego okienka nawigacji, kliknij **Dodaj pola** , a następnie w oknie dialogowym **Lista pól** wybierz wymagane pola i kliknij przycisk **OK.**</span><span class="sxs-lookup"><span data-stu-id="83ae2-188">If you are editing a view, use the right navigation pane, click **Add fields** , and in the **Field listing** dialog box, select the fields that you need and click **Ok**.</span></span>

<span data-ttu-id="83ae2-189">Poniższa tabela zawiera wyczerpującą listę gotowych formularzy i widoków, wyszczególnionych według encji, które należy zaktualizować o te pola.</span><span class="sxs-lookup"><span data-stu-id="83ae2-189">The following table provides a comprehensive list of out-of-the-box forms and views, by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="83ae2-190">Jeśli którekolwiek dodatkowe widoki lub formularze w dostosowaniach korzystają z tych encji, należy dodać nowe pola również do nich.</span><span class="sxs-lookup"><span data-stu-id="83ae2-190">If you have any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

| <span data-ttu-id="83ae2-191">Encja Project Service</span><span class="sxs-lookup"><span data-stu-id="83ae2-191">Project Service Entity</span></span>        | <span data-ttu-id="83ae2-192">Formularz, które wymagają nowego pola</span><span class="sxs-lookup"><span data-stu-id="83ae2-192">Forms that need the new field</span></span>   |<span data-ttu-id="83ae2-193">Widoki, które wymagają nowego pola</span><span class="sxs-lookup"><span data-stu-id="83ae2-193">Views that need the new field</span></span>      |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="83ae2-194">Cena roli</span><span class="sxs-lookup"><span data-stu-id="83ae2-194">Role Price</span></span>|<span data-ttu-id="83ae2-195">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-195">• Information</span></span> |<span data-ttu-id="83ae2-196">• Aktywne ceny kategorii zasobów</span><span class="sxs-lookup"><span data-stu-id="83ae2-196">• Active Resource Category Prices</span></span><br> <span data-ttu-id="83ae2-197">• Widok skojarzony ceny kategorii zasobów</span><span class="sxs-lookup"><span data-stu-id="83ae2-197">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="83ae2-198">Narzut na cenę dla roli</span><span class="sxs-lookup"><span data-stu-id="83ae2-198">Role Price Markup</span></span>|<span data-ttu-id="83ae2-199">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-199">• Information</span></span>|<span data-ttu-id="83ae2-200">• Aktywny narzut na cenę dla roli</span><span class="sxs-lookup"><span data-stu-id="83ae2-200">• Active Role Price Markup</span></span><br><span data-ttu-id="83ae2-201">• Widok skojarzony narzutu na cenę dla roli</span><span class="sxs-lookup"><span data-stu-id="83ae2-201">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="83ae2-202">Szczegóły wiersza oferty</span><span class="sxs-lookup"><span data-stu-id="83ae2-202">Quote line detail</span></span>|<span data-ttu-id="83ae2-203">• Informacje o projekcie</span><span class="sxs-lookup"><span data-stu-id="83ae2-203">• Project Information</span></span><br><span data-ttu-id="83ae2-204">• Szybkie tworzenie projektów</span><span class="sxs-lookup"><span data-stu-id="83ae2-204">• Project Quick Create</span></span>|<span data-ttu-id="83ae2-205">• Aktywne szczegóły wierszy ofert</span><span class="sxs-lookup"><span data-stu-id="83ae2-205">• Active Quote Line Detail</span></span><br><span data-ttu-id="83ae2-206">• Połączone szczegóły wierszy ofert</span><span class="sxs-lookup"><span data-stu-id="83ae2-206">• Combined Quote Line Details</span></span><br><span data-ttu-id="83ae2-207">• Widok skojarzony szczegółów wierszy oferty</span><span class="sxs-lookup"><span data-stu-id="83ae2-207">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="83ae2-208">Szczegóły pozycji kontraktu projektu</span><span class="sxs-lookup"><span data-stu-id="83ae2-208">Project Contract line detail</span></span>|<span data-ttu-id="83ae2-209">• Informacje o projekcie</span><span class="sxs-lookup"><span data-stu-id="83ae2-209">• Project Information</span></span><br><span data-ttu-id="83ae2-210">• Szybkie tworzenie projektów</span><span class="sxs-lookup"><span data-stu-id="83ae2-210">• Project Quick Create</span></span>|<span data-ttu-id="83ae2-211">• Połączone szczegóły pozycji kontraktu</span><span class="sxs-lookup"><span data-stu-id="83ae2-211">• Combined Contract Line Details</span></span><br><span data-ttu-id="83ae2-212">• Aktywne szczegóły pozycji kontraktu</span><span class="sxs-lookup"><span data-stu-id="83ae2-212">• Active Contract Line Details</span></span><br><span data-ttu-id="83ae2-213">• Widok skojarzony szczegółów pozycji kontraktu</span><span class="sxs-lookup"><span data-stu-id="83ae2-213">• Contract Line Details Associated View</span></span>|
|  <span data-ttu-id="83ae2-214">Zadanie projektu</span><span class="sxs-lookup"><span data-stu-id="83ae2-214">Project Task</span></span>|<span data-ttu-id="83ae2-215">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-215">• Information</span></span><br><span data-ttu-id="83ae2-216">• Nowy formularz</span><span class="sxs-lookup"><span data-stu-id="83ae2-216">• New Form</span></span>||
|  <span data-ttu-id="83ae2-217">Członek zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="83ae2-217">Project Team Member</span></span>|<span data-ttu-id="83ae2-218">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-218">• Information</span></span><br><span data-ttu-id="83ae2-219">• Nowy formularz</span><span class="sxs-lookup"><span data-stu-id="83ae2-219">• New Form</span></span>|<span data-ttu-id="83ae2-220">• Aktywni członkowie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="83ae2-220">• Active Project Team Members</span></span><br><span data-ttu-id="83ae2-221">• Członkowie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="83ae2-221">• Project Team Members</span></span><br><span data-ttu-id="83ae2-222">• Widok skojarzony członków zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="83ae2-222">• Project Team members associated View</span></span>|
|  <span data-ttu-id="83ae2-223">Wpis czasu</span><span class="sxs-lookup"><span data-stu-id="83ae2-223">Time Entry</span></span>|<span data-ttu-id="83ae2-224">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-224">• Information</span></span><br><span data-ttu-id="83ae2-225">• Utwórz wpis czasu</span><span class="sxs-lookup"><span data-stu-id="83ae2-225">• Create Time Entry</span></span>|<span data-ttu-id="83ae2-226">• Moje wpisy czasu według daty</span><span class="sxs-lookup"><span data-stu-id="83ae2-226">• My Time Entries By Date</span></span><br><span data-ttu-id="83ae2-227">• Moje wpisy czasu w tym tygodniu</span><span class="sxs-lookup"><span data-stu-id="83ae2-227">• My time Entries for this week</span></span><br><span data-ttu-id="83ae2-228">• Wpisy czasu do zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="83ae2-228">• Time entries for approval</span></span>|
|  <span data-ttu-id="83ae2-229">Wiersz arkusza</span><span class="sxs-lookup"><span data-stu-id="83ae2-229">Journal Line</span></span>|<span data-ttu-id="83ae2-230">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-230">• Information</span></span><br><span data-ttu-id="83ae2-231">• Szybkie tworzenie</span><span class="sxs-lookup"><span data-stu-id="83ae2-231">• Quick create</span></span>|<span data-ttu-id="83ae2-232">• Aktywne wiersze arkuszy</span><span class="sxs-lookup"><span data-stu-id="83ae2-232">• Active journal lines</span></span><br><span data-ttu-id="83ae2-233">• Widok skojarzony wiersza arkusza</span><span class="sxs-lookup"><span data-stu-id="83ae2-233">• Journal Line associated view</span></span>|
|  <span data-ttu-id="83ae2-234">Szczegóły wiersza faktury</span><span class="sxs-lookup"><span data-stu-id="83ae2-234">Invoice Line Detail</span></span>|<span data-ttu-id="83ae2-235">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-235">• Information</span></span><br><span data-ttu-id="83ae2-236">• Szybkie tworzenie</span><span class="sxs-lookup"><span data-stu-id="83ae2-236">• Quick create</span></span>|<span data-ttu-id="83ae2-237">• Aktywne szczegóły wierszy faktur</span><span class="sxs-lookup"><span data-stu-id="83ae2-237">• Active Invoice Line Details</span></span><br><span data-ttu-id="83ae2-238">• Odpłatne transakcje faktury</span><span class="sxs-lookup"><span data-stu-id="83ae2-238">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="83ae2-239">• Uzupełniające transakcje faktury</span><span class="sxs-lookup"><span data-stu-id="83ae2-239">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="83ae2-240">• Widok skojarzony szczegółów wiersza faktury</span><span class="sxs-lookup"><span data-stu-id="83ae2-240">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="83ae2-241">• Nieodpłatne transakcje faktury</span><span class="sxs-lookup"><span data-stu-id="83ae2-241">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="83ae2-242">Wartość rzeczywista</span><span class="sxs-lookup"><span data-stu-id="83ae2-242">Actual</span></span>|<span data-ttu-id="83ae2-243">• Informacja</span><span class="sxs-lookup"><span data-stu-id="83ae2-243">• Information</span></span><br><span data-ttu-id="83ae2-244">• Aktywne wartości rzeczywiste</span><span class="sxs-lookup"><span data-stu-id="83ae2-244">• Active Actuals</span></span>|<span data-ttu-id="83ae2-245">• Widok skojarzony wartości rzeczywistej</span><span class="sxs-lookup"><span data-stu-id="83ae2-245">• Actual Associated view</span></span>|

<span data-ttu-id="83ae2-246">Pola niestandardowe mogą być również dodawane w regułach biznesowych w zależności od zdefiniowanych opcji.</span><span class="sxs-lookup"><span data-stu-id="83ae2-246">Custom fields may also need to be added on business rules depending on what you have defined.</span></span> <span data-ttu-id="83ae2-247">Jednym z wbudowanych przykładów jest wprowadzenie reguły **możliwość edycji wpisu czasu na podstawie stanu**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-247">One out-of-the-box example is for the business rule **Editability of Time Entry based on status**.</span></span> <span data-ttu-id="83ae2-248">Ta reguła określa, które pola muszą być zablokowane, gdy wpis czasu będzie mieć stan, który nie jest edytowalny, np. **Zatwierdzony**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-248">This rule defines which fields need to be locked when the Time Entry is in a non-editable status such as **Approved**.</span></span> <span data-ttu-id="83ae2-249">Dodaj pola do tej reguły biznesowej, aby były zablokowane do edycji, kiedy wpis czasu ma status inny niż **Wersja robocza** lub **Zwrócony**.</span><span class="sxs-lookup"><span data-stu-id="83ae2-249">Add fields to this business rule so that the fields are locked for editing when the Time Entry is in a status other than **Draft** or **Returned**.</span></span>