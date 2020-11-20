---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 15, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 15, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 2112e70d7359e7f30725ef3069a18570da651c06
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119926"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="35003-103">Project Service Automation, wydanie 15, wer. 3</span><span class="sxs-lookup"><span data-stu-id="35003-103">Project Service Automation Update Release 15, V3</span></span>

<span data-ttu-id="35003-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="35003-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="35003-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="35003-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="35003-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="35003-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="35003-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="35003-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="35003-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="35003-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="35003-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 15.</span><span class="sxs-lookup"><span data-stu-id="35003-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="35003-110">Numer tej kompilacji to V3.10.5.28 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="35003-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="35003-111">Wydanie 15</span><span class="sxs-lookup"><span data-stu-id="35003-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="35003-112">Ulepszenia</span><span class="sxs-lookup"><span data-stu-id="35003-112">Enhancements</span></span>

- <span data-ttu-id="35003-113">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="35003-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="35003-114">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="35003-114">Bug fixes</span></span>

- <span data-ttu-id="35003-115">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="35003-115">Time and Expense</span></span>

  - <span data-ttu-id="35003-116">Naprawione: dodanie obsługi błędów podczas wczytywania w widoku uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="35003-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="35003-117">Naprawione: Centrum zasobów projektu: zmiana nazwy **kwoty** w celu zmniejszenia niejednoznaczności.</span><span class="sxs-lookup"><span data-stu-id="35003-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="35003-118">Naprawione: Dopasowanie widoku **kolumn wpisu czasu kopiowania**, aby zawierały typ.</span><span class="sxs-lookup"><span data-stu-id="35003-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="35003-119">Naprawione: czas trwania edycji czasu w widoku siatki za pomocą liczb dziesiętnych powoduje nieznane błędy w przypadku niektórych liczb.</span><span class="sxs-lookup"><span data-stu-id="35003-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="35003-120">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="35003-120">Project Management</span></span>

  - <span data-ttu-id="35003-121">Naprawione: menu rozwijane **użyj w widoku śledzenia** jest teraz rozwijane w zależności od szerokości opcji.</span><span class="sxs-lookup"><span data-stu-id="35003-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="35003-122">Naprawione: podczas zarządzania projektami w strefie czasowej +13 obliczenia zadań mogą wyświetlać niedokładne wyniki.</span><span class="sxs-lookup"><span data-stu-id="35003-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="35003-123">Naprawione: **czas zakończenia członka zespołu** został poprawiony podczas korzystania z kalendarza 24-godzinnego.</span><span class="sxs-lookup"><span data-stu-id="35003-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="35003-124">Naprawione: ponownie aktywowany **BPF** w formularzu głównym **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="35003-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="35003-125">Naprawione: obliczenie przypisań nie ignoruje już jednego dnia.</span><span class="sxs-lookup"><span data-stu-id="35003-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="35003-126">Naprawione: do formularza projektu został dodany nowy transparent powiadomień, gdy strefa czasowa różni się między użytkownikiem i projektem.</span><span class="sxs-lookup"><span data-stu-id="35003-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="35003-127">Sales</span><span class="sxs-lookup"><span data-stu-id="35003-127">Sales</span></span>

  - <span data-ttu-id="35003-128">Naprawione: Wyszukiwanie wg kategorii oszacowania kosztów może służyć do filtrowania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="35003-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="35003-129">Naprawione: kod w **PluginDomain.ExecuteInTryCatchBlock(..)** nie ukrywa już źródła wyjątku.</span><span class="sxs-lookup"><span data-stu-id="35003-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="35003-130">Naprawione: Komunikat błędu w **Wyszukiwaniu projektu** w formularzu **Wiersz oferty** nie pojawia się, gdy wprowadzono ponad 1000 projektów.</span><span class="sxs-lookup"><span data-stu-id="35003-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="35003-131">Naprawione: Siatka **Szacowane** dla oszacowań robocizny i oszacowań kosztów powoduje wyświetlenie poprawnego symbolu waluty.</span><span class="sxs-lookup"><span data-stu-id="35003-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="35003-132">Naprawione: po zaktualizowaniu PSA przez organizację z wydania 14 do wydania 15 karta **Harmonogram** nie pojawia się pusty w formularzu **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="35003-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
