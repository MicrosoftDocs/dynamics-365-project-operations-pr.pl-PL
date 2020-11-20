---
title: Ustanowienie nowego środowiska
description: W tym temacie zamieszczono informacje dotyczące tworzenia nowego środowiska w Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121186"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="904d3-103">Ustanowienie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="904d3-103">Provision a new environment</span></span>

<span data-ttu-id="904d3-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="904d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="904d3-105">W tym temacie zamieszczono informacje dotyczące sposobu ustanawiania nowego środowiska Dynamics 365 Project Operations do obsługi zasobów i niemagazynowanych scenariuszy.</span><span class="sxs-lookup"><span data-stu-id="904d3-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="904d3-106">Włączanie zautomatyzowanego ustanawiania Project Operations w ramach projektu LCS</span><span class="sxs-lookup"><span data-stu-id="904d3-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="904d3-107">Wykonaj poniższe kroki, aby włączyć zautomatyzowany przepływ ustanawiania Project Operations w ramach LCS.</span><span class="sxs-lookup"><span data-stu-id="904d3-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="904d3-108">Przejdź do [LCS](https://lcs.dynamics.com/v2) i wybierz kafelek **Zarządzanie podglądem funkcji**.</span><span class="sxs-lookup"><span data-stu-id="904d3-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="904d3-109">Na liście **Wersji zapoznawczej funkcji** wybierz **Funkcja Project Operations** i wybierz **Włącz wersje zapoznawcze funkcji**, aby włączyć Project Operations.</span><span class="sxs-lookup"><span data-stu-id="904d3-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="904d3-110">Ten krok jest wykonywany tylko raz dla każdego projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="904d3-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="904d3-111">Obsługiwanie środowiska Project Operations</span><span class="sxs-lookup"><span data-stu-id="904d3-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="904d3-112">Otwórz nowe [środowisko pokazowe](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance lub [piaskownicę/wdrożenie środowiska produkcyjnego](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="904d3-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="904d3-113">Wykonaj kroki kreatora **Inicjowania obsługi środowiska**.</span><span class="sxs-lookup"><span data-stu-id="904d3-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="904d3-114">Upewnij się, że wybrana wersja aplikacji to 10.0.13 lub wyższa.</span><span class="sxs-lookup"><span data-stu-id="904d3-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="904d3-115">Aby zainicjować obsługę Project Operations, w obszarze **Ustawienia zaawansowane** wybierz opcję **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="904d3-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="904d3-116">Aby włączyć to **Ustawienie Common Data Service**, należy wybrać opcję **Tak** i wprowadzić informacje w wymaganych polach:</span><span class="sxs-lookup"><span data-stu-id="904d3-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="904d3-117">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="904d3-117">Name</span></span>
  - <span data-ttu-id="904d3-118">Region</span><span class="sxs-lookup"><span data-stu-id="904d3-118">Region</span></span>
  - <span data-ttu-id="904d3-119">Język</span><span class="sxs-lookup"><span data-stu-id="904d3-119">Language</span></span>
  - <span data-ttu-id="904d3-120">Waluta</span><span class="sxs-lookup"><span data-stu-id="904d3-120">Currency</span></span>
 
5. <span data-ttu-id="904d3-121">W polu **Szablon Common Data Service** wybierz **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="904d3-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="904d3-122">Wybierz typ środowiska dla swojego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="904d3-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="904d3-123">Wersja próbna oparta na subskrypcji umożliwia wdrożenie środowiska CDS przez 30 dni.</span><span class="sxs-lookup"><span data-stu-id="904d3-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Ustawienia wdrażania](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="904d3-125">Wybierz opcję **Zgoda**, aby wyrazić zgodę na potwierdzenie warunków świadczenia usługi, a następnie wybierz opcję **Gotowy**, aby powrócić do ustawień wdrażania.</span><span class="sxs-lookup"><span data-stu-id="904d3-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Zgoda na wdrożenia](./media/2DeploymentConsent.png)

