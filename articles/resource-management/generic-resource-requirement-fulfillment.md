---
title: wRealizowanie ogólnych wymagań zasobów
description: Ta temat zawiera informacje o rezerwowaniu nazwanych zasobów na potrzeby ogólnego wymagania zasobu.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897599"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="5f9a6-103">wRealizowanie ogólnych wymagań zasobów</span><span class="sxs-lookup"><span data-stu-id="5f9a6-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="5f9a6-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="5f9a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5f9a6-105">Można użyć nazwanego zasobu, aby zastąpić ogólny zasób mający wymaganie zasobu.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="5f9a6-106">Na stronie **Projekty** wybierz pozycję **Zespół**.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="5f9a6-107">Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie wybierz opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="5f9a6-108">Możesz też otworzyć wymaganie zasobu, a następnie wybrać przycisk **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="5f9a6-109">Na stronie **Asystent planowania** wybierz nazwany zasób, który ma zostać zarezerwowany do Twojego zespołu projektu, a następnie wybierz opcję **Zarezerwuj**.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="5f9a6-110">Gdy rezerwacja jest zakończona i zaspokojona przez nazwany zasób, zasób ogólny jest zastępowany nazwanym zasobem.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="5f9a6-111">Również przypisania w harmonogramie zostaną zaktualizowane o nazwany zasób.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="5f9a6-112">Wypełnianie roli ogólnego zasobu wieloma nazwanym zasobami</span><span class="sxs-lookup"><span data-stu-id="5f9a6-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="5f9a6-113">Zaspokojenie wymagania na zasób ogólny za pomocą wielu nazwanych zasobów przypomina operację przypisania jednego nazwanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="5f9a6-114">Załóżmy na przykład, że istnieje zadanie o czasie trwania pięć dni i nakładzie pracy 120 godzin.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="5f9a6-115">Tego zadania nie może wykonać jeden zasób pracujący na typowej ośmiogodzinnej zmianie w pięciodniowym tygodniu pracy.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="5f9a6-116">Wymaganie opiewa na 120 godzin pracy inżynieryjnej przy robotach przez pięć dni, co oznacza 24 godziny na dobę.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="5f9a6-117">Jest to przykład sytuacji, kiedy do zaspokojenia żądania zasobu ogólnego potrzeba wielu nazwanych zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="5f9a6-118">W celu zrealizowania tego zapotrzebowania trzeba zarezerwować wiele zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="5f9a6-119">Główna różnica w tym scenariuszu polega na tym, że zasób ogólny pozostaje w zespole przypisanym do zadania, a członkowie zespołu będący zarezerwowanymi zasobami nazwanymi nie są przypisywani do zadania w ramach ich standardowych obowiązków.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="5f9a6-120">Menedżer projektu może odpowiednio przypisać pracę do nazwanych zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="5f9a6-121">Widok **Uzgadnianie** może pomóc menedżerowi projektu podzielić rezerwacje między wiele zasobów i przypisać im zadanie.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="5f9a6-122">Nie jest to wykonywane automatycznie, ponieważ w każdym scenariuszu bardziej skomplikowanym niż ten powyżej, na przykład gdy użytkownik ma pakiet zadań składających się na wymaganie lub system musi uwzględnić sposób, w jaki Menedżer projektu zamierza dokonywać przypisań.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="5f9a6-123">Ponieważ system nie jest w stanie zrozumieć zamierzeń, prawdopodobnie założenia mogą być inne niż zamierzone i może wystąpić nieprawidłowy lub nieprzewidywalny rezultat.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="5f9a6-124">Przewidywany wynik jest taki, że zasób ogólny pozostanie przypisany do czasu, aż menedżer projektu jednoznacznie utworzyć przypisania za pomocą widoku **Uzgadnianie**.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>

