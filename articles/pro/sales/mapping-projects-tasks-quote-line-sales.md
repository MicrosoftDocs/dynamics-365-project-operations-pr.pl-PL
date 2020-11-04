---
title: Mapowanie projektów i zadań do wiersza oferty opartej na projekcie
description: W tym temacie zamieszczono informacje dotyczące sposobu mapowania projektów i zadań na pozycje zadań oparte na projektach.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081904"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="4f1f4-103">Mapowanie projektów i zadań do wiersza oferty opartej na projekcie</span><span class="sxs-lookup"><span data-stu-id="4f1f4-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="4f1f4-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="4f1f4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4f1f4-105">W wierszach oferty opartej na projektach można zamapować określone zadania projektu, które są już skojarzone z wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="4f1f4-106">W przypadku mapowania zadań na wiersz oferty poniższe pozycje, które zdefiniowano w wierszu oferty, będą miały zastosowanie tylko do tych zadań:</span><span class="sxs-lookup"><span data-stu-id="4f1f4-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="4f1f4-107">Metoda rozliczania</span><span class="sxs-lookup"><span data-stu-id="4f1f4-107">Billing method</span></span>
- <span data-ttu-id="4f1f4-108">Opcje naliczania opłat</span><span class="sxs-lookup"><span data-stu-id="4f1f4-108">Chargeability options</span></span>
- <span data-ttu-id="4f1f4-109">Nieprzekraczalne limity</span><span class="sxs-lookup"><span data-stu-id="4f1f4-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="4f1f4-110">Klienci</span><span class="sxs-lookup"><span data-stu-id="4f1f4-110">Customers</span></span>

<span data-ttu-id="4f1f4-111">Na przykład może istnieć projekt z jedną fazą w cenie stałej i wszystkimi innymi etapami rozliczanymi na podstawie czasu i materiałów.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="4f1f4-112">W tym przypadku pierwszą fazę i wszystkie jej zadania podrzędne można skojarzyć z wierszem oferty w tej fazie z metodą fakturowania przy użyciu ustalonej ceny.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="4f1f4-113">Następnie można skojarzyć wszystkie pozostałe fazy z wierszem oferty opartej na czasie i na materiałach.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="4f1f4-114">Powiązanie zadań do wierszy oferty opartej na projekcie</span><span class="sxs-lookup"><span data-stu-id="4f1f4-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="4f1f4-115">Zadania można kojarzyć z wierszami oferty z następujących lokalizacji:</span><span class="sxs-lookup"><span data-stu-id="4f1f4-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="4f1f4-116">Strona **Projekt** > karta **Fakturowanie zadania** (optymalne)</span><span class="sxs-lookup"><span data-stu-id="4f1f4-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="4f1f4-117">Strona **Wiersz oferty** > karta **Zadania płatne**</span><span class="sxs-lookup"><span data-stu-id="4f1f4-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="4f1f4-118">Z poziomu strony projektu</span><span class="sxs-lookup"><span data-stu-id="4f1f4-118">From the Project page</span></span>

<span data-ttu-id="4f1f4-119">Na stronie **Projekt** można korzystać z optymalnego sposobu kojarzenia zadań z wierszami oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="4f1f4-120">Tej strony można użyć do wybrania wielu zadań i skojarzenia wszystkich rekordów wraz z ich zadaniami podrzędnymi z wybranym wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="4f1f4-121">Na karcie **Ogólne** wiersza oferty opartej na projekcie sprawdź, czy pole **Projekt** jest wypełnione.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="4f1f4-122">W polu **Uwzględnione zadania** wybierz opcję **Tylko zaznaczone zadania**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="4f1f4-123">Zapisz wiersz oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-123">Save the project-based quote line.</span></span> <span data-ttu-id="4f1f4-124">Po odświeżeniu formularza zostanie wyświetlona karta **Odpłatne zadania**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="4f1f4-125">Na karcie **Ogólne** wybierz łącze projektu z pola **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="4f1f4-126">Na stronie **Projekt** wybierz kartę **Rozliczanie zadania**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="4f1f4-127">W drugiej siatce dotyczącej konfigurowania fakturowania dla konkretnego zadania należy wybrać jedno lub więcej zadań, a następnie wybrać opcję **Przypisz wiersze oferty**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="4f1f4-128">Na wyświetlonej stronie dialogowej wybierz wiersz oferty, w którym są wyświetlane wiersze oferty oparte na projekcie w danej ofercie.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="4f1f4-129">W polu **Typ rozliczenia** wybierz, czy te zadania są płatne, czy niepłatne.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="4f1f4-130">Zaznacz pole wyboru, aby określić, czy skojarzenie powinno zawierać zadania podrzędne zaznaczonych zadań.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="4f1f4-131">Zaznaczenie pola spowoduje skojarzenie zadań podrzędnych zaznaczonych zadań z wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="4f1f4-132">Wybierz **OK** , aby zamknąć okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="4f1f4-133">Ze strony wiersz oferty</span><span class="sxs-lookup"><span data-stu-id="4f1f4-133">From the Quote line page</span></span>

