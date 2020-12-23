---
title: Zarządzanie szacowaniami przychodów
description: Ten temat zawiera informacje dotyczące pracy z szacowaniami przychodów dla projektów.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531513"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="a787f-103">Zarządzanie szacowaniami przychodów</span><span class="sxs-lookup"><span data-stu-id="a787f-103">Manage revenue estimates</span></span>

<span data-ttu-id="a787f-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="a787f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a787f-105">Możesz tworzyć, obliczać, księgować, cofać lub eliminować szacowania przychodów.</span><span class="sxs-lookup"><span data-stu-id="a787f-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="a787f-106">Można to zrobić ręcznie lub za pomocą procesu okresowego.</span><span class="sxs-lookup"><span data-stu-id="a787f-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="a787f-107">Ten temat zawiera informacje dotyczące pracy z szacowaniami przychodów dla projektów.</span><span class="sxs-lookup"><span data-stu-id="a787f-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="a787f-108">Ręczne zarządzanie szacowaniami przychodów</span><span class="sxs-lookup"><span data-stu-id="a787f-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="a787f-109">Na stronie projektu szacowania przychodów o stałej cenie lub na stronie **Zapytanie o oszacowanie** (**Zarządzanie projektami i księgowanie** > **Raporty i zapytania** > **Zapytania i raporty dotyczące szacowań**) wybierz pozycję **Szacowania**.</span><span class="sxs-lookup"><span data-stu-id="a787f-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="a787f-110">Zarządzanie szacowaniami przychodów przy użyciu procesu okresowego</span><span class="sxs-lookup"><span data-stu-id="a787f-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="a787f-111">Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Okresowe** > **Szacowania** i wybierz odpowiedni proces.</span><span class="sxs-lookup"><span data-stu-id="a787f-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="a787f-112">Tworzenie szacowania przychodów</span><span class="sxs-lookup"><span data-stu-id="a787f-112">Create a revenue estimate</span></span>

