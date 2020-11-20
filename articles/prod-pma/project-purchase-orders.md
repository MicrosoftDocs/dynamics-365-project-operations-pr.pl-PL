---
title: Zamówienia zakupu dla projektu
description: W tym artykule opisano różne metody korzystania z programu w celu tworzenia zamówień zakupu dla projektu. Użycie metody zależy od celu zamówienia zakupu oraz wtedy, gdy zakupione towary są konsumowane i pobierane z projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082000"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="5c57c-104">Zamówienia zakupu dla projektu</span><span class="sxs-lookup"><span data-stu-id="5c57c-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c57c-105">W tym artykule opisano różne metody korzystania z programu w celu tworzenia zamówień zakupu dla projektu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="5c57c-106">Użycie metody zależy od celu zamówienia zakupu oraz wtedy, gdy zakupione towary są konsumowane i pobierane z projektu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="5c57c-107">Metody tworzenia zamówienia zakupu</span><span class="sxs-lookup"><span data-stu-id="5c57c-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="5c57c-108">Aby utworzyć zamówienie zakupu w programie Zarządzanie projektami i ich księgowanie, można użyć jednej z następujących metod.</span><span class="sxs-lookup"><span data-stu-id="5c57c-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="5c57c-109">Cel zamówienia zakupu określa, kiedy zamówienie zakupu jest zużywane, a tym samym, kiedy towary są rozliczane w projekcie.</span><span class="sxs-lookup"><span data-stu-id="5c57c-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c57c-110">Metoda</span><span class="sxs-lookup"><span data-stu-id="5c57c-110">Method</span></span></th>
<th><span data-ttu-id="5c57c-111">Przeznaczenie</span><span class="sxs-lookup"><span data-stu-id="5c57c-111">Purpose</span></span></th>
<th><span data-ttu-id="5c57c-112">Zużycie towarów</span><span class="sxs-lookup"><span data-stu-id="5c57c-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c57c-113">Utwórz zamówienie zakupu bezpośrednio z poziomu projektu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="5c57c-114">Tej metody należy użyć w celu zakupienia towarów z zewnętrznego dostawcy w celu zużycia w projekcie.</span><span class="sxs-lookup"><span data-stu-id="5c57c-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="5c57c-115">Zamówienie zakupu można utworzyć na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="5c57c-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="5c57c-116">Z poziomu samego projektu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-116">From the project itself.</span></span> <span data-ttu-id="5c57c-117">W tym przypadku projekt jest już zdefiniowany dla zamówienia zakupu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="5c57c-118">Przejście do zamówienia zakupu dotyczącego projektu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="5c57c-119">Należy wybrać zarówno dostawcę, jak i projekt, dla którego ma zostać utworzone zamówienie zakupu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="5c57c-120">Towary są pobierane podczas aktualizacji faktury zakupu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c57c-121">Utwórz zamówienie zakupu na podstawie zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="5c57c-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="5c57c-122">Tej metody należy użyć w celu zakupienia towarów podczas tworzenia zamówienia sprzedaży na podstawie projektu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="5c57c-123">Towary są zużywane, kiedy zamówienie sprzedaży jest zafakturowane na klienta.</span><span class="sxs-lookup"><span data-stu-id="5c57c-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c57c-124">Utwórz zamówienie zakupu z zapotrzebowania na towary.</span><span class="sxs-lookup"><span data-stu-id="5c57c-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="5c57c-125">Ta metoda służy do kupowania towarów podczas tworzenia zapotrzebowania na towary z projektu.</span><span class="sxs-lookup"><span data-stu-id="5c57c-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="5c57c-126">Towary są zużywane podczas aktualizacji dokumentu dostawy zapotrzebowania na towary.</span><span class="sxs-lookup"><span data-stu-id="5c57c-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="5c57c-127">W przypadku aktualizowania faktury dostawcy lub dokumentu dostawy jest wyświetlany monit o zaktualizowanie dokumentu dostawy w zapotrzebowaniu na towary.</span><span class="sxs-lookup"><span data-stu-id="5c57c-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="5c57c-128">Aby uzyskać więcej informacji, zobacz temat [Pobierz towary w zamówieniu zakupu z zapotrzebowania na towary](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="5c57c-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>
