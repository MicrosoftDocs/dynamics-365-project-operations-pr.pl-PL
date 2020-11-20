---
title: Zarządzanie szansami sprzedaży opartymi na projektach
description: W tym temacie zamieszczono informacje dotyczące pracy z szansami sprzedaży związanymi z projektami.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5a8bfea5540432a62d7075443cf237571bfa4de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118486"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="b733a-103">Zarządzanie szansami sprzedaży opartymi na projektach</span><span class="sxs-lookup"><span data-stu-id="b733a-103">Manage project-based opportunities</span></span>

<span data-ttu-id="b733a-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="b733a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b733a-105">Przedsiębiorstwa oparte na projektach zwykle mają swoje działania w wielu krajach i lokalizacjach.</span><span class="sxs-lookup"><span data-stu-id="b733a-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="b733a-106">Koszty wykonania i dostawy projektu mogą się różnić zależnie od tego, gdzie projekt jest wykonywany, i który oddział się nim zajmuje.</span><span class="sxs-lookup"><span data-stu-id="b733a-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="b733a-107">Może to wpłynąć na marże transakcji.</span><span class="sxs-lookup"><span data-stu-id="b733a-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="b733a-108">Dostarczanie usług opartych na projektach zwykle polega na dużym poziomie zasobów ludzkich, znaczących kosztach podróży, kosztach materiałowych i innych kosztach.</span><span class="sxs-lookup"><span data-stu-id="b733a-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="b733a-109">Szanse sprzedaży w programie Dynamics 365 Project Operations są utworzone wraz z rozszerzeniami szans sprzedaży w Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b733a-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="b733a-110">Temat zawiera szczegółowe informacje o różnych polach i regułach biznesowych dołączonych do dodatkowych funkcji wymaganych przez firmy oparte na projektach, aby zarządzać szansami sprzedaży opartymi na projektach.</span><span class="sxs-lookup"><span data-stu-id="b733a-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="b733a-111">Wyświetlanie wszystkich szans sprzedaży opartych na projektach</span><span class="sxs-lookup"><span data-stu-id="b733a-111">View all project-based opportunities</span></span>

