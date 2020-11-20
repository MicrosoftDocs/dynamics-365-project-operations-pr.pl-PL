---
title: Parametry integracji Project Service Automation z Finance
description: W tym temacie wyjaśniono, jak skonfigurować sposób wprowadzania danych domyślnych podczas integracji Microsoft Dynamics 365 for Project Service Automation z Microsoft Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a0cee090e0ecb306aa3bda62c79a57dfade93c0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082152"
---
# <a name="project-service-automation-integration-parameters"></a><span data-ttu-id="d89b9-103">Parametry integracji Project Service Automation z Finance</span><span class="sxs-lookup"><span data-stu-id="d89b9-103">Project Service Automation integration parameters</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d89b9-104">Na stronie **parametry integracji rozwiązania Project Service Automation** można skonfigurować sposób wprowadzania danych domyślnych podczas integracji Dynamics 365 Project Service Automation z Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="d89b9-104">On the **Project Service Automation integration parameters** page, you can configure how default data is entered when you integrate Dynamics 365 Project Service Automation with Dynamics 365 Finance.</span></span> <span data-ttu-id="d89b9-105">Aby projekty zostały pomyślnie zsynchronizowane z Project Service Automation do Finance, należy skonfigurować następujące pola.</span><span class="sxs-lookup"><span data-stu-id="d89b9-105">For projects to be successfully synchronized from Project Service Automation to Finance, you must set up the following fields.</span></span>

<span data-ttu-id="d89b9-106">Aby otworzyć stronę **parametry integracji z Project Service Automation** , wybierz **Zarządzanie projektami i księgowanie** \> **Ustawienia** \> **Parametry integracji Dynamics 365 for Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="d89b9-106">To open the **Project Service Automation integration parameters** page, go to **Project management and accounting** \> **Setup** \> **Dynamics 365 for Project Service Automation integration parameters**.</span></span> 

> [!NOTE]
> - <span data-ttu-id="d89b9-107">W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.</span><span class="sxs-lookup"><span data-stu-id="d89b9-107">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="d89b9-108">Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="d89b9-108">Actuals integration is available in version 8.0.1 or later.</span></span>


