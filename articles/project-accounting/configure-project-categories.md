---
title: Konfigurowanie kategorii projektów
description: Ten temat zawiera informacje o ustawianiu kategorii projektów.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995184"
---
# <a name="configure-project-categories"></a><span data-ttu-id="62ae3-103">Konfigurowanie kategorii projektów</span><span class="sxs-lookup"><span data-stu-id="62ae3-103">Configure project categories</span></span>

<span data-ttu-id="62ae3-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="62ae3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="62ae3-105">Project Operations oferuje niezawodne funkcje służące do kategoryzowania przychodów i kosztów projektów.</span><span class="sxs-lookup"><span data-stu-id="62ae3-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="62ae3-106">Kategorie umożliwiają raportowanie i analizowanie transakcji projektów oraz przesyłanie księgowości do księgi głównej.</span><span class="sxs-lookup"><span data-stu-id="62ae3-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="62ae3-107">Na poniższym diagramie przedstawiono korelację między kategoriami transakcji, wspólnymi kategoriami i kategoriami projektów.</span><span class="sxs-lookup"><span data-stu-id="62ae3-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="62ae3-108">Kategorie transakcji są podstawowymi grupami transakcji projektów.</span><span class="sxs-lookup"><span data-stu-id="62ae3-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="62ae3-109">W ramach tego pogrupowania istnieje zestaw wspólnych kategorii, które mogą być współużytkowane w aplikacjach i modułach.</span><span class="sxs-lookup"><span data-stu-id="62ae3-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="62ae3-110">Kategorie projektów to najmniejsze i najdokładniejsze poziomy kategorii.</span><span class="sxs-lookup"><span data-stu-id="62ae3-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="62ae3-111">Kategorie projektów są specyficzne dla encji prawnej, modułu i aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62ae3-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelacja między kategoriami transakcji, wspólnymi kategoriami i kategoriami projektów](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="62ae3-113">Kategorie transakcji</span><span class="sxs-lookup"><span data-stu-id="62ae3-113">Transaction categories</span></span>

<span data-ttu-id="62ae3-114">Kategorie transakcji reprezentują podstawowe pogrupowanie transakcji projektu. Nie są specyficzne dla firmy lub typu transakcji.</span><span class="sxs-lookup"><span data-stu-id="62ae3-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="62ae3-115">Na przykład firma Contoso Robotics używa kategorii Projektowanie, podróż, instalacja i transakcja serwisowa do grupowania transakcji związanych z projektem.</span><span class="sxs-lookup"><span data-stu-id="62ae3-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="62ae3-116">Kategorie transakcji są definiowane w module Project Operations.</span><span class="sxs-lookup"><span data-stu-id="62ae3-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="62ae3-117">Przejdź do **Ustawienia** \> **Kategorie transakcji**, aby otworzyć formularz.</span><span class="sxs-lookup"><span data-stu-id="62ae3-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="62ae3-118">Aby utworzyć nową kategorię transakcji, należy wybrać opcję **Nowa** lub wybrać **Import z szablonu Excel**.</span><span class="sxs-lookup"><span data-stu-id="62ae3-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="62ae3-119">Udostępnione kategorie</span><span class="sxs-lookup"><span data-stu-id="62ae3-119">Shared categories</span></span>

<span data-ttu-id="62ae3-120">Dynamics 365 używa koncepcji Kategorie udostępnione do kategoryzowania wydatków w różnych aplikacjach, takich jak Dynamics 365 Finance, Dynamics 365 Supply Chain i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="62ae3-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="62ae3-121">W przypadku każdej utworzonej kategorii transakcji w ramach Project Operations są automatycznie tworzone cztery powiązane kategorie wspólne: godziny, wydatek, opłaty i przedmiot.</span><span class="sxs-lookup"><span data-stu-id="62ae3-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="62ae3-122">Udostępnione kategorie można przejrzeć i dopasować, przechodząc kolejno do **Zarządzania projektem i księgowania** \> **Konfiguracji** \> **Kategorii** \> **Kategorii wspólnych**.</span><span class="sxs-lookup"><span data-stu-id="62ae3-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="62ae3-123">Kategorie projektu</span><span class="sxs-lookup"><span data-stu-id="62ae3-123">Project categories</span></span>

<span data-ttu-id="62ae3-124">Kategorie projektu reprezentują najniższy, najbardziej dokładny poziom szczegółowości konfiguracji kategorii i muszą zostać skonfigurowane oddzielnie dla każdej firmy — przez księgowego projektu.</span><span class="sxs-lookup"><span data-stu-id="62ae3-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="62ae3-125">Przejdź do sekcji **Zarządzenie projektem i księgowanie** \> **Konfiguracja** \> **Kategorie** \> **Kategorie projektów**.</span><span class="sxs-lookup"><span data-stu-id="62ae3-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="62ae3-126">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="62ae3-126">Select **New**.</span></span>
3. <span data-ttu-id="62ae3-127">Wybierz **Identyfikator kategorii** współużytkowanej kategorii utworzonej w poprzedniej sekcji.</span><span class="sxs-lookup"><span data-stu-id="62ae3-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="62ae3-128">Project Operations umożliwia skorzystanie z wyłącznie tylko udostępnionych kategorii skojarzonych z kategoriami transakcji.</span><span class="sxs-lookup"><span data-stu-id="62ae3-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="62ae3-129">Wybierz grupę kategorii.</span><span class="sxs-lookup"><span data-stu-id="62ae3-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="62ae3-130">Grupy kategorii</span><span class="sxs-lookup"><span data-stu-id="62ae3-130">Category groups</span></span>

<span data-ttu-id="62ae3-131">Grupy kategorii umożliwiają udostępnianie właściwości, głównie profilom księgowania, między pokrewnymi kategoriami projektów.</span><span class="sxs-lookup"><span data-stu-id="62ae3-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="62ae3-132">Dla każdego typu transakcji musi istnieć co najmniej jedna grupa kategorii, a do każdej kategorii projektu jest przypisana grupa.</span><span class="sxs-lookup"><span data-stu-id="62ae3-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="62ae3-133">Specyfikacje księgowania w Project Operations są definiowane przez reguły profilu koszt projektu i przychód, kategorie projektów i grupy kategorii.</span><span class="sxs-lookup"><span data-stu-id="62ae3-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="62ae3-134">Grupy kategorii można skonfigurować, przechodząc do **Zarządzenie projektem i księgowanie** \> **Konfiguracja** \> **Kategorie** \> **Grupy kategorii**.</span><span class="sxs-lookup"><span data-stu-id="62ae3-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]