---
title: Konfigurowanie pól niestandardowych Project Operations jako wymiarów kalkulacji cen
description: Ten temat zawiera informacje o używaniu pól jako wymiarów kalkulacji cen w rozwiązaniu Dynamics 365 Project Operations.
author: rumant
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274651"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="9913c-103">Pola aplikacji Project Operations jako wymiary kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="9913c-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="9913c-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="9913c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9913c-105">Encja **Wartości rzeczywiste** zawiera wiele pól, które mogą być używane jako wymiary kalkulacji cen w przypadku kalkulacji cen opartej na zasobach.</span><span class="sxs-lookup"><span data-stu-id="9913c-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="9913c-106">Na przykład popularnym polem jest **Zasób, który można zarezerwować**.</span><span class="sxs-lookup"><span data-stu-id="9913c-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="9913c-107">Mniejsze firmy, które mają mniej niż 20–30 zasobów podlegających rozliczaniu, mogą uznać, że zdefiniowanie stawek rozliczania i kosztów specyficznych dla poszczególnych zasobów jest najprostsze.</span><span class="sxs-lookup"><span data-stu-id="9913c-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="9913c-108">Jednakże wraz z wzrastającą liczbą pracowników, stawki zawierające konkretne koszty mogą stać się trudne w obsłudze.</span><span class="sxs-lookup"><span data-stu-id="9913c-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="9913c-109">Koszty zasobów i stawki kosztów na początku zaczynają się różnić z czasem, gdyż pracownicy otrzymują awanse, zdobywają doświadczenie lub nowe umiejętności.</span><span class="sxs-lookup"><span data-stu-id="9913c-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="9913c-110">Innym przykładem jest kategoria transakcji.</span><span class="sxs-lookup"><span data-stu-id="9913c-110">Another example is that of transaction category.</span></span> <span data-ttu-id="9913c-111">Klienci i wdrożeniowcy używają kategorii transakcji do klasyfikowania pracy, a tego pola do określania cen i kosztów na podstawie kategorii pracy.</span><span class="sxs-lookup"><span data-stu-id="9913c-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]