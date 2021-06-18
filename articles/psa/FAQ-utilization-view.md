---
title: Wyświetlanie odpłatnego wykorzystania zasobów
description: W tym temacie zamieszczono informacje dotyczące widoku wykorzystania zasobów.
author: ruhercul
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
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992847"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="c05e3-103">Wyświetlanie odpłatnego wykorzystania zasobów</span><span class="sxs-lookup"><span data-stu-id="c05e3-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="c05e3-104">**Widok wykorzystania** dostępny na stronie **Wykorzystanie zasobów w usłudze Project Service** pokazuje odpłatne wykorzystanie każdego zasobu możliwego do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="c05e3-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="c05e3-105">Widok jest oparty na tablicy harmonogramu, więc zawiera wiele tych samych funkcji.</span><span class="sxs-lookup"><span data-stu-id="c05e3-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Zrzut ekranu przedstawiający Widok wykorzystania](media/FAQ-utilization-1.png)
 

<span data-ttu-id="c05e3-107">Obliczenia odpłatnego wykorzystania działają w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="c05e3-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="c05e3-108">Odpłatne wykorzystanie = (Odpłatne rzeczywiste godziny pracy) / (Dyspozycyjność zasobu)</span><span class="sxs-lookup"><span data-stu-id="c05e3-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="c05e3-109">Komórki reprezentują obliczone odpłatne wykorzystanie dla wybranego okresu (dni, tygodnie lub miesiące).</span><span class="sxs-lookup"><span data-stu-id="c05e3-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="c05e3-110">Kolory w każdej komórce ukazują odpłatne wykorzystanie zasobu w porównaniu z docelowym odpłatnym wykorzystaniem.</span><span class="sxs-lookup"><span data-stu-id="c05e3-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="c05e3-111">Wykorzystanie docelowe można ustawić w domyślnej roli zasobu lub w samym zasobie.</span><span class="sxs-lookup"><span data-stu-id="c05e3-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="c05e3-112">Obliczenia analizują najpierw osobę dla wykorzystania docelowego, a następnie domyślną rolę zasobu.</span><span class="sxs-lookup"><span data-stu-id="c05e3-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="c05e3-113">Ustawianie domyślnego wykorzystania zasobu</span><span class="sxs-lookup"><span data-stu-id="c05e3-113">Set target on a resource</span></span>

1. <span data-ttu-id="c05e3-114">Wybierz kolejno opcje **Zasoby** \> **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c05e3-115">Zaznacz zasób, aby otworzyć jego rekord.</span><span class="sxs-lookup"><span data-stu-id="c05e3-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="c05e3-116">Na karcie **Project Service** możesz ustawić docelowe wykorzystanie zasobu.</span><span class="sxs-lookup"><span data-stu-id="c05e3-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Zrzut ekranu przedstawiający wykorzystanie karty Project Service do ustawiania wykorzystania zasobu](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="c05e3-118">Ustawianie docelowego wykorzystania dla roli</span><span class="sxs-lookup"><span data-stu-id="c05e3-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="c05e3-119">Wybierz kolejno opcje **Zasoby** \> **Role zasobu**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c05e3-120">Zaznacz rolę i otwórz rekord.</span><span class="sxs-lookup"><span data-stu-id="c05e3-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="c05e3-121">Wybierz docelowe wykorzystanie dla roli.</span><span class="sxs-lookup"><span data-stu-id="c05e3-121">Set the target utilization for the role.</span></span>

