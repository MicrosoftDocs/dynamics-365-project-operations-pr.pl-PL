---
title: Aktualizowanie Project Operations w środowisku Finance
description: Ten temat zawiera informacje o tym, jak zaktualizować Project Operations w środowisku Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011069"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="f47b9-103">Aktualizowanie Project Operations w środowisku Finance</span><span class="sxs-lookup"><span data-stu-id="f47b9-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="f47b9-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="f47b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="f47b9-105">Ten temat zawiera informacje o tym, jak zaktualizować Dynamics 365 Project Operations w środowisku Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f47b9-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="f47b9-106">Istnieją trzy procedury, które są wymagane do aktualizacji Project Operations do aktualizacji 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="f47b9-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="f47b9-107">Importowanie pakietu do projektu w wersji zapoznawczej</span><span class="sxs-lookup"><span data-stu-id="f47b9-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="f47b9-108">Stosowanie aktualizacji</span><span class="sxs-lookup"><span data-stu-id="f47b9-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="f47b9-109">Aktualizacja środowiska Dataverse</span><span class="sxs-lookup"><span data-stu-id="f47b9-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="f47b9-110">Importowanie pakietu do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="f47b9-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="f47b9-111">Zaloguj się do [Lifecycle Services (LCS)](https://lcs.dynamics.com/) jako właściciel projektu lub menedżer środowiska.</span><span class="sxs-lookup"><span data-stu-id="f47b9-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="f47b9-112">Z listy projektów wybierz swój projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="f47b9-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="f47b9-113">Na stronie **Projekt** w grupie **Środowiska** otwórz środowisko, które chcesz zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="f47b9-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="f47b9-114">Sprawdź, czy środowisko jest uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f47b9-114">Verify that the environment is running.</span></span> <span data-ttu-id="f47b9-115">Jeśli nie zostało uruchomione, uruchom środowisko.</span><span class="sxs-lookup"><span data-stu-id="f47b9-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="f47b9-116">W sekcji **Nowa wersja** w obszarze **Dostępne aktualizacje** wybierz pozycję **Wyświetl aktualizację** dla wersji 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="f47b9-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Wyświetl przycisk aktualizacji](media/view-update.png)

6. <span data-ttu-id="f47b9-118">Na stronie **Aktualizacje binarne** wybierz pozycję **Zapisz pakiet**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="f47b9-119">Na stronie **Przejrzyj i zapisz aktualizacje** wybierz pozycję **Zapisz pakiet**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="f47b9-120">W okienku **Zapisz pakiet do biblioteki elementów zawartości**, które się otworzy, wprowadź nazwę pakietu, a następnie wybierz pozycję **Zapisz pakiet**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="f47b9-121">Po zakończeniu zapisywania pakietu przez LCS przycisk **Gotowe** jest włączony.</span><span class="sxs-lookup"><span data-stu-id="f47b9-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="f47b9-122">Wybierz pozycję **Gotowe**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-122">Select **Done**.</span></span> <span data-ttu-id="f47b9-123">LCS zweryfikuje pakiet.</span><span class="sxs-lookup"><span data-stu-id="f47b9-123">LCS will verify the package.</span></span> <span data-ttu-id="f47b9-124">Weryfikacja może potrwać kilka minut lub do jednej godziny.</span><span class="sxs-lookup"><span data-stu-id="f47b9-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="f47b9-125">Zastosuj aktualizację pakietu</span><span class="sxs-lookup"><span data-stu-id="f47b9-125">Apply the package update</span></span>

1. <span data-ttu-id="f47b9-126">W LCS na stronie **Szczegóły środowiska** wybierz pozycję **Zachowaj** > **Zastosuj aktualizacje**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="f47b9-127">Z listy wybierz pakiet zapisany wcześniej, a następnie wybierz pozycję **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="f47b9-128">Wybierz pozycję **Tak**, aby potwierdzić, że chcesz wdrożyć pakiet.</span><span class="sxs-lookup"><span data-stu-id="f47b9-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Okno dialogowe Potwierdzanie wdrażania pakietu](media/confirm-package-deployment.png)

4. <span data-ttu-id="f47b9-130">Wybierz pozycję **Tak**, aby potwierdzić, że chcesz aktualizować aplikację.</span><span class="sxs-lookup"><span data-stu-id="f47b9-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Okno dialogowe Potwierdzanie aktualizacji aplikacji](media/confirm-application-update.png)

