---
title: Skonfiguruj Project Service Automation
description: Kroki związane z konfigurowaniem usługi Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754309"
---
# <a name="configure-project-service"></a><span data-ttu-id="9b4de-103">Konfiguruj Project Service</span><span class="sxs-lookup"><span data-stu-id="9b4de-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9b4de-104">Przed skorzystaniem z możliwości automatyzacji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] w [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] do zarządzania kontami, projektami i zasobami, musisz wykonać kilka kroków konfiguracyjnych, aby upewnić się, że rozwiązanie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] odpowiada potrzebom Twojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="9b4de-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="9b4de-105">Kroki te obejmują:</span><span class="sxs-lookup"><span data-stu-id="9b4de-105">These steps include:</span></span>  
  
-   <span data-ttu-id="9b4de-106">[Skonfiguruj jednostki czasu](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="9b4de-107">Skonfiguruj jednostki czasu w katalogu produktów, który ma być używany jako podstawa do planowania oraz fakturowania projektów.</span><span class="sxs-lookup"><span data-stu-id="9b4de-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="9b4de-108">[Ustaw waluty i kursy wymiany](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="9b4de-109">Ustaw waluty, które będą używane dla projektów.</span><span class="sxs-lookup"><span data-stu-id="9b4de-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="9b4de-110">[Utwórz jednostki organizacyjne](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="9b4de-111">Ustaw grupy, których firma używa do podziału działalności, w oparciu o geografię, funkcje biznesowe lub inne logiczne podziały.</span><span class="sxs-lookup"><span data-stu-id="9b4de-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="9b4de-112">[Ustaw częstotliwość sporządzania faktur](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="9b4de-113">Ustaw okresy czasu, których chcesz używać podczas rozliczania klientów.</span><span class="sxs-lookup"><span data-stu-id="9b4de-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="9b4de-114">[Konfiguruj kategorie transakcji](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="9b4de-115">Ustaw kategorie transakcji, które konsultanci mogą obciążać kosztami ich godzin podlegających rozliczeniu i niepodlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="9b4de-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="9b4de-116">[Konfiguruj kategorie wydatków](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="9b4de-117">Ustaw kategorie, które konsultanci mogą obciążać kosztami ich godzin podlegających rozliczeniu i niepodlegających rozliczeniu.</span><span class="sxs-lookup"><span data-stu-id="9b4de-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="9b4de-118">[Utwórz katalog produktów](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="9b4de-119">Dodaj produkty, które sprzedajesz, takie jak licencje na oprogramowanie, do katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="9b4de-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="9b4de-120">[Utwórz cennik](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="9b4de-121">Skonfiguruj różne cenniki, w zależności od tego, ile chcesz naliczyć klientom za każdą z ról, której wymaga ich projekt.</span><span class="sxs-lookup"><span data-stu-id="9b4de-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="9b4de-122">[Konfigurowanie zasobów](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="9b4de-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="9b4de-123">Dodaj umiejętności, biegłości, role zasobów i inne informacje o zasobach, które będą potrzebne dla projektów.</span><span class="sxs-lookup"><span data-stu-id="9b4de-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9b4de-124">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="9b4de-124">See Also</span></span>  
 <span data-ttu-id="9b4de-125">[Przewodnik po rozwiązaniu Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="9b4de-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="9b4de-126">[Skonfiguruj Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="9b4de-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="9b4de-127">[Przewodnik menedżera kont](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9b4de-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="9b4de-128">[Przewodnik menedżera projektów](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9b4de-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="9b4de-129">[Przewodnik menedżera zasobów](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9b4de-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="9b4de-130">Przewodnik dotyczący czasu, wydatków i współpracy</span><span class="sxs-lookup"><span data-stu-id="9b4de-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
