---
title: Uwagi dotyczące deweloperów na temat zatwierdzeń
description: Ta temat zawiera dodatkowe informacje dla deweloperów, na temat pracy z zatwierdzaniem.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483961"
---
# <a name="developer-notes-for-approvals"></a>Uwagi dotyczące deweloperów na temat zatwierdzeń

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations zawiera logikę walidacji, która zapewnia prawidłowe przejście rekordów przez etapy zatwierdzania. Poprawne przejścia między rekordami upewnij się, że: 

  - Wszystkie wiersze obsługi są tworzone w tabelach pokrewnych, takich jak arkusze i wartości rzeczywiste.
  - Przed kontynuowaniem osoba zatwierdzająca jest oznaczona jako **Osoba zatwierdzająca projekt** w projekcie.
