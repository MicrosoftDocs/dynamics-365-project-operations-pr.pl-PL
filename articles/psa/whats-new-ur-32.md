---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 32, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 32, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129679"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="d57a3-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 32, wer. 3</span><span class="sxs-lookup"><span data-stu-id="d57a3-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d57a3-104">Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d57a3-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="d57a3-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="d57a3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d57a3-106">Jest ona kompatybilna z Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d57a3-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d57a3-107">Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="d57a3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="d57a3-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d57a3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d57a3-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 32.</span><span class="sxs-lookup"><span data-stu-id="d57a3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="d57a3-110">Ta wersja ma numer kompilacji wer. 3.10.53.108 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2021 r.</span><span class="sxs-lookup"><span data-stu-id="d57a3-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="d57a3-111">Wydanie 32</span><span class="sxs-lookup"><span data-stu-id="d57a3-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d57a3-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="d57a3-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="d57a3-113">Ogólne</span><span class="sxs-lookup"><span data-stu-id="d57a3-113">General</span></span>

- <span data-ttu-id="d57a3-114">W przypadku niepowodzenia poważnej aktualizacji należy zablokować tylko główne punkty wejścia do aplikacji, aby zapewnić, że współdzielone elementy są nadal dostępne.</span><span class="sxs-lookup"><span data-stu-id="d57a3-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="d57a3-115">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="d57a3-115">Time and Expense</span></span>

<span data-ttu-id="d57a3-116">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d57a3-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d57a3-117">**TimeEntriesImportFromResourceAssignment** nie zachowuje czasu rozpoczęcia i zakończenia wycinka konturu przydziału zasobów.</span><span class="sxs-lookup"><span data-stu-id="d57a3-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="d57a3-118">Wybór opcji **Otwórz wpis** w siatce **wprowadzania czasu** może uniemożliwić wybranie innych formularzy.</span><span class="sxs-lookup"><span data-stu-id="d57a3-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="d57a3-119">Podczas importowania zadań do wpisów czasu, zapytanie o kod klienta może wygenerować długi adres URL, który nie powiedzie się w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="d57a3-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="d57a3-120">Po usunięciu wartości z komórki w **siatce czasu** fokus nie pozostaje w siatce.</span><span class="sxs-lookup"><span data-stu-id="d57a3-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="d57a3-121">Przycisk **Odrzucanie** został usunięty z widoku **Przetwarzanie zatwierdzeń** dla nowych zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="d57a3-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="d57a3-122">Na stabilność i wydajność zbiorczego zatwierdzania wpisów czasu pracy mają wpływ martwe punkty i brak odpowiedniej obsługi dostosowań, które są związane z podmiotem **Wpis czasu**.</span><span class="sxs-lookup"><span data-stu-id="d57a3-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="d57a3-123">Planowanie projektu</span><span class="sxs-lookup"><span data-stu-id="d57a3-123">Project Planning</span></span>

- <span data-ttu-id="d57a3-124">Podczas aktualizacji projektu, który ma wartość null w polu **Jednostka kontraktująca**, generowany jest wyjątek odwołania do wartości null.</span><span class="sxs-lookup"><span data-stu-id="d57a3-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="d57a3-125">**Odświeżenie sumy projektu** w niepoprawny sposób oblicza pozostały koszt i pozostałą sprzedaż w projekcie.</span><span class="sxs-lookup"><span data-stu-id="d57a3-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="d57a3-126">Nadmiarowe obliczenia cenowe wpływają na wydajność związaną z aktualizacjami konturów przydziału zasobów.</span><span class="sxs-lookup"><span data-stu-id="d57a3-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="d57a3-127">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="d57a3-127">Resource Management</span></span>

<span data-ttu-id="d57a3-128">Naprawiono następujący problem:</span><span class="sxs-lookup"><span data-stu-id="d57a3-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="d57a3-129">Gdy pojemność kalendarza zasobu, który można zarezerwować jest większa niż 1, Project Service Automation błędnie rozpoznaje pojemność jako 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d57a3-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="d57a3-130">Dlatego w widoku harmonogramu pojawia się nieskończona pętla.</span><span class="sxs-lookup"><span data-stu-id="d57a3-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="d57a3-131">Sprzedaż</span><span class="sxs-lookup"><span data-stu-id="d57a3-131">Sales</span></span>

<span data-ttu-id="d57a3-132">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d57a3-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="d57a3-133">Gdy tworzona jest linia dziennika z niestandardowym typem transakcji, występuje następujący wyjątek null reference: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="d57a3-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="d57a3-134">Role i kategorie, które zostały dezaktywowane przed skopiowaniem oferty nie powinny być dodawane do ról i kategorii płatnych w nowo skopiowanej ofercie.</span><span class="sxs-lookup"><span data-stu-id="d57a3-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="d57a3-135">Data dokumentu i data księgowania nie są zgodne z datą początkową, która jest podawana na elemencie linii faktury, który jest tworzony bezpośrednio na projekcie faktury.</span><span class="sxs-lookup"><span data-stu-id="d57a3-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="d57a3-136">Wyjątki typu null reference generowane są w scenariuszach związanych z dezaktywacją ról i kategorii przed skopiowaniem oferty.</span><span class="sxs-lookup"><span data-stu-id="d57a3-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="d57a3-137">W akcji **Aktualizowanie cen** na stronie **Projekty** nie są aktualizowane szacowania wydatków i szacowania materiałowe.</span><span class="sxs-lookup"><span data-stu-id="d57a3-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
