---
title: Przegląd wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje na temat wymiarów kalkulacji cen w Dynamics 365 Project Operations.
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898229"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="d3109-103">Przegląd wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="d3109-103">Pricing dimensions overview</span></span>

<span data-ttu-id="d3109-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="d3109-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d3109-105">Wymiary używane w modułach kadrowych do konfigurowania kalkulacji cen i kosztów są podzielone na dwie kategorie:</span><span class="sxs-lookup"><span data-stu-id="d3109-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="d3109-106">Osoby</span><span class="sxs-lookup"><span data-stu-id="d3109-106">People</span></span>
- <span data-ttu-id="d3109-107">Zaplanowana praca</span><span class="sxs-lookup"><span data-stu-id="d3109-107">Planned work</span></span>

<span data-ttu-id="d3109-108">Z tego powodu są dostępne dwa typy wartości wymiarów kalkulacji cen:</span><span class="sxs-lookup"><span data-stu-id="d3109-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="d3109-109">**Zestawy opcji**: wymiary, które są ustalonymi elementami stałotekstowymi dla zbioru wartości.</span><span class="sxs-lookup"><span data-stu-id="d3109-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="d3109-110">**Wartości oparte na encjach**: wymiary, które mogą być różnymi zbiorami wartości.</span><span class="sxs-lookup"><span data-stu-id="d3109-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="d3109-111">Wymiary kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="d3109-111">Pricing dimensions</span></span>

<span data-ttu-id="d3109-112">Dynamics 365 Project Operations zawiera domyślny zestaw wymiarów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="d3109-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="d3109-113">Można obejrzeć te wymiary kalkulacji cen po wybraniu kolejno opcji **Project Operations** > **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="d3109-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="d3109-114">W rekordzie parametru na karcie **Wymiary kalkulacji cen oparte na kwocie** upewnij się, że rola **msdyn_resourcecategory** oraz jednostka organizacyjna zasobów **msdyn_organizationalunit** mają w polach **Ma zastosowanie do sprzedaży** i **Ma zastosowanie do kosztu** ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="d3109-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="d3109-115">Po uruchomieniu tych pól, pozwoli to skonfigurować cenę i koszt dla każdej kombinacji roli i jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="d3109-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="d3109-116">Jeśli trzeba określić ceny lub koszty zasobów przy użyciu dodatkowych atrybutów, można utworzyć niestandardowe pola, encje i wymiary.</span><span class="sxs-lookup"><span data-stu-id="d3109-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="d3109-117">Wycena pracy personelu</span><span class="sxs-lookup"><span data-stu-id="d3109-117">Pricing human resource time</span></span>
<span data-ttu-id="d3109-118">Sposób wyceny czasu pracy personelu w organizacji jest często ważnym strategicznym aspektem, który wpływa na rentowność organizacji.</span><span class="sxs-lookup"><span data-stu-id="d3109-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="d3109-119">Gdy organizacja jest gotowa do określenia, jak chce skonfigurować stawki rozliczania i kosztów dla czasu pracy ludzi, administrator systemu informatycznego powinien to zrobić wspólnie z zespołami finansowymi i szefami działów.</span><span class="sxs-lookup"><span data-stu-id="d3109-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="d3109-120">Inne kryteria wyceny to na przykład określenie, czy mają zostać wykorzystane pola i encje, które obecnie nie są wymiarami kalkulacji cen, ale nadają się do takiej funkcji w organizacji.</span><span class="sxs-lookup"><span data-stu-id="d3109-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="d3109-121">Pola takie jak **Kategoria transakcji** (**msdyn_transactioncategory**) i **Zasób, który można zarezerwować** (**bookableresource**) to przykłady kandydatów na wymiary.</span><span class="sxs-lookup"><span data-stu-id="d3109-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="d3109-122">Należy także rozważyć, czy wymiar kalkulacji cen powinien być tabelą, czy zestawem opcji.</span><span class="sxs-lookup"><span data-stu-id="d3109-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="d3109-123">Jeśli przewidujesz zmiany wartości wymiaru w liczbie przekraczającej 10 lub 12, w związku z czym będziesz potrzebować dodatkowych atrybutów w takich wymiarach, lepiej utworzyć encję, a nie zestaw opcji.</span><span class="sxs-lookup"><span data-stu-id="d3109-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="d3109-124">Zarządzanie zestawem opcji, czyli na przykład dodawanie lub usuwanie wartości, wymaga udziału administratora lub programisty, podczas nowe wiersze do tabeli może dodawać większość użytkowników.</span><span class="sxs-lookup"><span data-stu-id="d3109-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="d3109-125">W przykładzie pod spodem przedstawiono stawki rozliczania skonfigurowane na podstawie roli oraz jednostki organizacyjnej zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="d3109-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="d3109-126">Stawki kosztów są zwykle oparte na paśmie wynagrodzenia pracownika i na jednostce organizacyjnej, do której pracownik należy.</span><span class="sxs-lookup"><span data-stu-id="d3109-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="d3109-127">W tym przykładzie tabele stawek rozliczania i stawek kosztów wyglądają następująco:</span><span class="sxs-lookup"><span data-stu-id="d3109-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="d3109-128">**Przykładowe stawki rozliczania**</span><span class="sxs-lookup"><span data-stu-id="d3109-128">**Sample bill rates**</span></span>

