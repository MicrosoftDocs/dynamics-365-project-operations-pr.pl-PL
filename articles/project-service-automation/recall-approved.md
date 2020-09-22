---
title: Odwoływanie zatwierdzonych wpisów czasu lub wydatku
description: Ten temat zawiera informacje o sposobie odwoływania uprzednio zatwierdzonej transakcji rozliczanej według czasu lub transakcji wydatku.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754408"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="cbcb6-103">Odwoływanie zatwierdzonych wpisów czasu lub wydatku</span><span class="sxs-lookup"><span data-stu-id="cbcb6-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cbcb6-104">Członek zespołu projektu lub inna osoba, która prześle wpis czasu lub wydatku, może odwołać ten wpis po jego zatwierdzeniu.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="cbcb6-105">Proces odwoływania zatwierdzanego wpisu czasu lub wydatku ma dwa etapy:</span><span class="sxs-lookup"><span data-stu-id="cbcb6-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="cbcb6-106">Osoba przesyłająca prosi o odwołanie.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="cbcb6-107">Osobna zatwierdzająca akceptuje odwołanie.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="cbcb6-108">Wnioskowanie o odwołanie</span><span class="sxs-lookup"><span data-stu-id="cbcb6-108">Request a recall</span></span>

<span data-ttu-id="cbcb6-109">Wykonaj te kroki, aby poprosić o odwołanie zatwierdzonego wpisu czasu lub wydatku.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="cbcb6-110">W przypadku wpisów czasu wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Wpis czasu**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="cbcb6-111">–lub–</span><span class="sxs-lookup"><span data-stu-id="cbcb6-111">–or–</span></span>

    <span data-ttu-id="cbcb6-112">W przypadku wpisów wydatku wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Wydatki**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="cbcb6-113">W przypadku wpisów czasu zaznacz wszystkie wpisy czasu dla określonej kombinacji projektu i zadania.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="cbcb6-114">Alternatywnie w siatce zaznacz poszczególne komórki czasu w określonym dniu określonego projektu.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="cbcb6-115">–lub–</span><span class="sxs-lookup"><span data-stu-id="cbcb6-115">–or–</span></span>

    <span data-ttu-id="cbcb6-116">W przypadku wpisów wydatków zaznacz wiersz wpisu wydatku, który ma zostać odwołany.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="cbcb6-117">Wybierz pozycję **Odwołaj**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-117">Select **Recall**.</span></span> <span data-ttu-id="cbcb6-118">Pojawia się okno dialogowe potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="cbcb6-119">Jeśli zaznaczone wpisy czasu i wydatku były już zatwierdzone, zostanie wyświetlony monit o podanie przyczyny odwołania.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="cbcb6-120">Wprowadź przyczynę odwołania, a następnie wybierz przycisk **OK**, aby potwierdzić operację.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="cbcb6-121">System wyśle do użytkownika, który zatwierdził wpisy, prośbę o zatwierdzenie odwołania.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="cbcb6-122">Mimo że zatwierdzone wpisy czasu i wydatków można odwoływać, to jeśli za zatwierdzony czas lub wydatek już wystawiono odbiorcy fakturę, nie można utworzyć żądania odwołania.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="cbcb6-123">Użytkownik próbujący utworzyć żądanie odwołania zobaczy komunikat informujący o tym, że nie można odwołać wpisu czasu lub wydatku, ponieważ został on już zafakturowany.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="cbcb6-124">Zatwierdzanie lub odrzucanie żądania odwołania</span><span class="sxs-lookup"><span data-stu-id="cbcb6-124">Approve or reject a recall request</span></span>

<span data-ttu-id="cbcb6-125">Wykonaj te kroki, aby zatwierdzić lub odrzucić żądanie odwołania.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="cbcb6-126">Wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Zatwierdzenia**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="cbcb6-127">Na stronie listy **Zatwierdzenia** zmień widok na **Żądania odwołania do zatwierdzenia**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="cbcb6-128">Zostanie wyświetlona lista przesłanych żądań odwołania.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="cbcb6-129">Zaznacz jeden lub więcej wpisów, a następnie kliknij przycisk **Zatwierdź** lub **Odrzuć**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="cbcb6-130">W przypadku wybrania opcji **Zatwierdź** zostanie wyświetlony komunikat ostrzegawczy zawierający opis skutków zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="cbcb6-131">Wybierz pozycję **OK**, aby potwierdzić operację.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="cbcb6-132">Żądanie odwołania zostanie zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-132">The recall request is approved.</span></span>

    <span data-ttu-id="cbcb6-133">–lub–</span><span class="sxs-lookup"><span data-stu-id="cbcb6-133">–or–</span></span>

    <span data-ttu-id="cbcb6-134">W przypadku wybrania opcji **Odrzuć** żądanie odwołania zostanie odrzucone.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="cbcb6-135">Podobnie jak w przypadku wnioskowania o odwołanie, podczas zatwierdzania odwołania system sprawdza wszelkie ewentualne czynności fakturowania wpisów czasu lub wydatku.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="cbcb6-136">Jeśli wpis został już zafakturowany lub jeśli znajduje się on w wersji roboczej faktury, osoba zatwierdzająca zobaczy komunikat o błędzie z informacją, że nie można zatwierdzić odwołania czasu lub wydatku, ponieważ został on już zafakturowany.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="cbcb6-137">Wpływ żądania odwołania</span><span class="sxs-lookup"><span data-stu-id="cbcb6-137">Impact of a recall request</span></span>

