---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 28, wer. 3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 28, wersja 3.
author: ruhercul
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010529"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="dc6bb-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 28, wer. 3</span><span class="sxs-lookup"><span data-stu-id="dc6bb-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dc6bb-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="dc6bb-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="dc6bb-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dc6bb-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="dc6bb-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dc6bb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dc6bb-109">W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 28. Ta wersja ma numer kompilacji V3.10.46.32 i jest ogólnie dostępna po samodzielnej aktualizacji w styczniu 2021.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="dc6bb-110">Wydanie 28</span><span class="sxs-lookup"><span data-stu-id="dc6bb-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dc6bb-111">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="dc6bb-111">Bug fixes</span></span>

<span data-ttu-id="dc6bb-112">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="dc6bb-112">**Time and Expense**</span></span>

<span data-ttu-id="dc6bb-113">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="dc6bb-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="dc6bb-114">Użytkownicy mogą używać **Edycji zbiorczej** do aktualizowania wpisów czasu, które zostały zatwierdzone i przesłane.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="dc6bb-115">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="dc6bb-115">**Project Management**</span></span>

<span data-ttu-id="dc6bb-116">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="dc6bb-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="dc6bb-117">W przypadkach, gdy identyfikator GUID zadania jest zinterpretowany jako liczba, nie można otworzyć zadań do edycji przy użyciu funkcji **Edytuj zadanie** na wstążce na stronie **Struktura podziału zadania**.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="dc6bb-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="dc6bb-118">**Sales**</span></span>

<span data-ttu-id="dc6bb-119">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="dc6bb-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="dc6bb-120">Wyjątek odwołania do null jest generowany, gdy jest wywoływany dodatek plug-in **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="dc6bb-121">**Oznacz jako przygotowane do fakturowania** w siatce punktów kontrolnych tylko częściowo aktualizowane atrybuty, z wyjątkiem aktualizowanego atrybutu **InvoiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="dc6bb-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]