| <span data-ttu-id="d3109-129">Rola</span><span class="sxs-lookup"><span data-stu-id="d3109-129">Role</span></span>        | <span data-ttu-id="d3109-130">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="d3109-130">Org Unit</span></span>    |<span data-ttu-id="d3109-131">Jednostka</span><span class="sxs-lookup"><span data-stu-id="d3109-131">Unit</span></span>      |<span data-ttu-id="d3109-132">Cena</span><span class="sxs-lookup"><span data-stu-id="d3109-132">Price</span></span>      |<span data-ttu-id="d3109-133">Waluta</span><span class="sxs-lookup"><span data-stu-id="d3109-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d3109-134">Dla deweloperów</span><span class="sxs-lookup"><span data-stu-id="d3109-134">Developer</span></span>   | <span data-ttu-id="d3109-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d3109-135">Contoso US</span></span>  |<span data-ttu-id="d3109-136">Hour</span><span class="sxs-lookup"><span data-stu-id="d3109-136">Hour</span></span> | <span data-ttu-id="d3109-137">200</span><span class="sxs-lookup"><span data-stu-id="d3109-137">200</span></span>|<span data-ttu-id="d3109-138">USD</span><span class="sxs-lookup"><span data-stu-id="d3109-138">USD</span></span>     |
| <span data-ttu-id="d3109-139">Dla deweloperów</span><span class="sxs-lookup"><span data-stu-id="d3109-139">Developer</span></span>   | <span data-ttu-id="d3109-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d3109-140">Contoso India</span></span> |<span data-ttu-id="d3109-141">Hour</span><span class="sxs-lookup"><span data-stu-id="d3109-141">Hour</span></span>|   <span data-ttu-id="d3109-142">112</span><span class="sxs-lookup"><span data-stu-id="d3109-142">112</span></span>|<span data-ttu-id="d3109-143">USD</span><span class="sxs-lookup"><span data-stu-id="d3109-143">USD</span></span>     |


<span data-ttu-id="d3109-144">**Przykładowe stawki kosztów**</span><span class="sxs-lookup"><span data-stu-id="d3109-144">**Sample cost rates**</span></span>

| <span data-ttu-id="d3109-145">Pasmo wynagrodzenia</span><span class="sxs-lookup"><span data-stu-id="d3109-145">Salary Band</span></span>     | <span data-ttu-id="d3109-146">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="d3109-146">Org Unit</span></span>    |<span data-ttu-id="d3109-147">Jednostka</span><span class="sxs-lookup"><span data-stu-id="d3109-147">Unit</span></span>      |<span data-ttu-id="d3109-148">Cena</span><span class="sxs-lookup"><span data-stu-id="d3109-148">Price</span></span>      |<span data-ttu-id="d3109-149">Waluta</span><span class="sxs-lookup"><span data-stu-id="d3109-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d3109-150">Moja firma_pasmo1</span><span class="sxs-lookup"><span data-stu-id="d3109-150">My company_Band1</span></span> | <span data-ttu-id="d3109-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d3109-151">Contoso US</span></span>  |<span data-ttu-id="d3109-152">Hour</span><span class="sxs-lookup"><span data-stu-id="d3109-152">Hour</span></span> | <span data-ttu-id="d3109-153">145</span><span class="sxs-lookup"><span data-stu-id="d3109-153">145</span></span>|<span data-ttu-id="d3109-154">USD</span><span class="sxs-lookup"><span data-stu-id="d3109-154">USD</span></span>     |
| <span data-ttu-id="d3109-155">Moja firma_pasmo2</span><span class="sxs-lookup"><span data-stu-id="d3109-155">My company_Band2</span></span> | <span data-ttu-id="d3109-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d3109-156">Contoso India</span></span> |<span data-ttu-id="d3109-157">Hour</span><span class="sxs-lookup"><span data-stu-id="d3109-157">Hour</span></span>|   <span data-ttu-id="d3109-158">67</span><span class="sxs-lookup"><span data-stu-id="d3109-158">67</span></span>|<span data-ttu-id="d3109-159">USD</span><span class="sxs-lookup"><span data-stu-id="d3109-159">USD</span></span>     |