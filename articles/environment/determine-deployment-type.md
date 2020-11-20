---
title: Określenie typu wdrażania
description: W tym temacie zamieszczono informacje pozwalające wybrać odpowiedni typ wdrożenia Project Operations dla Twojej firmy.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401231"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="07ce8-103">Określenie typu wdrażania</span><span class="sxs-lookup"><span data-stu-id="07ce8-103">Determine your deployment type</span></span>

<span data-ttu-id="07ce8-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="07ce8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07ce8-105">Po zakupieniu licencji, zacznij tutaj, aby określić najlepszy model wdrażania Dynamics 365 Project Operations przy użyciu [Przepływu instalacji nadzorowanej](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="07ce8-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="07ce8-106">Po zakończeniu przepływu instalacji nadzorowanej, aby ją zakończyć, nastąpi przekierowanie do odpowiedniego portalu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="07ce8-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="07ce8-107">Więcej informacji na ten temat można znaleźć w części dotyczącej wdrożenia programu.</span><span class="sxs-lookup"><span data-stu-id="07ce8-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="07ce8-108">Istniejący klienci systemu Dynamics — korzystając z Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="07ce8-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="07ce8-109">Project Operations obejmuje funkcje dostarczone z automatyzacją usługi Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="07ce8-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="07ce8-110">Ścieżka aktualizacji zostanie wydana dla tych klientów w pierwszej fazie wydania 2021.</span><span class="sxs-lookup"><span data-stu-id="07ce8-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="07ce8-111">Obecni klienci Dynamics 365 Finance korzystający z programu Project Management and Accounting</span><span class="sxs-lookup"><span data-stu-id="07ce8-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="07ce8-112">Obecni klienci Finance, którzy używają funkcji zarządzania projektami i księgowości, mogą nadal korzystać z niej w obecnej postaci.</span><span class="sxs-lookup"><span data-stu-id="07ce8-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="07ce8-113">Zobacz [Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne](#pma).</span><span class="sxs-lookup"><span data-stu-id="07ce8-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="07ce8-114">Typy wdrożenia</span><span class="sxs-lookup"><span data-stu-id="07ce8-114">Deployment types</span></span>
<span data-ttu-id="07ce8-115">Project Operations obsługuje wiele opcji wdrażania spełniających wymagania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="07ce8-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="07ce8-116">Niezależnie od tego, czy jesteś nowym, czy istniejącym klientem Dynamics 365, Project Operations pomoże Ci w Twojej pracy.</span><span class="sxs-lookup"><span data-stu-id="07ce8-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="07ce8-117">Nasz [kwestionariusz wdrażania](https://aka.ms/provisionprojectoperations) pomoże Ci w określeniu odpowiednich wdrożeń.</span><span class="sxs-lookup"><span data-stu-id="07ce8-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="07ce8-118">Wyniki pozwolą CI wybrać jeden z następujących typów wdrożeń:</span><span class="sxs-lookup"><span data-stu-id="07ce8-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="07ce8-119">Wdrożenie uproszczone — od okazji do faktury pro forma</span><span class="sxs-lookup"><span data-stu-id="07ce8-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="07ce8-120">Project Operations — zasoby / scenariusze nieobejmujące magazynowania</span><span class="sxs-lookup"><span data-stu-id="07ce8-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="07ce8-121">Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="07ce8-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="07ce8-122">Project Operations obsługuje scenariusze dotyczące zleceń magazynowania / zlecenia produkcyjnego i scenariusze oparte na zasobach / zasobach niemagazynowanych w tym samym środowisku za pośrednictwem konfiguracji na poziomie firmy.</span><span class="sxs-lookup"><span data-stu-id="07ce8-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="07ce8-123">Firma Contoso może na przykład użyć funkcji zarządzania stanami magazynowymi/zleceniami produkcyjnymi swojej placówki w Stanach Zjednoczonych (osoba prawna = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="07ce8-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="07ce8-124">Firma Contoso może użyć funkcji zarządzania stanami magazynowymi/zleceniami produkcyjnymi swojej placówki w Wielkiej Brytanii (osoba prawna = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="07ce8-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="07ce8-125">Wdrożenie uproszczone — od okazji do faktury pro forma</span><span class="sxs-lookup"><span data-stu-id="07ce8-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="07ce8-126">We wdrożeniu uproszczonym dostępne są następujące możliwości:</span><span class="sxs-lookup"><span data-stu-id="07ce8-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="07ce8-127">Proces sprzedaży dla projektów, który rozszerza środowisko aplikacji Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="07ce8-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="07ce8-128">Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web</span><span class="sxs-lookup"><span data-stu-id="07ce8-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="07ce8-129">Wielowymiarowe ceny</span><span class="sxs-lookup"><span data-stu-id="07ce8-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="07ce8-130">Zunifikowane zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="07ce8-130">Unified resource management</span></span>
- <span data-ttu-id="07ce8-131">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="07ce8-131">Time tracking</span></span>
- <span data-ttu-id="07ce8-132">Podstawowe wydatki</span><span class="sxs-lookup"><span data-stu-id="07ce8-132">Basic expense</span></span>
- <span data-ttu-id="07ce8-133">Proforma i fakturowanie dla klientów</span><span class="sxs-lookup"><span data-stu-id="07ce8-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="07ce8-134">Kroki wdrażania</span><span class="sxs-lookup"><span data-stu-id="07ce8-134">Deployment steps</span></span>
<span data-ttu-id="07ce8-135">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="07ce8-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="07ce8-136">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](lite-preview-subscription-sign-up.md) i [Ustanowienie nowego środowiska](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="07ce8-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="07ce8-137">Project Operations — zasoby / scenariusze nieobejmujące magazynowania</span><span class="sxs-lookup"><span data-stu-id="07ce8-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="07ce8-138">Project Operations dotyczące scenariuszy zasobów i zasobów niemagazynowanych oferują następujące możliwości:</span><span class="sxs-lookup"><span data-stu-id="07ce8-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="07ce8-139">Proces sprzedaży dla projektów, który rozszerza aplikację Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="07ce8-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="07ce8-140">Planowanie projektów przy użyciu programu Microsoft Project dla sieci Web</span><span class="sxs-lookup"><span data-stu-id="07ce8-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="07ce8-141">Wielowymiarowe ceny</span><span class="sxs-lookup"><span data-stu-id="07ce8-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="07ce8-142">Zunifikowane zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="07ce8-142">Unified resource management</span></span>
- <span data-ttu-id="07ce8-143">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="07ce8-143">Time tracking</span></span>
- <span data-ttu-id="07ce8-144">Podstawowe wydatki</span><span class="sxs-lookup"><span data-stu-id="07ce8-144">Basic expense</span></span>
- <span data-ttu-id="07ce8-145">Wydatek pełny</span><span class="sxs-lookup"><span data-stu-id="07ce8-145">Full expense</span></span>
- <span data-ttu-id="07ce8-146">OCR paragonów</span><span class="sxs-lookup"><span data-stu-id="07ce8-146">Receipt OCR</span></span>
- <span data-ttu-id="07ce8-147">Proforma i fakturowanie dla klientów</span><span class="sxs-lookup"><span data-stu-id="07ce8-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="07ce8-148">Rozpoznawanie przychodów dla projektów</span><span class="sxs-lookup"><span data-stu-id="07ce8-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="07ce8-149">Kroki wdrażania</span><span class="sxs-lookup"><span data-stu-id="07ce8-149">Deployment steps</span></span>
<span data-ttu-id="07ce8-150">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="07ce8-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="07ce8-151">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](resource-sign-up-preview-subscription.md) i [Ustanowienie nowego środowiska](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="07ce8-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="07ce8-152">Project Operations — scenariusze obejmujące magazynowanie / zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="07ce8-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="07ce8-153">Planowanie projektu za pomocą WBS</span><span class="sxs-lookup"><span data-stu-id="07ce8-153">Project planning using WBS</span></span>
- <span data-ttu-id="07ce8-154">Zarządzanie zasobami</span><span class="sxs-lookup"><span data-stu-id="07ce8-154">Resource Management</span></span>
- <span data-ttu-id="07ce8-155">Śledzenie czasu</span><span class="sxs-lookup"><span data-stu-id="07ce8-155">Time Tracking</span></span>
- <span data-ttu-id="07ce8-156">Wydatek pełny</span><span class="sxs-lookup"><span data-stu-id="07ce8-156">Full Expense</span></span>
- <span data-ttu-id="07ce8-157">OCR paragonów</span><span class="sxs-lookup"><span data-stu-id="07ce8-157">Receipt OCR</span></span>
- <span data-ttu-id="07ce8-158">Pełne fakturowanie</span><span class="sxs-lookup"><span data-stu-id="07ce8-158">Full Invoicing</span></span>
- <span data-ttu-id="07ce8-159">Ujmowanie przychodów</span><span class="sxs-lookup"><span data-stu-id="07ce8-159">Revenue Recognition</span></span>
- <span data-ttu-id="07ce8-160">Zlecenia produkcyjne</span><span class="sxs-lookup"><span data-stu-id="07ce8-160">Production Orders</span></span>
- <span data-ttu-id="07ce8-161">Obsługa materiałów</span><span class="sxs-lookup"><span data-stu-id="07ce8-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="07ce8-162">Kroki wdrażania</span><span class="sxs-lookup"><span data-stu-id="07ce8-162">Deployment steps</span></span>
<span data-ttu-id="07ce8-163">Wyznaczanie najlepszego modelu wdrażania Project Operations przy użyciu [kwestionariusza rozmieszczenia](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="07ce8-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="07ce8-164">W tym wdrożeniu zobacz [Tworzenie konta dla subskrypcji w wersji zapoznawczej](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Ustanowienie nowego środowiska](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="07ce8-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

