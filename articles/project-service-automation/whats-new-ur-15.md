---
title: Nowości i zmiany w programie Project Service Automation, wydanie 15, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 15, wer. 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754323"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="6fab9-103">Project Service Automation, wer. 3, wydanie 15</span><span class="sxs-lookup"><span data-stu-id="6fab9-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="6fab9-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="6fab9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6fab9-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="6fab9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6fab9-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6fab9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6fab9-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="6fab9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6fab9-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6fab9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6fab9-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 15.</span><span class="sxs-lookup"><span data-stu-id="6fab9-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="6fab9-110">Numer tej kompilacji to V3.10.5.28 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="6fab9-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="6fab9-111">Wydanie 15</span><span class="sxs-lookup"><span data-stu-id="6fab9-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="6fab9-112">Ulepszenia</span><span class="sxs-lookup"><span data-stu-id="6fab9-112">Enhancements</span></span>

- <span data-ttu-id="6fab9-113">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="6fab9-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6fab9-114">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="6fab9-114">Bug fixes</span></span>

- <span data-ttu-id="6fab9-115">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="6fab9-115">Time and Expense</span></span>

  - <span data-ttu-id="6fab9-116">Naprawione: dodanie obsługi błędów podczas wczytywania w widoku uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="6fab9-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="6fab9-117">Naprawione: Centrum zasobów projektu: zmiana nazwy **kwoty** w celu zmniejszenia niejednoznaczności.</span><span class="sxs-lookup"><span data-stu-id="6fab9-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="6fab9-118">Naprawione: Dopasowanie widoku **kolumn wpisu czasu kopiowania**, aby zawierały typ.</span><span class="sxs-lookup"><span data-stu-id="6fab9-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="6fab9-119">Naprawione: czas trwania edycji czasu w widoku siatki za pomocą liczb dziesiętnych powoduje nieznane błędy w przypadku niektórych liczb.</span><span class="sxs-lookup"><span data-stu-id="6fab9-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="6fab9-120">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="6fab9-120">Project Management</span></span>

  - <span data-ttu-id="6fab9-121">Naprawione: menu rozwijane **użyj w widoku śledzenia** jest teraz rozwijane w zależności od szerokości opcji.</span><span class="sxs-lookup"><span data-stu-id="6fab9-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="6fab9-122">Naprawione: podczas zarządzania projektami w strefie czasowej +13 obliczenia zadań mogą wyświetlać niedokładne wyniki.</span><span class="sxs-lookup"><span data-stu-id="6fab9-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="6fab9-123">Naprawione: **czas zakończenia członka zespołu** został poprawiony podczas korzystania z kalendarza 24-godzinnego.</span><span class="sxs-lookup"><span data-stu-id="6fab9-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="6fab9-124">Naprawione: ponownie aktywowany **BPF** w formularzu głównym **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="6fab9-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="6fab9-125">Naprawione: obliczenie przypisań nie ignoruje już jednego dnia.</span><span class="sxs-lookup"><span data-stu-id="6fab9-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="6fab9-126">Naprawione: do formularza projektu został dodany nowy transparent powiadomień, gdy strefa czasowa różni się między użytkownikiem i projektem.</span><span class="sxs-lookup"><span data-stu-id="6fab9-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="6fab9-127">Sales</span><span class="sxs-lookup"><span data-stu-id="6fab9-127">Sales</span></span>

  - <span data-ttu-id="6fab9-128">Naprawione: Wyszukiwanie wg kategorii oszacowania kosztów może służyć do filtrowania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="6fab9-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="6fab9-129">Naprawione: kod w **PluginDomain.ExecuteInTryCatchBlock(..)** nie ukrywa już źródła wyjątku.</span><span class="sxs-lookup"><span data-stu-id="6fab9-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="6fab9-130">Naprawione: Komunikat błędu w **Wyszukiwaniu projektu** w formularzu **Wiersz oferty** nie pojawia się, gdy wprowadzono ponad 1000 projektów.</span><span class="sxs-lookup"><span data-stu-id="6fab9-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="6fab9-131">Naprawione: Siatka **Szacowane** dla oszacowań robocizny i oszacowań kosztów powoduje wyświetlenie poprawnego symbolu waluty.</span><span class="sxs-lookup"><span data-stu-id="6fab9-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="6fab9-132">Naprawione: po zaktualizowaniu PSA przez organizację z wydania 14 do wydania 15 karta **Harmonogram** nie pojawia się pusty w formularzu **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="6fab9-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
