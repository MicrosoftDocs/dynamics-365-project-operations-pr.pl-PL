---
title: Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych kosztu wydatków?
description: Rozwiązywanie problemu, dlaczego ceny domyślnie wynoszą 0 w wartościach rzeczywistych kosztu wydatków.
author: rumant
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
ms.openlocfilehash: a6e971ff0477d5a9cb8652541095538b9f9039c0870362077218df609871ed4f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990959"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Dlaczego cena domyślnie jest równa zero w wartościach rzeczywistych kosztu wydatków

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Te często zadawane pytanie dotyczy wartości rzeczywistych wydatków, gdzie klasa transakcji jest ustawiona na Wydatki a typ transakcji to Koszt.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Rozwiązywanie problemów związanych z kursem kosztów na wartościach rzeczywistych kosztu wydatków

Przejdź do odpowiedniego wydatku i upewnij się, że w polu wydatku wprowadzona została kwota. Jeśli źródłowy wpis dotyczący wydatku nie miał wypełnionego pola kwoty, znalazłeś problem.
 
Aby rozwiązać ten problem, należy ponownie utworzyć wpis wydatków wprowadzając prawidłową kwotę a następnie zatwierdzić go.


[!INCLUDE[footer-include](../includes/footer-banner.md)]