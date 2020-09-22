---
title: Skonfiguruj role zasobów
description: Konfigurowanie ról zasobów w Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0a180069-17d9-40fd-b4af-9b8d50f373ea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6a32ec4380e847b897931b6691fa8f9784d0cee7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754290"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="5249c-103">Konfiguruj role zasobów (Project Service)</span><span class="sxs-lookup"><span data-stu-id="5249c-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5249c-104">Role odgrywają istotną rolę w planowaniu projektów, przy ustalaniu wymagań dotyczących zasobów lub kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="5249c-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="5249c-105">Dla każdej roli wymaganej przez projekty musisz utworzyć rolę zasobu i skojarzyć z nią umiejętności i biegłości.</span><span class="sxs-lookup"><span data-stu-id="5249c-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="5249c-106">Na przykład możesz chcieć utworzyć role dla dewelopera, menedżera projektu lub testera gry.</span><span class="sxs-lookup"><span data-stu-id="5249c-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="5249c-107">Określisz również umiejętności i poziomy zaawansowania wymagane dla roli.</span><span class="sxs-lookup"><span data-stu-id="5249c-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="5249c-108">Konfiguruj role zasobów, aby zapewnić skuteczne szacowanie projektu dla Twojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="5249c-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="5249c-109">Ponadto upewnij się, że dokładnie ustawiłeś typ płatności.</span><span class="sxs-lookup"><span data-stu-id="5249c-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="5249c-110">Element, dla którego określono niepłatny typ fakturowania nie pojawia się w wierszach zamówienia lub oferty.</span><span class="sxs-lookup"><span data-stu-id="5249c-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="5249c-111">Po skonfigurowaniu ról zasobów, można skonfigurować koszt i ceny sprzedaży z cennikiem.</span><span class="sxs-lookup"><span data-stu-id="5249c-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="5249c-112">Dla każdej roli, którą chcesz dodać, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="5249c-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="5249c-113">Przejdź do **Project Service > Role zasobów**.</span><span class="sxs-lookup"><span data-stu-id="5249c-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="5249c-114">Kliknij pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="5249c-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="5249c-115">W obszarze **Ogólne** wprowadź nazwę roli w **Nazwa**, a następnie, jeśli to konieczne, wypełnij pozostałe pola.</span><span class="sxs-lookup"><span data-stu-id="5249c-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="5249c-116">Kliknij **Zapisz**, aby utworzyć rekord i móc kontynuować jego edycję.</span><span class="sxs-lookup"><span data-stu-id="5249c-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="5249c-117">W obszarze **Umiejętności** kliknij **+**, aby dodać umiejętność.</span><span class="sxs-lookup"><span data-stu-id="5249c-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="5249c-118">W okienku **Wymaganie kompetencji roli**, kliknij w polu **Umiejętność**, kliknij przycisk **Szukaj**, a następnie wybierz umiejętność.</span><span class="sxs-lookup"><span data-stu-id="5249c-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="5249c-119">Zaznacz poziom biegłości dla tej umiejętności, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="5249c-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="5249c-120">W razie potrzeby kontynuuj dodawanie umiejętności.</span><span class="sxs-lookup"><span data-stu-id="5249c-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="5249c-121">Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="5249c-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="5249c-122">Aby udostępnić rolę zasobu dla projektów, które mają jej używać, kliknij **Aktywuj**.</span><span class="sxs-lookup"><span data-stu-id="5249c-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5249c-123">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="5249c-123">See Also</span></span>  
 [<span data-ttu-id="5249c-124">Konfigurowanie zasobów</span><span class="sxs-lookup"><span data-stu-id="5249c-124">Set up resources</span></span>](../project-service/set-up-resources.md)
