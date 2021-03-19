---
title: Przeglądanie proponowanych zasobów
description: W tym temacie zamieszczono informacje dotyczące sposobu proponowania zasobów do projektu.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279286"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="bdcab-103">Przeglądanie proponowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="bdcab-103">Review proposed resources</span></span>

<span data-ttu-id="bdcab-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="bdcab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bdcab-105">Menedżerowie zasobów mogą proponować zasób menedżerowi projektu za pomocą żądania zasobu.</span><span class="sxs-lookup"><span data-stu-id="bdcab-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="bdcab-106">W siatce żądań lub w oknie samego żądania wybierz pozycję **Znajdź zasoby**.</span><span class="sxs-lookup"><span data-stu-id="bdcab-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="bdcab-107">Na stronie **Asystent planowania** wybierz zasób, a następnie w okienku **Utwórz rezerwację zasobu** w polu **Stan rezerwacji** wybierz opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="bdcab-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="bdcab-108">Dojdzie do następujących aktualizacji stanu:</span><span class="sxs-lookup"><span data-stu-id="bdcab-108">The following status updates occur:</span></span>

- <span data-ttu-id="bdcab-109">Na stronie **Asystent planowania** wskaźniki stanu zostaną zaktualizowane i będą wskazywać, że rezerwacja została zaproponowana, a nie dokonana ostatecznie.</span><span class="sxs-lookup"><span data-stu-id="bdcab-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="bdcab-110">W oknie żądania zasobu stan zmieni się na **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="bdcab-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="bdcab-111">W ustawieniach projektu na karcie **Zespół** wartość w polu **Stan żądania** dla ogólnego członka zespołu zmieni się na **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="bdcab-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="bdcab-112">Menedżer projektu może zaakceptować lub odrzucić propozycję.</span><span class="sxs-lookup"><span data-stu-id="bdcab-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="bdcab-113">Gdy menedżerowie zasobów przetwarzają żądania zasobów, mogą używać następujących metod:</span><span class="sxs-lookup"><span data-stu-id="bdcab-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="bdcab-114">Zaproponowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób na wszystkie wymagane godziny.</span><span class="sxs-lookup"><span data-stu-id="bdcab-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="bdcab-115">Proponowane godziny są następnie dzielone między wszystkie zasoby mogące zaspokoić zapotrzebowanie na godziny.</span><span class="sxs-lookup"><span data-stu-id="bdcab-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="bdcab-116">W tym scenariuszu godziny nie mogą się pokrywać.</span><span class="sxs-lookup"><span data-stu-id="bdcab-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="bdcab-117">Zaproponowanie mniejszej ilości zasobów niż potrzeba.</span><span class="sxs-lookup"><span data-stu-id="bdcab-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="bdcab-118">W tym scenariuszu proponowana dyspozycyjność zasobów jest mniejsza niż wymagana liczba godzin określona przez wnioskodawcę.</span><span class="sxs-lookup"><span data-stu-id="bdcab-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="bdcab-119">W związku z tym kiedy wnioskodawca zaakceptuje zaproponowane zasoby, jest tworzone niezrealizowane wymaganie zasobu w celu odnotowania pozostałego zapotrzebowania.</span><span class="sxs-lookup"><span data-stu-id="bdcab-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="bdcab-120">Zarezerwowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób do wykonania całej pracy.</span><span class="sxs-lookup"><span data-stu-id="bdcab-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="bdcab-121">Zarezerwowanie mniejszej ilości zasobów niż potrzeba.</span><span class="sxs-lookup"><span data-stu-id="bdcab-121">Book fewer resources than are required.</span></span> <span data-ttu-id="bdcab-122">W tym scenariuszu zarezerwowana liczba godzin jest mniejsza niż wymagana liczba godzin.</span><span class="sxs-lookup"><span data-stu-id="bdcab-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="bdcab-123">System poprowadzi użytkownika do zaproponowania zasobów zamiast ich rezerwowania, dzięki czemu wnioskodawca może zweryfikować i śledzić pozostałe zapotrzebowania.</span><span class="sxs-lookup"><span data-stu-id="bdcab-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="bdcab-124">Dostępność zasobów</span><span class="sxs-lookup"><span data-stu-id="bdcab-124">Resource availability</span></span>

<span data-ttu-id="bdcab-125">Bardzo ważne jest, aby menedżerowie zasobów mogli przeglądać dostępne zasoby i aktualizować rezerwacje.</span><span class="sxs-lookup"><span data-stu-id="bdcab-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="bdcab-126">Czasami nie ma formalnego wymogu (żądania zasobu), ale menedżer zasobów musi reagować na nieplanowane zapotrzebowanie pochodzące z kanału takiego jak poczta e-mail, rozmowa telefoniczna lub wiadomość błyskawiczna.</span><span class="sxs-lookup"><span data-stu-id="bdcab-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="bdcab-127">Menedżerowie zasobów używają tablicy harmonogramu do aktualizowania zasobów i rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="bdcab-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="bdcab-128">Godziny pracy zasobu są używane jako podstawa do obliczenia dostępności zasobu.</span><span class="sxs-lookup"><span data-stu-id="bdcab-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="bdcab-129">Rezerwacje zasobów powodują zużywanie dyspozycyjności zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdcab-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="bdcab-130">Tablica harmonogramu korzysta z kolorów i cieniowania w celu pokazania rezerwacji, dostępności i nakładania się rezerwacji, a także stanu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="bdcab-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="bdcab-131">Opcja w ustawieniach tablicy harmonogramu umożliwia wyświetlenie legendy.</span><span class="sxs-lookup"><span data-stu-id="bdcab-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="bdcab-132">Jeśli w tablicy harmonogramu obok konkretnego zasobu możliwego do zarezerwowania widać znak strzałki w prawo, można rozwinąć zasób, aby wyświetlić szczegółowe informacje o pracy, dla której zasób został zarezerwowany.</span><span class="sxs-lookup"><span data-stu-id="bdcab-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="bdcab-133">Program Dynamics 365 Project Operations korzysta z aparatu Universal Resource Scheduling, dlatego jeśli zainstalowano również aplikację Dynamics 365 Field Service, można wyświetlić szczegółowe informacje o rezerwacjach zasobów dla projektów, zleceń pracy i innych encji, na które rozszerzono planowanie.</span><span class="sxs-lookup"><span data-stu-id="bdcab-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="bdcab-134">Aby wyświetlić więcej informacji na temat konkretnego zasobu, kliknij go prawym przyciskiem myszy, a zostanie otwarta karta zasobu.</span><span class="sxs-lookup"><span data-stu-id="bdcab-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]