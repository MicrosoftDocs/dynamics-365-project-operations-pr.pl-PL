---
title: Skonfiguruj zasoby projektu
description: W tym temacie zamieszczono informacje dotyczące ustalania lub żądania zasobów w ramach projektu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997704"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="9ec53-103">Skonfiguruj zasoby projektu</span><span class="sxs-lookup"><span data-stu-id="9ec53-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ec53-104">Należy skonfigurować kalendarz i skojarzyć go z pracownikiem lub robotnikiem.</span><span class="sxs-lookup"><span data-stu-id="9ec53-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="9ec53-105">Kalendarz jest używany do zaplanowania projektu i czasu pracy zasobów, które są zarezerwowane dla projektu.</span><span class="sxs-lookup"><span data-stu-id="9ec53-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="9ec53-106">Podczas konfigurowania kalendarza kierownicy projektów mogą przeprowadzać bilansowanie zasobów w ramach optymalizacji zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ec53-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="9ec53-107">Na podstawie harmonogramu kalendarza można przystąpić do umieszczania ograniczeń zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ec53-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="9ec53-108">Kalendarz można skonfigurować na stronie **Kalendarze**.</span><span class="sxs-lookup"><span data-stu-id="9ec53-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="9ec53-109">Po skonfigurowaniu pracownika jako zasobu projektu możesz wybrać spośród pracowników pracujących w firmie, dla której konfigurujesz zasoby.</span><span class="sxs-lookup"><span data-stu-id="9ec53-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="9ec53-110">Alternatywnie można wybrać pracowników z innych firm należących do organizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec53-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="9ec53-111">Ci pracownicy są określani jako zasoby międzyfirmowe.</span><span class="sxs-lookup"><span data-stu-id="9ec53-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="9ec53-112">Poniższe procedury wyjaśniają, jak skonfigurować pracownika jako zasób projektu w firmie i jak skonfigurować zasób projektu międzyfirmowego.</span><span class="sxs-lookup"><span data-stu-id="9ec53-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="9ec53-113">Konfigurowanie pracownika jako zasobu projektu</span><span class="sxs-lookup"><span data-stu-id="9ec53-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="9ec53-114">Na stronie **Pracownicy** na liście **Pracownicy** wybierz pracownika, który ma być dodawany jako zasób projektu, i otwórz rekord pracownika.</span><span class="sxs-lookup"><span data-stu-id="9ec53-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="9ec53-115">W okienku akcji wybierz **Projekt** &gt; **Ustawienia** &gt; **Ustawienia projektu**.</span><span class="sxs-lookup"><span data-stu-id="9ec53-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="9ec53-116">Zaznacz kalendarz i zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9ec53-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="9ec53-117">Można również określić domyślne projekty zasobu jako typ przypisywania wstępnego.</span><span class="sxs-lookup"><span data-stu-id="9ec53-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="9ec53-118">Przypisań wstępnych można użyć, gdy menedżer zasobów lub kierownik projektu wie z wyprzedzeniem, nad którymi projektami będzie pracował zasób.</span><span class="sxs-lookup"><span data-stu-id="9ec53-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="9ec53-119">Przypisania wstępne mogą być również oparte na żądaniu sponsora lub klienta projektu.</span><span class="sxs-lookup"><span data-stu-id="9ec53-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="9ec53-120">Aby wstępnie przydzielić projekt, na stronie **Przypisywanie projektów**, na karcie **Projekty**, na liście **Pozostałe projekty** wybierz odpowiedni projekt.</span><span class="sxs-lookup"><span data-stu-id="9ec53-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="9ec53-121">Konfigurowanie zasobu międzyfirmowego</span><span class="sxs-lookup"><span data-stu-id="9ec53-121">Set up an intercompany resource</span></span>

<span data-ttu-id="9ec53-122">W przypadku konfigurowania pracownika jako zasobu międzyfirmowego należy przeprowadzić konfigurację zarówno w firmie pożyczającej, jak i firmie pożyczającej.</span><span class="sxs-lookup"><span data-stu-id="9ec53-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="9ec53-123">W firmie pożyczkowej</span><span class="sxs-lookup"><span data-stu-id="9ec53-123">In the lending company</span></span>

