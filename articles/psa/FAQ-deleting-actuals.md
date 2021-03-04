---
title: Dlaczego nie mogę usunąć rekordów z encji Wartości rzeczywiste?
description: W tym temacie zamieszczono informacje dotyczące przyczyny niemożności usunięcia rekordów z encji Wartości rzeczywiste.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148971"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="6c7eb-103">Dlaczego nie mogę usunąć rekordów z encji Wartości rzeczywiste?</span><span class="sxs-lookup"><span data-stu-id="6c7eb-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6c7eb-104">Program Project Service Automation (PSA) nie zezwala na usuwanie wartości rzeczywistych, ponieważ są one źródłem prawdziwych informacji dla transakcji powodujących skutki finansowe w dalszych systemach, takich jak księga główna.</span><span class="sxs-lookup"><span data-stu-id="6c7eb-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="6c7eb-105">Jeśli można byłoby usuwać wartości rzeczywiste, ktoś mógłby kwestionować rzetelność transakcji w sprawozdawczości finansowej.</span><span class="sxs-lookup"><span data-stu-id="6c7eb-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="6c7eb-106">Aby ustanowić dziennik inspekcji, klienci powinni używać arkuszy do tworzenia transakcji kompensacyjnych.</span><span class="sxs-lookup"><span data-stu-id="6c7eb-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

