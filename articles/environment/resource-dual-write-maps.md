---
title: Wersje map podwójnego zapisu aplikacji Project Operations
description: Ten temat zawiera listę wymaganych map podwójnego zapisu w Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939025"
---
# <a name="project-operations-dual-write-map-versions"></a><span data-ttu-id="fb095-103">Wersje map podwójnego zapisu aplikacji Project Operations</span><span class="sxs-lookup"><span data-stu-id="fb095-103">Project Operations dual-write map versions</span></span>

<span data-ttu-id="fb095-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="fb095-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fb095-105">Użycie Dynamics 365 Project Operations do scenariuszy z zasobami w magazynie/niemagazynowanymi wymaga uruchomienia w środowisku zestawu map podwójnego zapisu.</span><span class="sxs-lookup"><span data-stu-id="fb095-105">Using Dynamics 365 Project Operations for resource/non-stocked scenarios requires a set of dual-write maps to be running in the environment.</span></span> 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a><span data-ttu-id="fb095-106">Wymagane mapy: Rozwiązanie aranżacji podwójnego zapisu</span><span class="sxs-lookup"><span data-stu-id="fb095-106">Prerequisite maps: Dual-write orchestration solution</span></span>

<span data-ttu-id="fb095-107">Następujące mapy są wymaganymi warunkami wstępnymi dla rozwiązania Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fb095-107">The following maps are required prerequisites for the Project Operations solution.</span></span> <span data-ttu-id="fb095-108">Pamiętaj, aby uruchomić mapowania wymienione w poniższej tabeli oraz dowolne mapowania tabel pokrewnych w środowisku.</span><span class="sxs-lookup"><span data-stu-id="fb095-108">Make sure to run the maps listed in the following table and any related table maps in your environment.</span></span>

| <span data-ttu-id="fb095-109">Mapowanie tabeli</span><span class="sxs-lookup"><span data-stu-id="fb095-109">Table map</span></span> | <span data-ttu-id="fb095-110">Synchronizacja początkowa</span><span class="sxs-lookup"><span data-stu-id="fb095-110">Initial sync</span></span> |
| --- | --- |
| <span data-ttu-id="fb095-111">Księga (msdyn_ledgers)</span><span class="sxs-lookup"><span data-stu-id="fb095-111">Ledger (msdyn_ledgers)</span></span> | <span data-ttu-id="fb095-112">Wymaga wstępnej synchronizacji mapy tabeli i wszystkich wymagań wstępnych.</span><span class="sxs-lookup"><span data-stu-id="fb095-112">Requires initial sync for the table map and all prerequisites.</span></span> <span data-ttu-id="fb095-113">Wzorzec dla synchronizacji początkowej to aplikacje Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fb095-113">Master for initial sync is Finance and Operations apps.</span></span> |
| <span data-ttu-id="fb095-114">Firmy (cdm_companies)</span><span class="sxs-lookup"><span data-stu-id="fb095-114">Legal entities (cdm_companies)</span></span> | <span data-ttu-id="fb095-115">Niewymagane.</span><span class="sxs-lookup"><span data-stu-id="fb095-115">Not required.</span></span> <span data-ttu-id="fb095-116">System wypełnia tę encję automatycznie, gdy środowiska są połączone przy użyciu funkcji podwójnego zapisu.</span><span class="sxs-lookup"><span data-stu-id="fb095-116">The system populates this entity automatically when environments are linked using dual-write.</span></span> |
| <span data-ttu-id="fb095-117">Klienci V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="fb095-117">Customers V3 (accounts)</span></span> | <span data-ttu-id="fb095-118">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-118">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-119">Vendors V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="fb095-119">Vendors V2 (msdyn_vendors)</span></span> | <span data-ttu-id="fb095-120">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-120">Not required for provisioning.</span></span> |