<span data-ttu-id="4f1f4-134">Zadania projektu można kojarzyć z wierszami oferty na karcie **Opłatne zadania** na stronie **Wiersz oferty**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="4f1f4-135">Optymalne miejsce do kojarzenia zadań projektu z wierszami oferty znajduje się na karcie **Rozliczanie zadań** na stronie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="4f1f4-136">Jeśli zadania zostaną skojarzone z kartą **Odpłatne zadania** na stronie **Wiersz oferty** , należy ręcznie skojarzyć poszczególne projekty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="4f1f4-137">Na karcie **Ogólne** wiersza oferty opartej na projekcie sprawdź, czy w polu **Projekt** jest wybrany projekt.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="4f1f4-138">W polu **Uwzględnione zadania** wybierz opcję **Tylko zaznaczone zadania**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="4f1f4-139">Zapisz wiersz oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-139">Save the project-based quote line.</span></span> <span data-ttu-id="4f1f4-140">Po odświeżeniu formularza zostanie wyświetlona karta **Odpłatne zadania**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="4f1f4-141">Na karcie **Odpłatne zadania** wybierz pozycję **Dodaj zadanie wiersza oferty**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="4f1f4-142">Na stronie **Zadanie z wierszem oferty** w polu **Zadania** wybierz zadanie, a następnie w polu **Typ rozliczenia** wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="4f1f4-143">Zamyknij stronę.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-143">Close the page.</span></span> <span data-ttu-id="4f1f4-144">Wybrane zadanie jest teraz skojarzone z wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="4f1f4-145">Anulowanie powiązań zadań z wierszami oferty opartej na projekcie</span><span class="sxs-lookup"><span data-stu-id="4f1f4-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="4f1f4-146">Z poziomu strony projektu</span><span class="sxs-lookup"><span data-stu-id="4f1f4-146">From the Project page</span></span>

<span data-ttu-id="4f1f4-147">Ta metoda pozwala w optymalny sposób anulować powiązania zadań z wierszami oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="4f1f4-148">Tej strony można użyć do wybrania wielu zadań i anulowania skojarzenia wszystkich rekordów wraz z ich zadaniami podrzędnymi z wybranym wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="4f1f4-149">Na karcie **Ogólne** wiersza oferty opartej na projekcie, w polu **Projekt** wybierz link do projektu.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="4f1f4-150">Na stronie **Projekt** wybierz kartę **Rozliczanie zadania**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="4f1f4-151">W drugiej siatce dotyczącej konfigurowania fakturowania dla konkretnego zadania należy wybrać jedno lub więcej zadań, a następnie wybrać opcję **Anuluj przypisanie wierszy oferty**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="4f1f4-152">Na wyświetlonej stronie dialogowej wybierz wiersz oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="4f1f4-153">Zaznacz pole wyboru, aby określić, czy skojarzenie powinno być usunięte z zadań podrzędnych dla zaznaczonych zadań.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="4f1f4-154">Zaznaczenie pola spowoduje anulowanie skojarzenia zadań podrzędnych zaznaczonych zadań z wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="4f1f4-155">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-155">Select **OK**.</span></span> <span data-ttu-id="4f1f4-156">Komunikat ostrzegawczy informuje, że jeśli to skojarzenie zostanie usunięte, wszystkie wartości rzeczywiste zarejestrowane wcześniej w tym zadaniu mogą też zostać cofnięte.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="4f1f4-157">Wybierz przycisk **OK** , aby kontynuować, i usuń skojarzenie między zadaniem a wierszem oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="4f1f4-158">Ze strony wiersz oferty</span><span class="sxs-lookup"><span data-stu-id="4f1f4-158">From the Quote line page</span></span>

<span data-ttu-id="4f1f4-159">Skojarzenia zadań projektu można także anulować odnośnie do wierszy oferty na karcie **Opłatne zadania** na stronie **Wiersz oferty**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="4f1f4-160">Na karcie **Odpłatne zadania** wybierz pozycję **Usuń zadanie wiersza oferty**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="4f1f4-161">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-161">Select **OK**.</span></span> <span data-ttu-id="4f1f4-162">Komunikat ostrzegawczy informuje, że jeśli to skojarzenie zostanie usunięte, wszystkie wartości rzeczywiste zarejestrowane wcześniej w tym zadaniu mogą też zostać cofnięte.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="4f1f4-163">Wybierz przycisk **OK** , aby kontynuować, i usuń skojarzenie między zadaniem a wierszem oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="4f1f4-164">Ta procedura nie powoduje usunięcia zadania z projektu.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="4f1f4-165">Usuwane jest tylko powiązanie zadania z wiersza oferty opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="4f1f4-165">It only removes the task association from the project-based quote line.</span></span>
