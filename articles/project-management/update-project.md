---
title: Aktualizowanie projektu
description: W tym temacie zamieszczono informacje o aktualizowaniu projektu w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286396"
---
# <a name="update-a-project"></a><span data-ttu-id="0bd05-103">Aktualizowanie projektu</span><span class="sxs-lookup"><span data-stu-id="0bd05-103">Update a project</span></span>

<span data-ttu-id="0bd05-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="0bd05-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0bd05-105">Poniżej zamieszczono podsumowanie pól, które mogą być aktualizowane po utworzeniu projektu oraz wszystkich odpowiednich skutków aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="0bd05-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="0bd05-106">Pola szczegółów projektu</span><span class="sxs-lookup"><span data-stu-id="0bd05-106">Project detail fields</span></span>

- <span data-ttu-id="0bd05-107">**Nazwa**: Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="0bd05-108">**Opis**: Opis projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="0bd05-109">**Klient**: firma, której będzie dostarczony projekt.</span><span class="sxs-lookup"><span data-stu-id="0bd05-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="0bd05-110">**Szablon kalendarza**: godziny pracy projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="0bd05-111">Po zmianie pola nastąpi ponowne obliczenie całego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="0bd05-112">**Waluta**: Waluta projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="0bd05-113">Wartość domyślna tego pola jest określana na podstawie waluty określonej w obszarze jednostki zamawiającej.</span><span class="sxs-lookup"><span data-stu-id="0bd05-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="0bd05-114">Po zaktualizowaniu jednostki zamawiającej to pole jest również aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="0bd05-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="0bd05-115">**Jednostka zamawiająca**: jednostka organizacyjna reprezentująca grupę lub oddział firmy, która jest głównie odpowiedzialna za sprzedaż i zarządzanie dostawą pracy i usług do klienta.</span><span class="sxs-lookup"><span data-stu-id="0bd05-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="0bd05-116">**Menedżer projektu**: członek zespołu projektu, który ma uprawnienia do przeglądania i zatwierdzania wpisów czasu oraz wydatków.</span><span class="sxs-lookup"><span data-stu-id="0bd05-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="0bd05-117">Pola oszacowań</span><span class="sxs-lookup"><span data-stu-id="0bd05-117">Estimate fields</span></span>

- <span data-ttu-id="0bd05-118">**Szacowana data rozpoczęcia**: Data rozpoczęcia projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="0bd05-119">Po zaktualizowaniu tego pola wszelkie zadania w projekcie będą proporcjonalnie przesunięte względem nowej daty rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="0bd05-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="0bd05-120">**Data zakończenia**: planowana data zakończenia projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="0bd05-121">**Nakład pracy**: szacowany nakład pracy w projekcie.</span><span class="sxs-lookup"><span data-stu-id="0bd05-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="0bd05-122">W przypadku dodawania zadań do projektu to pole nie jest już dostępne do edycji.</span><span class="sxs-lookup"><span data-stu-id="0bd05-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="0bd05-123">**Szacowany koszt pracy**: szacowany koszt pracy w projekcie.</span><span class="sxs-lookup"><span data-stu-id="0bd05-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="0bd05-124">W przypadku dodawania kosztów pracy do projektu to pole nie jest już dostępne do edycji.</span><span class="sxs-lookup"><span data-stu-id="0bd05-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="0bd05-125">**Szacowane wydatki**: szacowane wydatki w projekcie.</span><span class="sxs-lookup"><span data-stu-id="0bd05-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="0bd05-126">W przypadku dodawania wydatków do projektu to pole nie jest już dostępne do edycji.</span><span class="sxs-lookup"><span data-stu-id="0bd05-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="0bd05-127">Pola wartości rzeczywistych projektu</span><span class="sxs-lookup"><span data-stu-id="0bd05-127">Project actual fields</span></span>
- <span data-ttu-id="0bd05-128">**Rzeczywisty początek**: Data rozpoczęcia projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="0bd05-129">**Rzeczywisty koniec**: do zaktualizowania po zakończeniu projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="0bd05-130">Pole stanu projektu</span><span class="sxs-lookup"><span data-stu-id="0bd05-130">Project status fields</span></span>

- <span data-ttu-id="0bd05-131">**Ogólny stan projektu**: ogólna kondycja projektu podana przez menedżera projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="0bd05-132">**Komentarze**: Opis aktualnej kondycji projektu dostarczony przez menedżera projektu.</span><span class="sxs-lookup"><span data-stu-id="0bd05-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]