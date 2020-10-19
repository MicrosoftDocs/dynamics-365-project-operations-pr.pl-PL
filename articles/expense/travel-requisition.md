---
title: Wnioski wyjazdowe
description: Ten temat zawiera informacje o wnioskach wyjazdowych.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906280"
---
# <a name="travel-requisitions"></a><span data-ttu-id="53a17-103">Wnioski wyjazdowe</span><span class="sxs-lookup"><span data-stu-id="53a17-103">Travel requisitions</span></span>

<span data-ttu-id="53a17-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="53a17-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="53a17-105">W ramach wniosków wyjazdowych przedstawione są wydatki, które będą ponoszone w celu wyjazdu.</span><span class="sxs-lookup"><span data-stu-id="53a17-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="53a17-106">Wniosek wyjazdowy jest przedkładany do przeglądu i może być używany do zatwierdzania kosztów.</span><span class="sxs-lookup"><span data-stu-id="53a17-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="53a17-107">Może zaistnieć konieczność przesłania wniosków wyjazdowych przed poniesieniem kosztów naliczanych przez organizację.</span><span class="sxs-lookup"><span data-stu-id="53a17-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="53a17-108">To wymaganie ma zastosowanie bez względu na to, czy obciążana jest firmowa karta kredytowa, wydawana jest gotówka z zaliczki, czy ponoszone są koszty własne, które zostaną zwrócone później.</span><span class="sxs-lookup"><span data-stu-id="53a17-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="53a17-109">Aby pomóc w zarządzaniu wydatkami organizacji, można użyć wniosków wyjazdowych i zasad.</span><span class="sxs-lookup"><span data-stu-id="53a17-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="53a17-110">Jeśli na przykład organizacja pracuje nad projektem o stałej cenie, który wymaga podróży, koszty podróży członków zespołu projektu muszą mieścić się w budżecie projektu.</span><span class="sxs-lookup"><span data-stu-id="53a17-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="53a17-111">Wymagając, aby koszty podróży były zatwierdzane przed ich poniesieniem, organizacja może pomóc w upewnieniu się, że projekt nie przekracza budżetu.</span><span class="sxs-lookup"><span data-stu-id="53a17-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="53a17-112">Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="53a17-112">Configuration</span></span> 

<span data-ttu-id="53a17-113">We wstępnym zapotrzebowaniu na wyjazd można skonfigurować parametr jako obowiązkowy, dzięki włączeniu w parametrach zarządzania wydatkami parametru „Wstępne zezwolenie na podróż jest obowiązkowe”.</span><span class="sxs-lookup"><span data-stu-id="53a17-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="53a17-114">Tworzenie i przesyłanie wniosków wyjazdowych</span><span class="sxs-lookup"><span data-stu-id="53a17-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="53a17-115">Przejdź do obszaru **Moje wydatki: wniosek wyjazdowy** i wybierz **Nowy wniosek wyjazdowy**.</span><span class="sxs-lookup"><span data-stu-id="53a17-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="53a17-116">Wprowadź cel i miejsce docelowe zapotrzebowania.</span><span class="sxs-lookup"><span data-stu-id="53a17-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="53a17-117">W polu **Opis podróży** wprowadź dowolne dodatkowe informacje.</span><span class="sxs-lookup"><span data-stu-id="53a17-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="53a17-118">Dla każdego z przewidywanych kosztów, takich jak loty, posiłki lub wynajem samochodów, utwórz element wiersza wydatku.</span><span class="sxs-lookup"><span data-stu-id="53a17-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="53a17-119">Dołącz szacowaną datę i kwotę oraz walutę dla każdego wydatku.</span><span class="sxs-lookup"><span data-stu-id="53a17-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="53a17-120">Po zakończeniu dodawania przewidywanych wydatków wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="53a17-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="53a17-121">Po przygotowaniu wniosku wyjazdowego wybierz opcję **Przepływ pracy** > **Prześlij**.</span><span class="sxs-lookup"><span data-stu-id="53a17-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="53a17-122">Swoje zaakceptowane wnioski wyjazdowe można wyświetlić w ramach sekcji **Moje wyjazdy: wnioski wyjazdowe**.</span><span class="sxs-lookup"><span data-stu-id="53a17-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="53a17-123">Wyświetl dostępne wnioski wyjazdowe</span><span class="sxs-lookup"><span data-stu-id="53a17-123">View available travel requisitions</span></span>

<span data-ttu-id="53a17-124">Wszystkie wnioski wyjazdowe można wyświetlić w ramach sekcji **Moje wyjazdy: wnioski wyjazdowe**.</span><span class="sxs-lookup"><span data-stu-id="53a17-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="53a17-125">Zatwierdź wnioski wyjazdowe</span><span class="sxs-lookup"><span data-stu-id="53a17-125">Approve travel requisitions</span></span>

<span data-ttu-id="53a17-126">Wybierz wniosek wyjazdowy, który chcesz zatwierdzić, a następnie wybierz pozycję **Przepływ pracy** > **Zatwierdź**.</span><span class="sxs-lookup"><span data-stu-id="53a17-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="53a17-127">Wysyłanie raportu z wydatków za pomocą zatwierdzonego wniosku wyjazdowego</span><span class="sxs-lookup"><span data-stu-id="53a17-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="53a17-128">Utwórz nowy raport wydatków i w nagłówku raportu i na liście zatwierdzonych wniosków wyjazdowych wybierz pozycję **Zamapuj do wniosku wyjazdowego**.</span><span class="sxs-lookup"><span data-stu-id="53a17-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="53a17-129">Pole **Kwoty wniosku wyjazdowego** jest automatycznie aktualizowane w nagłówku raportu o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="53a17-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="53a17-130">Dodaj koszty poniesione podczas podróży.</span><span class="sxs-lookup"><span data-stu-id="53a17-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="53a17-131">Jeśli zaznaczone jest pole **Wstępnie autoryzowane**, zostanie zaktualizowana kwota uzgodniona i kwota zatwierdzona dla określonej kategorii wydatków.</span><span class="sxs-lookup"><span data-stu-id="53a17-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="53a17-132">W przypadku zamapowania raportu z wydatków do zatwierdzonego wniosku wyjazdowego, kwota transakcji nie może być większa od kwoty dozwolonej.</span><span class="sxs-lookup"><span data-stu-id="53a17-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
