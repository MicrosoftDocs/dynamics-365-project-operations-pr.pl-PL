---
title: Analiza ofert projektów
description: Ten temat zawiera informacje na temat analizowania ofert w projektach.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754267"
---
# <a name="analysis-of-project-quotes"></a>Analiza ofert projektów

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Program Dynamics 365 Project Service Automation analizuje oferty do projektów w celu oszacowania rentowności. Analizuje również, w jakim stopniu oferta jest dopasowana do oczekiwań klienta w kwestii daty dostawy lub wykonania oraz oczekiwań budżetowych.

## <a name="profitability-analysis"></a>Analiza rentowności

Rozwiązanie Project Service Automation analizuje rentowność, korzystając z kryteriów marży brutto i skorygowanej marży brutto.

- Marża brutto jest obliczana za pomocą poniższego wzoru:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Skorygowana marża brutto jest obliczana za pomocą poniższego wzoru:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Jeśli wartości marży brutto i skorygowanej marży brutto różnią bardzo się różnią, duża część pracy w ofercie jest klasyfikowana jako niepłatna.

## <a name="analysis-of-customer-expectations"></a>Analiza oczekiwań klienta

Można analizować oferty oraz generować wykresy oczekiwań klientów w odniesieniu do harmonogramu i budżetu po wprowadzeniu wartości w następujących polach:

- Pole **Żądana data dostawy** w nagłówku oferty.
- Pole **Budżet klienta** dla każdego wiersza oferty (w przypadku wierszy opartych na projektach i na wierszy opartych na produktach).

Analiza oczekiwań klienta w kwestii harmonogramu polega na porównaniu najpóźniejszej daty zakończenia w szczegółach wiersza oferty z żądaną datą dostawy we wszystkich wierszach oferty.

Analiza oczekiwań klientów w kwestii budżetu polega na porównaniu sumy całkowitego budżetu klienta z kwotą oferty we wszystkich wierszach oferty.
