---
title: Etapy projektu
description: Ten temat zawiera informacje o etapach projektów.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754300"
---
# <a name="project-stages"></a><span data-ttu-id="96c96-103">Etapy projektu</span><span class="sxs-lookup"><span data-stu-id="96c96-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="96c96-104">Etapy projektu są aktualizowane w celu odzwierciedlenia stanu projektu w miarę postępu jego realizacji.</span><span class="sxs-lookup"><span data-stu-id="96c96-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="96c96-105">Domyślny przepływ procesów biznesowych powoduje automatyczne aktualizowanie niektórych etapów projektu, podczas gdy inne etapy są aktualizowane ręcznie przez menedżera projektu.</span><span class="sxs-lookup"><span data-stu-id="96c96-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="96c96-106">Poniższe etapy są zdefiniowane w domyślnym przepływie procesów biznesowych (BPF):</span><span class="sxs-lookup"><span data-stu-id="96c96-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="96c96-107">Nowe</span><span class="sxs-lookup"><span data-stu-id="96c96-107">New</span></span>
- <span data-ttu-id="96c96-108">Oferta</span><span class="sxs-lookup"><span data-stu-id="96c96-108">Quote</span></span>
- <span data-ttu-id="96c96-109">Planowanie</span><span class="sxs-lookup"><span data-stu-id="96c96-109">Plan</span></span>
- <span data-ttu-id="96c96-110">Dostarczenie</span><span class="sxs-lookup"><span data-stu-id="96c96-110">Deliver</span></span>
- <span data-ttu-id="96c96-111">Ukończono</span><span class="sxs-lookup"><span data-stu-id="96c96-111">Complete</span></span>
- <span data-ttu-id="96c96-112">Zamknij</span><span class="sxs-lookup"><span data-stu-id="96c96-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="96c96-113">Nowe</span><span class="sxs-lookup"><span data-stu-id="96c96-113">New</span></span>

<span data-ttu-id="96c96-114">Podczas tworzenia projektu jego etap jest ustawiany jako **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="96c96-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="96c96-115">Jeśli projekt został utworzony z szablonu, może mieć harmonogram, oszacowanie i dane zespołu.</span><span class="sxs-lookup"><span data-stu-id="96c96-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="96c96-116">W przeciwnym razie jest to tylko konspekt projektu, a pozostałe składniki trzeba wprowadzić.</span><span class="sxs-lookup"><span data-stu-id="96c96-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="96c96-117">Oferta</span><span class="sxs-lookup"><span data-stu-id="96c96-117">Quote</span></span>

<span data-ttu-id="96c96-118">Podczas kojarzenia projektu z ofertą lub tworzenia projektu z oferty etap projektu jest ustawiany jako **Oferta**, a szacunkowe daty rozpoczęcia i zakończenia są aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="96c96-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="96c96-119">Gdy projekt jest na etapie **Oferta**, na karcie **Sprzedaż** na stronie **Encja projektu** widać szczegóły oferty.</span><span class="sxs-lookup"><span data-stu-id="96c96-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="96c96-120">Planowanie</span><span class="sxs-lookup"><span data-stu-id="96c96-120">Plan</span></span>

<span data-ttu-id="96c96-121">Gdy wygrywasz ofertą związaną z projektem i kiedy projekt przechodzi do fazy **Kontrakt**, etap projektu zostaje aktualizowany do **Planowanie**.</span><span class="sxs-lookup"><span data-stu-id="96c96-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="96c96-122">Gdy projekt jest na etapie **Planowanie**, na stronie **Encja projektu** są wyświetlane szczegóły kontraktu.</span><span class="sxs-lookup"><span data-stu-id="96c96-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="96c96-123">Dostarczenie</span><span class="sxs-lookup"><span data-stu-id="96c96-123">Deliver</span></span>

<span data-ttu-id="96c96-124">Po zakończeniu planowania projektu, gdy wszystko jest gotowe do rozpoczęcia projektu, menedżer projektu powinien zaktualizować etap projektu na **Dostarczenie**, aby pokazać, że projekt się rozpoczął.</span><span class="sxs-lookup"><span data-stu-id="96c96-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="96c96-125">Ukończono</span><span class="sxs-lookup"><span data-stu-id="96c96-125">Complete</span></span> 

<span data-ttu-id="96c96-126">Po zakończeniu prac w projekcie menedżer projektu może zaktualizować etap na **Ukończono**.</span><span class="sxs-lookup"><span data-stu-id="96c96-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="96c96-127">Aktualizując etap projektu na **Ukończono**, menedżer projektu wskazuje, że praca została w całości wykonana, ale projekt nadal pozostaje otwarty, tak aby można w nim było zarejestrować wszystkie zaległe wpisy czasu lub wydatków.</span><span class="sxs-lookup"><span data-stu-id="96c96-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="96c96-128">Zamknij</span><span class="sxs-lookup"><span data-stu-id="96c96-128">Close</span></span>

<span data-ttu-id="96c96-129">Po zarejestrowaniu wszystkich transakcji w projekcie menedżer projektu może zaktualizować etap na **Zamknięto**.</span><span class="sxs-lookup"><span data-stu-id="96c96-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="96c96-130">Odtąd nie można rejestrować żadnych transakcji, a projekt jest ustawiany jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="96c96-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
