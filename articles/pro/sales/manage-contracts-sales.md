---
title: Zarządzanie kontraktami projektu
description: Ten temat zawiera informacje o wyświetlaniu umów opartych na projektach.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273220"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="a0202-103">Zarządzanie kontraktami projektu</span><span class="sxs-lookup"><span data-stu-id="a0202-103">Manage project contracts</span></span>

<span data-ttu-id="a0202-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="a0202-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a0202-105">Kontrakty projektów zawarte w rozwiązaniu Dynamics 365 Project Operations przechwytują i zarządzają umownie uzgodnieniami dotyczącymi zobowiązań i informacji na temat rozliczania projektu.</span><span class="sxs-lookup"><span data-stu-id="a0202-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="a0202-106">Struktura umowy projektowej w Project Operations jest dostosowana do pracy opartej na projektach z następującymi komponentami:</span><span class="sxs-lookup"><span data-stu-id="a0202-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="a0202-107">Pozycje kontraktu umożliwiające identyfikację dyskretnych składników pracy, które będą prezentowane na fakturze projektu jako składniki wysokiego poziomu.</span><span class="sxs-lookup"><span data-stu-id="a0202-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="a0202-108">Szczegóły pozycji kontraktu umożliwiające identyfikację i ocenę pracy każdej części składowej wysokiego poziomu lub pozycji kontraktu.</span><span class="sxs-lookup"><span data-stu-id="a0202-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="a0202-109">Prognoza zawiera harmonogram i aspekty finansowe pracy związane z pozycją kontraktu.</span><span class="sxs-lookup"><span data-stu-id="a0202-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="a0202-110">Modele i składniki kontraktów płatnych są konfigurowane dla każdej pozycji kontraktu, która zawiera układ fakturowania dla każdej pozycji kontraktu i całościowego kontraktu.</span><span class="sxs-lookup"><span data-stu-id="a0202-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="a0202-111">Wyświetlanie kontraktów opartych na projekcie</span><span class="sxs-lookup"><span data-stu-id="a0202-111">View all project-based contracts</span></span>

<span data-ttu-id="a0202-112">Listę wszystkich kontraktów projektów można zobaczyć na stronie listy **Kontraktów**.</span><span class="sxs-lookup"><span data-stu-id="a0202-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="a0202-113">Wybierz kolejno pozycje **Sprzedaż** > **Kontakty**.</span><span class="sxs-lookup"><span data-stu-id="a0202-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="a0202-114">Zostanie wyświetlona lista wszystkich kontraktów dotyczących projektu zawartych w systemie.</span><span class="sxs-lookup"><span data-stu-id="a0202-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="a0202-115">Wybierz **Przełącznik widoku** (strzałkę w dół obok nazwy widoku), aby wybrać inne widoki filtrowane.</span><span class="sxs-lookup"><span data-stu-id="a0202-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="a0202-116">Użytkownik może tworzyć własne widoki z kryteriami filtrowania niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="a0202-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="a0202-117">Kontrakty można tworzyć i usuwać na tej stronie listy lub na stronach szczegółów.</span><span class="sxs-lookup"><span data-stu-id="a0202-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]