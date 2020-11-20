---
title: Metody alokacji zarezerwowania w Project Service Automation
description: Ten temat zawiera informacje na temat różnych sposobów rezerwowania alokacji.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 295da428ce15e7775450dfa94e96047f200bdede
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082006"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a><span data-ttu-id="abd87-103">Metody alokacji zarezerwowania w Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="abd87-103">Booking allocation methods in Project Service Automation</span></span>

<span data-ttu-id="abd87-104">Niezależnie, czy dodajesz członka zespołu bezpośrednio do projektu na karcie **Zespół** , czy rezerwujesz zasób dla projektu lub wymaganie z tablicy harmonogramu, istnieje kilka metod rezerwacji przydziału, które mogą zostać użyte.</span><span class="sxs-lookup"><span data-stu-id="abd87-104">Whether you add a team member directly to a project on the **Team** tab, or book a resource to a project or requirement from the Schedule board, there are a few different booking allocation methods you can use.</span></span> <span data-ttu-id="abd87-105">W tym temacie wyjaśniono, jak działa każda z tych metod, i które z tych metod mogą spowodować nałożenie się rezerwacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="abd87-105">This topic explains how each method works, and which methods could lead to overbooking resources.</span></span>

## <a name="full-capacity"></a><span data-ttu-id="abd87-106">Pełna dyspozycyjność</span><span class="sxs-lookup"><span data-stu-id="abd87-106">Full Capacity</span></span> 
<span data-ttu-id="abd87-107">Metoda Pełna dyspozycyjność rezerwuje pełną dyspozycyjność zasobu dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="abd87-107">The Full Capacity method books the resource’s full capacity for the specified from and to dates.</span></span> <span data-ttu-id="abd87-108">Na przykład jeśli zasób ma kalendarz skonfigurowany dla pracy osiem godzin dziennie, pięć dni w tygodniu, ustawienie dat rozpoczęcia i zakończenia, które obejmują pięć dni roboczych, zarezerwuje zasób na 40 godzin.</span><span class="sxs-lookup"><span data-stu-id="abd87-108">For example, if a resource has a calendar set to work eight hours per day, five days a week, setting a start and end date that covers five working days will book the resource for 40 hours.</span></span> <span data-ttu-id="abd87-109">Rezerwacja odbywa się bez wzięcia pod uwagę pozostałej dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="abd87-109">The booking is done without regard to the resource's remaining capacity.</span></span> <span data-ttu-id="abd87-110">Jeśli zasób jest już zarezerwowany w tym samym okresie dla innych projektów, 40 godzin zostanie zarezerwowane jako dodatkowe godziny, potencjalnie prowadząc do nakładania się rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="abd87-110">If a resource is already booked on other projects during that period, the 40 hours is booked as additional hours, which potentially leads to overbookings.</span></span>

## <a name="remaining-capacity"></a><span data-ttu-id="abd87-111">Pozostała dyspozycyjność</span><span class="sxs-lookup"><span data-stu-id="abd87-111">Remaining Capacity</span></span>
<span data-ttu-id="abd87-112">Metoda Pozostała dyspozycyjność jest dostępna tylko w przypadku, gdy przeprowadzasz rezerwację bezpośrednio dla projektu przy użyciu tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="abd87-112">The Remaining Capacity method is only available when you book directly to a project using the Schedule board.</span></span> <span data-ttu-id="abd87-113">Ta metoda rezerwuje dostępną dyspozycyjności zasobu w określonym zakresie dat.</span><span class="sxs-lookup"><span data-stu-id="abd87-113">This method books the resource’s available capacity within the specified date range.</span></span> <span data-ttu-id="abd87-114">Na przykład jeśli zasób ma dyspozycyjność równą 40 godzin w tygodniu i został już zarezerwowany na 10 godzin, rezerwacja na ten sam tydzień spowoduje rezerwację na pozostałe 30 godzin dyspozycyjności w tygodniu.</span><span class="sxs-lookup"><span data-stu-id="abd87-114">For example, if a resource has a capacity of 40 hours per week and has already been booked 10 hours, booking for the same week results in booking the remaining 30 hours of capacity for that week.</span></span>

