---
title: Księgowanie raportów wydatków
description: W tym artykule opisano sposób księgowania raportów wydatków.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524883"
---
# <a name="post-expense-reports"></a>Księgowanie raportów wydatków

Po zatwierdzeniu i przeniesieniu raportu wydatków do dziennika głównego można go opublikować. Podczas księgowania raportu wydatków są identyfikowane wydatki kwalifikujące się do zwrotu podatku VAT. Zadanie sprawdzania i odzyskiwania płatności VAT jest przypisywane do pracownika, który jest odpowiedzialny za sprawdzanie raportu z wydatków.

Jeśli wydatki w raporcie obciążają inną firmę niż ta, zatrudniająca pracownika, należy sprawdzić zarówno firmę obciążającą, jak i firmę obciążaną. Na przykład pracownik, który przedstawił raport z wydatków, pracuje dla firmy DAT, ale ponosił koszty względem firmy DIR. W tym przypadku DAT to firma obciążająca a DIR to firma obciążana. Po sprawdzeniu wierszy dziennika można je zaksięgować w księdze głównej.

W celu zaksięgowania raportu z wydatków na stronie **Zatwierdzone raporty o wydatkach** wybierz raport o wydatkach, a następnie w okienku akcji wybierz pozycję **Księguj**.

Można również zaksięgować wszystkie raporty o wydatkach na liście w tym samym czasie. Zaznacz wszystkie raporty o wydatkach, a następnie wybierz pozycję **Księguj**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Włącz możliwość księgowania zobowiązań z tytułu kosztów w walucie sprzedawcy dla metody płatności gotówkowej

Funkcja **Możliwość księgowania zobowiązań z tytułu wydatków w walucie sprzedawcy dla metody płatności gotówkowej** umożliwia księgowanie raportów wydatków w walucie sprzedawcy dla metody płatności gotówkowej.

Obecnie, kiedy zgłaszasz wydatki gotówkowe, raporty wydatków są księgowane w walucie księgowej. Ze względu na przeliczanie kwot między walutą transakcji, walutą księgową i walutą sprzedawcy, sprzedawcy wypłacana jest niepoprawna kwota, jeśli data transakcji wydatku i data faktycznej płatności mają różne kursy wymiany.

Dzięki tej funkcji saldo sprzedawcy zostanie zapisane w walucie sprzedawcy podczas księgowania raportu wydatków.

1. Wybierz kolejno pozycje **Obszary robocze** \> **Zarządzanie funkcjami**.
2. Na liście znajdź i wybierz **Możliwość księgowania zobowiązania z tytułu kosztów w walucie dostawcy dla metody płatności gotówkowej**, a następnie wybierz **Włącz teraz**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
