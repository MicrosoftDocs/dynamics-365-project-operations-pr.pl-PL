---
title: Synchronizowanie szacowań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations
description: W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania szacunków godzin projektu i szacunków kosztów projektu bezpośrednio z Microsoft Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999729"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b0998-103">Synchronizowanie szacowań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b0998-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b0998-104">W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania szacunków godzin projektu i szacunków kosztów projektu bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b0998-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="b0998-105">W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.</span><span class="sxs-lookup"><span data-stu-id="b0998-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="b0998-106">Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="b0998-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="b0998-107">Przepływ danych dla Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="b0998-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="b0998-108">Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="b0998-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b0998-109">Szablony integracji, które są dostępne z funkcją integracji danych, umożliwiają przepływ danych o szacunkach godzin projektu i szacunkach kosztów projektu z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="b0998-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b0998-110">Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b0998-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b0998-111">[![Przepływ danych do integracji Project Service Automation z Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b0998-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="b0998-112">Szacowania godzin projektu</span><span class="sxs-lookup"><span data-stu-id="b0998-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="b0998-113">Szablon i zadania</span><span class="sxs-lookup"><span data-stu-id="b0998-113">Template and tasks</span></span>

<span data-ttu-id="b0998-114">Aby uzyskać dostęp do dostępnych szablonów, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty**, a następnie w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać szablony publiczne.</span><span class="sxs-lookup"><span data-stu-id="b0998-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b0998-115">Następujący szablon i podstawowe zadania są używane do synchronizowania szacowań godzin projektu z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="b0998-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b0998-116">**Nazwa szablonu podczas integracji danych:** szacowania godzin projektu (PSA do Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="b0998-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b0998-117">**Nazwa zadań w projekcie:**</span><span class="sxs-lookup"><span data-stu-id="b0998-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="b0998-118">Relacje transakcji</span><span class="sxs-lookup"><span data-stu-id="b0998-118">Transaction relationships</span></span>
    - <span data-ttu-id="b0998-119">Szacowanie wydatków</span><span class="sxs-lookup"><span data-stu-id="b0998-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="b0998-120">Zestaw encji</span><span class="sxs-lookup"><span data-stu-id="b0998-120">Entity set</span></span>

| <span data-ttu-id="b0998-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b0998-121">Project Service Automation</span></span> | <span data-ttu-id="b0998-122">Finanse</span><span class="sxs-lookup"><span data-stu-id="b0998-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b0998-123">Zadania projektu</span><span class="sxs-lookup"><span data-stu-id="b0998-123">Project tasks</span></span>              | <span data-ttu-id="b0998-124">Encja integrująca dla oszacowań godzin projektu</span><span class="sxs-lookup"><span data-stu-id="b0998-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="b0998-125">Przepływ encji</span><span class="sxs-lookup"><span data-stu-id="b0998-125">Entity flow</span></span>

<span data-ttu-id="b0998-126">Szacunkami godzin projektu można zarządzać w Project Service Automation i synchronizować je z Finance jako prognozy godzin projektu.</span><span class="sxs-lookup"><span data-stu-id="b0998-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b0998-127">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="b0998-127">Prerequisites</span></span>

<span data-ttu-id="b0998-128">Zanim będzie można synchronizować oszacowania godzin projektu, należy zsynchronizować projekty, zadania projektów i kategorie transakcji z wydatkami projektu.</span><span class="sxs-lookup"><span data-stu-id="b0998-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="b0998-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="b0998-129">Power Query</span></span>

<span data-ttu-id="b0998-130">W szablonie szacunków godzin projektu należy użyć dodatku Microsoft Power Query dla programu Excel, aby wykonać następujące zadania:</span><span class="sxs-lookup"><span data-stu-id="b0998-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="b0998-131">Ustaw domyślny identyfikator modelu prognozy, który będzie używany podczas integracji tworzenia nowych prognoz godzinowych.</span><span class="sxs-lookup"><span data-stu-id="b0998-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="b0998-132">Odfiltruj wszystkie rekordy specyficzne dla zasobów w zadaniu, których integracja nie powiedzie się, do prognoz godzinowych.</span><span class="sxs-lookup"><span data-stu-id="b0998-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="b0998-133">Umożliwia odfiltrowanie pustych wierszy kategorii transakcji.</span><span class="sxs-lookup"><span data-stu-id="b0998-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="b0998-134">Niepowodzenie wykonania tego zadania może spowodować nieprawidłową prognozę godzinową.</span><span class="sxs-lookup"><span data-stu-id="b0998-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="b0998-135">Ustaw domyślny identyfikator modelu prognozy</span><span class="sxs-lookup"><span data-stu-id="b0998-135">Set the default forecast model ID</span></span>

<span data-ttu-id="b0998-136">Aby zaktualizować domyslny identyfikator modelu prognozy w szablonie, kliknij strzałkę na **mapie**, aby otworzyć mapowanie.</span><span class="sxs-lookup"><span data-stu-id="b0998-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="b0998-137">Zaznacz łącze **Zaawansowane zapytania i filtrowania**.</span><span class="sxs-lookup"><span data-stu-id="b0998-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="b0998-138">Jeśli używasz domyślnego szablonu szacowania godzin projektu (PSA do Fin i Ops), wybierz opcję **Wstawiony warunek** z listy **zastosowanych kroków**.</span><span class="sxs-lookup"><span data-stu-id="b0998-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="b0998-139">We wpisie **Funkcja** zamień **O\_forecast** na nazwę identyfikatora modelu prognozy, która ma być używana podczas integracji.</span><span class="sxs-lookup"><span data-stu-id="b0998-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="b0998-140">Szablon domyślny ma identyfikator modelu prognozy z danych demonstracyjnych.</span><span class="sxs-lookup"><span data-stu-id="b0998-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="b0998-141">Jeśli tworzysz nowy szablon, musisz dodać tę kolumnę.</span><span class="sxs-lookup"><span data-stu-id="b0998-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="b0998-142">W Power Query wybierz opcję **Dodaj kolumnę warunkową** i wprowadź nazwę nowej kolumny, na przykład **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="b0998-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="b0998-143">Wprowadź warunek dla kolumny, gdzie, jeśli zadanie projektowe nie ma wartości null, wtedy \<enter the forecast model ID\>. W przeciwnym razie ma wartość null.</span><span class="sxs-lookup"><span data-stu-id="b0998-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="b0998-144">Filtrowanie rekordów specyficznych dla zasobu</span><span class="sxs-lookup"><span data-stu-id="b0998-144">Filter out resource-specific records</span></span>

<span data-ttu-id="b0998-145">Szablon szacowania godzin projektu (PSA do Fin i Ops) zawiera domyślny filtr, który usuwa wszelkie rekordy specyficzne dla zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0998-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="b0998-146">W przypadku utworzenia własnego szablonu należy dodać ten filtr.</span><span class="sxs-lookup"><span data-stu-id="b0998-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="b0998-147">Zaznacz łącze **Zaawansowane zapytania i filtrowania**, aby filtrować kolumnę **msdyn\_islinetask** tak, aby zawierała tylko **Fałszywe** rekordy.</span><span class="sxs-lookup"><span data-stu-id="b0998-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="b0998-148">Odfiltruj puste wiersze kategorii transakcji</span><span class="sxs-lookup"><span data-stu-id="b0998-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="b0998-149">Aby usunąć wiersze, które mają puste kategorie transakcji, należy dodać filtr.</span><span class="sxs-lookup"><span data-stu-id="b0998-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="b0998-150">To zadanie jest wymagane, bez względu na to, czy jest używany szablon domyślny, czy też użytkownik tworzy własny szablon.</span><span class="sxs-lookup"><span data-stu-id="b0998-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="b0998-151">Ten filtr usuwa wszystkie wiersze podsumowania z usługi Project Service Automation, które mogą powodować niepoprawne prognozy godzinowe w Finance.</span><span class="sxs-lookup"><span data-stu-id="b0998-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="b0998-152">Wybierz łącze **Zaawansowane zapytania i filtrowania** w celu odfiltrowania pustych rekordów w kolumnie **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="b0998-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b0998-153">Mapowanie szablonów w integracji danych</span><span class="sxs-lookup"><span data-stu-id="b0998-153">Template mapping in Data integration</span></span>

<span data-ttu-id="b0998-154">Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych.</span><span class="sxs-lookup"><span data-stu-id="b0998-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b0998-155">Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="b0998-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b0998-156">[![Mapowanie szablonów zadań w integracji danych](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b0998-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="b0998-157">Szacunki kosztów projektu</span><span class="sxs-lookup"><span data-stu-id="b0998-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="b0998-158">Szablon i zadania</span><span class="sxs-lookup"><span data-stu-id="b0998-158">Template and tasks</span></span>

<span data-ttu-id="b0998-159">Następujący szablon i podstawowe zadania są używane do synchronizowania szacowań wydatków projektu z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="b0998-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b0998-160">**Nazwa szablonu podczas integracji danych:** szacowania wydatków projektu (PSA do Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="b0998-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b0998-161">**Nazwa zadań w projekcie:**</span><span class="sxs-lookup"><span data-stu-id="b0998-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="b0998-162">Relacje transakcji</span><span class="sxs-lookup"><span data-stu-id="b0998-162">Transaction relationships</span></span> 
    - <span data-ttu-id="b0998-163">Szacowanie wydatków</span><span class="sxs-lookup"><span data-stu-id="b0998-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="b0998-164">Zestaw encji</span><span class="sxs-lookup"><span data-stu-id="b0998-164">Entity set</span></span>

| <span data-ttu-id="b0998-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b0998-165">Project Service Automation</span></span> | <span data-ttu-id="b0998-166">Finanse</span><span class="sxs-lookup"><span data-stu-id="b0998-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="b0998-167">Połączenia transakcji</span><span class="sxs-lookup"><span data-stu-id="b0998-167">Transaction Connections</span></span>    | <span data-ttu-id="b0998-168">Encja integrująca dla transakcji projektu relacje</span><span class="sxs-lookup"><span data-stu-id="b0998-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="b0998-169">Wiersze szacowania</span><span class="sxs-lookup"><span data-stu-id="b0998-169">Estimate Lines</span></span>             | <span data-ttu-id="b0998-170">Encja integrująca dla oszacowań wydatków projektu</span><span class="sxs-lookup"><span data-stu-id="b0998-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="b0998-171">Przepływ encji</span><span class="sxs-lookup"><span data-stu-id="b0998-171">Entity flow</span></span>

<span data-ttu-id="b0998-172">Szacunkami wydatków projektu można zarządzać w Project Service Automation i synchronizować je z Finance jako prognozy wydatków projektu.</span><span class="sxs-lookup"><span data-stu-id="b0998-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b0998-173">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="b0998-173">Prerequisites</span></span>

<span data-ttu-id="b0998-174">Zanim będzie można synchronizować oszacowania wydatków projektu, należy zsynchronizować projekty, zadania projektów i kategorie transakcji z wydatkami projektu.</span><span class="sxs-lookup"><span data-stu-id="b0998-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="b0998-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="b0998-175">Power Query</span></span>

<span data-ttu-id="b0998-176">W szablonie szacowania wydatków projektu należy użyć dodatku Power Query do wykonania następujących zadań:</span><span class="sxs-lookup"><span data-stu-id="b0998-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="b0998-177">Filtr, w którym znajdują się tylko rekordy wierszy szacowanego wydatku.</span><span class="sxs-lookup"><span data-stu-id="b0998-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="b0998-178">Ustaw domyślny identyfikator modelu prognozy, który będzie używany podczas integracji tworzenia nowych prognoz godzinowych.</span><span class="sxs-lookup"><span data-stu-id="b0998-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="b0998-179">Przekształć typy fakturowania.</span><span class="sxs-lookup"><span data-stu-id="b0998-179">Transform the billing types.</span></span>
- <span data-ttu-id="b0998-180">Przekształć typy transakcji.</span><span class="sxs-lookup"><span data-stu-id="b0998-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="b0998-181">Filtr, w którym znajdują się tylko wiersze szacowanego wydatku.</span><span class="sxs-lookup"><span data-stu-id="b0998-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="b0998-182">Szablon Szacunki wydatków projektu (PSA do Fin i Ops) ma domyślny filtr, który obejmuje tylko wiersze wydatków w integracji.</span><span class="sxs-lookup"><span data-stu-id="b0998-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="b0998-183">W przypadku utworzenia własnego szablonu należy dodać ten filtr.</span><span class="sxs-lookup"><span data-stu-id="b0998-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="b0998-184">Zaznacz zadanie **Relacje transakcyjne**, a następnie kliknij strzałkę **Mapa**, aby otworzyć mapowanie.</span><span class="sxs-lookup"><span data-stu-id="b0998-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="b0998-185">Wybierz łącze **Zaawansowane zapytania i filtrowania**.</span><span class="sxs-lookup"><span data-stu-id="b0998-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="b0998-186">Przefiltruj kolumnę **msdyn\_transactiontype1**, tak aby zawierała tylko **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="b0998-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="b0998-187">Ustaw domyślny identyfikator modelu prognozy</span><span class="sxs-lookup"><span data-stu-id="b0998-187">Set the default forecast model ID</span></span>

<span data-ttu-id="b0998-188">Aby zaktualizować domyslny identyfikator modelu prognozy w szablonie, wybierz zadanie **Szacowanie wydatków**, a potem kliknij strzałkę **Mapa**, aby otworzyć mapowanie.</span><span class="sxs-lookup"><span data-stu-id="b0998-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="b0998-189">Wybierz łącze **Zaawansowane zapytania i filtrowania**.</span><span class="sxs-lookup"><span data-stu-id="b0998-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="b0998-190">Jeśli są używane szablony domyślne szacowania wydatków projektów (PSA do Fin i Ops), w Power Query wybierz najpierw **Wstawiony warunek** z sekcji **Zastosowane kroki**.</span><span class="sxs-lookup"><span data-stu-id="b0998-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="b0998-191">We wpisie **Funkcja** zamień **O\_forecast** na nazwę identyfikatora modelu prognozy, która ma być używana podczas integracji.</span><span class="sxs-lookup"><span data-stu-id="b0998-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="b0998-192">Szablon domyślny ma identyfikator modelu prognozy z danych demonstracyjnych.</span><span class="sxs-lookup"><span data-stu-id="b0998-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="b0998-193">Jeśli tworzysz nowy szablon, musisz dodać tę kolumnę.</span><span class="sxs-lookup"><span data-stu-id="b0998-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="b0998-194">W Power Query wybierz opcję **Dodaj kolumnę warunkową** i wprowadź nazwę nowej kolumny, na przykład **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="b0998-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="b0998-195">Wprowadź warunek dla kolumny, gdzie, jeśli identyfikator linii oszacowania nie ma wartości null, wtedy \<enter the forecast model ID\>. W przeciwnym razie ma wartość null.</span><span class="sxs-lookup"><span data-stu-id="b0998-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="b0998-196">Przekształć typy fakturowania</span><span class="sxs-lookup"><span data-stu-id="b0998-196">Transform the billing types</span></span>

<span data-ttu-id="b0998-197">Szablon Szacunki kosztów projektu (od PSA do Fin i Ops) zawiera kolumnę warunkową używaną do przekształcania typów rozliczeń otrzymywanych z Project Service Automation podczas integracji.</span><span class="sxs-lookup"><span data-stu-id="b0998-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="b0998-198">Jeśli tworzysz własny szablon, musisz dodać tę kolumnę warunkową.</span><span class="sxs-lookup"><span data-stu-id="b0998-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="b0998-199">Wybierz łącze **Zaawansowane zapytania i filtrowania**, a następnie wybierz opcję **Dodaj kolumnę warunkową**.</span><span class="sxs-lookup"><span data-stu-id="b0998-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="b0998-200">Wprowadź nazwę nowej kolumny, na przykład nazwa **TypRozliczenia**.</span><span class="sxs-lookup"><span data-stu-id="b0998-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="b0998-201">Następnie wprowadź następujący warunek:</span><span class="sxs-lookup"><span data-stu-id="b0998-201">Then enter the following condition:</span></span>

<span data-ttu-id="b0998-202">Jeśli **msdyn\_billingtype** = 192350000, to **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="b0998-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="b0998-203">inaczej jeśli **msdyn\_billingtype** = 192350001, to **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="b0998-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="b0998-204">inaczej jeśli **msdyn\_billingtype** = 192350002, to **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="b0998-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="b0998-205">inaczej **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="b0998-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="b0998-206">Przekształć typy transakcji</span><span class="sxs-lookup"><span data-stu-id="b0998-206">Transform the transaction types</span></span>

<span data-ttu-id="b0998-207">Szablon Szacunki kosztów projektu (od PSA do Fin i Ops) zawiera kolumnę warunkową używaną do przekształcania typów transakcji otrzymywanych z Project Service Automation podczas integracji.</span><span class="sxs-lookup"><span data-stu-id="b0998-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="b0998-208">Jeśli tworzysz własny szablon, musisz dodać tę kolumnę warunkową.</span><span class="sxs-lookup"><span data-stu-id="b0998-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="b0998-209">Wybierz łącze **Zaawansowane zapytania i filtrowania**, a następnie wybierz opcję **Dodaj kolumnę warunkową**.</span><span class="sxs-lookup"><span data-stu-id="b0998-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="b0998-210">Wprowadź nazwę nowej kolumny, na przykład nazwa **TypTransakcji**.</span><span class="sxs-lookup"><span data-stu-id="b0998-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="b0998-211">Następnie wprowadź następujący warunek:</span><span class="sxs-lookup"><span data-stu-id="b0998-211">Then enter the following condition:</span></span>

<span data-ttu-id="b0998-212">Jeśli **msdyn\_transactiontypecode** = 192350000, **Koszt**</span><span class="sxs-lookup"><span data-stu-id="b0998-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="b0998-213">inaczej jeśli **msdyn\_transactiontypecode** = 192350005, **Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="b0998-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="b0998-214">inaczej **null**</span><span class="sxs-lookup"><span data-stu-id="b0998-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b0998-215">Mapowanie szablonów w integracji danych</span><span class="sxs-lookup"><span data-stu-id="b0998-215">Template mapping in Data integration</span></span>

<span data-ttu-id="b0998-216">Poniższe ilustracje przedstawiają przykłady odwzorowań zadań szablonu w integracji danych.</span><span class="sxs-lookup"><span data-stu-id="b0998-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="b0998-217">Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="b0998-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b0998-218">[![Mapowanie szablonów transakcji szacowania wydatków](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b0998-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="b0998-219">[![Mapowanie szablonów szacowania wydatków](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b0998-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]