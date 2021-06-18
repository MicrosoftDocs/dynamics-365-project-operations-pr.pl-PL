---
title: Zarządzaj zasobami
description: W tym temacie zamieszczono informacje dotyczące sposobu zarządzania zasobami.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997839"
---
# <a name="manage-resources"></a><span data-ttu-id="2fba4-103">Zarządzaj zasobami</span><span class="sxs-lookup"><span data-stu-id="2fba4-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2fba4-104">Dynamics 365 Project Service Automation zawiera pulpit nawigacyjny Menedżer zasobów umożliwiający graficzne przeglądy popytu i wykorzystania zasobów w całej organizacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="2fba4-105">Korzystając z wykresów na tym pulpicie nawigacyjnym, można wizualizować następujące informacje:</span><span class="sxs-lookup"><span data-stu-id="2fba4-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="2fba4-106">**Zapotrzebowanie na zasoby** — na wykresie **Aktywne żądania zasobów** przedstawiono zasoby, które zostały przesłane.</span><span class="sxs-lookup"><span data-stu-id="2fba4-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="2fba4-107">Zasoby są agregowane według ról lub projektów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="2fba4-108">**Nieprzesłane zapotrzebowanie na zasoby** — wykres **Nieprzydzielone zapotrzebowanie na zasoby** pokazuje wszystkie wymagania zasobu, które nie zostały przesłane.</span><span class="sxs-lookup"><span data-stu-id="2fba4-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="2fba4-109">Ułatwia to menedżerom zasobów wyświetlanie zapotrzebowania, które nie jest firmą i może być przesłane za pośrednictwem żądania zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="2fba4-110">**Wykorzystanie do rozliczenia za ubiegły tydzień** — wykres **Wykorzystanie według roli** pokazuje procent rzeczywistego wykorzystania zasobu do rozliczenia według roli względem docelowego wykorzystania według roli, które podlega rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fba4-111">Aby wykres **Wykorzystanie według roli** był dostępny, należy utworzyć zadanie, które uruchamia przepływ pracy UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="2fba4-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="2fba4-112">To zadanie cykliczne jest uruchamiane co siedem dni w celu obliczenia wykorzystania do zafakturowania przez ostatnie siedem dni.</span><span class="sxs-lookup"><span data-stu-id="2fba4-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="2fba4-113">Wyniki są agregowane według ról.</span><span class="sxs-lookup"><span data-stu-id="2fba4-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="2fba4-114">Członkowie zespołu zarządzania projektem</span><span class="sxs-lookup"><span data-stu-id="2fba4-114">Manage project team members</span></span>

<span data-ttu-id="2fba4-115">Menedżerowie projektów mogą używać pulpitu nawigacyjnego Menedżer zasobów do zarządzania zasobami w projektach.</span><span class="sxs-lookup"><span data-stu-id="2fba4-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="2fba4-116">Na przykład użytkownicy mogą dodawać członków zespołu bezpośrednio do projektu i rezerwować członków zespołu, aby spełnić wymagania dotyczące zasobów przechwycone przez zasób ogólny.</span><span class="sxs-lookup"><span data-stu-id="2fba4-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="2fba4-117">Dodawanie członka zespołu bezpośrednio do projektu</span><span class="sxs-lookup"><span data-stu-id="2fba4-117">Add a team member directly to a project</span></span>

<span data-ttu-id="2fba4-118">Aby dodać członka zespołu bezpośrednio do projektu, na stronie **projekty** na karcie **zespół** wybierz opcję **nowy.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="2fba4-119">Zostanie wyświetlone okno dialogowe **szybkie tworzenie: członek zespołu projektu**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="2fba4-120">W tym oknie dialogowym można wykonać następujące zadania:</span><span class="sxs-lookup"><span data-stu-id="2fba4-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="2fba4-121">**Zarezerwowanie nazwanego zasobu** – w polu **Zasób, który można zarezerwować** wybierz nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="2fba4-122">Następnie wybierz rolę, ustaw okres i wybierz metodę alokacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="2fba4-123">Wybrany nazwany zasób jest dodawany do projektu przy użyciu wybranej metody alokacji i kalendarza zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="2fba4-124">**Dodaj zasób ogólny** — pozostaw puste pole **zasobu, który można zarezerwować**, a następnie wybierz rolę, ustaw okres i wybierz preferowaną metodę alokacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="2fba4-125">Zasób ogólny jest dodawany do zespołu jako symbol zastępczy w celu przechowywania wzorca popytu używanego do rezerwowania nazwanych zasobów w zespole.</span><span class="sxs-lookup"><span data-stu-id="2fba4-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="2fba4-126">Wymóg jest składany zgodnie z kalendarzem projektu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="2fba4-127">**Dodaj nazwany zasób do zespołu bez zużywania dyspozycyjności zasobu** — w polu **zasobu, który można zarezerwować** wybierz zasób.</span><span class="sxs-lookup"><span data-stu-id="2fba4-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="2fba4-128">Następnie wybierz okres i zaznacz **Brak** jako metodę alokacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="2fba4-129">Zasób jest dodawany do zespołu, ale jego dyspozycyjność nie jest wykorzystywana poprzez rezerwację.</span><span class="sxs-lookup"><span data-stu-id="2fba4-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="2fba4-130">Rezerwowanie członka zespołu w celu spełnienia wymagań dotyczących zasobów dla zasobu ogólnego</span><span class="sxs-lookup"><span data-stu-id="2fba4-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="2fba4-131">W usłudze PSA można zarezerwować zasób ogólny w zespole projektu i określić jego rolę, wymaganą dyspozycyjność i sposób dystrybucji tej dyspozycyjności.</span><span class="sxs-lookup"><span data-stu-id="2fba4-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="2fba4-132">W zapotrzebowaniu na zasoby można określić atrybuty, które są skojarzone z zasobem ogólnym.</span><span class="sxs-lookup"><span data-stu-id="2fba4-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="2fba4-133">Do atrybutów tych zalicza się wymagane kwalifikacje, preferowaną jednostkę organizacyjną i preferowane zasoby.</span><span class="sxs-lookup"><span data-stu-id="2fba4-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="2fba4-134">Wykonaj te kroki, aby określić wymagane kwalifikacje dla zasobu ogólnego w przypadku dewelopera.</span><span class="sxs-lookup"><span data-stu-id="2fba4-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="2fba4-135">Na stronie **projekty** na karcie **zespół** wybierz opcję **nowy**, aby zarezerwować zasób ogólny.</span><span class="sxs-lookup"><span data-stu-id="2fba4-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Zasób ogólny zarezerwowany w zespole](media/Resource-Management-image9.png)

