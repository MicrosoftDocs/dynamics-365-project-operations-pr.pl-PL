---
title: Konfigurowanie kategorii projektów
description: Ten temat zawiera informacje o ustawianiu kategorii projektów.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895979"
---
# <a name="configure-project-categories"></a><span data-ttu-id="a2062-103">Konfigurowanie kategorii projektów</span><span class="sxs-lookup"><span data-stu-id="a2062-103">Configure project categories</span></span>

<span data-ttu-id="a2062-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="a2062-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a2062-105">Project Operations oferuje niezawodne funkcje służące do kategoryzowania przychodów i kosztów projektów.</span><span class="sxs-lookup"><span data-stu-id="a2062-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="a2062-106">Kategorie umożliwiają raportowanie i analizowanie transakcji projektów oraz przesyłanie księgowości do księgi głównej.</span><span class="sxs-lookup"><span data-stu-id="a2062-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="a2062-107">Na poniższym diagramie przedstawiono korelację między kategoriami transakcji, wspólnymi kategoriami i kategoriami projektów.</span><span class="sxs-lookup"><span data-stu-id="a2062-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="a2062-108">Kategorie transakcji są podstawowymi grupami transakcji projektów.</span><span class="sxs-lookup"><span data-stu-id="a2062-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="a2062-109">W ramach tego pogrupowania istnieje zestaw wspólnych kategorii, które mogą być współużytkowane w aplikacjach i modułach.</span><span class="sxs-lookup"><span data-stu-id="a2062-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="a2062-110">Kategorie projektów to najmniejsze i najdokładniejsze poziomy kategorii.</span><span class="sxs-lookup"><span data-stu-id="a2062-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="a2062-111">Kategorie projektów są specyficzne dla encji prawnej, modułu i aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a2062-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelacja między kategoriami transakcji, wspólnymi kategoriami i kategoriami projektów](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="a2062-113">Kategorie transakcji</span><span class="sxs-lookup"><span data-stu-id="a2062-113">Transaction categories</span></span>

<span data-ttu-id="a2062-114">Kategorie transakcji reprezentują podstawowe pogrupowanie transakcji projektu. Nie są specyficzne dla firmy lub typu transakcji.</span><span class="sxs-lookup"><span data-stu-id="a2062-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="a2062-115">Na przykład firma Contoso Robotics używa kategorii „projektowanie”, „podróże”, „instalacja” i „transakcja usług” do grupowania transakcji projektów.</span><span class="sxs-lookup"><span data-stu-id="a2062-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="a2062-116">Kategorie transakcji są definiowane w module Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a2062-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="a2062-117">Przejdź do **Ustawienia** \> **Kategorie transakcji**, aby otworzyć formularz.</span><span class="sxs-lookup"><span data-stu-id="a2062-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="a2062-118">Aby utworzyć nową kategorię transakcji, należy wybrać opcję **Nowa** lub wybrać **Import z szablonu Excel**.</span><span class="sxs-lookup"><span data-stu-id="a2062-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="a2062-119">Udostępnione kategorie</span><span class="sxs-lookup"><span data-stu-id="a2062-119">Shared categories</span></span>

<span data-ttu-id="a2062-120">Program Dynamics 365 używa koncepcji wspólnych kategorii do kategoryzowania kosztów w różnych aplikacjach, takich jak Dynamics 365 Finance, Dynamics 365 Supply Chain oraz Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a2062-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="a2062-121">W przypadku każdej utworzonej kategorii transakcji w ramach Project Operations są automatycznie tworzone cztery powiązane kategorie wspólne: godziny, wydatek, opłaty i przedmiot.</span><span class="sxs-lookup"><span data-stu-id="a2062-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="a2062-122">Udostępnione kategorie można przejrzeć i dopasować, przechodząc kolejno do **Zarządzania projektem i księgowania** \> **Konfiguracji** \> **Kategorii** \> **Kategorii wspólnych**.</span><span class="sxs-lookup"><span data-stu-id="a2062-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="a2062-123">Kategorie projektu</span><span class="sxs-lookup"><span data-stu-id="a2062-123">Project categories</span></span>

<span data-ttu-id="a2062-124">Kategorie projektu reprezentują najniższy, najbardziej dokładny poziom szczegółowości konfiguracji kategorii i muszą zostać skonfigurowane oddzielnie dla każdej firmy — przez księgowego projektu.</span><span class="sxs-lookup"><span data-stu-id="a2062-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="a2062-125">Przejdź do sekcji **Zarządzenie projektem i księgowanie** \> **Konfiguracja** \> **Kategorie** \> **Kategorie projektów**.</span><span class="sxs-lookup"><span data-stu-id="a2062-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="a2062-126">Wybierz **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="a2062-126">Select **New**.</span></span>
3. <span data-ttu-id="a2062-127">Wybierz **Identyfikator kategorii** współużytkowanej kategorii utworzonej w poprzedniej sekcji.</span><span class="sxs-lookup"><span data-stu-id="a2062-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="a2062-128">Project Operations umożliwia skorzystanie z wyłącznie tylko udostępnionych kategorii skojarzonych z kategoriami transakcji.</span><span class="sxs-lookup"><span data-stu-id="a2062-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="a2062-129">Wybierz grupę kategorii.</span><span class="sxs-lookup"><span data-stu-id="a2062-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="a2062-130">Grupy kategorii</span><span class="sxs-lookup"><span data-stu-id="a2062-130">Category groups</span></span>

<span data-ttu-id="a2062-131">Grupy kategorii umożliwiają udostępnianie właściwości, głównie profilom księgowania, między pokrewnymi kategoriami projektów.</span><span class="sxs-lookup"><span data-stu-id="a2062-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="a2062-132">Dla każdego typu transakcji musi istnieć co najmniej jedna grupa kategorii, a do każdej kategorii projektu jest przypisana grupa.</span><span class="sxs-lookup"><span data-stu-id="a2062-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="a2062-133">Specyfikacje księgowania w Project Operations są definiowane przez reguły profilu koszt projektu i przychód, kategorie projektów i grupy kategorii.</span><span class="sxs-lookup"><span data-stu-id="a2062-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="a2062-134">Grupy kategorii można skonfigurować, przechodząc do **Zarządzenie projektem i księgowanie** \> **Konfiguracja** \> **Kategorie** \> **Grupy kategorii**.</span><span class="sxs-lookup"><span data-stu-id="a2062-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
