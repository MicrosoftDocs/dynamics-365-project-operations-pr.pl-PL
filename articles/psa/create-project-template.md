---
title: Tworzeniu szablonu projektu
description: Tworzenie szablonu projektu w Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082025"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="c3990-103">Utwórz szablon projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c3990-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c3990-104">Szablony projektu pozwalają Ci zaoszczędzić czas, jeśli Twoja firma regularnie bierze udział w licytacji podobnych typów projektów.</span><span class="sxs-lookup"><span data-stu-id="c3990-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="c3990-105">Zapewniają one standardowy zestaw ról oraz szacowane godziny dla typu projektu.</span><span class="sxs-lookup"><span data-stu-id="c3990-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="c3990-106">Menedżerowie kont i menedżerowie projektów mogą tworzyć projekty na podstawie szablonu projektu lub mogą skopiować szablon i tworzyć własne.</span><span class="sxs-lookup"><span data-stu-id="c3990-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="c3990-107">Składniki szablonu projektu</span><span class="sxs-lookup"><span data-stu-id="c3990-107">Components of project template</span></span>
 <span data-ttu-id="c3990-108">Szablon projektu składa się z trzech elementów:</span><span class="sxs-lookup"><span data-stu-id="c3990-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="c3990-109">**Struktura podziału pracy** : Struktura podziału pracy w szablonie projektu ma ten sam zestaw elementów, co projekt.</span><span class="sxs-lookup"><span data-stu-id="c3990-109">**Work breakdown structure** : A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="c3990-110">Możesz utworzyć hierarchię zadań, powiązać role z zadaniem, zdefiniować atrybuty harmonogramu, ustawić zależności i wyświetlić wszystkie dane na wykresie Gantta.</span><span class="sxs-lookup"><span data-stu-id="c3990-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="c3990-111">Struktura podziału pracy w szablonach projektu obsługuje również tryby zadań dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="c3990-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="c3990-112">Podczas tworzenia harmonogramu pracy nie ma różnicy między szablonem projektu a projektem.</span><span class="sxs-lookup"><span data-stu-id="c3990-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="c3990-113">**Szacowania projektu** : Szacowania projektu w szablonach działają tak samo, jak w projektach, z takim wyjątkiem, że cenniki za domyślne koszty i ceny sprzedaży są zawsze domyślnym kosztem i cenami sprzedaży zdefiniowanymi w parametrach [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="c3990-113">**Project estimates** : Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="c3990-114">Reszta funkcji jest taka sama, jak w projekcie.</span><span class="sxs-lookup"><span data-stu-id="c3990-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="c3990-115">**Tworzenie zespołu projektu** : Podczas tworzenia zespołu projektu dla szablonu projektu, nie można dokonać rezerwacji nazwanego zasobu w szablonie.</span><span class="sxs-lookup"><span data-stu-id="c3990-115">**Project team formation** : When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="c3990-116">Można użyć **Generuj zespół projektu** w strukturze podziału pracy, aby wygenerować zestaw zasobów rodzajowych.</span><span class="sxs-lookup"><span data-stu-id="c3990-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="c3990-117">Można również określić wymagane umiejętności i poziomy biegłości dla zasobów rodzajowych.</span><span class="sxs-lookup"><span data-stu-id="c3990-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="c3990-118">Nie można zastąpić zasobu rodzajowego zasobem możliwym do zarezerwowania w szablonach projektu.</span><span class="sxs-lookup"><span data-stu-id="c3990-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="c3990-119">Utwórz projekt na podstawie szablonu</span><span class="sxs-lookup"><span data-stu-id="c3990-119">Create a project from a template</span></span>  
 <span data-ttu-id="c3990-120">Oto różne sposoby, w jakie można tworzyć projekt na podstawie szablonu:</span><span class="sxs-lookup"><span data-stu-id="c3990-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="c3990-121">Podczas tworzenia projektu z oferty, można wybrać szablon projektu w formularzu szybkiego tworzenia.</span><span class="sxs-lookup"><span data-stu-id="c3990-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="c3990-122">Podczas tworzenia projektu po kliknięciu **Nowy projekt** , formularz projektu jest wyświetlany przed zapisaniem rekordu.</span><span class="sxs-lookup"><span data-stu-id="c3990-122">When creating a project by clicking **New Project** , the project form displays before you save the record.</span></span> <span data-ttu-id="c3990-123">W tym miejscu, można kliknąć pole **Wybierz szablon** , aby wybrać z listy wstępnie zdefiniowanych szablonów projektu w organizacji.</span><span class="sxs-lookup"><span data-stu-id="c3990-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="c3990-124">Kliknij **Utwórz projekt na podstawie szablonu** na stronie **Szablon projektu** , aby utworzyć projekt z szablonu.</span><span class="sxs-lookup"><span data-stu-id="c3990-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="c3990-125">Kopiowanie elementów szablonu do projektu</span><span class="sxs-lookup"><span data-stu-id="c3990-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="c3990-126">Podczas kopiowania elementów szablonu do projektu, istnieje kilka rzeczy, o których należy wiedzieć.</span><span class="sxs-lookup"><span data-stu-id="c3990-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="c3990-127">**Kopiowanie struktury podziału pracy** : Podczas kopiowania struktury podziału pracy z szablonu projektu, jeśli projekt ma inny kalendarz projektu niż szablon, godziny pracy z kalendarza projektu zostaną zastosowane dla harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="c3990-127">**Copying a work breakdown structure** : When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="c3990-128">Dopasowuje to harmonogram do kopii kalendarza projektu.</span><span class="sxs-lookup"><span data-stu-id="c3990-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="c3990-129">Pierwsze zadanie na strukturze podziału pracy przyjmuje datę rozpoczęcia projektu, więc pozostała część harmonogramu hierarchii zadania jest aktualizowana na podstawie czasu trwania i zależności określone w strukturze podziału pracy szablonu.</span><span class="sxs-lookup"><span data-stu-id="c3990-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="c3990-130">**Kopiowanie oszacowań projektu** : Podczas kopiowania wierszy szacowania projektu, cenniki są aktualizowane na podstawie jednostki będącej właścicielem projektu dla listy koszt własny i klient dla listy cen sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="c3990-130">**Copying project estimates** : When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="c3990-131">Koszt jednostkowy i ceny sprzedaży są ustalane na podstawie tych cenników dla projektów, które są skojarzone z encją sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="c3990-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="c3990-132">**Kopiowanie członków zespołu projektu** : Podczas kopiowania członków zespołu projektu z szablonu do projektu, kopiowane są również zasoby rodzajowe, wraz z umiejętnościami i poziomami biegłości zdefiniowanymi w szablonie.</span><span class="sxs-lookup"><span data-stu-id="c3990-132">**Copying a project team** : When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="c3990-133">Przydziały zasobów rodzajowych są także obsługiwane jak w szablonie projektu.</span><span class="sxs-lookup"><span data-stu-id="c3990-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c3990-134">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="c3990-134">See Also</span></span>  
 [<span data-ttu-id="c3990-135">Przewodnik menedżera projektu</span><span class="sxs-lookup"><span data-stu-id="c3990-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