2. <span data-ttu-id="2fba4-137">W widoku **wszyscy członków zespołu** w kolumnie **wymagania dotyczące zasobu** wybierz łącze, aby dodać wymagane umiejętności dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="2fba4-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Łącze do wymagań](media/Resource-Management-image10.png)

3. <span data-ttu-id="2fba4-139">Na wyświetlonej stronie **Wymagania dotyczące zasobu** w siatce **umiejętności** wybierz wielokropek (**...**), a następnie wybierz opcję **Dodaj nową cechę wymagania**, aby dodać wymagane umiejętności dla swojego dewelopera.</span><span class="sxs-lookup"><span data-stu-id="2fba4-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Polecenie dodawania nowej cechy wymagania](media/Resource-Management-image11.png)

4. <span data-ttu-id="2fba4-141">W oknie dialogowym **szybkie tworzenie: cecha**, które zostanie wyświetlone, w polu **cecha** wybierz wymagane umiejętności.</span><span class="sxs-lookup"><span data-stu-id="2fba4-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="2fba4-142">Następnie w polu **Wartość klasyfikacji** wybierz poziom biegłości dla tej umiejętności.</span><span class="sxs-lookup"><span data-stu-id="2fba4-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="2fba4-143">Na koniec w polu **Wymaganie zasobu** należy ustawić wymagania dotyczące zasobów źródłowych z jednostek organizacyjnych lub nawet nazwanych zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="2fba4-144">Kiedy skończysz, wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-144">When you've finished, select **Save**.</span></span>

    ![Okno dialogowe Szybkie tworzenie: cecha wymagania](media/Resource-Management-image12.png)

5. <span data-ttu-id="2fba4-146">Na stronie **Zapotrzebowania zasobu** wybierz pozycję **Rezerwuj**, aby spełnić wymagania dotyczące zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Przycisk Rezerwuj na stronie zapotrzebowanie zasobu](media/Resource-Management-image13.png)

    <span data-ttu-id="2fba4-148">Można też wybrać zasób ogólny w siatce **wszystkie członków zespołu**, a następnie wybrać opcję **Rezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Przycisk Rezerwuj nad siatką wszystkich członków zespołu](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="2fba4-150">W tym przykładzie jest 40 wymaganych godzin, ale nie ma rzeczywistych zarezerwowanych godzin, ponieważ zasoby ogólne nie mają rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="2fba4-151">Oprócz tego nie ma przydzielonych godzin, ponieważ zasób ogólny został dodany bezpośrednio do zespołu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="2fba4-152">Nie został dodany przy użyciu przypisania zadania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="2fba4-153">Na stronie **asystent planowania** można filtrować dostępne zasoby według wymagań określonych w zapotrzebowaniu zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="2fba4-154">Zasoby są sortowane zgodnie z parametrami sortowania określonymi na tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Strona Asystent planowania](media/Resource-Management-image15.png)

    <span data-ttu-id="2fba4-156">Oto kilka często używanych filtrów:</span><span class="sxs-lookup"><span data-stu-id="2fba4-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="2fba4-157">**Charakterystyki wraz z oceną** — Filtruj według kwalifikacji, certyfikatów i innych cech zasobów, a także oceny biegłości.</span><span class="sxs-lookup"><span data-stu-id="2fba4-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="2fba4-158">**Role** — Filtruj według ról domyślnych przypisanych do zasobów, które można rezerwować.</span><span class="sxs-lookup"><span data-stu-id="2fba4-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="2fba4-159">**Jednostki organizacyjne** — Filtruj zasoby możliwe do zarezerwowania według jednostek organizacyjnych, do których są przypisane.</span><span class="sxs-lookup"><span data-stu-id="2fba4-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="2fba4-160">Jeśli wyniki pierwszego wyszukiwania wymagania nie są zadowalające, można zmienić kryteria filtrowania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="2fba4-161">Rozwiń okienko **widoku filtra** po lewej stronie, a następnie wybierz pozycję **Wyszukaj** w celu wyszukania dodatkowych zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Okienko widoku filtra](media/Resource-Management-image16.png)

