---
title: Szablony projektów
description: W tym temacie przedstawiono informacje na temat korzystania z szablonów projektów w celu szybkiego konfigurowania projektów.
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
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998289"
---
# <a name="project-templates"></a><span data-ttu-id="618bb-103">Szablony projektów</span><span class="sxs-lookup"><span data-stu-id="618bb-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="618bb-104">Szablon projektu to wstępnie zdefiniowana struktura, która pomaga szybko i łatwo rozpocząć pracę nad projektem.</span><span class="sxs-lookup"><span data-stu-id="618bb-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="618bb-105">Można użyć wstępnie zdefiniowanego szablonu w celu utworzenia nowego projektu jednym kliknięciem.</span><span class="sxs-lookup"><span data-stu-id="618bb-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="618bb-106">Tak jak w przypadku projektów, dla szablonów projektów należy zdefiniować wymagania wstępne.</span><span class="sxs-lookup"><span data-stu-id="618bb-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="618bb-107">Należy zdefiniować kalendarz projektu dla każdego szablonu projektu, a w organizacji muszą być wstępnie zdefiniowane role i cenniki, tak aby składniki szablonu miały użyteczne dane.</span><span class="sxs-lookup"><span data-stu-id="618bb-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="618bb-108">Szablon projektu zawiera trzy składniki: harmonogram, oszacowania projektu i członków zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="618bb-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="618bb-109">Zaplanuj</span><span class="sxs-lookup"><span data-stu-id="618bb-109">Schedule</span></span>

<span data-ttu-id="618bb-110">Harmonogram w szablonie projektu ma taki sam zestaw elementów, jak harmonogram w projekcie.</span><span class="sxs-lookup"><span data-stu-id="618bb-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="618bb-111">Możesz utworzyć hierarchię zadań, powiązać role z zadaniami, zdefiniować atrybuty harmonogramu oraz ustawić zależności.</span><span class="sxs-lookup"><span data-stu-id="618bb-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="618bb-112">Harmonogram w szablonie projektu obsługuje również tryby zadań dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="618bb-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="618bb-113">W związku z tym obsługuje aparat planowania.</span><span class="sxs-lookup"><span data-stu-id="618bb-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="618bb-114">Z projektem należy skojarzyć kalendarz projektu.</span><span class="sxs-lookup"><span data-stu-id="618bb-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="618bb-115">Podczas tworzenia harmonogramu pracy nie ma różnicy między szablonem projektu a projektem.</span><span class="sxs-lookup"><span data-stu-id="618bb-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="618bb-116">Szacowania projektu</span><span class="sxs-lookup"><span data-stu-id="618bb-116">Project estimates</span></span>

<span data-ttu-id="618bb-117">Szacunki projektu w szablonie projektu działają tak samo, jak szacunki projektu w projekcie.</span><span class="sxs-lookup"><span data-stu-id="618bb-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="618bb-118">Różnica polega na tym, że koszty własne i ceny sprzedaży są pobierane z domyślnych list kosztów własnych i cenników sprzedaży zdefiniowanych w parametrach.</span><span class="sxs-lookup"><span data-stu-id="618bb-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="618bb-119">Tworzenie projektu na podstawie szablonu</span><span class="sxs-lookup"><span data-stu-id="618bb-119">Creating a project from a template</span></span>
 
<span data-ttu-id="618bb-120">Istnieje kilka sposobów utworzenia projektu na podstawie szablonu projektu:</span><span class="sxs-lookup"><span data-stu-id="618bb-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="618bb-121">Podczas tworzenia projektu z oferty można wybrać szablon projektu w oknie dialogowym **Szybkie tworzenie: Projekt**.</span><span class="sxs-lookup"><span data-stu-id="618bb-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Okno dialogowe Szybkie tworzenie: Projekt](media/project-11.png)

- <span data-ttu-id="618bb-123">Podczas tworzenia projektu przez wybranie opcji **Nowy projekt** strona **Projektu** jest wyświetlana przed zapisaniem rekordu.</span><span class="sxs-lookup"><span data-stu-id="618bb-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="618bb-124">W polu **Wybierz szablon** wybierz jeden ze wstępnie zdefiniowanych szablonów projektów istniejących w organizacji.</span><span class="sxs-lookup"><span data-stu-id="618bb-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="618bb-125">Użycie opcji **Utwórz projekt na podstawie szablonu** na stronie **Encja Szablon**.</span><span class="sxs-lookup"><span data-stu-id="618bb-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="618bb-126">Kopiowanie elementów szablonu do projektu</span><span class="sxs-lookup"><span data-stu-id="618bb-126">Copying components of template to project</span></span>

<span data-ttu-id="618bb-127">Podczas kopiowania składników szablonu projektu do projektu mogą nastąpić pewne zastąpienia, zależnie od ustawień w projekcie.</span><span class="sxs-lookup"><span data-stu-id="618bb-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="618bb-128">Kopiowanie harmonogramu</span><span class="sxs-lookup"><span data-stu-id="618bb-128">Copying the schedule</span></span>

<span data-ttu-id="618bb-129">Jeśli podczas kopiowania harmonogramu z szablonu projektu projekt ma inny kalendarz projektu niż szablon, godziny pracy z kalendarza projektu zostaną zastosowane do harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="618bb-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="618bb-130">W ten sposób harmonogram zostanie dopasowany do kopii kalendarza projektu.</span><span class="sxs-lookup"><span data-stu-id="618bb-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="618bb-131">Analogicznie pierwsze zadanie w harmonogramie przyjmuje datę rozpoczęcia projektu, a harmonogram pozostałej części hierarchii jest aktualizowany na podstawie czasu trwania i zależności określonych w szablonie.</span><span class="sxs-lookup"><span data-stu-id="618bb-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="618bb-132">Kopiowanie szacowań projektów</span><span class="sxs-lookup"><span data-stu-id="618bb-132">Copying project estimates</span></span> 

<span data-ttu-id="618bb-133">Podczas kopiowania między wierszami szacowania projektu są aktualizowane cenniki.</span><span class="sxs-lookup"><span data-stu-id="618bb-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="618bb-134">W przypadku listy kosztów własnych te aktualizacje bazują na jednostce będącej właścicielem projektu.</span><span class="sxs-lookup"><span data-stu-id="618bb-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="618bb-135">Dla cennika sprzedaży bazują na odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="618bb-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="618bb-136">W projektach skojarzonych z encją sprzedaży koszt jednostkowy i ceny sprzedaży są ustalane na podstawie tych cenników.</span><span class="sxs-lookup"><span data-stu-id="618bb-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="618bb-137">Kopiowanie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="618bb-137">Copying a project team</span></span>

<span data-ttu-id="618bb-138">Podczas kopiowania zespołu projektu z szablonu projektu do projektu kopiowane są zasoby ogólne wraz z umiejętnościami i poziomami biegłości zdefiniowanymi w szablonie.</span><span class="sxs-lookup"><span data-stu-id="618bb-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="618bb-139">Przypisania zasobów ogólnych są także obsługiwane jak w szablonie projektu.</span><span class="sxs-lookup"><span data-stu-id="618bb-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="618bb-140">Nazwane zasoby nie są obsługiwane w szablonach projektów.</span><span class="sxs-lookup"><span data-stu-id="618bb-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]