<span data-ttu-id="a787f-113">Wykonaj następujące kroki, aby utworzyć szacowanie przychodów.</span><span class="sxs-lookup"><span data-stu-id="a787f-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="a787f-114">Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Okresowe** > **Szacowania**.</span><span class="sxs-lookup"><span data-stu-id="a787f-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="a787f-115">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="a787f-115">Select **New**.</span></span> <span data-ttu-id="a787f-116">Na stronie **Tworzenie szacowania** wybierz następujące parametry:</span><span class="sxs-lookup"><span data-stu-id="a787f-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="a787f-117">**Kod okresu**: Ten kod wskazuje, jak często szacowania są księgowane.</span><span class="sxs-lookup"><span data-stu-id="a787f-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="a787f-118">**Data szacowania**: data przetwarzania szacowania.</span><span class="sxs-lookup"><span data-stu-id="a787f-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="a787f-119">**Ciągłe**: zaznacz to pole wyboru, aby tworzyć szacowania tylko wtedy, gdy szacowania zostały zaksięgowane w poprzednim okresie lub jeśli szacowanie jest pierwszym utworzonym szacowaniem.</span><span class="sxs-lookup"><span data-stu-id="a787f-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="a787f-120">Jeśli to pole nie jest zaznaczone, szacowania są tworzone, nawet jeśli nie zostały zaksięgowane w poprzednim okresie.</span><span class="sxs-lookup"><span data-stu-id="a787f-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="a787f-121">**Metoda kosztu wykonania**: zdefiniuj sposób szacowania pozostałej pracy projektowej.</span><span class="sxs-lookup"><span data-stu-id="a787f-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="a787f-122">Aby uzyskać więcej informacji, zobacz [Metoda kosztu wykonania](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a787f-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="a787f-123">**Metoda wykonania**: wybierz metodę wykonania spośród następujących opcji:</span><span class="sxs-lookup"><span data-stu-id="a787f-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="a787f-124">**Automatycznie**: procent wykonania jest obliczany automatycznie, na podstawie wierszy kosztów uwzględnionych w obliczeniach.</span><span class="sxs-lookup"><span data-stu-id="a787f-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="a787f-125">Szablon kosztu definiuje wiersze kosztu do uwzględnienia.</span><span class="sxs-lookup"><span data-stu-id="a787f-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="a787f-126">**Ręcznie**: procent wykonania jest równy procentowi wykonania dla ostatniego oszacowania.</span><span class="sxs-lookup"><span data-stu-id="a787f-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="a787f-127">Po utworzeniu szacowania można zmienić opcję **Obliczanie ręczne** na stronie **Szacowania**.</span><span class="sxs-lookup"><span data-stu-id="a787f-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="a787f-128">**Z szablonu kosztów**: połączenie metod automatycznych i ręcznych.</span><span class="sxs-lookup"><span data-stu-id="a787f-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="a787f-129">Ta opcja jest ustawiana jako automatyczna lub ręczna, w zależności od wartości domyślnej w szablonie kosztu.</span><span class="sxs-lookup"><span data-stu-id="a787f-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="a787f-130">**Model prognozy**: wybierz model prognozy dla szacowania.</span><span class="sxs-lookup"><span data-stu-id="a787f-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="a787f-131">**Wydrukuj listę oszacowań**: utwórz i pokaż listę szacowań.</span><span class="sxs-lookup"><span data-stu-id="a787f-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="a787f-132">Lista zawiera stan bieżącej funkcji.</span><span class="sxs-lookup"><span data-stu-id="a787f-132">The list contains the status of the current function.</span></span> <span data-ttu-id="a787f-133">W raporcie można wydrukować ostrzeżenia dotyczące szacowania.</span><span class="sxs-lookup"><span data-stu-id="a787f-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="a787f-134">Następujące warunki powodują, że ostrzeżenia pojawiają się na liście szacowań:</span><span class="sxs-lookup"><span data-stu-id="a787f-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="a787f-135">Procent wykonania większy niż 100 procent.</span><span class="sxs-lookup"><span data-stu-id="a787f-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="a787f-136">Procent wykonania mniejszy niż zero procent.</span><span class="sxs-lookup"><span data-stu-id="a787f-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="a787f-137">Kwota ujemna w kolumnie **Do wykonania**.</span><span class="sxs-lookup"><span data-stu-id="a787f-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="a787f-138">Szacowanie bez odpowiedniej kwoty kontraktu.</span><span class="sxs-lookup"><span data-stu-id="a787f-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="a787f-139">Szacowanie bez dołączonego szacowania kosztów.</span><span class="sxs-lookup"><span data-stu-id="a787f-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="a787f-140">**Pokaż dziennik informacyjny**: wybierz tę opcję, aby otrzymać komunikat zawierający informacje o szacowanych projektach, które zostały przetworzone podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="a787f-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="a787f-141">Księgowanie PWT lub naliczeń</span><span class="sxs-lookup"><span data-stu-id="a787f-141">Post WIP or accruals</span></span>

<span data-ttu-id="a787f-142">Ocenione szacowania są utrzymywane, zmniejszane lub zwiększane.</span><span class="sxs-lookup"><span data-stu-id="a787f-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="a787f-143">Następnie można zaksięgować PWT podczas pracy przy użyciu zasad oceny **kontraktu ukończonego** lub zaksięgować naliczenia podczas pracy z zasadami oceny **Procent ukończenia**.</span><span class="sxs-lookup"><span data-stu-id="a787f-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="a787f-144">Stan okresu szacowania zmienia się z **Utworzono** na **Zaksięgowano**.</span><span class="sxs-lookup"><span data-stu-id="a787f-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="a787f-145">Odwracanie PWT lub naliczeń</span><span class="sxs-lookup"><span data-stu-id="a787f-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="a787f-146">Użyj opcji odwracania, aby uznać już zaksięgowane PWT lub naliczenia, a następnie utworzyć szacowania dla okresu.</span><span class="sxs-lookup"><span data-stu-id="a787f-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="a787f-147">Aby odwrócić okres, który znajduje się między innymi okresami, odwróć niezbędne okresy szacowania, a następnie ponownie je zaksięguj.</span><span class="sxs-lookup"><span data-stu-id="a787f-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="a787f-148">Ponieważ wszystkie kolejne okresy zależą od szacowań z poprzedniego okresu, nie pomijaj żadnych okresów.</span><span class="sxs-lookup"><span data-stu-id="a787f-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="a787f-149">Eliminowanie szacowania projektu i kończenie projektu</span><span class="sxs-lookup"><span data-stu-id="a787f-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="a787f-150">Ostatnim krokiem w procesie szacowania jest wyeliminowanie szacowania projektu i zakończenie projektu o stałej cenie, gdy procent ukończenia osiągnie 100 procent.</span><span class="sxs-lookup"><span data-stu-id="a787f-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="a787f-151">Po uruchomieniu eliminacji występują następujące sytuacje:</span><span class="sxs-lookup"><span data-stu-id="a787f-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="a787f-152">W przypadku projektu o stałej cenie z ukończonym kontraktem wartości PWT są czyszczone z kont bilansów i księgowane na kontach zysków i strat.</span><span class="sxs-lookup"><span data-stu-id="a787f-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="a787f-153">W przypadku projektu o stałej cenie z procentem ukończenia naliczenia są usuwane z kont zysków i strat.</span><span class="sxs-lookup"><span data-stu-id="a787f-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="a787f-154">Szacowanie zmienia stan na **Wyeliminowane**.</span><span class="sxs-lookup"><span data-stu-id="a787f-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="a787f-155">W szczególnych przypadkach wartość procentowa może przekraczać 100 procent.</span><span class="sxs-lookup"><span data-stu-id="a787f-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="a787f-156">W takim przypadku należy zmniejszyć procent ukończenia przy użyciu opcji **Ustaw metodę kosztu wykonania na zero**, aby osiągnąć 100 procent.</span><span class="sxs-lookup"><span data-stu-id="a787f-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="a787f-157">Wycofanie eliminacji</span><span class="sxs-lookup"><span data-stu-id="a787f-157">Reverse elimination</span></span>

1. <span data-ttu-id="a787f-158">Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Okresowe** > **Szacowania** > **Wycofanie eliminacji**.</span><span class="sxs-lookup"><span data-stu-id="a787f-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="a787f-159">W okienku akcji na karcie **Proces** w grupie **Obsługa** wybierz pozycję **Szacuj**.</span><span class="sxs-lookup"><span data-stu-id="a787f-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="a787f-160">Wybierz pozycję **Wycofanie eliminacji**.</span><span class="sxs-lookup"><span data-stu-id="a787f-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="a787f-161">Ta strona służy do wycofywania wszystkich eliminacji z określoną datą szacowania i stanem szacowania **Wyeliminowane**.</span><span class="sxs-lookup"><span data-stu-id="a787f-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="a787f-162">Stan transakcji zmienia się po wybraniu odpowiednich pól.</span><span class="sxs-lookup"><span data-stu-id="a787f-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="a787f-163">Spowoduje to również automatyczną zmianę stanu projektu na **W trakcie przetwarzania**, jeśli etap projektu jest ustawiony na ukończenie.</span><span class="sxs-lookup"><span data-stu-id="a787f-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="a787f-164">Stan szacowania okresu projektu zmienia się z powrotem na **Zaksięgowane**.</span><span class="sxs-lookup"><span data-stu-id="a787f-164">The estimate status of the project period changes back to **Posted**.</span></span>
