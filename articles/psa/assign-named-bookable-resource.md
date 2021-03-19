---
title: Rezerwowanie nazwanych zasobów możliwych do zarezerwowania dla zespołu projektu i przypisywanie zadań
description: Ten temat zawiera informacje na temat rezerwowania nazwanych zasobów dla zespołów projektów oraz o przypisywaniu ich do zadań.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 6169f2bdc107e63d666fb32d34f531fd5d472c2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291452"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="1649b-103">Rezerwowanie nazwanych zasobów możliwych do zarezerwowania dla zespołu projektu i przypisywanie zadań</span><span class="sxs-lookup"><span data-stu-id="1649b-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1649b-104">Nazwany zasób można dodać do zespołu projektu, rezerwując go bezpośrednio dla zespołu.</span><span class="sxs-lookup"><span data-stu-id="1649b-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="1649b-105">W tym celu wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="1649b-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="1649b-106">W programie Project Service Automation wybierz opcję **Projekty** i zaznacz otwarty projekt, dla którego chcesz dokonać rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="1649b-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="1649b-107">Na stronie **Projekt** na karcie **Zespół** kliknij opcję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="1649b-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Dodawanie członka zespołu z poziomu karty Zespół](media/RM-how-to-1.png)

3. <span data-ttu-id="1649b-109">W oknie dialogowym **Szybkie tworzenie członka zespołu projektu** zaznacz zasób możliwy do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="1649b-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="1649b-110">W polu **Rola** zostanie wstawiona domyślna rola zasobu, jeśli jest ona przypisana.</span><span class="sxs-lookup"><span data-stu-id="1649b-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="1649b-111">W razie potrzeby można zmienić rolę.</span><span class="sxs-lookup"><span data-stu-id="1649b-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="1649b-112">Wybierz daty początku i końca okresu, w którym zasób będzie potrzebny, oraz wybierz metodę alokacji dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="1649b-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="1649b-113">Jeśli chcesz, aby członek zespołu był osobą zatwierdzającą projekt, wybierz opcję **Tak** w polu **Osoba zatwierdzająca projekt**.</span><span class="sxs-lookup"><span data-stu-id="1649b-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="1649b-114">Oznacza to, że członek zespołu może zatwierdzać wpisy czasu i wydatków przesłane dla tego projektu.</span><span class="sxs-lookup"><span data-stu-id="1649b-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="1649b-115">Kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="1649b-115">Click **Save**.</span></span>

![Dodawanie członka zespołu w formularzu szybkiego tworzenia](media/RM-how-to-2.png)


<span data-ttu-id="1649b-117">Teraz zarezerwowany zasób można przypisywać do zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="1649b-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="1649b-118">Na stronie **Projekt** kliknij kartę **Harmonogram**, aby przypisać zadania nowemu zasobowi.</span><span class="sxs-lookup"><span data-stu-id="1649b-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="1649b-119">Selektor zasobów, który zostanie uruchomiony z pola **Zasoby** w siatce zadań, będzie przedstawiał członków zespołu, których można wybrać.</span><span class="sxs-lookup"><span data-stu-id="1649b-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Przypisywanie członka zespołu do zadania na karcie Harmonogram](media/RM-how-to-3.png)

<span data-ttu-id="1649b-121">W wersji 3 programu Project Service Automation (PSA) rezerwacje zasobów i przypisania zadań nie są ściśle powiązane.</span><span class="sxs-lookup"><span data-stu-id="1649b-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="1649b-122">Oznacza to, że podczas korzystania z selektora zasobów w harmonogramie można przypisywać zadania członkom zespołu na więcej godzin, niż określają ich rezerwacje w projekcie.</span><span class="sxs-lookup"><span data-stu-id="1649b-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="1649b-123">Różnice między rezerwacjami członków zespołu i ich przypisaniami można zobaczyć na karcie **Zespół** lub na karcie **Uzgadnianie zasobów**. Istnieje również możliwość uzgadniania różnic między rezerwacjami i przypisaniami zasobów na bardziej szczegółowym poziomie.</span><span class="sxs-lookup"><span data-stu-id="1649b-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Karta Uzgadnianie zasobów](media/RM-how-to-4.png)

<span data-ttu-id="1649b-125">Można również użyć selektora zasobów na karcie **Harmonogram** w celu wyszukiwania i zaznaczania zasobów możliwych do zarezerwowania, które jeszcze nie wchodzą w skład zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="1649b-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="1649b-126">Są one wyświetlane w selektorze zasobów jako **Inne zasoby**.</span><span class="sxs-lookup"><span data-stu-id="1649b-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Przypisywanie zasobu niebędącego członkiem zespołu do zadania](media/RM-how-to-5.png)

<span data-ttu-id="1649b-128">Po wykonaniu tej czynności zasób zostanie dodany do zespołu projektu i przypisany do zadania, ale nie zostaną wygenerowane żadne rezerwacje.</span><span class="sxs-lookup"><span data-stu-id="1649b-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Członek zespołu z przypisaniami, ale bez rezerwacji](media/RM-how-to-6.png)

<span data-ttu-id="1649b-130">Aby zarezerwować dyspozycyjność zasobu dla projektu, można użyć funkcji rozszerzania rezerwacji dostępnej na stronie **Uzgadnianie** albo okna **Tablica harmonogramu**.</span><span class="sxs-lookup"><span data-stu-id="1649b-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Rozszerzanie rezerwacji dla członka zespołu na karcie Uzgadnianie zasobów](media/RM-how-to-7.png)

<span data-ttu-id="1649b-132">Gdy członek zespołu jest zarezerwowany dla Twojego projektu, do zarządzania jego rezerwacjami możesz używać funkcji Obsługa rezerwacji albo bezpośrednio tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="1649b-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]