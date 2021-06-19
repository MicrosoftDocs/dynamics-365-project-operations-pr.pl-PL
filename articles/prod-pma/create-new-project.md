---
title: Tworzenie nowego projektu
description: W tym temacie zamieszczono informacje dotyczące tworzenia nowego projektu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006254"
---
# <a name="create-a-new-project"></a><span data-ttu-id="79665-103">Tworzenie nowego projektu</span><span class="sxs-lookup"><span data-stu-id="79665-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79665-104">Wykonaj poniższe kroki, aby utworzyć nowy projekt.</span><span class="sxs-lookup"><span data-stu-id="79665-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="79665-105">Na stronie **Zarządzanie projektem** wybierz **Nowy projekt**, a następnie wprowadź następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="79665-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="79665-106">**Typ projektu:** czas i materiały</span><span class="sxs-lookup"><span data-stu-id="79665-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="79665-107">**Nazwa projektu:** faza uaktualniania w XYZ 2</span><span class="sxs-lookup"><span data-stu-id="79665-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="79665-108">**Grupa projektów:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="79665-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="79665-109">**Identyfikator kontraktu projektu:** 00000002</span><span class="sxs-lookup"><span data-stu-id="79665-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="79665-110">Wybierz pozycję **Utwórz projekt**.</span><span class="sxs-lookup"><span data-stu-id="79665-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="79665-111">Przypisywanie zasobu do projektu</span><span class="sxs-lookup"><span data-stu-id="79665-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="79665-112">Na stronie **Pracownicy** na liście **Pracownicy** wybierz rekord pracownika, dla którego wcześniej skonfigurowano kompetencje, i otwórz rekord pracownika.</span><span class="sxs-lookup"><span data-stu-id="79665-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="79665-113">W okienku akcji na karcie **Projekt** w grupie **Ustawienia** kliknij opcję **Przypisz projekty**.</span><span class="sxs-lookup"><span data-stu-id="79665-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="79665-114">Na stronie **Przypisania projektów walidacji zasobów**, na karcie **Projekty**, w polu **Dodaj projekt do wybranych projektów** wybierz Filtr w projekcie **XYZ faza aktualizacji 2**.</span><span class="sxs-lookup"><span data-stu-id="79665-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="79665-115">W okienku **Pozostałe projekty** wybierz projekt, a następnie wybierz przycisk strzałki, aby dodać go do okienka **Wybrane projekty**.</span><span class="sxs-lookup"><span data-stu-id="79665-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="79665-116">Kategorie zasobu można również przypisać w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="79665-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="79665-117">Kategoria typu to albo **Koszt**, albo **Przychód**.</span><span class="sxs-lookup"><span data-stu-id="79665-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="79665-118">Typ kategorii jest określany przez organizację.</span><span class="sxs-lookup"><span data-stu-id="79665-118">The category type is determined by your organization.</span></span> <span data-ttu-id="79665-119">Jeśli do zasobu nie są przypisane żadne kategorie, Finance wyszukuje domyślną kategorię według cen godzinowych dla kosztów i przychodów.</span><span class="sxs-lookup"><span data-stu-id="79665-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="79665-120">Skonfiguruj zasoby projektu i cechy roli</span><span class="sxs-lookup"><span data-stu-id="79665-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="79665-121">Menedżer projektu może używać funkcji zasobów projektu do tworzenia ról wymaganych w projekcie.</span><span class="sxs-lookup"><span data-stu-id="79665-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="79665-122">Role mogą być używane, jeśli potwierdzone zasoby są nadal nieznane podczas rezerwowania zasobów.</span><span class="sxs-lookup"><span data-stu-id="79665-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="79665-123">Role mogą być tymczasowo rezerwowane jako planowane zasoby, aby można było kontynuować etapy planowania projektów.</span><span class="sxs-lookup"><span data-stu-id="79665-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="79665-124">[![Przykład roli](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="79665-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="79665-125">**Scenariusz:** Contoso zostało zatrudnione do realizacji projektu typu Czas i materiał, który posiada zatwierdzoną kartę projektu.</span><span class="sxs-lookup"><span data-stu-id="79665-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="79665-126">Młodszy kierownik projektu nadal kończy zakres projektu.</span><span class="sxs-lookup"><span data-stu-id="79665-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="79665-127">Menedżer zasobów obecnie identyfikuje konkretne zasoby, które będą zastrzeżone do pracy nad nowym projektem.</span><span class="sxs-lookup"><span data-stu-id="79665-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="79665-128">Ze względu na krytyczny charakter projektu, sponsor projektu poprosił starszego kierownika projektu jako jedną z ról.</span><span class="sxs-lookup"><span data-stu-id="79665-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="79665-129">Menedżer zasobów musi nabyć nowy zasób i zdefiniować rolę w systemie na wypadek, gdyby młodszy kierownik projektu potrzebował informacji o zasobach podczas planowania projektu.</span><span class="sxs-lookup"><span data-stu-id="79665-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="79665-130">Poniższe kroki pokazują, jak menedżer zasobów może skonfigurować rolę starszego kierownika projektu i skojarzyć z nią cechy zasobu.</span><span class="sxs-lookup"><span data-stu-id="79665-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="79665-131">Później roli można użyć do wyszukiwania dostępnych zasobów, które pasują do wymaganych kompetencji zasobów.</span><span class="sxs-lookup"><span data-stu-id="79665-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="79665-132">Na stronie **Role ustawień** wybierz **Nowy**, a następnie wprowadź następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="79665-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="79665-133">**Identyfikator roli:** starszy kierownik projektu</span><span class="sxs-lookup"><span data-stu-id="79665-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="79665-134">**Opis:** starszy kierownik projektu</span><span class="sxs-lookup"><span data-stu-id="79665-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="79665-135">Wybierz pozycję **Utwórz**.</span><span class="sxs-lookup"><span data-stu-id="79665-135">Select **Create**.</span></span>
3. <span data-ttu-id="79665-136">Zaznacz rolę **Starszy kierownik projektu**, a następnie wybierz pozycję **Konfigurowanie charakterystyki**.</span><span class="sxs-lookup"><span data-stu-id="79665-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="79665-137">W polu **Typ charakterystyki** wybierz opcję **Umiejętności**.</span><span class="sxs-lookup"><span data-stu-id="79665-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="79665-138">W polu **Dostępne charakterystyki** wprowadź umiejętność, która ma zostać wyszukana.</span><span class="sxs-lookup"><span data-stu-id="79665-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="79665-139">W polu **Typ charakterystyki** wybierz opcję **Certyfikat**.</span><span class="sxs-lookup"><span data-stu-id="79665-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="79665-140">W polu **Dostępne charakterystyki** wprowadź typ certyfikatu, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="79665-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="79665-141">Przypisz zasób projektu do projektu</span><span class="sxs-lookup"><span data-stu-id="79665-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="79665-142">Na stronie **Wszystkie projekty** wybierz projekt **XYZ uaktualnianie faza 2**.</span><span class="sxs-lookup"><span data-stu-id="79665-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="79665-143">Na karcie **Zespół projektowy i planowanie** wybierz opcję **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="79665-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="79665-144">W polu **Rola** wybierz pozycję **Członek zespołu**.</span><span class="sxs-lookup"><span data-stu-id="79665-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="79665-145">Wybierz **Rezerwuj z kalendarza**.</span><span class="sxs-lookup"><span data-stu-id="79665-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="79665-146">Na stronie **Dostępność zasobów** wybierz **Ustawienia widoku**.</span><span class="sxs-lookup"><span data-stu-id="79665-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="79665-147">Na stronie **Dostosowywanie ustawień widoku** wprowadź następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="79665-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="79665-148">**Format widoku zakresu dat:** Dzień</span><span class="sxs-lookup"><span data-stu-id="79665-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="79665-149">**Wyświetlanie opisów dostępności:** Tak</span><span class="sxs-lookup"><span data-stu-id="79665-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="79665-150">**Wyświetl wydajność pozostałą:** Tak</span><span class="sxs-lookup"><span data-stu-id="79665-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="79665-151">Na liście zasobów wybierz zasób.</span><span class="sxs-lookup"><span data-stu-id="79665-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="79665-152">Wybierz opcję **Ostateczna rezerwacja** i **Pełna dyspozycyjność**.</span><span class="sxs-lookup"><span data-stu-id="79665-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="79665-153">Przypisz zasób do roli domyślnej</span><span class="sxs-lookup"><span data-stu-id="79665-153">Assign a resource to a default role</span></span>

