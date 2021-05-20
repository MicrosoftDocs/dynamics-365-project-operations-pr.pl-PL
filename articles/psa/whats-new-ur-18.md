---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 18, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 18, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: bd6038b3594e8507c4a441b00ddc2eb240f796dc
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949197"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="63b7b-103">Project Service Automation, wydanie 18, wer. 3</span><span class="sxs-lookup"><span data-stu-id="63b7b-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="63b7b-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="63b7b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="63b7b-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="63b7b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="63b7b-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="63b7b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="63b7b-107">Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="63b7b-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="63b7b-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="63b7b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="63b7b-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 18.</span><span class="sxs-lookup"><span data-stu-id="63b7b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="63b7b-110">Ta wersja ma numer kompilacji V3.10.8.12 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w kwietniu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="63b7b-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="63b7b-111">Wydanie 18</span><span class="sxs-lookup"><span data-stu-id="63b7b-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="63b7b-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="63b7b-112">Bug fixes</span></span>

<span data-ttu-id="63b7b-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="63b7b-113">**Time and Expense**</span></span>

- <span data-ttu-id="63b7b-114">Naprawione: Przepływy **Odwołaj**, **Żądaj** i **Anuluj zatwierdzenie** powodują wyjątki z niejasnymi komunikatami o błędach.</span><span class="sxs-lookup"><span data-stu-id="63b7b-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="63b7b-115">Naprawione: Kiedy **Anuluj zatwierdzenie** nie powiedzie się dla wydatku, nie jest wywoływany stosowny błąd wyjątku.</span><span class="sxs-lookup"><span data-stu-id="63b7b-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="63b7b-116">Naprawione: Siatka wpisu czasu nieprawidłowo obsługuje dni wolne od pracy w Australii po zmianie z czasu letniego (DST) w październiku.</span><span class="sxs-lookup"><span data-stu-id="63b7b-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="63b7b-117">Naprawione: Nieprawidłowa domyślna logika uniemożliwia przesłanie kosztów.</span><span class="sxs-lookup"><span data-stu-id="63b7b-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="63b7b-118">Naprawione: Kiedy zatwierdzanie zapisu czasu kończyło się niepowodzeniem, zatwierdzenie pozostało w stanie **Oczekującym**.</span><span class="sxs-lookup"><span data-stu-id="63b7b-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="63b7b-119">Naprawione: Błędy SQL w zatwierdzeniach zbiorczych (zakleszczenie/przekroczenie limitu czasu).</span><span class="sxs-lookup"><span data-stu-id="63b7b-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="63b7b-120">Naprawione: Znaczne problemy z wydajnością, które wynikają z aktualizowania członków zespołu podczas zatwierdzania wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="63b7b-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="63b7b-121">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="63b7b-121">**Project Management**</span></span>

- <span data-ttu-id="63b7b-122">Stałe: Powiadomienie strefy czasowej przeniesione z widoku **Uzgadnianie** do głównego formularza **Projektu**.</span><span class="sxs-lookup"><span data-stu-id="63b7b-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="63b7b-123">Naprawione: Szablon kalendarza nie jest poprawnie ustawiony jako domyślny po otwarciu nowego formularza projektu.</span><span class="sxs-lookup"><span data-stu-id="63b7b-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="63b7b-124">Naprawione: W przypadku przeglądarek opartych na chromium użytkownicy nie mogą łatwo wybrać zadań poprzedników do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="63b7b-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="63b7b-125">Naprawione: Tworzenie lub kopiowanie **Projektu z pustego szablonu** pobiera niepokrewne przypisania.</span><span class="sxs-lookup"><span data-stu-id="63b7b-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="63b7b-126">Naprawione: W określonych skrajnych przypadkach tworzenie nowego przypisania z siatki zadań powoduje utworzenie zduplikowanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="63b7b-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="63b7b-127">Naprawione: W trybie ręcznym użytkownicy nie mogą aktualizować dat rozpoczęcia zadania, tak aby były późniejsze niż bieżąca data zapisana.</span><span class="sxs-lookup"><span data-stu-id="63b7b-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="63b7b-128">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="63b7b-128">**Resource Management**</span></span>

- <span data-ttu-id="63b7b-129">Stałe: Wiersz podsumy widoku **Uzgodnienie** nieprawidłowo oblicza wariancję księgowania po rozszerzeniu księgowania.</span><span class="sxs-lookup"><span data-stu-id="63b7b-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="63b7b-130">Naprawione: Widok **uzgadniania** powoduje nieprawidłowe wyświetlenie przydziałów zasobów, gdy zasób obsługujący rezerwacje jest kalendarzem niezgodnym z kalendarzem projektu.</span><span class="sxs-lookup"><span data-stu-id="63b7b-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="63b7b-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="63b7b-131">**Sales**</span></span>

- <span data-ttu-id="63b7b-132">Naprawione: Czas ponownego zatwierdzania wpisów (**Zatwierdzanie > Anulowanie >** Ponowne zatwierdzanie) powoduje utworzenie zduplikowanych wartości rzeczywistych, które nie są odliczane.</span><span class="sxs-lookup"><span data-stu-id="63b7b-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]