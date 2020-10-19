---
title: Księgowanie raportów wydatków
description: W tym temacie przedstawiono sposób księgowania raportów o wydatkach.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907421"
---
# <a name="post-expense-reports"></a><span data-ttu-id="603ef-103">Księgowanie raportów wydatków</span><span class="sxs-lookup"><span data-stu-id="603ef-103">Post expense reports</span></span>

<span data-ttu-id="603ef-104">Po zatwierdzeniu i przeniesieniu raportu wydatków do dziennika głównego można go opublikować.</span><span class="sxs-lookup"><span data-stu-id="603ef-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="603ef-105">Podczas księgowania raportu wydatków są identyfikowane wydatki kwalifikujące się do zwrotu podatku VAT.</span><span class="sxs-lookup"><span data-stu-id="603ef-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="603ef-106">Zadanie sprawdzania i odzyskiwania płatności VAT jest przypisywane do pracownika, który jest odpowiedzialny za sprawdzanie raportu z wydatków.</span><span class="sxs-lookup"><span data-stu-id="603ef-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="603ef-107">Jeśli wydatki w raporcie obciążają inną firmę niż ta, zatrudniająca pracownika, należy sprawdzić zarówno firmę obciążającą, jak i firmę obciążaną.</span><span class="sxs-lookup"><span data-stu-id="603ef-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="603ef-108">Na przykład pracownik, który przedstawił raport z wydatków, pracuje dla firmy DAT, ale ponosił koszty względem firmy DIR.</span><span class="sxs-lookup"><span data-stu-id="603ef-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="603ef-109">W tym przypadku DAT to firma obciążająca a DIR to firma obciążana.</span><span class="sxs-lookup"><span data-stu-id="603ef-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="603ef-110">Po sprawdzeniu wierszy dziennika można je zaksięgować w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="603ef-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="603ef-111">W celu zaksięgowania raportu z wydatków na stronie **Zatwierdzone raporty o wydatkach** wybierz raport o wydatkach, a następnie w okienku akcji wybierz pozycję **Księguj**.</span><span class="sxs-lookup"><span data-stu-id="603ef-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="603ef-112">Można również zaksięgować wszystkie raporty o wydatkach na liście w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="603ef-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="603ef-113">Zaznacz wszystkie raporty o wydatkach, a następnie wybierz pozycję **Księguj**.</span><span class="sxs-lookup"><span data-stu-id="603ef-113">Select all the expense reports, and then select **Post**.</span></span>
