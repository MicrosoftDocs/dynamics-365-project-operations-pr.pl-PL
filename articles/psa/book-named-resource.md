---
title: Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów
description: Ta temat zawiera informacje o rezerwowaniu nazwanych zasobów na potrzeby ogólnego wymagania zasobu.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291047"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="611cd-103">Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="611cd-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="611cd-104">Można użyć nazwanego zasobu, aby zastąpić ogólny zasób mający wymaganie zasobu.</span><span class="sxs-lookup"><span data-stu-id="611cd-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="611cd-105">W usłudze Project Service Automation (PSA) na stronie **Projekty** kliknij kartę **Zespół**.</span><span class="sxs-lookup"><span data-stu-id="611cd-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="611cd-106">Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="611cd-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="611cd-107">Możesz też otworzyć wymaganie zasobu, a następnie kliknąć przycisk **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="611cd-107">Or, open the resource requirement and then click **Book**.</span></span>


![Rezerwowanie ogólnego członka zespołu](media/RM-how-to-14.png)


3. <span data-ttu-id="611cd-109">Na stronie **Asystent planowania** wybierz nazwany zasób, który ma zostać zarezerwowany do Twojego zespołu projektu, a następnie kliknij opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="611cd-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Rezerwowanie ogólnego członka zespołu przy użyciu Asystenta planowania](media/RM-how-to-15.png)

<span data-ttu-id="611cd-111">Gdy rezerwacja jest zakończona i zaspokojona przez nazwany zasób, zasób ogólny jest zastępowany nazwanym zasobem.</span><span class="sxs-lookup"><span data-stu-id="611cd-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Nazwany członek zespołu zastępujący ogólnego członka zespołu](media/RM-how-to-16.png)

<span data-ttu-id="611cd-113">Również przypisania w harmonogramie zostaną zaktualizowane o nazwany zasób.</span><span class="sxs-lookup"><span data-stu-id="611cd-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Nazwany członek zespołu projektu przypisany do zadań projektu](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="611cd-115">Wypełnianie roli ogólnego zasobu wieloma nazwanym zasobami</span><span class="sxs-lookup"><span data-stu-id="611cd-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="611cd-116">Zaspokojenie wymagania na zasób ogólny za pomocą wielu nazwanych zasobów przypomina operację przypisania jednego nazwanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="611cd-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="611cd-117">Załóżmy na przykład, że istnieje zadanie o czasie trwania pięć dni i nakładzie pracy 120 godzin.</span><span class="sxs-lookup"><span data-stu-id="611cd-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="611cd-118">Tego zadania nie może wykonać jeden zasób pracujący na typowej ośmiogodzinnej zmianie w pięciodniowym tygodniu pracy.</span><span class="sxs-lookup"><span data-stu-id="611cd-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Zadanie wymagające 120 godzin pracy przez pięć dni](media/RM-how-to-21.png)

<span data-ttu-id="611cd-120">Wymaganie opiewa na 120 godzin pracy inżynieryjnej przy robotach przez pięć dni, co oznacza 24 godziny na dobę.</span><span class="sxs-lookup"><span data-stu-id="611cd-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Wymaganie na dzień](media/RM-how-to-22.png)

<span data-ttu-id="611cd-122">Jest to przykład sytuacji, kiedy do zaspokojenia żądania zasobu ogólnego potrzeba wielu nazwanych zasobów.</span><span class="sxs-lookup"><span data-stu-id="611cd-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="611cd-123">W celu zrealizowania tego zapotrzebowania trzeba zarezerwować wiele zasobów.</span><span class="sxs-lookup"><span data-stu-id="611cd-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Rezerwowanie wielu zasobów w celu zaspokojenia wymagania](media/RM-how-to-23.png)

<span data-ttu-id="611cd-125">Główna różnica w tym scenariuszu polega na tym, że zasób ogólny pozostaje w zespole przypisanym do zadania, a członkowie zespołu będący zarezerwowanymi zasobami nazwanymi nie są przypisywani do zadania w ramach ich standardowych obowiązków.</span><span class="sxs-lookup"><span data-stu-id="611cd-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="611cd-126">Menedżer projektu może odpowiednio przypisać pracę do nazwanych zasobów.</span><span class="sxs-lookup"><span data-stu-id="611cd-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="611cd-127">Widok **Uzgadnianie** może pomóc menedżerowi projektu podzielić rezerwacje między wiele zasobów i przypisać im zadanie.</span><span class="sxs-lookup"><span data-stu-id="611cd-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="611cd-128">Nie jest to wykonywane automatycznie, ponieważ w każdym scenariuszu bardziej skomplikowanym niż ten powyżej, na przykład gdy użytkownik ma pakiet zadań składających się na wymaganie, system musi uwzględnić sposób, w jaki Menedżer projektu zamierza dokonywać przypisań.</span><span class="sxs-lookup"><span data-stu-id="611cd-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="611cd-129">Ponieważ system nie jest w stanie zrozumieć zamierzeń, założenia mogą być inne niż zamierzania i może wystąpić nieprawidłowy lub nieprzewidywalny rezultat.</span><span class="sxs-lookup"><span data-stu-id="611cd-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="611cd-130">Przewidywany wynik jest taki, że zasób ogólny pozostanie przypisany do czasu, aż menedżer projektu jednoznacznie utworzyć przypisania za pomocą widoku **Uzgadnianie**.</span><span class="sxs-lookup"><span data-stu-id="611cd-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]