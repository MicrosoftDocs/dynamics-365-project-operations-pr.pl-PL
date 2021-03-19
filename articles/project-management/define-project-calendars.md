---
title: Definiowanie kalendarzy projektu
description: Ta temat zawiera informacje na temat korzystania z kalendarza projektu w celu śledzenia jego harmonogramu.
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286981"
---
# <a name="define-project-calendars"></a><span data-ttu-id="ffa41-103">Definiowanie kalendarzy projektu</span><span class="sxs-lookup"><span data-stu-id="ffa41-103">Define project calendars</span></span>

<span data-ttu-id="ffa41-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="ffa41-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ffa41-105">Aby utworzyć harmonogram projektu, należy utworzyć szablon kalendarza projektu, który definiuje liczbę godzin pracy w ciągu dnia i wszystkie dni wolne od pracy.</span><span class="sxs-lookup"><span data-stu-id="ffa41-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="ffa41-106">Aby utworzyć szablon kalendarza projektu, należy skojarzyć szablon pracy z polem **Szablon kalendarza** dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="ffa41-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="ffa41-107">Aby utworzyć szablon pracy, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="ffa41-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="ffa41-108">W lewym okienku nawigacji wybierz **Zasoby**.</span><span class="sxs-lookup"><span data-stu-id="ffa41-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="ffa41-109">Na stronie listy **Zasoby** otwórz rekord użytkownika, a następnie wybierz pozycję **Pokaż godziny pracy**.</span><span class="sxs-lookup"><span data-stu-id="ffa41-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ffa41-110">Upewnij się, że zezwolono na wyświetlanie wyskakujących okienek na stronie przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="ffa41-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="ffa41-111">Dzięki temu będziesz widzieć godzin pracy ustawione dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffa41-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="ffa41-112">Na karcie **Widok miesięczny** wybierz **Konfiguracja**.</span><span class="sxs-lookup"><span data-stu-id="ffa41-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="ffa41-113">Zostanie wyświetlona lista z trzema opcjami:</span><span class="sxs-lookup"><span data-stu-id="ffa41-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="ffa41-114">Nowy harmonogram tygodniowy</span><span class="sxs-lookup"><span data-stu-id="ffa41-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="ffa41-115">Harmonogram pracy na jeden dzień</span><span class="sxs-lookup"><span data-stu-id="ffa41-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="ffa41-116">Czas wolny</span><span class="sxs-lookup"><span data-stu-id="ffa41-116">Time Off</span></span>

4. <span data-ttu-id="ffa41-117">Zaznacz opcję **Nowy harmonogram tygodniowy**, a następnie ustaw opcje dla tego harmonogramu zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffa41-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="ffa41-118">Można określić cykliczny harmonogram tygodniowy, dzienne parametry godzinowe, dni wolne od pracy itd.</span><span class="sxs-lookup"><span data-stu-id="ffa41-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="ffa41-119">Ustaw zakres dat, kliknij przycisk **Zapisz**, a następnie wybierz **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="ffa41-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="ffa41-120">Wróć do strony listy **Zasoby** i wybierz zasób, dla którego ustawiono godziny pracy.</span><span class="sxs-lookup"><span data-stu-id="ffa41-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="ffa41-121">W ustawieniu **Ustaw kalendarz jako** określ szablon pracy.</span><span class="sxs-lookup"><span data-stu-id="ffa41-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="ffa41-122">W oknie dialogowym **Szablon pracy** nadaj nazwę szablonowi pracy, a następnie kliknij przycisk **Zastosuj**.</span><span class="sxs-lookup"><span data-stu-id="ffa41-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="ffa41-123">Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.</span><span class="sxs-lookup"><span data-stu-id="ffa41-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]