7. <span data-ttu-id="2fba4-163">Aby zmienić sposób sortowania wyników, wybierz **Sortuj**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Polecenie Sortuj](media/Resource-Management-image17.png)

8. <span data-ttu-id="2fba4-165">Wybierz zasoby według zapotrzebowania określonego w zapotrzebowaniu, tak jak to pokazano u górnej części siatki.</span><span class="sxs-lookup"><span data-stu-id="2fba4-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="2fba4-166">Użytkownik może wyczyścić wybrane komórki siatki i zostawić otwartą dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="2fba4-167">Tylko jeden zasób jednocześnie może być zaznaczony jako zarezerwowany.</span><span class="sxs-lookup"><span data-stu-id="2fba4-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="2fba4-168">Wybierz **Rezerwuj**, aby zarezerwować wybrany zasób i pozostaw otwartą tablicę harmonogramu, aby mieć możliwość wybrania dodatkowych zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="2fba4-169">Możesz również wybrać opcję **Zarezerwuj i wyjdź**, aby zarezerwować wybrany zasób i zamknąć tablicę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Zasób do zarezerwowania](media/Resource-Management-image19.png)

    <span data-ttu-id="2fba4-171">Otrzymujesz powiadomienie dotyczące zarezerwowanych godzin.</span><span class="sxs-lookup"><span data-stu-id="2fba4-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="2fba4-172">Wskaźniki popytu pokazują, w jakim stopniu zapotrzebowanie na rezerwację zostało spełnione oraz jaka część pozostaje.</span><span class="sxs-lookup"><span data-stu-id="2fba4-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="2fba4-173">Użytkownik może również sprawdzić, jaka część dyspozycyjności wybranego zasobu jest zużywana.</span><span class="sxs-lookup"><span data-stu-id="2fba4-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="2fba4-174">Wybierz opcję **rozwiń**, aby wyświetlić więcej szczegółów dotyczących rezerwacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="2fba4-175">Powróć do widoku **wszystkich członków zespołu**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="2fba4-176">W siatce zauważ, że zasób ogólny został zastąpiony przez nazwany zasób, a 40 godzin zostało zarezerwowanych dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Zaktualizowanie siatki wszystkich członków zespołu](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="2fba4-178">Nie są wyświetlane przypisane godziny, ponieważ są one zarezerwowane bezpośrednio w zespole.</span><span class="sxs-lookup"><span data-stu-id="2fba4-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="2fba4-179">Nie zostały one zarezerwowane przy użyciu przypisania zadania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="2fba4-180">Przypisywanie zasobów ogólnych do zadań i generowanie wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="2fba4-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="2fba4-181">W PSA można tworzyć zadania i przypisywać im zasoby ogólne.</span><span class="sxs-lookup"><span data-stu-id="2fba4-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="2fba4-182">W ten sposób zapotrzebowanie zasobu może być reprezentowane przez symbole zastępcze podczas szacowania harmonogramu i kwot.</span><span class="sxs-lookup"><span data-stu-id="2fba4-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="2fba4-183">Następnie można wygenerować zapotrzebowania zasobów dla zasobów ogólnych i zrealizować je.</span><span class="sxs-lookup"><span data-stu-id="2fba4-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="2fba4-184">Na stronie **projekty** na karcie **harmonogram** wybierz pozycję **Dodaj**, aby utworzyć zadanie.</span><span class="sxs-lookup"><span data-stu-id="2fba4-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Utworzono nowe zadanie](media/Resource-Management-image21.png)

2. <span data-ttu-id="2fba4-186">W polu **zasoby** wybierz symbol **selektora zasobów**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="2fba4-187">Zostanie wyświetlony selektor zasobów zawierający listę istniejących członków zespołu danego projektu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Selektor zasobów](media/Resource-Management-image22.png)

3. <span data-ttu-id="2fba4-189">Wprowadź nazwę nowego zasobu ogólnego i wybierz pozycję **Utwórz.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Wprowadzona nazwa nowego zasobu ogólnego](media/Resource-Management-image23.png)

4. <span data-ttu-id="2fba4-191">W oknie dialogowym **szybkie tworzenie: członek zespołu projektu**, które zostanie wyświetlone, w polu **Rola** wybierz rolę dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="2fba4-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="2fba4-192">W polu **Jednostka zasobów** wybierz jednostkę organizacyjną dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="2fba4-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="2fba4-193">Następnie wybierz opcję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-193">Then select **Save**.</span></span>

    ![Zostanie wyświetlone okno dialogowe szybkie tworzenie: członek zespołu projektu.](media/Resource-Management-image24.png)

    <span data-ttu-id="2fba4-195">Ogólny członek zespołu teraz jest przypisany do zadania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-195">The generic team member is now assigned to the task.</span></span>

    ![Ogólny członek zespołu przypisany do zadania.](media/Resource-Management-image25.png)

    <span data-ttu-id="2fba4-197">Na karcie **zespół** zobaczysz nowego ogólnego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="2fba4-198">Zauważ, że ma on tylko przypisane godziny.</span><span class="sxs-lookup"><span data-stu-id="2fba4-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="2fba4-199">Te godziny to suma wszystkich zadań przydzielonych do ogólnego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="2fba4-200">Ogólny członek zespołu nie ma jeszcze wymaganych godzin ani wymagania zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Ogólny członek zespołu na karcie Zespół](media/Resource-Management-image26.png)

