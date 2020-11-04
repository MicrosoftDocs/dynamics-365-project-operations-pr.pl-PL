---
title: Raporty wydatków i różne osoby zatwierdzające
description: Ta temat zawiera informacje na temat raportów z wydatków, które wymagają zatwierdzenia przez większą liczbę osób.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082168"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="669d9-103">Raporty wydatków i różne osoby zatwierdzające</span><span class="sxs-lookup"><span data-stu-id="669d9-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="669d9-104">W zależności od zasad zatwierdzania wydatków w danej organizacji, czasem więcej niż jedna osoba musi zatwierdzić przesłany przez pracownika raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="669d9-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="669d9-105">Podczas konfigurowania procesu przepływu pracy na potrzeby zatwierdzania raportów z wydatków można dodać elementy przepływu pracy zawierające zadania lub kroki dla jednej lub więcej osób zatwierdzających raporty o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="669d9-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="669d9-106">Na przykład może zaistnieć konieczność zatwierdzania wszystkich raportów z wydatków przez dwóch pracowników — najpierw przez kierownika pracownika, który je przedstawił, a potem przez koordynatora ds. rozrachunków z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="669d9-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="669d9-107">Jeśli zachodzi konieczność pracy przez wiele osób zatwierdzających raporty z wydatków, elementy przepływu pracy można dodać następującymi sposobami:</span><span class="sxs-lookup"><span data-stu-id="669d9-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="669d9-108">Dodaj jeden element zatwierdzający zawierający jeden krok.</span><span class="sxs-lookup"><span data-stu-id="669d9-108">Add one approval element that has one step.</span></span> <span data-ttu-id="669d9-109">Na przykład może zaistnieć konieczność przypisania do grupy użytkowników raportu o wydatkach i jego zaakceptowanie przez 50 procent członków grupy użytkowników.</span><span class="sxs-lookup"><span data-stu-id="669d9-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="669d9-110">Dodaj jeden element zatwierdzający zawierający wiele kroków.</span><span class="sxs-lookup"><span data-stu-id="669d9-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="669d9-111">Element zatwierdzania może na przykład zawierać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="669d9-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="669d9-112">Kierownik pracownika, który składa raport, zatwierdza go.</span><span class="sxs-lookup"><span data-stu-id="669d9-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="669d9-113">Pracownik ds. rozrachunków z dostawcami weryfikuje paragony i zapisy z raportów z wydatków.</span><span class="sxs-lookup"><span data-stu-id="669d9-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="669d9-114">Właściciel budżetu zatwierdza raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="669d9-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="669d9-115">Dodaj wiele elementów zatwierdzania, z których każdy zawiera jeden krok.</span><span class="sxs-lookup"><span data-stu-id="669d9-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="669d9-116">Można na przykład dodać osobny element zatwierdzania dla każdego z następujących kroków:</span><span class="sxs-lookup"><span data-stu-id="669d9-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="669d9-117">Kierownik pracownika zatwierdza raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="669d9-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="669d9-118">Właściciel budżetu zatwierdza raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="669d9-118">The budget owner approves the expense report.</span></span>
