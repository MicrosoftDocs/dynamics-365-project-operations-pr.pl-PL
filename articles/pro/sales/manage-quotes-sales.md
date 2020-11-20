---
title: Zarządzanie ofertami projektu
description: Ten temat zawiera informacje o ofertach projektów.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177839"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="06b2f-103">Zarządzanie ofertami projektu</span><span class="sxs-lookup"><span data-stu-id="06b2f-103">Manage project quotes</span></span>

<span data-ttu-id="06b2f-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="06b2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="06b2f-105">W Dynamics 365 Project Operations wyceny projektów są zaprojektowane, aby pomóc w tworzeniu propozycji do pracy nad projektem.</span><span class="sxs-lookup"><span data-stu-id="06b2f-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="06b2f-106">Struktura oferty projektu w operacjach projektowych jest podzielona na propozycje projektów z następującymi komponentami:</span><span class="sxs-lookup"><span data-stu-id="06b2f-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="06b2f-107">Pozycje ofert umożliwiające identyfikację dyskretnych składników pracy, które będą prezentowane jako składniki wysokiego poziomu.</span><span class="sxs-lookup"><span data-stu-id="06b2f-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="06b2f-108">Szczegóły pozycji oferty umożliwiające identyfikację i ocenę pracy każdej części składowej wysokiego poziomu lub pozycji oferty.</span><span class="sxs-lookup"><span data-stu-id="06b2f-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="06b2f-109">Harmonogram lub szacunki dat i aspekty finansowe prac są powiązane z tą linią oferty.</span><span class="sxs-lookup"><span data-stu-id="06b2f-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="06b2f-110">Modele i składniki dla instytucji zamawiających są ustawiane dla każdego wiersza oferty.</span><span class="sxs-lookup"><span data-stu-id="06b2f-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="06b2f-111">Dzięki tej konfiguracji można oszacować rozprzestrzenianie przychodów, wydatków i zyskowności dla każdego wiersza oferty i całej oferty.</span><span class="sxs-lookup"><span data-stu-id="06b2f-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="06b2f-112">Zobacz wszystkie oferty oparte na projektach</span><span class="sxs-lookup"><span data-stu-id="06b2f-112">View all project-based quotes</span></span>

<span data-ttu-id="06b2f-113">Listę wszystkich ofert projektów można zobaczyć na stronie listy **Oferty**.</span><span class="sxs-lookup"><span data-stu-id="06b2f-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="06b2f-114">Wybierz kolejno pozycje **Sprzedaż** > **Oferty**.</span><span class="sxs-lookup"><span data-stu-id="06b2f-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="06b2f-115">Zostanie wyświetlona lista wszystkich ofert dotyczących projektu zawartych w systemie.</span><span class="sxs-lookup"><span data-stu-id="06b2f-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="06b2f-116">Użyj **Przełącznik widoku**, aby wybrać inne filtrowane widoki ofert.</span><span class="sxs-lookup"><span data-stu-id="06b2f-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="06b2f-117">Korzystając z niestandardowych kryteriów filtrowania, można skonfigurować własne widoki i opcje nawigacji.</span><span class="sxs-lookup"><span data-stu-id="06b2f-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="06b2f-118">Oferty można tworzyć i usuwać na tej stronie listy lub na stronach szczegółów.</span><span class="sxs-lookup"><span data-stu-id="06b2f-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
