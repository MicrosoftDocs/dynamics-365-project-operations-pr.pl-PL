---
title: Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia szablonów projektów przy użyciu niestandardowej akcji kopiowania projektów.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131626"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="83e09-103">Projektowanie szablonów projektów przy użyciu narzędzia kopiowania projektów</span><span class="sxs-lookup"><span data-stu-id="83e09-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="83e09-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="83e09-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="83e09-105">Dynamics 365 Project Operations obsługują możliwość kopiowania projektu i przywracania wszystkich przypisań z powrotem do zasobów ogólnych reprezentujący rolę.</span><span class="sxs-lookup"><span data-stu-id="83e09-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="83e09-106">Dzięki tej funkcji użytkownicy mogą tworzyć podstawowe szablony projektów.</span><span class="sxs-lookup"><span data-stu-id="83e09-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="83e09-107">Po wybraniu opcji **Kopiowania projektów** status projektu docelowego jest aktualizowany.</span><span class="sxs-lookup"><span data-stu-id="83e09-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="83e09-108">Pole **Powód statusu** jest wykorzystywane do określenia, czy zadanie kopiowania jest zakończone.</span><span class="sxs-lookup"><span data-stu-id="83e09-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="83e09-109">Wybranie opcji **Kopiowania projektu** powoduje zaktualizowanie daty rozpoczęcia projektu do bieżącej daty rozpoczęcia, jeśli nie zostanie wykryta data docelowa w encji projektu docelowego.</span><span class="sxs-lookup"><span data-stu-id="83e09-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="83e09-110">Niestandardowa akcja kopiowania projektu</span><span class="sxs-lookup"><span data-stu-id="83e09-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="83e09-111">Nazwa/nazwisko</span><span class="sxs-lookup"><span data-stu-id="83e09-111">Name</span></span> 

<span data-ttu-id="83e09-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="83e09-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="83e09-113">Parametry wejściowe</span><span class="sxs-lookup"><span data-stu-id="83e09-113">Input parameters</span></span>
<span data-ttu-id="83e09-114">Istnieją 3 parametry wejściowe:</span><span class="sxs-lookup"><span data-stu-id="83e09-114">There are three input parameters:</span></span>

| <span data-ttu-id="83e09-115">Parametr</span><span class="sxs-lookup"><span data-stu-id="83e09-115">Parameter</span></span>          | <span data-ttu-id="83e09-116">Pisz</span><span class="sxs-lookup"><span data-stu-id="83e09-116">Type</span></span>   | <span data-ttu-id="83e09-117">Wartości</span><span class="sxs-lookup"><span data-stu-id="83e09-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="83e09-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="83e09-118">ProjectCopyOption</span></span>  | <span data-ttu-id="83e09-119">String</span><span class="sxs-lookup"><span data-stu-id="83e09-119">String</span></span> | <span data-ttu-id="83e09-120">**{"removeNamedResources":true}** lub **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="83e09-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="83e09-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="83e09-121">SourceProject</span></span>      | <span data-ttu-id="83e09-122">Odwołanie do encji</span><span class="sxs-lookup"><span data-stu-id="83e09-122">Entity Reference</span></span> | <span data-ttu-id="83e09-123">Projekt źródłowy</span><span class="sxs-lookup"><span data-stu-id="83e09-123">Source Project</span></span> |
| <span data-ttu-id="83e09-124">Język docelowy</span><span class="sxs-lookup"><span data-stu-id="83e09-124">Target</span></span>             | <span data-ttu-id="83e09-125">Odwołanie do encji</span><span class="sxs-lookup"><span data-stu-id="83e09-125">Entity Reference</span></span> | <span data-ttu-id="83e09-126">Projekt docelowy</span><span class="sxs-lookup"><span data-stu-id="83e09-126">Target Project</span></span> |


- <span data-ttu-id="83e09-127">**{"clearTeamsAndAssignments":true}**: domyślne zachowanie projektu sieciowego, usunie wszystkie przypisania i członków zespołu.</span><span class="sxs-lookup"><span data-stu-id="83e09-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="83e09-128">**{"removeNamedResources":true}** domyślne zachowanie Project Operations powoduje przywrócenie przydziałów do zasobów ogólnych.</span><span class="sxs-lookup"><span data-stu-id="83e09-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="83e09-129">Aby uzyskać więcej informacji na temat Akcji, zobacz [Korzystanie z akcji Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="83e09-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="83e09-130">Określ pola do skopiowania</span><span class="sxs-lookup"><span data-stu-id="83e09-130">Specify fields to copy</span></span> 
<span data-ttu-id="83e09-131">Po wywołaniu akcji **Kopiowanie projektu** zostanie wyświetlony widok projektu **Kopiuj kolumny projektu**, Aby określić, które pola zostaną skopiowane podczas kopiowania projektu.</span><span class="sxs-lookup"><span data-stu-id="83e09-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
