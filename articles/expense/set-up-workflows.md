---
title: Konfigurowanie przepływu pracy do zarządzania wydatkami
description: Użytkownik może skonfigurować proces przepływu pracy służący do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082039"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="ca70e-103">Konfigurowanie przepływu pracy do zarządzania wydatkami</span><span class="sxs-lookup"><span data-stu-id="ca70e-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="ca70e-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="ca70e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca70e-105">Użytkownik może skonfigurować proces przepływu pracy do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków.</span><span class="sxs-lookup"><span data-stu-id="ca70e-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="ca70e-106">Można zdefiniować przepływy pracy dla raportów wydatków, wniosków wyjazdowych i żądań zaliczek na poczet wydatków.</span><span class="sxs-lookup"><span data-stu-id="ca70e-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ca70e-107">Przepływ pracy reprezentuje proces biznesowy i definiuje sposób przepływu dokumentu przez system.</span><span class="sxs-lookup"><span data-stu-id="ca70e-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="ca70e-108">Przepływ pracy określa również, kto musi zakończyć zadanie lub zatwierdzić dokument.</span><span class="sxs-lookup"><span data-stu-id="ca70e-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ca70e-109">Istnieje szereg korzyści płynących z korzystania z systemu przepływu pracy w organizacji:</span><span class="sxs-lookup"><span data-stu-id="ca70e-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="ca70e-110">**Spójność procesu** : można zdefiniować proces zatwierdzania dla określonych dokumentów, takich jak zapotrzebowania na zakup i raporty o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="ca70e-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ca70e-111">Korzystanie z systemu przepływu pracy pomaga zagwarantować, że dokumenty zostaną przetwarzane i będą zatwierdzone w sposób spójny i skuteczny.</span><span class="sxs-lookup"><span data-stu-id="ca70e-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="ca70e-112">**Widoczność procesu** : można śledzić stan, historię i metryki wydajności dotyczące konkretnego wystąpienia przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="ca70e-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ca70e-113">Pomaga to w określeniu, czy w celu zwiększenia efektywności należy wprowadzić zmiany w przepływie pracy.</span><span class="sxs-lookup"><span data-stu-id="ca70e-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="ca70e-114">**Scentralizowana lista pracy** : użytkownicy mogą wyświetlać scentralizowaną listę zadań w celu wyświetlenia przydzielonych im zadań i zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="ca70e-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="ca70e-115">Typy przepływu pracy</span><span class="sxs-lookup"><span data-stu-id="ca70e-115">Workflow types</span></span>

<span data-ttu-id="ca70e-116">W poniższej tabeli przedstawiono typy przepływów pracy, które można tworzyć w module **Zarządzanie wydatkami**.</span><span class="sxs-lookup"><span data-stu-id="ca70e-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="ca70e-117"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ca70e-118"><strong>Tego typu należy używać, aby przeprowadzić</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="ca70e-119"><strong>Automatyczne zatwierdzanie raportów wydatków</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="ca70e-120">Tworzenie przepływów pracy zatwierdzania raportów o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="ca70e-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ca70e-121"><strong>Automatyczne księgowanie raportów wydatków</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ca70e-122">Tworzenie przepływów pracy automatycznego księgowania raportów o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="ca70e-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ca70e-123"><strong>Pozycja wydatku</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ca70e-124">Tworzenie przepływów pracy zatwierdzania raportów dla elementów wiersza w raportach dotyczących wydatków.</span><span class="sxs-lookup"><span data-stu-id="ca70e-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ca70e-125"><strong>Automatyczne księgowanie pozycji wiersza wydatków</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ca70e-126">Tworzenie przepływów pracy automatycznego księgowania elementów wiersza w raportach dotyczących wydatków.</span><span class="sxs-lookup"><span data-stu-id="ca70e-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ca70e-127"><strong>Wnioski wyjazdowe</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ca70e-128">Tworzenie przepływów pracy dla zatwierdzania wniosków wyjazdowych.</span><span class="sxs-lookup"><span data-stu-id="ca70e-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ca70e-129"><strong>Zaliczka gotówkowa — anulowanie</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ca70e-130">Tworzenie przepływów pracy zatwierdzania dla wniosków o zaliczkę w gotówce.</span><span class="sxs-lookup"><span data-stu-id="ca70e-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ca70e-131"><strong>Zwrot podatku VAT</strong></span><span class="sxs-lookup"><span data-stu-id="ca70e-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ca70e-132">Utwórz przepływy pracy zatwierdzenia w celu odzyskania podatku VAT.</span><span class="sxs-lookup"><span data-stu-id="ca70e-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