1. <span data-ttu-id="fb095-121">Z listy map wybierz mapowanie Księga **(msdyn\_ledgers)** ze wszystkimi wymaganiami wstępnymi i zaznacz pole wyboru **Synchronizacja początkowa**.</span><span class="sxs-lookup"><span data-stu-id="fb095-121">From the list of maps, select the Ledger **(msdyn\_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> <span data-ttu-id="fb095-122">W polu **Główny dla początkowej synchronizacji** wybierz **aplikacje Finance and Operations** zarówno dla mapy księgi głównej, jak i dla wszystkich map warunkowych.</span><span class="sxs-lookup"><span data-stu-id="fb095-122">In the **Master for initial sync** field, select **Finance and Operations apps** for both ledger map and all prerequisite maps.</span></span> <span data-ttu-id="fb095-123">Wybierz **Uruchom**.</span><span class="sxs-lookup"><span data-stu-id="fb095-123">Select **Run**.</span></span>

![Synchronizacja mapowania księgi](media/DW6.png)

1. <span data-ttu-id="fb095-125">Wykonaj te same kroki dla wszystkich pozostałych map tabel wymienionych w powyższej tabeli.</span><span class="sxs-lookup"><span data-stu-id="fb095-125">Follow the same steps for all remaining table maps listed in the above table.</span></span> <span data-ttu-id="fb095-126">Podczas uruchamiania tych map nie zaznaczaj pola wyboru **Synchronizacja początkowa**.</span><span class="sxs-lookup"><span data-stu-id="fb095-126">Do not select the **Initial sync** check box when running those maps.</span></span>

## <a name="project-operations-dual-write-maps"></a><span data-ttu-id="fb095-127">Project Operations — mapy podwójnego zapisu</span><span class="sxs-lookup"><span data-stu-id="fb095-127">Project Operations dual-write maps</span></span>

<span data-ttu-id="fb095-128">Następujące mapy są wymaganymi warunkami wstępnymi dla rozwiązania Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fb095-128">The following maps are required for a Project Operations solution.</span></span>

| <span data-ttu-id="fb095-129">**Mapowanie encji**</span><span class="sxs-lookup"><span data-stu-id="fb095-129">**Entity map**</span></span> | <span data-ttu-id="fb095-130">**Najnowsza wersja**</span><span class="sxs-lookup"><span data-stu-id="fb095-130">**Latest version**</span></span> | <span data-ttu-id="fb095-131">**Synchronizacja początkowa**</span><span class="sxs-lookup"><span data-stu-id="fb095-131">**Initial sync**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fb095-132">Encja integrująca dla transakcji projektu relacje (msdyn\_transactionconnections)</span><span class="sxs-lookup"><span data-stu-id="fb095-132">Integration entity for project transaction relationships (msdyn\_transactionconnections)</span></span> | <span data-ttu-id="fb095-133">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="fb095-133">1.0.0.0</span></span> | <span data-ttu-id="fb095-134">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-134">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-135">Nagłówki kontraktów projektów (sales orders)</span><span class="sxs-lookup"><span data-stu-id="fb095-135">Project contract headers (sales orders)</span></span> | <span data-ttu-id="fb095-136">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="fb095-136">1.0.0.1</span></span> | <span data-ttu-id="fb095-137">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-137">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-138">Pozycje kontraktu w projekcie (salesorderdetails)</span><span class="sxs-lookup"><span data-stu-id="fb095-138">Project contract lines (salesorderdetails)</span></span> | <span data-ttu-id="fb095-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="fb095-139">1.0.0.0</span></span> | <span data-ttu-id="fb095-140">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-140">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-141">Źródło danych projektu (msdyn_projectcontractsplitbillingrules)</span><span class="sxs-lookup"><span data-stu-id="fb095-141">Project funding source (msdyn_projectcontractsplitbillingrules)</span></span> | <span data-ttu-id="fb095-142">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="fb095-142">1.0.0.1</span></span> | <span data-ttu-id="fb095-143">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-143">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-144">Tabela integracji Project Operations dla szacowania materiałów (msdyn\_estimatelines)</span><span class="sxs-lookup"><span data-stu-id="fb095-144">Project Operations integration table for material estimates (msdyn\_estimatelines)</span></span> | <span data-ttu-id="fb095-145">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="fb095-145">1.0.0.0</span></span> | <span data-ttu-id="fb095-146">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-146">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-147">Propozycje faktury projektu V2 (invoices)</span><span class="sxs-lookup"><span data-stu-id="fb095-147">Project invoice proposals V2 (invoices)</span></span> | <span data-ttu-id="fb095-148">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="fb095-148">1.0.0.2</span></span> | <span data-ttu-id="fb095-149">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-149">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-150">Wartości rzeczywiste integracji Project Operations (msdyn_actuals)</span><span class="sxs-lookup"><span data-stu-id="fb095-150">Project Operations integration actuals (msdyn_actuals)</span></span> | <span data-ttu-id="fb095-151">1.0.0.14</span><span class="sxs-lookup"><span data-stu-id="fb095-151">1.0.0.14</span></span> | <span data-ttu-id="fb095-152">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-152">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-153">Punkty kontrolne pozycji kontraktu w integracji Project Operations (msdyn_contractlinesscheduleofvalues)</span><span class="sxs-lookup"><span data-stu-id="fb095-153">Project Operations integration contract line milestones (msdyn_contractlinesscheduleofvalues)</span></span> | <span data-ttu-id="fb095-154">1.0.0.4</span><span class="sxs-lookup"><span data-stu-id="fb095-154">1.0.0.4</span></span> | <span data-ttu-id="fb095-155">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-155">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-156">Encja integracji Project Operations na potrzeby oszacowania kosztów (msdyn_estimateslines)</span><span class="sxs-lookup"><span data-stu-id="fb095-156">Project Operations integration entity for expense estimates (msdyn_estimateslines)</span></span> | <span data-ttu-id="fb095-157">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="fb095-157">1.0.0.2</span></span> | <span data-ttu-id="fb095-158">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-158">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-159">Encja integracji Project Operations na potrzeby oszacowania godzinowego (msdyn_resourceassignments)</span><span class="sxs-lookup"><span data-stu-id="fb095-159">Project Operations integration entity for hour estimates (msdyn_resourceassignments)</span></span> | <span data-ttu-id="fb095-160">1.0.0.5</span><span class="sxs-lookup"><span data-stu-id="fb095-160">1.0.0.5</span></span> | <span data-ttu-id="fb095-161">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-161">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-162">Encja integracji kategorii wydatków projektowych Project Operations (msdyn_expensecategories)</span><span class="sxs-lookup"><span data-stu-id="fb095-162">Project Operations integration project expense categories export entity (msdyn_expensecategories)</span></span> | <span data-ttu-id="fb095-163">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="fb095-163">1.0.0.2</span></span> | <span data-ttu-id="fb095-164">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-164">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-165">Encja integracji wydatków projektowych Project Operations (msdyn_expenses)</span><span class="sxs-lookup"><span data-stu-id="fb095-165">Project Operations integration project expenses export entity (msdyn_expenses)</span></span> | <span data-ttu-id="fb095-166">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="fb095-166">1.0.0.2</span></span> | <span data-ttu-id="fb095-167">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-167">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-168">Integracja w Project Operations encji eksportu faktury dostawcy projektu (msdyn_projectvendorinvoices)</span><span class="sxs-lookup"><span data-stu-id="fb095-168">Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)</span></span> | <span data-ttu-id="fb095-169">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="fb095-169">1.0.0.0</span></span> | <span data-ttu-id="fb095-170">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-170">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-171">Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu (msdyn_projectvendorinvoicelines)</span><span class="sxs-lookup"><span data-stu-id="fb095-171">Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)</span></span> | <span data-ttu-id="fb095-172">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="fb095-172">1.0.0.0</span></span> | <span data-ttu-id="fb095-173">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-173">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-174">Role zasobów projektu dla wszystkich firm (bookableresourcecategories)</span><span class="sxs-lookup"><span data-stu-id="fb095-174">Project resource roles for all companies (bookableresourcecategories)</span></span> | <span data-ttu-id="fb095-175">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="fb095-175">1.0.0.1</span></span> | <span data-ttu-id="fb095-176">Wymaga wstępnej synchronizacji mapowania tabeli w celu zsynchronizowania ról zasobów Menedżer projektu i Członek zespołu, które zostały uzupełnione w środowisku usługi Dynamics 365 Dataverse podczas inicjowania obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="fb095-176">Requires an initial sync for the table map to synchronize the Project Manager and Team member resource roles that are populated in the Dynamics 365 Dataverse environment during provisioning.</span></span> <span data-ttu-id="fb095-177">Dataverse jest głównym źródłem początkowej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fb095-177">Dataverse is the main source for the initial synchronization.</span></span> |
| <span data-ttu-id="fb095-178">Zadania projektu (msdyn_projecttasks)</span><span class="sxs-lookup"><span data-stu-id="fb095-178">Project tasks (msdyn_projecttasks)</span></span> | <span data-ttu-id="fb095-179">1.0.0.4</span><span class="sxs-lookup"><span data-stu-id="fb095-179">1.0.0.4</span></span> | <span data-ttu-id="fb095-180">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-180">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-181">Kategorie transakcji projektu (msdyn_transactioncategories)</span><span class="sxs-lookup"><span data-stu-id="fb095-181">Project transaction categories (msdyn_transactioncategories)</span></span> | <span data-ttu-id="fb095-182">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="fb095-182">1.0.0.0</span></span> | <span data-ttu-id="fb095-183">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-183">Not required for provisioning.</span></span> |
| <span data-ttu-id="fb095-184">Projekty V2 (msdyn_projects)</span><span class="sxs-lookup"><span data-stu-id="fb095-184">Projects V2 (msdyn_projects)</span></span> | <span data-ttu-id="fb095-185">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="fb095-185">1.0.0.1</span></span> | <span data-ttu-id="fb095-186">Nie jest wymagane do inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="fb095-186">Not required for provisioning.</span></span> |

