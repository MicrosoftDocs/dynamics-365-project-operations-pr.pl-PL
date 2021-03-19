---
title: Integracja klienta programu Microsoft Project
description: Planowanie i utrzymywanie harmonogramu projektu może być skomplikowane, więc kierownicy projektów muszą używać narzędzi, które pomagają im zarządzać tym zadaniem. Integracja z Microsoft Project Client zapewnia wsparcie dla otwierania i zarządzania strukturą podziału pracy w projekcie.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289337"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="117ed-104">Integracja klienta programu Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="117ed-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="117ed-105">Planowanie i utrzymywanie harmonogramu projektu może być skomplikowane, więc kierownicy projektów muszą używać narzędzi, które pomagają im zarządzać tym zadaniem.</span><span class="sxs-lookup"><span data-stu-id="117ed-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="117ed-106">Integracja z Microsoft Project Client zapewnia wsparcie dla otwierania i zarządzania strukturą podziału pracy w projekcie.</span><span class="sxs-lookup"><span data-stu-id="117ed-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="117ed-107">Kierownik projektu może opublikować wszystkie zmiany wprowadzone z powrotem w strukturze podziału prac projektu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="117ed-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="117ed-108">W przypadku korzystania z aktualizacji z lipca (wersja 10.0.4) należy zainstalować program KB 4054797 i 4055884.</span><span class="sxs-lookup"><span data-stu-id="117ed-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="117ed-109">Konfigurowanie dodatku Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="117ed-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="117ed-110">Aby umożliwić integrację z Microsoft Project Client, dodatek Microsoft Dynamics 365 musi być zainstalowany w aplikacji klienta Microsoft Project użytkownika.</span><span class="sxs-lookup"><span data-stu-id="117ed-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="117ed-111">W tym celu należy otworzyć **Obszar roboczy zarządzanie projektami**.</span><span class="sxs-lookup"><span data-stu-id="117ed-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="117ed-112">•   Kliknij opcję **Konfigurowanie dodatku klienta projektu**, korzystając z sekcji **Łącza** > **Ustawienia** w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="117ed-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="117ed-113">•   Kliknij przycisk **Otwórz**, a następnie kliknij opcję **Uruchom** po wyświetleniu monitu.</span><span class="sxs-lookup"><span data-stu-id="117ed-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="117ed-114">Otwórz i edytuj istniejącą roboczą strukturę podziału pracy w programie Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="117ed-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="117ed-115">Jeśli projekt w Dynamics 365 Finance ma już utworzoną strukturę podziału pracy, strukturę podziału pracy można otworzyć w aplikacji Microsoft Project Client, jeśli struktura podziału pracy ma status wersji roboczej.</span><span class="sxs-lookup"><span data-stu-id="117ed-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="117ed-116">Aby otworzyć ze strony **Projektu**, kliknij łącze **Otwórz w programie Microsoft Project** na karcie **Plan**. Tę stronę można również otworzyć z poziomu aplikacji Microsoft Project Client, klikając **Otwórz** na karcie **Microsoft Dynamics 365**. Wybierz **Firma** i **Projekt** z listy.</span><span class="sxs-lookup"><span data-stu-id="117ed-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="117ed-117">Jeśli używasz przeglądarki Internet Explorer jako przeglądarki, musisz kliknąć przycisk **Zapisz**, aby ręcznie otworzyć plik z lokalizacji, do której został pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="117ed-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="117ed-118">Lub kliknij przycisk **Zapisz i Otwórz**, aby otworzyć plik w programie Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="117ed-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="117ed-119">Nie zmieniaj nazwy pliku przy zapisywaniu.</span><span class="sxs-lookup"><span data-stu-id="117ed-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="117ed-120">Przed wprowadzeniem jakichkolwiek zmian w pliku przy użyciu Microsoft Project Client należy go zaewidencjonować. Kliknij pozycję **Wyewidencjonuj** na karcie **Microsoft Dynamics 365**. Uniemożliwi to innym użytkownikom edytowanie struktury podziału prac z poziomu finansów w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="117ed-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="117ed-121">Aby opublikować strukturę podziału pracy po zakończeniu edycji, kliknij pozycję **Zaewidencjonuj** na karcie **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="117ed-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="117ed-122">Jeśli zespół projektowy został już dodany do projektu w programie Finance, lista zasobów zostanie wypełniona członkami zespołu.</span><span class="sxs-lookup"><span data-stu-id="117ed-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="117ed-123">Jeśli zespół projektu nie został jeszcze dodany do projektu, można wybrać zasoby i zbudować zespół w programie Microsoft Project Client, klikając przycisk **Zasoby** na karcie **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="117ed-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="117ed-124">Następujące dane będą synchronizowane z powrotem do Finance w ramach procesu ewidencjonowania:</span><span class="sxs-lookup"><span data-stu-id="117ed-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="117ed-125">•   Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="117ed-125">•   Task name</span></span>

