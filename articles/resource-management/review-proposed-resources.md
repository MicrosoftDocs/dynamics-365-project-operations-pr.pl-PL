---
title: Przeglądanie proponowanych zasobów
description: W tym temacie zamieszczono informacje dotyczące sposobu proponowania zasobów do projektu.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897374"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="43ad9-103">Przeglądanie proponowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="43ad9-103">Review proposed resources</span></span>

<span data-ttu-id="43ad9-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="43ad9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="43ad9-105">Menedżerowie zasobów mogą proponować zasób menedżerowi projektu za pomocą żądania zasobu.</span><span class="sxs-lookup"><span data-stu-id="43ad9-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="43ad9-106">W siatce żądań lub w oknie samego żądania wybierz pozycję **Znajdź zasoby**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="43ad9-107">Na stronie **Asystent planowania** wybierz zasób, a następnie w okienku **Utwórz rezerwację zasobu** w polu **Stan rezerwacji** wybierz opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="43ad9-108">Dojdzie do następujących aktualizacji stanu:</span><span class="sxs-lookup"><span data-stu-id="43ad9-108">The following status updates occur:</span></span>

- <span data-ttu-id="43ad9-109">Na stronie **Asystent planowania** wskaźniki stanu zostaną zaktualizowane i będą wskazywać, że rezerwacja została zaproponowana, a nie dokonana ostatecznie.</span><span class="sxs-lookup"><span data-stu-id="43ad9-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="43ad9-110">W oknie żądania zasobu stan zmieni się na **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="43ad9-111">W ustawieniach projektu na karcie **Zespół** wartość w polu **Stan żądania** dla ogólnego członka zespołu zmieni się na **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="43ad9-112">Menedżer projektu może zaakceptować lub odrzucić propozycję.</span><span class="sxs-lookup"><span data-stu-id="43ad9-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="43ad9-113">Gdy menedżerowie zasobów przetwarzają żądania zasobów, mogą używać następujących metod:</span><span class="sxs-lookup"><span data-stu-id="43ad9-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="43ad9-114">Zaproponowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób na wszystkie wymagane godziny.</span><span class="sxs-lookup"><span data-stu-id="43ad9-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="43ad9-115">Proponowane godziny są następnie dzielone między wszystkie zasoby mogące zaspokoić zapotrzebowanie na godziny.</span><span class="sxs-lookup"><span data-stu-id="43ad9-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="43ad9-116">W tym scenariuszu godziny nie mogą się pokrywać.</span><span class="sxs-lookup"><span data-stu-id="43ad9-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="43ad9-117">Zaproponowanie mniejszej ilości zasobów niż potrzeba.</span><span class="sxs-lookup"><span data-stu-id="43ad9-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="43ad9-118">W tym scenariuszu proponowana dyspozycyjność zasobów jest mniejsza niż wymagana liczba godzin określona przez wnioskodawcę.</span><span class="sxs-lookup"><span data-stu-id="43ad9-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="43ad9-119">W związku z tym kiedy wnioskodawca zaakceptuje zaproponowane zasoby, jest tworzone niezrealizowane wymaganie zasobu w celu odnotowania pozostałego zapotrzebowania.</span><span class="sxs-lookup"><span data-stu-id="43ad9-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="43ad9-120">Zarezerwowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób do wykonania całej pracy.</span><span class="sxs-lookup"><span data-stu-id="43ad9-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="43ad9-121">Zarezerwowanie mniejszej ilości zasobów niż potrzeba.</span><span class="sxs-lookup"><span data-stu-id="43ad9-121">Book fewer resources than are required.</span></span> <span data-ttu-id="43ad9-122">W tym scenariuszu zarezerwowana liczba godzin jest mniejsza niż wymagana liczba godzin.</span><span class="sxs-lookup"><span data-stu-id="43ad9-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="43ad9-123">System poprowadzi użytkownika do zaproponowania zasobów zamiast ich rezerwowania, dzięki czemu wnioskodawca może zweryfikować i śledzić pozostałe zapotrzebowania.</span><span class="sxs-lookup"><span data-stu-id="43ad9-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="43ad9-124">Wykorzystanie podlegające rozliczeniu</span><span class="sxs-lookup"><span data-stu-id="43ad9-124">Billable utilization</span></span>

