---
title: Pobierz towary w zamówieniu zakupu od zapotrzebowania na towary
description: W tym temat przedstawiono sposób przyjmowania zapasów na zamówienie zakupu z zapotrzebowania na towary.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011699"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="7fea8-103">Pobierz towary w zamówieniu zakupu od zapotrzebowania na towary</span><span class="sxs-lookup"><span data-stu-id="7fea8-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7fea8-104">W tym temat przedstawiono sposób przyjmowania zapasów na zamówienie zakupu z zapotrzebowania na towary.</span><span class="sxs-lookup"><span data-stu-id="7fea8-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="7fea8-105">Używając zapotrzebowania na towary zamiast transakcji na towary, można zaplanować dostawę tuż przed faktycznym wykorzystaniem towaru, utworzyć zamówienie zakupu, uwzględnić towar w ramach umowy handlowej i uwzględnić zapotrzebowanie na towary w planowaniu produkcji.</span><span class="sxs-lookup"><span data-stu-id="7fea8-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="7fea8-106">W tym zadaniu jest używany zestaw danych USSI.</span><span class="sxs-lookup"><span data-stu-id="7fea8-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="7fea8-107">W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Projekty > Wszystkie projekty**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="7fea8-108">Na liście wybierz łącze w żądanym wierszu.</span><span class="sxs-lookup"><span data-stu-id="7fea8-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="7fea8-109">W okienku akcji wybierz pozycję **Plan**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="7fea8-110">Wybierz **Zapotrzebowania na towary**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="7fea8-111">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-111">Select **New**.</span></span>
6. <span data-ttu-id="7fea8-112">W nowym wierszu wprowadź lub wybierz wartość w polu **Kod towaru**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="7fea8-113">W polu **Ilość** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="7fea8-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="7fea8-114">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-114">Select **Save**.</span></span>
9. <span data-ttu-id="7fea8-115">W okienku akcji wybierz pozycję **Zarządzaj**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="7fea8-116">Wybierz **Funkcje**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-116">Select **Functions**.</span></span>
11. <span data-ttu-id="7fea8-117">Wybierz **Utwórz zamówienie zakupu**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="7fea8-118">Zaznacz pole wyboru **Dołącz wszystkie**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="7fea8-119">W polu **Konto sprzedawcy** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="7fea8-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="7fea8-120">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-120">Select **OK**.</span></span>
15. <span data-ttu-id="7fea8-121">W okienku nawigacji wybierz kolejno pozycje **Moduły > Rozrachunki z dostawcami > Zamówienia zakupu > Wszystkie zamówienia zakupu**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="7fea8-122">Na liście wybierz łącze w żądanym wierszu.</span><span class="sxs-lookup"><span data-stu-id="7fea8-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="7fea8-123">W okienku akcji wybierz pozycję **Zakup**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="7fea8-124">Wybierz pozycję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="7fea8-125">W okienku akcji wybierz pozycję **Otrzymaj**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="7fea8-126">Wybierz **Odbiór produktu**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="7fea8-127">Wpisz wartość w polu **Odbiór produktu**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="7fea8-128">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fea8-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]