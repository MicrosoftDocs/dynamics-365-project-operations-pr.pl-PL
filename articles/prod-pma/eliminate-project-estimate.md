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
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082065"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="c1518-103">Eliminowanie oszacowania projektu</span><span class="sxs-lookup"><span data-stu-id="c1518-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1518-104">Szacowania projektu zapewniają widok finansowy dla prac oszacowanych i zaplanowanych dla projektu.</span><span class="sxs-lookup"><span data-stu-id="c1518-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="c1518-105">Aby pracować z oszacowaniami projektu, należy załączyć projekt do projektu szacowanego.</span><span class="sxs-lookup"><span data-stu-id="c1518-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="c1518-106">Projekt szacowany jest zawsze oparty na projekcie istniejącym, ale wiele projektów może odwoływać się do jednego projektu szacowanego.</span><span class="sxs-lookup"><span data-stu-id="c1518-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="c1518-107">Do projektów szacowanych można dołączać tylko projekty o stałej cenie i projekty inwestycyjne, a te projekty muszą należeć do tej samej grupy projektów jak projekt szacowany.</span><span class="sxs-lookup"><span data-stu-id="c1518-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="c1518-108">W celu wyeliminowania projektu szacowanego należy go zakończyć.</span><span class="sxs-lookup"><span data-stu-id="c1518-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="c1518-109">Poniższe kroki opisują sposób eliminacji oszacowania.</span><span class="sxs-lookup"><span data-stu-id="c1518-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="c1518-110">Przejdź do **Zarządzanie projektami i księgowanie** > **Wszystkie projekty** i wybierz projekt.</span><span class="sxs-lookup"><span data-stu-id="c1518-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="c1518-111">Na karcie **Zarządzanie** wybierz pozycję **Oszacowania** i na stronie **Oszacowania** wybierz pozycję **Eliminuj**.</span><span class="sxs-lookup"><span data-stu-id="c1518-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="c1518-112">Na stronie **Eliminowanie oszacowania** na karcie **Ogólne** ustaw następujące opcje:</span><span class="sxs-lookup"><span data-stu-id="c1518-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="c1518-113">**Kod okresu** : należy wybrać kod okresu, aby wybrać odpowiednie szacowanie projektu.</span><span class="sxs-lookup"><span data-stu-id="c1518-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="c1518-114">**Data szacowania** : należy wybrać datę oszacowania dotyczącą eliminacji.</span><span class="sxs-lookup"><span data-stu-id="c1518-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="c1518-115">**Usuń z ostrzeżeniami PWT** : Włącz tę opcję, aby zapewnić powiadamianie w przypadku wyeliminowania oszacowania skojarzonego z pracą w toku (PWT).</span><span class="sxs-lookup"><span data-stu-id="c1518-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="c1518-116">Jeśli ta opcja nie jest włączona, eliminacja nie może być kontynuowana, jeśli istnieje nieoszacowana transakcja.</span><span class="sxs-lookup"><span data-stu-id="c1518-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="c1518-117">Ta opcja jest dostępna tylko wtedy, gdy do projektu szacowanego zastosowano eliminację.</span><span class="sxs-lookup"><span data-stu-id="c1518-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="c1518-118">Nie jest ona dostępna, jeśli używane jest księgowanie okresowe.</span><span class="sxs-lookup"><span data-stu-id="c1518-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="c1518-119">To ustawienie działa z ustawieniami na karcie **Szacowanie** na stronie **Parametry projektu** , w grupie pól **Zezwalaj na eliminację, kiedy istnieją nieoszacowane transakcje**.</span><span class="sxs-lookup"><span data-stu-id="c1518-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="c1518-120">**Ustaw etap jako gotowy** : włącz tę opcję, aby ustawić etap projektu szacowanego na **Zakończony** po przeprowadzeniu eliminacji.</span><span class="sxs-lookup"><span data-stu-id="c1518-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="c1518-121">**Drukuj listę oszacowań** : służy do wybierania informacji, które mają być uwzględnione podczas drukowania listy oszacowań.</span><span class="sxs-lookup"><span data-stu-id="c1518-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="c1518-122">**Pokaż dziennik informacyjny** : włącz tę opcję, aby wyświetlić dziennik informacyjny.</span><span class="sxs-lookup"><span data-stu-id="c1518-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="c1518-123">**Data księgowania** : należy wybrać datę księgowania w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="c1518-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="c1518-124">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1518-124">Select **OK**.</span></span>
5. <span data-ttu-id="c1518-125">Po zakończeniu procesu eliminacji dla wyeliminowanego projektu szacowanego jest wyświetlany element o ujemnych wartościach.</span><span class="sxs-lookup"><span data-stu-id="c1518-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="c1518-126">Jeśli nie zachodzi potrzeba wyeliminowania oszacowania, można wybrać wyeliminowaną wartość szacunkową i wybrać pozycję **Cofnij eliminację**.</span><span class="sxs-lookup"><span data-stu-id="c1518-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   