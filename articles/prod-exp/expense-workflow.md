---
title: Przepływ pracy zarządzania wydatkami
description: W tym temacie przedstawiono sposób korzystania z systemu przepływu pracy w Microsoft Dynamics 365 Finance w celu skonfigurowania procesu przeglądu raportów o wydatkach w zarządzaniu wydatkami.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271681"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="f29a9-103">Przepływ pracy zarządzania wydatkami</span><span class="sxs-lookup"><span data-stu-id="f29a9-103">Expense management workflow</span></span>

<span data-ttu-id="f29a9-104">Sposób korzystania z systemu przepływu pracy można dostosować w celu skonfigurowania procesu przeglądu raportów o wydatkach w zarządzaniu wydatkami.</span><span class="sxs-lookup"><span data-stu-id="f29a9-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="f29a9-105">Użytkownik może skonfigurować przepływ pracy, który korzysta z następujących kryteriów w celu określenia, kto zatwierdza raporty o wydatkach:</span><span class="sxs-lookup"><span data-stu-id="f29a9-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="f29a9-106">Hierarchia raportowania pracowników i wstępnie zdefiniowane ograniczenia zatwierdzania</span><span class="sxs-lookup"><span data-stu-id="f29a9-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="f29a9-107">Zatwierdzanie na wielu poziomach, które obsługuje zatwierdzanie tymczasowe i ostateczną osobę zatwierdzającą</span><span class="sxs-lookup"><span data-stu-id="f29a9-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="f29a9-108">Zakres finansowy i zakres odpowiedzialności projektu</span><span class="sxs-lookup"><span data-stu-id="f29a9-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="f29a9-109">Przypisywanie do określonych użytkowników lub grup użytkowników</span><span class="sxs-lookup"><span data-stu-id="f29a9-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="f29a9-110">Zatwierdzanie przepływu pracy można utworzyć na potrzeby raportów z wydatków, wniosków wyjazdowych, zaliczek w gotówce oraz zwrotu podatku VAT.</span><span class="sxs-lookup"><span data-stu-id="f29a9-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="f29a9-111">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="f29a9-111">**Example**</span></span>

<span data-ttu-id="f29a9-112">Poniższy proces stanowi przykład przepływu pracy Zarządzanie wydatkami w ramach raportu z wydatków.</span><span class="sxs-lookup"><span data-stu-id="f29a9-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="f29a9-113">Pracownik tworzy i zapisuje raport wydatków.</span><span class="sxs-lookup"><span data-stu-id="f29a9-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="f29a9-114">Pracownik przesyła raport do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="f29a9-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="f29a9-115">Osoba zatwierdzająca jest identyfikowana na podstawie reguł zdefiniowanych podczas konfigurowania przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="f29a9-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="f29a9-116">Osoba zatwierdzająca otrzymuje powiadomienie o przygotowaniu raportu o wydatkach do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="f29a9-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="f29a9-117">Sprawdza, a następnie zatwierdza raport z wydatków i potwierdza, że są spełnione następujące warunki:</span><span class="sxs-lookup"><span data-stu-id="f29a9-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="f29a9-118">Koszty nie naruszają żadnych zasad dotyczących wydatków.</span><span class="sxs-lookup"><span data-stu-id="f29a9-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="f29a9-119">Jeśli wydatek narusza zasadę, osoba zatwierdzająca weryfikuje, czy raport z wydatków zawiera prawidłowe uzasadnienie biznesowe.</span><span class="sxs-lookup"><span data-stu-id="f29a9-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="f29a9-120">Do raportu z wydatków są dołączone paragony w wersji cyfrowej.</span><span class="sxs-lookup"><span data-stu-id="f29a9-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="f29a9-121">Osoba zatwierdzająca zatwierdza raport o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="f29a9-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="f29a9-122">Raport o wydatkach jest przypisywany do koordynatora rozrachunków z klientami w celu zaksięgowania.</span><span class="sxs-lookup"><span data-stu-id="f29a9-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="f29a9-123">W zależności od tego, czy skonfigurowane jest automatyczne księgowanie, czy nie, ma miejsce jedno z następujących:</span><span class="sxs-lookup"><span data-stu-id="f29a9-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="f29a9-124">Jeśli skonfigurowano automatyczne księgowanie, raport o wydatkach jest przetwarzany w celu dokonania płatności, a stan raportu o wydatkach jest zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="f29a9-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="f29a9-125">Jeśli automatyczne księgowanie nie jest skonfigurowane, wtedy koordynator ds. rozrachunków z dostawcami weryfikuje, że wszystkie oryginalne paragony zostały przesłane i że zgadzają się z kosztami w raporcie z wydatków.</span><span class="sxs-lookup"><span data-stu-id="f29a9-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="f29a9-126">Wszystkie kody podatków wprowadzone w raporcie z wydatkami również muszą zostać sprawdzone pod kątem poprawności.</span><span class="sxs-lookup"><span data-stu-id="f29a9-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="f29a9-127">Dopiero po sprawdzeniu tych wymagań raport jest księgowany.</span><span class="sxs-lookup"><span data-stu-id="f29a9-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="f29a9-128">Po zaksięgowaniu raportu o wydatkach płatność jest zatwierdzana, a pracownik otrzymuje zwrot.</span><span class="sxs-lookup"><span data-stu-id="f29a9-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]