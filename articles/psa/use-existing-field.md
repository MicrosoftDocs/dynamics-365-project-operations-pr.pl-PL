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
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082090"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="e6d25-103">Używanie pola istniejącego w programie Project Service jako wymiaru kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="e6d25-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="e6d25-104">Program Project Service Automation (PSA) ma w encji **Wartości rzeczywiste** wiele pól, których można używać jako wymiarów kalkulacji cen opartych na zasobach w organizacjach działających poprzez projekty.</span><span class="sxs-lookup"><span data-stu-id="e6d25-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="e6d25-105">Na przykład popularnym polem jest **Zasób, który można zarezerwować**.</span><span class="sxs-lookup"><span data-stu-id="e6d25-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="e6d25-106">Mniejsze firmy, które mają mniej niż 20–30 zasobów podlegających rozliczaniu, mogą uznać, że zdefiniowanie stawek rozliczania i kosztów specyficznych dla poszczególnych zasobów jest najprostsze.</span><span class="sxs-lookup"><span data-stu-id="e6d25-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="e6d25-107">Wraz ze wzrostem liczby pracowników podlegających rozliczaniu takie podejście staje się nierealistyczne, ponieważ stawki kosztów i rozliczania zasobów zaczynają się różnić wraz z awansowaniem, zdobywaniem doświadczenia czy pozyskiwaniem nowych umiejętności przez pracowników.</span><span class="sxs-lookup"><span data-stu-id="e6d25-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="e6d25-108">Ponieważ ta metoda działa w firmach o określonej wielkości, przejdź do tematu [Używanie zasobu możliwego do zarezerwowania jako wymiaru kalkulacji cen](bookable-resource-pricing-dimension.md), gdzie wyjaśniono, jak można wykorzystywać istniejące pole programu Project Service w roli wymiaru kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="e6d25-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="e6d25-109">Innym przykładem jest kategoria transakcji.</span><span class="sxs-lookup"><span data-stu-id="e6d25-109">Another example is that of transaction category.</span></span> <span data-ttu-id="e6d25-110">Klienci i wdrożeniowcy używają kategorii transakcji w programie PSA do klasyfikowania pracy, a tego pola do określania cen i kosztów na podstawie kategorii pracy.</span><span class="sxs-lookup"><span data-stu-id="e6d25-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="e6d25-111">Aby uzyskać więcej informacji, zobacz [Używanie kategorii transakcji jako wymiaru kalkulacji cen](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="e6d25-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