1. <span data-ttu-id="9ec53-124">W Finance sprawdź, czy wybrano firmę pożyczkową, a następnie wykonaj procedurę opisaną w poprzedniej sekcji „Konfigurowanie pracownika jako zasobu projektu”.</span><span class="sxs-lookup"><span data-stu-id="9ec53-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="9ec53-125">Na stronie **Księgowość międzyfirmowa** kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="9ec53-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="9ec53-126">W polu **Identyfikator firmy** wybierz firmę pożyczkową.</span><span class="sxs-lookup"><span data-stu-id="9ec53-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="9ec53-127">Wypełnij odpowiednio pozostałe pola, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="9ec53-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="9ec53-128">Na stronie **Cena przeniesienia** kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="9ec53-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="9ec53-129">W polu **Firma pożyczająca** wybierz odpowiednią firmę.</span><span class="sxs-lookup"><span data-stu-id="9ec53-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="9ec53-130">Aby pożyczyć firmie pożyczającej tylko zasób utworzony na początku tej sekcji, w polu **Zasób** wybierz nazwę utworzonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ec53-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="9ec53-131">Aby udostępnić wszystkim zasobom w firmie wypożyczanie spółce zażyczania, pole **Zasobu** powinno pozostać puste.</span><span class="sxs-lookup"><span data-stu-id="9ec53-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="9ec53-132">Na stronie **Parametry Zarządzanie projektami i księgowanie** na karcie **Międzyfirmowe** ustaw opcję **Włącz Międzyfirmowe planowanie zasobów i grafiki** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="9ec53-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="9ec53-133">W firmie pożyczającej</span><span class="sxs-lookup"><span data-stu-id="9ec53-133">In the borrowing company</span></span>

- <span data-ttu-id="9ec53-134">Na stronie **Lista zasobów** w filtrze wyszukiwania wprowadź nazwę zasobu utworzonego dla firmy służącej do wypożyczania, aby sprawdzić, czy nazwa znajduje się na liście zasobów dla firmy, która jest pożyczana.</span><span class="sxs-lookup"><span data-stu-id="9ec53-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="9ec53-135">Żądanie zasobów projektu</span><span class="sxs-lookup"><span data-stu-id="9ec53-135">Request project resources</span></span>
<span data-ttu-id="9ec53-136">Funkcjonalność planowania zasobów projektu pozwala tylko menedżerom zasobów na dystrybucję zasobów personelu w ramach zleceń lub projektów.</span><span class="sxs-lookup"><span data-stu-id="9ec53-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="9ec53-137">Aby włączyć tę funkcję, należy wykonać następujące zadania lub sprawdzić, czy zostały wykonane:</span><span class="sxs-lookup"><span data-stu-id="9ec53-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="9ec53-138">Konfigurowanie sekwencji numerów.</span><span class="sxs-lookup"><span data-stu-id="9ec53-138">Set up number sequences.</span></span>
- <span data-ttu-id="9ec53-139">Konfigurowanie przepływu pracy dotyczącego zarządzania projektami i księgowań.</span><span class="sxs-lookup"><span data-stu-id="9ec53-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="9ec53-140">Włączanie przepływu pracy żądania zasobu.</span><span class="sxs-lookup"><span data-stu-id="9ec53-140">Enable resource request workflows.</span></span>

<span data-ttu-id="9ec53-141">Po wykonaniu powyższych czynności można wykonać następujące zadania, które są wymagane:</span><span class="sxs-lookup"><span data-stu-id="9ec53-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="9ec53-142">Utwórz zlecenie zasobu na podstawie wstępnie zarezerwowanego zasobu pracowniczego.</span><span class="sxs-lookup"><span data-stu-id="9ec53-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="9ec53-143">Monitoruj żądania zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ec53-143">Monitor resource requests.</span></span>
- <span data-ttu-id="9ec53-144">Realizowanie żądań zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ec53-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="9ec53-145">Zażądanie zasobu pracowniczego z SPP.</span><span class="sxs-lookup"><span data-stu-id="9ec53-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="9ec53-146">Zarezerwuj zasoby do projektu bez żądania zasobu pracowniczego.</span><span class="sxs-lookup"><span data-stu-id="9ec53-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]