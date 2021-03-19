---
title: Tworzenie zespołu projektu
description: W tym temacie zamieszczono informacje dotyczące tworzenia nowego zespołu projektu i zarządzania nim.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270871"
---
# <a name="create-a-project-team"></a><span data-ttu-id="ffe9d-103">Tworzenie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="ffe9d-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffe9d-104">Aby użyć ról, które zostały wcześniej skonfigurowane w projekcie, kierownik projektu musi skojarzyć role z projektem.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="ffe9d-105">Do danego projektu można przypisać wiele ról.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="ffe9d-106">W celu uniknięcia niejasności te role są automatycznie oznaczane podczas rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="ffe9d-107">Na przykład, jeśli kierownik projektu wymaga trzech inżynierów oprogramowania, trzy role inżyniera oprogramowania, których etykiety mają **inżyniera oprogramowania 1**, **inżyniera oprogramowania 2** i **inżyniera oprogramowania 3**, są generowane automatycznie.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="ffe9d-108">Jeśli właściwości roli zostały wcześniej ustawione dla roli, są one stosowane jako filtr podczas wyszukiwania zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="ffe9d-109">Dodatkowe charakterystyki można dodać w zależności od potrzeb, aby dokładniej uściślić wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="ffe9d-110">Ustawienia widoku mogą być również dostosowywane w celu lepszego wyświetlenia dostępności zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="ffe9d-111">Dostępne są opcje umożliwiające pokazanie godzinowych, dziennych, tygodniowych, miesięcznych i rocznych oraz rocznej dostępności.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="ffe9d-112">Istnieje również możliwość wyświetlenia dostępnej i pozostałej wydajności zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="ffe9d-113">Ta opcja jest przydatna przy szacowaniu czasu dostępności, kiedy oceniany jest dostępny czas na działania lub dostępność zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="ffe9d-114">Kierownik projektu może wybrać rolę na stronie, a następnie, jeśli dostępny jest zasób, który spełnia wymagania, może zarezerwować zasób do wypełnienia roli.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="ffe9d-115">Należy pamiętać, że zasoby nie muszą być rezerwowane w tym punkcie etapu planowania.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="ffe9d-116">Podczas tworzenia SPP można zastępować role przy użyciu zasobów pracowniczych dla danego projektu.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="ffe9d-117">Jeśli role zostaną zamienione na zasoby służbowe w SPP, konfiguracja zasobu powoduje automatyczne zaktualizowanie listy i harmonogramu planowania zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="ffe9d-118">[![Lista zespołu projektowego zawierająca zarówno role, jak i rzeczywiste zasoby](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="ffe9d-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="ffe9d-119">Menedżer projektu ma różne opcje rezerwacji zasobu, takie jak **Wydajność pozostała**, **Pełna wydajność**, **Procent wydajności** i **Określona liczba godzin**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="ffe9d-120">Te opcje rezerwacji można anulować w dowolnym momencie, jeśli zmienią się przydziały zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="ffe9d-121">Obsługiwane są dwa typy rezerwacji:</span><span class="sxs-lookup"><span data-stu-id="ffe9d-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="ffe9d-122">**Rezerwacja ostateczna** — Rezerwacja zasobów została zatwierdzona i potwierdzona do pracy nad zaangażowaniem przez określony czas.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="ffe9d-123">**Wstępna rezerwacja** — Rezerwacje zasobów zostały wstępnie ustawione do pracy nad zaangażowaniem przez określony czas.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="ffe9d-124">Poniższa procedura wyjaśnia, jak utworzyć zespół projektowy.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="ffe9d-125">Tworzenie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="ffe9d-125">Create a project team</span></span>

1. <span data-ttu-id="ffe9d-126">Na stronie lista **Wszystkie projekty** wybierz projekt, a następnie wybierz pozycję **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="ffe9d-127">Na karcie **Zespół projektowy i planowanie** w polu **Data zakończenia harmonogramu** wprowadź datę rozpoczęcia harmonogramu plus jeden miesiąc.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="ffe9d-128">Jeśli na przykład Data rozpoczęcia planowania wynosi 24 czerwca 2017 (24/06/2017), wprowadź **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="ffe9d-129">Wybierz **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-129">Select **Add**.</span></span>
4. <span data-ttu-id="ffe9d-130">W okienku **Dodaj role do projektu**, w polu **Rola** wybierz pozycję **Starszy kierownik projektu**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="ffe9d-131">Wybierz **Wymagane kompetencje**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="ffe9d-132">Na stronie **Wybierz cechy** cechy, które zostały wcześniej ustawione dla roli starszego kierownika projektu, są zaznaczone domyślnie.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="ffe9d-133">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-133">Select **OK**.</span></span>
7. <span data-ttu-id="ffe9d-134">Na stronie **Dodawanie ról do projektu**, w polu **Liczba zasobów**, wprowadź wartość **1**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="ffe9d-135">W polu **Zasób** jest wyświetlane wszystkie zasoby o wymaganych kwalifikacjach.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="ffe9d-136">Wybierz opcję **Daniel Goldschmidt**, a następnie wybierz pozycję **Utwórz**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="ffe9d-137">Na stronie **Projekt** wybierz opcję **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="ffe9d-138">W okienku **Dodaj role do projektu**, w polu **Rola** wybierz pozycję **Członek zespołu**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="ffe9d-139">W polu **Liczba zasobów** wprowadź liczbę **5**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="ffe9d-140">Wybierz pozycję **Utwórz**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-140">Select **Create**.</span></span>
12. <span data-ttu-id="ffe9d-141">Na stronie **Projekty** wybierz pozycję **Spełniaj zasoby**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="ffe9d-142">Monitoruj zespoły projektów</span><span class="sxs-lookup"><span data-stu-id="ffe9d-142">Monitor project teams</span></span>
1. <span data-ttu-id="ffe9d-143">Na stronie **Wszystkie projekty** wybierz łącze **Identyfikator projektu** dla projektu **XYZ uaktualnianie faza 2**.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="ffe9d-144">Na skróconej karcie **Zespół projektowy i planowanie** sprawdź, czy wymienione zasoby projektu są poprawne.</span><span class="sxs-lookup"><span data-stu-id="ffe9d-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]