<span data-ttu-id="cbcb6-138">Odwołanie zatwierdzonego wpisu ma wpływ na stronę operacyjną i finansową.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="cbcb6-139">Wpływ operacyjny</span><span class="sxs-lookup"><span data-stu-id="cbcb6-139">Operational impact</span></span>

<span data-ttu-id="cbcb6-140">Jeśli żądanie odwołania zostanie zatwierdzone, rekord zatwierdzenia jest oznaczany jako **Odrzucono**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="cbcb6-141">Stan wpisu zmieni się na **Zwrócono** lub **Odrzucono**, w zależności od tego, czy jest to wpis czasu, czy wpis wydatku.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="cbcb6-142">Członek zespołu projektu może wyświetlać wpisy, edytować je i ponownie wysyłać albo całkowicie usuwać.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="cbcb6-143">Jeśli żądanie odwołania zostanie odrzucone, wpis zachowuje stan **Zatwierdzono**, a wpisu nie może edytować członek zespołu projektu ani osoba zatwierdzająca w projekcie.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="cbcb6-144">Wpływ finansowy</span><span class="sxs-lookup"><span data-stu-id="cbcb6-144">Financial impact</span></span>

<span data-ttu-id="cbcb6-145">Jeśli żądanie odwołania zostanie zatwierdzane, odnośne wartości rzeczywiste dotyczące kosztu i sprzedaży są aktualizowane w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="cbcb6-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="cbcb6-146">Pole **Stan korekty** zmienia wartość na **Skorygowano**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="cbcb6-147">Pole **Stan rozliczania** zmienia wartość na **Anulowano**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="cbcb6-148">Następnie w tabeli Wartości rzeczywiste są tworzone wpisy wycofania.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="cbcb6-149">Aby utworzyć wpisy wycofania, system kopiuje wartości pól z pierwotnych wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="cbcb6-150">Jedyne wartości, które nie są kopiowane, to wartości ilości.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="cbcb6-151">Zamiast tego te wartości są wycofywane.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-151">These values are reversed instead.</span></span> <span data-ttu-id="cbcb6-152">Wycofane wartości rzeczywiste są tworzone dla wartości rzeczywistych **Koszt** i **Nierozliczona sprzedaż**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="cbcb6-153">Pole **Stan korekty** w wycofanych wartościach rzeczywistych otrzymuje wartość **Nie można skorygować**, a pole **Stan rozliczania** otrzymuje wartość **Anulowano**.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="cbcb6-154">Ze względu na te zmiany zarejestrowane wydatki oraz zaległości przychodów w projekcie nie będą już uwzględniały kwot reprezentowanych przez te wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="cbcb6-155">Jeśli żądanie odwołania zostanie odrzucone, nie ma żadnego wpływu finansowego na projekt.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="cbcb6-156">Zmiany w rekordach wpisów czasu</span><span class="sxs-lookup"><span data-stu-id="cbcb6-156">Changes to time entry records</span></span>

<span data-ttu-id="cbcb6-157">Na poniższej ilustracji pokazano zmiany występujące w zatwierdzonych wpisach czasu po ich odwołaniu.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Zmiany stanu wpisu czasu](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="cbcb6-159">Zmiany w rekordach wpisu wydatku</span><span class="sxs-lookup"><span data-stu-id="cbcb6-159">Changes to expense entry records</span></span>

<span data-ttu-id="cbcb6-160">Na poniższej ilustracji pokazano zmiany występujące w zatwierdzonych wpisach wydatków po ich odwołaniu.</span><span class="sxs-lookup"><span data-stu-id="cbcb6-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Zmiany stanu wpisu wydatku](media/ExpenseEntryStateTransitions.png)
