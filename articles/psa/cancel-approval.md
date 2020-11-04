---
title: Anulowanie zatwierdzonych wcześniej wpisów czasu i wydatku
description: Ten temat zawiera informacje o sposobie anulowania zatwierdzonej transakcji rozliczanej według czasu i wydatku.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082187"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="b7aa1-103">Anulowanie zatwierdzonych wcześniej wpisów czasu lub wydatku</span><span class="sxs-lookup"><span data-stu-id="b7aa1-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b7aa1-104">W najnowszej wersji programu Dynamics 365 Project Service Automation osoby zatwierdzające mogą anulować wpisy czasu lub wydatku, które zostały wcześniej zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="b7aa1-105">Anulowanie zatwierdzonego wcześniej wpisu czasu lub wydatku</span><span class="sxs-lookup"><span data-stu-id="b7aa1-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="b7aa1-106">Wykonaj te kroki, aby anulować wpis czasu lub wydatku, który wcześniej został przez Ciebie zaakceptowany.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="b7aa1-107">Wybierz kolejno opcje **Projekty** \> **Moja praca** \> **Zatwierdzenia**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="b7aa1-108">Na stronie listy **Zatwierdzenia** zmień widok na **Moje przeszłe zatwierdzenia**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="b7aa1-109">Zostanie wyświetlona lista wpisów czasu i wydatku uprzednio zatwierdzonych przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="b7aa1-110">Zaznacz jeden lub więcej wpisów, a następnie kliknij przycisk **Anuluj zatwierdzenie**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="b7aa1-111">Zostanie wyświetlony komunikat ostrzegawczy.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-111">You receive a warning message.</span></span>
4. <span data-ttu-id="b7aa1-112">Kliknij przycisk **OK** , aby anulować zatwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="b7aa1-113">Informacje o skutkach anulowania zatwierdzania wpisu czasu lub wydatku</span><span class="sxs-lookup"><span data-stu-id="b7aa1-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="b7aa1-114">Anulowanie zatwierdzonego wpisu ma wpływ na stronę operacyjną i finansową.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="b7aa1-115">Wpływ operacyjny</span><span class="sxs-lookup"><span data-stu-id="b7aa1-115">Operational impact</span></span>

<span data-ttu-id="b7aa1-116">Pod względem operacyjnym po anulowaniu zatwierdzenia stan rekordu jest resetowany do wartości **Wersja robocza** , a zatwierdzenie nie jest już wyświetlane w widoku **Moje przeszłe zatwierdzenia**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft** , and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="b7aa1-117">Zamiast tego anulowane zatwierdzenie jest wyświetlane w widoku **Wpisy czasu do zatwierdzenia** lub widoku **Wpisy wydatków do zatwierdzenia** , w zależności od tego, czy był to wpis czasu, czy wydatku.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="b7aa1-118">Ponadto stan pokrewnego wpisu czasu lub wydatku zmienia się na **Przesłano** , tak aby ów wpis był spójny z zatwierdzeniami mającymi stan **Wersja robocza**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-118">Additionally, the status of the related time or expense entry is changed to **Submitted** , so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="b7aa1-119">Jako osoba zatwierdzająca, możesz edytować niektóre pola zatwierdzania mającego stan **Wersja robocza**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="b7aa1-120">Są to pola **Typ rozliczania** oraz **Godziny podlegające rozliczeniu dla wpisów czasu**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="b7aa1-121">Po dokonaniu zmian możesz ponownie zatwierdzić rekord.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="b7aa1-122">Alternatywnie możesz odrzucić wpis.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="b7aa1-123">Odrzucenie zatwierdzenia wpisu czasu spowoduje zmianę stanu wpisu na **Zwrócono**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="b7aa1-124">Odrzucenie zatwierdzenia wpisu wydatku spowoduje zmianę stanu wpisu na **Odrzucono**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="b7aa1-125">Pod względem funkcjonalnym wpisy zwrócone i odrzucone zachowują się tak samo, jak wpisy o stanie **Wersja robocza**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="b7aa1-126">Członek zespołu projektu może wprowadzić wszelkie wymagane zmiany we wpisie i ponownie go przesłać do zatwierdzenia albo całkowicie usunąć wpis.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="b7aa1-127">Wpływ finansowy</span><span class="sxs-lookup"><span data-stu-id="b7aa1-127">Financial impact</span></span>

<span data-ttu-id="b7aa1-128">Anulowanie zatwierdzenia wpływa również finansowo na projekt.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="b7aa1-129">Najpierw odnośne wartości rzeczywiste dotyczące kosztu i sprzedaży są aktualizowane w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="b7aa1-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="b7aa1-130">Stan korekty jest ustawiany jako **Skorygowano**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="b7aa1-131">Stan rozliczania jest ustawiany jako **Anulowano**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="b7aa1-132">Następnie w tabeli Wartości rzeczywiste są tworzone wpisy wycofania.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="b7aa1-133">Aby utworzyć wpisy wycofania, system kopiuje wartości pól z pierwotnych wartości rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="b7aa1-134">Jedyne wartości, które nie są kopiowane, to wartości ilości.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="b7aa1-135">Zamiast tego te wartości są wycofywane.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-135">These values are reversed instead.</span></span> <span data-ttu-id="b7aa1-136">Wycofane wartości rzeczywiste są tworzone dla wartości rzeczywistych **Koszt** i **Nierozliczona sprzedaż**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="b7aa1-137">Pole **Stan korekty** w wycofanych wartościach rzeczywistych otrzymuje wartość **Nie można skorygować** , a stan rozliczania otrzymuje wartość **Anulowano**.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable** , and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="b7aa1-138">Po wprowadzeniu tych zmian kwota zarejestrowana jako wydana w projekcie oraz zaległości przychodów w projekcie nie będą już uwzględniały kwot reprezentowanych przez te wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="b7aa1-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
