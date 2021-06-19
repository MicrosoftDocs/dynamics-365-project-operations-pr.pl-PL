---
title: Księgowanie raportu wydatków
description: W tym temacie przedstawiono sposób księgowania raportu z wydatków w księdze głównej.
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24dd945ea7ea73b37806e209a90d5301ac09d956
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005804"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="f48ee-103">Księgowanie raportu wydatków</span><span class="sxs-lookup"><span data-stu-id="f48ee-103">Post an expense report</span></span>

<span data-ttu-id="f48ee-104">Po zatwierdzeniu i przeniesieniu raportu wydatków do dziennika głównego można go opublikować w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="f48ee-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="f48ee-105">Podczas księgowania raportu wydatków są identyfikowane wydatki kwalifikujące się do zwrotu podatku VAT.</span><span class="sxs-lookup"><span data-stu-id="f48ee-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="f48ee-106">Zadanie sprawdzania i odzyskiwania płatności VAT jest przypisywane do pracownika, który jest odpowiedzialny za sprawdzanie raportu z wydatków.</span><span class="sxs-lookup"><span data-stu-id="f48ee-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="f48ee-107">Jeśli wydatki w raporcie obciążają inną firmę niż ta, zatrudniająca pracownika, należy sprawdzić zarówno firmę obciążającą, jak i firmę obciążaną wydatkami.</span><span class="sxs-lookup"><span data-stu-id="f48ee-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="f48ee-108">Na przykład pracownik, który przedstawił raport z wydatków, pracuje dla firmy DAT, ale ponosił koszty względem firmy DIR.</span><span class="sxs-lookup"><span data-stu-id="f48ee-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="f48ee-109">W tym przypadku DAT to firma obciążająca a DIR to firma obciążana.</span><span class="sxs-lookup"><span data-stu-id="f48ee-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="f48ee-110">Po sprawdzeniu wierszy dziennika można je zaksięgować w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="f48ee-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="f48ee-111">W celu zaksięgowania raportu z wydatków na stronie **Zatwierdzone raporty o wydatkach** wybierz raport o wydatkach, a następnie w okienku akcji wybierz pozycję **Księguj**.</span><span class="sxs-lookup"><span data-stu-id="f48ee-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="f48ee-112">Można również zaksięgować wszystkie raporty o wydatkach na liście w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="f48ee-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="f48ee-113">Zaznacz wszystkie raporty o wydatkach, a następnie wybierz pozycję **Księguj**.</span><span class="sxs-lookup"><span data-stu-id="f48ee-113">Select all the expense reports, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]