## <a name="percentage-capacity"></a><span data-ttu-id="abd87-115">Dyspozycyjność procentowa</span><span class="sxs-lookup"><span data-stu-id="abd87-115">Percentage Capacity</span></span>
<span data-ttu-id="abd87-116">Metoda Dyspozycyjność procentowa rezerwuje procent dyspozycyjności zasobu dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="abd87-116">The Percentage Capacity method books the resource for a percentage of capacity for the specified from and to dates.</span></span> <span data-ttu-id="abd87-117">Na przykład jeśli zasób ma kalendarz skonfigurowany dla pracy osiem godzin dziennie, pięć dni w tygodniu, ustawienie dat rozpoczęcia i zakończenia, które obejmują pięć dni roboczych z 50-procentową dyspozycyjnością, zarezerwuje zasób na 20 godzin.</span><span class="sxs-lookup"><span data-stu-id="abd87-117">For example, if a resource's calendar is set to work eight hours per day, five days a week, setting a start and end date that covers five working days at 50% capacity would book the resource for 20 hours.</span></span> <span data-ttu-id="abd87-118">Poszczególne rezerwacje na dzień są rozkładane po równo na cały ten okres, w tym przykładzie na cztery godziny w ciągu dnia.</span><span class="sxs-lookup"><span data-stu-id="abd87-118">The individual bookings per day are spread equally across the period, four hours per day in this example.</span></span> <span data-ttu-id="abd87-119">Rezerwacja odbywa się bez wzięcia pod uwagę pozostałej dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="abd87-119">The booking is done without regard to the resource’s remaining capacity.</span></span> <span data-ttu-id="abd87-120">Jeśli zasób jest już zarezerwowany w tym samym okresie dla innych projektów, 20 godzin zostanie zarezerwowane jako dodatkowe godziny, potencjalnie prowadząc do nakładania się rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="abd87-120">If the resource is already booked during that period on other projects, the 20 hours is booked as additional hours, which potentially leads to overbookings.</span></span>

## <a name="evenly-distribute-hours"></a><span data-ttu-id="abd87-121">Godziny — rozłóż równomiernie</span><span class="sxs-lookup"><span data-stu-id="abd87-121">Evenly Distribute Hours</span></span>
<span data-ttu-id="abd87-122">Metoda Godziny — rozłóż równomiernie rezerwuje zasób na określoną liczbą godzin, rozkładając czas równomiernie w ciągu dnia dla określonych dat Od i Do.</span><span class="sxs-lookup"><span data-stu-id="abd87-122">The Evenly Distribute Hours method books the resource for a specified number of hours, distributing the time evenly per day over the specified from and to dates.</span></span> <span data-ttu-id="abd87-123">Na przykład jeśli rezerwujesz zasób na 20 godzin przez okres pięciu dni, ta metoda rozkłada 20 godzin równomiernie na cztery godziny w ciągu dnia.</span><span class="sxs-lookup"><span data-stu-id="abd87-123">For example, if you book a resource for 20 hours over a five day period, this method distributes the 20 hours evenly at four hours per day.</span></span> <span data-ttu-id="abd87-124">Rezerwacja odbywa się bez wzięcia pod uwagę pozostałej dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="abd87-124">The booking is done without regard to the resource's remaining capacity.</span></span> <span data-ttu-id="abd87-125">Jeśli zasób jest już zarezerwowany w tym samym okresie dla innych projektów, 20 godzin zostanie zarezerwowane jako dodatkowe godziny, potencjalnie prowadząc do nakładania się rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="abd87-125">If the resource is already booked during that period on other projects, the 20 hours is booked as additional hours, which potentially leads to overbookings.</span></span>

