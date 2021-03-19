---
title: Synchronizowanie zadań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations
description: Ta temat opisuje szablon i podstawowe zadanie używane do synchronizowania zadań projektu bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288932"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b398e-103">Synchronizowanie zadań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b398e-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b398e-104">Ta temat opisuje szablon i podstawowe zadanie używane do synchronizowania zadań projektu bezpośrednio z Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b398e-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="b398e-105">W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.</span><span class="sxs-lookup"><span data-stu-id="b398e-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="b398e-106">Jeśli używasz wersji Enterprise 7.3.0, po zainstalowaniu KB 4132657 i KB 4132660 będziesz mógł używać szablonów do integracji zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych, szacunków wydatków i danych rzeczywistych oraz do konfigurowania funkcji zamykający.</span><span class="sxs-lookup"><span data-stu-id="b398e-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b398e-107">Jeśli musisz zresetować dystrybucje rozliczeń, zalecamy również zainstalowanie KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="b398e-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="b398e-108">Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="b398e-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="b398e-109">Przepływ danych dla Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="b398e-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="b398e-110">Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="b398e-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b398e-111">Szablon integracji dostępny z funkcją integracji danych umożliwia przepływ danych o zadaniach projektowych z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="b398e-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b398e-112">Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="b398e-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b398e-113">[![Przepływ danych do integracji Project Service Automation z Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b398e-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="b398e-114">Szablon i zadanie</span><span class="sxs-lookup"><span data-stu-id="b398e-114">Template and task</span></span>

<span data-ttu-id="b398e-115">Aby uzyskać dostęp do szablonu, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty**, a następnie w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać szablony publiczne.</span><span class="sxs-lookup"><span data-stu-id="b398e-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b398e-116">Następujący szablon i podstawowe zadanie służą do synchronizowania zadań projektu z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="b398e-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b398e-117">**Nazwa szablonu podczas integracji danych:** zadania projektu (PSA do Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="b398e-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b398e-118">**Nazwa zadania w projekcie:** Zadania projektu</span><span class="sxs-lookup"><span data-stu-id="b398e-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="b398e-119">Przed synchronizacją zadań projektu należy zsynchronizować umowy dotyczące projektów i projekty.</span><span class="sxs-lookup"><span data-stu-id="b398e-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="b398e-120">Zestaw encji</span><span class="sxs-lookup"><span data-stu-id="b398e-120">Entity set</span></span>

| <span data-ttu-id="b398e-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b398e-121">Project Service Automation</span></span> | <span data-ttu-id="b398e-122">Finanse</span><span class="sxs-lookup"><span data-stu-id="b398e-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="b398e-123">Zadania projektu</span><span class="sxs-lookup"><span data-stu-id="b398e-123">Project Tasks</span></span>              | <span data-ttu-id="b398e-124">Encja integrująca dla zadania projektu</span><span class="sxs-lookup"><span data-stu-id="b398e-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b398e-125">Przepływ encji</span><span class="sxs-lookup"><span data-stu-id="b398e-125">Entity flow</span></span>

<span data-ttu-id="b398e-126">Zadaniami projektu zarządza się w Project Service Automation i są one synchronizowane z Finance jako działania projektów.</span><span class="sxs-lookup"><span data-stu-id="b398e-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b398e-127">Wymagania wstępne i ustawienia mapowania</span><span class="sxs-lookup"><span data-stu-id="b398e-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="b398e-128">Przed synchronizacją zadań projektu należy zsynchronizować umowy dotyczące projektów i projekty.</span><span class="sxs-lookup"><span data-stu-id="b398e-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="b398e-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="b398e-129">Power Query</span></span>

<span data-ttu-id="b398e-130">Aby filtrować dane po spełnieniu tego warunku, należy użyć programu Microsoft Power Query dla programu Excel.</span><span class="sxs-lookup"><span data-stu-id="b398e-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="b398e-131">W zadaniu projektu są rekordy specyficzne dla zasobów.</span><span class="sxs-lookup"><span data-stu-id="b398e-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="b398e-132">Jeśli konieczne jest użycie Power Query, wykonaj następujące wytyczne:</span><span class="sxs-lookup"><span data-stu-id="b398e-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="b398e-133">Szablon Zadania projektu (PSA do Fin and Ops) zawiera domyślny filtr, który wyklucza rekordy specyficzne dla zasobów z zadania projektu, ustawiając filtr na **IsLineTask** jako **False**.</span><span class="sxs-lookup"><span data-stu-id="b398e-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="b398e-134">W przypadku utworzenia własnego szablonu należy dodać ten filtr.</span><span class="sxs-lookup"><span data-stu-id="b398e-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b398e-135">Mapowanie szablonów w integracji danych</span><span class="sxs-lookup"><span data-stu-id="b398e-135">Template mapping in Data integration</span></span>

<span data-ttu-id="b398e-136">Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych.</span><span class="sxs-lookup"><span data-stu-id="b398e-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="b398e-137">Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="b398e-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b398e-138">[![Mapowanie szablonu](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="b398e-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]