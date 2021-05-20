---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 28, wer. 3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 28, wersja 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948702"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="d0513-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 28, wer. 3</span><span class="sxs-lookup"><span data-stu-id="d0513-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d0513-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d0513-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d0513-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="d0513-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d0513-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d0513-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d0513-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="d0513-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d0513-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d0513-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d0513-109">W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 28. Ta wersja ma numer kompilacji V3.10.46.32 i jest ogólnie dostępna po samodzielnej aktualizacji w styczniu 2021.</span><span class="sxs-lookup"><span data-stu-id="d0513-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="d0513-110">Wydanie 28</span><span class="sxs-lookup"><span data-stu-id="d0513-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d0513-111">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="d0513-111">Bug fixes</span></span>

<span data-ttu-id="d0513-112">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="d0513-112">**Time and Expense**</span></span>

<span data-ttu-id="d0513-113">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d0513-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="d0513-114">Użytkownicy mogą używać **Edycji zbiorczej** do aktualizowania wpisów czasu, które zostały zatwierdzone i przesłane.</span><span class="sxs-lookup"><span data-stu-id="d0513-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="d0513-115">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="d0513-115">**Project Management**</span></span>

<span data-ttu-id="d0513-116">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d0513-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d0513-117">W przypadkach, gdy identyfikator GUID zadania jest zinterpretowany jako liczba, nie można otworzyć zadań do edycji przy użyciu funkcji **Edytuj zadanie** na wstążce na stronie **Struktura podziału zadania**.</span><span class="sxs-lookup"><span data-stu-id="d0513-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="d0513-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d0513-118">**Sales**</span></span>

<span data-ttu-id="d0513-119">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="d0513-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="d0513-120">Wyjątek odwołania do null jest generowany, gdy jest wywoływany dodatek plug-in **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="d0513-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="d0513-121">**Oznacz jako przygotowane do fakturowania** w siatce punktów kontrolnych tylko częściowo aktualizowane atrybuty, z wyjątkiem aktualizowanego atrybutu **InvoiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="d0513-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]