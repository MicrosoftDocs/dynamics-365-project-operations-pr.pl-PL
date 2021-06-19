---
title: Przesyłanie żądania zasobu
description: W tym temacie zamieszczono informacje dotyczące przesyłania wniosku o zasób do projektu.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013184"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="e783b-103">Przesyłanie żądania zasobu</span><span class="sxs-lookup"><span data-stu-id="e783b-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e783b-104">Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu.</span><span class="sxs-lookup"><span data-stu-id="e783b-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="e783b-105">Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.</span><span class="sxs-lookup"><span data-stu-id="e783b-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="e783b-106">W usłudze Project Service Automation (PSA) na stronie **Projekty** kliknij kartę **Zespół**, aby wyświetlić listę zasobów możliwych do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="e783b-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="e783b-107">Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Prześlij żądanie**.</span><span class="sxs-lookup"><span data-stu-id="e783b-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Przesyłanie żądania zasobu](media/RM-how-to-18.png)

<span data-ttu-id="e783b-109">Stan żądania o ogólnego członka zespołu zmieni się na **"Przesłano**.</span><span class="sxs-lookup"><span data-stu-id="e783b-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="e783b-110">Gdy menedżer zasobów zrealizuje żądanie, ogólny zasób zostanie zastąpiony nazwanym zasobem, jeśli menedżer zasobów zrealizował żądanie poprzez zarezerwowanie nazwanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="e783b-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="e783b-111">W przeciwnym razie zasób ogólny pozostanie w zespole, a stan żądania zmieni się na **Wymaga przeglądu**, jeśli menedżer zasobów zaproponował nazwany zasób.</span><span class="sxs-lookup"><span data-stu-id="e783b-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]