5. <span data-ttu-id="2fba4-202">Teraz możesz przypisać ogólnego członka zespołu do innych zadań za pomocą selektora zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Ogólny członek zespołu w selektorze zasobów](media/Resource-Management-image27.png)

    <span data-ttu-id="2fba4-204">Po zakończeniu przypisywania ogólnego zasobu do zadań można wygenerować zapotrzebowanie zasobu dla zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="2fba4-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="2fba4-205">Na karcie **zespół** wybierz zasób ogólny i wybierz opcję **Generuj zapotrzebowanie.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Polecenie Generuj wymaganie](media/Resource-Management-image28.png)

    <span data-ttu-id="2fba4-207">Kiedy zapotrzebowanie jest generowane, ogólny członek zespołu będzie dysponować godzinami i łączem dotyczącym wymagania zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Łącze wymaganie zasobu](media/Resource-Management-image29.png)

    <span data-ttu-id="2fba4-209">Po zarezerwowaniu nazwanego zasobu zasób ogólny jest usuwany z zespołu i zastępowany zasobem o nazwie.</span><span class="sxs-lookup"><span data-stu-id="2fba4-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Zasób ogólny zastąpiony zasobem nazwanym](media/Resource-Management-image30.png)

    <span data-ttu-id="2fba4-211">Na karcie **harmonogram** przydział zasobu ogólnego zostanie usunięty i zastąpiony nazwanym zasobem.</span><span class="sxs-lookup"><span data-stu-id="2fba4-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Przypisania zasobu ogólnego zastąpione zasobem o nazwie na karcie harmonogramu](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="2fba4-213">To zachowanie występuje tylko wtedy, gdy nazwany zasób jest w pełni zarezerwowany dla wymagania zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="2fba4-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="2fba4-214">Gdy zasób o nazwie częściowo zastępuje zapotrzebowanie na zasób ogólny lub wiele nazwanych zasobów zastępuje zapotrzebowanie na zasób ogólny, zasób ogólny pozostaje przydzielony do zadania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="2fba4-215">Na poniższym rysunku zaplanowano 80-godzinne zadanie z czasem trwania 5 dni (16 godzin dziennie) i został przypisany do zasobu ogólnego o nazwie **"funkcjonalny**".</span><span class="sxs-lookup"><span data-stu-id="2fba4-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-godzinne, 5-dniowe zadanie przypisane do zasobu ogólnego Funkcjonalny](media/Resource-Management-image32.png)

    <span data-ttu-id="2fba4-217">W przypadku generowania wymagania będzie ono obejmowało 80 godzin w ciągu 5 dni.</span><span class="sxs-lookup"><span data-stu-id="2fba4-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Wygenerowane zapotrzebowanie na 80 godzin w ciągu 5 dni](media/Resource-Management-image33.png)

    <span data-ttu-id="2fba4-219">Ponieważ dostępne zasoby pracują tylko po 8 godzin dziennie, do spełnienia zapotrzebowania potrzeba dwóch zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Drugi zasób](media/Resource-Management-image35.png)

    <span data-ttu-id="2fba4-221">Na karcie **zespół** zobaczysz, że zasób ogólny nie ma wymaganych godzin, ale przydzielone godziny wciąż są wyświetlane razem z dwoma nazwanymi zasobami, które zrealizują zapotrzebowanie.</span><span class="sxs-lookup"><span data-stu-id="2fba4-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dwa nazwane zasoby na karcie zespół](media/Resource-Management-image36.png)

    <span data-ttu-id="2fba4-223">Na karcie **Harmonogram** zasób ogólny pozostaje przydzielony do zadania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Zasoby ogólne na karcie Harmonogram](media/Resource-Management-image37.png)

<span data-ttu-id="2fba4-225">PSA nie przypisuje obu zasobów do zadania, ponieważ to zachowanie mogłoby spowodować wygenerowanie mniej przewidywalnego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="2fba4-226">W tym prostym przykładzie łatwo podzielić godziny równo na dwa zasoby.</span><span class="sxs-lookup"><span data-stu-id="2fba4-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="2fba4-227">Jednak w bardziej złożonych scenariuszach obejmujących wiele zadań i wiele zasobów, PSA musi wprowadzić założenia dotyczące alokacji rezerwacji odbieranych przez wiele zasobów na wiele zadań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="2fba4-228">W tym scenariuszu menedżer projektu jest odpowiedzialny za analizowanie wielu rezerwacji i przypisywanie ich według potrzeb.</span><span class="sxs-lookup"><span data-stu-id="2fba4-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="2fba4-229">Aby alokować rezerwacje, menedżer projektu przypisuje zadania z zasobów ogólnych do nazwanych zasobów, a następnie korzysta z widoku **uzgodnienie** w celu upewnienia się, że alokacja jest zgodna z rezerwacjami.</span><span class="sxs-lookup"><span data-stu-id="2fba4-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="2fba4-230">Edycja wymagania zasobu</span><span class="sxs-lookup"><span data-stu-id="2fba4-230">Edit a resource requirement</span></span>

