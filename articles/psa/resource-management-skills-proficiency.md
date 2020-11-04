---
title: Modele umiejętności i biegłości
description: Ten temat zawiera informacje na temat korzystania z modeli umiejętności i biegłości.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082232"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="efb60-103">Modele umiejętności i biegłości</span><span class="sxs-lookup"><span data-stu-id="efb60-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="efb60-104">Umiejętności to cechy zasobów, które są współdzielone między programami Dynamics 365 Project Service Automation i (jeśli istnieje) Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="efb60-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="efb60-105">Aby zarządzać repozytorium umiejętności w rozwiązaniu Project Service Automation, wybierz kolejno opcje **Zasoby** \> **Umiejętności zasobu**.</span><span class="sxs-lookup"><span data-stu-id="efb60-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Umiejętności zasobu](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="efb60-107">Używanie modeli biegłości do oceniania zasobów</span><span class="sxs-lookup"><span data-stu-id="efb60-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="efb60-108">Umiejętności zasobów są oceniane za pomocą modeli biegłości.</span><span class="sxs-lookup"><span data-stu-id="efb60-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="efb60-109">Poszczególne oceny są w jednym modelu.</span><span class="sxs-lookup"><span data-stu-id="efb60-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="efb60-110">Aby utworzyć model biegłości, wybierz kolejno opcje **Zasoby** \> **Modele poziomów biegłości** , a następnie kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="efb60-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="efb60-111">W nowym modelu oceniania określ minimalną wartość oceny, maksymalną wartość oceny oraz ocenianą encję.</span><span class="sxs-lookup"><span data-stu-id="efb60-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="efb60-112">W podsiatce **Wartości oceny** można zdefiniować różne wartości ocen, od minimalnej do maksymalnej.</span><span class="sxs-lookup"><span data-stu-id="efb60-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Zdefiniowane oceny minimalna i maksymalna](media/Resource-Management-image85.png)

<span data-ttu-id="efb60-114">Te wartości ocen są wyświetlane w filtrach **Wymagania zasobów** , **Tablica harmonogramu** i **Asystent planowania**.</span><span class="sxs-lookup"><span data-stu-id="efb60-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
