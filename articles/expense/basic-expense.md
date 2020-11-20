---
title: Wpis wydatków (lekkich)
description: W tym temat zamieszczono informacje na temat pracy z wpisem wydatków w ramach wdrożenia w wersji uproszczonej.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121096"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="f37a9-103">Wpis wydatków (lekkich)</span><span class="sxs-lookup"><span data-stu-id="f37a9-103">Expense entry (lite)</span></span>

<span data-ttu-id="f37a9-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="f37a9-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f37a9-105">Podstawowe lub uproszczone zarządzanie wydatkami polega na zarejestrowaniu prostych kosztów.</span><span class="sxs-lookup"><span data-stu-id="f37a9-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="f37a9-106">Istnieje możliwość rejestrowania kosztów w stosunku do projektu, a następnie analizy i zatwierdzenia ich przez osobę zatwierdzającą w projekcie.</span><span class="sxs-lookup"><span data-stu-id="f37a9-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="f37a9-107">Aby uzyskać więcej informacji o możliwościach wydatkowych w Dynamics 365 Project Operations zobacz temat [Informacje o wydatkach](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f37a9-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="f37a9-108">Rejestrowanie podstawowego wydatku</span><span class="sxs-lookup"><span data-stu-id="f37a9-108">Capture a basic expense</span></span>

<span data-ttu-id="f37a9-109">Wydatki można rejestrować, aby można było przesłać je do osoby zatwierdzającej.</span><span class="sxs-lookup"><span data-stu-id="f37a9-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="f37a9-110">Przejdź do obszaru **Wydatki** i wybierz pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="f37a9-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="f37a9-111">Na stronie **Nowy wydatek** wprowadź wymagane informacje o wydatkach, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="f37a9-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="f37a9-112">Przesyłanie podstawowego wydatku</span><span class="sxs-lookup"><span data-stu-id="f37a9-112">Submit a basic expense</span></span>

<span data-ttu-id="f37a9-113">Po zakończeniu przechwytywania wszystkich kosztów i przygotowaniu ich do zatwierdzenia należy je przesłać.</span><span class="sxs-lookup"><span data-stu-id="f37a9-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="f37a9-114">Przejdź do obszaru **Wydatki** i wybierz wydatek.</span><span class="sxs-lookup"><span data-stu-id="f37a9-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="f37a9-115">Można też wybrać wszystkie wydatki, korzystając z pola wyboru w nagłówku.</span><span class="sxs-lookup"><span data-stu-id="f37a9-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="f37a9-116">Wybierz **Prześlij**.</span><span class="sxs-lookup"><span data-stu-id="f37a9-116">Select **Submit**.</span></span> <span data-ttu-id="f37a9-117">System przetwarza wybrane wpisy, a następnie tworzy żądania zatwierdzeń wydatków.</span><span class="sxs-lookup"><span data-stu-id="f37a9-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="f37a9-118">Wycofanie podstawowego wydatku</span><span class="sxs-lookup"><span data-stu-id="f37a9-118">Recall a basic expense</span></span>

<span data-ttu-id="f37a9-119">Jeśli wydatek został przesłany przez pomyłkę, można go wycofać.</span><span class="sxs-lookup"><span data-stu-id="f37a9-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="f37a9-120">Czas wymagany do wycofania wpisu wydatku zależy od etapu zatwierdzania, na którym się znajduje.</span><span class="sxs-lookup"><span data-stu-id="f37a9-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="f37a9-121">Jeśli osoba zatwierdzająca jeszcze nie zatwierdziła wpisu, odwołanie może nastąpić natychmiast.</span><span class="sxs-lookup"><span data-stu-id="f37a9-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="f37a9-122">Jeśli jednak wpis został już zatwierdzony, należy poprosić osobę zatwierdzającą o zatwierdzenie wycofania i odwrócenie transakcji.</span><span class="sxs-lookup"><span data-stu-id="f37a9-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="f37a9-123">Przejdź do obszaru **Koszty**, a następnie na liście wydatków wybierz koszty, które chcesz wycofać.</span><span class="sxs-lookup"><span data-stu-id="f37a9-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="f37a9-124">Wybierz pozycję **Odwołaj**.</span><span class="sxs-lookup"><span data-stu-id="f37a9-124">Select **Recall**.</span></span> <span data-ttu-id="f37a9-125">Jeśli pozycja wydatku nie została jeszcze zatwierdzona, system natychmiast ją wycofa.</span><span class="sxs-lookup"><span data-stu-id="f37a9-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="f37a9-126">Jeśli zapis wydatków został już zatwierdzony, jest tworzone żądanie wycofania umożliwiające powiadomienie osoby zatwierdzającej o chęci odwrócenia wydatku.</span><span class="sxs-lookup"><span data-stu-id="f37a9-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="f37a9-127">Osoba zatwierdzająca potwierdzi również, że można dokonać odwrócenia, a wpis zostanie cofnięty.</span><span class="sxs-lookup"><span data-stu-id="f37a9-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="f37a9-128">Usunięcie podstawowego wydatku</span><span class="sxs-lookup"><span data-stu-id="f37a9-128">Delete a basic expense</span></span>

<span data-ttu-id="f37a9-129">Wydatki które nie zostały jeszcze przesłane, można usunąć.</span><span class="sxs-lookup"><span data-stu-id="f37a9-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="f37a9-130">Aby usunąć wydatek, który został już przesłany, należy go najpierw wycofać.</span><span class="sxs-lookup"><span data-stu-id="f37a9-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="f37a9-131">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="f37a9-131">See also</span></span>

- [<span data-ttu-id="f37a9-132">Omówienie zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="f37a9-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
