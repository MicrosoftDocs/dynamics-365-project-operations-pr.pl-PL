---
title: Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i zespołu projektu
description: Ten temat zawiera informacje o rezerwowaniu ogólnych zasobów dla zadań i zespołów projektów.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754421"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="d4d17-103">Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="d4d17-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d4d17-104">Oprócz rezerwowania i przypisywania nazwanych lub rzeczywistych zasobów do projektu można również przypisywać zasoby ogólne do zadań projektu.</span><span class="sxs-lookup"><span data-stu-id="d4d17-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="d4d17-105">Te zasoby mogą służyć jako zastępcze dla zasobów nazwanych, dopóki użytkownik nie będzie gotowy do obsadzenia projektu nazwanymi zasobami.</span><span class="sxs-lookup"><span data-stu-id="d4d17-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="d4d17-106">W usłudze Project Service Automation (PSA) otwórz stronę **Projekt** na karcie **Harmonogram** wprowadź nazwę stanowiska ogólnego zasobu w komórce **Zasób** w harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="d4d17-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="d4d17-107">Alternatywnie w komórce kliknij ikonę **Zasób**, aby otworzyć selektora zasobów, a następnie wpisz nazwę zasobu ogólnego, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="d4d17-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Tworzenie i przypisywanie ogólnego członka zespołu](media/RM-how-to-9.png)

<span data-ttu-id="d4d17-109">Spowoduje to otwarcie panelu **Szybkie tworzenie: Członek zespołu projektu**.</span><span class="sxs-lookup"><span data-stu-id="d4d17-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="d4d17-110">Wprowadź rolę i jednostkę organizacyjną członka zespołu będącego zasobem ogólnym, a następnie kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="d4d17-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Szybkie tworzenie ogólnego członka zespołu](media/RM-how-to-10.png)

3. <span data-ttu-id="d4d17-112">Po utworzeniu nowego członka zespołu będącego zasobem ogólnym zostanie on przypisany do zadania.</span><span class="sxs-lookup"><span data-stu-id="d4d17-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="d4d17-113">Możesz nadal przypisywać ten zasób ogólny do innych zdań w harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="d4d17-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Przypisywanie istniejącego ogólnego członka zespołu do zadań](media/RM-how-to-11.png)

4. <span data-ttu-id="d4d17-115">Po przypisaniu ogólnego zasobu można wygenerować wymaganie zasobu i je zrealizować poprzez bezpośrednie zarezerwowanie albo przesyłając żądanie zasobu do menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4d17-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generowanie wymagania dla ogólnego członka zespołu](media/RM-how-to-12.png)

<span data-ttu-id="d4d17-117">W siatce członków zespołu można nie tylko używać selektora zasobów, jak wspomniano powyżej, ale również dodawać zasoby ogólne bezpośrednio.</span><span class="sxs-lookup"><span data-stu-id="d4d17-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="d4d17-118">Zasoby zostaną dodane z wymaganiami zasobów opartymi na datach początkowych i końcowych oraz metodzie alokacji określonej w panelu **Szybkie tworzenie: Członek zespołu projektu**.</span><span class="sxs-lookup"><span data-stu-id="d4d17-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="d4d17-119">Widać różnicę, jeśli dodasz ogólnego członka zespołu bezpośrednio, a następnie przypiszesz mu więcej zadań, niż ma on wymaganych godzin do pokrycia.</span><span class="sxs-lookup"><span data-stu-id="d4d17-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="d4d17-120">Kliknij opcję **Generuj wymaganie**, aby ponownie wygenerować wymaganie w celu zrównoważenia wymaganych godzin z przypisaniem.</span><span class="sxs-lookup"><span data-stu-id="d4d17-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="d4d17-121">Możesz także kliknąć łącze **Wymaganie zasobów** w siatce zespołu, aby otworzyć wymaganie i dodać umiejętności, preferowane zasoby itd.</span><span class="sxs-lookup"><span data-stu-id="d4d17-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Wymaganie zasobów](media/RM-how-to-13.png)

