---
title: Podaj szacowaną ilość pracy dla projektu w czasie procesu sprzedaży
description: Podawanie szacowanej ilość pracy dla projektu w czasie procesu sprzedaży w Project Service
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283561"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="c4d9a-103">Podaj szacowaną ilość pracy dla projektu w czasie procesu sprzedaży (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c4d9a-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c4d9a-104">Podczas procesu sprzedaży możesz od podstaw opracowywać szacunki sprzedaży korzystając z wierszy oferty.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="c4d9a-105">Możliwości [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] w [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] zapewniają bardziej naukowy i deterministyczny sposób przygotowywania szacunków sprzedaży polegający na rozbijaniu pozycji roboczych i kojarzeniu odpowiednich atrybutów, które przyczyniają się do szacunków dla projektu, ze strukturą podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="c4d9a-106">Gdy już wygrasz sprzedaż, możesz użyć skojarzonej struktury podziału pracy w planie projektu, dopracowując ją, jeśli jest to niezbędne dla pomyślnego zakończenia projektu.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="c4d9a-107">Połącz projekt z wierszem oferty</span><span class="sxs-lookup"><span data-stu-id="c4d9a-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="c4d9a-108">Podczas tworzenia wiersza oferty związanego z projektem możesz tworzyć nowy projekt z wiersza oferty.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="c4d9a-109">Następnie możesz użyć szablonów projektu, które są wstępnie skonfigurowanymi standardowymi planami projektu i prognoz finansowych wspólnych dla organizacji lub kopii planu projektu i oszacowań z ostatniego projektu.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="c4d9a-110">Podczas tworzenia projektu, wybór szablonu projektu stanowi podstawę do dopracowania projektu planu, szacunków i wymagań roli.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="c4d9a-111">W przypadku tworzenia projektu z oferty, projekt jest automatycznie kojarzony z wierszem oferty.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="c4d9a-112">Składniki szacowania projektu</span><span class="sxs-lookup"><span data-stu-id="c4d9a-112">Project estimate components</span></span>  
 <span data-ttu-id="c4d9a-113">Struktura podziału pracy dla projektu zapewnia sposób podziału prac na zadania, utrzymania hierarchii zadań i przypisywania oszacowania nakładu prac wymaganych do wykonania każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="c4d9a-114">Możesz także powiązać role z zadaniem, aby wskazać oszacowanie typu zasobu wymaganego do ukończenia zadania oraz harmonogram.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="c4d9a-115">Struktura podziału pracy pomaga określić nakład pracy i zaplanować oszacowania.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="c4d9a-116">Domyślnie projekt używa cenników domyślnych, które zostały przez Ciebie zdefiniowane wcześniej.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="c4d9a-117">Koszt i ceny sprzedaży określone w cennikach pomagają określać szacunki finansowe dla podziału pracy projektu.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="c4d9a-118">Jeśli projekt jest skojarzony z ofertą, a oferta ma inny cennik niż cennik domyślny, cennik oferty jest używany do sporządzania szacunków finansowych.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="c4d9a-119">Importuj oszacowania z projektu do oferty</span><span class="sxs-lookup"><span data-stu-id="c4d9a-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="c4d9a-120">Po przygotowaniu oszacowań projektu w projekcie, możesz zaimportować te oszacowania do wiersza oferty:</span><span class="sxs-lookup"><span data-stu-id="c4d9a-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="c4d9a-121">W **Szczegóły wiersza oferty**, kliknij **Importuj z oszacowań**.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="c4d9a-122">Określ, czy chcesz importować oszacowania projektu podsumowane według typu transakcji, roli czy poziomu węzła struktury podziału pracy.</span><span class="sxs-lookup"><span data-stu-id="c4d9a-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c4d9a-123">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="c4d9a-123">See Also</span></span>  
 [<span data-ttu-id="c4d9a-124">Przewodnik menedżera projektu</span><span class="sxs-lookup"><span data-stu-id="c4d9a-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]