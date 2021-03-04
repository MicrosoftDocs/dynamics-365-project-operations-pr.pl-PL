---
title: Ustawienia projektu
description: Ten temat zawiera informacje o ustawieniach zarządzania projektami.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148161"
---
# <a name="project-settings"></a><span data-ttu-id="0cc72-103">Ustawienia projektu</span><span class="sxs-lookup"><span data-stu-id="0cc72-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0cc72-104">Użyj poniższych ustawień, aby uzyskać dostęp do funkcji planowania projektów.</span><span class="sxs-lookup"><span data-stu-id="0cc72-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="0cc72-105">Szablon pracy</span><span class="sxs-lookup"><span data-stu-id="0cc72-105">Work template</span></span>

<span data-ttu-id="0cc72-106">Aby utworzyć harmonogram projektu, należy utworzyć szablon kalendarza projektu, który definiuje liczbę godzin pracy w ciągu dnia i wszystkie dni wolne od pracy.</span><span class="sxs-lookup"><span data-stu-id="0cc72-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="0cc72-107">Aby utworzyć szablon kalendarza projektu, należy skojarzyć szablon pracy z polem **Szablon kalendarza** dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="0cc72-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="0cc72-108">Aby utworzyć szablon pracy, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="0cc72-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="0cc72-109">W programie PSA w lewym okienku nawigacji kliknij pozycję **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="0cc72-110">Na stronie listy **Zasoby** otwórz rekord użytkownika, a następnie wybierz pozycję **Pokaż godziny pracy**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="0cc72-111">Upewnij się, że zezwolono na wyświetlanie wyskakujących okienek na stronie przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="0cc72-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="0cc72-112">Dzięki temu będziesz widzieć godzin pracy ustawione dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cc72-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="0cc72-113">Na karcie **Widok miesięczny** kliknij opcję **Konfiguracja**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="0cc72-114">Zostanie wyświetlona lista z trzema opcjami:</span><span class="sxs-lookup"><span data-stu-id="0cc72-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="0cc72-115">Nowy harmonogram tygodniowy</span><span class="sxs-lookup"><span data-stu-id="0cc72-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="0cc72-116">Harmonogram pracy na jeden dzień</span><span class="sxs-lookup"><span data-stu-id="0cc72-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="0cc72-117">Czas wolny</span><span class="sxs-lookup"><span data-stu-id="0cc72-117">Time Off</span></span>

> ![Opcje konfigurowania](media/project-13.png)

4. <span data-ttu-id="0cc72-119">Zaznacz opcję **Nowy harmonogram tygodniowy**, a następnie ustaw opcje dla tego harmonogramu zasobów.</span><span class="sxs-lookup"><span data-stu-id="0cc72-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="0cc72-120">Można określić cykliczny harmonogram tygodniowy, dzienne parametry godzinowe, dni wolne od pracy itd.</span><span class="sxs-lookup"><span data-stu-id="0cc72-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="0cc72-121">Ustaw zakres dat, kliknij przycisk **Zapisz**, a następnie kliknij przycisk **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="0cc72-122">Wróć do strony listy **Zasoby** i wybierz zasób, dla którego ustawiono godziny pracy.</span><span class="sxs-lookup"><span data-stu-id="0cc72-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="0cc72-123">W ustawieniu **Ustaw kalendarz jako** określ szablon pracy.</span><span class="sxs-lookup"><span data-stu-id="0cc72-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="0cc72-124">W oknie dialogowym **Szablon pracy** nadaj nazwę szablonowi pracy, a następnie kliknij przycisk **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="0cc72-125">Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.</span><span class="sxs-lookup"><span data-stu-id="0cc72-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="0cc72-126">Role zasobu</span><span class="sxs-lookup"><span data-stu-id="0cc72-126">Resource roles</span></span>

<span data-ttu-id="0cc72-127">Termin *rola zasobu* odnosi się do zestawu umiejętności, kompetencji i certyfikacji koniecznych do wykonania określonego zestawu zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="0cc72-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="0cc72-128">Program PSA umożliwia określenie kosztów i rozliczenia czasu pracy zasobu na podstawie roli, z którą zasób jest skojarzony.</span><span class="sxs-lookup"><span data-stu-id="0cc72-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="0cc72-129">Każda organizacja musi skonfigurować te role, korzystając z lewego okienka nawigacji w menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="0cc72-130">Każda organizacja musi skonfigurować te role na stronie **Aktywne kategorie zasobów**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="0cc72-131">Aby otworzyć tę stronę, w lewym okienku nawigacji wybierz pozycję **Role zasobów**.</span><span class="sxs-lookup"><span data-stu-id="0cc72-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="0cc72-132">Cenniki</span><span class="sxs-lookup"><span data-stu-id="0cc72-132">Price lists</span></span>

<span data-ttu-id="0cc72-133">Cenniki umożliwiają określanie kosztów i cen sprzedaży dla ról zasobów, kategorii wydatków, produktów i innych elementów w organizacji.</span><span class="sxs-lookup"><span data-stu-id="0cc72-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="0cc72-134">Przed utworzeniem szacunków finansowych dla prac, które muszą zostać wykonane w projekcie, należy utworzyć zapasową listę kosztów i cennik sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="0cc72-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="0cc72-135">W sekcji parametrów należy także skonfigurować domyślną listę kosztów i cennik sprzedaży, które mają zastosowanie do wszystkich projektów tworzonych w organizacji.</span><span class="sxs-lookup"><span data-stu-id="0cc72-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="0cc72-136">Na stronie **Aktywne parametry projektu** upewnij się, że skonfigurowano domyślną listę kosztów i cennik sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="0cc72-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
