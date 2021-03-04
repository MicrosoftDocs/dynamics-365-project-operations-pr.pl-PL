---
title: Używanie pola istniejącego w programie Project Service jako wymiaru kalkulacji cen
description: W tym temacie zamieszczono informacje na temat używania istniejących pól programu Project Service jako wymiarów kalkulacji cen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bc3a1df7669dac43b45d781448ed5c795a65be4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144183"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="4b130-103">Używanie pola istniejącego w programie Project Service jako wymiaru kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="4b130-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4b130-104">Program Project Service Automation (PSA) ma w encji **Wartości rzeczywiste** wiele pól, których można używać jako wymiarów kalkulacji cen opartych na zasobach w organizacjach działających poprzez projekty.</span><span class="sxs-lookup"><span data-stu-id="4b130-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="4b130-105">Na przykład popularnym polem jest **Zasób, który można zarezerwować**.</span><span class="sxs-lookup"><span data-stu-id="4b130-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="4b130-106">Mniejsze firmy, które mają mniej niż 20–30 zasobów podlegających rozliczaniu, mogą uznać, że zdefiniowanie stawek rozliczania i kosztów specyficznych dla poszczególnych zasobów jest najprostsze.</span><span class="sxs-lookup"><span data-stu-id="4b130-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="4b130-107">Wraz ze wzrostem liczby pracowników podlegających rozliczaniu takie podejście staje się nierealistyczne, ponieważ koszty zasobów i stawki opłat zaczną się zmieniać w miarę awansowania zasobów, zdobywania większego doświadczenia lub nabywania innego zestawu umiejętności.</span><span class="sxs-lookup"><span data-stu-id="4b130-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="4b130-108">Ponieważ ta metoda działa w firmach o określonej wielkości, przejdź do [Używanie zasobu możliwego do zarezerwowania jako wymiaru kalkulacji cen](bookable-resource-pricing-dimension.md), gdzie wyjaśniono, jak można wykorzystywać istniejące pole programu Project Service w roli wymiaru kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="4b130-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="4b130-109">Innym przykładem jest kategoria transakcji.</span><span class="sxs-lookup"><span data-stu-id="4b130-109">Another example is that of transaction category.</span></span> <span data-ttu-id="4b130-110">Klienci i wdrożeniowcy używają kategorii transakcji w programie PSA do klasyfikowania pracy, a tego pola do określania cen i kosztów na podstawie kategorii pracy.</span><span class="sxs-lookup"><span data-stu-id="4b130-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="4b130-111">Aby uzyskać więcej informacji, zobacz [Używanie kategorii transakcji jako wymiaru kalkulacji cen](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="4b130-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
