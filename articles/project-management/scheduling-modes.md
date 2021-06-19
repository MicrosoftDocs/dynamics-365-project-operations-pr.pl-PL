---
title: Tryby planowania
description: Ten temat zawiera informacje o trybach planowania.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116720"
---
# <a name="scheduling-modes"></a><span data-ttu-id="21a00-103">Tryby planowania</span><span class="sxs-lookup"><span data-stu-id="21a00-103">Scheduling modes</span></span>

<span data-ttu-id="21a00-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="21a00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="21a00-105">Dynamics 365 Project Operations umożliwia organizacjom definiowanie sposobu zarządzania zmianami w kluczowych zmiennych w zadaniach w strukturze organizacyjnej pracy.</span><span class="sxs-lookup"><span data-stu-id="21a00-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="21a00-106">W zależności od konkretnych potrzeb organizacji menedżerowie projektów mogą wprowadzać zmiany w trybie planowania podczas tworzenia projektu.</span><span class="sxs-lookup"><span data-stu-id="21a00-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="21a00-107">W Project Operations dostępne są trzy tryby planowania:</span><span class="sxs-lookup"><span data-stu-id="21a00-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="21a00-108">Stały czas trwania (jest to tryb domyślny)</span><span class="sxs-lookup"><span data-stu-id="21a00-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="21a00-109">Stały nakład pracy (*Praca*)</span><span class="sxs-lookup"><span data-stu-id="21a00-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="21a00-110">Stałe jednostki</span><span class="sxs-lookup"><span data-stu-id="21a00-110">Fixed units</span></span>

<span data-ttu-id="21a00-111">Wartości, na które mają wpływ definicje określonego trybu planowania, są określane za pomocą następującej formuły:</span><span class="sxs-lookup"><span data-stu-id="21a00-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="21a00-112">Nakład pracy = Czas trwania x jednostki</span><span class="sxs-lookup"><span data-stu-id="21a00-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="21a00-113">Podczas definiowania trybu planowania projektu jest ustawiana jedna z tych wartości, której nie można już zmienić.</span><span class="sxs-lookup"><span data-stu-id="21a00-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="21a00-114">Utrzymywanie tej wartości jako stałej nadaje jej priorytet, co powiadamia system, aby nie zmieniał jej, gdy zmienią się dwie pozostałe wartości.</span><span class="sxs-lookup"><span data-stu-id="21a00-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="21a00-115">W poniższej tabeli przedstawiono informacje o wpływie wyboru konkretnego trybu.</span><span class="sxs-lookup"><span data-stu-id="21a00-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="21a00-116">**W tym zadaniu**</span><span class="sxs-lookup"><span data-stu-id="21a00-116">**In this task**</span></span>             | <span data-ttu-id="21a00-117">**Jeśli poprawiono jednostki**</span><span class="sxs-lookup"><span data-stu-id="21a00-117">**If you revise units**</span></span>   | <span data-ttu-id="21a00-118">**Jeśli poprawiono czas trwania**</span><span class="sxs-lookup"><span data-stu-id="21a00-118">**If you revise duration**</span></span> | <span data-ttu-id="21a00-119">**Jeśli poprawiono nakład pracy**</span><span class="sxs-lookup"><span data-stu-id="21a00-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="21a00-120">Zadanie — stałe jednostki</span><span class="sxs-lookup"><span data-stu-id="21a00-120">Fixed units task</span></span>     | <span data-ttu-id="21a00-121">Czas trwania jest ponownie przeliczany.</span><span class="sxs-lookup"><span data-stu-id="21a00-121">Duration is recalculated.</span></span> | <span data-ttu-id="21a00-122">Nakład pracy jest ponownie przeliczany.</span><span class="sxs-lookup"><span data-stu-id="21a00-122">Effort is recalculated.</span></span>    | <span data-ttu-id="21a00-123">Czas trwania jest ponownie przeliczany.</span><span class="sxs-lookup"><span data-stu-id="21a00-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="21a00-124">Zadanie — stały nakład pracy</span><span class="sxs-lookup"><span data-stu-id="21a00-124">Fixed effort task</span></span>    | <span data-ttu-id="21a00-125">Czas trwania jest ponownie przeliczany.</span><span class="sxs-lookup"><span data-stu-id="21a00-125">Duration is recalculated.</span></span> | <span data-ttu-id="21a00-126">Jednostki są ponownie przeliczane.</span><span class="sxs-lookup"><span data-stu-id="21a00-126">Units are recalculated.</span></span>    | <span data-ttu-id="21a00-127">Czas trwania jest ponownie przeliczany.</span><span class="sxs-lookup"><span data-stu-id="21a00-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="21a00-128">Zadanie — stały czas trwania</span><span class="sxs-lookup"><span data-stu-id="21a00-128">Fixed duration task</span></span>  | <span data-ttu-id="21a00-129">Nakład pracy jest ponownie przeliczany.</span><span class="sxs-lookup"><span data-stu-id="21a00-129">Effort is recalculated.</span></span>   | <span data-ttu-id="21a00-130">Nakład pracy jest ponownie przeliczany.</span><span class="sxs-lookup"><span data-stu-id="21a00-130">Effort is recalculated.</span></span>    | <span data-ttu-id="21a00-131">Jednostki są ponownie przeliczane.</span><span class="sxs-lookup"><span data-stu-id="21a00-131">Units are recalculated.</span></span>   |