## <a name="front-load-hours"></a><span data-ttu-id="abd87-126">Godziny — najwięcej na początku</span><span class="sxs-lookup"><span data-stu-id="abd87-126">Front Load Hours</span></span>
<span data-ttu-id="abd87-127">Metoda Godziny — najwięcej na początku rezerwuje zasób na określoną liczbą godzin, kładąc nacisk na godziny początkowe w ciągu dnia dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="abd87-127">The Front Load Hours method books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span> <span data-ttu-id="abd87-128">Położenie nacisku na godziny początkowe zużywa dostępną dyspozycyjność zasobu w kolejności "pierwszy wchodzi - pierwszy schodzi".</span><span class="sxs-lookup"><span data-stu-id="abd87-128">Front-loading consumes the resource's available capacity in a “first-in-first-consumed” order.</span></span> <span data-ttu-id="abd87-129">Na przykład jeśli harmonogram pracy zasobu obejmuje osiem godzin na dobę przez pięć dni w tygodniu, i nie ma żadnych bieżących rezerwacji, zarezerwowanie zasobu na 20 godzin w okresie pięciu dni roboczych daje następujący wzorzec dzienny rezerwacji:</span><span class="sxs-lookup"><span data-stu-id="abd87-129">For example, if a resource’s work schedule is eight hours per day, five days per week, and they have no current bookings, booking the resource for 20 hours over a five working day period results in the following daily booking pattern:</span></span> 

|         <span data-ttu-id="abd87-130">Rezerwacje</span><span class="sxs-lookup"><span data-stu-id="abd87-130">Bookings</span></span>          |    <span data-ttu-id="abd87-131">Dzień 1</span><span class="sxs-lookup"><span data-stu-id="abd87-131">Day 1</span></span>    |    <span data-ttu-id="abd87-132">Dzień 2</span><span class="sxs-lookup"><span data-stu-id="abd87-132">Day 2</span></span>    |    <span data-ttu-id="abd87-133">Dzień 3</span><span class="sxs-lookup"><span data-stu-id="abd87-133">Day 3</span></span>    |    <span data-ttu-id="abd87-134">Dzień 4</span><span class="sxs-lookup"><span data-stu-id="abd87-134">Day 4</span></span>    |    <span data-ttu-id="abd87-135">Dzień 5</span><span class="sxs-lookup"><span data-stu-id="abd87-135">Day 5</span></span>    |    <span data-ttu-id="abd87-136">Łączna liczba</span><span class="sxs-lookup"><span data-stu-id="abd87-136">Total</span></span>    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    <span data-ttu-id="abd87-137">Istniejące rezerwacje</span><span class="sxs-lookup"><span data-stu-id="abd87-137">Existing   bookings</span></span>    |    <span data-ttu-id="abd87-138">0</span><span class="sxs-lookup"><span data-stu-id="abd87-138">0</span></span>        |    <span data-ttu-id="abd87-139">0</span><span class="sxs-lookup"><span data-stu-id="abd87-139">0</span></span>        |    <span data-ttu-id="abd87-140">0</span><span class="sxs-lookup"><span data-stu-id="abd87-140">0</span></span>        |    <span data-ttu-id="abd87-141">0</span><span class="sxs-lookup"><span data-stu-id="abd87-141">0</span></span>        |    <span data-ttu-id="abd87-142">0</span><span class="sxs-lookup"><span data-stu-id="abd87-142">0</span></span>        |    <span data-ttu-id="abd87-143">0</span><span class="sxs-lookup"><span data-stu-id="abd87-143">0</span></span>        |
|    <span data-ttu-id="abd87-144">Nowa rezerwacja</span><span class="sxs-lookup"><span data-stu-id="abd87-144">New   booking</span></span>          |    <span data-ttu-id="abd87-145">8</span><span class="sxs-lookup"><span data-stu-id="abd87-145">8</span></span>        |    <span data-ttu-id="abd87-146">8</span><span class="sxs-lookup"><span data-stu-id="abd87-146">8</span></span>        |    <span data-ttu-id="abd87-147">4</span><span class="sxs-lookup"><span data-stu-id="abd87-147">4</span></span>        |    <span data-ttu-id="abd87-148">0</span><span class="sxs-lookup"><span data-stu-id="abd87-148">0</span></span>        |    <span data-ttu-id="abd87-149">0</span><span class="sxs-lookup"><span data-stu-id="abd87-149">0</span></span>        |    <span data-ttu-id="abd87-150">20</span><span class="sxs-lookup"><span data-stu-id="abd87-150">20</span></span>       |

