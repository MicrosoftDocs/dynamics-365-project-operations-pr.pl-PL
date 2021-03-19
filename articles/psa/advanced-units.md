---
title: Grupy jednostek i jednostki
description: Ten temat zawiera informacje o grupach jednostek i jednostkach.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291632"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="9a6a1-103">Grupy jednostek i jednostki</span><span class="sxs-lookup"><span data-stu-id="9a6a1-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9a6a1-104">Grupy jednostek i jednostki są encjami podstawowymi w systemie Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="9a6a1-105">Jednostka jest pojedynczą jednostką miary, a wiele jednostek można połączyć w grupy jednostek.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="9a6a1-106">W interfejsie użytkownika (UI) programu Dynamics 365 grupa jednostek jest czasem określana mianem wykazu (harmonogramu) jednostek.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="9a6a1-107">Oto kilka przykładów jednostek i grup jednostek:</span><span class="sxs-lookup"><span data-stu-id="9a6a1-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="9a6a1-108">**Grupa jednostek**: Odległość</span><span class="sxs-lookup"><span data-stu-id="9a6a1-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="9a6a1-109">**Jednostki**: Mila, Kilometr itd.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="9a6a1-110">**Grupa jednostek**: Czas</span><span class="sxs-lookup"><span data-stu-id="9a6a1-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="9a6a1-111">**Jednostki**: Godzina, Dzień, Tydzień itd.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="9a6a1-112">Podczas konfigurowania wielu jednostek w grupie jednostek należy też zdefiniować współczynnik konwersji między nimi, wyznaczając pierwszą konfigurowaną jednostkę jako domyślną lub podstawową w grupie jednostek.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="9a6a1-113">Jeśli na przykład w grupie jednostek **Czas** jednostka **Godzina** zostanie ustawiona jako pierwsza, system wyznacza jednostkę **Godzina** jako domyślną.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="9a6a1-114">Jeśli następną konfigurowaną jednostką jest **Dzień**, należy skonfigurować współczynnik konwersji z **Dzień** na **Godzina**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="9a6a1-115">Jeśli następnie dodasz **Tydzień** jako trzecią jednostkę, należy skonfigurować współczynnik konwersji jednostki **Tydzień** na jednostkę **Dzień** lub **Godzina**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="9a6a1-116">Na poniższej ilustracji przedstawiono przykładową konfigurację jednostki **Dzień**, gdzie w polu **Ilość** jest wyświetlana liczba dni istniejących w dniu, oraz jednostki **Tydzień**, gdzie pole **Ilość** zawiera liczbę dni w tygodniu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Grupa jednostek: strona Informacje](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="9a6a1-118">Używanie jednostek i grup jednostek</span><span class="sxs-lookup"><span data-stu-id="9a6a1-118">Using units and unit groups</span></span>

<span data-ttu-id="9a6a1-119">Program Dynamics 365 Project Service Automation używa jednostek i grup jednostek do przetwarzania oszacowań i wpisów dla kosztów i czasu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="9a6a1-120">W przypadku kosztów każda kategoria wydatku ma domyślną grupę jednostek i jednostkę.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="9a6a1-121">Te wartości są wprowadzane jako wartości domyślne w pozycjach cennika dla kategorii wydatków.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="9a6a1-122">Na przykład masz kategorię wydatków o nazwie **Przebieg**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="9a6a1-123">Ma ona grupę jednostek o nazwie **Odległość** oraz jednostkę domyślną o nazwie **Mila**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="9a6a1-124">Jeśli skonfigurujesz grupę jednostek **Odległość** tak, aby zawierała dwie jednostki (**Mila** i **Kilometr**), można w jednym cenniku ustawić dwie ceny dla kategorii **Przebieg**: cenę za milę i cenę za kilometr.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="9a6a1-125">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="9a6a1-125">Expense category</span></span>  | <span data-ttu-id="9a6a1-126">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="9a6a1-126">Unit group</span></span>  | <span data-ttu-id="9a6a1-127">Jednostka</span><span class="sxs-lookup"><span data-stu-id="9a6a1-127">Unit</span></span>      | <span data-ttu-id="9a6a1-128">Metoda kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="9a6a1-128">Pricing method</span></span>  | <span data-ttu-id="9a6a1-129">Cena jednostkowa</span><span class="sxs-lookup"><span data-stu-id="9a6a1-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="9a6a1-130">Przebieg</span><span class="sxs-lookup"><span data-stu-id="9a6a1-130">Mileage</span></span>           | <span data-ttu-id="9a6a1-131">Odległość</span><span class="sxs-lookup"><span data-stu-id="9a6a1-131">Distance</span></span>      | <span data-ttu-id="9a6a1-132">Mila</span><span class="sxs-lookup"><span data-stu-id="9a6a1-132">Mile</span></span>      | <span data-ttu-id="9a6a1-133">Cena jednostkowa</span><span class="sxs-lookup"><span data-stu-id="9a6a1-133">Price per unit</span></span>    | <span data-ttu-id="9a6a1-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="9a6a1-134">10 USD</span></span>            |
| <span data-ttu-id="9a6a1-135">Przebieg</span><span class="sxs-lookup"><span data-stu-id="9a6a1-135">Mileage</span></span>           | <span data-ttu-id="9a6a1-136">Odległość</span><span class="sxs-lookup"><span data-stu-id="9a6a1-136">Distance</span></span>      | <span data-ttu-id="9a6a1-137">Kilometr</span><span class="sxs-lookup"><span data-stu-id="9a6a1-137">Kilometer</span></span> | <span data-ttu-id="9a6a1-138">Cena jednostkowa</span><span class="sxs-lookup"><span data-stu-id="9a6a1-138">Price per unit</span></span>    |  <span data-ttu-id="9a6a1-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="9a6a1-139">6 USD</span></span>            |

<span data-ttu-id="9a6a1-140">Po wprowadzeniu wydatku w projekcie system oblicza mu cenę na podstawie kombinacji kategorii i jednostki.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="9a6a1-141">Opis wydatku</span><span class="sxs-lookup"><span data-stu-id="9a6a1-141">Expense description</span></span>        | <span data-ttu-id="9a6a1-142">Kategoria wydatków</span><span class="sxs-lookup"><span data-stu-id="9a6a1-142">Expense category</span></span>  | <span data-ttu-id="9a6a1-143">Jednostka</span><span class="sxs-lookup"><span data-stu-id="9a6a1-143">Unit</span></span>  | <span data-ttu-id="9a6a1-144">Ilość</span><span class="sxs-lookup"><span data-stu-id="9a6a1-144">Quantity</span></span>  | <span data-ttu-id="9a6a1-145">Cena jednostkowa</span><span class="sxs-lookup"><span data-stu-id="9a6a1-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="9a6a1-146">Przejazd do lokalizacji klienta</span><span class="sxs-lookup"><span data-stu-id="9a6a1-146">Drive to client location</span></span> | <span data-ttu-id="9a6a1-147">Przebieg</span><span class="sxs-lookup"><span data-stu-id="9a6a1-147">Mileage</span></span>             | <span data-ttu-id="9a6a1-148">Mila</span><span class="sxs-lookup"><span data-stu-id="9a6a1-148">Mile</span></span>  | <span data-ttu-id="9a6a1-149">10</span><span class="sxs-lookup"><span data-stu-id="9a6a1-149">10</span></span>        | <span data-ttu-id="9a6a1-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="9a6a1-150">10 USD</span></span>         |

<span data-ttu-id="9a6a1-151">Dla czasu każdy nagłówek cennika ma pole **Domyślna jednostka czasu**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="9a6a1-152">Wartość jest ustawiana podczas tworzenia nagłówka cennika.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="9a6a1-153">Ta jednostka jest następnie używana do ustawiania wszystkich cen opartych na rolach w cenniku.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="9a6a1-154">Wiersze szacowania dla pola **Czas w ofercie** mogą być wyrażone w dowolnej jednostce czasu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="9a6a1-155">Natomiast wiersze szacowane w projektach oraz wpisy czasu dla projektów mogą używać tylko jednostki czasu **Godzina**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="9a6a1-156">Jeśli jednostka we wpisie czasu lub wierszu szacowania nie pasuje do jednostki w wierszu cennika dla danej roli, system przelicza cenę na jednostki zdefiniowane w oszacowaniu projektu lub w transakcji z wartościami rzeczywistymi projektu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="9a6a1-157">W poniższym przykładzie pokazano, jak system PSA używa grupy jednostek, jednostek i współczynników konwersji.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="9a6a1-158">Units</span><span class="sxs-lookup"><span data-stu-id="9a6a1-158">Units</span></span>

   - <span data-ttu-id="9a6a1-159">**Grupa jednostek**: Czas</span><span class="sxs-lookup"><span data-stu-id="9a6a1-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="9a6a1-160">**Jednostki**: Godzina</span><span class="sxs-lookup"><span data-stu-id="9a6a1-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="9a6a1-161">**Dzień** — Współczynnik konwersji: 8 godzin</span><span class="sxs-lookup"><span data-stu-id="9a6a1-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="9a6a1-162">**Tydzień** — Współczynnik konwersji: 40 godzin</span><span class="sxs-lookup"><span data-stu-id="9a6a1-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="9a6a1-163">Konfiguracja cennika w projekcie A:</span><span class="sxs-lookup"><span data-stu-id="9a6a1-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="9a6a1-164">**Nazwa**: Ceny sprzedaży na rynek brytyjski 2016</span><span class="sxs-lookup"><span data-stu-id="9a6a1-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="9a6a1-165">**Domyślna jednostka czasu**: Dzień</span><span class="sxs-lookup"><span data-stu-id="9a6a1-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="9a6a1-166">**Waluta**: GBP</span><span class="sxs-lookup"><span data-stu-id="9a6a1-166">**Currency**: GBP</span></span>

| <span data-ttu-id="9a6a1-167">Rola</span><span class="sxs-lookup"><span data-stu-id="9a6a1-167">Role</span></span>      | <span data-ttu-id="9a6a1-168">Grupa jednostek</span><span class="sxs-lookup"><span data-stu-id="9a6a1-168">Unit group</span></span> | <span data-ttu-id="9a6a1-169">Jednostka</span><span class="sxs-lookup"><span data-stu-id="9a6a1-169">Unit</span></span> | <span data-ttu-id="9a6a1-170">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="9a6a1-170">Organizational unit</span></span> | <span data-ttu-id="9a6a1-171">Cena</span><span class="sxs-lookup"><span data-stu-id="9a6a1-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="9a6a1-172">Dla deweloperów</span><span class="sxs-lookup"><span data-stu-id="9a6a1-172">Developer</span></span> | <span data-ttu-id="9a6a1-173">Time</span><span class="sxs-lookup"><span data-stu-id="9a6a1-173">Time</span></span>       | <span data-ttu-id="9a6a1-174">Day</span><span class="sxs-lookup"><span data-stu-id="9a6a1-174">Day</span></span>  | <span data-ttu-id="9a6a1-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="9a6a1-175">Contoso UK</span></span>          | <span data-ttu-id="9a6a1-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="9a6a1-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="9a6a1-177">Wpis czasu</span><span class="sxs-lookup"><span data-stu-id="9a6a1-177">Time entry</span></span>

<span data-ttu-id="9a6a1-178">W poniższej tabeli przedstawiono wynikowe transakcje po stronie sprzedaży utworzone przez rozwiązanie PSA dla 3-godzinnego projektu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="9a6a1-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="9a6a1-179">Project</span></span>   | <span data-ttu-id="9a6a1-180">Zadanie</span><span class="sxs-lookup"><span data-stu-id="9a6a1-180">Task</span></span>    | <span data-ttu-id="9a6a1-181">Rola</span><span class="sxs-lookup"><span data-stu-id="9a6a1-181">Role</span></span>      | <span data-ttu-id="9a6a1-182">Ilość</span><span class="sxs-lookup"><span data-stu-id="9a6a1-182">Quantity</span></span> | <span data-ttu-id="9a6a1-183">Jednostka</span><span class="sxs-lookup"><span data-stu-id="9a6a1-183">Unit</span></span>  | <span data-ttu-id="9a6a1-184">Cena jednostkowa</span><span class="sxs-lookup"><span data-stu-id="9a6a1-184">Unit price</span></span> | <span data-ttu-id="9a6a1-185">Kwota nierozliczonej sprzedaży</span><span class="sxs-lookup"><span data-stu-id="9a6a1-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="9a6a1-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="9a6a1-186">Project A</span></span> | <span data-ttu-id="9a6a1-187">Projekt</span><span class="sxs-lookup"><span data-stu-id="9a6a1-187">Design</span></span>  | <span data-ttu-id="9a6a1-188">Dla deweloperów</span><span class="sxs-lookup"><span data-stu-id="9a6a1-188">Developer</span></span> | <span data-ttu-id="9a6a1-189">3</span><span class="sxs-lookup"><span data-stu-id="9a6a1-189">3</span></span>        | <span data-ttu-id="9a6a1-190">Hour</span><span class="sxs-lookup"><span data-stu-id="9a6a1-190">Hour</span></span>  | <span data-ttu-id="9a6a1-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="9a6a1-191">100 GBP</span></span>    | <span data-ttu-id="9a6a1-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="9a6a1-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="9a6a1-193">Jednostka czasu — często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="9a6a1-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="9a6a1-194">Czy program PSA przekształca na inne jednostki w przypadku kosztów?</span><span class="sxs-lookup"><span data-stu-id="9a6a1-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="9a6a1-195">Nr</span><span class="sxs-lookup"><span data-stu-id="9a6a1-195">No.</span></span> <span data-ttu-id="9a6a1-196">Przeliczanie jednostek działa tylko dla czasu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-196">Unit conversion works only for time.</span></span> <span data-ttu-id="9a6a1-197">W przypadku kosztów — jeśli system nie może znaleźć ceny dla kombinacji kategorii wydatków i jednostki, cena jest domyślnie ustawiana na 0,00.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="9a6a1-198">Dlaczego rozwiązanie PSA konwertuje jednostki czasu?</span><span class="sxs-lookup"><span data-stu-id="9a6a1-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="9a6a1-199">W niektórych krajach lub regionach istnieje prawny wymóg, aby stawki rozliczania były konfigurowane w dniach.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="9a6a1-200">Negocjowanie cen i przyznawanie rabatów w procesie ofertowym odbywa się przy użyciu stawek dziennych dla każdej roli podlegającej rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="9a6a1-201">Szacowanie harmonogramów i wprowadzanie czasu odbywa się w godzinach.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="9a6a1-202">Aby uwzględnić tę różnicę w jednostkach czasu, program PSA konwertuje jednostki czasu.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="9a6a1-203">Czy w oszacowaniach projektów można zmieniać jednostki czasu?</span><span class="sxs-lookup"><span data-stu-id="9a6a1-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="9a6a1-204">Nr</span><span class="sxs-lookup"><span data-stu-id="9a6a1-204">No.</span></span> <span data-ttu-id="9a6a1-205">Szacowanie harmonogramów można obecnie wykonywać tylko w godzinach.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="9a6a1-206">Czy jednostki i grupy jednostek można edytować, usuwać i dodawać?</span><span class="sxs-lookup"><span data-stu-id="9a6a1-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="9a6a1-207">Tak.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-207">Yes.</span></span> <span data-ttu-id="9a6a1-208">Z wyjątkiem grupy jednostek **Czasu** i jednostki **Godzina** można usuwać i edytować wszystkie jednostki, a także dodawać nowe jednostki.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="9a6a1-209">W usłudze PSA nie można usuwać grupy jednostek **Czas** ani jednostki **Godzina**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="9a6a1-210">Można je jednak aktualizować o przetłumaczony tekst w polu **Nazwa**.</span><span class="sxs-lookup"><span data-stu-id="9a6a1-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]