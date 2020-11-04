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
# <a name="update-estimate-at-completion"></a><span data-ttu-id="98636-103">Aktualizacja szacowania przy zakończeniu</span><span class="sxs-lookup"><span data-stu-id="98636-103">Update estimate at completion</span></span>

<span data-ttu-id="98636-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="98636-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98636-105">Menedżerowie projektu często rewidują oryginalne wartości szacunkowe zadania.</span><span class="sxs-lookup"><span data-stu-id="98636-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="98636-106">Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu.</span><span class="sxs-lookup"><span data-stu-id="98636-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="98636-107">Niemniej n ie zalecamy, aby menedżerowie projektu zmieniali liczby podstawowe, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.</span><span class="sxs-lookup"><span data-stu-id="98636-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="98636-108">Istnieją dwa sposoby ponownego prognozowania nakładu pracy na zadania:</span><span class="sxs-lookup"><span data-stu-id="98636-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="98636-109">Zastąpienie domyślnej wartości czasu wymaganego do wykonania zadania (ETC) nową wartością szacunkową rzeczywistego pozostałego nakładu pracy na zadanie.</span><span class="sxs-lookup"><span data-stu-id="98636-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="98636-110">Zastąpienie domyślnej wartości procentowej postępu nową wartością rzeczywistego postępu.</span><span class="sxs-lookup"><span data-stu-id="98636-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="98636-111">Każda z tych metod powoduje ponowne obliczenie wartości ETC zadania, szacowania przy zakończeniu (EAC) i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem.</span><span class="sxs-lookup"><span data-stu-id="98636-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="98636-112">Wartości EAC, ETC i procent postępu w zadaniach sumarycznych są obliczane ponownie i dają nową projekcję odchylenia.</span><span class="sxs-lookup"><span data-stu-id="98636-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
