---
title: Omówienie Project Service Automation
description: W tym temat zamieszczono informacje dotyczące Dynamics 365 Project Service Automation do integracji z rozwiązaniem Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005894"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="3d2e2-103">Omówienie Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3d2e2-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3d2e2-104">Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Dynamics 365 Finance i Dynamics 365 Project Service Automation za pośrednictwem Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="3d2e2-105">Szablony integracji, które są dostępne z funkcją integracji danych, umożliwiają przepływ projektów, umów dotyczących projektów, wierszy umów dotyczących projektów, punktów kontrolnych wierszy umów dotyczących projektów, zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych i szacunków wydatków z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3d2e2-106">Jeśli jest używany program version 7.3.0, należy zainstalować 4074835 KB.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="3d2e2-107">Następnie będzie można zintegrować projekty o stałej cenie.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="3d2e2-108">Jeśli używasz wersji 7.3.0 i przenosisz transakcje opłat z Project Service Automation, musisz zainstalować KB 4345320, aby uwzględnić te opłaty na fakturze za projekt.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="3d2e2-109">Jeśli używasz wersji 8.0, będziesz mógł korzystać z integracji zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych, szacunków wydatków i blokowania funkcji.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="3d2e2-110">Jeśli używasz wersji 8.0.1 lub nowszej, będziesz mieć możliwość synchronizacji danych rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="3d2e2-111">Przed integracją Project Service Automation Finance należy skonfigurować parametry integracji Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="3d2e2-112">Więcej informacji znajdziesz w [Parametry integracji usługi Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3d2e2-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="3d2e2-113">To rozwiązanie integracji umożliwia bezpośrednią synchronizację w następujących sytuacjach:</span><span class="sxs-lookup"><span data-stu-id="3d2e2-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="3d2e2-114">Utrzymuj kontrakty projektowe w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3d2e2-115">Twórz projekty w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3d2e2-116">Utrzymuj pozycje kontraktu w projekcie w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3d2e2-117">Utrzymuj punkty kontrolne pozycji kontraktu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3d2e2-118">Utrzymuj zadania projektu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3d2e2-119">Utrzymuj kategorie transakcji wydatków w Finance i synchronizuj je bezpośrednio z Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="3d2e2-120">Twórz oszacowania godzin projektu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3d2e2-121">Twórz oszacowania wydatków projektu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3d2e2-122">Twórz wartości rzeczywiste czasu, wydatków i opłat projektu w Project Service Automation i utwórz transakcje projektu w arkuszu integracji Project Service Automation, aby można je było zaksięgować w Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="3d2e2-123">Synchronizacja danych</span><span class="sxs-lookup"><span data-stu-id="3d2e2-123">Data synchronization</span></span>

<span data-ttu-id="3d2e2-124">Na poniższej ilustracji przedstawiono sposób synchronizowania danych w ramach integracji między Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="3d2e2-125">Nie wszystkie szablony są obecnie dostępne.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-125">Not all templates are currently available.</span></span> <span data-ttu-id="3d2e2-126">Szablony będą wydawane po zakończeniu.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="3d2e2-127">[![Integracja Project Service Automation z Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="3d2e2-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="3d2e2-128">Wymagania systemowe dotyczące Finance</span><span class="sxs-lookup"><span data-stu-id="3d2e2-128">System requirements for Finance</span></span>

<span data-ttu-id="3d2e2-129">Aby korzystać z rozwiązania integracji Project Service Automation z Finance, należy zainstalować wersję Enterprise Edition 7.3 z aktualizacją platformy 12 lub nowszą.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="3d2e2-130">Wymagania systemowe dla Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3d2e2-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="3d2e2-131">Aby użyć rozwiązania integracji Project Service Automation z Finance, należy zainstalować następujące składniki:</span><span class="sxs-lookup"><span data-stu-id="3d2e2-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="3d2e2-132">Dynamics 365 Project Service Automation wersja 9.0.0.0 lub nowsza</span><span class="sxs-lookup"><span data-stu-id="3d2e2-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="3d2e2-133">Rozwiązanie od potencjalnego klienta do otrzymania gotówki dla Dynamics 365 Sales w wersji 1.14.0.0 (v14) lub nowszej</span><span class="sxs-lookup"><span data-stu-id="3d2e2-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="3d2e2-134">Rozwiązanie Project Service Automation do Finance dla Dynamics 365 Project Service Automation w wersji 1.0.0.0 lub nowszej</span><span class="sxs-lookup"><span data-stu-id="3d2e2-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="3d2e2-135">Zainstaluj rozwiązanie integracji Project Service Automation z Finance w swoim wystąpieniu Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3d2e2-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="3d2e2-136">Pobierz rozwiązanie integracji Project Service Automation do Finance z [Centrum pobierania Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) i wykonaj instrukcje zawarte w rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="3d2e2-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]