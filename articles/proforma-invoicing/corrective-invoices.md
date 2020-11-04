---
title: Faktury skorygowane
description: Ten temat zawiera informacje o skorygowanych fakturach.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082180"
---
# <a name="corrected-invoices"></a>Faktury skorygowane

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Potwierdzone faktury w PSA można korygować. W przypadku edytowania potwierdzonej faktury jest tworzona wersja robocza skorygowanej faktury. Ponieważ założono, że mają zostać wyzerowane wszystkie transakcje i ilości z oryginalnej faktury, ta faktura skorygowana zawiera wszystkie transakcje z oryginalnej faktury, a wszystkie jej ilości są równe 0 (zero).

Jeśli żadne transakcje nie wymagają korekty, można je usunąć z wersji roboczej faktury korygującej. Aby odwrócić lub dokonać zwrotu tylko ilości częściowej, można edytować pole ilość w szczegółach wiersza. Po otwarciu szczegółów wiersza faktury jest wyświetlana oryginalna ilość faktury. Następnie można edytować bieżącą ilość na fakturze, tak aby była mniejsza lub większa niż oryginalna ilość na fakturze.

Po potwierdzeniu faktury korygującej oryginalna rozliczona wartość rzeczywista sprzedaży jest cofana i system tworzy nową wartość rzeczywistą rozliczonej sprzedaży. Jeśli ilość została zmniejszona, różnica spowoduje utworzenie nowej nierozliczonej wartości rzeczywistej sprzedaży. Jeśli na przykład oryginalna rozliczona sprzedaż trwała 8 godzin, a wiersz faktury korygującej ograniczył ilość do sześciu godzin, oryginalny wiersz wyliczonych transakcji jest wycofany i utworzone są dwie nowe wartości rzeczywiste:

- Rozliczona wartość rzeczywista za sześć godzin.
- Nierozliczona sprzedaż za pozostałe dwie godziny. Ta transakcja może być rozliczona później lub oznakowana jako niepłatna, w zależności od ustaleń z klientem.
