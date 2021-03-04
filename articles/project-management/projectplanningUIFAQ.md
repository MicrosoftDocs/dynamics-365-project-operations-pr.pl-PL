---
title: Rozwiązywanie problemów z pracą w siatce Zadanie
description: Ten temat zawiera informacje na temat rozwiązywania problemów potrzebne podczas pracy w siatce Zadanie.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031550"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="2d7e8-103">Rozwiązywanie problemów z pracą w siatce Zadanie</span><span class="sxs-lookup"><span data-stu-id="2d7e8-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="2d7e8-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="2d7e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2d7e8-105">W tym temacie opisano, jak rozwiązać problemy, które mogą wystąpić podczas pracy z zarządzaniem kosztami.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="2d7e8-106">Włącz obsługę plików cookie</span><span class="sxs-lookup"><span data-stu-id="2d7e8-106">Enable cookies</span></span>

<span data-ttu-id="2d7e8-107">Project Operations wymaga włączenia plików cookie innych firm w celu renderowania struktury podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="2d7e8-108">Jeśli pliki cookie innych firm nie są włączone, zamiast zadań, po wybraniu karty **Zadania** na stronie **Projekt** zobaczysz pustą stronę.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Pusta karta w przypadku, gdy nie są włączone pliki cookie innych firm](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="2d7e8-110">Rozwiązanie</span><span class="sxs-lookup"><span data-stu-id="2d7e8-110">Workaround</span></span>
<span data-ttu-id="2d7e8-111">W przypadku przeglądarek Microsoft Edge lub Google Chrome poniższe procedury opisują sposób aktualizacji ustawień przeglądarki, aby włączyć pliki cookie innych firm.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="2d7e8-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2d7e8-112">Microsoft Edge</span></span>

1. <span data-ttu-id="2d7e8-113">Otwórz przeglądarkę Edge.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="2d7e8-114">W prawym górnym rogu wybierz pozycję **wielokropka** (...), a następnie pozycję **Ustawienia**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="2d7e8-115">W obszarze **Pliki cookie i uprawnienia witryny** wybierz pozycję **Pliki cookie i dane witryny**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="2d7e8-116">Wyłącz **Blokuj wszystkie pliki cookie innych firm**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="2d7e8-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="2d7e8-117">Google Chrome</span></span>

1. <span data-ttu-id="2d7e8-118">Otwórz przeglądarkę Chrome.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="2d7e8-119">W prawym górnym rogu zaznacz trzy pionowe kropki,, a następnie wybierz **Ustawienia**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="2d7e8-120">W obszarze **Prywatność i zabezpieczenia** wybierz pozycję **Pliki cookie i inne dane witryny**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="2d7e8-121">Wybierz **Zezwalaj na wszystkie pliki cookie**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d7e8-122">Jeśli zablokujesz pliki cookie innych firm, wszystkie pliki cookie i dane witryn z innych witryn zostaną zablokowane, nawet jeśli witryna jest dozwolona na liście wyjątków.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="2d7e8-123">Punkt końcowy systemu PEX</span><span class="sxs-lookup"><span data-stu-id="2d7e8-123">PEX Endpoint</span></span>

<span data-ttu-id="2d7e8-124">Project Operations wymaga, aby parametr projektu odwoływał się do punktu końcowego PEX.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="2d7e8-125">Ten punkt końcowy jest wymagany do komunikacji z usługą używaną do renderowania struktury podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="2d7e8-126">Jeśli parametr nie jest włączony, pojawi się błąd „Parametr projektu jest nieprawidłowy”.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="2d7e8-127">Rozwiązanie</span><span class="sxs-lookup"><span data-stu-id="2d7e8-127">Workaround</span></span>
 ![Pole PEX Endpoint w parametrze projektu](media/projectparameter.png)

1. <span data-ttu-id="2d7e8-129">Dodaj pole **punkt końcowy PEX** do strony **Parametry projektu**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="2d7e8-130">Zaktualizuj pole za pomocą następującej wartości: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="2d7e8-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="2d7e8-131">Usuń pole ze strony **Parametry projektu**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="2d7e8-132">Uprawnienia dotyczące projektu w sieci Web</span><span class="sxs-lookup"><span data-stu-id="2d7e8-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="2d7e8-133">Project Operations są związane z zewnętrzną usługą planowania.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="2d7e8-134">W usłudze jest wymagane przypisanie użytkownikowi kilku ról do odczytu i zapisu encji związanych z strukturą zabezpieczeń pracy.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="2d7e8-135">Te encje obejmują zadania projektu, przydziały zasobów i zależności zadań.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="2d7e8-136">Jeśli użytkownik nie może wyrenderować struktury podziału pracy po przejściu do karty **Zadania**, prawdopodobnie jest to spowodowane tym, że nie włączono programu Project for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="2d7e8-137">Użytkownik może otrzymać błąd roli zabezpieczeń lub błąd związany z odmową dostępu.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="2d7e8-138">Rozwiązanie</span><span class="sxs-lookup"><span data-stu-id="2d7e8-138">Workaround</span></span>

1. <span data-ttu-id="2d7e8-139">Przejdź do **Ustawienia > Zabezpieczenia > Użytkownicy > Użytkownicy aplikacji**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Czytnik aplikacji](media/applicationuser.jpg)
   