<span data-ttu-id="43ad9-125">Zasoby mogą mieć docelowe wykorzystanie podlegające rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="43ad9-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="43ad9-126">To docelowe wykorzystanie jest zdefiniowane jako atrybut w domyślnej roli zasobu albo ustawione w rekordzie konkretnego zasobu możliwego do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="43ad9-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="43ad9-127">Obliczenia wykorzystania bazują na rzeczywistej liczbie godzin zaraportowanej przez zasoby przy użyciu zatwierdzonych wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="43ad9-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="43ad9-128">Poniższe wzory służą do obliczania wykorzystania:</span><span class="sxs-lookup"><span data-stu-id="43ad9-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="43ad9-129">Wykorzystanie podlegające rozliczeniu = odpłatne rzeczywiste godziny pracy ÷ dyspozycyjność zasobu</span><span class="sxs-lookup"><span data-stu-id="43ad9-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="43ad9-130">Wykorzystanie niepodlegające rozliczeniu = rzeczywisty czas o identyfikatorze typu rozliczania = nieodpłatne, uzupełniające lub niedostępne ÷ dyspozycyjność zasobu</span><span class="sxs-lookup"><span data-stu-id="43ad9-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="43ad9-131">Wewnętrzne = rzeczywisty czas bez kontraktu sprzedaży ÷ dyspozycyjności zasobu</span><span class="sxs-lookup"><span data-stu-id="43ad9-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="43ad9-132">Dyspozycyjności zasobu = godziny pracy zasobu – poza biurem — dni wolne od pracy</span><span class="sxs-lookup"><span data-stu-id="43ad9-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="43ad9-133">Widok **Wykorzystanie zasobów** jest dostępny z poziomu okienka **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="43ad9-134">Każda komórka w siatce reprezentuje procent wykorzystania zasobu podlegający rozliczeniu w okresie, takim jak dzień, tydzień lub miesiąc.</span><span class="sxs-lookup"><span data-stu-id="43ad9-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="43ad9-135">Poniższe wzory służą do kolorowania komórek:</span><span class="sxs-lookup"><span data-stu-id="43ad9-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="43ad9-136">**Zielony:** wykorzystanie podlegające rozliczeniu \>= docelowe wykorzystanie zasobu</span><span class="sxs-lookup"><span data-stu-id="43ad9-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="43ad9-137">**Żółty:** docelowe wykorzystanie – 20 \<= wykorzystanie podlegające rozliczeniu \< docelowe wykorzystanie</span><span class="sxs-lookup"><span data-stu-id="43ad9-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="43ad9-138">**Czerwony:** wykorzystanie podlegające rozliczeniu \< docelowe wykorzystanie – 20</span><span class="sxs-lookup"><span data-stu-id="43ad9-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="43ad9-139">Ponieważ widok **Wykorzystanie zasobów** jest oparty na tablicy harmonogramu, można używać funkcji filtrowania dostępnych w tablicy harmonogramu do filtrowania wyników.</span><span class="sxs-lookup"><span data-stu-id="43ad9-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="43ad9-140">Siatka wymaga skonfigurowania docelowego wykorzystania dla roli lub konkretnego zasobu.</span><span class="sxs-lookup"><span data-stu-id="43ad9-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="43ad9-141">Aby wykonać te czynności konfiguracyjne, wybierz kolejno opcje **Zasoby** \> **Role zasobu**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="43ad9-142">Ponadto każdemu zasobowi możliwemu do zarezerwowania musi być przypisana rola domyślna.</span><span class="sxs-lookup"><span data-stu-id="43ad9-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="43ad9-143">Wybierz kolejno opcje **Zasoby** \> **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="43ad9-144">Na karcie **Project Service** sprawdź, czy została zdefiniowana rola zasobu, a pole **Jest domyślna** ma ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="43ad9-145">Można dodać kolejne role, w których **Jest domyślna = Nie**.</span><span class="sxs-lookup"><span data-stu-id="43ad9-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="43ad9-146">Rola z atrybutem **Jest domyślna = Tak** jest używana do oceny wykorzystania zasobu w stosunku do wartości docelowej dla tej roli.</span><span class="sxs-lookup"><span data-stu-id="43ad9-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="43ad9-147">Na karcie **Project Service** można również skonfigurować konkretne docelowe wykorzystanie zasobu.</span><span class="sxs-lookup"><span data-stu-id="43ad9-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="43ad9-148">Następnie aparat obliczania wykorzystania na podstawie docelowego wykorzystania ocenia wartość docelową dla zasobu, a nie dla jego domyślnej roli.</span><span class="sxs-lookup"><span data-stu-id="43ad9-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="43ad9-149">Wykorzystanie jest pokazywane dla zasobu tylko w przypadku, gdy zasób ma zatwierdzony czas odpłatny w okresie wyświetlanym w siatce.</span><span class="sxs-lookup"><span data-stu-id="43ad9-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="43ad9-150">Dostępność zasobów</span><span class="sxs-lookup"><span data-stu-id="43ad9-150">Resource availability</span></span>

