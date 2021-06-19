---
title: Kopiowanie projektu
description: Ten temat zawiera informacje o kopiowaniu projektów w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091267"
---
# <a name="copy-a-project"></a><span data-ttu-id="c447a-103">Kopiowanie projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-103">Copy a project</span></span>

<span data-ttu-id="c447a-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="c447a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c447a-105">Za pomocą programu Dynamics 365 Project Operations można szybko tworzyć nowe projekty, wybierając pozycję **Kopiuj projekt** w formularzu **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="c447a-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="c447a-106">Aby skopiować projekt, otwórz go, a następnie wybierz opcję **Kopiuj projekt**.</span><span class="sxs-lookup"><span data-stu-id="c447a-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="c447a-107">Czynność ta skopiuje:</span><span class="sxs-lookup"><span data-stu-id="c447a-107">The action will copy the following:</span></span>

- <span data-ttu-id="c447a-108">Właściwości projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-108">Project properties</span></span> 
- <span data-ttu-id="c447a-109">Struktura podziału pracy</span><span class="sxs-lookup"><span data-stu-id="c447a-109">Work breakdown structure</span></span>
- <span data-ttu-id="c447a-110">Członkowie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-110">Project team members</span></span>
- <span data-ttu-id="c447a-111">Szacowania projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-111">Project estimates</span></span>
- <span data-ttu-id="c447a-112">Szacunki kosztów projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-112">Project expense estimates</span></span>
- <span data-ttu-id="c447a-113">Oszacowanie materiałów projektowych</span><span class="sxs-lookup"><span data-stu-id="c447a-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="c447a-114">Właściwości projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-114">Project properties</span></span>

<span data-ttu-id="c447a-115">Podczas kopiowania projektu są kopiowane wartości z następujących pól:</span><span class="sxs-lookup"><span data-stu-id="c447a-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="c447a-116">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="c447a-116">Name</span></span>
- <span data-ttu-id="c447a-117">Opis</span><span class="sxs-lookup"><span data-stu-id="c447a-117">Description</span></span>
- <span data-ttu-id="c447a-118">Klient</span><span class="sxs-lookup"><span data-stu-id="c447a-118">Customer</span></span>
- <span data-ttu-id="c447a-119">Szablon kalendarza</span><span class="sxs-lookup"><span data-stu-id="c447a-119">Calendar Template</span></span>
- <span data-ttu-id="c447a-120">Waluta</span><span class="sxs-lookup"><span data-stu-id="c447a-120">Currency</span></span>
- <span data-ttu-id="c447a-121">Jednostka kontraktująca</span><span class="sxs-lookup"><span data-stu-id="c447a-121">Contracting Unit</span></span>
- <span data-ttu-id="c447a-122">Menedżer projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-122">Project Manager</span></span>
- <span data-ttu-id="c447a-123">Status</span><span class="sxs-lookup"><span data-stu-id="c447a-123">Status</span></span>
- <span data-ttu-id="c447a-124">Ogólny stan projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-124">Overall Project Status</span></span>
- <span data-ttu-id="c447a-125">Komentarze</span><span class="sxs-lookup"><span data-stu-id="c447a-125">Comments</span></span>
- <span data-ttu-id="c447a-126">Szacunki</span><span class="sxs-lookup"><span data-stu-id="c447a-126">Estimates</span></span>
- <span data-ttu-id="c447a-127">Szacowana data rozpoczęcia: Jest to data, kiedy projekt zostanie utworzony z kopii.</span><span class="sxs-lookup"><span data-stu-id="c447a-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="c447a-128">Szacowana data zakończenia: Ta data jest dostosowywana na podstawie daty rozpoczęcia nowego projektu, który został wykonany na podstawie kopii.</span><span class="sxs-lookup"><span data-stu-id="c447a-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="c447a-129">Nakład pracy (godziny)</span><span class="sxs-lookup"><span data-stu-id="c447a-129">Effort (Hours)</span></span>
- <span data-ttu-id="c447a-130">Szacowany koszt robocizny</span><span class="sxs-lookup"><span data-stu-id="c447a-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="c447a-131">Szacowany koszt wydatków</span><span class="sxs-lookup"><span data-stu-id="c447a-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="c447a-132">Szacowany koszt materiałowy</span><span class="sxs-lookup"><span data-stu-id="c447a-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="c447a-133">Kopiowanie projektu to operacja, która trwa długi czas.</span><span class="sxs-lookup"><span data-stu-id="c447a-133">Copy project is a long running operation.</span></span> <span data-ttu-id="c447a-134">Kopiowane są również rekordy projektu, ich odpowiednie atrybuty oraz wiele powiązanych z nimi encji.</span><span class="sxs-lookup"><span data-stu-id="c447a-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="c447a-135">Ze względu na długi czas trwania operacji, po rozpoczęciu kopiowania docelowa strona projektu jest zablokowana do edycji aż do zakończenia operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="c447a-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="c447a-136">Struktura podziału pracy</span><span class="sxs-lookup"><span data-stu-id="c447a-136">Work breakdown structure</span></span>

<span data-ttu-id="c447a-137">Podczas kopiowania projektu zostanie skopiowana cała struktura podziału prac załadowana do zasobu.</span><span class="sxs-lookup"><span data-stu-id="c447a-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="c447a-138">Nazwane zasoby zostaną zastąpione zasobami ogólnymi.</span><span class="sxs-lookup"><span data-stu-id="c447a-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="c447a-139">Jeśli nazwane zasoby nie korzystają z takich samych godzin pracy, jak zasób ogólny, harmonogram zostanie ponownie obliczony, a czas trwania zadań mogą ulec zmianie.</span><span class="sxs-lookup"><span data-stu-id="c447a-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="c447a-140">Członkowie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="c447a-140">Project team members</span></span>

<span data-ttu-id="c447a-141">W przypadku kopiowania zespołu projektu z projektu źródłowego, zasoby ogólne zostaną także skopiowane.</span><span class="sxs-lookup"><span data-stu-id="c447a-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="c447a-142">Przypisania zasobów ogólnych są także obsługiwane jak w projekcie źródłowym.</span><span class="sxs-lookup"><span data-stu-id="c447a-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="c447a-143">Nazwane zasoby zostaną przekonwertowane dla ogólnych członków zespołu.</span><span class="sxs-lookup"><span data-stu-id="c447a-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="c447a-144">Szacunki</span><span class="sxs-lookup"><span data-stu-id="c447a-144">Estimates</span></span>

<span data-ttu-id="c447a-145">Podczas kopiowania projektu z projektu źródłowego kopiowane są wiersze kosztorysu zasobów, wydatków i materiałów.</span><span class="sxs-lookup"><span data-stu-id="c447a-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="c447a-146">Informacje na temat sposobu programowego uzyskiwania dostępu do kopiowania projektów można znaleźć w artykule [projektowanie szablonów projektów przy użyciu narzędzia do kopiowania projektów](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="c447a-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
