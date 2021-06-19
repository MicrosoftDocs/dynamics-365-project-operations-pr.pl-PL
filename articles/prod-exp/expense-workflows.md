---
title: Konfigurowanie przepływu pracy do zarządzania wydatkami
description: Użytkownik może skonfigurować proces przepływu pracy do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005129"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="7d536-103">Konfigurowanie przepływu pracy do zarządzania wydatkami</span><span class="sxs-lookup"><span data-stu-id="7d536-103">Set up Expense management workflows</span></span>

<span data-ttu-id="7d536-104">Użytkownik może skonfigurować proces przepływu pracy służący do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków.</span><span class="sxs-lookup"><span data-stu-id="7d536-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="7d536-105">Dokumenty, dla których można zdefiniować przepływy pracy to raporty z wydatków, wnioski wyjazdowe i żądania zaliczek na poczet wydatków.</span><span class="sxs-lookup"><span data-stu-id="7d536-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="7d536-106">Przepływ pracy reprezentuje proces biznesowy.</span><span class="sxs-lookup"><span data-stu-id="7d536-106">A workflow represents a business process.</span></span> <span data-ttu-id="7d536-107">Definiuje sposób przepływu dokumentu za pośrednictwem systemu oraz wskazuje, kto musi zakończyć zadanie lub zatwierdzić dokument.</span><span class="sxs-lookup"><span data-stu-id="7d536-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="7d536-108">Istnieje szereg korzyści płynących z korzystania z systemu przepływu pracy w organizacji:</span><span class="sxs-lookup"><span data-stu-id="7d536-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="7d536-109">**Spójność procesu** — można zdefiniować proces zatwierdzania dla określonych dokumentów, takich jak zapotrzebowania na zakup i raporty o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="7d536-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="7d536-110">Korzystanie z systemu przepływu pracy pomaga zagwarantować, że dokumenty zostaną przetwarzane i będą zatwierdzone w sposób spójny i skuteczny.</span><span class="sxs-lookup"><span data-stu-id="7d536-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="7d536-111">Widoczność procesu — można śledzić stan, historię i metryki wydajności dotyczące konkretnego wystąpienia przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="7d536-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="7d536-112">Pomaga to w określeniu, czy w celu zwiększenia efektywności należy wprowadzić zmiany w przepływie pracy.</span><span class="sxs-lookup"><span data-stu-id="7d536-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="7d536-113">Scentralizowana lista pracy — użytkownicy mogą wyświetlać scentralizowaną listę zadań w celu wyświetlenia przydzielonych im zadań i zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="7d536-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="7d536-114">**Typy relacji między obiektami do utworzenia**</span><span class="sxs-lookup"><span data-stu-id="7d536-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="7d536-115">W poniższej tabeli przedstawiono typy przepływów pracy, które można tworzyć w module **Wydatków**.</span><span class="sxs-lookup"><span data-stu-id="7d536-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="7d536-116"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="7d536-117"><strong>Tego typu należy używać, aby przeprowadzić</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="7d536-118"><strong>Raport z wydatków</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="7d536-119">Tworzenie przepływów pracy zatwierdzania raportów o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="7d536-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="7d536-120"><strong>Automatyczne księgowanie raportów wydatków</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="7d536-121">Tworzenie przepływów pracy automatycznego księgowania raportów o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="7d536-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="7d536-122"><strong>Pozycja wydatku</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="7d536-123">Tworzenie przepływów pracy zatwierdzania raportów dla elementów wiersza w raportach dotyczących wydatków.</span><span class="sxs-lookup"><span data-stu-id="7d536-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="7d536-124"><strong>Automatyczne księgowanie pozycji wiersza wydatków</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="7d536-125">Tworzenie przepływów pracy automatycznego księgowania elementów wiersza w raportach dotyczących wydatków.</span><span class="sxs-lookup"><span data-stu-id="7d536-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="7d536-126"><strong>Wnioski wyjazdowe</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="7d536-127">Tworzenie przepływów pracy dla zatwierdzania wniosków wyjazdowych.</span><span class="sxs-lookup"><span data-stu-id="7d536-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="7d536-128"><strong>Zaliczka gotówkowa — anulowanie</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="7d536-129">Tworzenie przepływów pracy zatwierdzania dla wniosków o zaliczkę w gotówce.</span><span class="sxs-lookup"><span data-stu-id="7d536-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="7d536-130"><strong>Zwrot podatku VAT</strong></span><span class="sxs-lookup"><span data-stu-id="7d536-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="7d536-131">Utwórz przepływy pracy zatwierdzenia w celu odzyskania podatku VAT.</span><span class="sxs-lookup"><span data-stu-id="7d536-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]