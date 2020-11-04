---
title: Aktualizacja szacowania przy zakończeniu
description: W tym temacie zamieszczono informacje dotyczące aktualizowania projekcji w projekcie.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082195"
---
# <a name="update-estimate-at-completion"></a>Aktualizacja szacowania przy zakończeniu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Menedżerowie projektu często rewidują oryginalne wartości szacunkowe zadania. Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu. Niemniej n ie zalecamy, aby menedżerowie projektu zmieniali liczby podstawowe, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.

Istnieją dwa sposoby ponownego prognozowania nakładu pracy na zadania:

- Zastąpienie domyślnej wartości czasu wymaganego do wykonania zadania (ETC) nową wartością szacunkową rzeczywistego pozostałego nakładu pracy na zadanie. 
- Zastąpienie domyślnej wartości procentowej postępu nową wartością rzeczywistego postępu.

Każda z tych metod powoduje ponowne obliczenie wartości ETC zadania, szacowania przy zakończeniu (EAC) i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem. Wartości EAC, ETC i procent postępu w zadaniach sumarycznych są obliczane ponownie i dają nową projekcję odchylenia.