2. <span data-ttu-id="2d7e8-141">Kliknij dwukrotnie rekord użytkownika aplikacji, aby sprawdzić, czy:</span><span class="sxs-lookup"><span data-stu-id="2d7e8-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="2d7e8-142">Użytkownik ma dostęp do projektu.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-142">The user has access to the project.</span></span> <span data-ttu-id="2d7e8-143">Weryfikacja ta zwykle polega na upewnieniu się, że użytkownik ma rolę zabezpieczeń **Menedżer projektu**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="2d7e8-144">Użytkownik aplikacji Microsoft Project istnieje i jest poprawnie skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="2d7e8-145">Jeśli ten użytkownik nie istnieje, możesz utworzyć nowy rekord użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="2d7e8-146">Wybierz **Nowi użytkownicy**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-146">Select **New Users**.</span></span> <span data-ttu-id="2d7e8-147">Zmień formularz wprowadzania na **Użytkownik aplikacji**, a następnie dodaj **Identyfikator aplikacji**.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Dane użytkownika aplikacji](media/applicationuserdetails.jpg)

4. <span data-ttu-id="2d7e8-149">Sprawdź, czy użytkownikowi przypisano poprawną licencję i czy usługa jest włączona w szczegółach planu usług licencji.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="2d7e8-150">Sprawdź, czy użytkownik może otworzyć project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="2d7e8-151">Sprawdź za pomocą parametrów projektu, czy system wskazuje prawidłowy punkt końcowy projektu.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="2d7e8-152">Sprawdź, czy utworzono użytkownika aplikacji projektu.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="2d7e8-153">Zastosuj następujące role zabezpieczeń do użytkownika:</span><span class="sxs-lookup"><span data-stu-id="2d7e8-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="2d7e8-154">Użytkownik Dataverse</span><span class="sxs-lookup"><span data-stu-id="2d7e8-154">Dataverse User</span></span>
  - <span data-ttu-id="2d7e8-155">System Project Operations</span><span class="sxs-lookup"><span data-stu-id="2d7e8-155">Project Operations System</span></span>
  - <span data-ttu-id="2d7e8-156">System projektów</span><span class="sxs-lookup"><span data-stu-id="2d7e8-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="2d7e8-157">Błąd podczas aktualizacji struktury podziału pracy</span><span class="sxs-lookup"><span data-stu-id="2d7e8-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="2d7e8-158">Po wprowadzeniu co najmniej jednej aktualizacji struktury podziału pracy zmiany ostatecznie kończą się niepowodzeniem i nie są zapisywane.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="2d7e8-159">W siatce harmonogramu pojawia się błąd informujący, że „Nie można zapisać ostatniej wprowadzonej zmiany”.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="2d7e8-160">Rozwiązanie</span><span class="sxs-lookup"><span data-stu-id="2d7e8-160">Workaround</span></span>

1. <span data-ttu-id="2d7e8-161">Sprawdź, czy użytkownikowi przypisano poprawną licencję i czy usługa jest włączona w szczegółach planu usług licencji.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="2d7e8-162">Sprawdź, czy użytkownik może otworzyć project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="2d7e8-163">Sprawdź, czy system wskazuje prawidłowy punkt końcowy projektu.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="2d7e8-164">Sprawdź, czy utworzono użytkownika aplikacji Project.</span><span class="sxs-lookup"><span data-stu-id="2d7e8-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="2d7e8-165">Zastosuj następujące role zabezpieczeń do użytkownika:</span><span class="sxs-lookup"><span data-stu-id="2d7e8-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="2d7e8-166">Użytkownik Dataverse lub grupa użytkowników</span><span class="sxs-lookup"><span data-stu-id="2d7e8-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="2d7e8-167">System Project Operations</span><span class="sxs-lookup"><span data-stu-id="2d7e8-167">Project Operations System</span></span>
  - <span data-ttu-id="2d7e8-168">System projektów</span><span class="sxs-lookup"><span data-stu-id="2d7e8-168">Project System</span></span>
  - <span data-ttu-id="2d7e8-169">System podwójnego zapisu Project Operations (ta rola jest wymagana w przypadku wdrażania scenariusza dotyczącego zasobów/braku zapasów w ramach Project Operations).</span><span class="sxs-lookup"><span data-stu-id="2d7e8-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
