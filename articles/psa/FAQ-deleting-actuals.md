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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286081"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="cf0ab-103">Dlaczego nie mogę usunąć rekordów z encji Wartości rzeczywiste?</span><span class="sxs-lookup"><span data-stu-id="cf0ab-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cf0ab-104">Program Project Service Automation (PSA) nie zezwala na usuwanie wartości rzeczywistych, ponieważ są one źródłem prawdziwych informacji dla transakcji powodujących skutki finansowe w dalszych systemach, takich jak księga główna.</span><span class="sxs-lookup"><span data-stu-id="cf0ab-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="cf0ab-105">Jeśli można byłoby usuwać wartości rzeczywiste, ktoś mógłby kwestionować rzetelność transakcji w sprawozdawczości finansowej.</span><span class="sxs-lookup"><span data-stu-id="cf0ab-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="cf0ab-106">Aby ustanowić dziennik inspekcji, klienci powinni używać arkuszy do tworzenia transakcji kompensacyjnych.</span><span class="sxs-lookup"><span data-stu-id="cf0ab-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]