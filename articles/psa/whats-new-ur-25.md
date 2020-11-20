---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 25, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, wydanie 25, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183556"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="e2670-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 25, wer. 3</span><span class="sxs-lookup"><span data-stu-id="e2670-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="e2670-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e2670-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e2670-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="e2670-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e2670-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e2670-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e2670-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="e2670-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e2670-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e2670-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e2670-109">W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 25. Ta wersja ma numer kompilacji 3.10.43.76 i jest ogólnie dostępna po samodzielnej aktualizacji w październiku 2020 r.</span><span class="sxs-lookup"><span data-stu-id="e2670-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="e2670-110">Wydanie 25</span><span class="sxs-lookup"><span data-stu-id="e2670-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e2670-111">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="e2670-111">Bug fixes</span></span>

<span data-ttu-id="e2670-112">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="e2670-112">**Time and Expense**</span></span>

<span data-ttu-id="e2670-113">Naprawiono następujący problem:</span><span class="sxs-lookup"><span data-stu-id="e2670-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="e2670-114">Wykres wprowadzania czasu pokazujący dodatkowe dane na podstawie zbyt dużego zakresu pobieranych danych.</span><span class="sxs-lookup"><span data-stu-id="e2670-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="e2670-115">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="e2670-115">**Resource Management**</span></span>

<span data-ttu-id="e2670-116">Naprawiono następujący problem:</span><span class="sxs-lookup"><span data-stu-id="e2670-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="e2670-117">Dodano kod wdrożeniowy pakietu w celu pominięcia importu poprawki Universal Resource Scheduling, jeśli nowsza wersja poprawki już istnieje.</span><span class="sxs-lookup"><span data-stu-id="e2670-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="e2670-118">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="e2670-118">**Project Management**</span></span>

<span data-ttu-id="e2670-119">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="e2670-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="e2670-120">Poprawiono rozbieżności w zaokrąglaniu i kursach wymiany powodujące nieprawidłowy planowany koszt w siatce śledzenia projektu.</span><span class="sxs-lookup"><span data-stu-id="e2670-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="e2670-121">Umożliwia wyświetlanie w formularzu **Projektu** dwóch lub więcej siatek reagujących na zareagowanie.</span><span class="sxs-lookup"><span data-stu-id="e2670-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="e2670-122">Przy sprawdzeniu poprawności zaadresowano zdolność przypisywania zadania poza datą zakończenia kalendarza, co powoduje niepowodzenie przypisania zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2670-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="e2670-123">Ulepszona obsługa błędów w celu wygenerowania wyjątków dotyczących odwołań null z następujących programów:</span><span class="sxs-lookup"><span data-stu-id="e2670-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="e2670-124">Dodatek plug-in **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="e2670-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="e2670-125">**PreValidateProjectTaskCreate** kiedy zadanie projektu zostanie utworzone bez skojarzonego projektu</span><span class="sxs-lookup"><span data-stu-id="e2670-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="e2670-126">Dodatek plug-in **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="e2670-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="e2670-127">Dodatek plug-in **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="e2670-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="e2670-128">Dodatek plug-in **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="e2670-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="e2670-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e2670-129">**Sales**</span></span>

<span data-ttu-id="e2670-130">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="e2670-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="e2670-131">Ulepszona obsługa błędów w celu rozwiązania wyjątków odwołań null wygenerowanych z **Kopii projektu: szacuje zarządzanie HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="e2670-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="e2670-132">**Nie jest gotowy do zafakturowania** w **Rozliczeniu na czas i materiały** nie czyści stanu fakturowania.</span><span class="sxs-lookup"><span data-stu-id="e2670-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="e2670-133">przyciski z błędnie etykietowanymi **Cenami** zostały poprawione na karcie **Cena roli** i **Elementy katalogu**.</span><span class="sxs-lookup"><span data-stu-id="e2670-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