<span data-ttu-id="2fba4-231">Po utworzeniu wymagania zasobu menedżer projektu lub menedżer zasobów może edytować szczegóły, aby uściślić kryteria wyszukiwania podczas korzystania z tablicy harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="2fba4-232">Aby edytować wymagania zasobu, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="2fba4-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="2fba4-233">Na stronie **projekty** na karcie **zespół** wybierz łącze do dowolnego wymagania zasobu ogólnego.</span><span class="sxs-lookup"><span data-stu-id="2fba4-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="2fba4-234">Na stronie **wymaganie zasobu**, która zostanie wyświetlona, można zaktualizować kilka atrybutów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="2fba4-235">Oto kilka przykładów:</span><span class="sxs-lookup"><span data-stu-id="2fba4-235">Here are some examples:</span></span>

    - <span data-ttu-id="2fba4-236">Nazwisko</span><span class="sxs-lookup"><span data-stu-id="2fba4-236">Name</span></span>
    - <span data-ttu-id="2fba4-237">Od daty</span><span class="sxs-lookup"><span data-stu-id="2fba4-237">From Date</span></span>
    - <span data-ttu-id="2fba4-238">Do daty</span><span class="sxs-lookup"><span data-stu-id="2fba4-238">To Date</span></span>
    - <span data-ttu-id="2fba4-239">Czas trwania</span><span class="sxs-lookup"><span data-stu-id="2fba4-239">Duration</span></span>
    - <span data-ttu-id="2fba4-240">Typ zasobu</span><span class="sxs-lookup"><span data-stu-id="2fba4-240">Resource Type</span></span>

<span data-ttu-id="2fba4-241">Na stronie **wymagania zasobu** menedżer projektu lub menedżer zasobów może również zdefiniować następujące informacje:</span><span class="sxs-lookup"><span data-stu-id="2fba4-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="2fba4-242">Umiejętności</span><span class="sxs-lookup"><span data-stu-id="2fba4-242">Skills</span></span>
- <span data-ttu-id="2fba4-243">Roles</span><span class="sxs-lookup"><span data-stu-id="2fba4-243">Roles</span></span>
- <span data-ttu-id="2fba4-244">Preferencje dotyczące zasobu</span><span class="sxs-lookup"><span data-stu-id="2fba4-244">Resource preferences</span></span>
- <span data-ttu-id="2fba4-245">Preferowane jednostki organizacyjne</span><span class="sxs-lookup"><span data-stu-id="2fba4-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="2fba4-246">Aktualizacja rezerwacji zasobów po ich zarezerwowaniu w projekcie</span><span class="sxs-lookup"><span data-stu-id="2fba4-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="2fba4-247">Po dodaniu ogólnego lub nazwanego zasobu do zespołu projektu można zmienić rezerwacje zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="2fba4-248">Na stronie **projekty** na karcie **zespół** wybierz opcję członka zespołu, a następnie wybierz **Obsługa rezerwacji**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Tablica harmonogramu otwarta dla wybranego członka zespołu](media/Resource-Management-image40.png)

    <span data-ttu-id="2fba4-250">Zostanie wyświetlona tablica harmonogramu, która pokazuje rezerwacje członków zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="2fba4-251">Rozwiń rekord członka zespołu w celu wyświetlenia godzin zarezerwowanych dla tego projektu i innych projektów, które zużywają dyspozycyjność członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="2fba4-252">Zaznacz i przeciągnij rezerwację, aby ją wydłużyć lub skrócić.</span><span class="sxs-lookup"><span data-stu-id="2fba4-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="2fba4-253">Zostanie otwarte okno dialogowe **Utwórz rezerwację zasobu**, które umożliwia dostosowanie rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Okno dialogowe Utwórz rezerwację zasobu](media/Resource-Management-image41.png)

3. <span data-ttu-id="2fba4-255">Kliknij prawym przyciskiem myszy rezerwację.</span><span class="sxs-lookup"><span data-stu-id="2fba4-255">Right-click the booking.</span></span> <span data-ttu-id="2fba4-256">Można użyć menu skrótów do wykonania następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="2fba4-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="2fba4-257">Zmiana stanu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-257">Change the booking status.</span></span>
    - <span data-ttu-id="2fba4-258">Edycja rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-258">Edit the booking.</span></span>
    - <span data-ttu-id="2fba4-259">Zastępowanie zasobu w zespole projektu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="2fba4-260">Zmiana stanu rezerwacji</span><span class="sxs-lookup"><span data-stu-id="2fba4-260">Change the booking status</span></span>

<span data-ttu-id="2fba4-261">Można zmienić domyślny lub niestandardowy stan rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-261">You can change any default or custom booking status.</span></span>

![Polecenie Zmień stan](media/Resource-Management-image42.png)

