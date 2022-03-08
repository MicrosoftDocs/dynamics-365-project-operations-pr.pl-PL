---
title: Uwagi dotyczące deweloperów na temat zatwierdzeń
description: Ta temat zawiera dodatkowe informacje dla deweloperów, na temat pracy z zatwierdzaniem.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991679"
---
# <a name="developer-notes-for-approvals"></a>Uwagi dotyczące deweloperów na temat zatwierdzeń

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rozwiązaniu Dynamics 365 Project Operations zawiera logikę walidacji, która zapewnia prawidłowe przejście rekordów przez etapy zatwierdzania. Poprawne przejścia między rekordami upewnij się, że: 

  - Wszystkie wiersze obsługi są tworzone w tabelach pokrewnych, takich jak arkusze i wartości rzeczywiste.
  - Przed kontynuowaniem osoba zatwierdzająca jest oznaczona jako **Osoba zatwierdzająca projekt** w projekcie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]