---
title: Raporty wydatków i różne osoby zatwierdzające
description: Ta temat zawiera informacje na temat raportów z wydatków, które wymagają zatwierdzenia przez więcej niż jedną osobę.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121006"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="6a8c2-103">Raporty wydatków i różne osoby zatwierdzające</span><span class="sxs-lookup"><span data-stu-id="6a8c2-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="6a8c2-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="6a8c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a8c2-105">W zależności od zasad zatwierdzania wydatków w danej organizacji, czasem więcej niż jedna osoba musi zatwierdzić przesłany raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="6a8c2-106">Podczas konfigurowania procesu przepływu pracy na potrzeby zatwierdzania raportów z wydatków można dodać elementy przepływu pracy zawierające zadania lub kroki dla jednej lub więcej osób zatwierdzających raporty o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="6a8c2-107">Na przykład może zaistnieć konieczność zatwierdzania wszystkich raportów z wydatków przez dwóch pracowników — kierownika pracownika, który je przedstawił i koordynatora ds. rozrachunków z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="6a8c2-108">Jeśli zachodzi konieczność pracy przez wiele osób zatwierdzających raporty z wydatków, elementy przepływu pracy można dodać następującymi sposobami:</span><span class="sxs-lookup"><span data-stu-id="6a8c2-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="6a8c2-109">Dodaj jeden element zatwierdzający zawierający jeden krok.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-109">Add one approval element that has one step.</span></span> <span data-ttu-id="6a8c2-110">Na przykład może zaistnieć konieczność przypisania do grupy użytkowników raportu o wydatkach i jego zaakceptowanie przez 50 procent członków grupy użytkowników.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="6a8c2-111">Dodaj jeden element zatwierdzający zawierający wiele kroków.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="6a8c2-112">Element zatwierdzania może na przykład zawierać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="6a8c2-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="6a8c2-113">Kierownik pracownika, który składa raport, zatwierdza go.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="6a8c2-114">Pracownik ds. rozrachunków z dostawcami weryfikuje paragony i zapisy z raportów z wydatków.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="6a8c2-115">Właściciel budżetu zatwierdza raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="6a8c2-116">Dodaj wiele elementów zatwierdzania, z których każdy zawiera jeden krok.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="6a8c2-117">Można na przykład dodać osobny element zatwierdzania dla każdego z następujących kroków:</span><span class="sxs-lookup"><span data-stu-id="6a8c2-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="6a8c2-118">Kierownik pracownika zatwierdza raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="6a8c2-119">Właściciel budżetu zatwierdza raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="6a8c2-119">The budget owner approves the expense report.</span></span>
