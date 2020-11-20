---
title: Proponowanie zasobów projektu
description: W tym temacie zamieszczono informacje dotyczące proponowania zasobów do projektu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120196"
---
# <a name="propose-project-resources"></a><span data-ttu-id="009f1-103">Proponowanie zasobów projektu</span><span class="sxs-lookup"><span data-stu-id="009f1-103">Propose project resources</span></span>

<span data-ttu-id="009f1-104">Menedżerowie zasobów mogą proponować zasób menedżerowi projektu za pomocą żądania zasobu.</span><span class="sxs-lookup"><span data-stu-id="009f1-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="009f1-105">W siatce żądań lub w oknie samego żądania wybierz pozycję **Znajdź zasoby**.</span><span class="sxs-lookup"><span data-stu-id="009f1-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="009f1-106">Na stronie **Asystent planowania** wybierz zasób, a następnie w okienku **Utwórz rezerwację zasobu** w polu **Stan rezerwacji** wybierz opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="009f1-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Proponowany zasób wybrany](media/Resource-Management-image62.png)

<span data-ttu-id="009f1-108">Dojdzie do następujących aktualizacji stanu:</span><span class="sxs-lookup"><span data-stu-id="009f1-108">The following status updates occur:</span></span>

- <span data-ttu-id="009f1-109">Na stronie **Asystent planowania** wskaźniki stanu zostaną zaktualizowane i będą wskazywać, że rezerwacja została zaproponowana, a nie dokonana ostatecznie.</span><span class="sxs-lookup"><span data-stu-id="009f1-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Wskaźniki stanu proponowanej rezerwacje na stronie Asystent planowania](media/Resource-Management-image63.png)

- <span data-ttu-id="009f1-111">W oknie żądania zasobu stan zmieni się na **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="009f1-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Stan żądania zasobu zmieniony na Wymaga weryfikacji](media/Resource-Management-image64.png)

- <span data-ttu-id="009f1-113">W ustawieniach projektu na karcie **Zespół** wartość w polu **Stan żądania** dla ogólnego członka zespołu zmieni się na **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="009f1-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Stan żądania na karcie Zespół dla ogólnego członka zespołu zmieniony na Wymaga weryfikacji](media/Resource-Management-image48.png)

<span data-ttu-id="009f1-115">Menedżer projektu może zaakceptować lub odrzucić propozycję.</span><span class="sxs-lookup"><span data-stu-id="009f1-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="009f1-116">Gdy menedżerowie zasobów przetwarzają żądania zasobów, mogą używać następujących metod:</span><span class="sxs-lookup"><span data-stu-id="009f1-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="009f1-117">Zaproponowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób na wszystkie wymagane godziny.</span><span class="sxs-lookup"><span data-stu-id="009f1-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="009f1-118">Proponowane godziny są następnie dzielone między wszystkie zasoby mogące zaspokoić zapotrzebowanie na godziny.</span><span class="sxs-lookup"><span data-stu-id="009f1-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="009f1-119">W tym scenariuszu godziny nie mogą się pokrywać.</span><span class="sxs-lookup"><span data-stu-id="009f1-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="009f1-120">Zaproponowanie mniejszej ilości zasobów niż potrzeba.</span><span class="sxs-lookup"><span data-stu-id="009f1-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="009f1-121">W tym scenariuszu proponowana dyspozycyjność zasobów jest mniejsza niż wymagana liczba godzin określona przez wnioskodawcę.</span><span class="sxs-lookup"><span data-stu-id="009f1-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="009f1-122">W związku z tym kiedy wnioskodawca zaakceptuje zaproponowane zasoby, jest tworzone niezrealizowane wymaganie zasobu w celu odnotowania pozostałego zapotrzebowania.</span><span class="sxs-lookup"><span data-stu-id="009f1-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="009f1-123">Zarezerwowanie wielu zasobów, aby zaspokoić zapotrzebowanie, jeśli nie jest dostępny żaden pojedynczy zasób do wykonania całej pracy.</span><span class="sxs-lookup"><span data-stu-id="009f1-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="009f1-124">Zarezerwowanie mniejszej ilości zasobów niż potrzeba.</span><span class="sxs-lookup"><span data-stu-id="009f1-124">Book fewer resources than are required.</span></span> <span data-ttu-id="009f1-125">W tym scenariuszu zarezerwowana liczba godzin jest mniejsza niż wymagana liczba godzin.</span><span class="sxs-lookup"><span data-stu-id="009f1-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="009f1-126">System poprowadzi użytkownika do zaproponowania zasobów zamiast ich rezerwowania, dzięki czemu wnioskodawca może zweryfikować i śledzić pozostałe zapotrzebowania.</span><span class="sxs-lookup"><span data-stu-id="009f1-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="009f1-127">Wykorzystanie podlegające rozliczeniu</span><span class="sxs-lookup"><span data-stu-id="009f1-127">Billable utilization</span></span>

