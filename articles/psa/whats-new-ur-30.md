---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 30, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostepne w programie Project Service Automation, aktualizacja 30, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852881"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="83636-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie 30, wer. 3</span><span class="sxs-lookup"><span data-stu-id="83636-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="83636-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="83636-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="83636-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="83636-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="83636-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="83636-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="83636-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="83636-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="83636-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="83636-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="83636-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wer. 3, aktualizacja 30.</span><span class="sxs-lookup"><span data-stu-id="83636-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="83636-110">Ta wersja ma numer kompilacji V3.10.51.61 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w kwietniu 2021 r.</span><span class="sxs-lookup"><span data-stu-id="83636-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="83636-111">Wydanie 30</span><span class="sxs-lookup"><span data-stu-id="83636-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="83636-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="83636-112">Bug fixes</span></span>

<span data-ttu-id="83636-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="83636-113">**Time and Expense**</span></span>

<span data-ttu-id="83636-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="83636-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="83636-115">Podczas tworzenia i zapisywania pozycji czasu na stronie **Szybkie tworzenie**, jeśli pole **Rola** zostanie usunięte, występuje błąd.</span><span class="sxs-lookup"><span data-stu-id="83636-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="83636-116">Filtr Time Entry powoduje zastosowanie niewłaściwego operatora filtru.</span><span class="sxs-lookup"><span data-stu-id="83636-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="83636-117">Kopiowane czasokopi nie są automatycznie wyświetlane po wybraniu opcji **Kopiuj tydzień** w kontrolce wpisu godziny.</span><span class="sxs-lookup"><span data-stu-id="83636-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="83636-118">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="83636-118">**Resource Management**</span></span>

<span data-ttu-id="83636-119">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="83636-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="83636-120">Gdy przedłużasz rezerwację, status rezerwacji przypisany do twardej rezerwacji jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="83636-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="83636-121">Rozszerzenie rezerwacji obejmuje stan rezerwacji zdefiniowany jako **Zatwierdzone** w metadanych konfiguracji rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="83636-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="83636-122">Jeśli nie zostanie określony prawidłowy stan rezerwacji, komunikat o błędzie nie jest poprawnie zlokalizowany.</span><span class="sxs-lookup"><span data-stu-id="83636-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="83636-123">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="83636-123">**Project Management**</span></span>

<span data-ttu-id="83636-124">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="83636-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="83636-125">Nie można tworzyć projektów w jednej walucie i zawierać zadań pokrewnych w innej walucie.</span><span class="sxs-lookup"><span data-stu-id="83636-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="83636-126">**Sprzedaż**</span><span class="sxs-lookup"><span data-stu-id="83636-126">**Sales**</span></span>

<span data-ttu-id="83636-127">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="83636-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="83636-128">Podczas kopiowania cennika ceny nie są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="83636-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="83636-129">Zamknięcie oferty jako wygranej kończy się niepowodzeniem, gdy szczegóły kosztu mają wartość pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="83636-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="83636-130">W encji **Zadanie projektu** nazwa **Szacowanego kosztu** została zmieniona na **Planowany koszt (podstawowy)**.</span><span class="sxs-lookup"><span data-stu-id="83636-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="83636-131">Wyjątek zerowego odwołania jest generowany podczas tworzenia lub usuwania faktur.</span><span class="sxs-lookup"><span data-stu-id="83636-131">A null reference exception is generated when invoices are created or deleted.</span></span>
