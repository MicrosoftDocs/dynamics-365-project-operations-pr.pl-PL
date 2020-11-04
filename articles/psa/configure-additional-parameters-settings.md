---
title: Konfigurowanie ustawień dodatkowych parametrów
description: Konfigurowanie ustawień dodatkowych parametrów w Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082012"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="3a292-103">Konfiguruj ustawienia dodatkowych parametrów (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3a292-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3a292-104">Po skonfigurowaniu elementów w poprzednich tematach, należy ustawić dodatkowe parametry projektów, jakie mają być używane dla Twoich projektów.</span><span class="sxs-lookup"><span data-stu-id="3a292-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="3a292-105">Podczas pierwszej instalacji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] utworzyłeś ustawienia parametrów, aby najpierw utworzyć wszystkie rekordy wymagane dla [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="3a292-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="3a292-106">Teraz nadszedł czas, aby wrócić i skonfigurować dodatkowe pola dla tych ustawień.</span><span class="sxs-lookup"><span data-stu-id="3a292-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="3a292-107">Musisz skonfigurować następujące ustawienia:</span><span class="sxs-lookup"><span data-stu-id="3a292-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="3a292-108">Jednostka organizacyjna</span><span class="sxs-lookup"><span data-stu-id="3a292-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="3a292-109">Częstotliwość faktur</span><span class="sxs-lookup"><span data-stu-id="3a292-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="3a292-110">Szablon godzin pracy</span><span class="sxs-lookup"><span data-stu-id="3a292-110">Work hours template</span></span>  
  
-   <span data-ttu-id="3a292-111">Cennik</span><span class="sxs-lookup"><span data-stu-id="3a292-111">Price list</span></span>  
 
<span data-ttu-id="3a292-112">W tym kroku wskażesz również żądany typ alokacji zasobów:</span><span class="sxs-lookup"><span data-stu-id="3a292-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="3a292-113">**Centralny**.</span><span class="sxs-lookup"><span data-stu-id="3a292-113">**Central**.</span></span> <span data-ttu-id="3a292-114">Tylko menedżerowie zasobów mogą przydzielać zasoby do projektów.</span><span class="sxs-lookup"><span data-stu-id="3a292-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="3a292-115">**Hybrydowy**.</span><span class="sxs-lookup"><span data-stu-id="3a292-115">**Hybrid**.</span></span> <span data-ttu-id="3a292-116">Menedżerowie zasobów, menedżerowie projektów i menedżerowie kont mogą przydzielać zasoby do projektów.</span><span class="sxs-lookup"><span data-stu-id="3a292-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="3a292-117">Aby określić parametry projektu:</span><span class="sxs-lookup"><span data-stu-id="3a292-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="3a292-118">Przejdź do **Project Service > Parametry**.</span><span class="sxs-lookup"><span data-stu-id="3a292-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="3a292-119">Kliknij ustawienia parametrów, które chcesz skonfigurować (to utworzone podczas pierwszej instalacji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), lub kliknij **Nowe** , aby utworzyć nowe ustawienie.</span><span class="sxs-lookup"><span data-stu-id="3a292-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="3a292-120">W obszarze **Ogólne** , ustaw wszystkie opcje dla parametrów Twojego projektu.</span><span class="sxs-lookup"><span data-stu-id="3a292-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="3a292-121">W obszarze **Cennik** kliknij **+** , aby dodać cennik, wybierz cennik z listy rozwijanej **Cennik parametrów projektu** a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="3a292-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="3a292-122">Kliknij przycisk **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="3a292-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="3a292-123">Aby usługa Project Service działała prawidłowo, musi zostać zachowany rekord parametru projektu.</span><span class="sxs-lookup"><span data-stu-id="3a292-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="3a292-124">Ten rekord nie powinien być usuwany.</span><span class="sxs-lookup"><span data-stu-id="3a292-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="3a292-125">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="3a292-125">See Also</span></span>  
 [<span data-ttu-id="3a292-126">Konfigurowanie zasobów</span><span class="sxs-lookup"><span data-stu-id="3a292-126">Set up resources</span></span>](../psa/set-up-resources.md)
