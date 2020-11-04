---
title: Określenie typu wdrażania
description: W tym temacie zamieszczono informacje pozwalające wybrać odpowiedni typ wdrożenia Project Operations dla Twojej firmy.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082016"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="7fc2e-103">Określenie typu wdrażania</span><span class="sxs-lookup"><span data-stu-id="7fc2e-103">Determine your deployment type</span></span>

<span data-ttu-id="7fc2e-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="7fc2e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fc2e-105">Po zakupieniu licencji, zacznij tutaj, aby określić najlepszy model wdrażania Dynamics 365 Project Operations przy użyciu [Przepływu instalacji nadzorowanej](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="7fc2e-106">Po zakończeniu przepływu instalacji nadzorowanej, aby ją zakończyć, nastąpi przekierowanie do odpowiedniego portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="7fc2e-107">Więcej informacji na ten temat można znaleźć w części dotyczącej wdrożenia programu.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="7fc2e-108">Istniejący klienci systemu Dynamics — korzystając z Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7fc2e-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="7fc2e-109">Project Operations obejmuje funkcje dostarczone z automatyzacją usługi Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="7fc2e-110">W przyszłości dla tych klientów zostanie wydana ścieżka uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="7fc2e-111">Obecni klienci Dynamics 365 Finance korzystający z programu Project Management and Accounting</span><span class="sxs-lookup"><span data-stu-id="7fc2e-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="7fc2e-112">Istniejący użytkownicy Finance, którzy korzystają z Project Management and Accounting mogą dalej korzystać z programu w taki sam sposób, jak dotychczas.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="7fc2e-113">Zobacz [Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne](#pma).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="7fc2e-114">Typy wdrożenia</span><span class="sxs-lookup"><span data-stu-id="7fc2e-114">Deployment types</span></span>
<span data-ttu-id="7fc2e-115">Project Operations obsługuje wiele opcji wdrażania spełniających wymagania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="7fc2e-116">Niezależnie od tego, czy jesteś nowym, czy istniejącym klientem Dynamics 365, Project Operations pomoże Ci w Twojej pracy.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="7fc2e-117">Nasz [kwestionariusz wdrażania](https://aka.ms/provisionprojectoperations) pomoże Ci w określeniu odpowiednich wdrożeń.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="7fc2e-118">Wyniki pozwolą CI wybrać jeden z następujących typów wdrożeń:</span><span class="sxs-lookup"><span data-stu-id="7fc2e-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="7fc2e-119">Wdrożenie uproszczone — od okazji do faktury pro forma</span><span class="sxs-lookup"><span data-stu-id="7fc2e-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="7fc2e-120">Project Operations — zasoby / scenariusze nieobejmujące magazynowania</span><span class="sxs-lookup"><span data-stu-id="7fc2e-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="7fc2e-121">Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="7fc2e-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="7fc2e-122">Project Operations obsługuje scenariusze dotyczące zleceń magazynowania / zlecenia produkcyjnego i scenariusze oparte na zasobach / zasobach niemagazynowanych w tym samym środowisku za pośrednictwem konfiguracji na poziomie firmy.</span><span class="sxs-lookup"><span data-stu-id="7fc2e-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="7fc2e-123">Firma Contoso może na przykład użyć funkcji zarządzania stanami magazynowymi/zleceniami produkcyjnymi swojej placówki w Stanach Zjednoczonych (osoba prawna = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="7fc2e-124">Firma Contoso może użyć funkcji zarządzania stanami magazynowymi/zleceniami produkcyjnymi swojej placówki w Wielkiej Brytanii (osoba prawna = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="7fc2e-125">Wdrożenie uproszczone — od okazji do faktury pro forma</span><span class="sxs-lookup"><span data-stu-id="7fc2e-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="7fc2e-126">We wdrożeniu uproszczonym dostępne są następujące możliwości:</span><span class="sxs-lookup"><span data-stu-id="7fc2e-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="7fc2e-127">Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web</span><span class="sxs-lookup"><span data-stu-id="7fc2e-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7fc2e-128">Wielowymiarowe ceny</span><span class="sxs-lookup"><span data-stu-id="7fc2e-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7fc2e-129">Zunifikowane zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="7fc2e-129">Unified Resource Management</span></span>
- <span data-ttu-id="7fc2e-130">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="7fc2e-130">Time Tracking</span></span>
- <span data-ttu-id="7fc2e-131">Podstawowe wydatki</span><span class="sxs-lookup"><span data-stu-id="7fc2e-131">Basic Expense</span></span>
- <span data-ttu-id="7fc2e-132">Propozycja faktury</span><span class="sxs-lookup"><span data-stu-id="7fc2e-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7fc2e-133">Kroki wdrażania</span><span class="sxs-lookup"><span data-stu-id="7fc2e-133">Deployment steps</span></span>
<span data-ttu-id="7fc2e-134">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7fc2e-135">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](lite-preview-subscription-sign-up.md) i [Ustanowienie nowego środowiska](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="7fc2e-136">Project Operations — zasoby / scenariusze nieobejmujące magazynowania</span><span class="sxs-lookup"><span data-stu-id="7fc2e-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="7fc2e-137">Project Operations dotyczące scenariuszy zasobów i zasobów niemagazynowanych oferują następujące możliwości:</span><span class="sxs-lookup"><span data-stu-id="7fc2e-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="7fc2e-138">Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web</span><span class="sxs-lookup"><span data-stu-id="7fc2e-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7fc2e-139">Wielowymiarowe ceny</span><span class="sxs-lookup"><span data-stu-id="7fc2e-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7fc2e-140">Zunifikowane zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="7fc2e-140">Unified Resource Management</span></span>
- <span data-ttu-id="7fc2e-141">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="7fc2e-141">Time Tracking</span></span>
- <span data-ttu-id="7fc2e-142">Podstawowe wydatki</span><span class="sxs-lookup"><span data-stu-id="7fc2e-142">Basic Expense</span></span>
- <span data-ttu-id="7fc2e-143">Wydatek pełny</span><span class="sxs-lookup"><span data-stu-id="7fc2e-143">Full Expense</span></span>
- <span data-ttu-id="7fc2e-144">OCR paragonów</span><span class="sxs-lookup"><span data-stu-id="7fc2e-144">Receipt OCR</span></span>
- <span data-ttu-id="7fc2e-145">Pełne fakturowanie</span><span class="sxs-lookup"><span data-stu-id="7fc2e-145">Full Invoicing</span></span>
- <span data-ttu-id="7fc2e-146">Ujmowanie przychodów</span><span class="sxs-lookup"><span data-stu-id="7fc2e-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7fc2e-147">Kroki wdrażania</span><span class="sxs-lookup"><span data-stu-id="7fc2e-147">Deployment steps</span></span>
<span data-ttu-id="7fc2e-148">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7fc2e-149">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](resource-sign-up-preview-subscription.md) i [Ustanowienie nowego środowiska](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="7fc2e-150">Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="7fc2e-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="7fc2e-151">Planowanie projektu za pomocą WBS</span><span class="sxs-lookup"><span data-stu-id="7fc2e-151">Project planning using WBS</span></span>
- <span data-ttu-id="7fc2e-152">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="7fc2e-152">Resource Management</span></span>
- <span data-ttu-id="7fc2e-153">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="7fc2e-153">Time Tracking</span></span>
- <span data-ttu-id="7fc2e-154">Wydatek pełny</span><span class="sxs-lookup"><span data-stu-id="7fc2e-154">Full Expense</span></span>
- <span data-ttu-id="7fc2e-155">OCR paragonów</span><span class="sxs-lookup"><span data-stu-id="7fc2e-155">Receipt OCR</span></span>
- <span data-ttu-id="7fc2e-156">Pełne fakturowanie</span><span class="sxs-lookup"><span data-stu-id="7fc2e-156">Full Invoicing</span></span>
- <span data-ttu-id="7fc2e-157">Ujmowanie przychodów</span><span class="sxs-lookup"><span data-stu-id="7fc2e-157">Revenue Recognition</span></span>
- <span data-ttu-id="7fc2e-158">Zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="7fc2e-158">Production Orders</span></span>
- <span data-ttu-id="7fc2e-159">Obsługa materiałów</span><span class="sxs-lookup"><span data-stu-id="7fc2e-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7fc2e-160">Kroki wdrażania</span><span class="sxs-lookup"><span data-stu-id="7fc2e-160">Deployment steps</span></span>
<span data-ttu-id="7fc2e-161">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7fc2e-162">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Ustanowienie nowego środowiska](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7fc2e-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

