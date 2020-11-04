---
title: Użyj dodatku Project Service, aby zaplanować pracę w programie Microsoft Project | MicrosoftDocs
description: W tym temacie zamieszczono informacje dotyczące sposobu dodawania, konfigurowania i używania dodatku programu Microsoft Project dla programu Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082142"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="46e3c-103">Użyj dodatku Project Service Automation do planowania pracy w programie Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="46e3c-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="46e3c-104">ułatwia planowanie i oszacowywanie projektów.</span><span class="sxs-lookup"><span data-stu-id="46e3c-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="46e3c-105">Pracę można zdefiniować tak, aby koszty, wysiłek i wartość sprzedaży były jasne w momencie przedstawiania ostatecznej propozycji.</span><span class="sxs-lookup"><span data-stu-id="46e3c-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="46e3c-106">Teraz możesz zainstalować [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i przeprowadzać planowanie w znanym środowisku [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="46e3c-107">Użyj zaawansowanych funkcji planowania i zarządzania [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], , a następnie zaktualizuj swój plan projektu w Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="46e3c-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="46e3c-108">Aby używać funkcji zarządzania dokumentami programu SharePoint do przechowywania plików programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dla projektów programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], administrator programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] będzie musiał włączyć zarządzanie dokumentami.</span><span class="sxs-lookup"><span data-stu-id="46e3c-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="46e3c-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] jest zgodny tylko z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="46e3c-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="46e3c-110">Pobierz i zainstaluj dodatek</span><span class="sxs-lookup"><span data-stu-id="46e3c-110">Download and install the add-in</span></span>  
 <span data-ttu-id="46e3c-111">Przygotuj swoje dane do logowania w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="46e3c-112">Informacje te będą Ci potrzebne, aby połączyć [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="46e3c-113">Korzystając z Centrum Pobierania można pobrać dodatek dla używanej wersji programu Project Service — [wer. 2.X](https://go.microsoft.com/fwlink/?linkid=828268) lub [wer. 3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="46e3c-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="46e3c-114">Kliknij łącze pobierania.</span><span class="sxs-lookup"><span data-stu-id="46e3c-114">Click the download link.</span></span>  

3.  <span data-ttu-id="46e3c-115">Po zakończeniu pobierania kliknij **Tak** , aby zainstalować dodatek.</span><span class="sxs-lookup"><span data-stu-id="46e3c-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="46e3c-116">Skonfiguruj dodatek</span><span class="sxs-lookup"><span data-stu-id="46e3c-116">Configure the add-in</span></span>  

1. <span data-ttu-id="46e3c-117">Otwórz [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i kliknij kartę **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="46e3c-118">Kliknij **Połącz**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="46e3c-119">Wprowadź informacje logowania, a następnie kliknij **Zaloguj się**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="46e3c-120">Teraz możesz rozpocząć korzystanie z dodatku.</span><span class="sxs-lookup"><span data-stu-id="46e3c-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="46e3c-121">Odczytać z szablonu</span><span class="sxs-lookup"><span data-stu-id="46e3c-121">Read from a template</span></span>  
 <span data-ttu-id="46e3c-122">Odczytaj z szablonu, który utworzyłeś w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i skopiowałeś do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], aby rozpocząć planowanie projektów.</span><span class="sxs-lookup"><span data-stu-id="46e3c-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="46e3c-123">[Utwórz szablon projektu (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="46e3c-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="46e3c-124">W karcie **Project Service** kliknij **Odczytaj** > **Szablon projektu Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="46e3c-125">Wybierz szablon projektu z listy, a następnie kliknij **Otwórz**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="46e3c-126">Domyślnie zadania kopiowane z szablonu do Projektu są ustawiane jako ręcznie zaplanowane.</span><span class="sxs-lookup"><span data-stu-id="46e3c-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="46e3c-127">Przypisz role [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] do zasobów projektu</span><span class="sxs-lookup"><span data-stu-id="46e3c-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="46e3c-128">Otwórz projekt, a następnie kliknij wstążkę **Zadanie**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="46e3c-129">Kliknij menu **Wykres Gantta** , a następnie wybierz **Arkusz zasobów**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="46e3c-130">Na karcie Arkusz zasobów kliknij menu rozwijane **Rola usługi Project Service Automation** i wybierz rolę usługi Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="46e3c-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="46e3c-131">Zaopatrz projekt w zasoby</span><span class="sxs-lookup"><span data-stu-id="46e3c-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="46e3c-132">Na karcie Project Service zaznacz wiersz i kliknij **Znajdź zasoby**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="46e3c-133">Na ekranie **Zarezerwuj zasoby** wybierz zasób, którego chcesz użyć dla projektu.</span><span class="sxs-lookup"><span data-stu-id="46e3c-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="46e3c-134">Kliknij **Zarezerwuj** , a następnie kliknij **OK**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="46e3c-135">Opublikuj projekt</span><span class="sxs-lookup"><span data-stu-id="46e3c-135">Publish your project</span></span>  
<span data-ttu-id="46e3c-136">Po zakończeniu planowania projektu, następnym krokiem jest importowanie i publikowanie projektu w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="46e3c-137">Projektu zostanie zaimportowany do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="46e3c-138">Zastosowano proces generowania cen i zespołu.</span><span class="sxs-lookup"><span data-stu-id="46e3c-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="46e3c-139">Otwórz projekt w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aby zobaczyć, że zespół, oszacowania projektu i struktura podziału pracy zostały wygenerowane.</span><span class="sxs-lookup"><span data-stu-id="46e3c-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="46e3c-140">W poniższej tabeli pokazano, gdzie można znaleźć wyniki:</span><span class="sxs-lookup"><span data-stu-id="46e3c-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="46e3c-141">**Wykres Gantt**</span><span class="sxs-lookup"><span data-stu-id="46e3c-141">**Gantt Chart**</span></span>   | <span data-ttu-id="46e3c-142">Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Struktura podziału pracy**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="46e3c-143">**Arkusz zasobów**</span><span class="sxs-lookup"><span data-stu-id="46e3c-143">**Resource Sheet**</span></span> |   <span data-ttu-id="46e3c-144">Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Członkowie zespołu projektu**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="46e3c-145">**Użyj użycia**</span><span class="sxs-lookup"><span data-stu-id="46e3c-145">**Use Usage**</span></span>    |    <span data-ttu-id="46e3c-146">Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Szacowania projektów**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="46e3c-147">**Aby zaimportować i opublikować projekt**</span><span class="sxs-lookup"><span data-stu-id="46e3c-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="46e3c-148">W karcie **Project Service** kliknij **Opublikuj** > **Nowy projekt Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="46e3c-149">W oknie dialogowym **Publikuj w nowym projekcie w Project Service** wprowadź **Nazwa projektu** i wybierz **Klient**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="46e3c-150">Opcjonalnie zaznacz **Połącz plan projektu z usługą Project Service Automation** , aby połączyć plik projektu z usługą Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="46e3c-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="46e3c-151">Kliknij przycisk **Publikuj**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-151">Click **Publish**.</span></span>  

   <span data-ttu-id="46e3c-152">Łączenie pliku Projekt z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sprawia, że plik Projekt staje się wzorcem i ustawia strukturę podziału pracy w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="46e3c-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="46e3c-153">Aby wprowadzić zmiany do planu projektu, należy sporządzić je w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i opublikować jako aktualizacje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="46e3c-154">Edytuj projekt, który został importowany</span><span class="sxs-lookup"><span data-stu-id="46e3c-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="46e3c-155">Aby wprowadzić zmiany do planu projektu, który został zaimportowany do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], masz dwie opcje:</span><span class="sxs-lookup"><span data-stu-id="46e3c-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="46e3c-156">Otwórz plik główny i edytuj go w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="46e3c-157">Odłącz plik i edytuj go bezpośrednio w Project Service.</span><span class="sxs-lookup"><span data-stu-id="46e3c-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="46e3c-158">Domyślnie, projekt, który został przekazany z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] jest zablokowany i może być edytowany tylko w programie Project.</span><span class="sxs-lookup"><span data-stu-id="46e3c-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="46e3c-159">Aby edytować plik w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], pliku musi być odłączony.</span><span class="sxs-lookup"><span data-stu-id="46e3c-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="46e3c-160">Edytuj w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="46e3c-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="46e3c-161">Z menu głównego, kliknij **Project Service** > **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="46e3c-162">Z listy projektów otwórz ten, który został utworzony w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="46e3c-163">Kliknij **Otwórz w MS Project** ze Wstążki.</span><span class="sxs-lookup"><span data-stu-id="46e3c-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="46e3c-164">Otworzy to połączony plik główny w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="46e3c-165">Odłącz plik i edytuj go w Usłudze [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="46e3c-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="46e3c-166">Z menu głównego, kliknij **Project Service** > **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="46e3c-167">Z listy projektów otwórz ten, który został utworzony w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="46e3c-168">Kliknij **Odłącz od MS Project** ze wstążki.</span><span class="sxs-lookup"><span data-stu-id="46e3c-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="46e3c-169">Przekazywanie pliku programu Project do programu SharePoint lub usługi Office Groups</span><span class="sxs-lookup"><span data-stu-id="46e3c-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="46e3c-170">Możesz przesłać plik programu Project do programu SharePoint i znaleźć go w sekcji Dokumenty związane dla Twojego projektu programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="46e3c-171">Administrator musi skonfigurować zarządzanie dokumentami programu SharePoint i włączyć je dla encji Project.</span><span class="sxs-lookup"><span data-stu-id="46e3c-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="46e3c-172">Możesz również przesłać plik Projekt do [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jeśli masz skonfigurowane grupy Office.</span><span class="sxs-lookup"><span data-stu-id="46e3c-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="46e3c-173">Przekazywanie pliku do programu SharePoint</span><span class="sxs-lookup"><span data-stu-id="46e3c-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="46e3c-174">Z menu głównego, kliknij **Project Service** > **Przekaż**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="46e3c-175">Wybierz **Do dokumentów projektu usługi Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="46e3c-176">W oknie dialogowym **Włącz Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , wybierz **Tak** lub **Nie**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="46e3c-177">Po kliknięciu **Tak** będziesz w stanie wybrać przycisk **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** w Project Service Automation, uruchomić [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] oraz załadować plik programu Project z biblioteki dokumentów SharePoint.</span><span class="sxs-lookup"><span data-stu-id="46e3c-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="46e3c-178">Po kliknięciu **Nie** łącze dla przycisku **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nie będzie działać.</span><span class="sxs-lookup"><span data-stu-id="46e3c-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="46e3c-179">Plik [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] można znaleźć w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenty** dla danego projektu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="46e3c-180">Przekaż plik dla grup usługi Office</span><span class="sxs-lookup"><span data-stu-id="46e3c-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="46e3c-181">Z menu głównego, kliknij **Project Service** > **Przekaż**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="46e3c-182">Wybierz **Do dokumentów projektu usługi Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="46e3c-183">W oknie dialogowym **Włącz Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , wybierz **Tak** lub **Nie**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="46e3c-184">Po kliknięciu **Tak** będziesz w stanie wybrać przycisk **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** w Project Service Automation, uruchomić [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] oraz załadować plik programu Project z biblioteki dokumentów SharePoint.</span><span class="sxs-lookup"><span data-stu-id="46e3c-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="46e3c-185">Po kliknięciu **Nie** łącze dla przycisku **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nie będzie działać.</span><span class="sxs-lookup"><span data-stu-id="46e3c-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="46e3c-186">Plik [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] można znaleźć w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenty** dla danego projektu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="46e3c-187">Opublikuj projekt jako szablon</span><span class="sxs-lookup"><span data-stu-id="46e3c-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="46e3c-188">Można zapisać projekt i użyć go ponownie, zapisując go jako szablon projektu w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="46e3c-189">Szablony projektów to nadające się do wielokrotnego użytku plany projektów w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="46e3c-190">[Utwórz szablon projektu (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="46e3c-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="46e3c-191">W karcie **Project Service** kliknij **Opublikuj** > **Nowy szablon usługi Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="46e3c-192">W oknie dialogowym **Publikuj w nowym projekcie w szablonie Project Service** wprowadź **Nazwa szablonu projektu**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="46e3c-193">Opcjonalnie zaznacz **Połącz plan projektu z usługą Project Service Automation** , aby połączyć plik programu Project z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="46e3c-194">Kliknij przycisk **Publikuj**.</span><span class="sxs-lookup"><span data-stu-id="46e3c-194">Click **Publish**.</span></span>  

<span data-ttu-id="46e3c-195">Łączenie pliku Projekt z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sprawia, że plik Projekt staje się wzorcem i ustawia strukturę podziału pracy w szablonie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="46e3c-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="46e3c-196">Aby wprowadzić zmiany do planu projektu, należy sporządzić je w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i opublikować jako aktualizacje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="46e3c-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="46e3c-197">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="46e3c-197">See Also</span></span>  
 [<span data-ttu-id="46e3c-198">Przewodnik menedżera projektu</span><span class="sxs-lookup"><span data-stu-id="46e3c-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
