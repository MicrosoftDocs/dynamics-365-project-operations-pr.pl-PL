---
title: Strona główna wymiarów kalkulacji cen i kosztów
description: Ta temat zawiera omówienie funkcjonalności wymiarów kalkulacji cen.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754307"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="5c5c3-103">Strona główna wymiarów kalkulacji cen i kosztów</span><span class="sxs-lookup"><span data-stu-id="5c5c3-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="5c5c3-104">Wymiary używane w modułach kadrowych do konfigurowania kalkulacji cen i kosztów są podzielone na dwie kategorie:</span><span class="sxs-lookup"><span data-stu-id="5c5c3-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="5c5c3-105">Osoby</span><span class="sxs-lookup"><span data-stu-id="5c5c3-105">People</span></span>
- <span data-ttu-id="5c5c3-106">Zaplanowana praca</span><span class="sxs-lookup"><span data-stu-id="5c5c3-106">Planned work</span></span>

<span data-ttu-id="5c5c3-107">Z tego powodu w programie Project Service Automation (PSA) są dostępne dwa typy wartości wymiarów kalkulacji cen:</span><span class="sxs-lookup"><span data-stu-id="5c5c3-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="5c5c3-108">**Zestawy opcji** — wymiary, które są ustalonymi elementami stałotekstowymi dla zbioru wartości.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="5c5c3-109">**Wartości oparte na encjach** — wymiary, które mogą być różnymi zbiorami wartości.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="5c5c3-110">Wymiary kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="5c5c3-110">Pricing dimensions</span></span>

<span data-ttu-id="5c5c3-111">Program PSA zawiera fabrycznie domyślny zestaw wymiarów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="5c5c3-112">Można je obejrzeć po wybraniu kolejno opcji **Project Service** > **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="5c5c3-113">W rekordzie parametru na karcie **Wymiary kalkulacji cen oparte na kwocie** upewnij się, że rola **msdyn_resourcecategory** oraz jednostka organizacyjna zasobów **msdyn_organizationalunit** mają w polach **Ma zastosowanie do sprzedaży** i **Ma zastosowanie do kosztu** ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="5c5c3-114">Pozwoli to skonfigurować cenę i koszt dla każdej kombinacji roli i jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Zrzut ekranu z parametrami usługi Project Service z wyróżnioną opcją „Ma zastosowanie do sprzedaży”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="5c5c3-116">Jeżeli w wersji programu PSA sprzed 3 używano gotowych pól roli i jednostki organizacyjnej jako wymiarów kalkulacji cen, nie będzie żadnych zauważalnych zmian.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="5c5c3-117">Można nadal korzystać z usługi Project Service w zwykły sposób.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="5c5c3-118">Jeśli trzeba określić ceny lub koszty zasobów przy użyciu dodatkowych atrybutów, można utworzyć niestandardowe pola, encje i wymiary.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="5c5c3-119">Aby uzyskać więcej informacji, zobacz następujące tematy. Należy jednak pamiętać, że procedury trzeba wykonywać w poniższej kolejności:</span><span class="sxs-lookup"><span data-stu-id="5c5c3-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="5c5c3-120">Tworzenie niestandardowych pól i encji</span><span class="sxs-lookup"><span data-stu-id="5c5c3-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="5c5c3-121">Dodawanie pól niestandardowych do ustawień cen i encji transakcyjnych</span><span class="sxs-lookup"><span data-stu-id="5c5c3-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="5c5c3-122">Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="5c5c3-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="5c5c3-123">Aktualizowanie atrybutów dodatków plug-in w celu dołączenia nowych wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="5c5c3-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="5c5c3-124">Wycena pracy personelu</span><span class="sxs-lookup"><span data-stu-id="5c5c3-124">Pricing human resource time</span></span>
<span data-ttu-id="5c5c3-125">Sposób wyceny czasu pracy personelu w organizacji jest często ważnym strategicznym aspektem, który wpływa na rentowność organizacji.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="5c5c3-126">Gdy organizacja jest gotowa do określenia, jak chce skonfigurować stawki rozliczania i kosztów dla czasu pracy ludzi, administrator systemu informatycznego powinien to zrobić wspólnie z zespołami finansowymi i szefami działów.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="5c5c3-127">Inne kryteria wyceny to na przykład określenie, czy mają zostać wykorzystane pola i encje, które obecnie nie są wymiarami kalkulacji cen, ale nadają się do takiej funkcji w organizacji.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="5c5c3-128">Pola takie jak **Kategoria transakcji** (**msdyn_transactioncategory**) i **Zasób, który można zarezerwować** (**bookableresource**) to przykłady kandydatów na wymiary.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="5c5c3-129">Należy także rozważyć, czy wymiar kalkulacji cen powinien być tabelą, czy zestawem opcji.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="5c5c3-130">Jeśli przewidujesz zmiany wartości wymiaru w liczbie przekraczającej 10 lub 12, w związku z czym będziesz potrzebować dodatkowych atrybutów w takich wymiarach, lepiej utworzyć encję, a nie zestaw opcji.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="5c5c3-131">Zarządzanie zestawem opcji, czyli na przykład dodawanie lub usuwanie wartości, wymaga udziału administratora lub programisty, podczas nowe wiersze do tabeli może dodawać większość użytkowników.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="5c5c3-132">W przykładzie pod spodem przedstawiono stawki rozliczania skonfigurowane na podstawie roli oraz jednostki organizacyjnej zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="5c5c3-133">Stawki kosztów są zwykle oparte na paśmie wynagrodzenia pracownika i na jednostce organizacyjnej, do której pracownik należy.</span><span class="sxs-lookup"><span data-stu-id="5c5c3-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="5c5c3-134">W tym przykładzie tabele stawek rozliczania i stawek kosztów wyglądają następująco:</span><span class="sxs-lookup"><span data-stu-id="5c5c3-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="5c5c3-135">**Przykładowe stawki rozliczania**</span><span class="sxs-lookup"><span data-stu-id="5c5c3-135">**Sample bill rates**</span></span>

