---
title: Synchronizowanie dyspozycyjności zasobów
description: W tym temacie zamieszczono informacje dotyczące sposobu synchronizowania wydajności zasobu w kalendarzach i projektach.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081990"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="e8187-103">Synchronizowanie dyspozycyjności zasobów</span><span class="sxs-lookup"><span data-stu-id="e8187-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8187-104">Procesy synchronizacji zasobów pomagają zagwarantować, że informacje z kalendarza i kalendarza podstawowego trafiają do planowania zasobów projektu.</span><span class="sxs-lookup"><span data-stu-id="e8187-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="e8187-105">Jeśli zostanie zmieniony kalendarz, procesy będą wymagały aktualizacji planowania zasobów projektów.</span><span class="sxs-lookup"><span data-stu-id="e8187-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="e8187-106">Procesy pomagają również zwiększyć wydajność, ponieważ informacje o zasobach kalendarza są z góry synchronizowane.</span><span class="sxs-lookup"><span data-stu-id="e8187-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="e8187-107">Z tego powodu aktualizacje informacji o harmonogramach zasobów są wykonywane szybciej.</span><span class="sxs-lookup"><span data-stu-id="e8187-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="e8187-108">Zaleca się, aby zamiast pojedynczych procesów zaplanować przetwarzanie w postaci partii.</span><span class="sxs-lookup"><span data-stu-id="e8187-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="e8187-109">W przeciwnym razie istnieje ryzyko, że użytkownik zapamiętał datę utworzenia ostatniej synchronizacji informacji.</span><span class="sxs-lookup"><span data-stu-id="e8187-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="e8187-110">Jeśli nie są używane daty łączne, podczas synchronizacji między datami mogą następować przerwy.</span><span class="sxs-lookup"><span data-stu-id="e8187-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synchronizacja kalendarza](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="e8187-112">Synchronizuj podsumowania pojemności zasobów</span><span class="sxs-lookup"><span data-stu-id="e8187-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="e8187-113">Proces synchronizacji ma na celu zsynchronizowanie wszystkich informacji kalendarza zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8187-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="e8187-114">Te informacje obejmują informacje kalendarza podstawowego o wszelkich zmianach w tabeli pojemności kalendarza zasobów projektu.</span><span class="sxs-lookup"><span data-stu-id="e8187-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="e8187-115">Jeśli w projekcie zostaną dodane nowe zasoby, synchronizacja pomaga zagwarantować, że dostępne są zaktualizowane informacje w kalendarzu.</span><span class="sxs-lookup"><span data-stu-id="e8187-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="e8187-116">Tę synchronizację można wykonać w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="e8187-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="e8187-117">Zalecamy użycie partii.</span><span class="sxs-lookup"><span data-stu-id="e8187-117">We recommend that you use a batch.</span></span> <span data-ttu-id="e8187-118">Te opcje są dostępne podczas synchronizowania rezerwacji wydajności.</span><span class="sxs-lookup"><span data-stu-id="e8187-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="e8187-119">Wybieranie **Zarządzanie projektami i księgowanie** &gt; **Okresowe** &gt; **Synchronizacja pojemności** &gt; **Synchronizuj podsumowania pojemności zasobów**.</span><span class="sxs-lookup"><span data-stu-id="e8187-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="e8187-120">Ustaw opcje w poniższej tabeli.</span><span class="sxs-lookup"><span data-stu-id="e8187-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="e8187-121">Opcja</span><span class="sxs-lookup"><span data-stu-id="e8187-121">Option</span></span>      | <span data-ttu-id="e8187-122">Opis</span><span class="sxs-lookup"><span data-stu-id="e8187-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="e8187-123">Kod okresu</span><span class="sxs-lookup"><span data-stu-id="e8187-123">Period code</span></span> | <span data-ttu-id="e8187-124">Opcjonalnie wybierz kod interwału dat księgi głównej, aby ustawić daty rozpoczęcia i zakończenia procesu synchronizacji dla zbiorczych pojemności zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8187-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="e8187-125">Data rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="e8187-125">Start date</span></span>  | <span data-ttu-id="e8187-126">Wprowadź datę rozpoczęcia procesu synchronizacji dotyczącego zestawienia wydajności zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8187-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="e8187-127">Data zakończenia</span><span class="sxs-lookup"><span data-stu-id="e8187-127">End date</span></span>    | <span data-ttu-id="e8187-128">Wprowadź datę zakończenia procesu synchronizacji dotyczącego zestawienia wydajności zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8187-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="e8187-129">[![Proces synchronizacji](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="e8187-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>