<span data-ttu-id="009f1-128">Zasoby mogą mieć docelowe wykorzystanie podlegające rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="009f1-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="009f1-129">To docelowe wykorzystanie jest zdefiniowane jako atrybut w domyślnej roli zasobu albo ustawione w rekordzie konkretnego zasobu możliwego do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="009f1-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="009f1-130">Obliczenia wykorzystania bazują na rzeczywistej liczbie godzin zaraportowanej przez zasoby przy użyciu zatwierdzonych wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="009f1-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="009f1-131">Poniższe wzory służą do obliczania wykorzystania:</span><span class="sxs-lookup"><span data-stu-id="009f1-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="009f1-132">Wykorzystanie podlegające rozliczeniu = odpłatne rzeczywiste godziny pracy ÷ dyspozycyjność zasobu</span><span class="sxs-lookup"><span data-stu-id="009f1-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="009f1-133">Wykorzystanie niepodlegające rozliczeniu = rzeczywisty czas o identyfikatorze typu rozliczania = nieodpłatne, uzupełniające lub niedostępne ÷ dyspozycyjność zasobu</span><span class="sxs-lookup"><span data-stu-id="009f1-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="009f1-134">Wewnętrzne = rzeczywisty czas bez kontraktu sprzedaży ÷ dyspozycyjności zasobu</span><span class="sxs-lookup"><span data-stu-id="009f1-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="009f1-135">Dyspozycyjności zasobu = godziny pracy zasobu – poza biurem — dni wolne od pracy</span><span class="sxs-lookup"><span data-stu-id="009f1-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="009f1-136">Widok **Wykorzystanie zasobów** jest dostępny z poziomu okienka **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="009f1-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Widok Wykorzystanie zasobów](media/Resource-Management-image65.png)

<span data-ttu-id="009f1-138">Każda komórka w siatce reprezentuje procent wykorzystania zasobu podlegający rozliczeniu w okresie, takim jak dzień, tydzień lub miesiąc.</span><span class="sxs-lookup"><span data-stu-id="009f1-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="009f1-139">Poniższe wzory służą do kolorowania komórek:</span><span class="sxs-lookup"><span data-stu-id="009f1-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="009f1-140">**Zielony:** wykorzystanie podlegające rozliczeniu \>= docelowe wykorzystanie zasobu</span><span class="sxs-lookup"><span data-stu-id="009f1-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="009f1-141">**Żółty:** docelowe wykorzystanie – 20 \<= wykorzystanie podlegające rozliczeniu \< docelowe wykorzystanie</span><span class="sxs-lookup"><span data-stu-id="009f1-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="009f1-142">**Czerwony:** wykorzystanie podlegające rozliczeniu \< docelowe wykorzystanie – 20</span><span class="sxs-lookup"><span data-stu-id="009f1-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="009f1-143">Ponieważ widok **Wykorzystanie zasobów** jest oparty na tablicy harmonogramu, można używać funkcji filtrowania dostępnych w tablicy harmonogramu do filtrowania wyników.</span><span class="sxs-lookup"><span data-stu-id="009f1-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="009f1-144">Siatka wymaga skonfigurowania docelowego wykorzystania dla roli lub konkretnego zasobu.</span><span class="sxs-lookup"><span data-stu-id="009f1-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="009f1-145">Aby wykonać te czynności konfiguracyjne, wybierz kolejno opcje **Zasoby** \> **Role zasobu**.</span><span class="sxs-lookup"><span data-stu-id="009f1-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="009f1-146">Ponadto każdemu zasobowi możliwemu do zarezerwowania musi być przypisana rola domyślna.</span><span class="sxs-lookup"><span data-stu-id="009f1-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="009f1-147">Wybierz kolejno opcje **Zasoby** \> **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="009f1-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="009f1-148">Na karcie **Project Service** sprawdź, czy została zdefiniowana rola zasobu, a pole **Jest domyślna** ma ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="009f1-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="009f1-149">Można dodać kolejne role, w których **Jest domyślna = Nie**.</span><span class="sxs-lookup"><span data-stu-id="009f1-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="009f1-150">Rola z atrybutem **Jest domyślna = Tak** jest używana do oceny wykorzystania zasobu w stosunku do wartości docelowej dla tej roli.</span><span class="sxs-lookup"><span data-stu-id="009f1-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Domyślny zestaw ról](media/Resource-Management-image67.png)

