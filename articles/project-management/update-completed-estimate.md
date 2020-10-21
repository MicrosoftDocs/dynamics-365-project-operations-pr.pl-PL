---
title: Aktualizacja szacowania przy zakończeniu
description: W tym temacie zamieszczono informacje dotyczące aktualizowania projekcji w projekcie.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897779"
---
# <a name="update-estimate-at-completion"></a>Aktualizacja szacowania przy zakończeniu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Menedżerowie projektu często rewidują oryginalne wartości szacunkowe zadania. Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu. Niemniej n ie zalecamy, aby menedżerowie projektu zmieniali liczby podstawowe, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.

Istnieją dwa sposoby ponownego prognozowania nakładu pracy na zadania:

- Zastąpienie domyślnej wartości czasu wymaganego do wykonania zadania (ETC) nową wartością szacunkową rzeczywistego pozostałego nakładu pracy na zadanie. 
- Zastąpienie domyślnej wartości procentowej postępu nową wartością rzeczywistego postępu.

Każda z tych metod powoduje ponowne obliczenie wartości ETC zadania, szacowania przy zakończeniu (EAC) i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem. Wartości EAC, ETC i procent postępu w zadaniach sumarycznych są obliczane ponownie i dają nową projekcję odchylenia.
