---
title: Eliminowanie oszacowania projektu
description: W tym temacie zamieszczono informacje dotyczące eliminowania oszacowania projektu po jego zakończeniu.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270691"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="5d5ed-103">Eliminowanie oszacowania projektu</span><span class="sxs-lookup"><span data-stu-id="5d5ed-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d5ed-104">Szacowania projektu zapewniają widok finansowy dla prac oszacowanych i zaplanowanych dla projektu.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="5d5ed-105">Aby pracować z oszacowaniami projektu, należy załączyć projekt do projektu szacowanego.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="5d5ed-106">Projekt szacowany jest zawsze oparty na projekcie istniejącym, ale wiele projektów może odwoływać się do jednego projektu szacowanego.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="5d5ed-107">Do projektów szacowanych można dołączać tylko projekty o stałej cenie i projekty inwestycyjne, a te projekty muszą należeć do tej samej grupy projektów jak projekt szacowany.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="5d5ed-108">W celu wyeliminowania projektu szacowanego należy go zakończyć.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="5d5ed-109">Poniższe kroki opisują sposób eliminacji oszacowania.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="5d5ed-110">Przejdź do **Zarządzanie projektami i księgowanie** > **Wszystkie projekty** i wybierz projekt.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="5d5ed-111">Na karcie **Zarządzanie** wybierz pozycję **Oszacowania** i na stronie **Oszacowania** wybierz pozycję **Eliminuj**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="5d5ed-112">Na stronie **Eliminowanie oszacowania** na karcie **Ogólne** ustaw następujące opcje:</span><span class="sxs-lookup"><span data-stu-id="5d5ed-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="5d5ed-113">**Kod okresu**: należy wybrać kod okresu, aby wybrać odpowiednie szacowanie projektu.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="5d5ed-114">**Data szacowania**: należy wybrać datę oszacowania dotyczącą eliminacji.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="5d5ed-115">**Usuń z ostrzeżeniami PWT**: Włącz tę opcję, aby zapewnić powiadamianie w przypadku wyeliminowania oszacowania skojarzonego z pracą w toku (PWT).</span><span class="sxs-lookup"><span data-stu-id="5d5ed-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="5d5ed-116">Jeśli ta opcja nie jest włączona, eliminacja nie może być kontynuowana, jeśli istnieje nieoszacowana transakcja.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="5d5ed-117">Ta opcja jest dostępna tylko wtedy, gdy do projektu szacowanego zastosowano eliminację.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="5d5ed-118">Nie jest ona dostępna, jeśli używane jest księgowanie okresowe.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="5d5ed-119">To ustawienie działa z ustawieniami na karcie **Szacowanie** na stronie **Parametry projektu**, w grupie pól **Zezwalaj na eliminację, kiedy istnieją nieoszacowane transakcje**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="5d5ed-120">**Ustaw etap jako gotowy**: włącz tę opcję, aby ustawić etap projektu szacowanego na **Zakończony** po przeprowadzeniu eliminacji.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="5d5ed-121">**Drukuj listę oszacowań**: służy do wybierania informacji, które mają być uwzględnione podczas drukowania listy oszacowań.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="5d5ed-122">**Pokaż dziennik informacyjny**: włącz tę opcję, aby wyświetlić dziennik informacyjny.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="5d5ed-123">**Data księgowania**: należy wybrać datę księgowania w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="5d5ed-124">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-124">Select **OK**.</span></span>
5. <span data-ttu-id="5d5ed-125">Po zakończeniu procesu eliminacji dla wyeliminowanego projektu szacowanego jest wyświetlany element o ujemnych wartościach.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="5d5ed-126">Jeśli nie zachodzi potrzeba wyeliminowania oszacowania, można wybrać wyeliminowaną wartość szacunkową i wybrać pozycję **Cofnij eliminację**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]