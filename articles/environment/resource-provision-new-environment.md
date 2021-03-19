---
title: Ustanowienie nowego środowiska
description: W tym temacie zamieszczono informacje dotyczące tworzenia nowego środowiska w Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 50e623d3716c9dd03ce34ec293ba57b5d966d39e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276901"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="5d0b4-103">Ustanowienie nowego środowiska</span><span class="sxs-lookup"><span data-stu-id="5d0b4-103">Provision a new environment</span></span>

<span data-ttu-id="5d0b4-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="5d0b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5d0b4-105">Ten temat zawiera informacje o sposobach ustanawiania nowego środowiska aplikacji Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/braku zapasów.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="5d0b4-106">Włączanie zautomatyzowanego ustanawiania Project Operations w ramach projektu LCS</span><span class="sxs-lookup"><span data-stu-id="5d0b4-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="5d0b4-107">Wykonaj poniższe kroki, aby włączyć zautomatyzowany przepływ ustanawiania Project Operations w ramach LCS.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="5d0b4-108">Przejdź do [LCS](https://lcs.dynamics.com/v2) i wybierz kafelek **Zarządzanie podglądem funkcji**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="5d0b4-109">Na liście **Wersji zapoznawczej funkcji** wybierz **Funkcja Project Operations** i wybierz **Włącz wersje zapoznawcze funkcji**, aby włączyć Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="5d0b4-110">Ten krok jest wykonywany tylko raz dla każdego projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="5d0b4-111">Obsługiwanie środowiska Project Operations</span><span class="sxs-lookup"><span data-stu-id="5d0b4-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="5d0b4-112">Otwórz nowe [środowisko pokazowe](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance lub [piaskownicę/wdrożenie środowiska produkcyjnego](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="5d0b4-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="5d0b4-113">Wykonaj kroki kreatora **Inicjowania obsługi środowiska**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="5d0b4-114">Upewnij się, że wybrana wersja aplikacji to 10.0.13 lub wyższa.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="5d0b4-115">Aby zainicjować obsługę Project Operations, w obszarze **Ustawienia zaawansowane** wybierz opcję **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="5d0b4-116">Aby włączyć to **Ustawienie Common Data Service**, należy wybrać opcję **Tak** i wprowadzić informacje w wymaganych polach:</span><span class="sxs-lookup"><span data-stu-id="5d0b4-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="5d0b4-117">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="5d0b4-117">Name</span></span>
  - <span data-ttu-id="5d0b4-118">Region</span><span class="sxs-lookup"><span data-stu-id="5d0b4-118">Region</span></span>
  - <span data-ttu-id="5d0b4-119">Język</span><span class="sxs-lookup"><span data-stu-id="5d0b4-119">Language</span></span>
  - <span data-ttu-id="5d0b4-120">Waluta</span><span class="sxs-lookup"><span data-stu-id="5d0b4-120">Currency</span></span>
 
5. <span data-ttu-id="5d0b4-121">W polu **Szablon Common Data Service** wybierz **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="5d0b4-122">Wybierz typ środowiska dla swojego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="5d0b4-123">Wersja próbna oparta na subskrypcji umożliwia wdrożenie środowiska CDS przez 30 dni.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Ustawienia wdrażania](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="5d0b4-125">Wybierz opcję **Zgoda**, aby wyrazić zgodę na potwierdzenie warunków świadczenia usługi, a następnie wybierz opcję **Gotowy**, aby powrócić do ustawień wdrażania.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Zgoda na wdrożenia](./media/2DeploymentConsent.png)