<span data-ttu-id="fb095-187">Wykonaj następujące kroki, aby uruchomić wymienione mapowania.</span><span class="sxs-lookup"><span data-stu-id="fb095-187">Complete the following steps to run the listed maps.</span></span>

1. <span data-ttu-id="fb095-188">Włącz role zasobów projektu dla **wszystkich firm (bookableresourcecategories)**, ponieważ to mapowanie wymaga początkowej synchronizacji. W polu **Główny dla początkowej synchronizacji** wybierz usługę **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="fb095-188">Enable the Project resource roles for **all companies (bookableresourcecategories)** table map as this map requires the initial sync. In the **Master for initial sync** field, select **Common data service**.</span></span> 

 ![Synchronizacja mapowania tabeli ról zasobów](media/6ResourceInitialSync.jpg)

 <span data-ttu-id="fb095-190">Przed przejściem do następnego kroku poczekaj, aż stan mapy zmieni się na **Uruchomione**.</span><span class="sxs-lookup"><span data-stu-id="fb095-190">Wait until the status of the map is **Running** before you move to the next step.</span></span>

2. <span data-ttu-id="fb095-191">Wybierz wszystkie pozostałe wymagane mapowania.</span><span class="sxs-lookup"><span data-stu-id="fb095-191">Select all of the remaining required maps.</span></span> <span data-ttu-id="fb095-192">Można filtrować je na liście mapy podwójnego zapisu, używając słowa kluczowego **Projekt** w wyszukiwaniu w prawym górnym rogu.</span><span class="sxs-lookup"><span data-stu-id="fb095-192">You can filter them in the dual-write map list using the keyword, **Project** in search in the upper-right corner.</span></span> <span data-ttu-id="fb095-193">Możesz zaznaczyć wszystkie mapy, a następnie uruchomić.</span><span class="sxs-lookup"><span data-stu-id="fb095-193">You can multi-select all maps and then run.</span></span> <span data-ttu-id="fb095-194">Aby uzyskać więcej informacji, zobacz temat [Zarządzanie wieloma mapowaniami tabel](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps).</span><span class="sxs-lookup"><span data-stu-id="fb095-194">For more information, see [Manage multiple table maps](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps).</span></span> <span data-ttu-id="fb095-195">Pamiętaj, aby włączyć i uruchomić pokrewne mapowania encji.</span><span class="sxs-lookup"><span data-stu-id="fb095-195">Make sure to also enable and run related entity maps.</span></span>

