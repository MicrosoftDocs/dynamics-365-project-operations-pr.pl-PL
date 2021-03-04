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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150636"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="1acdc-103">Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 28, wer. 3</span><span class="sxs-lookup"><span data-stu-id="1acdc-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1acdc-104">Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1acdc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1acdc-105">To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności.</span><span class="sxs-lookup"><span data-stu-id="1acdc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1acdc-106">To wydanie jest zgodne z systemem Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1acdc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1acdc-107">Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację.</span><span class="sxs-lookup"><span data-stu-id="1acdc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1acdc-108">By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1acdc-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1acdc-109">W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 28. Ta wersja ma numer kompilacji V3.10.46.32 i jest ogólnie dostępna po samodzielnej aktualizacji w styczniu 2021.</span><span class="sxs-lookup"><span data-stu-id="1acdc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="1acdc-110">Wydanie 28</span><span class="sxs-lookup"><span data-stu-id="1acdc-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1acdc-111">Poprawki błędów</span><span class="sxs-lookup"><span data-stu-id="1acdc-111">Bug fixes</span></span>

<span data-ttu-id="1acdc-112">**Czas i wydatek**</span><span class="sxs-lookup"><span data-stu-id="1acdc-112">**Time and Expense**</span></span>

<span data-ttu-id="1acdc-113">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="1acdc-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="1acdc-114">Użytkownicy mogą używać **Edycji zbiorczej** do aktualizowania wpisów czasu, które zostały zatwierdzone i przesłane.</span><span class="sxs-lookup"><span data-stu-id="1acdc-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="1acdc-115">**Zarządzanie projektem**</span><span class="sxs-lookup"><span data-stu-id="1acdc-115">**Project Management**</span></span>

<span data-ttu-id="1acdc-116">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="1acdc-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="1acdc-117">W przypadkach, gdy identyfikator GUID zadania jest zinterpretowany jako liczba, nie można otworzyć zadań do edycji przy użyciu funkcji **Edytuj zadanie** na wstążce na stronie **Struktura podziału zadania**.</span><span class="sxs-lookup"><span data-stu-id="1acdc-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="1acdc-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1acdc-118">**Sales**</span></span>

<span data-ttu-id="1acdc-119">Rozwiązano następujące problemy:</span><span class="sxs-lookup"><span data-stu-id="1acdc-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="1acdc-120">Wyjątek odwołania do null jest generowany, gdy jest wywoływany dodatek plug-in **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="1acdc-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="1acdc-121">**Oznacz jako przygotowane do fakturowania** w siatce punktów kontrolnych tylko częściowo aktualizowane atrybuty, z wyjątkiem aktualizowanego atrybutu **InvoiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="1acdc-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

