---
title: Synchronizowanie dyspozycyjności zasobów
description: W tym temacie zamieszczono informacje dotyczące sposobu synchronizowania wydajności zasobu w kalendarzach i projektach.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997524"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="4da86-103">Synchronizowanie dyspozycyjności zasobów</span><span class="sxs-lookup"><span data-stu-id="4da86-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4da86-104">Procesy synchronizacji zasobów pomagają zagwarantować, że informacje z kalendarza i kalendarza podstawowego trafiają do planowania zasobów projektu.</span><span class="sxs-lookup"><span data-stu-id="4da86-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="4da86-105">Jeśli zostanie zmieniony kalendarz, procesy będą wymagały aktualizacji planowania zasobów projektów.</span><span class="sxs-lookup"><span data-stu-id="4da86-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="4da86-106">Procesy pomagają również zwiększyć wydajność, ponieważ informacje o zasobach kalendarza są z góry synchronizowane.</span><span class="sxs-lookup"><span data-stu-id="4da86-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="4da86-107">Z tego powodu aktualizacje informacji o harmonogramach zasobów są wykonywane szybciej.</span><span class="sxs-lookup"><span data-stu-id="4da86-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="4da86-108">Zaleca się, aby zamiast pojedynczych procesów zaplanować przetwarzanie w postaci partii.</span><span class="sxs-lookup"><span data-stu-id="4da86-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="4da86-109">W przeciwnym razie istnieje ryzyko, że użytkownik zapamiętał datę utworzenia ostatniej synchronizacji informacji.</span><span class="sxs-lookup"><span data-stu-id="4da86-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="4da86-110">Jeśli nie są używane daty łączne, podczas synchronizacji między datami mogą następować przerwy.</span><span class="sxs-lookup"><span data-stu-id="4da86-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synchronizacja kalendarza](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="4da86-112">Synchronizuj podsumowania pojemności zasobów</span><span class="sxs-lookup"><span data-stu-id="4da86-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="4da86-113">Proces synchronizacji ma na celu zsynchronizowanie wszystkich informacji kalendarza zasobów.</span><span class="sxs-lookup"><span data-stu-id="4da86-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="4da86-114">Te informacje obejmują informacje kalendarza podstawowego o wszelkich zmianach w tabeli pojemności kalendarza zasobów projektu.</span><span class="sxs-lookup"><span data-stu-id="4da86-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="4da86-115">Jeśli w projekcie zostaną dodane nowe zasoby, synchronizacja pomaga zagwarantować, że dostępne są zaktualizowane informacje w kalendarzu.</span><span class="sxs-lookup"><span data-stu-id="4da86-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="4da86-116">Tę synchronizację można wykonać w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="4da86-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="4da86-117">Zalecamy użycie partii.</span><span class="sxs-lookup"><span data-stu-id="4da86-117">We recommend that you use a batch.</span></span> <span data-ttu-id="4da86-118">Te opcje są dostępne podczas synchronizowania rezerwacji wydajności.</span><span class="sxs-lookup"><span data-stu-id="4da86-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="4da86-119">Wybieranie **Zarządzanie projektami i księgowanie** &gt; **Okresowe** &gt; **Synchronizacja pojemności** &gt; **Synchronizuj podsumowania pojemności zasobów**.</span><span class="sxs-lookup"><span data-stu-id="4da86-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="4da86-120">Ustaw opcje w poniższej tabeli.</span><span class="sxs-lookup"><span data-stu-id="4da86-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="4da86-121">Opcja</span><span class="sxs-lookup"><span data-stu-id="4da86-121">Option</span></span>      | <span data-ttu-id="4da86-122">Opis</span><span class="sxs-lookup"><span data-stu-id="4da86-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="4da86-123">Kod okresu</span><span class="sxs-lookup"><span data-stu-id="4da86-123">Period code</span></span> | <span data-ttu-id="4da86-124">Opcjonalnie wybierz kod interwału dat księgi głównej, aby ustawić daty rozpoczęcia i zakończenia procesu synchronizacji dla zbiorczych pojemności zasobów.</span><span class="sxs-lookup"><span data-stu-id="4da86-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4da86-125">Data rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="4da86-125">Start date</span></span>  | <span data-ttu-id="4da86-126">Wprowadź datę rozpoczęcia procesu synchronizacji dotyczącego zestawienia wydajności zasobów.</span><span class="sxs-lookup"><span data-stu-id="4da86-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4da86-127">Data zakończenia</span><span class="sxs-lookup"><span data-stu-id="4da86-127">End date</span></span>    | <span data-ttu-id="4da86-128">Wprowadź datę zakończenia procesu synchronizacji dotyczącego zestawienia wydajności zasobów.</span><span class="sxs-lookup"><span data-stu-id="4da86-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="4da86-129">[![Proces synchronizacji](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="4da86-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]