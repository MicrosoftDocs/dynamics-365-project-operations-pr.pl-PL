---
title: Uwagi dotyczące deweloperów na temat zatwierdzeń
description: W tym artykule przedstawiono dodatkowe informacje dla deweloperów na temat pracy z zatwierdzeniami.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924765"
---
# <a name="developer-notes-for-approvals"></a>Uwagi dotyczące deweloperów na temat zatwierdzeń

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rozwiązaniu Dynamics 365 Project Operations zawiera logikę walidacji, która zapewnia prawidłowe przejście rekordów przez etapy zatwierdzania. Poprawne przejścia między rekordami upewnij się, że: 

  - Wszystkie wiersze obsługi są tworzone w tabelach pokrewnych, takich jak arkusze i wartości rzeczywiste.
  - Przed kontynuowaniem osoba zatwierdzająca jest oznaczona jako **Osoba zatwierdzająca projekt** w projekcie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]