<span data-ttu-id="2fba4-263">W PSA dostępne są trzy stany:</span><span class="sxs-lookup"><span data-stu-id="2fba4-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="2fba4-264">**Anulowany** — ten stan powoduje anulowanie rezerwacji zasobu i zwolnienie dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="2fba4-265">**Rezerwacja ostateczna** — ten stan zużywa dyspozycyjność zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="2fba4-266">Rezerwacja zazwyczaj jest tym stanem po otworzeniu **Obsługa rezerwacji** w siatce **wszystkich członków zespołu** na stronie **projekty.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="2fba4-267">**Rezerwacja wstępna** — ten stan powoduje dodanie zasobu do zespołu, ale nie zużywa dyspozycyjności zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="2fba4-268">Oznacza to, że zasób został zarezerwowany do potencjalnej pracy, ale jest nadal dyspozycyjny, gdyby był potrzebny do wykonywania innych zadań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="2fba4-269">W widoku ogólnej dostępności zasobu rezerwacje wstępne mają inny stan niż rezerwacje ostateczne.</span><span class="sxs-lookup"><span data-stu-id="2fba4-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="2fba4-270">**Zaproponowano** — ten stan reprezentuje propozycję Menedżera zasobów lub projektu dotyczącą zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="2fba4-271">Propozycje nie zużywają dyspozycyjności zasobu, a zasób nie jest dodawany do zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="2fba4-272">Aby ostatecznie zarezerwować zasób w zespole, menedżer projektu musi zaakceptować propozycję.</span><span class="sxs-lookup"><span data-stu-id="2fba4-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="2fba4-273">Prześlij żądania zasobów</span><span class="sxs-lookup"><span data-stu-id="2fba4-273">Submit resource requests</span></span>

<span data-ttu-id="2fba4-274">Żądania zasobu są używane do zgłaszania popytu (wymagania zasobu), który musi zostać zrealizowany przez menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="2fba4-275">W przypadku zasobu ogólnego, który już znajduje się w zespole, można przesłać żądanie zasobu bezpośrednio.</span><span class="sxs-lookup"><span data-stu-id="2fba4-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="2fba4-276">Żądanie zasobu może być zrealizowane na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="2fba4-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="2fba4-277">Menedżer zasobów bezpośrednio wypełnia żądanie.</span><span class="sxs-lookup"><span data-stu-id="2fba4-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="2fba4-278">W tym przypadku zasób ogólny jest zastępowany rezerwacją ostateczną, która ma nazwany zasób.</span><span class="sxs-lookup"><span data-stu-id="2fba4-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="2fba4-279">Menedżer zasobów proponuje zasób menedżerowi projektu, a Menedżer projektu zatwierdza lub odrzuca zaproponowany zasób.</span><span class="sxs-lookup"><span data-stu-id="2fba4-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="2fba4-280">Bezpośrednie zrealizowanie żądań zasobów</span><span class="sxs-lookup"><span data-stu-id="2fba4-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="2fba4-281">Po wygenerowaniu wymagania zasobu Menedżer projektu może przesłać żądanie zasobu ogólnego, wybierając zasób, a następnie wybierając opcję **przesyłania żądania.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Przycisk PRZEŚLIJ ŻĄDANIE](media/Resource-Management-image45.png)

<span data-ttu-id="2fba4-283">Komentarze dotyczące zasobu można podać menedżerowi zasobów, który realizuje realizację żądania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="2fba4-284">Po przesłaniu żądania pole **stanu** dla członka zespołu zostanie zmienione na **przesłane.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Wprowadzanie opcjonalnych komentarzy](media/Resource-Management-image46.png)

<span data-ttu-id="2fba4-286">Gdy Menedżer zasobów realizuje żądanie, ogólny członek zespołu zostaje zastąpiony zasobem nazwanym w siatce **wszystkich członków zespołu**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Ogólny członek zespołu został zastąpiony przez nazwany zasób na siatce wszystkich członków zespołu](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="2fba4-288">Korzystanie z propozycji zasobów na potrzeby żądań zasobów</span><span class="sxs-lookup"><span data-stu-id="2fba4-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="2fba4-289">Zamiast bezpośredniego zarezerwowania zasobu dla żądania zasobu Menedżer zasobów może zaproponować zasób menedżerowi projektu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="2fba4-290">Menedżer zasobów może użyć tej opcji, jeśli dokładne dopasowania dotyczące zapotrzebowań nie są dostępne.</span><span class="sxs-lookup"><span data-stu-id="2fba4-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="2fba4-291">Gdy Menedżer zasobów proponuje dany zasób, Menedżer projektu widzi, że pole **stanu** dla ogólnego członka zespołu jest zmienione na **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Stan ogólnego członka zespołu zmieniono na Wymaga weryfikacji](media/Resource-Management-image48.png)

<span data-ttu-id="2fba4-293">Aby wyświetlić zaproponowany zasób wraz z wizualizacją skutków rezerwacji proponowanego zasobu, kliknij dwukrotnie członka zespołu o stanie **Wymaga weryfikacji**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="2fba4-294">Następnie wybierz kartę **proponowane zasoby**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-294">Then select the **Proposed Resources** tab.</span></span>

![Karta Proponowane zasoby](media/Resource-Management-image49.png)

