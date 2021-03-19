---
title: Mobilny obszar roboczy wprowadzania czasu projektu
description: Ten temat zawiera informacje o mobilnym obszarze roboczym Wpis czasu projektu. Ten obszar roboczy umożliwia użytkownikom wejście do projektu i zaoszczędzenie czasu przy użyciu urządzenia mobilnego.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eae471cf42f02e64844a4682cc8ed02cbb14c34
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288887"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="d5393-104">Mobilny obszar roboczy wprowadzania czasu projektu</span><span class="sxs-lookup"><span data-stu-id="d5393-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5393-105">Ten temat zawiera informacje o mobilnym obszarze roboczym **Wpis czasu projektu**.</span><span class="sxs-lookup"><span data-stu-id="d5393-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="d5393-106">Ten obszar roboczy umożliwia użytkownikom wejście do projektu i zaoszczędzenie czasu przy użyciu urządzenia mobilnego.</span><span class="sxs-lookup"><span data-stu-id="d5393-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="d5393-107">Ten mobilny obszar roboczy jest przeznaczony do użytku z aplikacją mobilną Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="d5393-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="d5393-108">Omówienie</span><span class="sxs-lookup"><span data-stu-id="d5393-108">Overview</span></span>
<span data-ttu-id="d5393-109">W ramach codziennej pracy zasoby projektów zwykle są na terenie lub podróżują.</span><span class="sxs-lookup"><span data-stu-id="d5393-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="d5393-110">Mobilny obszar roboczy **Wpis czasu projektu** umożliwia użytkownikom wprowadzanie czasu do rozliczenia lub nierozliczenia w stosunku do projektu na wybranym urządzeniu mobilnym.</span><span class="sxs-lookup"><span data-stu-id="d5393-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="d5393-111">Zasoby projektu mogą więc rejestrować wpisy czasu w dowolnym czasie i z dowolnego miejsca.</span><span class="sxs-lookup"><span data-stu-id="d5393-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="d5393-112">Mogą również wyświetlać wpisy godzin, które już zostały zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="d5393-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="d5393-113">W szczególności w obszarze roboczym **Wpis czasu projektu** użytkownicy mogą wykonywać następujące zadania:</span><span class="sxs-lookup"><span data-stu-id="d5393-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="d5393-114">W przypadku każdej wybranej daty wprowadź liczbę godzin poświęconego na wykonanie określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="d5393-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="d5393-115">Wyszukaj według nazwy projektu lub klienta w celu wyszukania projektu i wprowadzenia czasu na nie.</span><span class="sxs-lookup"><span data-stu-id="d5393-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="d5393-116">Określ kategorię i działanie na czas spędzony przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d5393-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="d5393-117">Umożliwia rejestrowanie czasu jako faktury lub opłaty niepodlegającego rozliczaniu w projekcie.</span><span class="sxs-lookup"><span data-stu-id="d5393-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="d5393-118">Opcjonalnie wprowadź komentarze zewnętrzne lub wewnętrzne.</span><span class="sxs-lookup"><span data-stu-id="d5393-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d5393-119">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="d5393-119">Prerequisites</span></span>
<span data-ttu-id="d5393-120">Te wymagania są różne, zależnie od wersji Microsoft Dynamics 365, która została wdrożona w danej organizacji.</span><span class="sxs-lookup"><span data-stu-id="d5393-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="d5393-121">Wymagania wstępne dotyczące korzystania z Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d5393-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="d5393-122">Jeśli w organizacji wdrożono rozwiązanie Finance, administrator systemu musi opublikować mobilny obszar roboczy **Wprowadzanie czasu projektu**.</span><span class="sxs-lookup"><span data-stu-id="d5393-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="d5393-123">Aby uzyskać instrukcje, zobacz [Publikowanie przestrzeni roboczej dla urządzeń przenośnych](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="d5393-123">For instructions, see [Publish a mobile workspace](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="d5393-124">Wymagania wstępne, jeśli używasz wersji 1611 z aktualizacją platformy 3 lub nowszą</span><span class="sxs-lookup"><span data-stu-id="d5393-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="d5393-125">Jeśli w organizacji wdrożono wersję 1611 z aktualizacją platformy 3 lub nowszą, administrator systemu musi spełnić następujące wymagania wstępne.</span><span class="sxs-lookup"><span data-stu-id="d5393-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d5393-126">Warunek wstępny</span><span class="sxs-lookup"><span data-stu-id="d5393-126">Prerequisite</span></span></th>
<th><span data-ttu-id="d5393-127">Rola</span><span class="sxs-lookup"><span data-stu-id="d5393-127">Role</span></span></th>
<th><span data-ttu-id="d5393-128">Opis</span><span class="sxs-lookup"><span data-stu-id="d5393-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="d5393-129">Implementowanie 4018050 KB.</span><span class="sxs-lookup"><span data-stu-id="d5393-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="d5393-130">Administrator systemu</span><span class="sxs-lookup"><span data-stu-id="d5393-130">System administrator</span></span></td>
<td><span data-ttu-id="d5393-131">KB 4018050 to aktualizacja X ++ lub poprawka metadanych, która zawiera mobilny obszar roboczy <strong>Wpis czasu projektu</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5393-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="d5393-132">Aby zaimplementować KB 4018050, administrator systemu musi wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="d5393-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="d5393-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Pobierz poprawkę metadanych z Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="d5393-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="d5393-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Zainstaluj poprawkę metadanych</a>.</span><span class="sxs-lookup"><span data-stu-id="d5393-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="d5393-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Utwórz pakiet wdrożeniowy</a> zawierający <strong>ApplicationSuite</strong> i <strong>ProjectMobile</strong>, a następnie przekaż pakiet wdrożeniowy na LCS.</span><span class="sxs-lookup"><span data-stu-id="d5393-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="d5393-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Zastosowanie pakietu, który ma zostać wdrożony</a>.</span><span class="sxs-lookup"><span data-stu-id="d5393-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5393-137">Opublikuj mobilny obszar roboczy <strong>Wpis czasu projektu</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5393-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="d5393-138">Administrator systemu</span><span class="sxs-lookup"><span data-stu-id="d5393-138">System administrator</span></span></td>
<td><span data-ttu-id="d5393-139">Zobacz <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publikowanie przestrzeni roboczej dla urządzeń przenośnych</a>.</span><span class="sxs-lookup"><span data-stu-id="d5393-139">See <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d5393-140">Pobierz i zainstaluj aplikację mobilną</span><span class="sxs-lookup"><span data-stu-id="d5393-140">Download and install the mobile app</span></span>

<span data-ttu-id="d5393-141">Pobierz i zainstaluj aplikację mobilną Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="d5393-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="d5393-142">Na telefony Android</span><span class="sxs-lookup"><span data-stu-id="d5393-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d5393-143">Dla telefonów iPhone</span><span class="sxs-lookup"><span data-stu-id="d5393-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d5393-144">Zaloguj się do aplikacji mobilnej</span><span class="sxs-lookup"><span data-stu-id="d5393-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="d5393-145">Uruchom aplikację na swoim urządzeniu mobilnym.</span><span class="sxs-lookup"><span data-stu-id="d5393-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d5393-146">Wprowadź swój adres URL Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d5393-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d5393-147">Po pierwszym zalogowaniu się jest wyświetlany monit o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="d5393-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d5393-148">Wprowadź poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="d5393-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="d5393-149">Po zalogowaniu się zostaną wyświetlone dostępne obszary robocze dla firmy.</span><span class="sxs-lookup"><span data-stu-id="d5393-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d5393-150">Należy pamiętać, że jeśli system Administrator opublikuje nowy obszar roboczy później, konieczne będzie odświeżenie listy obszarów roboczych urządzeń przenośnych.</span><span class="sxs-lookup"><span data-stu-id="d5393-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="d5393-151">[![Przeciągnij, aby odświeżyć](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d5393-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="d5393-152">Wprowadź czas za pomocą mobilnego obszaru roboczego Wpis czasu projektu</span><span class="sxs-lookup"><span data-stu-id="d5393-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="d5393-153">Na urządzeniu przenośnym wybierz obszar roboczy **Wpisu czasu projektu**.</span><span class="sxs-lookup"><span data-stu-id="d5393-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="d5393-154">Wybierz **Wpis czasu**.</span><span class="sxs-lookup"><span data-stu-id="d5393-154">Select **Time entry**.</span></span> <span data-ttu-id="d5393-155">Zostaną wyświetlone daty w kalendarzu dla bieżącego tygodnia.</span><span class="sxs-lookup"><span data-stu-id="d5393-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="d5393-156">W przypadku wybranej daty wybierz **Akcje** &gt; **Nowy wpis**.</span><span class="sxs-lookup"><span data-stu-id="d5393-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="d5393-157">Wprowadź liczbę godzin do nagrania.</span><span class="sxs-lookup"><span data-stu-id="d5393-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="d5393-158">Wybierz projekt dla wpisu czasu.</span><span class="sxs-lookup"><span data-stu-id="d5393-158">Select the project for the time entry.</span></span> <span data-ttu-id="d5393-159">Lista zawiera projekty, które są ładowane do aplikacji do użytku w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="d5393-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="d5393-160">Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę.</span><span class="sxs-lookup"><span data-stu-id="d5393-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="d5393-161">Aby uzyskać więcej informacji, zobacz [Platforma mobilna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="d5393-161">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="d5393-162">Jeśli projekt nie znajduje się na liście, wybierz pozycję **Wyszukaj**.</span><span class="sxs-lookup"><span data-stu-id="d5393-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="d5393-163">Wyszukaj według nazwy lub przejdź do wyszukiwania według nazwy projektu lub klienta.</span><span class="sxs-lookup"><span data-stu-id="d5393-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="d5393-164">Wybierz kategorię.</span><span class="sxs-lookup"><span data-stu-id="d5393-164">Select a category.</span></span> <span data-ttu-id="d5393-165">Lista zawiera kategorie, które są ładowane do aplikacji do użytku w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="d5393-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="d5393-166">Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę.</span><span class="sxs-lookup"><span data-stu-id="d5393-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="d5393-167">Aby uzyskać więcej informacji, zobacz [Platforma mobilna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="d5393-167">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="d5393-168">Jeśli kategoria nie znajduje się na liście, wybierz pozycję **Wyszukaj**.</span><span class="sxs-lookup"><span data-stu-id="d5393-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="d5393-169">Wyszukaj według kategorii lub przejdź do wyszukiwania według nazwy kategorii.</span><span class="sxs-lookup"><span data-stu-id="d5393-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="d5393-170">Wybierz działanie.</span><span class="sxs-lookup"><span data-stu-id="d5393-170">Select an activity.</span></span> <span data-ttu-id="d5393-171">Lista zawiera działania, które są ładowane do aplikacji do użytku w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="d5393-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="d5393-172">Domyślnie ładowanych jest 50 elementów, ale programista może zmienić tę liczbę.</span><span class="sxs-lookup"><span data-stu-id="d5393-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="d5393-173">Aby uzyskać więcej informacji, zobacz [Platforma mobilna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="d5393-173">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="d5393-174">Jeśli działanie nie znajduje się na liście, wybierz pozycję **Wyszukaj**.</span><span class="sxs-lookup"><span data-stu-id="d5393-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="d5393-175">Wyszukaj według numeru działania lub przejdź do wyszukiwania według przeznaczenia.</span><span class="sxs-lookup"><span data-stu-id="d5393-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="d5393-176">Wybierz właściwość wiersza.</span><span class="sxs-lookup"><span data-stu-id="d5393-176">Select the line property.</span></span>
12. <span data-ttu-id="d5393-177">Opcjonalnie: wprowadź wszelkie komentarze zewnętrzne i wewnętrzne.</span><span class="sxs-lookup"><span data-stu-id="d5393-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="d5393-178">Wybierz **Gotowe**.</span><span class="sxs-lookup"><span data-stu-id="d5393-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]