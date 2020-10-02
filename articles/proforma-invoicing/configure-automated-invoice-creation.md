---
title: Konfigurowanie zautomatyzowanego tworzenia faktury
description: W tym temat zamieszczono informacje na temat pracy z systemem na żywo w celu automatycznego generowania faktur.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898139"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="d3c58-103">Konfigurowanie zautomatyzowanego tworzenia faktury</span><span class="sxs-lookup"><span data-stu-id="d3c58-103">Configure automated invoice creation</span></span>

<span data-ttu-id="d3c58-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="d3c58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d3c58-105">Wykonaj następujące kroki, aby skonfigurować zautomatyzowany przebieg fakturowania w Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d3c58-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="d3c58-106">Przejdź do **Ustawienia** \> **Zadania wsadowe**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="d3c58-107">Utwórz zadanie przetwarzania wsadowego i nazwij je **Tworzenie faktur w Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="d3c58-108">Nazwa zadania wsadowego musi zawierać termin „Tworzenie faktur”.</span><span class="sxs-lookup"><span data-stu-id="d3c58-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="d3c58-109">W polu **typ zadania** wybierz **Brak**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="d3c58-110">Domyślnie opcje **Częstotliwość dzienna** i **Jest aktywne** są ustawione na **Tak.**</span><span class="sxs-lookup"><span data-stu-id="d3c58-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="d3c58-111">Wybierz **Uruchom przepływ pracy**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-111">Select **Run Workflow**.</span></span> <span data-ttu-id="d3c58-112">W oknie dialogowym **wyszukiwania rekordu** zostaną wyświetlone trzy przepływy pracy:</span><span class="sxs-lookup"><span data-stu-id="d3c58-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="d3c58-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="d3c58-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="d3c58-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="d3c58-114">ProcessRunner</span></span>
    - <span data-ttu-id="d3c58-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="d3c58-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="d3c58-116">Wybierz **ProcessRunCaller**, a następnie wybierz opcję **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="d3c58-117">W następnym oknie dialogowym wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="d3c58-118">Po wykonaniu przepływu pracy **Uśpienie** następuje przepływ pracy **Proces**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="d3c58-119">Możesz również wybrać opcję **ProcessRunner** w kroku 5.</span><span class="sxs-lookup"><span data-stu-id="d3c58-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="d3c58-120">Następnie po wybraniu opcji **OK**przepływ pracy **Proces** jest zastępowany przepływem pracy **Uśpienie**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="d3c58-121">Przepływy pracy **ProcessRunCaller** i **ProcessRunner** tworzą faktury.</span><span class="sxs-lookup"><span data-stu-id="d3c58-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="d3c58-122">**ProcessRunCaller** wywołuje **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="d3c58-123">**ProcessRunner** to przepływ pracy, który w rzeczywistości tworzy faktury.</span><span class="sxs-lookup"><span data-stu-id="d3c58-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="d3c58-124">Przechodzi między wszystkimi pozycjami kontraktu, dla których muszą zostać utworzone faktury i tworzy faktury dla tych pozycji.</span><span class="sxs-lookup"><span data-stu-id="d3c58-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="d3c58-125">W celu określenia pozycji kontraktu, dla których mają zostać utworzone faktury, zadanie będzie znajdzie daty rozpoczęcia fakturowania w pozycjach kontraktu.</span><span class="sxs-lookup"><span data-stu-id="d3c58-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="d3c58-126">Jeśli pozycje kontraktu należące do jednego kontraktu mają taką samą datę rozpoczęcia fakturowania, transakcje zostaną połączone na jedną fakturę zawierającą dwa wiersze faktury.</span><span class="sxs-lookup"><span data-stu-id="d3c58-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="d3c58-127">W przypadku braku transakcji do utworzenia faktur dla zadania program pominie tworzenie faktur.</span><span class="sxs-lookup"><span data-stu-id="d3c58-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="d3c58-128">Kiedy **ProcessRunner** zakończy działanie, wywołuje **ProcessRunCaller**, dostarcza godzinę zakończenia i następuje zamknięcie.</span><span class="sxs-lookup"><span data-stu-id="d3c58-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="d3c58-129">**ProcessRunCaller** następnie uruchamia zegar, który trwa 24 godziny od określonego czasu końcowego.</span><span class="sxs-lookup"><span data-stu-id="d3c58-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="d3c58-130">Po upływie tego czasu program **ProcessRunCaller** jest zamknięty.</span><span class="sxs-lookup"><span data-stu-id="d3c58-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="d3c58-131">Zadanie przetwarzania wsadowego umożliwiającego tworzenie faktur jest zadaniem powtarzanym.</span><span class="sxs-lookup"><span data-stu-id="d3c58-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="d3c58-132">Jeśli ten proces wsadowy jest wykonywany wiele razy, system tworzy wiele wystąpień zadania i powoduje to wystąpienie błędów.</span><span class="sxs-lookup"><span data-stu-id="d3c58-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="d3c58-133">Z tego powodu proces przetwarzania wsadowego powinien być uruchamiany tylko raz. Aby uruchomić go tylko wtedy, gdy zakończy się jego działanie.</span><span class="sxs-lookup"><span data-stu-id="d3c58-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="d3c58-134">Fakturowanie wsadowe jest wykonywane tylko dla wierszy kontraktu projektu, które są konfigurowane przez harmonogramy faktur.</span><span class="sxs-lookup"><span data-stu-id="d3c58-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="d3c58-135">Pozycja kontraktu z metodą fakturowania przy stałej cenie musi mieć skonfigurowany punkt kontrolny.</span><span class="sxs-lookup"><span data-stu-id="d3c58-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="d3c58-136">Pozycja kontraktu projektu z metodą rozliczania czasu i materiału będzie wymagała konfiguracji harmonogramu fakturowania opartego na datach.</span><span class="sxs-lookup"><span data-stu-id="d3c58-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="d3c58-137">To samo dotyczy pozycji kontraktu opartej na projektach.</span><span class="sxs-lookup"><span data-stu-id="d3c58-137">The same applies to a project-based contract line.</span></span>     
