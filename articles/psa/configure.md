---
title: Skonfiguruj Project Service Automation
description: Kroki związane z konfigurowaniem usługi Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129196"
---
# <a name="configure-project-service"></a><span data-ttu-id="7db64-103">Konfiguruj Project Service</span><span class="sxs-lookup"><span data-stu-id="7db64-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7db64-104">Przed skorzystaniem z możliwości automatyzacji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] w [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] do zarządzania kontami, projektami i zasobami, musisz wykonać kilka kroków konfiguracyjnych, aby upewnić się, że rozwiązanie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] odpowiada potrzebom Twojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="7db64-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="7db64-105">Kroki te obejmują:</span><span class="sxs-lookup"><span data-stu-id="7db64-105">These steps include:</span></span>  
  
-   <span data-ttu-id="7db64-106">[Skonfiguruj jednostki czasu](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="7db64-107">Skonfiguruj jednostki czasu w katalogu produktów, który ma być używany jako podstawa do planowania oraz fakturowania projektów.</span><span class="sxs-lookup"><span data-stu-id="7db64-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="7db64-108">[Ustaw waluty i kursy wymiany](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="7db64-109">Ustaw waluty, które będą używane dla projektów.</span><span class="sxs-lookup"><span data-stu-id="7db64-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="7db64-110">[Utwórz jednostki organizacyjne](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="7db64-111">Ustaw grupy, których firma używa do podziału działalności, w oparciu o geografię, funkcje biznesowe lub inne logiczne podziały.</span><span class="sxs-lookup"><span data-stu-id="7db64-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="7db64-112">[Ustaw częstotliwość sporządzania faktur](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="7db64-113">Ustaw okresy czasu, których chcesz używać podczas rozliczania klientów.</span><span class="sxs-lookup"><span data-stu-id="7db64-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="7db64-114">[Konfiguruj kategorie transakcji](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="7db64-115">Ustaw kategorie transakcji, które konsultanci mogą obciążać kosztami ich godzin podlegających rozliczeniu i niepodlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="7db64-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="7db64-116">[Konfiguruj kategorie wydatków](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="7db64-117">Ustaw kategorie, które konsultanci mogą obciążać kosztami ich godzin podlegających rozliczeniu i niepodlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="7db64-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="7db64-118">[Utwórz katalog produktów](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="7db64-119">Dodaj produkty, które sprzedajesz, takie jak licencje na oprogramowanie, do katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="7db64-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="7db64-120">[Utwórz cennik](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="7db64-121">Skonfiguruj różne cenniki, w zależności od tego, ile chcesz naliczyć klientom za każdą z ról, której wymaga ich projekt.</span><span class="sxs-lookup"><span data-stu-id="7db64-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="7db64-122">[Konfigurowanie zasobów](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7db64-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="7db64-123">Dodaj umiejętności, biegłości, role zasobów i inne informacje o zasobach, które będą potrzebne dla projektów.</span><span class="sxs-lookup"><span data-stu-id="7db64-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7db64-124">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="7db64-124">See Also</span></span>  
 <span data-ttu-id="7db64-125">[Przewodnik po rozwiązaniu Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="7db64-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="7db64-126">[Skonfiguruj Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="7db64-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="7db64-127">[Przewodnik menedżera kont](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7db64-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="7db64-128">[Przewodnik menedżera projektów](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7db64-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="7db64-129">[Przewodnik menedżera zasobów](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7db64-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="7db64-130">Przewodnik dotyczący czasu, wydatków i współpracy</span><span class="sxs-lookup"><span data-stu-id="7db64-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)