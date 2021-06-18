---
title: Synchronizacja kategorii wydatku projektu między Finance and Operations i Project Service Automation
description: W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania kategorii wydatków projektu między Microsoft Dynamics 365 Finance do Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999864"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="22c9f-103">Synchronizacja kategorii wydatku projektu między Finance and Operations i Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22c9f-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="22c9f-104">W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania kategorii wydatków projektu między Dynamics 365 Finance do Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22c9f-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="22c9f-105">W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.</span><span class="sxs-lookup"><span data-stu-id="22c9f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="22c9f-106">Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="22c9f-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="22c9f-107">Jeśli używasz wersji Enterprise 7.3.0, po zainstalowaniu KB 4132657 i KB 4132660 będziesz mógł używać szablonów do integracji zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych, szacunków wydatków i danych rzeczywistych oraz do konfigurowania funkcji zamykający.</span><span class="sxs-lookup"><span data-stu-id="22c9f-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="22c9f-108">Jeśli musisz zresetować dystrybucje rozliczeń, zalecamy również zainstalowanie KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="22c9f-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="22c9f-109">Przepływ danych dla Project Service Automation i Finance</span><span class="sxs-lookup"><span data-stu-id="22c9f-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="22c9f-110">Rozwiązanie do integracji Project Service Automation i Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="22c9f-111">Szablony integracji, które są dostępne z funkcją integracji danych, umożliwiają przepływ danych o kategoriach transakcji wydatków projektu między Finance i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22c9f-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="22c9f-112">Jeśli kategorie wydatków projektu są na pewno finansowane w finansach, przepływ integracji jest najpierw z Finance do rozwiązania Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22c9f-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="22c9f-113">Identyfikatory integracji kategorii wydatków projektu są następnie aktualizowane poprzez synchronizację z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="22c9f-114">Jeśli kategorie wydatków projektu są opanowane w Project Service Automation, przepływ integracji jest najpierw z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="22c9f-115">Kategorie projektów muszą być już skonfigurowane w Finance przed synchronizacją z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22c9f-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="22c9f-116">Następnie zsynchronizuj z Finance z powrotem do Project Service Automation, a następnie ponownie z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="22c9f-117">W ten sposób pomagasz zagwarantować, że kategorie są połączone i że nie są tworzone żadne duplikaty.</span><span class="sxs-lookup"><span data-stu-id="22c9f-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="22c9f-118">Zazwyczaj kategorie wydatków projektu są opanowane w Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="22c9f-119">Jeśli jednak tak nie jest lub jeśli kategorie wydatków zostały już utworzone w programie Project Service Automation, należy najpierw zsynchronizować za pomocą szablonu Kategorie transakcji wydatków projektu (PSA do Fin i Ops).</span><span class="sxs-lookup"><span data-stu-id="22c9f-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="22c9f-120">Następnie zsynchronizuj za pomocą szablonu Kategorie transakcji wydatków projektu (Fin i Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="22c9f-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="22c9f-121">Następnie należy jeszcze raz uruchomić synchronizację z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="22c9f-122">Jeśli synchronizujesz najpierw z Project Service Automation, przed uruchomieniem synchronizacji w Finance muszą być spełnione następujące wymagania:</span><span class="sxs-lookup"><span data-stu-id="22c9f-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="22c9f-123">Kategoria udostępniona, która jest zgodna z kategorią projektu skonfigurowaną w programie Project Service Automation, musi istnieć i musi być włączona zarówno dla **Projektu**, jak i dla **Wydatków**.</span><span class="sxs-lookup"><span data-stu-id="22c9f-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="22c9f-124">Dla każdej firmy finansowej, z którą należy zintegrować, muszą istnieć następujące kategorie projektów:</span><span class="sxs-lookup"><span data-stu-id="22c9f-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="22c9f-125">**Kategoria projektu** istnieje.</span><span class="sxs-lookup"><span data-stu-id="22c9f-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="22c9f-126">**Użycie funkcji w wydatkach** jest włączone.</span><span class="sxs-lookup"><span data-stu-id="22c9f-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="22c9f-127">**Aktywny w arkuszu** jest włączony.</span><span class="sxs-lookup"><span data-stu-id="22c9f-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="22c9f-128">**Typ transakcji** jest ustawiony na **Koszt**.</span><span class="sxs-lookup"><span data-stu-id="22c9f-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="22c9f-129">Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="22c9f-130">[![Przepływ danych do integracji Project Service Automation z Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="22c9f-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="22c9f-131">Synchronizacja kategorii wydatków projektu z Finance do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22c9f-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="22c9f-132">Szablon i zadanie</span><span class="sxs-lookup"><span data-stu-id="22c9f-132">Template and task</span></span>

<span data-ttu-id="22c9f-133">Aby uzyskać dostęp do szablonu, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty**, a następnie w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać szablony publiczne.</span><span class="sxs-lookup"><span data-stu-id="22c9f-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="22c9f-134">Następujący szablon i podstawowe zadanie służą do synchronizowania kategorii wydatków projektu z Finance do Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="22c9f-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="22c9f-135">**Nazwa szablonu podczas integracji danych:** Kategorie transakcji wydatków projektu (od Fin i Ops do PSA)</span><span class="sxs-lookup"><span data-stu-id="22c9f-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="22c9f-136">**Nazwa zadania w projekcie:** Synchronizacja kategorii do PSA</span><span class="sxs-lookup"><span data-stu-id="22c9f-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="22c9f-137">Zestaw encji</span><span class="sxs-lookup"><span data-stu-id="22c9f-137">Entity set</span></span>

| <span data-ttu-id="22c9f-138">Finanse</span><span class="sxs-lookup"><span data-stu-id="22c9f-138">Finance</span></span>                           | <span data-ttu-id="22c9f-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22c9f-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="22c9f-140">Encja integrująca dla kategorii</span><span class="sxs-lookup"><span data-stu-id="22c9f-140">Integration entity for categories</span></span> | <span data-ttu-id="22c9f-141">Kategorie transakcji</span><span class="sxs-lookup"><span data-stu-id="22c9f-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="22c9f-142">Przepływ encji</span><span class="sxs-lookup"><span data-stu-id="22c9f-142">Entity flow</span></span>

<span data-ttu-id="22c9f-143">Kategorie wydatków projektów są zarządzane w Finance i są synchronizowane z Project Service Automation jako kategorie transakcji.</span><span class="sxs-lookup"><span data-stu-id="22c9f-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="22c9f-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="22c9f-144">Power Query</span></span>

<span data-ttu-id="22c9f-145">Przy synchronizowaniu z Project Service Automation należy użyć Microsoft Power Query dla Excel w celu ustawienia typu fakturowania w kategorii transakcji.</span><span class="sxs-lookup"><span data-stu-id="22c9f-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="22c9f-146">Kategoria transakcji wydatku projektu (Fin i Ops do PSA) zawiera domyślną kolumnę i mapowanie.</span><span class="sxs-lookup"><span data-stu-id="22c9f-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="22c9f-147">Aby utworzyć własny szablon, należy w Power Query dodać kolumnę warunkową.</span><span class="sxs-lookup"><span data-stu-id="22c9f-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="22c9f-148">Wykonaj poniższe kroki.</span><span class="sxs-lookup"><span data-stu-id="22c9f-148">Follow these steps.</span></span>

1. <span data-ttu-id="22c9f-149">Kliknij strzałkę, aby otworzyć mapowanie zadania kategorii wydatków projektu w szablonie Kategorie transakcji wydatków w projekcie (Fin i Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="22c9f-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="22c9f-150">Kliknij łącze **Zaawansowane zapytania i filtrowania**, aby otworzyć Power Query.</span><span class="sxs-lookup"><span data-stu-id="22c9f-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="22c9f-151">Wybierz opcję **Dodaj kolumnę warunkową**.</span><span class="sxs-lookup"><span data-stu-id="22c9f-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="22c9f-152">Wprowadź nazwę nowej kolumny, na przykład nazwa **TypRozliczenia**.</span><span class="sxs-lookup"><span data-stu-id="22c9f-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="22c9f-153">Wprowadź następujący warunek: **Jeśli CATEGORYID nie jest równy zero, 19235001, w przeciwnym razie zero**.</span><span class="sxs-lookup"><span data-stu-id="22c9f-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="22c9f-154">Kliknij **OK** w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="22c9f-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="22c9f-155">Należy pamiętać, aby zamapować tę nową kolumnę na stronie mapowania.</span><span class="sxs-lookup"><span data-stu-id="22c9f-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="22c9f-156">Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych.</span><span class="sxs-lookup"><span data-stu-id="22c9f-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="22c9f-157">Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z rozwiązania Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22c9f-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="22c9f-158">[![Synchronizacja kategorii wydatków projektu z mapowaniem szablonów Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="22c9f-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="22c9f-159">Synchronizacja kategorii wydatków projektu z Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="22c9f-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="22c9f-160">Szablon i zadanie</span><span class="sxs-lookup"><span data-stu-id="22c9f-160">Template and task</span></span>

<span data-ttu-id="22c9f-161">Następujący szablon i podstawowe zadanie służą do synchronizowania kategorii wydatków projektu z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="22c9f-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="22c9f-162">**Nazwa szablonu podczas integracji danych:** Kategorie transakcji wydatków projektu (PSA do Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="22c9f-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="22c9f-163">**Nazwa zadania w projekcie:** Synchronizacja kategorii do Fin Ops</span><span class="sxs-lookup"><span data-stu-id="22c9f-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="22c9f-164">Zestaw encji</span><span class="sxs-lookup"><span data-stu-id="22c9f-164">Entity set</span></span>

| <span data-ttu-id="22c9f-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="22c9f-165">Project Service Automation</span></span> | <span data-ttu-id="22c9f-166">Finanse</span><span class="sxs-lookup"><span data-stu-id="22c9f-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="22c9f-167">Kategorie transakcji</span><span class="sxs-lookup"><span data-stu-id="22c9f-167">Transaction categories</span></span>     | <span data-ttu-id="22c9f-168">Encja integrująca dla kategorii</span><span class="sxs-lookup"><span data-stu-id="22c9f-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="22c9f-169">Przepływ encji</span><span class="sxs-lookup"><span data-stu-id="22c9f-169">Entity flow</span></span>

<span data-ttu-id="22c9f-170">Kategorie wydatków projektów są zarządzane w Finance i są synchronizowane z Project Service Automation jako kategorie transakcji.</span><span class="sxs-lookup"><span data-stu-id="22c9f-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="22c9f-171">Synchronizacja z powrotem do Finance aktualizuje kategorię projektu w Finance za pomocą identyfikatora integracji z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="22c9f-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="22c9f-172">Mapowanie szablonów w integracji danych</span><span class="sxs-lookup"><span data-stu-id="22c9f-172">Template mapping in Data integration</span></span>

<span data-ttu-id="22c9f-173">Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych.</span><span class="sxs-lookup"><span data-stu-id="22c9f-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="22c9f-174">Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="22c9f-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="22c9f-175">[![Mapowanie szablonu Project Service Automation z Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="22c9f-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]