<span data-ttu-id="2fba4-296">Zaznacz pole wyboru **Zaakceptuj wszystkie propozycje**, aby zaakceptować wszystkie proponowane zasoby, lub **Odrzuć wszystkie propozycje**, aby je odrzucić.</span><span class="sxs-lookup"><span data-stu-id="2fba4-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="2fba4-297">Jeśli zaakceptujesz zaproponowane zasoby, są one zarezerwowane w projekcie jako członkowie zespołu i zastępują zasoby ogólne.</span><span class="sxs-lookup"><span data-stu-id="2fba4-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="2fba4-298">Użytkownik musi akceptować lub odrzucać wszystkie proponowane zasoby.</span><span class="sxs-lookup"><span data-stu-id="2fba4-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="2fba4-299">Nie można częściowo zaakceptować lub odrzucić.</span><span class="sxs-lookup"><span data-stu-id="2fba4-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="2fba4-300">Zastępowanie zasobu w zespole projektu</span><span class="sxs-lookup"><span data-stu-id="2fba4-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="2fba4-301">Czasami Menedżer projektu musi zastąpić zarezerwowanego członka zespołu w projekcie.</span><span class="sxs-lookup"><span data-stu-id="2fba4-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="2fba4-302">Na stronie **projekty** na karcie **zespół** wybierz zasób, który wymaga zastąpienia, a następnie wybierz **Obsługa rezerwacji**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="2fba4-303">Rozwiń zasób, aby wyświetlić projekty, do których jest przypisany.</span><span class="sxs-lookup"><span data-stu-id="2fba4-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Zasób rozwinięty w celu pokazania przydzielonych projektów](media/Resource-Management-image50.png)

3. <span data-ttu-id="2fba4-305">Kliknij prawym przyciskiem myszy projekt, a następnie wybierz polecenie **Zastąp zasób**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="2fba4-306">Jeśli znasz zasób, którym chcesz zastąpić bieżący zasób, wybierz lub wpisz nazwę, a następnie wybierz opcję **ponowne przypisanie.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Określanie zastępstwa zasobu](media/Resource-Management-image51.png)

    <span data-ttu-id="2fba4-308">Można również wykonać następujące kroki, aby wyszukać zasób:</span><span class="sxs-lookup"><span data-stu-id="2fba4-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="2fba4-309">Wybierz pozycję **Znajdź zastępstwo**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-309">Select **Find Substitution**.</span></span>

        ![Wyszukiwanie zastępstwa zasobu](media/Resource-Management-image52.png)

        <span data-ttu-id="2fba4-311">Asystent harmonogramu zwraca listę dostępnych zastępców.</span><span class="sxs-lookup"><span data-stu-id="2fba4-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="2fba4-312">W Asystencie planowania można dalej filtrować dostępne zasoby, aby znaleźć odpowiednie zastępstwo.</span><span class="sxs-lookup"><span data-stu-id="2fba4-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Lista dostępnych zastępców](media/Resource-Management-image53.png)

    2. <span data-ttu-id="2fba4-314">Aby zastąpić zasób, wybierz żądany zasób, a następnie wybierz **Zastąp**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Wybrany zasób na zastępstwo](media/Resource-Management-image54.png)

    <span data-ttu-id="2fba4-316">Rezerwacje i przypisania są zastępowane nowym zasobem.</span><span class="sxs-lookup"><span data-stu-id="2fba4-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezerwacje i przypisania są zastępowane nowym zasobem](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="2fba4-318">Uzgadnianie rezerwacji i przypisań członka zespołu</span><span class="sxs-lookup"><span data-stu-id="2fba4-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="2fba4-319">Członkowie zespołu, rezerwacje i przydziały są luźno sprzężone.</span><span class="sxs-lookup"><span data-stu-id="2fba4-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="2fba4-320">Innymi słowy, zasoby mogą mieć przydziały, ale mogą nie mieć rezerwacji lub mogą mieć rezerwacje bez przypisań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="2fba4-321">Najlepiej, kiedy rezerwacje i przypisania w projekcie są zgodne, bo wtedy zasoby mają zatwierdzoną dyspozycyjność do wykonania przypisanych im zadań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="2fba4-322">Jednak rezerwacje mogą być oparte na dostępności, a czasy zadań mogą ulec zmianie w miarę kontynuowania projektu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="2fba4-323">Z tego względu swobodne powiązanie rezerwacji i przypisań zapewnia elastyczność.</span><span class="sxs-lookup"><span data-stu-id="2fba4-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="2fba4-324">PSA oferuje kartę **Uzgadnianie**, która pozwala menedżerom projektu uzgadniać rezerwacje członków zespołu i ich przypisania w zespołach projektów.</span><span class="sxs-lookup"><span data-stu-id="2fba4-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Karta Uzgadnianie](media/Resource-Management-image56.png)