<span data-ttu-id="abd87-151">Metoda Najwięcej na początku bierze pod uwagę istniejące rezerwacje i dostępną dyspozycyjność.</span><span class="sxs-lookup"><span data-stu-id="abd87-151">The front load method takes into consideration existing bookings and available capacity.</span></span> <span data-ttu-id="abd87-152">Na przykład jeśli ten sam zasób ma już 20 godzin rezerwacji na dany tydzień roboczy, nowe rezerwacje zużywają pozostałą dyspozycyjność w poniższy sposób:</span><span class="sxs-lookup"><span data-stu-id="abd87-152">For example, if the same resource already has 20 hours of bookings in the work week, the new bookings consume the remaining capacity as follows:</span></span>

|   <span data-ttu-id="abd87-153">Rezerwacje</span><span class="sxs-lookup"><span data-stu-id="abd87-153">Bookings</span></span>          | <span data-ttu-id="abd87-154">Dzień 1</span><span class="sxs-lookup"><span data-stu-id="abd87-154">Day 1</span></span> | <span data-ttu-id="abd87-155">Dzień 2</span><span class="sxs-lookup"><span data-stu-id="abd87-155">Day 2</span></span> | <span data-ttu-id="abd87-156">Dzień 3</span><span class="sxs-lookup"><span data-stu-id="abd87-156">Day 3</span></span> | <span data-ttu-id="abd87-157">Dzień 4</span><span class="sxs-lookup"><span data-stu-id="abd87-157">Day 4</span></span> | <span data-ttu-id="abd87-158">Dzień 5</span><span class="sxs-lookup"><span data-stu-id="abd87-158">Day 5</span></span> | <span data-ttu-id="abd87-159">Łączna liczba</span><span class="sxs-lookup"><span data-stu-id="abd87-159">Total</span></span> |
|---------------------|-------|-------|-------|-------|-------|-------|
| <span data-ttu-id="abd87-160">Istniejące rezerwacje</span><span class="sxs-lookup"><span data-stu-id="abd87-160">Existing   bookings</span></span> | <span data-ttu-id="abd87-161">8</span><span class="sxs-lookup"><span data-stu-id="abd87-161">8</span></span>     | <span data-ttu-id="abd87-162">8</span><span class="sxs-lookup"><span data-stu-id="abd87-162">8</span></span>     | <span data-ttu-id="abd87-163">100</span><span class="sxs-lookup"><span data-stu-id="abd87-163">4</span></span>     | <span data-ttu-id="abd87-164">0</span><span class="sxs-lookup"><span data-stu-id="abd87-164">0</span></span>     | <span data-ttu-id="abd87-165">0</span><span class="sxs-lookup"><span data-stu-id="abd87-165">0</span></span>     | <span data-ttu-id="abd87-166">20</span><span class="sxs-lookup"><span data-stu-id="abd87-166">20</span></span>    |
| <span data-ttu-id="abd87-167">Nowa rezerwacja</span><span class="sxs-lookup"><span data-stu-id="abd87-167">New   booking</span></span>       | <span data-ttu-id="abd87-168">0</span><span class="sxs-lookup"><span data-stu-id="abd87-168">0</span></span>     | <span data-ttu-id="abd87-169">0</span><span class="sxs-lookup"><span data-stu-id="abd87-169">0</span></span>     | <span data-ttu-id="abd87-170">4</span><span class="sxs-lookup"><span data-stu-id="abd87-170">4</span></span>     | <span data-ttu-id="abd87-171">8</span><span class="sxs-lookup"><span data-stu-id="abd87-171">8</span></span>     | <span data-ttu-id="abd87-172">8</span><span class="sxs-lookup"><span data-stu-id="abd87-172">8</span></span>     | <span data-ttu-id="abd87-173">20</span><span class="sxs-lookup"><span data-stu-id="abd87-173">20</span></span>    |

<span data-ttu-id="abd87-174">Ponieważ dostępna dyspozycyjność jest brana pod uwagę, możesz otrzymać komunikat o błędzie, jeśli zasób nie ma już dyspozycyjności, która może zostać pobrana przez rezerwację.</span><span class="sxs-lookup"><span data-stu-id="abd87-174">Because available capacity is considered, you may get an error message if the resource has no remaining capacity that can be absorbed by the booking.</span></span> <span data-ttu-id="abd87-175">W przypadku tej metody nie można doprowadzić do nakładania się rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="abd87-175">With this method, you can’t overbook.</span></span>

