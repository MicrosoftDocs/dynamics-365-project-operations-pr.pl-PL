---
title: Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych kosztu wydatków?
description: Rozwiązywanie problemu, dlaczego ceny domyślnie wynoszą 0 w wartościach rzeczywistych kosztu wydatków.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146361"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="53187-103">Dlaczego cena domyślnie jest równa zero w wartościach rzeczywistych kosztu wydatków</span><span class="sxs-lookup"><span data-stu-id="53187-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="53187-104">Te często zadawane pytanie dotyczy wartości rzeczywistych wydatków, gdzie klasa transakcji jest ustawiona na Wydatki a typ transakcji to Koszt.</span><span class="sxs-lookup"><span data-stu-id="53187-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="53187-105">Rozwiązywanie problemów związanych z kursem kosztów na wartościach rzeczywistych kosztu wydatków</span><span class="sxs-lookup"><span data-stu-id="53187-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="53187-106">Przejdź do odpowiedniego wydatku i upewnij się, że w polu wydatku wprowadzona została kwota.</span><span class="sxs-lookup"><span data-stu-id="53187-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="53187-107">Jeśli źródłowy wpis dotyczący wydatku nie miał wypełnionego pola kwoty, znalazłeś problem.</span><span class="sxs-lookup"><span data-stu-id="53187-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="53187-108">Aby rozwiązać ten problem, należy ponownie utworzyć wpis wydatków wprowadzając prawidłową kwotę a następnie zatwierdzić go.</span><span class="sxs-lookup"><span data-stu-id="53187-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
