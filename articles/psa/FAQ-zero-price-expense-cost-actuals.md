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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122131"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="5f39c-103">Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych kosztu wydatków?</span><span class="sxs-lookup"><span data-stu-id="5f39c-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5f39c-104">Te często zadawane pytanie dotyczy wartości rzeczywistych wydatków, gdzie klasa transakcji jest ustawiona na Wydatki a typ transakcji to Koszt.</span><span class="sxs-lookup"><span data-stu-id="5f39c-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="5f39c-105">Rozwiązywanie problemów związanych z kursem kosztów na wartościach rzeczywistych kosztu wydatków</span><span class="sxs-lookup"><span data-stu-id="5f39c-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="5f39c-106">Przejdź do odpowiedniego wydatku i upewnij się, że w polu wydatku wprowadzona została kwota.</span><span class="sxs-lookup"><span data-stu-id="5f39c-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="5f39c-107">Jeśli źródłowy wpis dotyczący wydatku nie miał wypełnionego pola kwoty, znalazłeś problem.</span><span class="sxs-lookup"><span data-stu-id="5f39c-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="5f39c-108">Aby rozwiązać ten problem, należy ponownie utworzyć wpis wydatków wprowadzając prawidłową kwotę a następnie zatwierdzić go.</span><span class="sxs-lookup"><span data-stu-id="5f39c-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