## <a name="none"></a><span data-ttu-id="abd87-176">Brak</span><span class="sxs-lookup"><span data-stu-id="abd87-176">None</span></span>
<span data-ttu-id="abd87-177">Metoda Brak jest dostępna tylko w przypadku, gdy rezerwację przeprowadzasz z karty **Zespół** w ramach projektu.</span><span class="sxs-lookup"><span data-stu-id="abd87-177">The None method is only available when you book from the **Team** tab within a project.</span></span> <span data-ttu-id="abd87-178">Ta metoda dodaje zasób jako członka zespołu projektu, ale nie tworzy żadnych rezerwacji, które absorbują dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="abd87-178">This method adds the resource as a team member on the project, but doesn’t create any bookings that absorb the resource's capacity.</span></span> <span data-ttu-id="abd87-179">Ta metoda jest używana gdy domyślny członek zespołu Menedżer projektu jest dodawany podczas tworzenia projektu.</span><span class="sxs-lookup"><span data-stu-id="abd87-179">This method is used when the default project manager team member is added when a project is created.</span></span> <span data-ttu-id="abd87-180">Użytkownik Menedżer projektu, który utworzył projekt jest domyślnie dodawany do projektu, tak aby rekordu encji projektu miał właściciela i istnieje jedna osoba zatwierdzająca projekt.</span><span class="sxs-lookup"><span data-stu-id="abd87-180">The project manager user who created the project is added by default to the project, so that the project entity record has an owner and there is one approver on the project.</span></span> <span data-ttu-id="abd87-181">Ponieważ ten użytkownik nie ma żadnych rezerwacji, jeśli chcesz zarezerwować zasób, możesz albo usunąć i ponownie je dodać przy użyciu innej metody alokacji, albo dodać zasób do zadań, a następnie użyć **Rozszerz rezerwacje** na karcie **Uzgadnianie** , aby utworzyć rezerwacje dla przypisań.</span><span class="sxs-lookup"><span data-stu-id="abd87-181">Because this user doesn't have any bookings, if you do want to book the resource, you can either delete and then re-add them using a different allocation method, or add the resource to tasks and then use **Extend Bookings** on the **Reconciliation** tab to create bookings for the assignments.</span></span>

## <a name="allocation-methods-that-lead-to-overbooking"></a><span data-ttu-id="abd87-182">Metody alokacji prowadzące do nakładania się rezerwacji</span><span class="sxs-lookup"><span data-stu-id="abd87-182">Allocation methods that lead to overbooking</span></span>
<span data-ttu-id="abd87-183">Podsumowując, poniższe metody alokacji prowadzą do nakładania się rezerwacji, jeśli zasób zajmuje się już innymi projektami (lub innymi zleceniami pracy lub encjami, które można objąć harmonogramem):</span><span class="sxs-lookup"><span data-stu-id="abd87-183">To summarize, the following allocation methods lead to overbooking if the resource is already committed in other projects (or for other work orders or schedulable entities):</span></span>

- <span data-ttu-id="abd87-184">Pełna dyspozycyjność</span><span class="sxs-lookup"><span data-stu-id="abd87-184">Full Capacity</span></span>
- <span data-ttu-id="abd87-185">Dyspozycyjność procentowa</span><span class="sxs-lookup"><span data-stu-id="abd87-185">Percentage Capacity</span></span>
- <span data-ttu-id="abd87-186">Godziny — rozłóż równomiernie</span><span class="sxs-lookup"><span data-stu-id="abd87-186">Evenly Distribute Hours</span></span>

<span data-ttu-id="abd87-187">Korzystając z jednej z tych trzech metod alokacji nie zostaniesz powiadomiony, że zasób został nadmiarowo zarezerwowany.</span><span class="sxs-lookup"><span data-stu-id="abd87-187">When using one of these three allocation methods, you won’t be notified that the resource is overbooked.</span></span> <span data-ttu-id="abd87-188">Aby rozwiązać problem nakładania się rezerwacji, należy użyć tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="abd87-188">To correct the overbooking, you’ll need to use the Schedule board.</span></span>