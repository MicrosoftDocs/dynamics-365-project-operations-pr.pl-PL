---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 33, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 33, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334581"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="62827-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 33, wer. 3</span><span class="sxs-lookup"><span data-stu-id="62827-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="62827-104">Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="62827-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="62827-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="62827-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="62827-106">Jest ona kompatybilna z Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="62827-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="62827-107">Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="62827-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="62827-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="62827-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="62827-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 33.</span><span class="sxs-lookup"><span data-stu-id="62827-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="62827-110">Ta wersja zawiera numer kompilacji V3.10.54.98 i jest ogólnie dostępna w ramach samoobsługowej aktualizacji z lipca 2021 r.</span><span class="sxs-lookup"><span data-stu-id="62827-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="62827-111">Wydanie 33</span><span class="sxs-lookup"><span data-stu-id="62827-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="62827-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="62827-112">Bug fixes</span></span>

<span data-ttu-id="62827-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="62827-113">**Time and Expense**</span></span>

<span data-ttu-id="62827-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="62827-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="62827-115">Dwa zablokowane pola, **msdyn_description** i **msdyn_externaldescription**, można edytować po przesłaniu.</span><span class="sxs-lookup"><span data-stu-id="62827-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="62827-116">Jeśli zostanie utworzony koszt niepowiązany z projektem, pojawia się komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="62827-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="62827-117">Po utworzeniu wpisu czasu rola zasobu jest domyślnie ustawiana na rolę nieaktywną.</span><span class="sxs-lookup"><span data-stu-id="62827-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="62827-118">Wiersze arkusza skojarzone z wycofanym i usuniętym wydatkiem nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="62827-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="62827-119">W **formularzu szybkiego tworzenia wpisu czasu** zaktualizuj widok **Lista zadań projektu**, aby zmienić wyświetlaną domyślnie datę na datę rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="62827-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="62827-120">Podczas tworzenia wpisu czasu na karcie **Pokrewne** zasobu do zarezerwowania wpis czasu jest niepoprawnie tworzony dla zalogowanego użytkownika, zamiast nadrzędnego zasobu, który można zarezerwować.</span><span class="sxs-lookup"><span data-stu-id="62827-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="62827-121">Nowe pola zostaną dodane do okna dialogowego **zbiorczego zatwierdzania (MDD)**.</span><span class="sxs-lookup"><span data-stu-id="62827-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="62827-122">**Planowanie projektu**</span><span class="sxs-lookup"><span data-stu-id="62827-122">**Project planning**</span></span>

<span data-ttu-id="62827-123">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="62827-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="62827-124">Mała wydajność tworzenia projektów w przypadku stosowania szablonów godzin pracy projektu w złożonych kalendarzach.</span><span class="sxs-lookup"><span data-stu-id="62827-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="62827-125">Gdy data rozpoczęcia jest późniejsza niż data zakończenia, w szablonie kopii szablonu projektu jest wyświetlany błąd z powodu różnic w składniku czasowym poszczególnych pól.</span><span class="sxs-lookup"><span data-stu-id="62827-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="62827-126">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="62827-126">**Resource management**</span></span>

<span data-ttu-id="62827-127">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="62827-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="62827-128">Niepoprawny parametr jest używany w zapytaniu wykorzystania zasobów i kodzie XML, co prowadzi do niepoprawnych wyników filtrowania w siatce **wykorzystania zasobów**.</span><span class="sxs-lookup"><span data-stu-id="62827-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="62827-129">Potwierdzenie **rozszerzenia rezerwacji** powoduje wyświetlenie nieprawidłowej daty zakończenia rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="62827-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="62827-130">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="62827-130">**Sales**</span></span>

<span data-ttu-id="62827-131">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="62827-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="62827-132">Komunikat o błędzie pojawia się, jeśli cena kategorii jest tworzona z brakującymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="62827-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="62827-133">Komunikat o błędzie pojawia się w przypadku utworzenia kamienia milowego pozycji kontraktu bez wiersza zamówienia.</span><span class="sxs-lookup"><span data-stu-id="62827-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