<span data-ttu-id="f47b9-132">Rozpocznie się aktualizacja wdrożenia i aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f47b9-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="f47b9-133">Na stronie **Szczegóły środowiska** w prawym górnym rogu stan środowiska zostanie zaktualizowany do **Serwisu**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="f47b9-134">Za około dwie godziny aktualizacja zostanie zakończona.</span><span class="sxs-lookup"><span data-stu-id="f47b9-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="f47b9-135">Informacje o wersji aplikacji zostaną zaktualizowane do **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, a stan środowiska zostanie zaktualizowany do **Wdrożonego**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="f47b9-136">Aktualizacja środowiska Dataverse</span><span class="sxs-lookup"><span data-stu-id="f47b9-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="f47b9-137">Zaloguj się w [Centrum administracyjnym Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="f47b9-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="f47b9-138">Na liście znajdź i otwórz środowisko używane do instalowania Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f47b9-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="f47b9-139">Na stronie **Środowiska** wybierz **Zasób** > **aplikacje Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="f47b9-140">Na liście znajdź pozycję **Microsoft Dynamics 365 Project Operations**, a następnie w kolumnie **Stan** wybierz opcję **Dostępna aktualizacja**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="f47b9-141">Zaznacz pole wyboru **Wyrażam zgodę na warunki usługi**, a następnie wybierz opcję **Aktualizuj**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="f47b9-142">Zostanie zainstalowana najnowsza wersja rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="f47b9-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="f47b9-143">Po zakończeniu instalacji zostanie zainstalowana wersja 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="f47b9-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="f47b9-144">Konfigurowanie nowych funkcji</span><span class="sxs-lookup"><span data-stu-id="f47b9-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="f47b9-145">Włącz mapowanie z podwójnym zapisem</span><span class="sxs-lookup"><span data-stu-id="f47b9-145">Enable dual-write mapping</span></span>

<span data-ttu-id="f47b9-146">Po zakończeniu aktualizacji w środowiskach Finance i Dataverse można włączyć wymagane mapowania z podwójnym zapisem.</span><span class="sxs-lookup"><span data-stu-id="f47b9-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="f47b9-147">Wykonaj następujące procedury, aby włączyć mapowanie z podwójnym zapisem.</span><span class="sxs-lookup"><span data-stu-id="f47b9-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="f47b9-148">Aktualizowanie ustawień zabezpieczeń w środowisku Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="f47b9-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="f47b9-149">Odśwież encje danych</span><span class="sxs-lookup"><span data-stu-id="f47b9-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="f47b9-150">Aktualizowanie i uruchamianie mapowań z podwójnym zapisem</span><span class="sxs-lookup"><span data-stu-id="f47b9-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="f47b9-151">Aktualizowanie ustawień zabezpieczeń w środowisku Dataverse</span><span class="sxs-lookup"><span data-stu-id="f47b9-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="f47b9-152">W ramach aktualizacji UR5 są wymagane następujące aktualizacje uprawnień zabezpieczeń encji.</span><span class="sxs-lookup"><span data-stu-id="f47b9-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="f47b9-153">W środowisku Dataverse wybierz opcję **Ustawienia** i w grupie **System** wybierz opcję **Zabezpieczenia**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Ustawienia środowiska usługi Dataverse](media/Picture21.png)

2. <span data-ttu-id="f47b9-155">Wybierz **Role zabezpieczeń**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="f47b9-156">Z listy ról wybierz **użytkownik aplikacji z podwójnym zapisem** i wybierz kartę **Encje niestandardowe**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="f47b9-157">Sprawdź, czy rola ma uprawnienia **Odczyt** i **Dołączanie do** dla:</span><span class="sxs-lookup"><span data-stu-id="f47b9-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="f47b9-158">**Typ kursu wymiany waluty**</span><span class="sxs-lookup"><span data-stu-id="f47b9-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="f47b9-159">**Plan kont**</span><span class="sxs-lookup"><span data-stu-id="f47b9-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="f47b9-160">**Kalendarz obrachunkowy**</span><span class="sxs-lookup"><span data-stu-id="f47b9-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="f47b9-161">**Księga**</span><span class="sxs-lookup"><span data-stu-id="f47b9-161">**Ledger**</span></span>

5. <span data-ttu-id="f47b9-162">Po rola zabezpieczeń należy wybrać pozycję **Ustawienia** > **Zabezpieczenia** > **Teams**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="f47b9-163">Sprawdź, czy do zespołu została zastosowana rola **użytkownika aplikacji z podwójnym zapisem**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="f47b9-164">Odświeżanie encji danych z aktualizacji</span><span class="sxs-lookup"><span data-stu-id="f47b9-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="f47b9-165">W środowisku Finance otwórz obszar roboczy **Zarządzania danymi**, a następnie otwórz stronę **parametrów Framework**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="f47b9-166">Na karcie **Ustawienia encji** wybierz opcję **Odśwież listę encji**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="f47b9-167">Wybierz opcję **Zamknij**, aby potwierdzić odświeżenie encji.</span><span class="sxs-lookup"><span data-stu-id="f47b9-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="f47b9-168">Ten proces zajmie około 20 minut.</span><span class="sxs-lookup"><span data-stu-id="f47b9-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="f47b9-169">Po zakończeniu odświeżania otrzymasz powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="f47b9-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="f47b9-170">Zaktualizuj mapowania z podwójnym zapisem</span><span class="sxs-lookup"><span data-stu-id="f47b9-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="f47b9-171">W obszarze roboczym **Zarządzania danymi** wybierz opcję **Podwójny zapis**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="f47b9-172">Wybierz opcję **Zastosuj rozwiązania**, wybierz oba rozwiązania z listy, a następnie wybierz opcję **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="f47b9-173">Na stronie **Podwójny zapis** wybierz poniższe mapowania tabeli, a następnie wybierz opcję **Zatrzymaj**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="f47b9-174">**Wartości rzeczywiste integracji Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="f47b9-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="f47b9-175">**Kategorie kosztów projektu integracji z Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="f47b9-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="f47b9-176">**Integracja Project Operations aktualizuje jednostkę eksportu kosztów projektu (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="f47b9-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="f47b9-177">Na stronie **Wersja mapowania tabeli** można zastosować nową wersję mapowania do każdej z trzech encji.</span><span class="sxs-lookup"><span data-stu-id="f47b9-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="f47b9-178">Na stronie **Podwójny zapis** wybierz opcję Uruchom, aby ponownie uruchomić mapowania.</span><span class="sxs-lookup"><span data-stu-id="f47b9-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="f47b9-179">Z listy map wybierz mapowanie **Księga (msdyn_ledgers)** ze wszystkimi wymaganiami wstępnymi i zaznacz pole wyboru **Synchronizacja początkowa**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="f47b9-180">W polu **Wzorzec dla synchronizacji początkowej** wybierz **aplikacje Finance and Operations**, a następnie wybierz opcję **Uruchom**.</span><span class="sxs-lookup"><span data-stu-id="f47b9-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synchronizacja mapowania księgi](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]