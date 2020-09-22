---
title: Szacowania sprzedaży w projektach
description: W tym temacie zamieszczono informacje dotyczące sposobu korzystania z mechanizmów harmonogramów i szacunków w procesie sprzedaży.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754304"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="1c94f-103">Szacowania sprzedaży w projektach</span><span class="sxs-lookup"><span data-stu-id="1c94f-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1c94f-104">Podczas procesu sprzedaży można tworzyć oszacowania sprzedaży poprzez powiązanie projektu z ofertą sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="1c94f-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="1c94f-105">W ten sposób w procesie sprzedaży może nastąpić oszacowanie deterministyczne wykorzystujące funkcje planowania i szacowania dostępne w projektach.</span><span class="sxs-lookup"><span data-stu-id="1c94f-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="1c94f-106">Jeśli sprzedaż zostanie pomyślnie sfinalizowana, harmonogramu użytego do celów oszacowania sprzedaży można użyć jako bazy do dalszego dopracowywania planu projektu.</span><span class="sxs-lookup"><span data-stu-id="1c94f-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="1c94f-107">Łączenie projektu z wierszem oferty</span><span class="sxs-lookup"><span data-stu-id="1c94f-107">Linking a project to a quote line</span></span>

<span data-ttu-id="1c94f-108">Podczas tworzenia wiersza oferty opartej na projekcie można na stronie **Wiersz oferty** utworzyć nowy projekt lub skojarzyć istniejący projekt.</span><span class="sxs-lookup"><span data-stu-id="1c94f-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formularz Wiersz oferty](media/project-8.png)
 
<span data-ttu-id="1c94f-110">Podczas tworzenia nowego projektu na podstawie szczegółów wiersza oferty można skorzystać z szablonów projektów.</span><span class="sxs-lookup"><span data-stu-id="1c94f-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="1c94f-111">Szablony projektów są projektami modelowymi, które reprezentują standardowe plany projektów i oszacowania finansowe typowe w organizacji.</span><span class="sxs-lookup"><span data-stu-id="1c94f-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="1c94f-112">Mogą one także stanowić kopie planów projektów i oszacowań z przeszłych projektów.</span><span class="sxs-lookup"><span data-stu-id="1c94f-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Szczegóły wiersza oferty](media/project-9.png)
  
<span data-ttu-id="1c94f-114">Podczas tworzenia projektu z oferty projekt jest automatycznie kojarzony z wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="1c94f-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="1c94f-115">Składniki oszacowań w projekcie</span><span class="sxs-lookup"><span data-stu-id="1c94f-115">Components of estimates in a project</span></span>

<span data-ttu-id="1c94f-116">W harmonogramie można dzielić prace na zadania, zarządzać hierarchią zadań, określać, jakie zasoby są niezbędne do wykonania danego zadania, oraz przypisywać szacowany nakład pracy wymagany do wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="1c94f-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="1c94f-117">Do definiowania oszacowań nakładu pracy i harmonogramów można używać pól na karcie **Harmonogram** na stronie **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="1c94f-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="1c94f-118">Ze względu na fakt, że cennik jest skojarzony z projektem, szacunki finansowe są obliczane na podstawie kosztów własnych i cen sprzedaży zdefiniowanych w cenniku.</span><span class="sxs-lookup"><span data-stu-id="1c94f-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="1c94f-119">Importowanie oszacowań z projektu do oferty</span><span class="sxs-lookup"><span data-stu-id="1c94f-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="1c94f-120">Po zdefiniowaniu szacunków dla projektu można je zaimportować do wiersza oferty.</span><span class="sxs-lookup"><span data-stu-id="1c94f-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="1c94f-121">Na stronie **Szczegóły wiersza oferty** na wstążce kliknij przycisk **Importuj z oszacowań**, aby podsumować szacunki projektu według typu zadania, roli lub poziomu zadania.</span><span class="sxs-lookup"><span data-stu-id="1c94f-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
