---
title: Skonfiguruj zasoby projektu
description: W tym temacie zamieszczono informacje dotyczące ustalania lub żądania zasobów w ramach projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082184"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="2a8c1-103">Skonfiguruj zasoby projektu</span><span class="sxs-lookup"><span data-stu-id="2a8c1-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a8c1-104">Należy skonfigurować kalendarz i skojarzyć go z pracownikiem lub robotnikiem.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="2a8c1-105">Kalendarz jest używany do zaplanowania projektu i czasu pracy zasobów, które są zarezerwowane dla projektu.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="2a8c1-106">Podczas konfigurowania kalendarza kierownicy projektów mogą przeprowadzać bilansowanie zasobów w ramach optymalizacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="2a8c1-107">Na podstawie harmonogramu kalendarza można przystąpić do umieszczania ograniczeń zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="2a8c1-108">Kalendarz można skonfigurować na stronie **Kalendarze**.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="2a8c1-109">Po skonfigurowaniu pracownika jako zasobu projektu możesz wybrać spośród pracowników pracujących w firmie, dla której konfigurujesz zasoby.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="2a8c1-110">Alternatywnie można wybrać pracowników z innych firm należących do organizacji.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="2a8c1-111">Ci pracownicy są określani jako zasoby międzyfirmowe.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="2a8c1-112">Poniższe procedury wyjaśniają, jak skonfigurować pracownika jako zasób projektu w firmie i jak skonfigurować zasób projektu międzyfirmowego.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="2a8c1-113">Konfigurowanie pracownika jako zasobu projektu</span><span class="sxs-lookup"><span data-stu-id="2a8c1-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="2a8c1-114">Na stronie **Pracownicy** na liście **Pracownicy** wybierz pracownika, który ma być dodawany jako zasób projektu, i otwórz rekord pracownika.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="2a8c1-115">W okienku akcji wybierz **Projekt** &gt; **Ustawienia** &gt; **Ustawienia projektu**.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="2a8c1-116">Zaznacz kalendarz i zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="2a8c1-117">Można również określić domyślne projekty zasobu jako typ przypisywania wstępnego.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="2a8c1-118">Przypisań wstępnych można użyć, gdy menedżer zasobów lub kierownik projektu wie z wyprzedzeniem, nad którymi projektami będzie pracował zasób.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="2a8c1-119">Przypisania wstępne mogą być również oparte na żądaniu sponsora lub klienta projektu.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="2a8c1-120">Aby wstępnie przydzielić projekt, na stronie **Przypisywanie projektów** , na karcie **Projekty** , na liście **Pozostałe projekty** wybierz odpowiedni projekt.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="2a8c1-121">Konfigurowanie zasobu międzyfirmowego</span><span class="sxs-lookup"><span data-stu-id="2a8c1-121">Set up an intercompany resource</span></span>

<span data-ttu-id="2a8c1-122">W przypadku konfigurowania pracownika jako zasobu międzyfirmowego należy przeprowadzić konfigurację zarówno w firmie pożyczającej, jak i firmie pożyczającej.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="2a8c1-123">W firmie pożyczkowej</span><span class="sxs-lookup"><span data-stu-id="2a8c1-123">In the lending company</span></span>

1. <span data-ttu-id="2a8c1-124">W Finance sprawdź, czy wybrano firmę pożyczkową, a następnie wykonaj procedurę opisaną w poprzedniej sekcji „Konfigurowanie pracownika jako zasobu projektu”.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="2a8c1-125">Na stronie **Księgowość międzyfirmowa** kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="2a8c1-126">W polu **Identyfikator firmy** wybierz firmę pożyczkową.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="2a8c1-127">Wypełnij odpowiednio pozostałe pola, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="2a8c1-128">Na stronie **Cena przeniesienia** kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="2a8c1-129">W polu **Firma pożyczająca** wybierz odpowiednią firmę.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="2a8c1-130">Aby pożyczyć firmie pożyczającej tylko zasób utworzony na początku tej sekcji, w polu **Zasób** wybierz nazwę utworzonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="2a8c1-131">Aby udostępnić wszystkim zasobom w firmie wypożyczanie spółce zażyczania, pole **Zasobu** powinno pozostać puste.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="2a8c1-132">Na stronie **Parametry Zarządzanie projektami i księgowanie** na karcie **Międzyfirmowe** ustaw opcję **Włącz Międzyfirmowe planowanie zasobów i grafiki** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="2a8c1-133">W firmie pożyczającej</span><span class="sxs-lookup"><span data-stu-id="2a8c1-133">In the borrowing company</span></span>

- <span data-ttu-id="2a8c1-134">Na stronie **Lista zasobów** w filtrze wyszukiwania wprowadź nazwę zasobu utworzonego dla firmy służącej do wypożyczania, aby sprawdzić, czy nazwa znajduje się na liście zasobów dla firmy, która jest pożyczana.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="2a8c1-135">Żądanie zasobów projektu</span><span class="sxs-lookup"><span data-stu-id="2a8c1-135">Request project resources</span></span>
<span data-ttu-id="2a8c1-136">Funkcjonalność planowania zasobów projektu pozwala tylko menedżerom zasobów na dystrybucję zasobów personelu w ramach zleceń lub projektów.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="2a8c1-137">Aby włączyć tę funkcję, należy wykonać następujące zadania lub sprawdzić, czy zostały wykonane:</span><span class="sxs-lookup"><span data-stu-id="2a8c1-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="2a8c1-138">Konfigurowanie sekwencji numerów.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-138">Set up number sequences.</span></span>
- <span data-ttu-id="2a8c1-139">Konfigurowanie przepływu pracy dotyczącego zarządzania projektami i księgowań.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="2a8c1-140">Włączanie przepływu pracy żądania zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-140">Enable resource request workflows.</span></span>

<span data-ttu-id="2a8c1-141">Po wykonaniu powyższych czynności można wykonać następujące zadania, które są wymagane:</span><span class="sxs-lookup"><span data-stu-id="2a8c1-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="2a8c1-142">Utwórz zlecenie zasobu na podstawie wstępnie zarezerwowanego zasobu pracowniczego.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="2a8c1-143">Monitoruj żądania zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-143">Monitor resource requests.</span></span>
- <span data-ttu-id="2a8c1-144">Realizowanie żądań zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="2a8c1-145">Zażądanie zasobu pracowniczego z SPP.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="2a8c1-146">Zarezerwuj zasoby do projektu bez żądania zasobu pracowniczego.</span><span class="sxs-lookup"><span data-stu-id="2a8c1-146">Book resources to a project without having a request for a staffed resource.</span></span>
