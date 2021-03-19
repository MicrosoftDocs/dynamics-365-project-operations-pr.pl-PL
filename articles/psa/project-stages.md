---
title: Typy etapów projektu
description: Ten temat zawiera informacje o etapach projektów.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283696"
---
# <a name="project-stage-types"></a><span data-ttu-id="ed655-103">Typy etapów projektu</span><span class="sxs-lookup"><span data-stu-id="ed655-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ed655-104">Etapy projektu są zaprojektowane w celu odzwierciedlenia stanu projektu w miarę postępu jego realizacji.</span><span class="sxs-lookup"><span data-stu-id="ed655-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="ed655-105">Przy użyciu dostosowań można automatycznie aktualizować etapy przepływu procesów biznesowych, Power Automate, a także rozszerzenia dodatków plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed655-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="ed655-106">Poniższe etapy są zdefiniowane w domyślnym przepływie procesów biznesowych (BPF):</span><span class="sxs-lookup"><span data-stu-id="ed655-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="ed655-107">Nowa</span><span class="sxs-lookup"><span data-stu-id="ed655-107">New</span></span>
- <span data-ttu-id="ed655-108">Oferta</span><span class="sxs-lookup"><span data-stu-id="ed655-108">Quote</span></span>
- <span data-ttu-id="ed655-109">Planowanie</span><span class="sxs-lookup"><span data-stu-id="ed655-109">Plan</span></span>
- <span data-ttu-id="ed655-110">Dostarczenie</span><span class="sxs-lookup"><span data-stu-id="ed655-110">Deliver</span></span>
- <span data-ttu-id="ed655-111">Ukończono</span><span class="sxs-lookup"><span data-stu-id="ed655-111">Complete</span></span>
- <span data-ttu-id="ed655-112">Zamknij</span><span class="sxs-lookup"><span data-stu-id="ed655-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="ed655-113">Nowe</span><span class="sxs-lookup"><span data-stu-id="ed655-113">New</span></span>

<span data-ttu-id="ed655-114">Podczas tworzenia projektu jego etap jest ustawiany jako **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="ed655-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="ed655-115">Jeśli projekt został utworzony z szablonu, może mieć harmonogram, oszacowanie i dane zespołu.</span><span class="sxs-lookup"><span data-stu-id="ed655-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="ed655-116">W przeciwnym razie jest to tylko konspekt projektu, a pozostałe składniki trzeba wprowadzić.</span><span class="sxs-lookup"><span data-stu-id="ed655-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="ed655-117">Oferta</span><span class="sxs-lookup"><span data-stu-id="ed655-117">Quote</span></span>

<span data-ttu-id="ed655-118">Podczas kojarzenia projektu z ofertą lub tworzenia projektu z oferty etap projektu jest ustawiany jako **Oferta**, a szacunkowe daty rozpoczęcia i zakończenia są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="ed655-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="ed655-119">Gdy projekt jest na etapie **Oferta**, na karcie **Sprzedaż** na stronie **Encja projektu** widać szczegóły oferty.</span><span class="sxs-lookup"><span data-stu-id="ed655-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="ed655-120">Planowanie</span><span class="sxs-lookup"><span data-stu-id="ed655-120">Plan</span></span>

<span data-ttu-id="ed655-121">Gdy wygrywasz ofertą związaną z projektem i kiedy projekt przechodzi do fazy **Kontrakt**, etap projektu zostaje aktualizowany do **Planowanie**.</span><span class="sxs-lookup"><span data-stu-id="ed655-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="ed655-122">Gdy projekt jest na etapie **Planowanie**, na stronie **Encja projektu** są wyświetlane szczegóły kontraktu.</span><span class="sxs-lookup"><span data-stu-id="ed655-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="ed655-123">Dostarczenie</span><span class="sxs-lookup"><span data-stu-id="ed655-123">Deliver</span></span>

<span data-ttu-id="ed655-124">Po zakończeniu planowania projektu, gdy wszystko jest gotowe do rozpoczęcia projektu, menedżer projektu powinien zaktualizować etap projektu na **Dostarczenie**, aby pokazać, że projekt się rozpoczął.</span><span class="sxs-lookup"><span data-stu-id="ed655-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="ed655-125">Ukończono</span><span class="sxs-lookup"><span data-stu-id="ed655-125">Complete</span></span> 

<span data-ttu-id="ed655-126">Po zakończeniu prac w projekcie menedżer projektu może zaktualizować etap na **Ukończono**.</span><span class="sxs-lookup"><span data-stu-id="ed655-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="ed655-127">Aktualizując etap projektu na **Ukończono**, menedżer projektu wskazuje, że praca została w całości wykonana, ale projekt nadal pozostaje otwarty, tak aby można w nim było zarejestrować wszystkie zaległe wpisy czasu lub wydatków.</span><span class="sxs-lookup"><span data-stu-id="ed655-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="ed655-128">Zamknij</span><span class="sxs-lookup"><span data-stu-id="ed655-128">Close</span></span>

<span data-ttu-id="ed655-129">Po zarejestrowaniu wszystkich transakcji w projekcie menedżer projektu może zaktualizować etap na **Zamknięto**.</span><span class="sxs-lookup"><span data-stu-id="ed655-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="ed655-130">Odtąd nie można rejestrować żadnych transakcji, a projekt jest ustawiany jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ed655-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]