<span data-ttu-id="117ed-126">•   Data rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="117ed-126">•   Start date</span></span>

<span data-ttu-id="117ed-127">•   Data zakończenia</span><span class="sxs-lookup"><span data-stu-id="117ed-127">•   Finish date</span></span>

<span data-ttu-id="117ed-128">•   Elementy poprzedzające</span><span class="sxs-lookup"><span data-stu-id="117ed-128">•   Predecessors</span></span>

<span data-ttu-id="117ed-129">•   Nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="117ed-129">•   Resource names</span></span>

<span data-ttu-id="117ed-130">•   Kategoria</span><span class="sxs-lookup"><span data-stu-id="117ed-130">•   Category</span></span>

<span data-ttu-id="117ed-131">•   Kategoria zasobów</span><span class="sxs-lookup"><span data-stu-id="117ed-131">•   Resource category</span></span>

<span data-ttu-id="117ed-132">•   Godziny pracy</span><span class="sxs-lookup"><span data-stu-id="117ed-132">•   Work hours</span></span>

<span data-ttu-id="117ed-133">•   Notatki</span><span class="sxs-lookup"><span data-stu-id="117ed-133">•   Notes</span></span>

<span data-ttu-id="117ed-134">•   Priorytet</span><span class="sxs-lookup"><span data-stu-id="117ed-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="117ed-135">Dodanie innych kolumn do pliku klienta programu Microsoft Project spowoduje, że nie zostaną one zapisane w pliku i nie zostaną wyświetlone po ponownym otwarciu pliku.</span><span class="sxs-lookup"><span data-stu-id="117ed-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="117ed-136">Tworzenie struktury podziału pracy dla istniejącego projektu przy użyciu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="117ed-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="117ed-137">Aby utworzyć nową strukturę podziału pracy za pomocą Microsoft Project Client, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="117ed-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="117ed-138">Otwórz Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="117ed-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="117ed-139">Na karcie **Microsoft Dynamics 365** kliknij opcję **Opcje**.</span><span class="sxs-lookup"><span data-stu-id="117ed-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="117ed-140">Wybierz **Firma** dla projektu.</span><span class="sxs-lookup"><span data-stu-id="117ed-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="117ed-141">Wybierz **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="117ed-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="117ed-142">Kliknij pozycję **Zapoznaj się** na karcie **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="117ed-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="117ed-143">Gdy jest gotowy do opublikowania w Finance, kliknij opcję **Zaewidencjonuj** na karcie **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="117ed-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="117ed-144">Zastąp istniejącą strukturę podziału pracy dla istniejącego projektu przy użyciu programu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="117ed-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="117ed-145">Aby utworzyć nową strukturę podziału pracy przy użyciu programu Microsoft Project Client i zastąpić istniejącą strukturę podziału pracy dla istniejącego projektu, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="117ed-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="117ed-146">Otwórz Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="117ed-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="117ed-147">Utwórz harmonogram w programie Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="117ed-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="117ed-148">Na karcie **Microsoft Dynamics 365** kliknij przycisk **Zapisz zmiany** > **Zastąp istniejący projekt**.</span><span class="sxs-lookup"><span data-stu-id="117ed-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="117ed-149">Wybierz **Firma** dla projektu.</span><span class="sxs-lookup"><span data-stu-id="117ed-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="117ed-150">Wybierz **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="117ed-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="117ed-151">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="117ed-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="117ed-152">Tworzenie nowego projektu z poziomu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="117ed-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="117ed-153">Otwórz Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="117ed-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="117ed-154">Utwórz harmonogram w programie Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="117ed-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="117ed-155">Na karcie **Microsoft Dynamics 365** kliknij przycisk **Zapisz zmiany** > **Zapisz do nowego projektu**.</span><span class="sxs-lookup"><span data-stu-id="117ed-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="117ed-156">Wybierz **Firma** dla projektu.</span><span class="sxs-lookup"><span data-stu-id="117ed-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="117ed-157">W razie potrzeby wprowadź **Identyfikator projektu**.</span><span class="sxs-lookup"><span data-stu-id="117ed-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="117ed-158">Wprowadź **Nazwa projektu**.</span><span class="sxs-lookup"><span data-stu-id="117ed-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="117ed-159">Wybierz **Typ projektu**, **Grupę projektów** oraz **Identyfikator kontraktu projektu**.</span><span class="sxs-lookup"><span data-stu-id="117ed-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="117ed-160">Można również utworzyć nowy kontrakt dotyczący projektu, klikając opcję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="117ed-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="117ed-161">Wybierz **Kalendarz**, który ma być używany do ponownego wyszukania.</span><span class="sxs-lookup"><span data-stu-id="117ed-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="117ed-162">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="117ed-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]