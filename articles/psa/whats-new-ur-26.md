---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 26, wer. 3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 26, wersja 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948837"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="3dd95-103">Project Service Automation, wydanie aktualizacji 26, wer. 3</span><span class="sxs-lookup"><span data-stu-id="3dd95-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3dd95-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3dd95-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3dd95-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="3dd95-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3dd95-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3dd95-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3dd95-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="3dd95-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3dd95-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3dd95-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3dd95-109">W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 26, wer. 3.</span><span class="sxs-lookup"><span data-stu-id="3dd95-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="3dd95-110">Ta wersja ma numer kompilacji V3.10.44.59 i jest ogólnie dostępna za pośrednictwem samodzielnej aktualizacji w grudniu 2020 r.</span><span class="sxs-lookup"><span data-stu-id="3dd95-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="3dd95-111">Wydanie 26</span><span class="sxs-lookup"><span data-stu-id="3dd95-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3dd95-112">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="3dd95-112">Bug fixes</span></span>

<span data-ttu-id="3dd95-113">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="3dd95-113">**Time and Expense**</span></span>

<span data-ttu-id="3dd95-114">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="3dd95-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3dd95-115">Użytkownicy mogą zmienić zadanie we wpisie czasu, który został zatwierdzony/przesłany.</span><span class="sxs-lookup"><span data-stu-id="3dd95-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="3dd95-116">Błąd „Nie ustawiono odwołania do obiektu” podczas zapisywania wpisu czasu.</span><span class="sxs-lookup"><span data-stu-id="3dd95-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="3dd95-117">Importowanie wpisów czasu z przydziałów zasobów powoduje utworzenie wpisów czasu o nieprawidłowych wartościach DateTime.</span><span class="sxs-lookup"><span data-stu-id="3dd95-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="3dd95-118">Po zainstalowaniu programu Project Service Automation i aplikacji Field Service przycisk **Nowy** jest wyświetlany dwa razy na pasku poleceń dla wpisów czasu w aplikacji Field Service.</span><span class="sxs-lookup"><span data-stu-id="3dd95-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="3dd95-119">Aktualizacje komórek typu **Zezwalanie na aktualizacje** i **Grupa jednostek** działają teraz w ramach siatki **Szacunki wydatków**.</span><span class="sxs-lookup"><span data-stu-id="3dd95-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="3dd95-120">Formularz **Aktualizowanie wpisu czasu — edytowanie** zawiera obszar **Oś czasu**.</span><span class="sxs-lookup"><span data-stu-id="3dd95-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="3dd95-121">Zatwierdzanie czasu dla nieprojektowych wpisów czasu powoduje blokowanie systemu w przypadku wyszukiwania roli osoby zatwierdzającej w projekcie.</span><span class="sxs-lookup"><span data-stu-id="3dd95-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="3dd95-122">**Zarządzanie zasobami**</span><span class="sxs-lookup"><span data-stu-id="3dd95-122">**Resource Management**</span></span>

<span data-ttu-id="3dd95-123">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="3dd95-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="3dd95-124">Dodano walidację w dodatku plug-in **PostProjectCreate** w celu wyszukania podstawowego wymagania przed jego utworzeniem.</span><span class="sxs-lookup"><span data-stu-id="3dd95-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="3dd95-125">Formularz szybkiego tworzenia **Członek zespołu projektu** zgłasza wyjątek odwołania o wartości null w przypadku usuwania pól z formularza.</span><span class="sxs-lookup"><span data-stu-id="3dd95-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="3dd95-126">Generowanie zapotrzebowań na 12 godzin w ciągu 1 roku będzie kończyć się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3dd95-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="3dd95-127">Ulepszono wyjątek odwołania o wartości null dla komunikatu o błędzie podczas tworzenia zapotrzebowania dotyczącego zasobu.</span><span class="sxs-lookup"><span data-stu-id="3dd95-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="3dd95-128">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="3dd95-128">**Project Management**</span></span>

<span data-ttu-id="3dd95-129">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="3dd95-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="3dd95-130">Ulepszono walidację, aby rozwiązać problem dotyczący wyjątku odwołania o wartości null generowanego w dodatku plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="3dd95-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="3dd95-131">Projekty publikowane przez dodatek plug-in Microsoft Project dla komputerów stacjonarnych usuwają nieprzypisane przypisania.</span><span class="sxs-lookup"><span data-stu-id="3dd95-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="3dd95-132">Dodano nową walidację w przypadku, gdy odwołanie do projektu zadania jest nieprawidłowe z powodu wyjątku odwołania o wartości null w dodatku plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="3dd95-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="3dd95-133">W siatce członków zespołu nie są pokazywane żadne unikatowe przypisania dla rekordu członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="3dd95-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="3dd95-134">Dodano nowe komunikaty walidacji i komunikaty o błędach wynikające z wyjątku odwołania o wartości null w dodatku plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="3dd95-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="3dd95-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3dd95-135">**Sales**</span></span>

<span data-ttu-id="3dd95-136">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="3dd95-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="3dd95-137">W przypadku wybierania wiersza opartego na projekcie w ofercie lub kontrakcie przycisk **Sugestia** powinien być widoczny tylko podczas wybierania wiersza opartego na produkcie skojarzonego z istniejącym produktem.</span><span class="sxs-lookup"><span data-stu-id="3dd95-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="3dd95-138">Oddzielono uprawnienie **Create_Product** od uprawnienia **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="3dd95-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="3dd95-139">Usunięcie wiersza faktury powoduje niepowodzenie odwołania do wartości null w elemencie **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="3dd95-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]