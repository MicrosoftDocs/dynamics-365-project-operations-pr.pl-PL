---
title: Nowości i zmiany w Project Service Automation, wydanie 22, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w Project Service Automation, aktualizacja 22, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150996"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="1a81d-103">Project Service Automation, wydanie 22, wer. 3</span><span class="sxs-lookup"><span data-stu-id="1a81d-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1a81d-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1a81d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1a81d-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="1a81d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1a81d-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1a81d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1a81d-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="1a81d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1a81d-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1a81d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1a81d-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w Project Service Automation, wer. 3, aktualizacja 22.</span><span class="sxs-lookup"><span data-stu-id="1a81d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="1a81d-110">Ta wersja ma numer kompilacji wer. 3.10.33.48 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w czerwcu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="1a81d-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="1a81d-111">Wydanie 22</span><span class="sxs-lookup"><span data-stu-id="1a81d-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1a81d-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="1a81d-112">Bug fixes</span></span>



<span data-ttu-id="1a81d-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="1a81d-113">**Time and Expense**</span></span>

<span data-ttu-id="1a81d-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="1a81d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1a81d-115">**Wpisy czasu** nie są automatycznie dodawane do harmonogramu wpisów godzin po zaimportowaniu.</span><span class="sxs-lookup"><span data-stu-id="1a81d-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="1a81d-116">Selektor dat siatki **Wpisów czasu** nie rozpoznaje ustawień regionalnych użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a81d-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="1a81d-117">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="1a81d-117">**Resource Management**</span></span>

<span data-ttu-id="1a81d-118">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="1a81d-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="1a81d-119">W trybie ręcznym zmiany rozkładu **Przydziału zasobu** nie są rozpoznawane przy generowaniu **Wymagań dotyczących zasobów**.</span><span class="sxs-lookup"><span data-stu-id="1a81d-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="1a81d-120">**Żądania zasobów** nie obsługują niestandardowych stanów żądań.</span><span class="sxs-lookup"><span data-stu-id="1a81d-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="1a81d-121">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="1a81d-121">**Project Management**</span></span>

<span data-ttu-id="1a81d-122">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="1a81d-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="1a81d-123">Korzystanie z dwukrotnego kliknięcia opcji EstimateGridControl nie spowoduje zaprogramowania poprawnie analizy liczb w formacie holenderskim.</span><span class="sxs-lookup"><span data-stu-id="1a81d-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="1a81d-124">Przypisane godziny nie są poprawnie aktualizowane, gdy przydziały są zmieniane za pomocą dodatku klienta klasycznego Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="1a81d-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="1a81d-125">Siatki śledzenia projektu i szacowania wyświetlają niepoprawny kod waluty sprzedaży, gdy waluta umowy jest inna niż waluta klienta, a organizacja jest skonfigurowana do wyświetlania kodów walut zamiast symboli walut.</span><span class="sxs-lookup"><span data-stu-id="1a81d-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="1a81d-126">Data zakończenia członka zespołu doda jeden dzień, jeśli harmonogram godzin pracy wynosi 24 godziny na dobę.</span><span class="sxs-lookup"><span data-stu-id="1a81d-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="1a81d-127">W harmonogramie projektu dodanie kategorii transakcji do zadania nie powoduje uruchomienia automatycznego zapisu.</span><span class="sxs-lookup"><span data-stu-id="1a81d-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="1a81d-128">Podczas dodawania członka zespołu do szablonu projektu wyświetlany jest następujący błąd: „Wymagania dotyczące zasobów nie mogą być powiązane z szablonami projektu”.</span><span class="sxs-lookup"><span data-stu-id="1a81d-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="1a81d-129">Skrypt reguły wstążki „msdyn.Approval.CanApproveOrReject” wyświetla błąd przekroczenia limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="1a81d-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="1a81d-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1a81d-130">**Sales**</span></span>

<span data-ttu-id="1a81d-131">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="1a81d-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="1a81d-132">Komunikat o błędzie walidacji nie jest wyświetlany, gdy cennik kosztów jest wybrany w wyszukiwaniu cennika w formularzu / encji „Nowy cennik projektu oferty”.</span><span class="sxs-lookup"><span data-stu-id="1a81d-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="1a81d-133">Zamknięcie oferty jako wygranej nie powoduje przejścia do utworzonego kontraktu, jeśli BPF dołączony do oferty jest na ostatnim etapie.</span><span class="sxs-lookup"><span data-stu-id="1a81d-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="1a81d-134">Wycofanie **Niezafakturowanej sprzedaży** jest powiązane z oryginalnym kosztem po odwołaniu wpisu czasu.</span><span class="sxs-lookup"><span data-stu-id="1a81d-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="1a81d-135">Po wybraniu przycisku **Potwierdź** status faktury nie zmieni się na **Potwierdzony**, chyba że faktura jest odświeżana.</span><span class="sxs-lookup"><span data-stu-id="1a81d-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
