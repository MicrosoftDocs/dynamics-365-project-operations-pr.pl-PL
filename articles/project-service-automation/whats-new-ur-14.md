---
title: Nowości i zmiany w programie Project Service Automation, wydanie 14, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 14, wer. 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754324"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="85607-103">Project Service Automation, wer. 3, wydanie 14</span><span class="sxs-lookup"><span data-stu-id="85607-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="85607-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="85607-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="85607-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="85607-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="85607-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="85607-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="85607-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="85607-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="85607-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="85607-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="85607-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 14.</span><span class="sxs-lookup"><span data-stu-id="85607-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="85607-110">Numer tej kompilacji to 3.10.4.21 i jest on dostępny w następującym harmonogramie:</span><span class="sxs-lookup"><span data-stu-id="85607-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="85607-111">**Powszechne udostępnienie (samoaktualizacja):** styczeń 2020</span><span class="sxs-lookup"><span data-stu-id="85607-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="85607-112">**Automatyczna aktualizacja:** luty 2020</span><span class="sxs-lookup"><span data-stu-id="85607-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="85607-113">Wydanie 14</span><span class="sxs-lookup"><span data-stu-id="85607-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="85607-114">Ulepszenia</span><span class="sxs-lookup"><span data-stu-id="85607-114">Enhancements</span></span>

- <span data-ttu-id="85607-115">Sales</span><span class="sxs-lookup"><span data-stu-id="85607-115">Sales</span></span>

     - <span data-ttu-id="85607-116">Wartości pól niestandardowych z **Szczegóły wiersza oferty** są kopiowane do **Szczegóły wiersza kontraktu projektu** podczas aktualizowania oferty do **Zamknięta jako wykorzystana**.</span><span class="sxs-lookup"><span data-stu-id="85607-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="85607-117">Potwierdzone projekty można **Zamknąć jako utracone**.</span><span class="sxs-lookup"><span data-stu-id="85607-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="85607-118">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="85607-118">Resource Management</span></span>

     - <span data-ttu-id="85607-119">Podczas rozszerzania rezerwacji użytkownicy będą proszeni o potwierdzenie, aby podsumować wyniki rezerwacji i podać łącze do obsługi rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="85607-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="85607-120">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="85607-120">Bug fixes</span></span>

- <span data-ttu-id="85607-121">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="85607-121">Time and Expense</span></span>

     - <span data-ttu-id="85607-122">Poprawione: udoskonalony sposób pracy użytkownika, jeśli użytkownik nie wybrał żadnych wpisów do skorygowania.</span><span class="sxs-lookup"><span data-stu-id="85607-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="85607-123">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="85607-123">Resource Management</span></span>

     - <span data-ttu-id="85607-124">Stałe: wielokrotna rezerwacja zasobu przepełnia nazwę rezerwowanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="85607-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="85607-125">Sales</span><span class="sxs-lookup"><span data-stu-id="85607-125">Sales</span></span>

     - <span data-ttu-id="85607-126">Ustalone: Łączna cena sprzedaży nie jest obliczana, dopóki użytkownik nie wprowadzi kosztu własnego dla oszacowania kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="85607-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="85607-127">Naprawione: zamknięcie oferty jako **wykorzystanej** kończy się niepowodzeniem, jeśli skojarzony kontrakt dotyczący projektu nie znajduje się w stanie **roboczym**.</span><span class="sxs-lookup"><span data-stu-id="85607-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

