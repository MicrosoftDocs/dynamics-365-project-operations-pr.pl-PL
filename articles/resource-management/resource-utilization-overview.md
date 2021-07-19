---
title: Omówienie wykorzystania zasobów
description: W tym temacie zamieszczono informacje dotyczące widoku wykorzystania zasobów w Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367949"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="4b9c1-103">Omówienie wykorzystania zasobów</span><span class="sxs-lookup"><span data-stu-id="4b9c1-103">Resource utilization overview</span></span>

<span data-ttu-id="4b9c1-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="4b9c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b9c1-105">Zasoby mogą mieć docelowe wykorzystanie podlegające rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="4b9c1-106">To docelowe wykorzystanie jest zdefiniowane jako atrybut w domyślnej roli zasobu albo ustawione w rekordzie konkretnego zasobu możliwego do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="4b9c1-107">Obliczenia wykorzystania bazują na rzeczywistej liczbie godzin zaraportowanej przez zasoby przy użyciu zatwierdzonych wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="4b9c1-108">Poniższe wzory służą do obliczania wykorzystania:</span><span class="sxs-lookup"><span data-stu-id="4b9c1-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="4b9c1-109">Wykorzystanie podlegające rozliczeniu = odpłatne rzeczywiste godziny pracy ÷ dyspozycyjność zasobu</span><span class="sxs-lookup"><span data-stu-id="4b9c1-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="4b9c1-110">Wykorzystanie niepodlegające rozliczeniu = rzeczywisty czas o identyfikatorze typu rozliczania = nieodpłatne, uzupełniające lub niedostępne ÷ dyspozycyjność zasobu</span><span class="sxs-lookup"><span data-stu-id="4b9c1-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="4b9c1-111">Wewnętrzne = rzeczywisty czas bez kontraktu sprzedaży ÷ dyspozycyjności zasobu</span><span class="sxs-lookup"><span data-stu-id="4b9c1-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="4b9c1-112">Dyspozycyjności zasobu = godziny pracy zasobu – poza biurem — dni wolne od pracy</span><span class="sxs-lookup"><span data-stu-id="4b9c1-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="4b9c1-113">Widok **Wykorzystanie zasobów** jest dostępny z poziomu okienka **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="4b9c1-114">Każda komórka w siatce reprezentuje procent wykorzystania zasobu podlegający rozliczeniu w okresie, takim jak dzień, tydzień lub miesiąc.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="4b9c1-115">Poniższe wzory służą do kolorowania komórek:</span><span class="sxs-lookup"><span data-stu-id="4b9c1-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="4b9c1-116">**Zielony**: Wykorzystanie do rozliczenia >= docelowe wykorzystanie zasobów</span><span class="sxs-lookup"><span data-stu-id="4b9c1-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="4b9c1-117">**Żółty**: Docelowe wykorzystanie - 20 <= Wykorzystanie do rozliczenia < Docelowe wykorzystanie</span><span class="sxs-lookup"><span data-stu-id="4b9c1-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="4b9c1-118">**Czerwony**: Wykorzystanie do rozliczenia < Docelowe wykorzystanie - 20</span><span class="sxs-lookup"><span data-stu-id="4b9c1-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="4b9c1-119">Ponieważ widok **Wykorzystanie zasobów** jest oparty na tablicy harmonogramu, można używać funkcji filtrowania dostępnych w tablicy harmonogramu do filtrowania wyników.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="4b9c1-120">Siatka wymaga skonfigurowania docelowego wykorzystania dla roli lub konkretnego zasobu.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="4b9c1-121">Aby wykonać te czynności konfiguracyjne, wybierz kolejno opcje **Zasoby** > **Role zasobu**.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="4b9c1-122">Ponadto każdemu zasobowi możliwemu do zarezerwowania musi być przypisana rola domyślna.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="4b9c1-123">Wybierz kolejno opcje **Zasoby** > **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="4b9c1-124">Na karcie **Project Service** sprawdź, czy została zdefiniowana rola zasobu, a pole **Jest domyślna** ma ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="4b9c1-125">Można dodać kolejne role, w których **Jest domyślna** = **Nie**.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="4b9c1-126">Rola z atrybutem **Jest domyślna** = **Tak** jest używana do oceny wykorzystania zasobu w stosunku do wartości docelowej dla tej roli.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="4b9c1-127">Na karcie **Project Service** można również skonfigurować konkretne docelowe wykorzystanie zasobu.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="4b9c1-128">Następnie aparat obliczania wykorzystania na podstawie docelowego wykorzystania ocenia wartość docelową dla zasobu, a nie dla jego domyślnej roli.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="4b9c1-129">Wykorzystanie jest pokazywane dla zasobu tylko w przypadku, gdy zasób ma zatwierdzony czas odpłatny w okresie wyświetlanym w siatce.</span><span class="sxs-lookup"><span data-stu-id="4b9c1-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]