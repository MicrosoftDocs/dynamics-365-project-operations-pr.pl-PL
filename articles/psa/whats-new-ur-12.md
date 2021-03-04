---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 12, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 12, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143841"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="60414-103">Project Service Automation, wydanie 12, wer. 3</span><span class="sxs-lookup"><span data-stu-id="60414-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="60414-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="60414-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="60414-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="60414-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="60414-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="60414-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="60414-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="60414-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="60414-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="60414-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="60414-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 14.</span><span class="sxs-lookup"><span data-stu-id="60414-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="60414-110">Numer tej kompilacji to V3.10.2.34 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w październiku 2019.</span><span class="sxs-lookup"><span data-stu-id="60414-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="60414-111">Wydanie 12</span><span class="sxs-lookup"><span data-stu-id="60414-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="60414-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="60414-112">Bug fixes</span></span>

- <span data-ttu-id="60414-113">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="60414-113">Time and Expense</span></span>

    - <span data-ttu-id="60414-114">Naprawione: błąd zapisu godziny został zaktualizowany w celu uzyskania odpowiedniego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="60414-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="60414-115">Naprawione: Siatka wprowadzania godziny i harmonogram poprawnie wyświetlają pasek przewijania w pionie, gdy to konieczne.</span><span class="sxs-lookup"><span data-stu-id="60414-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="60414-116">Naprawione: przesłane wpisy wydatków i czasu mogą być zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="60414-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="60414-117">Naprawione: okno dialogowe anulowania zatwierdzania zostało poprawione w celu odzwierciedlenia stanu zatwierdzenia po zmianie z **zatwierdzonego** na **przesłane**.</span><span class="sxs-lookup"><span data-stu-id="60414-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="60414-118">Naprawione: pola **Cena**, **Jednostka** i **ilość** są teraz zablokowane w rekordzie wydatków po jego zatwierdzeniu.</span><span class="sxs-lookup"><span data-stu-id="60414-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="60414-119">Zarządzanie projektem</span><span class="sxs-lookup"><span data-stu-id="60414-119">Project Management</span></span>

    - <span data-ttu-id="60414-120">Naprawione: Czynność **Nowe** w głównym formularzu **członka zespołu** została usunięta.</span><span class="sxs-lookup"><span data-stu-id="60414-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="60414-121">Naprawione: przydziały zasobów zostały zaktualizowane w celu brania pod uwagę niedokładnych błędów zaokrąglania, które prowadzą do zmiany daty zakończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="60414-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="60414-122">Naprawione: w siatce zadań powiązane błędy po stronie serwera zostaną ukazane użytkownikowi.</span><span class="sxs-lookup"><span data-stu-id="60414-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="60414-123">Naprawione: Nazwa członka zespołu jest teraz renderowana w selektorze osób zadania zamiast nazwy pozycji.</span><span class="sxs-lookup"><span data-stu-id="60414-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="60414-124">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="60414-124">Resource Management</span></span>

    - <span data-ttu-id="60414-125">Naprawione: szczegóły wymagania dotyczące zasobów dla projektów utworzonych na podstawie szablonu są realizowane za pomocą kalendarza projektu.</span><span class="sxs-lookup"><span data-stu-id="60414-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="60414-126">Naprawione: umiejętności i kompetencje są obecnie domyślne na podstawie danych głównych ról w zapotrzebowaniu na zasoby utworzonemu dla tej roli.</span><span class="sxs-lookup"><span data-stu-id="60414-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="60414-127">Sales</span><span class="sxs-lookup"><span data-stu-id="60414-127">Sales</span></span>

    - <span data-ttu-id="60414-128">Naprawione: w formularzu **głównym kontraktu** znaleziono zduplikowane identyfikatory obiektów.</span><span class="sxs-lookup"><span data-stu-id="60414-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="60414-129">Naprawione: logika została zaktualizowana tak, by karta **Analiza oferty** była wyświetlana w celu ukazania konfiguracji metadanych karty.</span><span class="sxs-lookup"><span data-stu-id="60414-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="60414-130">Naprawione: Data księgowania w aktualnym rekordzie zaczyna się od daty wprowadzenia godzin/wydatku, a nie daty zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="60414-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
