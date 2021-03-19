---
title: Etapy projektu
description: W tym temacie zamieszczono informacje na temat etapów projektów, które są dostępne w Microsoft Dynamics Project operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286801"
---
# <a name="project-stages"></a><span data-ttu-id="a27a6-103">Etapy projektu</span><span class="sxs-lookup"><span data-stu-id="a27a6-103">Project stages</span></span>

<span data-ttu-id="a27a6-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="a27a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a27a6-105">Etapy projektu są zaprojektowane w celu odzwierciedlenia stanu projektu w miarę postępu jego realizacji.</span><span class="sxs-lookup"><span data-stu-id="a27a6-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="a27a6-106">Przy użyciu dostosowań można automatycznie aktualizować etapy przepływu procesów biznesowych, Power Automate, a także rozszerzenia dodatków plug-in.</span><span class="sxs-lookup"><span data-stu-id="a27a6-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="a27a6-107">Poniższe etapy są zdefiniowane w domyślnym przepływie procesów biznesowych:</span><span class="sxs-lookup"><span data-stu-id="a27a6-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="a27a6-108">Nowa</span><span class="sxs-lookup"><span data-stu-id="a27a6-108">New</span></span>
- <span data-ttu-id="a27a6-109">Oferta</span><span class="sxs-lookup"><span data-stu-id="a27a6-109">Quote</span></span>
- <span data-ttu-id="a27a6-110">Plan</span><span class="sxs-lookup"><span data-stu-id="a27a6-110">Plan</span></span>
- <span data-ttu-id="a27a6-111">Dostarczenie</span><span class="sxs-lookup"><span data-stu-id="a27a6-111">Deliver</span></span>
- <span data-ttu-id="a27a6-112">Zakończony</span><span class="sxs-lookup"><span data-stu-id="a27a6-112">Complete</span></span>
- <span data-ttu-id="a27a6-113">Zamykanie</span><span class="sxs-lookup"><span data-stu-id="a27a6-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="a27a6-114">Nowa</span><span class="sxs-lookup"><span data-stu-id="a27a6-114">New</span></span>

<span data-ttu-id="a27a6-115">Podczas tworzenia projektu jego etap jest ustawiany jako **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="a27a6-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="a27a6-116">Jeśli projekt został utworzony z szablonu, może mieć harmonogram, oszacowanie i dane zespołu.</span><span class="sxs-lookup"><span data-stu-id="a27a6-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="a27a6-117">W przeciwnym razie jest to konspekt projektu, a pozostałe składniki trzeba wprowadzić.</span><span class="sxs-lookup"><span data-stu-id="a27a6-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="a27a6-118">Oferta</span><span class="sxs-lookup"><span data-stu-id="a27a6-118">Quote</span></span>

<span data-ttu-id="a27a6-119">Podczas kojarzenia projektu z ofertą lub tworzenia projektu z oferty etap projektu jest ustawiany jako **Oferta**, a szacunkowe daty rozpoczęcia i zakończenia są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="a27a6-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="a27a6-120">Gdy projekt jest na etapie **Oferta**, na karcie **Sprzedaż** na stronie **Encja projektu** widać szczegóły oferty.</span><span class="sxs-lookup"><span data-stu-id="a27a6-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="a27a6-121">Planowanie</span><span class="sxs-lookup"><span data-stu-id="a27a6-121">Plan</span></span>

<span data-ttu-id="a27a6-122">Gdy wygrywasz ofertą związaną z projektem i kiedy projekt przechodzi do fazy **Kontrakt**, etap projektu zostaje aktualizowany do **Planowanie**.</span><span class="sxs-lookup"><span data-stu-id="a27a6-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="a27a6-123">Gdy projekt jest na etapie **Planowanie**, na stronie **Encja projektu** są wyświetlane szczegóły kontraktu.</span><span class="sxs-lookup"><span data-stu-id="a27a6-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="a27a6-124">Dostarczenie</span><span class="sxs-lookup"><span data-stu-id="a27a6-124">Deliver</span></span>

<span data-ttu-id="a27a6-125">Po zakończeniu planowania projektu, gdy wszystko jest gotowe do rozpoczęcia projektu, menedżer projektu powinien zaktualizować etap projektu na **Dostarczenie**, aby pokazać, że projekt się rozpoczął.</span><span class="sxs-lookup"><span data-stu-id="a27a6-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="a27a6-126">Ukończono</span><span class="sxs-lookup"><span data-stu-id="a27a6-126">Complete</span></span> 

<span data-ttu-id="a27a6-127">Po zakończeniu prac w projekcie menedżer projektu może zaktualizować etap na **Ukończono**.</span><span class="sxs-lookup"><span data-stu-id="a27a6-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="a27a6-128">Aktualizując etap projektu na **Ukończono**, menedżer projektu wskazuje, że praca została w całości wykonana, ale projekt nadal pozostaje otwarty, tak aby można w nim było zarejestrować wszystkie zaległe wpisy czasu lub wydatków.</span><span class="sxs-lookup"><span data-stu-id="a27a6-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="a27a6-129">Zamknij</span><span class="sxs-lookup"><span data-stu-id="a27a6-129">Close</span></span>

<span data-ttu-id="a27a6-130">Po zarejestrowaniu wszystkich transakcji w projekcie menedżer projektu może zaktualizować etap na **Zamknięto**.</span><span class="sxs-lookup"><span data-stu-id="a27a6-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="a27a6-131">Odtąd nie można rejestrować żadnych transakcji, a projekt jest ustawiany jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="a27a6-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]