<span data-ttu-id="79665-154">Aby pomóc menedżerom projektów lub zasobów, można dokładniej przeanalizować zasoby, które można zarezerwować dla projektu.</span><span class="sxs-lookup"><span data-stu-id="79665-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="79665-155">Możesz skojarzyć rolę domyślną z istniejącym zasobem lub nowo nabytym zasobem.</span><span class="sxs-lookup"><span data-stu-id="79665-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="79665-156">Na przykład, kiedy Daniel został zatrudniony, posiadał doświadczenia i umiejętności umożliwiające wypełnienie roli analityka biznesowego.</span><span class="sxs-lookup"><span data-stu-id="79665-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="79665-157">Kierownik zasobów przypisał tę rolę jako domyślną rolę Daniela.</span><span class="sxs-lookup"><span data-stu-id="79665-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="79665-158">Dlatego kierownik ds. zasobów dodał Daniela do puli analityków biznesowych, którzy są dostępni do pracy nad projektami.</span><span class="sxs-lookup"><span data-stu-id="79665-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="79665-159">Podczas rezerwacji zasobów kierownicy projektów mogą filtrować zasoby ról, które są dostępne do pracy nad projektami.</span><span class="sxs-lookup"><span data-stu-id="79665-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="79665-160">Mogą one wykorzystywać te informacje jako kryterium podczas wykonywania wielokryteriówowych analiz decyzji podczas realizacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="79665-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="79665-161">W celu wyszukania zasobów z określonymi umiejętnościami, edukacją i doświadczeniem dla danego projektu mogą również dodać inne charakterystyki zasobów.</span><span class="sxs-lookup"><span data-stu-id="79665-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="79665-162">**Scenariusz:** Rozpoczął się zatwierdzony projekt, a rola starszego kierownika projektu została zarezerwowana jako planowany zasób na etapie planowania projektu.</span><span class="sxs-lookup"><span data-stu-id="79665-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="79665-163">Kierownik zasobów uzyskał teraz zasób do pełnienia roli starszego kierownika projektu.</span><span class="sxs-lookup"><span data-stu-id="79665-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="79665-164">Na stronie **Lista zasobów** wybierz pozycję **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="79665-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="79665-165">Na stronie **Rola zasobu** wybierz **Nowy**, a następnie wprowadź następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="79665-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="79665-166">**Efektywność:** wprowadź aktualną datę.</span><span class="sxs-lookup"><span data-stu-id="79665-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="79665-167">**Data wygaśnięcia:** wprowadź **nigdy**.</span><span class="sxs-lookup"><span data-stu-id="79665-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="79665-168">**Rola:** Wpisz **starszy kierownik projektu**.</span><span class="sxs-lookup"><span data-stu-id="79665-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="79665-169">Wybierz **Zapisz**, a następnie zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="79665-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="79665-170">Na karcie **kompetencje** dodaj umiejętność **ProjectMgmt** i certyfikat **PMP**.</span><span class="sxs-lookup"><span data-stu-id="79665-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]