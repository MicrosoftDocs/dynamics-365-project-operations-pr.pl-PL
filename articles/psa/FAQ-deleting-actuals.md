---
title: Dlaczego nie mogę usunąć rekordów z encji Wartości rzeczywiste?
description: W tym temacie zamieszczono informacje dotyczące przyczyny niemożności usunięcia rekordów z encji Wartości rzeczywiste.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002884"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Dlaczego nie mogę usunąć rekordów z encji Wartości rzeczywiste?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Program Project Service Automation (PSA) nie zezwala na usuwanie wartości rzeczywistych, ponieważ są one źródłem prawdziwych informacji dla transakcji powodujących skutki finansowe w dalszych systemach, takich jak księga główna. Jeśli można byłoby usuwać wartości rzeczywiste, ktoś mógłby kwestionować rzetelność transakcji w sprawozdawczości finansowej. Aby ustanowić dziennik inspekcji, klienci powinni używać arkuszy do tworzenia transakcji kompensacyjnych.



[!INCLUDE[footer-include](../includes/footer-banner.md)]