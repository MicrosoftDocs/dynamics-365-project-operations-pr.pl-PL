---
title: Definiowanie kalendarzy projektu
description: Ten temat zawiera informacje na temat stosowania szablonu kalendarza projektu w celu śledzenia harmonogramu projektu.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999009"
---
# <a name="define-project-calendars"></a><span data-ttu-id="7f7d1-103">Definiowanie kalendarzy projektu</span><span class="sxs-lookup"><span data-stu-id="7f7d1-103">Define project calendars</span></span>

<span data-ttu-id="7f7d1-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="7f7d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7f7d1-105">Aby utworzyć projekt i zarządzać nim, należy zastosować do projektu szablon kalendarza.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="7f7d1-106">W szablonie kalendarza są następujące atrybuty projektu:</span><span class="sxs-lookup"><span data-stu-id="7f7d1-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="7f7d1-107">Godziny pracy, w tym godzina rozpoczęcia i zakończenia</span><span class="sxs-lookup"><span data-stu-id="7f7d1-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="7f7d1-108">Dni robocze</span><span class="sxs-lookup"><span data-stu-id="7f7d1-108">Working days</span></span>
- <span data-ttu-id="7f7d1-109">Wyjątki kalendarzowe, np. dni niepracujące</span><span class="sxs-lookup"><span data-stu-id="7f7d1-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="7f7d1-110">Szablon kalendarza zastosowany do projektu jest kopią szablonu kalendarza zdefiniowanego w ustawieniach organizacji.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="7f7d1-111">W przypadku zmiany szablonu kalendarza te zmiany nie są przenoszone na godziny pracy projektu.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="7f7d1-112">Aby zmienić godziny pracy projektu, należy zastosować nowy szablon.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="7f7d1-113">Aby utworzyć szablon kalendarza dla organizacji, należy spełnić dwa najważniejsze wymagania:</span><span class="sxs-lookup"><span data-stu-id="7f7d1-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="7f7d1-114">Definiować wymagane godziny pracy szablonu przy użyciu nowego lub istniejącego zasobu, który można zarezerwować.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="7f7d1-115">Utworzyć nowy szablon kalendarza i skojarzyć szablon z zasobem, który można zarezerwować.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="7f7d1-116">**Określenie godzin pracy — szablon**</span><span class="sxs-lookup"><span data-stu-id="7f7d1-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="7f7d1-117">Wybierz kolejno opcje **Zasoby** \> **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="7f7d1-118">Utwórz nowy zasób, do który chcesz się odwoływać w szablonie kalendarza lub wybierz istniejący zasób.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="7f7d1-119">Wybierz kartę **Godziny pracy** zasobu i wykonaj instrukcje z [Ustawianie godzin pracy dla zasobu](/dynamics365/field-service/set-work-hours-resource.md) w celu skonfigurowania reguł kalendarza.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="7f7d1-120">**Utwórz nowy szablon kalendarza**</span><span class="sxs-lookup"><span data-stu-id="7f7d1-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="7f7d1-121">Wybierz kolejno opcje **Ustawienia** \> **Szablon kalendarza**.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="7f7d1-122">Wybierz opcję **Nowy** i wprowadź nazwę, opis i zasób szablonu.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="7f7d1-123">Kiedy do zasobu odwołuje się szablon kalendarza, kopia kalendarza zasobu jest skojarzona z szablonem kalendarza.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="7f7d1-124">Jeśli godziny pracy skopiowanego szablonu ulegną zmianie, zmiany te nie zostaną przeniesione do szablonu kalendarza.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="7f7d1-125">Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.</span><span class="sxs-lookup"><span data-stu-id="7f7d1-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

