---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 14, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 14, wer. 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081970"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="a4f4a-103">Project Service Automation, wydanie 14, wer. 3</span><span class="sxs-lookup"><span data-stu-id="a4f4a-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="a4f4a-104">Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a4f4a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a4f4a-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a4f4a-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a4f4a-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a4f4a-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a4f4a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a4f4a-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 14.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="a4f4a-110">Numer tej kompilacji to 3.10.4.21 i jest on dostępny w następującym harmonogramie:</span><span class="sxs-lookup"><span data-stu-id="a4f4a-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="a4f4a-111">**Powszechne udostępnienie (samoaktualizacja):** styczeń 2020</span><span class="sxs-lookup"><span data-stu-id="a4f4a-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="a4f4a-112">**Automatyczna aktualizacja:** luty 2020</span><span class="sxs-lookup"><span data-stu-id="a4f4a-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="a4f4a-113">Wydanie 14</span><span class="sxs-lookup"><span data-stu-id="a4f4a-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="a4f4a-114">Ulepszenia</span><span class="sxs-lookup"><span data-stu-id="a4f4a-114">Enhancements</span></span>

- <span data-ttu-id="a4f4a-115">Sales</span><span class="sxs-lookup"><span data-stu-id="a4f4a-115">Sales</span></span>

     - <span data-ttu-id="a4f4a-116">Wartości pól niestandardowych z **Szczegóły wiersza oferty** są kopiowane do **Szczegóły wiersza kontraktu projektu** podczas aktualizowania oferty do **Zamknięta jako wykorzystana**.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="a4f4a-117">Potwierdzone projekty można **Zamknąć jako utracone**.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="a4f4a-118">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="a4f4a-118">Resource Management</span></span>

     - <span data-ttu-id="a4f4a-119">Podczas rozszerzania rezerwacji użytkownicy będą proszeni o potwierdzenie, aby podsumować wyniki rezerwacji i podać łącze do obsługi rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="a4f4a-120">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="a4f4a-120">Bug fixes</span></span>

- <span data-ttu-id="a4f4a-121">Czas i wydatek</span><span class="sxs-lookup"><span data-stu-id="a4f4a-121">Time and Expense</span></span>

     - <span data-ttu-id="a4f4a-122">Poprawione: udoskonalony sposób pracy użytkownika, jeśli użytkownik nie wybrał żadnych wpisów do skorygowania.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="a4f4a-123">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="a4f4a-123">Resource Management</span></span>

     - <span data-ttu-id="a4f4a-124">Stałe: wielokrotna rezerwacja zasobu przepełnia nazwę rezerwowanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="a4f4a-125">Sales</span><span class="sxs-lookup"><span data-stu-id="a4f4a-125">Sales</span></span>

     - <span data-ttu-id="a4f4a-126">Ustalone: Łączna cena sprzedaży nie jest obliczana, dopóki użytkownik nie wprowadzi kosztu własnego dla oszacowania kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="a4f4a-127">Naprawione: zamknięcie oferty jako **wykorzystanej** kończy się niepowodzeniem, jeśli skojarzony kontrakt dotyczący projektu nie znajduje się w stanie **roboczym**.</span><span class="sxs-lookup"><span data-stu-id="a4f4a-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

