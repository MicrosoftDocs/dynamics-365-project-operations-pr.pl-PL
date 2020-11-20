---
title: Zarządzanie strefami czasowymi
description: Po utworzeniu projektu jego strefa czasowa jest oparta na strefie czasowej określonej w szablonie godziny pracy zastosowanym w programie.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119836"
---
# <a name="manage-time-zones"></a><span data-ttu-id="ccce6-103">Zarządzanie strefami czasowymi</span><span class="sxs-lookup"><span data-stu-id="ccce6-103">Manage time zones</span></span>

<span data-ttu-id="ccce6-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="ccce6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="ccce6-105">Projekty</span><span class="sxs-lookup"><span data-stu-id="ccce6-105">Projects</span></span>

<span data-ttu-id="ccce6-106">Po utworzeniu projektu jego strefa czasowa jest oparta na strefie czasowej określonej w szablonie godziny pracy zastosowanym w programie.</span><span class="sxs-lookup"><span data-stu-id="ccce6-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="ccce6-107">W szablonie **Projekt** daty są zawsze określane względem strefy czasowej użytkownika zalogowanego na każdej karcie, z wyjątkiem karty **Zadanie**. Podczas wyświetlania struktury podziału pracy daty będą zawsze wyświetlane w strefie czasowej projektu.</span><span class="sxs-lookup"><span data-stu-id="ccce6-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="ccce6-108">Zadania</span><span class="sxs-lookup"><span data-stu-id="ccce6-108">Tasks</span></span>

<span data-ttu-id="ccce6-109">Podczas tworzenia zadania godzina rozpoczęcia, godzina zakończenia i liczba godzin/dzień jest kontrolowana przez godziny pracy projektu.</span><span class="sxs-lookup"><span data-stu-id="ccce6-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="ccce6-110">Jeśli na przykład zadanie zostanie utworzone dla projektu, którego strefa czasowa ma wartość -8 PST i ma następujące godziny pracy: 9:00 rano – 5:00 po południu od poniedziałku do piątku, każde zadanie utworzone bez przydziału będzie respektować godzinę rozpoczęcia i zakończenia w kalendarzu projektu.</span><span class="sxs-lookup"><span data-stu-id="ccce6-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="ccce6-111">Zarządzanie zasobami za pomocą stref czasowych</span><span class="sxs-lookup"><span data-stu-id="ccce6-111">Manage resources with time zones</span></span>

<span data-ttu-id="ccce6-112">Aby uzyskać dokładne i przewidywalne wyniki podczas korzystania z **Przedłużenia rezerwacja**, należy spełnić dwa podstawowe kluczowe wymagania:</span><span class="sxs-lookup"><span data-stu-id="ccce6-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="ccce6-113">Użytkownik musi skonfigurować strefę czasową swoich urządzeń, aby odpowiadała strefom czasowym zdefiniowanym w **ustawieniach personalizacji** systemu.</span><span class="sxs-lookup"><span data-stu-id="ccce6-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Ustawienia strefy czasowej w systemie Windows 10](media/reconcile-assignments-03.png)

  ![Ustawienia strefy czasowej w ustawieniach personalizacji](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="ccce6-116">Zasób możliwy do zarezerwowania musi mieć co najmniej jedną minutę czasu pracy, który pokrywa się z rozkładem używanym do definiowania żądanego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ccce6-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="ccce6-117">Na przykład następujące zasoby z godzinami pracy, które mieszczą się w zakresie 9:00 rano i 7:00 wieczorem.</span><span class="sxs-lookup"><span data-stu-id="ccce6-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Porównanie rozkładów zasobów](media/reconcile-assignments-05.png)

<span data-ttu-id="ccce6-119">W poniższej tabeli przedstawiono:</span><span class="sxs-lookup"><span data-stu-id="ccce6-119">The following table shows:</span></span>

- <span data-ttu-id="ccce6-120">Szablon kalendarza projektu</span><span class="sxs-lookup"><span data-stu-id="ccce6-120">A project calendar template</span></span>
- <span data-ttu-id="ccce6-121">Zasób A: ten zasób ma ten sam kalendarz i znajduje się w tej samej strefie czasowej, co projekt.</span><span class="sxs-lookup"><span data-stu-id="ccce6-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="ccce6-122">Godziną rozpoczęcia rezerwacji będzie 9:00.</span><span class="sxs-lookup"><span data-stu-id="ccce6-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="ccce6-123">Zasób B: ten zasób znajduje się w innej strefie czasowej niż projekt i zaczyna pracę o 7:00 rano w swojej strefie czasowej.</span><span class="sxs-lookup"><span data-stu-id="ccce6-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="ccce6-124">Jednak rezerwacje zaczynają się od godziny 9:00, która jest najwcześniejszym czasem rozpoczęcia rozkładu przydziału.</span><span class="sxs-lookup"><span data-stu-id="ccce6-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="ccce6-125">Zasoby C i D: zasoby znajdują się w różnych strefach czasowych, różniącymi się między sobą i projektem, a ich rezerwacje zaczynają się nie wcześniej niż ich dostęp do swoich godzin rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="ccce6-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="ccce6-126">Encja</span><span class="sxs-lookup"><span data-stu-id="ccce6-126">Entity</span></span>  |<span data-ttu-id="ccce6-127">Kalendarz</span><span class="sxs-lookup"><span data-stu-id="ccce6-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="ccce6-128">Szablon kalendarza projektu</span><span class="sxs-lookup"><span data-stu-id="ccce6-128">Project calendar template</span></span>   | ![kalendarz projektu](media/reconcile-assignments-06.png) |
|<span data-ttu-id="ccce6-130">Zasób A</span><span class="sxs-lookup"><span data-stu-id="ccce6-130">Resource A</span></span>  | ![Kalendarz zasobu A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="ccce6-132">Zasób B</span><span class="sxs-lookup"><span data-stu-id="ccce6-132">Resource B</span></span>  |  ![Kalendarz zasobu B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="ccce6-134">Zasób C</span><span class="sxs-lookup"><span data-stu-id="ccce6-134">Resource C</span></span>  |  ![Kalendarz zasobu C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="ccce6-136">Zasób D</span><span class="sxs-lookup"><span data-stu-id="ccce6-136">Resource D</span></span>  | ![Kalendarz zasobu D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="ccce6-138">Po przejściu do widoku **uzgodnienia** zostaną wyświetlone przydziały zasobów i skojarzone niedobory rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="ccce6-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Uzgadnianie widoku przed rozszerzeniem](media/reconcile-assignments-10.png)

<span data-ttu-id="ccce6-140">Po zastosowaniu funkcji przedłużenia rezerwacji dla każdego zasobu rezerwacje są pomyślnie przedłużane dla każdego zasobu, ponieważ godziny pracy poszczególnych zasobów pokrywają się z rozkładem niedoborów.</span><span class="sxs-lookup"><span data-stu-id="ccce6-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Widok Uzgodnienie po rozszerzeniu rezerwacji](media/reconcile-assignments-11.png) 

<span data-ttu-id="ccce6-142">Należy zwrócić uwagę, że bliższe zapoznanie się z szczegółowymi informacjami dotyczącymi rezerwacji pokazuje różnice w czasie rozpoczęcia rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="ccce6-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="ccce6-143">Rezerwacje zaczynają się nie wcześniej niż godzina rozpoczęcia rozkładu przydziału i nie wcześniej niż jest dostępna godzina rozpoczęcia zasobu.</span><span class="sxs-lookup"><span data-stu-id="ccce6-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nowe rezerwacje zasobów na tablicy harmonogramu](media/reconcile-assignments-12.png)