| <span data-ttu-id="d89b9-109">Zakładka</span><span class="sxs-lookup"><span data-stu-id="d89b9-109">Tab</span></span>                    | <span data-ttu-id="d89b9-110">Pole</span><span class="sxs-lookup"><span data-stu-id="d89b9-110">Field</span></span>                | <span data-ttu-id="d89b9-111">Opis</span><span class="sxs-lookup"><span data-stu-id="d89b9-111">Description</span></span> |
|------------------------|----------------------|-------------|
| <span data-ttu-id="d89b9-112">Ogólne</span><span class="sxs-lookup"><span data-stu-id="d89b9-112">General</span></span>                | <span data-ttu-id="d89b9-113">Domyślny typ projektu</span><span class="sxs-lookup"><span data-stu-id="d89b9-113">Default project type</span></span> | <span data-ttu-id="d89b9-114">Wybierz domyślny typ projektu.</span><span class="sxs-lookup"><span data-stu-id="d89b9-114">Select the default project type.</span></span> <span data-ttu-id="d89b9-115">Jeśli projekty są synchronizowane z rozwiązania Project Service Automation, ta wartość jest używana, jeśli w szablonie integracji nie została wybrana wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="d89b9-115">When projects are synchronized from Project Service Automation, this value is used if you didn't provide a default value in the integration template.</span></span> <span data-ttu-id="d89b9-116">Podczas synchronizacji pole **Typ projektu** dla nowych projektów ma ustawioną tę wartość.</span><span class="sxs-lookup"><span data-stu-id="d89b9-116">During synchronization, the **Project type** field of new projects is set to this value.</span></span> <span data-ttu-id="d89b9-117">Jednak wartość może zostać zaktualizowana w momencie, gdy pozycje kontraktu projektu zostaną zsynchronizowane z rozwiązania Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d89b9-117">However, the value might be updated when the project contract lines are synchronized from Project Service Automation.</span></span> |
|                        | <span data-ttu-id="d89b9-118">Kategoria czasu</span><span class="sxs-lookup"><span data-stu-id="d89b9-118">Time category</span></span>        | <span data-ttu-id="d89b9-119">Wybierz domyślną kategorię czasową.</span><span class="sxs-lookup"><span data-stu-id="d89b9-119">Select the default time category.</span></span> <span data-ttu-id="d89b9-120">Ta wartość jest używana przy synchronizowaniu oszacowania godzinnego z rozwiązania Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d89b9-120">This value is used when hour estimates are synchronized from Project Service Automation.</span></span> <span data-ttu-id="d89b9-121">Kiedy wartości szacunkowe godzin i godzin są synchronizowane z rozwiązania Project Service Automation, pole **Kategoria** w nowych prognozach godzin projektów w Finance ma ustawioną tę wartość.</span><span class="sxs-lookup"><span data-stu-id="d89b9-121">When the hour estimates and hour actuals are synchronized from Project Service Automation, the **Category** field of new project hour forecasts in Finance is set to this value.</span></span> |
|                        | <span data-ttu-id="d89b9-122">Kategoria opłat</span><span class="sxs-lookup"><span data-stu-id="d89b9-122">Fee category</span></span>         | <span data-ttu-id="d89b9-123">Wybierz domyślną kategorię opłat.</span><span class="sxs-lookup"><span data-stu-id="d89b9-123">Select the default fee category.</span></span> <span data-ttu-id="d89b9-124">Ta wartość jest używana, gdy wartości rzeczywiste opłat są synchronizowane z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d89b9-124">This value is used when fee actuals are synchronized from Project Service Automation.</span></span> <span data-ttu-id="d89b9-125">Kiedy wartości rzeczywiste opłat i godzin są synchronizowane z rozwiązania Project Service Automation, pole **Kategoria** w nowych opłatach za transakcje w Finance ma ustawioną tę wartość.</span><span class="sxs-lookup"><span data-stu-id="d89b9-125">When the fee actuals are synchronized from Project Service Automation, the **Category** field of new fee transactions in Finance is set to this value.</span></span> |
| <span data-ttu-id="d89b9-126">Domyślne ustawienia grup projektów</span><span class="sxs-lookup"><span data-stu-id="d89b9-126">Project group defaults</span></span> | <span data-ttu-id="d89b9-127">Typ projektu</span><span class="sxs-lookup"><span data-stu-id="d89b9-127">Project type</span></span>         | <span data-ttu-id="d89b9-128">Kliknij pozycję **Nowy** , aby dodać wiersz, w którym można wybrać typ projektu, dla którego ma zostać ustawiona domyślna grupa projektów.</span><span class="sxs-lookup"><span data-stu-id="d89b9-128">Click **New** to add a row where you can select the project type to set the default project group for.</span></span> <span data-ttu-id="d89b9-129">Określony typ projektu może być wybierany w konfiguracji tylko raz.</span><span class="sxs-lookup"><span data-stu-id="d89b9-129">A specific project type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="d89b9-130">Grupa projektów</span><span class="sxs-lookup"><span data-stu-id="d89b9-130">Project group</span></span>        | <span data-ttu-id="d89b9-131">Wybierz grupę domyślnych projektów dla wybranego typu projektu.</span><span class="sxs-lookup"><span data-stu-id="d89b9-131">Select the default project group for the selected project type.</span></span> <span data-ttu-id="d89b9-132">Kiedy nowe projekty są synchronizowane z rozwiązania Project Service Automation, w polu **Grupa projektów** jest ustawiona wartość domyślna dla typu projektu, jeśli szablon integracji nie zawiera wartości domyślnej.</span><span class="sxs-lookup"><span data-stu-id="d89b9-132">When new projects are synchronized from Project Service Automation, the **Project group** field is set to the default value for the project type if you didn't provide a default value in the integration template.</span></span> |
| <span data-ttu-id="d89b9-133">Domyślne typy fakturowania</span><span class="sxs-lookup"><span data-stu-id="d89b9-133">Billing type defaults</span></span>  | <span data-ttu-id="d89b9-134">Typ rozliczania</span><span class="sxs-lookup"><span data-stu-id="d89b9-134">Billing type</span></span>         | <span data-ttu-id="d89b9-135">Kliknij opcję **Nowy** , aby dodać wiersz, w którym można wybrać typ rozliczenia, dla którego ustawić domyślną właściwość linii.</span><span class="sxs-lookup"><span data-stu-id="d89b9-135">Click **New** to add a row where you can select the billing type to set the default line property for.</span></span> <span data-ttu-id="d89b9-136">Określony typ rozliczenia można wybrać tylko raz w konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d89b9-136">A specific billing type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="d89b9-137">Właściwość wiersza</span><span class="sxs-lookup"><span data-stu-id="d89b9-137">Line property</span></span>        | <span data-ttu-id="d89b9-138">Wybierz domyślną właściwość linii dla wybranego typu rozliczenia.</span><span class="sxs-lookup"><span data-stu-id="d89b9-138">Select the default line property for the selected billing type.</span></span> <span data-ttu-id="d89b9-139">Gdy nowe szacunki godzinowe, nowe szacunki wydatków lub nowe wartości rzeczywiste są synchronizowane z Project Service Automation, pole **Właściwości wiersz** jest ustawiane na wartość domyślną dla typu rozliczenia.</span><span class="sxs-lookup"><span data-stu-id="d89b9-139">When new hour estimates, new expense estimates, or new actuals are synchronized from Project Service Automation, the **Line property** field is set to the default value for the billing type.</span></span> |
| <span data-ttu-id="d89b9-140">Blokowanie funkcjonalności</span><span class="sxs-lookup"><span data-stu-id="d89b9-140">Functionality locking</span></span>  | <span data-ttu-id="d89b9-141">Nie dotyczy</span><span class="sxs-lookup"><span data-stu-id="d89b9-141">Not applicable</span></span>       | <span data-ttu-id="d89b9-142">Wybierz funkcję do wyłączenia w Finance dla projektów i umów, które pochodzą z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d89b9-142">Select the functionality to disable in Finance for projects and contracts that originated from Project Service Automation.</span></span> <span data-ttu-id="d89b9-143">Na przykład można wyłączyć możliwość edytowania umów i projektów, tworzenia struktur podziału pracy i wprowadzania grafików pracy w Finance.</span><span class="sxs-lookup"><span data-stu-id="d89b9-143">For example, you can turn off the ability to edit contracts and projects, create work breakdown structures, and enter timesheets in Finance.</span></span> <span data-ttu-id="d89b9-144">Pola związane z księgowością będą nadal aktywne, nawet jeśli są niedostępne przez ustawienie parametru.</span><span class="sxs-lookup"><span data-stu-id="d89b9-144">Accounting-related fields will continue to be enabled, even if they are made unavailable by the parameter setting.</span></span> <span data-ttu-id="d89b9-145">Domyślnie wszystkie funkcje są włączone.</span><span class="sxs-lookup"><span data-stu-id="d89b9-145">By default, all functionality is enabled.</span></span> |