<span data-ttu-id="b733a-112">Listę wszystkich szans sprzedaży opartych na projektach można zobaczyć na stronie listy **Szansy sprzedaży**.</span><span class="sxs-lookup"><span data-stu-id="b733a-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="b733a-113">Wybierz kolejno pozycje **Sprzedaż** > **Szanse sprzedaży**.</span><span class="sxs-lookup"><span data-stu-id="b733a-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="b733a-114">Użyj **Przełączników widoku**, aby wybrać inne filtrowane widoki szans sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b733a-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="b733a-115">Aby skonfigurować te widoki i opcje nawigacji, można utworzyć własne widoki z kryteriami filtrowania niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="b733a-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="b733a-116">Szanse sprzedaży projektu mogą być tworzone lub usuwane na stronie listy lub na stronie szczegółów.</span><span class="sxs-lookup"><span data-stu-id="b733a-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="b733a-117">Przepływ procesów biznesowych w transakcjach opartych na projektach</span><span class="sxs-lookup"><span data-stu-id="b733a-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="b733a-118">Poniższe przepływy procesów biznesowych są obsługiwane w przypadku transakcji opartych na projektach w Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b733a-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="b733a-119">Proces biznesowy Od potencjalnego klienta do szansy sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="b733a-120">Proces sprzedaży w ramach szansy sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="b733a-121">Proces biznesowy — od potencjalnego klienta do szansy sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="b733a-122">Proces biznesowy — od potencjalnego klienta do szansy sprzedaży obsługuje następujące etapy:</span><span class="sxs-lookup"><span data-stu-id="b733a-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="b733a-123">Etap</span><span class="sxs-lookup"><span data-stu-id="b733a-123">Stage</span></span> | <span data-ttu-id="b733a-124">Mapowana encja</span><span class="sxs-lookup"><span data-stu-id="b733a-124">Mapped entity</span></span> | <span data-ttu-id="b733a-125">Funkcje</span><span class="sxs-lookup"><span data-stu-id="b733a-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b733a-126">Kwalifikuj</span><span class="sxs-lookup"><span data-stu-id="b733a-126">Qualify</span></span> | <span data-ttu-id="b733a-127">Potencjalny klient</span><span class="sxs-lookup"><span data-stu-id="b733a-127">Lead</span></span> | <span data-ttu-id="b733a-128">Kwalifikowanie potencjalnego klienta tworzy konto, kontakt oraz szansę sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b733a-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="b733a-129">Opracuj</span><span class="sxs-lookup"><span data-stu-id="b733a-129">Develop</span></span> | <span data-ttu-id="b733a-130">Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-130">Opportunity</span></span> | <span data-ttu-id="b733a-131">Rozwijanie szansy sprzedaży w celu dodania informacji o związanej pracy, kluczowych udziałowcach i konkurencji.</span><span class="sxs-lookup"><span data-stu-id="b733a-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="b733a-132">Zaproponuj</span><span class="sxs-lookup"><span data-stu-id="b733a-132">Propose</span></span> | <span data-ttu-id="b733a-133">Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-133">Opportunity</span></span> | <span data-ttu-id="b733a-134">Opracowanie i uzyskanie zgody zespołu na przegląd wewnętrzny.</span><span class="sxs-lookup"><span data-stu-id="b733a-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="b733a-135">Zamykanie</span><span class="sxs-lookup"><span data-stu-id="b733a-135">Close</span></span> | <span data-ttu-id="b733a-136">Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-136">Opportunity</span></span> | <span data-ttu-id="b733a-137">Wykorzystaj szansę sprzedaży, aby zamknąć ofertę.</span><span class="sxs-lookup"><span data-stu-id="b733a-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="b733a-138">Proces sprzedaży w ramach szansy sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-138">Opportunity sales process</span></span>
<span data-ttu-id="b733a-139">Proces sprzedaży szans sprzedaży w Project Operations jest rozszerzeniem przepływu pracy procesu sprzedaży w aplikacji Sales.</span><span class="sxs-lookup"><span data-stu-id="b733a-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="b733a-140">Ten proces biznesowy został zaprojektowany z myślą o obsłudze poniższych etapów w szansie sprzedaży opartej na projekcie.</span><span class="sxs-lookup"><span data-stu-id="b733a-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="b733a-141">Etap</span><span class="sxs-lookup"><span data-stu-id="b733a-141">Stage</span></span> | <span data-ttu-id="b733a-142">Mapowana encja</span><span class="sxs-lookup"><span data-stu-id="b733a-142">Mapped entity</span></span> | <span data-ttu-id="b733a-143">Funkcje</span><span class="sxs-lookup"><span data-stu-id="b733a-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b733a-144">Kwalifikuj</span><span class="sxs-lookup"><span data-stu-id="b733a-144">Qualify</span></span> | <span data-ttu-id="b733a-145">Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b733a-145">Opportunity</span></span> | <span data-ttu-id="b733a-146">Kwalifikowanie potencjalnego klienta tworzy konto, kontakt oraz szansę sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b733a-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="b733a-147">Zaproponuj</span><span class="sxs-lookup"><span data-stu-id="b733a-147">Propose</span></span> | <span data-ttu-id="b733a-148">Oferta</span><span class="sxs-lookup"><span data-stu-id="b733a-148">Quote</span></span> | <span data-ttu-id="b733a-149">Opracowanie za pomocą oferty projektu i uzyskanie zgody zespołu na przegląd wewnętrzny.</span><span class="sxs-lookup"><span data-stu-id="b733a-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="b733a-150">Kontrakt</span><span class="sxs-lookup"><span data-stu-id="b733a-150">Contract</span></span> | <span data-ttu-id="b733a-151">Kontrakt projektu</span><span class="sxs-lookup"><span data-stu-id="b733a-151">Project Contract</span></span> | <span data-ttu-id="b733a-152">Aby utworzyć kontrakt i rozpocząć jego realizację, należy wygrać ofertę.</span><span class="sxs-lookup"><span data-stu-id="b733a-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="b733a-153">Zamykanie</span><span class="sxs-lookup"><span data-stu-id="b733a-153">Close</span></span> | <span data-ttu-id="b733a-154">Kontrakt projektu</span><span class="sxs-lookup"><span data-stu-id="b733a-154">Project Contract</span></span> | <span data-ttu-id="b733a-155">Z powodzeniem zakończ pracę i zamknij kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="b733a-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="b733a-156">Jeśli transakcja oparta na projekcie została wyzwolona przez potencjalnego klienta, pierwszeństwo w procesie biznesowym ma proces „Od potencjalnego klienta do szansy sprzedaży”.</span><span class="sxs-lookup"><span data-stu-id="b733a-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="b733a-157">Jeśli transakcja oparta na projekcie została wyzwolona przez szansę sprzedaży, pierwszeństwo w procesie biznesowym ma proces „Szansy sprzedaży”.</span><span class="sxs-lookup"><span data-stu-id="b733a-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="b733a-158">Użytkownik może edytować przepływ procesów biznesowych produktu lub tworzyć własne przepływy procesów biznesowych umożliwiające śledzenie procesu sprzedaży w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="b733a-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="b733a-159">Aby uzyskać więcej informacji na temat przepływu procesów biznesowych, zobacz [Omówienie przepływu procesów biznesowych](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="b733a-159">For more information about the business process flow, see [Business process flows overview](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>