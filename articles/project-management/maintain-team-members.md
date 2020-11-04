---
title: Obsługa członków zespołu
description: Ten temat zawiera informacje o rezerwowaniu nazwanych zasobów dla zespołów projektów oraz o przypisywaniu ich do zadań.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081878"
---
# <a name="maintain-team-members"></a><span data-ttu-id="150a5-103">Obsługa członków zespołu</span><span class="sxs-lookup"><span data-stu-id="150a5-103">Maintain team members</span></span>

<span data-ttu-id="150a5-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="150a5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="150a5-105">Nazwany zasób można dodać do zespołu projektu, rezerwując go bezpośrednio dla zespołu.</span><span class="sxs-lookup"><span data-stu-id="150a5-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="150a5-106">W programie Dynamics 365 Project Operations wybierz opcję **Projekty** i zaznacz otwarty projekt, dla którego chcesz dokonać rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="150a5-106">In Dynamics 365 Project Operations, go to **Projects** , and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="150a5-107">Na stronie **Projekt** na karcie **Zespół** wybierz opcję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="150a5-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="150a5-108">W oknie dialogowym **Szybkie tworzenie członka zespołu projektu** zaznacz zasób możliwy do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="150a5-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="150a5-109">W polu **Rola** zostanie wstawiona domyślna rola zasobu, jeśli jest ona przypisana.</span><span class="sxs-lookup"><span data-stu-id="150a5-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="150a5-110">Można zmienić rolę.</span><span class="sxs-lookup"><span data-stu-id="150a5-110">You can change the role.</span></span> 
4. <span data-ttu-id="150a5-111">Wybierz daty początku i końca okresu, w którym zasób będzie potrzebny, oraz wybierz metodę alokacji dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="150a5-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="150a5-112">Jeśli chcesz, aby członek zespołu był osobą zatwierdzającą projekt, wybierz opcję **Tak** w polu **Osoba zatwierdzająca projekt**.</span><span class="sxs-lookup"><span data-stu-id="150a5-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="150a5-113">Ten członek zespołu może zatwierdzać wpisy czasu i wydatków przesłane dla tego projektu.</span><span class="sxs-lookup"><span data-stu-id="150a5-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="150a5-114">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="150a5-114">Select **Save**.</span></span>

<span data-ttu-id="150a5-115">Teraz zarezerwowany zasób można przypisywać do zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="150a5-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="150a5-116">Na stronie **Projekt** kliknij kartę **Harmonogram** , aby przypisać zadania nowemu zasobowi.</span><span class="sxs-lookup"><span data-stu-id="150a5-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="150a5-117">Selektor zasobów, który zostanie uruchomiony z pola **Zasoby** w siatce zadań, będzie przedstawiał członków zespołu, których można wybrać.</span><span class="sxs-lookup"><span data-stu-id="150a5-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="150a5-118">W Project Operations nie są ściśle sprzężone rezerwacje zasobów i przydziały zadań.</span><span class="sxs-lookup"><span data-stu-id="150a5-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="150a5-119">Podczas korzystania z selektora zasobów w harmonogramie można przypisywać zadania członkom zespołu na więcej godzin, niż określają ich rezerwacje w projekcie.</span><span class="sxs-lookup"><span data-stu-id="150a5-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="150a5-120">Różnice między rezerwacjami członków zespołu i przydziałami są widoczne na kartach **Zespół** oraz **Uzgadnianie zasobów**.</span><span class="sxs-lookup"><span data-stu-id="150a5-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="150a5-121">Istnieje również możliwość uzgodnienia różnic między zaksięgowaniem a przydziałami dla zasobów na bardziej szczegółowym poziomie.</span><span class="sxs-lookup"><span data-stu-id="150a5-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="150a5-122">Użyj selektora zasobów na karcie **Harmonogram** w celu wyszukiwania i zaznaczania zasobów możliwych do zarezerwowania, które jeszcze nie wchodzą w skład zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="150a5-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="150a5-123">Zasoby są wyświetlane w selektorze zasobów jako **Inne zasoby**.</span><span class="sxs-lookup"><span data-stu-id="150a5-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="150a5-124">Po dokonaniu wyboru zasób zostanie dodany do zespołu projektu i przypisany do zadania, ale nie zostaną wygenerowane żadne rezerwacje.</span><span class="sxs-lookup"><span data-stu-id="150a5-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="150a5-125">Aby zarezerwować dyspozycyjność zasobu dla projektu, można użyć funkcji rozszerzania rezerwacji dostępnej na stronie **Uzgadnianie** albo okna **Tablica harmonogramu**.</span><span class="sxs-lookup"><span data-stu-id="150a5-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="150a5-126">Gdy członek zespołu jest zarezerwowany dla Twojego projektu, do **zarządzania jego rezerwacjami** możesz używać funkcji **Obsługa rezerwacji** albo bezpośrednio tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="150a5-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