<span data-ttu-id="009f1-152">Na karcie **Project Service** można również skonfigurować konkretne docelowe wykorzystanie zasobu.</span><span class="sxs-lookup"><span data-stu-id="009f1-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="009f1-153">Następnie aparat obliczania wykorzystania na podstawie docelowego wykorzystania ocenia wartość docelową dla zasobu, a nie dla jego domyślnej roli.</span><span class="sxs-lookup"><span data-stu-id="009f1-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="009f1-154">Wykorzystanie jest pokazywane dla zasobu tylko w przypadku, gdy zasób ma zatwierdzony czas odpłatny w okresie wyświetlanym w siatce.</span><span class="sxs-lookup"><span data-stu-id="009f1-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="009f1-155">Dostępność zasobów</span><span class="sxs-lookup"><span data-stu-id="009f1-155">Resource availability</span></span>

<span data-ttu-id="009f1-156">Bardzo ważne jest, aby menedżerowie zasobów mogli przeglądać dostępne zasoby i aktualizować rezerwacje.</span><span class="sxs-lookup"><span data-stu-id="009f1-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="009f1-157">Czasami nie ma formalnego wymogu (żądania zasobu), ale menedżer zasobów musi reagować na nieplanowane zapotrzebowanie pochodzące z kanału takiego jak poczta e-mail, rozmowa telefoniczna lub wiadomość błyskawiczna.</span><span class="sxs-lookup"><span data-stu-id="009f1-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="009f1-158">Menedżerowie zasobów używają tablicy harmonogramu do aktualizowania zasobów i rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="009f1-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="009f1-159">Godziny pracy zasobu są używane jako podstawa do obliczenia dostępności zasobu.</span><span class="sxs-lookup"><span data-stu-id="009f1-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="009f1-160">Rezerwacje zasobów powodują zużywanie dyspozycyjności zasobów.</span><span class="sxs-lookup"><span data-stu-id="009f1-160">Resource bookings consume the capacity of the resources.</span></span>

![Tablica harmonogramu](media/Resource-Management-image68.png)

<span data-ttu-id="009f1-162">Tablica harmonogramu korzysta z kolorów i cieniowania w celu pokazania rezerwacji, dostępności i nakładania się rezerwacji, a także stanu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="009f1-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="009f1-163">Opcja w ustawieniach tablicy harmonogramu umożliwia wyświetlenie legendy.</span><span class="sxs-lookup"><span data-stu-id="009f1-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="009f1-164">Jeśli w tablicy harmonogramu obok konkretnego zasobu możliwego do zarezerwowania widać znak strzałki w prawo, można rozwinąć zasób, aby wyświetlić szczegółowe informacje o pracy, dla której zasób został zarezerwowany.</span><span class="sxs-lookup"><span data-stu-id="009f1-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Zasoby możliwe do zarezerwowania rozwinięte w tablicy harmonogramu](media/Resource-Management-image69.png)

<span data-ttu-id="009f1-166">Program Dynamics 365 Project Service Automation korzysta z aparatu Universal Resource Scheduling, dlatego jeśli zainstalowano również aplikację Dynamics 365 Field Service, można wyświetlić szczegółowe informacje o rezerwacjach zasobów dla projektów, zleceń pracy i innych encji, na które rozszerzono planowanie.</span><span class="sxs-lookup"><span data-stu-id="009f1-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Szczegółowe informacje o rezerwacjach zasobów do projektów i zleceń pracy](media/Resource-Management-image70.png)

<span data-ttu-id="009f1-168">Aby wyświetlić więcej informacji na temat konkretnego zasobu, kliknij go prawym przyciskiem myszy, a zostanie otwarta karta zasobu.</span><span class="sxs-lookup"><span data-stu-id="009f1-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Karta zasobu](media/Resource-Management-image71.png)
