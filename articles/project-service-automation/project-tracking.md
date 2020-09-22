---
title: Postępu projektu i poniesione koszty
description: W tym temat zamieszczono informacje dotyczące śledzenia postępu i zużycia kosztów w programie project.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754384"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="05c09-103">Postępu projektu i poniesione koszty</span><span class="sxs-lookup"><span data-stu-id="05c09-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="05c09-104">Konieczność śledzenia postępu w harmonogramie zależy od branży.</span><span class="sxs-lookup"><span data-stu-id="05c09-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="05c09-105">Niektóre branże są śledzone na niższym poziomie szczegółowości, podczas gdy inne branże śledzone są na wyższym poziomie.</span><span class="sxs-lookup"><span data-stu-id="05c09-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="05c09-106">W tym temat pokazano, jak planować w celu spełnienia wymagań organizacji.</span><span class="sxs-lookup"><span data-stu-id="05c09-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="05c09-107">Widok Śledzenie nakładu pracy</span><span class="sxs-lookup"><span data-stu-id="05c09-107">Effort tracking view</span></span>

<span data-ttu-id="05c09-108">W widoku **Śledzenie nakładu pracy** są śledzone postępy zadań w harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="05c09-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="05c09-109">Porównuje rzeczywisty nakład godzin pracy spędzonych nad zadaniem z planowanym nakładem pracy w godzinach dla zadania.</span><span class="sxs-lookup"><span data-stu-id="05c09-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="05c09-110">Korzystając z poniższych formuł, program PSA obliczy metryki śledzenia:</span><span class="sxs-lookup"><span data-stu-id="05c09-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="05c09-111">Procent postęp = rzeczywisty nakład pracy do dnia dzisiejszego ÷ planowany nakład pracy dla zadania</span><span class="sxs-lookup"><span data-stu-id="05c09-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="05c09-112">Szacowane do zakończenia (ETC) = planowany nakład pracy — rzeczywisty nakład pracy do dnia dzisiejszego</span><span class="sxs-lookup"><span data-stu-id="05c09-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="05c09-113">Szacowane przy zakończeniu (SPZ) = pozostały nakład pracy + rzeczywisty nakład pracy do dnia dzisiejszego</span><span class="sxs-lookup"><span data-stu-id="05c09-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="05c09-114">Przewidywane odchylenie nakładu pracy = planowany nakład pracy — SPZ</span><span class="sxs-lookup"><span data-stu-id="05c09-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="05c09-115">W programie PSA jest wyświetlona projekcja odchylenia danego zadania.</span><span class="sxs-lookup"><span data-stu-id="05c09-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="05c09-116">Jeśli wartość SPZ przekracza planowany nakład pracy, zadanie jest rzutowane na czas dłuższy niż planowano.</span><span class="sxs-lookup"><span data-stu-id="05c09-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="05c09-117">Z tego powodu nie mieści się w harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="05c09-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="05c09-118">Jeśli wartość SPZ jest mniejsza niż planowany nakład pracy, zadanie jest rzutowane na czas krótszy niż planowano.</span><span class="sxs-lookup"><span data-stu-id="05c09-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="05c09-119">Z tego powodu zadanie wyprzedza harmonogram.</span><span class="sxs-lookup"><span data-stu-id="05c09-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="05c09-120">Ponowne prognozowanie nakładu pracy</span><span class="sxs-lookup"><span data-stu-id="05c09-120">Re-projecting effort</span></span>

<span data-ttu-id="05c09-121">Menedżerowie projektu często rewidują oryginalne wartości szacunkowe zadania.</span><span class="sxs-lookup"><span data-stu-id="05c09-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="05c09-122">Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu.</span><span class="sxs-lookup"><span data-stu-id="05c09-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="05c09-123">Niemniej n ie zalecamy, aby menedżerowie projektu zmieniali liczby podstawowe, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.</span><span class="sxs-lookup"><span data-stu-id="05c09-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="05c09-124">Istnieją dwa sposoby ponownego prognozowania nakładu pracy na zadania:</span><span class="sxs-lookup"><span data-stu-id="05c09-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="05c09-125">Zastąpienie domyślnej wartości ETC nową wartością szacunkową rzeczywistego pozostałego nakładu pracy na zadanie.</span><span class="sxs-lookup"><span data-stu-id="05c09-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="05c09-126">Zastąpienie domyślnej wartości procentowej postępu nową wartością rzeczywistego postępu.</span><span class="sxs-lookup"><span data-stu-id="05c09-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="05c09-127">Każda z tych metod powoduje ponowne obliczenie wartości ETC zadania, SPZ i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem.</span><span class="sxs-lookup"><span data-stu-id="05c09-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="05c09-128">Wartości SPZ, ETC i procent postępu w zadaniach sumarycznych są również obliczane ponownie i dają nową projekcję odchylenia.</span><span class="sxs-lookup"><span data-stu-id="05c09-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="05c09-129">Ponowna projekcja nakładów na zadania sumaryczne</span><span class="sxs-lookup"><span data-stu-id="05c09-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="05c09-130">Nakład pracy na zadania sumaryczne lub zadania kontenera można zaprojektować ponownie.</span><span class="sxs-lookup"><span data-stu-id="05c09-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="05c09-131">Bez względu na to, czy użytkownik ponownie pracuje nad projektami przy użyciu pozostałego nakładu lub procentu postępu w zadaniach sumarycznych, zaczyna się następujący zestaw obliczeń:</span><span class="sxs-lookup"><span data-stu-id="05c09-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="05c09-132">Wartości SPZ, ETC i procent postępu są obliczane względem zadania.</span><span class="sxs-lookup"><span data-stu-id="05c09-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="05c09-133">Nowe wartości SPZ są rozkładane w dół na zadania podrzędne w takiej samej proporcji jak w oryginalnym elemencie SPZ w ramach danego zadania.</span><span class="sxs-lookup"><span data-stu-id="05c09-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="05c09-134">Obliczana jest nowa wartość SPZ w każdym z zadań w dół względem poszczególnych węzłów typu liść.</span><span class="sxs-lookup"><span data-stu-id="05c09-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="05c09-135">Następuje ponowne przeliczenie ETC i procenta postępu zadań podrzędnych do węzła liścia na podstawie wartości SPZ.</span><span class="sxs-lookup"><span data-stu-id="05c09-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="05c09-136">W wyniku tego powstaje nowa projekcja odchylenia nakładu pracy nad zadaniem.</span><span class="sxs-lookup"><span data-stu-id="05c09-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="05c09-137">System ponownie oblicza EAC zadań sumarycznych na całej drodze do węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="05c09-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="05c09-138">Widok śledzenia kosztów</span><span class="sxs-lookup"><span data-stu-id="05c09-138">Cost tracking view</span></span> 

