---
title: Projekty szacowanych przychodów o stałej cenie
description: Ten temat zawiera informacje o przychodach o stałej cenie w projektach.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278926"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="f1d1e-103">Projekty szacowanych przychodów o stałej cenie</span><span class="sxs-lookup"><span data-stu-id="f1d1e-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="f1d1e-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="f1d1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f1d1e-105">Podczas tworzenia pozycji kontraktu projektu z następującymi atrybutami w aplikacji Dynamics 365 Project Operations w usłudze Microsoft Dataverse system automatycznie tworzy projekt szacowanych przychodów o stałej cenie.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="f1d1e-106">Informacje zawarte w tym projekcie są oparte na następujących elementach:</span><span class="sxs-lookup"><span data-stu-id="f1d1e-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="f1d1e-107">Metoda rozliczania stałych cen.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="f1d1e-108">Skojarzony projekt.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-108">An associated project.</span></span>
  - <span data-ttu-id="f1d1e-109">Co najmniej jeden punkt kontrolny zdefiniowany na karcie **Harmonogram faktur** na stronie **Pozycja kontraktu projektu**.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="f1d1e-110">Przeglądanie projektów szacowanych przychodów o stałej cenie</span><span class="sxs-lookup"><span data-stu-id="f1d1e-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="f1d1e-111">Aby przejrzeć projekty szacowanych przychodów o stałej cenie, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="f1d1e-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="f1d1e-112">W środowisku aplikacji Dynamics 365 Finance przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Projekty** > **Projekty szacowanych przychodów o stałej cenie**.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="f1d1e-113">Wybierz projekt, który chcesz wyświetlić, i kliknij dwukrotnie **identyfikator projektu szacowania**, aby otworzyć rekord i przejrzeć szczegóły projektu.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="f1d1e-114">Rozwiń kartę **Projekt**. Jeden projekt zostanie wyświetlony w siatce **Wybrane projekty**.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="f1d1e-115">System używa tego jako projektu domyślnego, ponieważ jest to projekt skojarzony z pozycją kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="f1d1e-116">Aby zmienić skojarzenie, wybierz dodatkowe projekty i dodaj je do siatki **Wybrane projekty**.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="f1d1e-117">Jeśli w tej siatce wybrano wiele projektów, procent wykonania projektu i szacowane przychody są obliczane razem dla wszystkich wybranych projektów.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="f1d1e-118">Koszt projektu, profil przychodów, szablon kosztów i kod okresu można ustawić ręcznie.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="f1d1e-119">Jeśli nie są one ustawione ręcznie, wartości domyślne zostaną ustawione podczas pierwszego obliczenia szacowania dla projektu przy użyciu reguł skonfigurowanych dla profilów przychodów i kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="f1d1e-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]