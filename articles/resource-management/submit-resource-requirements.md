---
title: Przesyłanie żądania zasobów
description: Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu. Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279151"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="b75df-104">Przesyłanie żądania zasobów</span><span class="sxs-lookup"><span data-stu-id="b75df-104">Submit a resource request</span></span>

<span data-ttu-id="b75df-105">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="b75df-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b75df-106">Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu.</span><span class="sxs-lookup"><span data-stu-id="b75df-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="b75df-107">Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.</span><span class="sxs-lookup"><span data-stu-id="b75df-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="b75df-108">W rozwiązaniu Dynamics 365 Project Operations na stronie **Projekty** kliknij kartę **Zespół**, aby wyświetlić listę zasobów możliwych do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="b75df-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="b75df-109">Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Prześlij żądanie**.</span><span class="sxs-lookup"><span data-stu-id="b75df-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="b75df-110">Stan żądania o ogólnego członka zespołu zmieni się na **"Przesłano**.</span><span class="sxs-lookup"><span data-stu-id="b75df-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="b75df-111">Gdy żądanie zostanie zrealizowane, ogólny zasób zostanie zastąpiony nazwanym zasobem, jeśli menedżer zasobów zrealizował żądanie poprzez zarezerwowanie nazwanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="b75df-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="b75df-112">W przeciwnym razie, jeśli menedżer zaproponuje nazwany zasób, zasób ogólny pozostanie w zespole, a stan żądania zmieni się na **Wymaga przeglądu**, jeśli menedżer zasobów zaproponował nazwany zasób.</span><span class="sxs-lookup"><span data-stu-id="b75df-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]