---
title: Definiowanie umiejętności i biegłości
description: Ten temat zawiera informacje na temat konfigurowania modeli umiejętności w celu oceny zasobów.
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
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897644"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="b5679-103">Definiowanie umiejętności i biegłości</span><span class="sxs-lookup"><span data-stu-id="b5679-103">Define skills and proficiencies</span></span>

<span data-ttu-id="b5679-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="b5679-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5679-105">Umiejętności to cechy zasobów, które są współdzielone między programami Dynamics 365 Project Operations i (jeśli istnieje) Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b5679-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="b5679-106">Aby zarządzać repozytorium umiejętności w rozwiązaniu Project Operations, wybierz kolejno opcje **Zasoby** \> **Umiejętności zasobu**.</span><span class="sxs-lookup"><span data-stu-id="b5679-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="b5679-107">Używanie modeli biegłości do oceniania zasobów</span><span class="sxs-lookup"><span data-stu-id="b5679-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="b5679-108">Umiejętności zasobów są oceniane za pomocą modeli biegłości.</span><span class="sxs-lookup"><span data-stu-id="b5679-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="b5679-109">Poszczególne oceny są w jednym modelu.</span><span class="sxs-lookup"><span data-stu-id="b5679-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="b5679-110">Aby utworzyć model biegłości, wybierz kolejno opcje **Zasoby** \> **Modele poziomów biegłości**, a następnie kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="b5679-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="b5679-111">W nowym modelu oceniania określ minimalną wartość oceny, maksymalną wartość oceny oraz ocenianą encję.</span><span class="sxs-lookup"><span data-stu-id="b5679-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="b5679-112">W podsiatce **Wartości oceny** można zdefiniować różne wartości ocen, od minimalnej do maksymalnej.</span><span class="sxs-lookup"><span data-stu-id="b5679-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="b5679-113">Te wartości ocen są wyświetlane w filtrach **Wymagania zasobów**, **Tablica harmonogramu** i **Asystent planowania**.</span><span class="sxs-lookup"><span data-stu-id="b5679-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
