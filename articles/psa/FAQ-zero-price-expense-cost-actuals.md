---
title: Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych kosztu wydatków?
description: Rozwiązywanie problemu, dlaczego ceny domyślnie wynoszą 0 w wartościach rzeczywistych kosztu wydatków.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082033"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych kosztu wydatków?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Te często zadawane pytanie dotyczy wartości rzeczywistych wydatków, gdzie klasa transakcji jest ustawiona na Wydatki a typ transakcji to Koszt.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Rozwiązywanie problemów związanych z kursem kosztów na wartościach rzeczywistych kosztu wydatków

Przejdź do odpowiedniego wydatku i upewnij się, że w polu wydatku wprowadzona została kwota. Jeśli źródłowy wpis dotyczący wydatku nie miał wypełnionego pola kwoty, znalazłeś problem.
 
Aby rozwiązać ten problem, należy ponownie utworzyć wpis wydatków wprowadzając prawidłową kwotę a następnie zatwierdzić go.