7. <span data-ttu-id="5d0b4-127">Opcjonalnie — zastosuj dane demonstracyjne do środowiska.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="5d0b4-128">Przejdź do **Ustawienia zaawansowane**, wybierz pozycję **Dostosuj konfigurację bazy danych SQL** i ustaw opcję **Określ zestaw danych dla bazy danych aplikacji** na **Demo**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="5d0b4-129">Wykonaj pozostałe wymagane pola kreatora i potwierdź wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="5d0b4-130">Czas udostępnienia środowiska różni się w zależności od typu środowiska.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="5d0b4-131">Inicjowanie obsługi może potrwać do sześciu godzin.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="5d0b4-132">Po pomyślnym zakończeniu wdrożenia środowisko będzie widoczne jako **Wdrożone**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="5d0b4-133">Aby potwierdzić pomyślne wdrożenie środowiska, wybierz pozycję **Zaloguj się** i zaloguj się do środowiska, aby potwierdzić.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Szczegóły środowiska ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="5d0b4-135">Stosowanie aktualizacji środowiska Finance</span><span class="sxs-lookup"><span data-stu-id="5d0b4-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="5d0b4-136">Project Operations wymaga środowiska Finance korzystającego z aplikacji w wersji **10.0.13 (10.0.569.20009)** lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="5d0b4-137">W celu uzyskania tej wersji może być konieczne zastosowanie aktualizacji dotyczących jakości w środowisku Finance.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="5d0b4-138">W programie LCS na stronie **Szczegóły środowiska** w sekcji **Dostępne aktualizacje** wybierz pozycję **Wyświetl aktualizacje**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Wyświetl aktualizacje](./media/5ViewUpdates.png)

2. <span data-ttu-id="5d0b4-140">Na stronie **Aktualizacje binarne** wybierz pozycję **Zapisz pakiet.**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-140">On the **Binary updates** page, select **Save package.**</span></span>

![Zapisz pakiet](./media/6SavePackage.png)

3. <span data-ttu-id="5d0b4-142">Wybierz pozycje **Wybierz wszystko**, a następnie wybierz **Zapisz pakiet**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-142">Click **Select all** and then select **Save package**.</span></span>

![Przeglądanie i zapisywanie aktualizacji](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="5d0b4-144">Wprowadź nazwę i opis pakietu, a następnie wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="5d0b4-145">W zależności od jakości połączenia internetowego, proces ten może potrwać dłużej.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-145">Depending on the internet connection, this process might take some time.</span></span>

![Prześlij pakiet do biblioteki zasobów](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="5d0b4-147">Po zapisaniu pakietu wybierz opcję **Zrobione** i zapisz ten pakiet w bibliotece zasobów w projekcie programu LCS.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="5d0b4-148">Zapisanie i sprawdzanie poprawności pakietu może zająć około 15 minut.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="5d0b4-149">Aby zastosować aktualizację, przejdź na stronę **Szczegółów środowiska** w programie LCS i wybierz pozycję **Obsługa** > **Zastosuj aktualizacje**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Obsługa środowisk](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="5d0b4-151">Na liście aktualizacji zaznacz utworzony pakiet i wybierz przycisk **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Stosowanie aktualizacji](./media/10ApplyUpdates.png)

<span data-ttu-id="5d0b4-153">Obsługa środowiska zajmie trochę czasu.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-153">Environment servicing will take some time.</span></span> <span data-ttu-id="5d0b4-154">Po zakończeniu środowisko powróci do stanu wdrożonego.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-154">After it is complete, the environment will return to a deployed state.</span></span>

![Wdrożone środowisko](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="5d0b4-156">Ustanawianie połączenia podwójnego zapisu</span><span class="sxs-lookup"><span data-stu-id="5d0b4-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="5d0b4-157">W projekcie LCS przejdź na stronę **Szczegóły środowiska**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5d0b4-158">W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="5d0b4-159">Po zakończeniu tworzenia łącza wybierz ponownie opcję **Połącz z CDS dla aplikacji**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="5d0b4-160">Nastąpi przekierowanie do podwójnego zapisu w Finance.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-160">You will be redirected to Dual Write in Finance.</span></span>

![Link do systemu CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="5d0b4-162">Wybierz opcję **Zastosuj rozwiązanie**, aby uzyskać dostęp do encji, które zostaną zamapowane na integrację.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Zastosuj rozwiązania](./media/13ApplySolutions.png)

5. <span data-ttu-id="5d0b4-164">Wybierz obydwa rozwiązania, **Dynamics 365 Finance and Operations — mapa encji podwójnego zapisu** i **Dynamics 365 Project Operations — mapa encji podwójnego zapisu**, a następnie wybierz przycisk **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potwierdzanie rozwiązań](./media/14ConfirmSolutions.png)

<span data-ttu-id="5d0b4-166">Po zastosowaniu rozwiązań do środowiska jest stosowana encja podwójnego zapisu.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Stosowanie rozwiązań](./media/15ApplyingSolutions.png)

