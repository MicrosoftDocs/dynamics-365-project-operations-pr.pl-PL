---
title: Wydajność planowania zasobów projektu
description: W tym temacie zamieszczono informacje dotyczące zwiększania wydajności planowania zasobów na dużą liczbę projektów.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289022"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="02662-103">Wydajność planowania zasobów projektu</span><span class="sxs-lookup"><span data-stu-id="02662-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="02662-104">Problemy dotyczące wydajności związanej z planowaniem zasobów mogą mieć znaczenie, gdy liczba jest bardzo duża.</span><span class="sxs-lookup"><span data-stu-id="02662-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="02662-105">Aby poprawić wydajność planowania zasobów, można uzyskać dostęp do funkcji, która pozwoli użytkownikom skrócić czas potrzebny na uruchomienie formularza dostępności zasobów.</span><span class="sxs-lookup"><span data-stu-id="02662-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="02662-106">W szczególności powoduje to usunięcie procesu synchronizacji zestawienia dyspozycyjności zasobów i użycie tabeli **ResProjectResource** w celu przyspieszenia wyszukiwania zasobów.</span><span class="sxs-lookup"><span data-stu-id="02662-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="02662-107">Zauważ, że tabela **ResRollup** nie będzie już używana.</span><span class="sxs-lookup"><span data-stu-id="02662-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02662-108">Jeśli istnieje zależność między procesem synchronizacji zestawienia wydajności zasobów lub tabelą **ResProjectResource**, nie należy korzystać z tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="02662-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="02662-109">Włączanie zwiększania wydajności planowania zasobów</span><span class="sxs-lookup"><span data-stu-id="02662-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="02662-110">Aby włączyć podniesienie wydajności planowania zasobów, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="02662-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="02662-111">Wybierz kolejno opcje **Zarządzanie funkcjami** > **Wszystkie** i na liście funkcji znajdź pozycję **Włącz funkcję zwiększania wydajności planowania zasobów projektu**.</span><span class="sxs-lookup"><span data-stu-id="02662-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="02662-112">Wybierz opcję **Włącz teraz**.</span><span class="sxs-lookup"><span data-stu-id="02662-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="02662-113">Jeśli nie można znaleźć tej funkcji na liście, wybierz pozycję **Sprawdź, czy są aktualizacje** w celu odświeżenia listy.</span><span class="sxs-lookup"><span data-stu-id="02662-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="02662-114">Odśwież przeglądarkę, a następnie przejdź do obszaru **Zarządzanie projektami i księgowanie** > **Okresowe** > **Zasoby projektu** > **Synchronizacja kalendarzy zasobów projektu we wszystkich firmach**.</span><span class="sxs-lookup"><span data-stu-id="02662-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="02662-115">Aby usunąć poprzednie dane, należy ustawić opcję **Usuń istniejące rekordy wydajności** na wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="02662-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="02662-116">Jeśli chcesz wygenerować przyrostowe dane, ustaw wartość na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="02662-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="02662-117">W polu **Kod okresu** wybierz okres, w którym mają zostać wygenerowane dane.</span><span class="sxs-lookup"><span data-stu-id="02662-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="02662-118">W przypadku wybrania kodu okresu nie jest konieczne zdefiniowanie daty rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="02662-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="02662-119">Jeśli pole **Kod okresu** pozostanie puste, wybierz określone daty rozpoczęcia i zakończenia, aby utworzyć dane.</span><span class="sxs-lookup"><span data-stu-id="02662-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="02662-120">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="02662-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="02662-121">Spowoduje to dystrybuowanie danych ogólnych do tabeli **ResCalendarCapacity** we wszystkich firmach w środowisku, więc zadanie wsadowe musi zostać uruchomione tylko w jednej firmie.</span><span class="sxs-lookup"><span data-stu-id="02662-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="02662-122">Dane w tym zadaniu wsadowym są potrzebne do obliczenia wydajności zasobów za pośrednictwem skojarzonego kalendarza.</span><span class="sxs-lookup"><span data-stu-id="02662-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="02662-123">Przejdź do obszaru **Zarządzanie projektami i księgowanie** > **Okresowe** > **Zasoby projektu** > **Wypełnij zasoby projektu we wszystkich firmach**, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="02662-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="02662-124">Jest to skrypt uaktualniania danych dla ogólnych danych w tabelach **ResProjectResource**, **ResCalendarDateTimeRange** oraz **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="02662-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="02662-125">Wartości pola **PSAPRojSchedRole.RootObject** są również aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="02662-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="02662-126">Jeśli nie zostanie uruchomione, zostanie wyświetlone ostrzeżenie podczas próby wykonania operacji planowania zasobów.</span><span class="sxs-lookup"><span data-stu-id="02662-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="02662-127">Wyłączanie zwiększania wydajności planowania zasobów</span><span class="sxs-lookup"><span data-stu-id="02662-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="02662-128">Wybierz kolejno opcje **Zarządzanie funkcjami** > **Wszystkie** i wyszukaj opcji **Włącz funkcję zwiększania wydajności planowania zasobów projektu**.</span><span class="sxs-lookup"><span data-stu-id="02662-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="02662-129">Zaznacz funkcję, a następnie wybierz przycisk **Wyłącz**.</span><span class="sxs-lookup"><span data-stu-id="02662-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="02662-130">Odśwież przeglądarkę.</span><span class="sxs-lookup"><span data-stu-id="02662-130">Refresh your browser.</span></span>
4. <span data-ttu-id="02662-131">Przejdź do **Zarządzanie projektami i księgowanie** > **Okresowe** > **Synchronizacja pojemności** > **Synchronizuj podsumowania pojemności zasobów**.</span><span class="sxs-lookup"><span data-stu-id="02662-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="02662-132">Na stronie **Synchronizacja pojemności** wybierz wartość **Tak** w polu **Usuń istniejące rekordy pojemności**.</span><span class="sxs-lookup"><span data-stu-id="02662-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="02662-133">Jeśli chcesz wygenerować przyrostowe dane, ustaw wartość na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="02662-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="02662-134">W polu **Kod okresu** wybierz okres, w którym mają zostać wygenerowane dane.</span><span class="sxs-lookup"><span data-stu-id="02662-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="02662-135">W przypadku wybrania kodu okresu nie jest konieczne zdefiniowanie daty rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="02662-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="02662-136">Jeśli pole **Kod okresu** pozostanie puste, wybierz określone daty rozpoczęcia i zakończenia, aby utworzyć dane.</span><span class="sxs-lookup"><span data-stu-id="02662-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="02662-137">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="02662-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="02662-138">Spowoduje to dystrybuowanie danych ogólnych do tabeli **ResRollup** we wszystkich firmach w środowisku, więc zadanie wsadowe musi zostać uruchomione tylko w jednej firmie.</span><span class="sxs-lookup"><span data-stu-id="02662-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="02662-139">To zadanie wsadowe jest wymagane we wszystkich widokach **Dostępności zasobów**.</span><span class="sxs-lookup"><span data-stu-id="02662-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="02662-140">Jeśli to zadanie wsadowe nie zostanie uruchomione, dane **ResRollup** będą generowane na żywo, co może zajmować czas.</span><span class="sxs-lookup"><span data-stu-id="02662-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]