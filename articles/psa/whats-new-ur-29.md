---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 29, wer. V3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 29, wersja V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948667"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="72102-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 29, wer. V3</span><span class="sxs-lookup"><span data-stu-id="72102-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="72102-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="72102-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="72102-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="72102-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="72102-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="72102-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="72102-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="72102-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="72102-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="72102-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="72102-109">W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 29.</span><span class="sxs-lookup"><span data-stu-id="72102-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="72102-110">Ta wersja ma numer kompilacji V3.10.47.7 i jest ogólnie dostępna za pośrednictwem samodzielnej aktualizacji w lutym 2021 r.</span><span class="sxs-lookup"><span data-stu-id="72102-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="72102-111">Wydanie 29</span><span class="sxs-lookup"><span data-stu-id="72102-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="72102-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="72102-112">Bug fixes</span></span>

<span data-ttu-id="72102-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="72102-113">**Time and Expense**</span></span>

<span data-ttu-id="72102-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="72102-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="72102-115">Użytkownicy nie widzą godzin pracy zalogowanych w dniach wolnych od pracy w siatce wprowadzania czasu.</span><span class="sxs-lookup"><span data-stu-id="72102-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="72102-116">Zatwierdzone zapisy wydatków mogą być edytowane w siatce.</span><span class="sxs-lookup"><span data-stu-id="72102-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="72102-117">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="72102-117">**Project Management**</span></span>

<span data-ttu-id="72102-118">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="72102-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="72102-119">Brak logiki sprawdzania poprawności, w celu upewnienia się, że godziny nakładu pracy przypisania zasobów nie mogą być ujemne.</span><span class="sxs-lookup"><span data-stu-id="72102-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="72102-120">Akcja niestandardowa **AssignResourcesForTask** aktualizuje wszystkie pola, a nie tylko zmienione pola.</span><span class="sxs-lookup"><span data-stu-id="72102-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="72102-121">Podczas kopiowania projektu w środowisku z dodatkami lub przepływami pracy, które są zarejestrowane w zdarzeniu **CreateProject**, atrybut **msdyn_bulkgenerationstatus** nie jest aktualizowany, jeśli **CopyWBSToProject** nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="72102-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="72102-122">Po rozwinięciu kalendarza projektu dni robocze nie są sortowane w kolejności rosnącej, co powoduje niepowodzenie niektórych aktualizacji zadań projektu.</span><span class="sxs-lookup"><span data-stu-id="72102-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="72102-123">Zmiana menedżera projektu w istniejącym projekcie wyzwala logikę domyślnego działania jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="72102-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="72102-124">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="72102-124">**Sales**</span></span>

<span data-ttu-id="72102-125">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="72102-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="72102-126">Karta **Wydajność kontraktu** na stronie **Kontrakt** nie powiedzie się podczas inicjowania, gdy nie ma żadnych pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="72102-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>