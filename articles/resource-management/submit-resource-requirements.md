---
title: Przesyłanie żądania zasobów
description: Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu. Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961734"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="0d0cc-104">Przesyłanie żądania zasobów</span><span class="sxs-lookup"><span data-stu-id="0d0cc-104">Submit a resource request</span></span>

<span data-ttu-id="0d0cc-105">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="0d0cc-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d0cc-106">Wygenerowane wymaganie zasobu można przesłać jako żądanie zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d0cc-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="0d0cc-107">Żądanie jest następnie wysyłane do menedżera zasobów w celu zrealizowania.</span><span class="sxs-lookup"><span data-stu-id="0d0cc-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="0d0cc-108">W usłudze Dynamics 365 Project Operations na stronie **Projekty** wybierz kartę **Zespół**, aby wyświetlić listę zasobów możliwych do zarezerwowania.</span><span class="sxs-lookup"><span data-stu-id="0d0cc-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="0d0cc-109">Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Prześlij żądanie**.</span><span class="sxs-lookup"><span data-stu-id="0d0cc-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="0d0cc-110">Stan żądania o ogólnego członka zespołu zmieni się na **"Przesłano**.</span><span class="sxs-lookup"><span data-stu-id="0d0cc-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="0d0cc-111">Gdy żądanie zostanie zrealizowane, ogólny zasób zostanie zastąpiony nazwanym zasobem, jeśli menedżer zasobów zrealizował żądanie poprzez zarezerwowanie nazwanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d0cc-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="0d0cc-112">W przeciwnym razie, jeśli menedżer zaproponuje nazwany zasób, zasób ogólny pozostanie w zespole, a stan żądania zmieni się na **Wymaga przeglądu**, jeśli menedżer zasobów zaproponował nazwany zasób.</span><span class="sxs-lookup"><span data-stu-id="0d0cc-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
