---
title: Typy wdrożenia
description: W tym temacie zamieszczono informacje pozwalające wybrać odpowiedni typ wdrożenia Project Operations dla Twojej firmy.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949008"
---
# <a name="deployment-types"></a><span data-ttu-id="04bf2-103">Typy wdrożenia</span><span class="sxs-lookup"><span data-stu-id="04bf2-103">Deployment types</span></span>

<span data-ttu-id="04bf2-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="04bf2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04bf2-105">Po zakupieniu licencji, zacznij tutaj, aby określić najlepszy model wdrażania Dynamics 365 Project Operations przy użyciu [Przepływu instalacji nadzorowanej](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="04bf2-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="04bf2-106">Po zakończeniu przepływu instalacji nadzorowanej, aby ją zakończyć, nastąpi przekierowanie do odpowiedniego portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="04bf2-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="04bf2-107">Więcej informacji na ten temat można znaleźć w części dotyczącej wdrożenia programu.</span><span class="sxs-lookup"><span data-stu-id="04bf2-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="04bf2-108">Istniejący klienci systemu Dynamics — korzystając z Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="04bf2-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="04bf2-109">Project Operations obejmuje funkcje dostarczone z automatyzacją usługi Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="04bf2-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="04bf2-110">W przyszłości dla tych klientów zostanie wydana ścieżka uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="04bf2-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="04bf2-111">Obecni klienci Dynamics 365 Finance korzystający z programu Project Management and Accounting</span><span class="sxs-lookup"><span data-stu-id="04bf2-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="04bf2-112">Istniejący użytkownicy Finance, którzy korzystają z Project Management and Accounting mogą dalej korzystać z programu w taki sam sposób, jak dotychczas.</span><span class="sxs-lookup"><span data-stu-id="04bf2-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="04bf2-113">Zobacz [Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne](#pma).</span><span class="sxs-lookup"><span data-stu-id="04bf2-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="04bf2-114">Project Operations obsługuje wiele opcji wdrażania spełniających wymagania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="04bf2-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="04bf2-115">Niezależnie od tego, czy jesteś nowym, czy istniejącym klientem Dynamics 365, Project Operations pomoże Ci w Twojej pracy.</span><span class="sxs-lookup"><span data-stu-id="04bf2-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="04bf2-116">Nasz [kwestionariusz wdrażania](https://aka.ms/provisionprojectoperations) pomoże Ci w określeniu odpowiednich wdrożeń.</span><span class="sxs-lookup"><span data-stu-id="04bf2-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="04bf2-117">Wyniki pozwolą CI wybrać jeden z następujących typów wdrożeń:</span><span class="sxs-lookup"><span data-stu-id="04bf2-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="04bf2-118">Wdrożenie uproszczone — od okazji do faktury pro forma</span><span class="sxs-lookup"><span data-stu-id="04bf2-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="04bf2-119">Project Operations — zasoby / scenariusze nieobejmujące magazynowania</span><span class="sxs-lookup"><span data-stu-id="04bf2-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="04bf2-120">Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="04bf2-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="04bf2-121">Project Operations obsługuje scenariusze dotyczące zleceń magazynowania / zlecenia produkcyjnego i scenariusze oparte na zasobach / zasobach niemagazynowanych w tym samym środowisku za pośrednictwem konfiguracji na poziomie firmy.</span><span class="sxs-lookup"><span data-stu-id="04bf2-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="04bf2-122">Firma Contoso może na przykład skorzystać z funkcji zarządzania stanami magazynowymi/zleceniami produkcyjnymi w ramach swojego zakładu produkcji (firma = Contoso Manufacturing United States) i funkcji opartej na zasobach / zasobach niemagazynowanych w ramach swojego zakładu Contoso Robotics Arms w Wielkiej Brytanii (firma = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="04bf2-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="04bf2-123"><a name="lite"><a/>Wdrożenie uproszczone — od okazji do faktury pro forma</span><span class="sxs-lookup"><span data-stu-id="04bf2-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="04bf2-124">We wdrożeniu uproszczonym dostępne są następujące możliwości:</span><span class="sxs-lookup"><span data-stu-id="04bf2-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="04bf2-125">Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web</span><span class="sxs-lookup"><span data-stu-id="04bf2-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="04bf2-126">Wielowymiarowe ceny</span><span class="sxs-lookup"><span data-stu-id="04bf2-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="04bf2-127">Zunifikowane zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="04bf2-127">Unified Resource Management</span></span>
- <span data-ttu-id="04bf2-128">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="04bf2-128">Time Tracking</span></span>
- <span data-ttu-id="04bf2-129">Podstawowe wydatki</span><span class="sxs-lookup"><span data-stu-id="04bf2-129">Basic Expense</span></span>
- <span data-ttu-id="04bf2-130">Propozycja faktury</span><span class="sxs-lookup"><span data-stu-id="04bf2-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="04bf2-131">Kroki wdrażania:</span><span class="sxs-lookup"><span data-stu-id="04bf2-131">Deployment steps:</span></span>
<span data-ttu-id="04bf2-132">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="04bf2-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="04bf2-133">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](lite-preview-subscription-sign-up.md) i [Ustanowienie nowego środowiska](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="04bf2-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="04bf2-134"><a name="integrated"><a/>Project Operations — zasoby / scenariusze nieobejmujące magazynowania</span><span class="sxs-lookup"><span data-stu-id="04bf2-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="04bf2-135">Project Operations dotyczące scenariuszy zasobów i zasobów niemagazynowanych oferują następujące możliwości:</span><span class="sxs-lookup"><span data-stu-id="04bf2-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="04bf2-136">Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web</span><span class="sxs-lookup"><span data-stu-id="04bf2-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="04bf2-137">Wielowymiarowe ceny</span><span class="sxs-lookup"><span data-stu-id="04bf2-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="04bf2-138">Zunifikowane zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="04bf2-138">Unified Resource Management</span></span>
- <span data-ttu-id="04bf2-139">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="04bf2-139">Time Tracking</span></span>
- <span data-ttu-id="04bf2-140">Podstawowe wydatki</span><span class="sxs-lookup"><span data-stu-id="04bf2-140">Basic Expense</span></span>
- <span data-ttu-id="04bf2-141">Wydatek pełny</span><span class="sxs-lookup"><span data-stu-id="04bf2-141">Full Expense</span></span>
- <span data-ttu-id="04bf2-142">OCR paragonów</span><span class="sxs-lookup"><span data-stu-id="04bf2-142">Receipt OCR</span></span>
- <span data-ttu-id="04bf2-143">Pełne fakturowanie</span><span class="sxs-lookup"><span data-stu-id="04bf2-143">Full Invoicing</span></span>
- <span data-ttu-id="04bf2-144">Ujmowanie przychodów</span><span class="sxs-lookup"><span data-stu-id="04bf2-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="04bf2-145">Kroki wdrażania:</span><span class="sxs-lookup"><span data-stu-id="04bf2-145">Deployment steps:</span></span>
<span data-ttu-id="04bf2-146">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="04bf2-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="04bf2-147">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](resource-sign-up-preview-subscription.md) i [Ustanowienie nowego środowiska](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="04bf2-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="04bf2-148">Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="04bf2-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="04bf2-149">Planowanie projektu za pomocą WBS</span><span class="sxs-lookup"><span data-stu-id="04bf2-149">Project planning using WBS</span></span>
- <span data-ttu-id="04bf2-150">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="04bf2-150">Resource Management</span></span>
- <span data-ttu-id="04bf2-151">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="04bf2-151">Time Tracking</span></span>
- <span data-ttu-id="04bf2-152">Wydatek pełny</span><span class="sxs-lookup"><span data-stu-id="04bf2-152">Full Expense</span></span>
- <span data-ttu-id="04bf2-153">OCR paragonów</span><span class="sxs-lookup"><span data-stu-id="04bf2-153">Receipt OCR</span></span>
- <span data-ttu-id="04bf2-154">Pełne fakturowanie</span><span class="sxs-lookup"><span data-stu-id="04bf2-154">Full Invoicing</span></span>
- <span data-ttu-id="04bf2-155">Ujmowanie przychodów</span><span class="sxs-lookup"><span data-stu-id="04bf2-155">Revenue Recognition</span></span>
- <span data-ttu-id="04bf2-156">Zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="04bf2-156">Production Orders</span></span>
- <span data-ttu-id="04bf2-157">Obsługa materiałów</span><span class="sxs-lookup"><span data-stu-id="04bf2-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="04bf2-158">Kroki wdrażania:</span><span class="sxs-lookup"><span data-stu-id="04bf2-158">Deployment steps:</span></span>
<span data-ttu-id="04bf2-159">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="04bf2-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="04bf2-160">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Ustanowienie nowego środowiska](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="04bf2-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



