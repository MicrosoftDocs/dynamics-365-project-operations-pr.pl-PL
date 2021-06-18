---
title: Ustawienia projektu
description: Ten temat zawiera informacje o ustawieniach zarządzania projektami.
author: ruhercul
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
ms.openlocfilehash: 24032a77834005c444972f8d234d3acb33d19135
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998334"
---
# <a name="project-settings"></a><span data-ttu-id="9ed3d-103">Ustawienia projektu</span><span class="sxs-lookup"><span data-stu-id="9ed3d-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9ed3d-104">Użyj poniższych ustawień, aby uzyskać dostęp do funkcji planowania projektów.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="9ed3d-105">Szablon pracy</span><span class="sxs-lookup"><span data-stu-id="9ed3d-105">Work template</span></span>

<span data-ttu-id="9ed3d-106">Aby utworzyć harmonogram projektu, należy utworzyć szablon kalendarza projektu, który definiuje liczbę godzin pracy w ciągu dnia i wszystkie dni wolne od pracy.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="9ed3d-107">Aby utworzyć szablon kalendarza projektu, należy skojarzyć szablon pracy z polem **Szablon kalendarza** dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="9ed3d-108">Aby utworzyć szablon pracy, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="9ed3d-109">W programie PSA w lewym okienku nawigacji kliknij pozycję **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="9ed3d-110">Na stronie listy **Zasoby** otwórz rekord użytkownika, a następnie wybierz pozycję **Pokaż godziny pracy**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9ed3d-111">Upewnij się, że zezwolono na wyświetlanie wyskakujących okienek na stronie przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="9ed3d-112">Dzięki temu będziesz widzieć godzin pracy ustawione dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="9ed3d-113">Na karcie **Widok miesięczny** kliknij opcję **Konfiguracja**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="9ed3d-114">Zostanie wyświetlona lista z trzema opcjami:</span><span class="sxs-lookup"><span data-stu-id="9ed3d-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="9ed3d-115">Nowy harmonogram tygodniowy</span><span class="sxs-lookup"><span data-stu-id="9ed3d-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="9ed3d-116">Harmonogram pracy na jeden dzień</span><span class="sxs-lookup"><span data-stu-id="9ed3d-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="9ed3d-117">Czas wolny</span><span class="sxs-lookup"><span data-stu-id="9ed3d-117">Time Off</span></span>

> ![Opcje konfigurowania](media/project-13.png)

4. <span data-ttu-id="9ed3d-119">Zaznacz opcję **Nowy harmonogram tygodniowy**, a następnie ustaw opcje dla tego harmonogramu zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="9ed3d-120">Można określić cykliczny harmonogram tygodniowy, dzienne parametry godzinowe, dni wolne od pracy itd.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="9ed3d-121">Ustaw zakres dat, kliknij przycisk **Zapisz**, a następnie kliknij przycisk **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="9ed3d-122">Wróć do strony listy **Zasoby** i wybierz zasób, dla którego ustawiono godziny pracy.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="9ed3d-123">W ustawieniu **Ustaw kalendarz jako** określ szablon pracy.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="9ed3d-124">W oknie dialogowym **Szablon pracy** nadaj nazwę szablonowi pracy, a następnie kliknij przycisk **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="9ed3d-125">Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="9ed3d-126">Role zasobu</span><span class="sxs-lookup"><span data-stu-id="9ed3d-126">Resource roles</span></span>

<span data-ttu-id="9ed3d-127">Termin *rola zasobu* odnosi się do zestawu umiejętności, kompetencji i certyfikacji koniecznych do wykonania określonego zestawu zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="9ed3d-128">Program PSA umożliwia określenie kosztów i rozliczenia czasu pracy zasobu na podstawie roli, z którą zasób jest skojarzony.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="9ed3d-129">Każda organizacja musi skonfigurować te role, korzystając z lewego okienka nawigacji w menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="9ed3d-130">Każda organizacja musi skonfigurować te role na stronie **Aktywne kategorie zasobów**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="9ed3d-131">Aby otworzyć tę stronę, w lewym okienku nawigacji wybierz pozycję **Role zasobów**.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="9ed3d-132">Cenniki</span><span class="sxs-lookup"><span data-stu-id="9ed3d-132">Price lists</span></span>

<span data-ttu-id="9ed3d-133">Cenniki umożliwiają określanie kosztów i cen sprzedaży dla ról zasobów, kategorii wydatków, produktów i innych elementów w organizacji.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="9ed3d-134">Przed utworzeniem szacunków finansowych dla prac, które muszą zostać wykonane w projekcie, należy utworzyć zapasową listę kosztów i cennik sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="9ed3d-135">W sekcji parametrów należy także skonfigurować domyślną listę kosztów i cennik sprzedaży, które mają zastosowanie do wszystkich projektów tworzonych w organizacji.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="9ed3d-136">Na stronie **Aktywne parametry projektu** upewnij się, że skonfigurowano domyślną listę kosztów i cennik sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="9ed3d-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]