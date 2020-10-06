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
# <a name="update-estimate-at-completion"></a><span data-ttu-id="e0310-103">Aktualizacja szacowania przy zakończeniu</span><span class="sxs-lookup"><span data-stu-id="e0310-103">Update estimate at completion</span></span>

<span data-ttu-id="e0310-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="e0310-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e0310-105">Menedżerowie projektu często rewidują oryginalne wartości szacunkowe zadania.</span><span class="sxs-lookup"><span data-stu-id="e0310-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e0310-106">Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu.</span><span class="sxs-lookup"><span data-stu-id="e0310-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e0310-107">Niemniej n ie zalecamy, aby menedżerowie projektu zmieniali liczby podstawowe, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.</span><span class="sxs-lookup"><span data-stu-id="e0310-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e0310-108">Istnieją dwa sposoby ponownego prognozowania nakładu pracy na zadania:</span><span class="sxs-lookup"><span data-stu-id="e0310-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="e0310-109">Zastąpienie domyślnej wartości czasu wymaganego do wykonania zadania (ETC) nową wartością szacunkową rzeczywistego pozostałego nakładu pracy na zadanie.</span><span class="sxs-lookup"><span data-stu-id="e0310-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e0310-110">Zastąpienie domyślnej wartości procentowej postępu nową wartością rzeczywistego postępu.</span><span class="sxs-lookup"><span data-stu-id="e0310-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e0310-111">Każda z tych metod powoduje ponowne obliczenie wartości ETC zadania, szacowania przy zakończeniu (EAC) i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem.</span><span class="sxs-lookup"><span data-stu-id="e0310-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e0310-112">Wartości EAC, ETC i procent postępu w zadaniach sumarycznych są obliczane ponownie i dają nową projekcję odchylenia.</span><span class="sxs-lookup"><span data-stu-id="e0310-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>