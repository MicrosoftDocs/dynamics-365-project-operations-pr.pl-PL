---
title: Jak przypisać zasób, który można zarezerwować, do zadania w aplikacji sieci Web
description: Przegląd sposobów przypisywania zasobów możliwych do zarezerwowania.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146586"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="9d2de-103">Jak przypisać zasób, który można zarezerwować do zadania w aplikacji sieci Web (aplikacja Project Service, v2.x)?</span><span class="sxs-lookup"><span data-stu-id="9d2de-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9d2de-104">Istnieją dwa sposoby przypisywania zasobu do zadania w Project Service.</span><span class="sxs-lookup"><span data-stu-id="9d2de-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="9d2de-105">Możesz rezerwować zasób jako członek zespołu, a następnie przypisać go do zadania.</span><span class="sxs-lookup"><span data-stu-id="9d2de-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="9d2de-106">Lub możesz też utworzyć ogólnego członka zespołu za pośrednictwem przypisywania roli na zadaniach, wygenerować zespół, a następnie spełnić związane z nim wymagania za pomocą zasobu nazwanego.</span><span class="sxs-lookup"><span data-stu-id="9d2de-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="9d2de-107">Należy zauważyć, że jeśli chcesz przypisać zasób, który można zarezerwować do zadania, członek zespołu zasobu, który można zarezerwować musi posiadać wystarczającą ilość dostępnych rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="9d2de-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="9d2de-108">Stan rezerwacji musi być określony jako Typ zatwierdzenia Zarezerwowano ostatecznie a Stan Zatwierdzono.</span><span class="sxs-lookup"><span data-stu-id="9d2de-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="9d2de-109">Jeśli nie ma wystarczającej liczby rezerwacji dla zasobu, Project Service usuwa przypisania i wyświetla następujący komunikat o błędzie:</span><span class="sxs-lookup"><span data-stu-id="9d2de-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="9d2de-110">*Nie można przypisać zasobu do zadania - Następujące zasoby nie mają zarezerwowanej wystarczającej liczby godzin dla tego projektu*</span><span class="sxs-lookup"><span data-stu-id="9d2de-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="9d2de-111">Zarezerwuj zasób jako członek zespołu, a następnie przypisz zasób do zadania</span><span class="sxs-lookup"><span data-stu-id="9d2de-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="9d2de-112">Dzięki tej metodzie dodajesz zasób do zespołu projektu, a następnie przypisujesz zadania do zasobu w harmonogramie projektu.</span><span class="sxs-lookup"><span data-stu-id="9d2de-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="9d2de-113">Oto, jak to zrobić:</span><span class="sxs-lookup"><span data-stu-id="9d2de-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="9d2de-114">W siatce Członek zespołu dodaj nowego członka zespołu, wybierając **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="9d2de-115">Na ekranie Szybkie tworzenie członków zespołu wybierz nazwę zasobu, który można zarezerwować, i ustaw rolę.</span><span class="sxs-lookup"><span data-stu-id="9d2de-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="9d2de-116">Wybierz daty **Od** i **Do**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="9d2de-117">![Zrzut ekranu składnika Dodawanie członka zespołu](media/FAQ-Resources-to-Tasks2-1.png "Zrzut ekranu składnika Dodawanie członka zespołu")</span><span class="sxs-lookup"><span data-stu-id="9d2de-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="9d2de-118">Wybierz jedną z następujących metod alokacji, aby zarezerwować zasób:</span><span class="sxs-lookup"><span data-stu-id="9d2de-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="9d2de-119">**Pełna dyspozycyjność** rezerwuje pełną dyspozycyjność zasobu dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="9d2de-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9d2de-120">**Dyspozycyjność procentowa** rezerwuje zasób procentowo dla dyspozycyjności zasobu dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="9d2de-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9d2de-121">**Według godzin — rozłóż równomiernie** rezerwuje zasób na określoną liczbą godzin, rozkładając je równomiernie w ciągu dnia dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="9d2de-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="9d2de-122">**Według godzin — Najwięcej na początku** rezerwuje zasób na określoną liczbą godzin, kładąc nacisk na godziny początkowe w ciągu dnia dla określonych dat Od/Do.</span><span class="sxs-lookup"><span data-stu-id="9d2de-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="9d2de-123">Nie wybieraj **Brak**, ponieważ ta metoda dodaje zasób do zespołu, ale nie tworzy żadnych rezerwacji, które absorbują dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d2de-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="9d2de-124">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-124">Select **Save**.</span></span>

    <span data-ttu-id="9d2de-125">Należy zauważyć, że godziny rezerwacji muszą pokrywać nakład pracy i zakres dat zadań, które można przypisać do tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d2de-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="9d2de-126">Jeśli nie są one zgodne, nie możesz przypisać zasobu do zadania.</span><span class="sxs-lookup"><span data-stu-id="9d2de-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="9d2de-127">Na strukturze podziału pracy (SPP) dla zadania kliknij listę rozwijaną komórki zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d2de-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="9d2de-128">Następnie:</span><span class="sxs-lookup"><span data-stu-id="9d2de-128">Then:</span></span> 

    1. <span data-ttu-id="9d2de-129">Wybierz **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-129">Select **Add**.</span></span>
    2. <span data-ttu-id="9d2de-130">Wybierz listę rozwijaną w obszarze **Zasoby** i wybierz dodanego powyżej członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="9d2de-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="9d2de-131">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-131">Select **OK**.</span></span> <span data-ttu-id="9d2de-132">Członek zespołu teraz jest przypisany do zadania.</span><span class="sxs-lookup"><span data-stu-id="9d2de-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="9d2de-133">![Zrzut ekranu dotyczący dodawania zasobów z SPP](media/FAQ-Resources-to-Tasks2-2.png "Zrzut ekranu dotyczący dodawania zasobów z SPP")</span><span class="sxs-lookup"><span data-stu-id="9d2de-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="9d2de-134">Na siatce członków zespołu zobaczysz sumę godzin przypisanych do zasobu w obszarze Przypisane godziny.</span><span class="sxs-lookup"><span data-stu-id="9d2de-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="9d2de-135">Będzie on mniejsza od liczby godzin zarezerwowanych dla zasobu lub równa z nią.</span><span class="sxs-lookup"><span data-stu-id="9d2de-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9d2de-136">![Zrzut ekranu z przypisanymi godzinami dla zasobu](media/FAQ-Resources-to-Tasks2-3.png "Zrzut ekranu z przypisanymi godzinami dla zasobu")</span><span class="sxs-lookup"><span data-stu-id="9d2de-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="9d2de-137">Jeśli zadanie, które próbujesz przypisać do zasobu rozpoczyna się dacie zakończenia rezerwacji zasobów, zasób nie będzie widoczny na liście rozwijanej.</span><span class="sxs-lookup"><span data-stu-id="9d2de-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="9d2de-138">Należy zauważyć, że można przypisać zasób do większej liczny godzin niż godziny zarezerwowane jeśli zasób posiada jeszcze nieprzypisaną dyspozycyjność.</span><span class="sxs-lookup"><span data-stu-id="9d2de-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="9d2de-139">W tym przypadku zasób będzie tylko częściowo przypisany do ich rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="9d2de-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="9d2de-140">Można wyświetlić te pozostałe godziny nieprzypisane do zadań dodając kolumnę Nieobsadzone godziny do struktury podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="9d2de-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="9d2de-141">Jeśli zasoby są przypisane do zarezerwowanych godzin (liczba godzin dla nich zarezerwowanych równa się liczbie przypisanych do nich godzin), pojawi się komunikat o błędzie podczas próby przypisania do nich kolejnych zadań:</span><span class="sxs-lookup"><span data-stu-id="9d2de-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="9d2de-142">*Nie można przypisać zasobu do zadania - Następujące zasoby nie mają zarezerwowanej wystarczającej liczby godzin dla tego projektu.*</span><span class="sxs-lookup"><span data-stu-id="9d2de-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="9d2de-143">Ponadto domyślny członek zespołu menedżera projektu, który jest dodawany do zespołu podczas tworzenia projektu jest dodawany bez żadnych rezerwacji i nie można go przypisać do żadnego zadania.</span><span class="sxs-lookup"><span data-stu-id="9d2de-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="9d2de-144">Nie będą oni widoczni na liście rozwijanej zasobów dla zadań.</span><span class="sxs-lookup"><span data-stu-id="9d2de-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="9d2de-145">Jeśli chcesz przypisać ten zasób, musisz ich usunąć z zespołu, a następnie ponownie dodaj za pomocą metody alokacji innej niż Brak.</span><span class="sxs-lookup"><span data-stu-id="9d2de-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="9d2de-146">Są oni dodawani do zespołu podczas tworzenia projektu, aby projekt miał domyślnie co najmniej jedną osobę zatwierdzającą.</span><span class="sxs-lookup"><span data-stu-id="9d2de-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="9d2de-147">Utwórz ogólnego członka zespołu za pomocą przypisania roli do zadania</span><span class="sxs-lookup"><span data-stu-id="9d2de-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="9d2de-148">Ta metoda sprawia, że zasoby mają odpowiednią ilość rezerwacji dla zadań.</span><span class="sxs-lookup"><span data-stu-id="9d2de-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="9d2de-149">Po pierwsze tworzysz symbol zastępczy lub zasób ogólny, który opisuje cechy zasobu nazwanego, który ma ostatecznie pracować na zadaniach, tworząc zespół po przypisaniu ról do zadań.</span><span class="sxs-lookup"><span data-stu-id="9d2de-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="9d2de-150">Oto, jak to zrobić:</span><span class="sxs-lookup"><span data-stu-id="9d2de-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="9d2de-151">Na strukturze podziału pracy wybierz zadanie.</span><span class="sxs-lookup"><span data-stu-id="9d2de-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="9d2de-152">Wybierz ikonę listy rozwijanej **Rola przypisana** w komórce zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d2de-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="9d2de-153">Wybierz listę rozwijaną **Rola** i wybierz rolę dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="9d2de-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="9d2de-154">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="9d2de-155">![Zrzut ekranu dotyczący użycia SPP do dodawania zasobów](media/FAQ-Resources-to-Tasks2-4.png "Zrzut ekranu dotyczący użycia SPP do dodawania zasobów")</span><span class="sxs-lookup"><span data-stu-id="9d2de-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="9d2de-156">Po zakończeniu przypisywania ról do zadań w SPP, wybierz **Wygeneruj zespół projektu**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="9d2de-157">Usługa Project Service tworzy minimalną liczbę ogólnych członków zespołu, w oparciu o role, korzystając z jednostek organizacyjnych i kalendarza projektu agregując przypisania zadań.</span><span class="sxs-lookup"><span data-stu-id="9d2de-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9d2de-158">![Zrzut ekranu z generowaniem zespołu projektu](media/FAQ-Resources-to-Tasks2-5.png "Zrzut ekranu z generowaniem zespołu projektu")</span><span class="sxs-lookup"><span data-stu-id="9d2de-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="9d2de-159">Na siatce Członek zespołu zobaczysz zasoby typu Zasób ogólny z nazwą roli i stanowiska.</span><span class="sxs-lookup"><span data-stu-id="9d2de-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="9d2de-160">Jeśli dwa zasoby są potrzebne dla roli, aby zakończyć pracę, funkcja Generuj zespół tworzy dwóch członków zespołu i używa nazwy stanowiska, aby odróżnić ich od siebie.</span><span class="sxs-lookup"><span data-stu-id="9d2de-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9d2de-161">![Zrzut ekranu pokazujący dodawanie dwóch zasobów ogólnych](media/FAQ-Resources-to-Tasks2-6.png "Zrzut ekranu pokazujący dodawanie dwóch zasobów ogólnych")</span><span class="sxs-lookup"><span data-stu-id="9d2de-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="9d2de-162">Można otworzyć bazowe wymagania zasobu dla ogólnego członka zespołu, wybierając łącze w obszarze Wymaganie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d2de-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9d2de-163">![Zrzut ekranu przedstawiający otwieranie bazowego wymagania zasobu](media/FAQ-Resources-to-Tasks2-7.png "Zrzut ekranu przedstawiający otwieranie bazowego wymagania zasobu")</span><span class="sxs-lookup"><span data-stu-id="9d2de-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="9d2de-164">Wybierz **Zarezerwuj** dla zasobu ogólnego, a w następnym kroku będziesz mógł użyć tablicy harmonogramu, aby wyszukać i zarezerwować rzeczywisty zasób.</span><span class="sxs-lookup"><span data-stu-id="9d2de-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="9d2de-165">Można również przesłać wymagania do spełnienia przez menedżera zasobu wybierając **Prześlij żądanie**.</span><span class="sxs-lookup"><span data-stu-id="9d2de-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="9d2de-166">Gdy zasób ogólny jest zrealizowany przez zasób nazwany, zasób ogólny jest usuwany z zespołu a przypisania zadań dla zasobu ogólnego są przypisywane do zasobu nazwanego, który zrealizował wymaganie zasobu dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="9d2de-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