### <a name="project-operations-dual-write-map-versions"></a><span data-ttu-id="fb095-196">Wersje map podwójnego zapisu aplikacji Project Operations</span><span class="sxs-lookup"><span data-stu-id="fb095-196">Project Operations dual-write map versions</span></span>

<span data-ttu-id="fb095-197">Zawsze uruchamiaj najnowszą wersję mapy w środowisku użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fb095-197">Always run the latest version of the map in your environment.</span></span> <span data-ttu-id="fb095-198">Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli istnieje któryś z następujących warunków:</span><span class="sxs-lookup"><span data-stu-id="fb095-198">Certain features and capabilities might not work correctly if any of the following conditions exist:</span></span>

- <span data-ttu-id="fb095-199">Mapowanie nie jest aktywowane.</span><span class="sxs-lookup"><span data-stu-id="fb095-199">A map isn't activated.</span></span>
- <span data-ttu-id="fb095-200">Najnowsza wersja mapy nie jest aktywowana.</span><span class="sxs-lookup"><span data-stu-id="fb095-200">The latest version of the map isn't activated.</span></span> 
- <span data-ttu-id="fb095-201">Powiązane mapowania tabel nie są aktywowane.</span><span class="sxs-lookup"><span data-stu-id="fb095-201">Related table maps aren't activated.</span></span>

<span data-ttu-id="fb095-202">Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**.</span><span class="sxs-lookup"><span data-stu-id="fb095-202">You can view the active version of the map in the **Version** column on the **Dual-write** page.</span></span> <span data-ttu-id="fb095-203">Aby uaktywnić nową wersję mapy, należy wybrać **Wersję mapowania tabeli**, a następnie zapisać wybraną wersję po wybraniu najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="fb095-203">You can activate a new version of the map by selecting **Table map versions**, selecting the latest version, and then saving the selected version.</span></span> <span data-ttu-id="fb095-204">Jeśli dostosowałeś niestandardową mapę tabeli, będziesz musiał ponownie zastosować zmiany.</span><span class="sxs-lookup"><span data-stu-id="fb095-204">If you have customized an out-of-the-box table map, you will need reapply the changes.</span></span> <span data-ttu-id="fb095-205">Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).</span><span class="sxs-lookup"><span data-stu-id="fb095-205">For more information, see [Application lifecycle management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).</span></span>