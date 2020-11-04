---
title: Dlaczego nie mogę usunąć rekordów z encji Wartości rzeczywiste?
description: W tym temacie zamieszczono informacje dotyczące przyczyny niemożności usunięcia rekordów z encji Wartości rzeczywiste.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082138"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="dfbc9-103">Dlaczego nie mogę usunąć rekordów z encji Wartości rzeczywiste?</span><span class="sxs-lookup"><span data-stu-id="dfbc9-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dfbc9-104">Program Project Service Automation (PSA) nie zezwala na usuwanie wartości rzeczywistych, ponieważ są one źródłem prawdziwych informacji dla transakcji powodujących skutki finansowe w dalszych systemach, takich jak księga główna.</span><span class="sxs-lookup"><span data-stu-id="dfbc9-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="dfbc9-105">Jeśli można byłoby usuwać wartości rzeczywiste, ktoś mógłby kwestionować rzetelność transakcji w sprawozdawczości finansowej.</span><span class="sxs-lookup"><span data-stu-id="dfbc9-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="dfbc9-106">Aby ustanowić dziennik inspekcji, klienci powinni używać arkuszy do tworzenia transakcji kompensacyjnych.</span><span class="sxs-lookup"><span data-stu-id="dfbc9-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