7. <span data-ttu-id="904d3-127">Wykonaj pozostałe wymagane pola kreatora i potwierdź wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="904d3-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="904d3-128">Czas inicjowania obsługi środowiska jest różny w zależności od typu środowiska.</span><span class="sxs-lookup"><span data-stu-id="904d3-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="904d3-129">Inicjowanie obsługi może potrwać do sześciu godzin.</span><span class="sxs-lookup"><span data-stu-id="904d3-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="904d3-130">Po pomyślnym zakończeniu wdrożenia środowisko będzie widoczne jako **Wdrożone**.</span><span class="sxs-lookup"><span data-stu-id="904d3-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="904d3-131">Aby upewnić się, że środowisko zostało pomyślnie wdrożone, wybierz opcję **Logowanie** i zaloguj się do środowiska w celu potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="904d3-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Szczegóły środowiska ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="904d3-133">Stosowanie finansowych danych demonstracyjnych Finance w Project Operations (opcjonalny krok)</span><span class="sxs-lookup"><span data-stu-id="904d3-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="904d3-134">Umożliwia zastosowanie danych demonstracyjnych Finance w Project Operations do hostowanego w chmurze środowiska w wersji 10.0.13, jak to opisano w [tym artykule](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="904d3-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="904d3-135">Stosowanie aktualizacji środowiska Finance</span><span class="sxs-lookup"><span data-stu-id="904d3-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="904d3-136">Project Operations wymaga środowiska Finance korzystającego z aplikacji w wersji **10.0.13 (10.0.569.20009)** lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="904d3-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="904d3-137">W celu uzyskania tej wersji może być konieczne zastosowanie aktualizacji dotyczących jakości w środowisku Finance.</span><span class="sxs-lookup"><span data-stu-id="904d3-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="904d3-138">W programie LCS na stronie **Szczegóły środowiska** w sekcji **Dostępne aktualizacje** wybierz pozycję **Wyświetl aktualizacje**.</span><span class="sxs-lookup"><span data-stu-id="904d3-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Wyświetl aktualizacje](./media/5ViewUpdates.png)

2. <span data-ttu-id="904d3-140">Na stronie **Aktualizacje binarne** wybierz pozycję **Zapisz pakiet.**</span><span class="sxs-lookup"><span data-stu-id="904d3-140">On the **Binary updates** page, select **Save package.**</span></span>

![Zapisz pakiet](./media/6SavePackage.png)

3. <span data-ttu-id="904d3-142">Wybierz pozycje **Wybierz wszystko**, a następnie wybierz **Zapisz pakiet**.</span><span class="sxs-lookup"><span data-stu-id="904d3-142">Click **Select all** and then select **Save package**.</span></span>

![Przeglądanie i zapisywanie aktualizacji](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="904d3-144">Wprowadź nazwę i opis pakietu, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="904d3-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="904d3-145">W zależności od jakości połączenia internetowego, proces ten może potrwać dłużej.</span><span class="sxs-lookup"><span data-stu-id="904d3-145">Depending on the internet connection, this process might take some time.</span></span>

![Prześlij pakiet do biblioteki zasobów](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="904d3-147">Po zapisaniu pakietu wybierz opcję **Zrobione** i zapisz ten pakiet w bibliotece zasobów w projekcie programu LCS.</span><span class="sxs-lookup"><span data-stu-id="904d3-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="904d3-148">Zapisanie i sprawdzanie poprawności pakietu może zająć około 15 minut.</span><span class="sxs-lookup"><span data-stu-id="904d3-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="904d3-149">Aby zastosować aktualizację, przejdź na stronę **Szczegółów środowiska** w programie LCS i wybierz pozycję **Obsługa** > **Zastosuj aktualizacje**.</span><span class="sxs-lookup"><span data-stu-id="904d3-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Obsługa środowisk](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="904d3-151">Na liście aktualizacji zaznacz utworzony pakiet i wybierz przycisk **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="904d3-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Stosowanie aktualizacji](./media/10ApplyUpdates.png)

<span data-ttu-id="904d3-153">Obsługa środowiska zajmie trochę czasu.</span><span class="sxs-lookup"><span data-stu-id="904d3-153">Environment servicing will take some time.</span></span> <span data-ttu-id="904d3-154">Po zakończeniu środowisko powróci do stanu wdrożonego.</span><span class="sxs-lookup"><span data-stu-id="904d3-154">After it is complete, the environment will return to a deployed state.</span></span>

![Wdrożone środowisko](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="904d3-156">Ustanawianie połączenia podwójnego zapisu</span><span class="sxs-lookup"><span data-stu-id="904d3-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="904d3-157">W projekcie LCS przejdź na stronę **Szczegóły środowiska**.</span><span class="sxs-lookup"><span data-stu-id="904d3-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="904d3-158">W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji**.</span><span class="sxs-lookup"><span data-stu-id="904d3-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="904d3-159">Po zakończeniu tworzenia łącza wybierz ponownie opcję **Połącz z CDS dla aplikacji**.</span><span class="sxs-lookup"><span data-stu-id="904d3-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="904d3-160">Nastąpi przekierowanie do podwójnego zapisu w Finance.</span><span class="sxs-lookup"><span data-stu-id="904d3-160">You will be redirected to Dual Write in Finance.</span></span>

![Link do systemu CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="904d3-162">Wybierz opcję **Zastosuj rozwiązanie**, aby uzyskać dostęp do encji, które zostaną zamapowane na integrację.</span><span class="sxs-lookup"><span data-stu-id="904d3-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Zastosuj rozwiązania](./media/13ApplySolutions.png)

5. <span data-ttu-id="904d3-164">Zaznacz oba rozwiązania, **Mapowanie encji z podwójnym zapisem Dynamics 365 Finance and Operations** i **Mapowanie encji z podwójnym zapisem Dynamics 365 Project Operations**, a następnie kliknij przycisk **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="904d3-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potwierdzanie rozwiązań](./media/14ConfirmSolutions.png)

<span data-ttu-id="904d3-166">Po zastosowaniu rozwiązań do środowiska jest stosowana encja podwójnego zapisu.</span><span class="sxs-lookup"><span data-stu-id="904d3-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Stosowanie rozwiązań](./media/15ApplyingSolutions.png)

<span data-ttu-id="904d3-168">Po zastosowaniu encji wszystkie dostępne mapowania będą wyświetlane w środowisku.</span><span class="sxs-lookup"><span data-stu-id="904d3-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapy podwójnego zapisu](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="904d3-170">Odśwież encje danych po aktualizacji</span><span class="sxs-lookup"><span data-stu-id="904d3-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="904d3-171">W Finance przejdź do obszaru roboczego **Zarządzanie danymi**.</span><span class="sxs-lookup"><span data-stu-id="904d3-171">In Finance, go to the **Data management** workspace.</span></span>

![Obszar roboczy Zarządzanie danymi](./media/16DataManagement.png)

2. <span data-ttu-id="904d3-173">Wybierz kafelek **Parametry struktury**.</span><span class="sxs-lookup"><span data-stu-id="904d3-173">Select the **Framework parameters** tile.</span></span>

![Parametry struktury](./media/17FrameworkParameters.png)

3. <span data-ttu-id="904d3-175">Na stronie **Ustawienia encji** wybierz pozycję **Odśwież listę encji**.</span><span class="sxs-lookup"><span data-stu-id="904d3-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Odśwież listę encji](./media/18RefreshEntityList.png)

<span data-ttu-id="904d3-177">Odświeżenie zajmie około 20 minut.</span><span class="sxs-lookup"><span data-stu-id="904d3-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="904d3-178">Po jego zakończeniu otrzymasz alert.</span><span class="sxs-lookup"><span data-stu-id="904d3-178">You will receive an alert when it is complete.</span></span>

![Potwierdzenie odświeżenia](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="904d3-180">Uruchomienie map podwójnego zapisu Project Operations</span><span class="sxs-lookup"><span data-stu-id="904d3-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="904d3-181">W projekcie LCS przejdź na stronę **Szczegóły środowiska**.</span><span class="sxs-lookup"><span data-stu-id="904d3-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="904d3-182">W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji.**</span><span class="sxs-lookup"><span data-stu-id="904d3-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="904d3-183">Po wybraniu łącza nastąpi przekierowanie do listy encji w mapowaniach.</span><span class="sxs-lookup"><span data-stu-id="904d3-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="904d3-184">Uruchom mapowanie w sposób opisany w poniższej tabeli.</span><span class="sxs-lookup"><span data-stu-id="904d3-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="904d3-185">Upewnij się, że kolejność jest zgodna z tą na liście.</span><span class="sxs-lookup"><span data-stu-id="904d3-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="904d3-186">**Mapowanie encji**</span><span class="sxs-lookup"><span data-stu-id="904d3-186">**Entity Map**</span></span> | <span data-ttu-id="904d3-187">**Odśwież encje**</span><span class="sxs-lookup"><span data-stu-id="904d3-187">**Refresh entity**</span></span> | <span data-ttu-id="904d3-188">**Synchronizacja początkowa**</span><span class="sxs-lookup"><span data-stu-id="904d3-188">**Initial sync**</span></span> | <span data-ttu-id="904d3-189">**Wzorzec dla synchronizacji początkowej**</span><span class="sxs-lookup"><span data-stu-id="904d3-189">**Master for initial sync**</span></span> | <span data-ttu-id="904d3-190">**Uruchom wymagania wstępne**</span><span class="sxs-lookup"><span data-stu-id="904d3-190">**Run prerequisites**</span></span> | <span data-ttu-id="904d3-191">**Synchronizacja początkowa wymagań**</span><span class="sxs-lookup"><span data-stu-id="904d3-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="904d3-192">**Role zasobów projektu dla wszystkich firm (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="904d3-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="904d3-193">No</span><span class="sxs-lookup"><span data-stu-id="904d3-193">No</span></span> | <span data-ttu-id="904d3-194">Tak</span><span class="sxs-lookup"><span data-stu-id="904d3-194">Yes</span></span> | <span data-ttu-id="904d3-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="904d3-195">Common Data Service</span></span> | <span data-ttu-id="904d3-196">No</span><span class="sxs-lookup"><span data-stu-id="904d3-196">No</span></span> | <span data-ttu-id="904d3-197">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-197">N\A</span></span> |
| <span data-ttu-id="904d3-198">**Firmy (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="904d3-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="904d3-199">No</span><span class="sxs-lookup"><span data-stu-id="904d3-199">No</span></span> | <span data-ttu-id="904d3-200">Tak</span><span class="sxs-lookup"><span data-stu-id="904d3-200">Yes</span></span> | <span data-ttu-id="904d3-201">Aplikacje rozwiązania Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="904d3-201">Finance and Operations apps</span></span> | <span data-ttu-id="904d3-202">No</span><span class="sxs-lookup"><span data-stu-id="904d3-202">No</span></span> | <span data-ttu-id="904d3-203">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-203">N\A</span></span> |
| <span data-ttu-id="904d3-204">**Wartości rzeczywiste integracji Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="904d3-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="904d3-205">No</span><span class="sxs-lookup"><span data-stu-id="904d3-205">No</span></span> | <span data-ttu-id="904d3-206">No</span><span class="sxs-lookup"><span data-stu-id="904d3-206">No</span></span> | <span data-ttu-id="904d3-207">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-207">N\A</span></span> | <span data-ttu-id="904d3-208">Tak</span><span class="sxs-lookup"><span data-stu-id="904d3-208">Yes</span></span> | <span data-ttu-id="904d3-209">No</span><span class="sxs-lookup"><span data-stu-id="904d3-209">No</span></span> |
| <span data-ttu-id="904d3-210">**Pozycje kontraktu w projekcie (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="904d3-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="904d3-211">No</span><span class="sxs-lookup"><span data-stu-id="904d3-211">No</span></span> | <span data-ttu-id="904d3-212">No</span><span class="sxs-lookup"><span data-stu-id="904d3-212">No</span></span> | <span data-ttu-id="904d3-213">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-213">N\A</span></span> | <span data-ttu-id="904d3-214">No</span><span class="sxs-lookup"><span data-stu-id="904d3-214">No</span></span> | <span data-ttu-id="904d3-215">No</span><span class="sxs-lookup"><span data-stu-id="904d3-215">No</span></span> |
| <span data-ttu-id="904d3-216">**Encja integrująca dla transakcji projektu relacje (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="904d3-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="904d3-217">No</span><span class="sxs-lookup"><span data-stu-id="904d3-217">No</span></span> | <span data-ttu-id="904d3-218">No</span><span class="sxs-lookup"><span data-stu-id="904d3-218">No</span></span> | <span data-ttu-id="904d3-219">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-219">N\A</span></span> | <span data-ttu-id="904d3-220">No</span><span class="sxs-lookup"><span data-stu-id="904d3-220">No</span></span> | <span data-ttu-id="904d3-221">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-221">N\A</span></span> |
| <span data-ttu-id="904d3-222">**Punkty kontrolne pozycji kontraktu w integracji Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="904d3-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="904d3-223">No</span><span class="sxs-lookup"><span data-stu-id="904d3-223">No</span></span> | <span data-ttu-id="904d3-224">No</span><span class="sxs-lookup"><span data-stu-id="904d3-224">No</span></span> | <span data-ttu-id="904d3-225">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-225">N\A</span></span> | <span data-ttu-id="904d3-226">No</span><span class="sxs-lookup"><span data-stu-id="904d3-226">No</span></span> | <span data-ttu-id="904d3-227">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-227">N\A</span></span> |
| <span data-ttu-id="904d3-228">**Encja integracji Project Operations na potrzeby oszacowania kosztów (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="904d3-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="904d3-229">No</span><span class="sxs-lookup"><span data-stu-id="904d3-229">No</span></span> | <span data-ttu-id="904d3-230">No</span><span class="sxs-lookup"><span data-stu-id="904d3-230">No</span></span> | <span data-ttu-id="904d3-231">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-231">N\A</span></span> | <span data-ttu-id="904d3-232">No</span><span class="sxs-lookup"><span data-stu-id="904d3-232">No</span></span> | <span data-ttu-id="904d3-233">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-233">N\A</span></span> |
| <span data-ttu-id="904d3-234">**Encja integracji kategorii wydatków projektowych Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="904d3-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="904d3-235">No</span><span class="sxs-lookup"><span data-stu-id="904d3-235">No</span></span> | <span data-ttu-id="904d3-236">No</span><span class="sxs-lookup"><span data-stu-id="904d3-236">No</span></span> | <span data-ttu-id="904d3-237">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-237">N\A</span></span> | <span data-ttu-id="904d3-238">No</span><span class="sxs-lookup"><span data-stu-id="904d3-238">No</span></span> | <span data-ttu-id="904d3-239">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-239">N\A</span></span> |
| <span data-ttu-id="904d3-240">**Encja integracji wydatków projektowych Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="904d3-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="904d3-241">Tak</span><span class="sxs-lookup"><span data-stu-id="904d3-241">Yes</span></span> | <span data-ttu-id="904d3-242">No</span><span class="sxs-lookup"><span data-stu-id="904d3-242">No</span></span> | <span data-ttu-id="904d3-243">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-243">N\A</span></span> | <span data-ttu-id="904d3-244">No</span><span class="sxs-lookup"><span data-stu-id="904d3-244">No</span></span> | <span data-ttu-id="904d3-245">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-245">N\A</span></span> |
| <span data-ttu-id="904d3-246">**Encja integracji Project Operations na potrzeby oszacowania godzinowego (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="904d3-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="904d3-247">Tak</span><span class="sxs-lookup"><span data-stu-id="904d3-247">Yes</span></span> | <span data-ttu-id="904d3-248">No</span><span class="sxs-lookup"><span data-stu-id="904d3-248">No</span></span> | <span data-ttu-id="904d3-249">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-249">N\A</span></span> | <span data-ttu-id="904d3-250">No</span><span class="sxs-lookup"><span data-stu-id="904d3-250">No</span></span> | <span data-ttu-id="904d3-251">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="904d3-251">N\A</span></span> |


4. <span data-ttu-id="904d3-252">Aby odświeżyć encję, wybierz nazwę mapowania, a następnie wybierz opcję **Odśwież encje**.</span><span class="sxs-lookup"><span data-stu-id="904d3-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Odśwież mapowanie](./media/20RefreshMapping.png)

5. <span data-ttu-id="904d3-254">Po odświeżeniu uruchom mapowanie.</span><span class="sxs-lookup"><span data-stu-id="904d3-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="904d3-255">Przed włączeniem następnego mapowania należy sprawdzić, czy mapowanie w tabeli jest w stanie **Działającym**.</span><span class="sxs-lookup"><span data-stu-id="904d3-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="904d3-256">Uruchamianie mapowania z większą liczbą wstępnie wymaganych programów może zająć dużo czasu.</span><span class="sxs-lookup"><span data-stu-id="904d3-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="904d3-257">Aby uruchomić mapowanie z wymaganiami wstępnymi, włącz przełącznik **Pokaż mapowania encji pokrewnych**.</span><span class="sxs-lookup"><span data-stu-id="904d3-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="904d3-258">Jeśli tabela wskazuje , że **Wymagana wstępna synchronizacja** ma stan **Nie** sprawdź, czy flaga **Wstępna synchronizacja** jest **wyłączona** we wszystkich mapowaniach wymagań wstępnych, zanim zostanie ono uruchomione.</span><span class="sxs-lookup"><span data-stu-id="904d3-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Uruchom mapowanie](./media/21RunMap.png)

6. <span data-ttu-id="904d3-260">Sprawdź poprawność wszystkich mapowań powiązanych z projektem.</span><span class="sxs-lookup"><span data-stu-id="904d3-260">Validate all project related maps are in the running state.</span></span>

![Wszystkie mapowania uruchomione](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="904d3-262">Stosowanie danych konfiguracyjnych w usłudze CDS do aplikacji Project Operations (opcjonalne)</span><span class="sxs-lookup"><span data-stu-id="904d3-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="904d3-263">Jeśli dane demonstracyjne zostały zastosowane do środowiska Finance, zobacz [Konfigurowanie i stosowanie danych konfiguracyjnych w Common Data Service dla Project Operations](resource-apply-pro-setup-config-data.md) w celu zastosowania danych demonstracyjnych w środowisku CDS.</span><span class="sxs-lookup"><span data-stu-id="904d3-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="904d3-264">Środowisko Project Operations jest teraz obsługiwane i konfigurowane.</span><span class="sxs-lookup"><span data-stu-id="904d3-264">Your Project Operations environment is now provisioned and configured.</span></span> 
