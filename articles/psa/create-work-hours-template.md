---
title: Tworzenie szablonu godzin pracy
description: W tym temacie opisano tworzenie szablonu godzin pracy w Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981268"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="818e7-103">Twórz szablon godzin pracy (Project Service)</span><span class="sxs-lookup"><span data-stu-id="818e7-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="818e7-104">Aby utworzyć projekt i zarządzać nim, należy zastosować do projektu szablon kalendarza.</span><span class="sxs-lookup"><span data-stu-id="818e7-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="818e7-105">W szablonie kalendarza są następujące atrybuty projektu:</span><span class="sxs-lookup"><span data-stu-id="818e7-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="818e7-106">Godziny pracy, w tym godzina rozpoczęcia i zakończenia</span><span class="sxs-lookup"><span data-stu-id="818e7-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="818e7-107">Dni robocze</span><span class="sxs-lookup"><span data-stu-id="818e7-107">Working days</span></span>
- <span data-ttu-id="818e7-108">Wyjątki kalendarzowe, np. dni niepracujące</span><span class="sxs-lookup"><span data-stu-id="818e7-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="818e7-109">Szablon kalendarza zastosowany do projektu jest kopią szablonu kalendarza zdefiniowanego w ustawieniach organizacji.</span><span class="sxs-lookup"><span data-stu-id="818e7-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="818e7-110">W przypadku zmiany szablonu kalendarza te zmiany nie są przenoszone na godziny pracy projektu.</span><span class="sxs-lookup"><span data-stu-id="818e7-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="818e7-111">Aby zmienić godziny pracy projektu, należy zastosować nowy szablon.</span><span class="sxs-lookup"><span data-stu-id="818e7-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="818e7-112">Aby utworzyć szablon kalendarza dla organizacji, należy spełnić dwa najważniejsze wymagania:</span><span class="sxs-lookup"><span data-stu-id="818e7-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="818e7-113">Definiować wymagane godziny pracy szablonu przy użyciu nowego lub istniejącego zasobu, który można zarezerwować.</span><span class="sxs-lookup"><span data-stu-id="818e7-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="818e7-114">Utworzyć nowy szablon kalendarza i skojarzyć szablon z zasobem, który można zarezerwować.</span><span class="sxs-lookup"><span data-stu-id="818e7-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="818e7-115">**Określenie godzin pracy — szablon**</span><span class="sxs-lookup"><span data-stu-id="818e7-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="818e7-116">Wybierz kolejno opcje **Zasoby** \> **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="818e7-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="818e7-117">Utwórz nowy zasób, do który chcesz się odwoływać w szablonie kalendarza lub wybierz istniejący zasób.</span><span class="sxs-lookup"><span data-stu-id="818e7-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="818e7-118">Wybierz kartę **Godziny pracy** zasobu i wykonaj instrukcje z [Ustawianie godzin pracy dla zasobu](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) w celu skonfigurowania reguł kalendarza.</span><span class="sxs-lookup"><span data-stu-id="818e7-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="818e7-119">**Utwórz nowy szablon kalendarza**</span><span class="sxs-lookup"><span data-stu-id="818e7-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="818e7-120">Wybierz kolejno opcje **Ustawienia** \> **Szablon kalendarza**.</span><span class="sxs-lookup"><span data-stu-id="818e7-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="818e7-121">Wybierz opcję **Nowy** i wprowadź nazwę, opis i zasób szablonu.</span><span class="sxs-lookup"><span data-stu-id="818e7-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="818e7-122">Kiedy do zasobu odwołuje się szablon kalendarza, kopia kalendarza zasobu jest skojarzona z szablonem kalendarza.</span><span class="sxs-lookup"><span data-stu-id="818e7-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="818e7-123">Jeśli godziny pracy skopiowanego szablonu ulegną zmianie, zmiany te nie zostaną przeniesione do szablonu kalendarza.</span><span class="sxs-lookup"><span data-stu-id="818e7-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="818e7-124">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="818e7-124">See Also</span></span>  
 [<span data-ttu-id="818e7-125">Ustawianie zasobów</span><span class="sxs-lookup"><span data-stu-id="818e7-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
