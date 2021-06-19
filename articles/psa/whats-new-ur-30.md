---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 30, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 30, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010439"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="bd677-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 30, wer. 3</span><span class="sxs-lookup"><span data-stu-id="bd677-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bd677-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bd677-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bd677-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="bd677-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bd677-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bd677-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bd677-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="bd677-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bd677-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="bd677-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="bd677-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 30.</span><span class="sxs-lookup"><span data-stu-id="bd677-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="bd677-110">Ta wersja ma numer kompilacji V3.10.51.61 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w kwietniu 2021 r.</span><span class="sxs-lookup"><span data-stu-id="bd677-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="bd677-111">Wydanie 30</span><span class="sxs-lookup"><span data-stu-id="bd677-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bd677-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="bd677-112">Bug fixes</span></span>

<span data-ttu-id="bd677-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="bd677-113">**Time and Expense**</span></span>

<span data-ttu-id="bd677-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="bd677-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bd677-115">Podczas tworzenia i zapisywania pozycji czasu na stronie **Szybkie tworzenie**, jeśli pole **Rola** zostanie usunięte, występuje błąd.</span><span class="sxs-lookup"><span data-stu-id="bd677-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="bd677-116">Filtr Time Entry powoduje zastosowanie niewłaściwego operatora filtru.</span><span class="sxs-lookup"><span data-stu-id="bd677-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="bd677-117">Kopiowane czasokopi nie są automatycznie wyświetlane po wybraniu opcji **Kopiuj tydzień** w kontrolce wpisu godziny.</span><span class="sxs-lookup"><span data-stu-id="bd677-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="bd677-118">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="bd677-118">**Resource Management**</span></span>

<span data-ttu-id="bd677-119">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="bd677-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="bd677-120">Gdy przedłużasz rezerwację, status rezerwacji przypisany do twardej rezerwacji jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="bd677-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="bd677-121">Rozszerzenie rezerwacji obejmuje stan rezerwacji zdefiniowany jako **Zatwierdzone** w metadanych konfiguracji rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="bd677-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="bd677-122">Jeśli nie zostanie określony prawidłowy stan rezerwacji, komunikat o błędzie nie jest poprawnie zlokalizowany.</span><span class="sxs-lookup"><span data-stu-id="bd677-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="bd677-123">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="bd677-123">**Project Management**</span></span>

<span data-ttu-id="bd677-124">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="bd677-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="bd677-125">Nie można tworzyć projektów w jednej walucie i zawierać zadań pokrewnych w innej walucie.</span><span class="sxs-lookup"><span data-stu-id="bd677-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="bd677-126">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="bd677-126">**Sales**</span></span>

<span data-ttu-id="bd677-127">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="bd677-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="bd677-128">Podczas kopiowania cennika ceny nie są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="bd677-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="bd677-129">Zamknięcie oferty jako wygranej kończy się niepowodzeniem, gdy szczegóły kosztu mają wartość pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="bd677-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="bd677-130">W encji **Zadanie projektu** nazwa **Szacowanego kosztu** została zmieniona na **Planowany koszt (podstawowy)**.</span><span class="sxs-lookup"><span data-stu-id="bd677-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="bd677-131">Wyjątek zerowego odwołania jest generowany podczas tworzenia lub usuwania faktur.</span><span class="sxs-lookup"><span data-stu-id="bd677-131">A null reference exception is generated when invoices are created or deleted.</span></span>
