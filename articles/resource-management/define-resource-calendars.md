---
title: Definiowanie kalendarzy zasobów
description: W tym temacie zamieszczono informacje dotyczące sposobu definiowania kalendarzy godzin pracy dla zasobów w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123931"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="5d140-103">Definiowanie kalendarzy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d140-103">Define resource calendars</span></span>

<span data-ttu-id="5d140-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="5d140-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d140-105">Każdy zasób zaksięgowany w pracy nad projektem musi wykorzystywać kalendarz godzin pracy, aby zdefiniować swoją dostępność.</span><span class="sxs-lookup"><span data-stu-id="5d140-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="5d140-106">Godziny pracy zasobu można zdefiniować na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="5d140-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="5d140-107">Definiowanie poszczególnych reguł kalendarza dla zasobu</span><span class="sxs-lookup"><span data-stu-id="5d140-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="5d140-108">Stosowanie istniejącego szablonu kalendarza dla zasobu</span><span class="sxs-lookup"><span data-stu-id="5d140-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="5d140-109">Określenie godzin pracy zasobu</span><span class="sxs-lookup"><span data-stu-id="5d140-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="5d140-110">W menu **Zasoby** wybierz polecenie **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="5d140-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5d140-111">W widoku siatki wybierz odpowiedni **Zasób zaksięgowany**.</span><span class="sxs-lookup"><span data-stu-id="5d140-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="5d140-112">Na stronie **Szczegóły zasobu** wybierz kartę **Godziny pracy**. Domyślnie w programie jest ustawiona domyślna liczba godzin pracy z domyślnym szablonem czasu pracy, który jest zdefiniowany dla organizacji.</span><span class="sxs-lookup"><span data-stu-id="5d140-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="5d140-113">Aby zaktualizować godziny pracy, kliknij prawym przyciskiem myszy datę rozpoczęcia proponowanej reguły kalendarza, która ma zostać zdefiniowana.</span><span class="sxs-lookup"><span data-stu-id="5d140-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="5d140-114">Aby zdefiniować regułę kalendarza dla określonego dnia, pozostałej części serii lub całego kalendarza, należy użyć menu reguł kalendarza.</span><span class="sxs-lookup"><span data-stu-id="5d140-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="5d140-115">Po wybraniu opcji można zdefiniować następujące dane:</span><span class="sxs-lookup"><span data-stu-id="5d140-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="5d140-116">Dzień tygodnia, w którym będą stosowane godziny pracy.</span><span class="sxs-lookup"><span data-stu-id="5d140-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="5d140-117">Godziny pracy każdego dnia.</span><span class="sxs-lookup"><span data-stu-id="5d140-117">The working times within each day.</span></span>
    - <span data-ttu-id="5d140-118">Strefę czasową dla reguły kalendarza.</span><span class="sxs-lookup"><span data-stu-id="5d140-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="5d140-119">W stosownych przypadkach można również określić czas wolny od pracy dla reguły.</span><span class="sxs-lookup"><span data-stu-id="5d140-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="5d140-120">Zastosowanie szablonu kalendarza do zasobu</span><span class="sxs-lookup"><span data-stu-id="5d140-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="5d140-121">W menu **Zasoby** wybierz polecenie **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="5d140-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5d140-122">W widoku siatki wybierz maksymalnie 25 **Zasobów do zaksięgowania**, które chcesz zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="5d140-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="5d140-123">Wybierz opcję **Ustaw kalendarz**. Wyświetli się się monit z listą dostępnych szablonów godzin pracy.</span><span class="sxs-lookup"><span data-stu-id="5d140-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="5d140-124">Wybierz go, aby znaleźć wybrany szablon, a następnie wybierz opcję **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="5d140-124">Select the template you want to use, and then select **Apply**.</span></span>
