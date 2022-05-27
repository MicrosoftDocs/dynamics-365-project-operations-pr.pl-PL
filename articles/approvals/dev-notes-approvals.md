---
title: Uwagi dotyczące deweloperów na temat zatwierdzeń
description: Ta temat zawiera dodatkowe informacje dla deweloperów, na temat pracy z zatwierdzaniem.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579733"
---
# <a name="developer-notes-for-approvals"></a>Uwagi dotyczące deweloperów na temat zatwierdzeń

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rozwiązaniu Dynamics 365 Project Operations zawiera logikę walidacji, która zapewnia prawidłowe przejście rekordów przez etapy zatwierdzania. Poprawne przejścia między rekordami upewnij się, że: 

  - Wszystkie wiersze obsługi są tworzone w tabelach pokrewnych, takich jak arkusze i wartości rzeczywiste.
  - Przed kontynuowaniem osoba zatwierdzająca jest oznaczona jako **Osoba zatwierdzająca projekt** w projekcie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]