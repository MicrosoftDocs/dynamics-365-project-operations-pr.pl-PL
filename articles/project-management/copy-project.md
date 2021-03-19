---
title: Kopiowanie projektu
description: Ten temat zawiera informacje o kopiowaniu projektów w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479532"
---
# <a name="copy-a-project"></a><span data-ttu-id="47cd8-103">Kopiowanie projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-103">Copy a project</span></span>

<span data-ttu-id="47cd8-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="47cd8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47cd8-105">Za pomocą programu Dynamics 365 Project Operations można szybko tworzyć nowe projekty, wybierając pozycję **Kopiuj projekt** w formularzu **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="47cd8-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="47cd8-106">Aby skopiować projekt, otwórz go, a następnie wybierz opcję **Kopiuj projekt**.</span><span class="sxs-lookup"><span data-stu-id="47cd8-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="47cd8-107">Zostaną skopiowane następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="47cd8-107">The action will copy:</span></span>

- <span data-ttu-id="47cd8-108">Właściwości projektu (szacowana data rozpoczęcia jest kopiowana z projektu źródłowego)</span><span class="sxs-lookup"><span data-stu-id="47cd8-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="47cd8-109">Struktura podziału pracy</span><span class="sxs-lookup"><span data-stu-id="47cd8-109">The Work breakdown structure</span></span>
- <span data-ttu-id="47cd8-110">Członkowie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-110">Project team members</span></span>
- <span data-ttu-id="47cd8-111">Szacowania projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-111">Project estimates</span></span>
- <span data-ttu-id="47cd8-112">Szacunki kosztów projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="47cd8-113">Właściwości projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-113">Project properties</span></span>

<span data-ttu-id="47cd8-114">Podczas kopiowania projektu są kopiowane wartości z następujących pól:</span><span class="sxs-lookup"><span data-stu-id="47cd8-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="47cd8-115">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="47cd8-115">Name</span></span>
- <span data-ttu-id="47cd8-116">Opis</span><span class="sxs-lookup"><span data-stu-id="47cd8-116">Description</span></span>
- <span data-ttu-id="47cd8-117">Klient</span><span class="sxs-lookup"><span data-stu-id="47cd8-117">Customer</span></span>
- <span data-ttu-id="47cd8-118">Szablon kalendarza</span><span class="sxs-lookup"><span data-stu-id="47cd8-118">Calendar Template</span></span>
- <span data-ttu-id="47cd8-119">Waluta</span><span class="sxs-lookup"><span data-stu-id="47cd8-119">Currency</span></span>
- <span data-ttu-id="47cd8-120">Jednostka kontraktująca</span><span class="sxs-lookup"><span data-stu-id="47cd8-120">Contracting Unit</span></span>
- <span data-ttu-id="47cd8-121">Menedżer projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-121">Project Manager</span></span>
- <span data-ttu-id="47cd8-122">Status</span><span class="sxs-lookup"><span data-stu-id="47cd8-122">Status</span></span>
- <span data-ttu-id="47cd8-123">Ogólny stan projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-123">Overall Project Status</span></span>
- <span data-ttu-id="47cd8-124">Komentarze</span><span class="sxs-lookup"><span data-stu-id="47cd8-124">Comments</span></span>
- <span data-ttu-id="47cd8-125">Szacunki</span><span class="sxs-lookup"><span data-stu-id="47cd8-125">Estimates</span></span>
- <span data-ttu-id="47cd8-126">Szacowana data rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="47cd8-126">Estimated Start Date</span></span>
- <span data-ttu-id="47cd8-127">Data zakończenia</span><span class="sxs-lookup"><span data-stu-id="47cd8-127">Finish Date</span></span>
- <span data-ttu-id="47cd8-128">Nakład pracy (godziny)</span><span class="sxs-lookup"><span data-stu-id="47cd8-128">Effort (Hours)</span></span>
- <span data-ttu-id="47cd8-129">Szacowany koszt robocizny</span><span class="sxs-lookup"><span data-stu-id="47cd8-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="47cd8-130">Szacowany koszt wydatków</span><span class="sxs-lookup"><span data-stu-id="47cd8-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="47cd8-131">Struktura podziału pracy</span><span class="sxs-lookup"><span data-stu-id="47cd8-131">Work breakdown structure</span></span>

<span data-ttu-id="47cd8-132">Podczas kopiowania projektu zostanie skopiowana cała struktura podziału prac załadowana do zasobu.</span><span class="sxs-lookup"><span data-stu-id="47cd8-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="47cd8-133">Nazwane zasoby zostaną zastąpione zasobami ogólnymi.</span><span class="sxs-lookup"><span data-stu-id="47cd8-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="47cd8-134">Jeśli nazwane zasoby nie korzystają z takich samych godzin pracy, jak zasób ogólny, harmonogram zostanie ponownie obliczony, a czas trwania zadań mogą ulec zmianie.</span><span class="sxs-lookup"><span data-stu-id="47cd8-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="47cd8-135">Członkowie zespołu projektu</span><span class="sxs-lookup"><span data-stu-id="47cd8-135">Project team members</span></span>

<span data-ttu-id="47cd8-136">W przypadku kopiowania zespołu projektu z projektu źródłowego, zasoby ogólne zostaną także skopiowane.</span><span class="sxs-lookup"><span data-stu-id="47cd8-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="47cd8-137">Przypisania zasobów ogólnych są także obsługiwane jak w projekcie źródłowym.</span><span class="sxs-lookup"><span data-stu-id="47cd8-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="47cd8-138">Nazwane zasoby zostaną przekonwertowane dla ogólnych członków zespołu.</span><span class="sxs-lookup"><span data-stu-id="47cd8-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="47cd8-139">Szacunki</span><span class="sxs-lookup"><span data-stu-id="47cd8-139">Estimates</span></span>

<span data-ttu-id="47cd8-140">Po skopiowaniu projektu wiersze szacowania zasobu i wydatku są kopiowane z projektu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="47cd8-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="47cd8-141">Informacje na temat sposobu programowego uzyskiwania dostępu do kopiowania projektów można znaleźć w artykule [projektowanie szablonów projektów przy użyciu narzędzia do kopiowania projektów](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="47cd8-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
