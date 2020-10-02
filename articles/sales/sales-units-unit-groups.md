---
title: Jednostki i grupy jednostek
description: W tym temat zamieszczono informacje dotyczące sposobu tworzenia jednostek i grup jednostek w Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898769"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="1c35a-103">Jednostki i grupy jednostek</span><span class="sxs-lookup"><span data-stu-id="1c35a-103">Units and unit groups</span></span>

<span data-ttu-id="1c35a-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="1c35a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1c35a-105">Jednostki to ilości lub wielkości, w jakich sprzedajesz swoje produkty lub usługi.</span><span class="sxs-lookup"><span data-stu-id="1c35a-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="1c35a-106">Na przykład jeśli sprzedajesz zaopatrzenie ogrodnicze, możesz sprzedawać nasiona w paczkach, pudełkach oraz na paletach.</span><span class="sxs-lookup"><span data-stu-id="1c35a-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="1c35a-107">Grupa jednostek jest zbiorem tych różnych jednostek.</span><span class="sxs-lookup"><span data-stu-id="1c35a-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="1c35a-108">Aby wykonać czynności opisane w tym temacie należy się upewnić, że użytkownik został przypisany do roli administratora systemu lub menedżer ds. sprzedaży, lub że posiada równoważne uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="1c35a-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="1c35a-109">Tworzenie grupy jednostek</span><span class="sxs-lookup"><span data-stu-id="1c35a-109">Create a unit group</span></span>

1. <span data-ttu-id="1c35a-110">Na mapie witryny, wybierz **Jednostki**.</span><span class="sxs-lookup"><span data-stu-id="1c35a-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="1c35a-111">Wybierz **Nowa** w oknie dialogowym **Utwórz grupę jednostek** i wprowadź nazwę jednostki.</span><span class="sxs-lookup"><span data-stu-id="1c35a-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="1c35a-112">W polu **Jednostka podstawowa** wpisz najmniejszą wspólną jednostkę miary, w której produkt będzie sprzedawany.</span><span class="sxs-lookup"><span data-stu-id="1c35a-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="1c35a-113">Można na przykład wprowadzić „sztukę” lub „uncję”.</span><span class="sxs-lookup"><span data-stu-id="1c35a-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="1c35a-114">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c35a-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="1c35a-115">Grupy jednostek i dodawanie do nich jednostek</span><span class="sxs-lookup"><span data-stu-id="1c35a-115">Add units to a unit group</span></span>

1. <span data-ttu-id="1c35a-116">Otwórz grupę jednostek, a następnie na karcie **Powiązane** wybierz pozycję **Jednostki**.</span><span class="sxs-lookup"><span data-stu-id="1c35a-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="1c35a-117">Zobaczysz, że jednostka podstawowa została już dodana.</span><span class="sxs-lookup"><span data-stu-id="1c35a-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="1c35a-118">Wybierz opcję **Dodaj nową jednostkę** i na stronie **Szybkie tworzenie: jednostka** w polu **Nazwa** wprowadź nazwę jednostki.</span><span class="sxs-lookup"><span data-stu-id="1c35a-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="1c35a-119">W polu **Ilość** wprowadź ilość, jaką będzie zawierać dana jednostka.</span><span class="sxs-lookup"><span data-stu-id="1c35a-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="1c35a-120">Na przykład jeśli pudełko zawiera dwie sztuki, należy wpisać „2”.</span><span class="sxs-lookup"><span data-stu-id="1c35a-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="1c35a-121">W polu **Jednostka podstawowa** wybierz jednostkę podstawową, aby ustanowić najmniejszą jednostkę miary w jednostce.</span><span class="sxs-lookup"><span data-stu-id="1c35a-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="1c35a-122">Można na przykład wybrać pozycję „sztuka”.</span><span class="sxs-lookup"><span data-stu-id="1c35a-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="1c35a-123">Wybierz pozycję **Zapisz**:</span><span class="sxs-lookup"><span data-stu-id="1c35a-123">Select **Save**:</span></span>