<span data-ttu-id="2fba4-326">Na karcie **Uzgadnianie** są wyświetlane rezerwacje i przypisania na wszystkich poziomach szczegółowości, aż do poszczególnych zadań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="2fba4-327">W komórkach widać godziny, które reprezentują okresy od miesięcy aż po dni.</span><span class="sxs-lookup"><span data-stu-id="2fba4-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="2fba4-328">Na karcie przedstawiono również ogólną sumę netto projektu wraz z kolumną sumy.</span><span class="sxs-lookup"><span data-stu-id="2fba4-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="2fba4-329">Dla każdego zasobu karta oblicza różnicę między rezerwacjami członka zespołu w projekcie a zestawieniem zadań przypisanych temu członkowi zespołu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="2fba4-330">Najlepiej, aby różnica wynosiła 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2fba4-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="2fba4-331">Innymi słowy nie powinno być żadnej różnicy między rezerwacjami zasobu a jego przypisaniami zadań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="2fba4-332">Różnice są oznaczone kolorami i zacienione, aby zwrócić uwagę na dwa warunki:</span><span class="sxs-lookup"><span data-stu-id="2fba4-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="2fba4-333">**Niedobór rezerwacji** — niedobory rezerwacji powstają wtedy, gdy zasób ma więcej przypisań, niż rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="2fba4-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="2fba4-334">Ponieważ dyspozycyjność nie została zarezerwowana, menedżer projektu może naprawić tę sytuację poprzez rozszerzenie rezerwacji zasobu w sposób pokrywający niedobór.</span><span class="sxs-lookup"><span data-stu-id="2fba4-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="2fba4-335">**Nadmiarowe rezerwacje** — nadmierne rezerwacje występują, gdy zasób zarezerwowano do projektu, ale nie przypisano go do zadań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="2fba4-336">Ten warunek może być akceptowalny w przypadkach, gdy zasób został zarezerwowany w projekcie przed przydziałem zadania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="2fba4-337">Jednak w innych przypadkach być może nie jest planowane przypisanie zasobu do zadań.</span><span class="sxs-lookup"><span data-stu-id="2fba4-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="2fba4-338">Wtedy menedżer projektu powinien rozważyć anulowanie rezerwacji zasobu, tak aby jego dyspozycyjność można było wykorzystać w innym projekcie.</span><span class="sxs-lookup"><span data-stu-id="2fba4-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="2fba4-339">W niektórych przypadkach, kiedy oglądasz czas na wyższym poziomie niż poziom dnia (np. na poziomie miesiąca), może się pojawić różnica netto zasobu równa zero (innymi słowy, rezerwacje = przydziały).</span><span class="sxs-lookup"><span data-stu-id="2fba4-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="2fba4-340">Natomiast w poziomie Tydzień można zauważyć, że istnieją przypisania równe 0 (zero) godzin i rezerwacje 40 godzin w pierwszym tygodniu miesiąca oraz przypisania 40 godzin i rezerwacje równe 0 (zero) godzin w drugim tygodniu miesiąca.</span><span class="sxs-lookup"><span data-stu-id="2fba4-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="2fba4-341">Ogólnie rzecz biorąc, rezerwacje i przydziały są uzgadniane, ale różnią się od siebie między tygodniami.</span><span class="sxs-lookup"><span data-stu-id="2fba4-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="2fba4-342">Po wyświetleniu wyższych poziomów czasu na karcie **Uzgadnianie** widać wskaźnik komórki informujący o różnicach na niższych poziomach czasu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="2fba4-343">Dwukrotne kliknięcie komórki umożliwia powiększenie i wyświetlenie różnicy.</span><span class="sxs-lookup"><span data-stu-id="2fba4-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="2fba4-344">Następnie kliknij prawym przyciskiem myszy, aby pomniejszyć. Zaznaczając zasób, a następnie korzystając z przycisku **Następna różnica** z paska narzędzi siatki można przejść do następnej różnicy między rezerwacjami a przydziałami danego zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="2fba4-345">Następnie można skorzystać z opcji **Poprzednia różnica**, aby wrócić.</span><span class="sxs-lookup"><span data-stu-id="2fba4-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="2fba4-346">Istnieje również możliwość wyłączenia wskaźnika różnic i zachowania nawigacji w obszarze **ustawienia.**</span><span class="sxs-lookup"><span data-stu-id="2fba4-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Wskaźnik różnic](media/Resource-Management-image57.png)

<span data-ttu-id="2fba4-348">W sytuacjach, gdy istnieją przypisania zadań dla zasobu, ale nie ma rezerwacji, na stronie **Projekty** na karcie **Uzgadnianie** można wybrać niedobór rezerwacji, a następnie kliknąć przycisk **Rozszerz rezerwację**.</span><span class="sxs-lookup"><span data-stu-id="2fba4-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="2fba4-349">Zostanie wyświetlone okno dialogowe **Rozszerz rezerwację**, w którym przedstawiono rezerwację potrzebną do wyeliminowania problemu niedoboru zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fba4-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="2fba4-350">Okno to pokazuje również istniejące rezerwacje zasobu we wszystkich projektach lub innych encjach zaplanowania.</span><span class="sxs-lookup"><span data-stu-id="2fba4-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="2fba4-351">W przypadku wybrania opcji **OK**, aby utworzyć rezerwację zasobu niezależnie od dostępności tego zasobu, może wystąpić rezerwacja ponad dyspozycyjność.</span><span class="sxs-lookup"><span data-stu-id="2fba4-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Okno dialogowe Rozszerz rezerwację](media/Resource-Management-image58.png)

<span data-ttu-id="2fba4-353">Następnie menedżer projektu lub menedżer zasobów może za pomocą tablicy harmonogramu rozwiązać sytuację, w której zasób został zarezerwowany ponad jego dyspozycyjność.</span><span class="sxs-lookup"><span data-stu-id="2fba4-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]