<span data-ttu-id="21a00-132">Aby uzyskać więcej informacji dotyczących konsekwencji danego trybu, zobacz temat [Zmiana typu zadania w celu dokładniejszego planowania](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="21a00-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="21a00-133">W tym temacie termin **Praca** jest używany zamiast terminu **Nakład pracy**.</span><span class="sxs-lookup"><span data-stu-id="21a00-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="21a00-134">Zmienianie trybu planowania organizacji</span><span class="sxs-lookup"><span data-stu-id="21a00-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="21a00-135">Wykonaj następujące kroki, aby zdefiniować tryb planowania organizacji.</span><span class="sxs-lookup"><span data-stu-id="21a00-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="21a00-136">Wybierz **Ustawienia** \> **Ogólne** \> **Parametry**, a następnie wybierz parametr projektowy.</span><span class="sxs-lookup"><span data-stu-id="21a00-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="21a00-137">Na stronie **Parametry projektu** wybierz domyślny tryb planowania dla organizacji, a następnie zdefiniuj możliwość zastępowania ustawienia przez menedżera projektu podczas tworzenia nowego projektu.</span><span class="sxs-lookup"><span data-stu-id="21a00-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="21a00-138">Zmienianie ustawienia trybu planowania w projekcie</span><span class="sxs-lookup"><span data-stu-id="21a00-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="21a00-139">Jeśli organizacja zezwala menedżerowi projektu na zastępowanie domyślnego trybu planowania, menedżer projektu może dokonać tej zmiany podczas tworzenia nowego projektu.</span><span class="sxs-lookup"><span data-stu-id="21a00-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="21a00-140">Jednak po zapisaniu projektu nie można zmienić trybu planowania.</span><span class="sxs-lookup"><span data-stu-id="21a00-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="21a00-141">Skopiowane projekty</span><span class="sxs-lookup"><span data-stu-id="21a00-141">Copied projects</span></span>

<span data-ttu-id="21a00-142">Ponieważ projekt jest tworzony po utworzeniu akcji kopiowania, menedżer projektu nie może ustawić trybu planowania.</span><span class="sxs-lookup"><span data-stu-id="21a00-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="21a00-143">Projekt docelowy będzie zawsze domyślnie ustawiony na tryb zdefiniowany na poziomie organizacyjnym.</span><span class="sxs-lookup"><span data-stu-id="21a00-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="21a00-144">Skopiowane zadania</span><span class="sxs-lookup"><span data-stu-id="21a00-144">Copied tasks</span></span>

<span data-ttu-id="21a00-145">Po skopiowaniu zadania z jednego projektu do innego zadanie dziedziczy tryb planowania docelowego projektu.</span><span class="sxs-lookup"><span data-stu-id="21a00-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