<span data-ttu-id="5d0b4-168">Po zastosowaniu encji wszystkie dostępne mapowania będą wyświetlane w środowisku.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapy podwójnego zapisu](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="5d0b4-170">Odśwież encje danych po aktualizacji</span><span class="sxs-lookup"><span data-stu-id="5d0b4-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="5d0b4-171">W Finance przejdź do obszaru roboczego **Zarządzanie danymi**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-171">In Finance, go to the **Data management** workspace.</span></span>

![Obszar roboczy Zarządzanie danymi](./media/16DataManagement.png)

2. <span data-ttu-id="5d0b4-173">Wybierz kafelek **Parametry struktury**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-173">Select the **Framework parameters** tile.</span></span>

![Parametry struktury](./media/17FrameworkParameters.png)

3. <span data-ttu-id="5d0b4-175">Na stronie **Ustawienia encji** wybierz pozycję **Odśwież listę encji**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Odśwież listę encji](./media/18RefreshEntityList.png)

<span data-ttu-id="5d0b4-177">Odświeżenie zajmie około 20 minut.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="5d0b4-178">Po jego zakończeniu otrzymasz alert.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-178">You will receive an alert when it is complete.</span></span>

![Potwierdzenie odświeżenia](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="5d0b4-180">Aktualizowanie ustawień zabezpieczeń w programie Project Operations w Dataverse</span><span class="sxs-lookup"><span data-stu-id="5d0b4-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="5d0b4-181">Przejdź do Project Operations w swoim środowisku Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="5d0b4-182">Przejdź do **Ustawienia** > **Zabezpieczenia** > **Role zabezpieczeń**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="5d0b4-183">Na stronie **Role zabezpieczeń** z listy ról wybierz **użytkownik aplikacji z podwójnym zapisem** i wybierz kartę **Encje niestandardowe**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="5d0b4-184">Sprawdź, czy rola ma uprawnienia **Odczyt** i **Dołączanie do** dla:</span><span class="sxs-lookup"><span data-stu-id="5d0b4-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="5d0b4-185">**Typ kursu wymiany waluty**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="5d0b4-186">**Plan kont**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="5d0b4-187">**Kalendarz obrachunkowy**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="5d0b4-188">**Księga**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-188">**Ledger**</span></span>

5. <span data-ttu-id="5d0b4-189">Po zaktualizowaniu rola zabezpieczeń przejdź do **Ustawienia** > **Zabezpieczenia** > **Teams** i wybierz domyślny zespół w widoku zespołu **Lokalnego właściciela firmy**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="5d0b4-190">Wybierz pozycję **Zarządzaj rolami** i sprawdź, czy uprawnienie zabezpieczeń **użytkownika aplikacji z podwójnym zapisem** jest stosowane do tego zespołu.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="5d0b4-191">Uruchomienie map podwójnego zapisu Project Operations</span><span class="sxs-lookup"><span data-stu-id="5d0b4-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="5d0b4-192">W projekcie LCS przejdź na stronę **Szczegóły środowiska**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5d0b4-193">W obszarze **Informacje o środowisku Common Data Service** wybierz pozycję **Połącz z CDS dla aplikacji.**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="5d0b4-194">Po wybraniu łącza nastąpi przekierowanie do listy encji w mapowaniach.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="5d0b4-195">Uruchom mapowanie w sposób opisany w poniższej tabeli.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="5d0b4-196">Upewnij się, że kolejność jest zgodna z tą na liście.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="5d0b4-197">**Mapowanie encji**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-197">**Entity Map**</span></span> | <span data-ttu-id="5d0b4-198">**Odśwież encje**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-198">**Refresh entity**</span></span> | <span data-ttu-id="5d0b4-199">**Synchronizacja początkowa**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-199">**Initial sync**</span></span> | <span data-ttu-id="5d0b4-200">**Wzorzec dla synchronizacji początkowej**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-200">**Master for initial sync**</span></span> | <span data-ttu-id="5d0b4-201">**Uruchom wymagania wstępne**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-201">**Run prerequisites**</span></span> | <span data-ttu-id="5d0b4-202">**Synchronizacja początkowa wymagań**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="5d0b4-203">**Role zasobów projektu dla wszystkich firm (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="5d0b4-204">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-204">No</span></span> | <span data-ttu-id="5d0b4-205">Tak</span><span class="sxs-lookup"><span data-stu-id="5d0b4-205">Yes</span></span> | <span data-ttu-id="5d0b4-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5d0b4-206">Common Data Service</span></span> | <span data-ttu-id="5d0b4-207">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-207">No</span></span> | <span data-ttu-id="5d0b4-208">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-208">N\A</span></span> |
| <span data-ttu-id="5d0b4-209">**Firmy (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="5d0b4-210">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-210">No</span></span> | <span data-ttu-id="5d0b4-211">Tak</span><span class="sxs-lookup"><span data-stu-id="5d0b4-211">Yes</span></span> | <span data-ttu-id="5d0b4-212">Aplikacje rozwiązania Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5d0b4-212">Finance and Operations apps</span></span> | <span data-ttu-id="5d0b4-213">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-213">No</span></span> | <span data-ttu-id="5d0b4-214">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-214">N\A</span></span> |
| <span data-ttu-id="5d0b4-215">**Księga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="5d0b4-216">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-216">No</span></span> | <span data-ttu-id="5d0b4-217">Tak</span><span class="sxs-lookup"><span data-stu-id="5d0b4-217">Yes</span></span> | <span data-ttu-id="5d0b4-218">Aplikacje rozwiązania Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5d0b4-218">Finance and Operations apps</span></span> | <span data-ttu-id="5d0b4-219">Tak</span><span class="sxs-lookup"><span data-stu-id="5d0b4-219">Yes</span></span> | <span data-ttu-id="5d0b4-220">Tak, aplikacje Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5d0b4-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="5d0b4-221">**Wartości rzeczywiste integracji Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="5d0b4-222">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-222">No</span></span> | <span data-ttu-id="5d0b4-223">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-223">No</span></span> | <span data-ttu-id="5d0b4-224">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-224">N\A</span></span> | <span data-ttu-id="5d0b4-225">Tak</span><span class="sxs-lookup"><span data-stu-id="5d0b4-225">Yes</span></span> | <span data-ttu-id="5d0b4-226">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-226">No</span></span> |
| <span data-ttu-id="5d0b4-227">**Pozycje kontraktu w projekcie (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="5d0b4-228">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-228">No</span></span> | <span data-ttu-id="5d0b4-229">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-229">No</span></span> | <span data-ttu-id="5d0b4-230">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-230">N\A</span></span> | <span data-ttu-id="5d0b4-231">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-231">No</span></span> | <span data-ttu-id="5d0b4-232">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-232">No</span></span> |
| <span data-ttu-id="5d0b4-233">**Encja integrująca dla transakcji projektu relacje (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="5d0b4-234">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-234">No</span></span> | <span data-ttu-id="5d0b4-235">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-235">No</span></span> | <span data-ttu-id="5d0b4-236">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-236">N\A</span></span> | <span data-ttu-id="5d0b4-237">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-237">No</span></span> | <span data-ttu-id="5d0b4-238">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-238">N\A</span></span> |
| <span data-ttu-id="5d0b4-239">**Punkty kontrolne pozycji kontraktu w integracji Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="5d0b4-240">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-240">No</span></span> | <span data-ttu-id="5d0b4-241">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-241">No</span></span> | <span data-ttu-id="5d0b4-242">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-242">N\A</span></span> | <span data-ttu-id="5d0b4-243">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-243">No</span></span> | <span data-ttu-id="5d0b4-244">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-244">N\A</span></span> |
| <span data-ttu-id="5d0b4-245">**Encja integracji Project Operations na potrzeby oszacowania kosztów (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="5d0b4-246">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-246">No</span></span> | <span data-ttu-id="5d0b4-247">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-247">No</span></span> | <span data-ttu-id="5d0b4-248">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-248">N\A</span></span> | <span data-ttu-id="5d0b4-249">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-249">No</span></span> | <span data-ttu-id="5d0b4-250">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-250">N\A</span></span> |
| <span data-ttu-id="5d0b4-251">**Encja integracji kategorii wydatków projektowych Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="5d0b4-252">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-252">No</span></span> | <span data-ttu-id="5d0b4-253">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-253">No</span></span> | <span data-ttu-id="5d0b4-254">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-254">N\A</span></span> | <span data-ttu-id="5d0b4-255">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-255">No</span></span> | <span data-ttu-id="5d0b4-256">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-256">N\A</span></span> |
| <span data-ttu-id="5d0b4-257">**Encja integracji wydatków projektowych Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="5d0b4-258">Tak</span><span class="sxs-lookup"><span data-stu-id="5d0b4-258">Yes</span></span> | <span data-ttu-id="5d0b4-259">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-259">No</span></span> | <span data-ttu-id="5d0b4-260">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-260">N\A</span></span> | <span data-ttu-id="5d0b4-261">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-261">No</span></span> | <span data-ttu-id="5d0b4-262">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-262">N\A</span></span> |
| <span data-ttu-id="5d0b4-263">**Encja integracji Project Operations na potrzeby oszacowania godzinowego (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="5d0b4-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="5d0b4-264">Tak</span><span class="sxs-lookup"><span data-stu-id="5d0b4-264">Yes</span></span> | <span data-ttu-id="5d0b4-265">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-265">No</span></span> | <span data-ttu-id="5d0b4-266">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-266">N\A</span></span> | <span data-ttu-id="5d0b4-267">No</span><span class="sxs-lookup"><span data-stu-id="5d0b4-267">No</span></span> | <span data-ttu-id="5d0b4-268">nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="5d0b4-268">N\A</span></span> |


4. <span data-ttu-id="5d0b4-269">Aby odświeżyć encję, wybierz nazwę mapowania, a następnie wybierz opcję **Odśwież encje**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Odśwież mapowanie](./media/20RefreshMapping.png)

5. <span data-ttu-id="5d0b4-271">Po odświeżeniu uruchom mapowanie.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="5d0b4-272">Przed włączeniem następnego mapowania należy sprawdzić, czy mapowanie w tabeli jest w stanie **Działającym**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="5d0b4-273">Uruchamianie mapowania z większą liczbą wstępnie wymaganych programów może zająć dużo czasu.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="5d0b4-274">Aby uruchomić mapowanie z wymaganiami wstępnymi, włącz przełącznik **Pokaż mapowania encji pokrewnych**.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="5d0b4-275">Jeśli tabela wskazuje , że **Wymagana wstępna synchronizacja** ma stan **Nie** sprawdź, czy flaga **Wstępna synchronizacja** jest **wyłączona** we wszystkich mapowaniach wymagań wstępnych, zanim zostanie ono uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Uruchom mapowanie](./media/21RunMap.png)

6. <span data-ttu-id="5d0b4-277">Sprawdź poprawność wszystkich mapowań powiązanych z projektem.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-277">Validate all project related maps are in the running state.</span></span>

![Wszystkie mapowania uruchomione](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="5d0b4-279">Stosowanie danych konfiguracyjnych w usłudze CDS do aplikacji Project Operations (opcjonalne)</span><span class="sxs-lookup"><span data-stu-id="5d0b4-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="5d0b4-280">Jeśli dane demonstracyjne zostały zastosowane do środowiska Finance, zobacz [Konfigurowanie i stosowanie danych konfiguracyjnych w Common Data Service dla Project Operations](resource-apply-pro-setup-config-data.md) w celu zastosowania danych demonstracyjnych w środowisku CDS.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="5d0b4-281">Środowisko Project Operations jest teraz obsługiwane i konfigurowane.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]