<span data-ttu-id="43ad9-151">Bardzo ważne jest, aby menedżerowie zasobów mogli przeglądać dostępne zasoby i aktualizować rezerwacje.</span><span class="sxs-lookup"><span data-stu-id="43ad9-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="43ad9-152">Czasami nie ma formalnego wymogu (żądania zasobu), ale menedżer zasobów musi reagować na nieplanowane zapotrzebowanie pochodzące z kanału takiego jak poczta e-mail, rozmowa telefoniczna lub wiadomość błyskawiczna.</span><span class="sxs-lookup"><span data-stu-id="43ad9-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="43ad9-153">Menedżerowie zasobów używają tablicy harmonogramu do aktualizowania zasobów i rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="43ad9-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="43ad9-154">Godziny pracy zasobu są używane jako podstawa do obliczenia dostępności zasobu.</span><span class="sxs-lookup"><span data-stu-id="43ad9-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="43ad9-155">Rezerwacje zasobów powodują zużywanie dyspozycyjności zasobów.</span><span class="sxs-lookup"><span data-stu-id="43ad9-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="43ad9-156">Tablica harmonogramu korzysta z kolorów i cieniowania w celu pokazania rezerwacji, dostępności i nakładania się rezerwacji, a także stanu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="43ad9-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="43ad9-157">Opcja w ustawieniach tablicy harmonogramu umożliwia wyświetlenie legendy.</span><span class="sxs-lookup"><span data-stu-id="43ad9-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="43ad9-158">Jeśli w tablicy harmonogramu obok konkretnego zasobu możliwego do zarezerwowania widać znak strzałki w prawo, można rozwinąć zasób, aby wyświetlić szczegółowe informacje o pracy, dla której zasób został zarezerwowany.</span><span class="sxs-lookup"><span data-stu-id="43ad9-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="43ad9-159">Program Dynamics 365 Project Operations korzysta z aparatu Universal Resource Scheduling, dlatego jeśli zainstalowano również aplikację Dynamics 365 Field Service, można wyświetlić szczegółowe informacje o rezerwacjach zasobów dla projektów, zleceń pracy i innych encji, na które rozszerzono planowanie.</span><span class="sxs-lookup"><span data-stu-id="43ad9-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="43ad9-160">Aby wyświetlić więcej informacji na temat konkretnego zasobu, kliknij go prawym przyciskiem myszy, a zostanie otwarta karta zasobu.</span><span class="sxs-lookup"><span data-stu-id="43ad9-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

