---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 23, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 23, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: f90c0d2168b261cf1b6ef10374f282274ea61af5
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948972"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="2d590-103">Project Service Automation, wydanie 23, wer. 3</span><span class="sxs-lookup"><span data-stu-id="2d590-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2d590-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2d590-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2d590-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="2d590-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2d590-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2d590-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2d590-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="2d590-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2d590-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2d590-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2d590-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 23.</span><span class="sxs-lookup"><span data-stu-id="2d590-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="2d590-110">Numer tej kompilacji to V3.10.34.30 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w sierpniu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="2d590-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="2d590-111">Wydanie 23</span><span class="sxs-lookup"><span data-stu-id="2d590-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2d590-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="2d590-112">Bug fixes</span></span>

<span data-ttu-id="2d590-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="2d590-113">**Time and Expense**</span></span>

<span data-ttu-id="2d590-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="2d590-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="2d590-115">Obsługa przypadków krawędzi w programie **Usuwanie członka zespołu projektu** w celu utworzenia zrozumiałego wyjątku.</span><span class="sxs-lookup"><span data-stu-id="2d590-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="2d590-116">W wyniku importu przydziałów jest pusty ekran usuwania.</span><span class="sxs-lookup"><span data-stu-id="2d590-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="2d590-117">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="2d590-117">**Resource Management**</span></span>

<span data-ttu-id="2d590-118">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="2d590-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d590-119">**Karta zasobu siatki wykorzystania zasobów** zawiera nieprawidłowe dane, gdy skala czasu jest dłuższa niż pięć dni.</span><span class="sxs-lookup"><span data-stu-id="2d590-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="2d590-120">Kiedy klienci tworzą zasób z możliwością rezerwacji, dodatek nie może automatycznie dodać zasobu do grupy Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="2d590-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="2d590-121">W widoku **Uzgadnianie** nieprawidłowo wyświetlane są ręczne rozkłady w widoku **Tydzień** lub **Miesiąc**.</span><span class="sxs-lookup"><span data-stu-id="2d590-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="2d590-122">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="2d590-122">**Project Management**</span></span>

<span data-ttu-id="2d590-123">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="2d590-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d590-124">Zbyt duża liczba jednostek **retrievemultiple dla usersettings** powoduje spadek wydajności zatwierdzania projektów i innych operacji.</span><span class="sxs-lookup"><span data-stu-id="2d590-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="2d590-125">Wyszukiwanie zasobu w siatce **Planowania zadań** jest ograniczone, aby było widocznych tylko pięciu członków zespołu z zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="2d590-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="2d590-126">Funkcja **wyszukiwania zasobów** w siatce planowania zadań nie filtruje zasobów nieaktywnych.</span><span class="sxs-lookup"><span data-stu-id="2d590-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="2d590-127">Tryb ręczny nie działa zgodnie z oczekiwaniami w strukturze podziału pracy planowania projektu.</span><span class="sxs-lookup"><span data-stu-id="2d590-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="2d590-128">W siatce **Planowania zadań** są wyświetlane **Nieaktywne kategorie transakcji**.</span><span class="sxs-lookup"><span data-stu-id="2d590-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="2d590-129">Siatka **Przypisania zasobu** jest zaokrąglana nieprawidłowo, gdy zadanie ma wiele przypisań.</span><span class="sxs-lookup"><span data-stu-id="2d590-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="2d590-130">Wartości zaokrąglania są różne między kosztem planowanym i kosztem rzeczywistym jednego zadania.</span><span class="sxs-lookup"><span data-stu-id="2d590-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="2d590-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2d590-131">**Sales**</span></span>

<span data-ttu-id="2d590-132">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="2d590-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d590-133">Dwukrotne kliknięcie **Pobierania wszystkich kategorii transakcji** powoduje utworzenie wielu wierszy.</span><span class="sxs-lookup"><span data-stu-id="2d590-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]