> ![Zrzut ekranu przedstawiający wykorzystanie Ról zasobów do ustawiania wykorzystania zasobu](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="c05e3-123">Obliczanie odpłatnego wykorzystania zasobu</span><span class="sxs-lookup"><span data-stu-id="c05e3-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="c05e3-124">Aby obliczyć odpłatne wykorzystanie zasobu, należy spełnić kilka warunków wstępnych.</span><span class="sxs-lookup"><span data-stu-id="c05e3-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="c05e3-125">Ustawianie domyślnej roli dla pojedynczego zasobu</span><span class="sxs-lookup"><span data-stu-id="c05e3-125">Set default role for individual resource</span></span>

<span data-ttu-id="c05e3-126">Po pierwsze wykorzystanie docelowe musi zostać ustawione dla konkretnego zasobu lub dla ról zasobów.</span><span class="sxs-lookup"><span data-stu-id="c05e3-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="c05e3-127">Jeśli korzystasz z ról zasobów dla celów to każdy pojedynczy zasób musi mieć rolę domyślną.</span><span class="sxs-lookup"><span data-stu-id="c05e3-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="c05e3-128">Aby to ustawić, wybierz kolejno opcje **Zasoby** \> **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c05e3-129">Wybierz zasób, otwórz rekord, a następnie wybierz kartę **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="c05e3-130">W siatce **Rola zasobu** upewnij się, że istnieje tylko jedna rola dla zasobu, a pole **Jest domyślne** zawiera wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="c05e3-131">Zmiana typu rozliczania roli zasobu</span><span class="sxs-lookup"><span data-stu-id="c05e3-131">Change billing type for resource role</span></span>

<span data-ttu-id="c05e3-132">Role zasobów muszą mieć ustawiony typ rozliczania **Odpłatne**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="c05e3-133">Wybierz kolejno opcje **Zasoby** \> **Role zasobu**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c05e3-134">Otwórz rekord, który chcesz zaktualizować, a następnie ustaw typ rozliczania domyślnie na **Odpłatne**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="c05e3-135">Określanie godzin pracy dla roli zasobów</span><span class="sxs-lookup"><span data-stu-id="c05e3-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="c05e3-136">Zasób musi mieć określone godziny pracy dla obliczania wydajności.</span><span class="sxs-lookup"><span data-stu-id="c05e3-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="c05e3-137">Wybierz kolejno opcje **Zasoby** \> **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c05e3-138">Zaznacz zasób, aby otworzyć rekord, a następnie kliknij opcję **Pokaż godziny pracy**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="c05e3-139">Możesz zbiorczo zaktualizować listę zasobów, stosując polecenie **Szablon czasu pracy** z poziomu widoku **Lista zasobów**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="c05e3-140">Rozwiązywanie problemów z odpłatnymi rzeczywistymi godzinami</span><span class="sxs-lookup"><span data-stu-id="c05e3-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="c05e3-141">Odpłatne rzeczywiste godziny pracy pochodzą z encji **Wartości rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="c05e3-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="c05e3-142">Wartości rzeczywiste z typem rozliczania **Odpłatne** są uwzględniane w obliczeniach, więc musisz posiadać projekty, gdzie wartości rzeczywiste są odpłatne.</span><span class="sxs-lookup"><span data-stu-id="c05e3-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="c05e3-143">Jeśli nie widzisz wykorzystania odpłatnego, oto co możesz sprawdzić:</span><span class="sxs-lookup"><span data-stu-id="c05e3-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="c05e3-144">Zasób ma godziny pracy zdefiniowane dla wydajności.</span><span class="sxs-lookup"><span data-stu-id="c05e3-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="c05e3-145">Zasób ma indywidualnie zdefiniowane docelowe wykorzystanie lub ma przypisaną rolę domyślną.</span><span class="sxs-lookup"><span data-stu-id="c05e3-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="c05e3-146">Rola ma zdefiniowane dla niej docelowe wykorzystanie.</span><span class="sxs-lookup"><span data-stu-id="c05e3-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="c05e3-147">Wartości rzeczywiste mają typ rozliczania **Odpłatne** dla okresu, dla którego zamierzasz obliczyć wykorzystanie.</span><span class="sxs-lookup"><span data-stu-id="c05e3-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="c05e3-148">Sprawdź następujące parametry, jeśli widzisz wartości rzeczywiste z typem rozliczania innym niż Odpłatne:</span><span class="sxs-lookup"><span data-stu-id="c05e3-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="c05e3-149">Rola użyta dla wartości rzeczywistej ma domyślny typ rozliczania inny niż odpłatne.</span><span class="sxs-lookup"><span data-stu-id="c05e3-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="c05e3-150">Rola dla pozycji kontraktu projektu, z kopią projektu została ustawiona na nieodpłatne.</span><span class="sxs-lookup"><span data-stu-id="c05e3-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="c05e3-151">Projekt nie posiada skojarzonej pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="c05e3-151">The project does not have an associated contract line.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]