<span data-ttu-id="05c09-139">W widoku **śledzenia kosztów** jest porównywany koszt rzeczywisty, który został wydany na wykonanie zadania według planowanego kosztu.</span><span class="sxs-lookup"><span data-stu-id="05c09-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="05c09-140">W tym widoku są wyświetlane tylko koszty robocizny i nie są uwzględniane koszty szacunków kosztów.</span><span class="sxs-lookup"><span data-stu-id="05c09-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="05c09-141">Korzystając z poniższych formuł, program PSA obliczy metryki śledzenia:</span><span class="sxs-lookup"><span data-stu-id="05c09-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="05c09-142">Procent zużytego kosztu = koszt rzeczywisty poniesiony do dnia ÷ planowany koszt zadania</span><span class="sxs-lookup"><span data-stu-id="05c09-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="05c09-143">Koszt do zakończenia (CTC) = planowany koszt — rzeczywisty koszt poniesiony do dnia</span><span class="sxs-lookup"><span data-stu-id="05c09-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="05c09-144">SPZ = CTC + koszt rzeczywisty poniesiony do dnia</span><span class="sxs-lookup"><span data-stu-id="05c09-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="05c09-145">Prognozowane odchylenie kosztu = koszt planowany – SPZ</span><span class="sxs-lookup"><span data-stu-id="05c09-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="05c09-146">Prognoza odchylenia kosztu jest widoczna w zadaniu.</span><span class="sxs-lookup"><span data-stu-id="05c09-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="05c09-147">Jeśli wartość SPZ przekracza planowany koszt, zadaniu jest przypisywany koszt wyższy niż planowano na początku.</span><span class="sxs-lookup"><span data-stu-id="05c09-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="05c09-148">Z tego powodu ma ono tendencję do przekroczenia budżetu.</span><span class="sxs-lookup"><span data-stu-id="05c09-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="05c09-149">Jeśli wartość SPZ jest mniejsza od planowanego kosztu, zadaniu jest przypisywany koszt niższy niż planowano na początku.</span><span class="sxs-lookup"><span data-stu-id="05c09-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="05c09-150">Z tego powodu ma ono tendencję do niewykorzystania budżetu.</span><span class="sxs-lookup"><span data-stu-id="05c09-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="05c09-151">Ponowne prognozowanie kosztów przez menedżera projektu</span><span class="sxs-lookup"><span data-stu-id="05c09-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="05c09-152">W przypadku ponownego prognozowanego nakładu pracy CTC, SPZ, procent zużytego kosztu i przewidywane odchylenie kosztów są ponownie obliczane w widoku **śledzenia kosztów**.</span><span class="sxs-lookup"><span data-stu-id="05c09-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="05c09-153">Podsumowanie statusu projektu</span><span class="sxs-lookup"><span data-stu-id="05c09-153">Project status summary</span></span>

<span data-ttu-id="05c09-154">Śledzenie danych w widokach **śledzenie nakładu pracy** i **śledzenie kosztów** wskazuje postępy i zużycie kosztów na poziomach zadań w głównym węźle projektu, zadania sumaryczne i węzły liścia.</span><span class="sxs-lookup"><span data-stu-id="05c09-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="05c09-155">Sekcja **stan** na stronie **encja projektu** zawiera podsumowanie stanu na poziomie projektu.</span><span class="sxs-lookup"><span data-stu-id="05c09-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="05c09-156">Pola podsumowania stanu</span><span class="sxs-lookup"><span data-stu-id="05c09-156">Status summary fields</span></span>

<span data-ttu-id="05c09-157">Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu.</span><span class="sxs-lookup"><span data-stu-id="05c09-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="05c09-158">Używa kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko.</span><span class="sxs-lookup"><span data-stu-id="05c09-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="05c09-159">Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu.</span><span class="sxs-lookup"><span data-stu-id="05c09-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="05c09-160">Pole **Stan zaktualizowany w dniu** nie jest edytowalne, a wartość jest sygnaturą czasową wskazującą datę ostatniej aktualizacji stanu.</span><span class="sxs-lookup"><span data-stu-id="05c09-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="05c09-161">Pola **wydajność planowania** i **wydajność kosztów** są ustawiane na podstawie daty śledzenia.</span><span class="sxs-lookup"><span data-stu-id="05c09-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="05c09-162">Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, można ustawić te pola na**mieści się**.</span><span class="sxs-lookup"><span data-stu-id="05c09-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="05c09-163">Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne, można ustawić je na wartość **nie mieści się**.</span><span class="sxs-lookup"><span data-stu-id="05c09-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