| <span data-ttu-id="5c5c3-136">Rola</span><span class="sxs-lookup"><span data-stu-id="5c5c3-136">Role</span></span>        | <span data-ttu-id="5c5c3-137">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="5c5c3-137">Org Unit</span></span>    |<span data-ttu-id="5c5c3-138">Jednostka</span><span class="sxs-lookup"><span data-stu-id="5c5c3-138">Unit</span></span>      |<span data-ttu-id="5c5c3-139">Cena</span><span class="sxs-lookup"><span data-stu-id="5c5c3-139">Price</span></span>      |<span data-ttu-id="5c5c3-140">Waluta</span><span class="sxs-lookup"><span data-stu-id="5c5c3-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5c5c3-141">Dla deweloperów</span><span class="sxs-lookup"><span data-stu-id="5c5c3-141">Developer</span></span>   | <span data-ttu-id="5c5c3-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5c5c3-142">Contoso US</span></span>  |<span data-ttu-id="5c5c3-143">Hour</span><span class="sxs-lookup"><span data-stu-id="5c5c3-143">Hour</span></span> | <span data-ttu-id="5c5c3-144">200</span><span class="sxs-lookup"><span data-stu-id="5c5c3-144">200</span></span>|<span data-ttu-id="5c5c3-145">USD</span><span class="sxs-lookup"><span data-stu-id="5c5c3-145">USD</span></span>     |
| <span data-ttu-id="5c5c3-146">Dla deweloperów</span><span class="sxs-lookup"><span data-stu-id="5c5c3-146">Developer</span></span>   | <span data-ttu-id="5c5c3-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="5c5c3-147">Contoso India</span></span> |<span data-ttu-id="5c5c3-148">Hour</span><span class="sxs-lookup"><span data-stu-id="5c5c3-148">Hour</span></span>|   <span data-ttu-id="5c5c3-149">112</span><span class="sxs-lookup"><span data-stu-id="5c5c3-149">112</span></span>|<span data-ttu-id="5c5c3-150">USD</span><span class="sxs-lookup"><span data-stu-id="5c5c3-150">USD</span></span>     |


<span data-ttu-id="5c5c3-151">**Przykładowe stawki kosztów**</span><span class="sxs-lookup"><span data-stu-id="5c5c3-151">**Sample cost rates**</span></span>

| <span data-ttu-id="5c5c3-152">Pasmo wynagrodzenia</span><span class="sxs-lookup"><span data-stu-id="5c5c3-152">Salary Band</span></span>     | <span data-ttu-id="5c5c3-153">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="5c5c3-153">Org Unit</span></span>    |<span data-ttu-id="5c5c3-154">Jednostka</span><span class="sxs-lookup"><span data-stu-id="5c5c3-154">Unit</span></span>      |<span data-ttu-id="5c5c3-155">Cena</span><span class="sxs-lookup"><span data-stu-id="5c5c3-155">Price</span></span>      |<span data-ttu-id="5c5c3-156">Waluta</span><span class="sxs-lookup"><span data-stu-id="5c5c3-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5c5c3-157">Moja firma_pasmo1</span><span class="sxs-lookup"><span data-stu-id="5c5c3-157">My company_Band1</span></span> | <span data-ttu-id="5c5c3-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5c5c3-158">Contoso US</span></span>  |<span data-ttu-id="5c5c3-159">Hour</span><span class="sxs-lookup"><span data-stu-id="5c5c3-159">Hour</span></span> | <span data-ttu-id="5c5c3-160">145</span><span class="sxs-lookup"><span data-stu-id="5c5c3-160">145</span></span>|<span data-ttu-id="5c5c3-161">USD</span><span class="sxs-lookup"><span data-stu-id="5c5c3-161">USD</span></span>     |
| <span data-ttu-id="5c5c3-162">Moja firma_pasmo2</span><span class="sxs-lookup"><span data-stu-id="5c5c3-162">My company_Band2</span></span> | <span data-ttu-id="5c5c3-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="5c5c3-163">Contoso India</span></span> |<span data-ttu-id="5c5c3-164">Hour</span><span class="sxs-lookup"><span data-stu-id="5c5c3-164">Hour</span></span>|   <span data-ttu-id="5c5c3-165">67</span><span class="sxs-lookup"><span data-stu-id="5c5c3-165">67</span></span>|<span data-ttu-id="5c5c3-166">USD</span><span class="sxs-lookup"><span data-stu-id="5c5c3-166">USD</span></span>     |
