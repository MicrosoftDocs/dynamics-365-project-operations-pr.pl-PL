---
title: Zastępowanie cenników sprzedaży projektu
description: Ten temat zawiera informacje na temat tworzenia niestandardowych cenników sprzedaży.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995094"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="29ffd-103">Zastępowanie cenników sprzedaży projektu</span><span class="sxs-lookup"><span data-stu-id="29ffd-103">Override project sales price lists</span></span>

<span data-ttu-id="29ffd-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="29ffd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="29ffd-105">Cenniki projektów dostosowane do potrzeb klienta</span><span class="sxs-lookup"><span data-stu-id="29ffd-105">Customer-specific project price lists</span></span>

<span data-ttu-id="29ffd-106">Umowy cenowe specyficzne dla klienta można skonfigurować jako cenniki projektu w rekordzie konta w aplikacji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="29ffd-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="29ffd-107">W celu skonfigurowania cennika projektu specyficznego dla klienta w obszarze **Sprzedaż** przejdź do rekordu klienta.</span><span class="sxs-lookup"><span data-stu-id="29ffd-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="29ffd-108">Otwórz stronę listy **Konta**.</span><span class="sxs-lookup"><span data-stu-id="29ffd-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="29ffd-109">Znajdź i kliknij dwukrotnie rekord klienta, aby otworzyć stronę szczegóły **Konta**.</span><span class="sxs-lookup"><span data-stu-id="29ffd-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="29ffd-110">Na karcie **Cenniki projektów** wybierz **+ Nowy cennik projektu**.</span><span class="sxs-lookup"><span data-stu-id="29ffd-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="29ffd-111">Na stronie **Nowy cennik projektu** wybierz cennik z listy rozwijanej.</span><span class="sxs-lookup"><span data-stu-id="29ffd-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="29ffd-112">Uwzględnione zostaną tylko te cenniki, dla których ustawiono wartość **Sprzedaż** i z której walutą jest zgodna waluta klienta.</span><span class="sxs-lookup"><span data-stu-id="29ffd-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="29ffd-113">Nazwij powiązanie, a następnie wybierz **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="29ffd-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="29ffd-114">Tworzony jest cennik projektu dla klienta.</span><span class="sxs-lookup"><span data-stu-id="29ffd-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="29ffd-115">Ten cennik będzie używany do domyślnych cen projektu w ofertach projektu lub umowach utworzonych dla tego klienta, jeśli data utworzenia oferty lub umowy dotyczącej projektu przypada w okresie obowiązywania cennika.</span><span class="sxs-lookup"><span data-stu-id="29ffd-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="29ffd-116">Niestandardowa kalkulacja cen w ofertach projektu</span><span class="sxs-lookup"><span data-stu-id="29ffd-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="29ffd-117">Na ofertach w ramach projektu można mieć cenę, która zaczyna się od domyślnego cennika standardowego, który jest wybierany domyślnie z klienta lub z parametrów projektu.</span><span class="sxs-lookup"><span data-stu-id="29ffd-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="29ffd-118">Kiedy potrzebna jest cena niestandardowa w odniesieniu do prac związanych z projektem dla określonej oferty, można ją uzyskać z poziomu encji skojarzonych z cennikami projektu.</span><span class="sxs-lookup"><span data-stu-id="29ffd-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="29ffd-119">Wykonaj następujące kroki, aby skonfigurować konkretne oferty dotyczące kalkulacji cen w projekcie.</span><span class="sxs-lookup"><span data-stu-id="29ffd-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="29ffd-120">Otwórz ofertę projektu i wybierz kartę **Cenniki projektów**.</span><span class="sxs-lookup"><span data-stu-id="29ffd-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="29ffd-121">W podsiatce wybierz **Utwórz niestandardowy cennik**.</span><span class="sxs-lookup"><span data-stu-id="29ffd-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="29ffd-122">Wszystkie cenniki projektu dołączone do oferty zostaną skopiowane na nowe cenniki.</span><span class="sxs-lookup"><span data-stu-id="29ffd-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="29ffd-123">Nazwy nowych cenników odzwierciedlają nazwę oferty zawierającą sygnaturę Data/godzina, dla której utworzono te cenniki.</span><span class="sxs-lookup"><span data-stu-id="29ffd-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="29ffd-124">Można użyć poszczególnych cenników i wprowadzić zmiany dotyczące robocizny (cena roli) i koszty (cena kategorii).</span><span class="sxs-lookup"><span data-stu-id="29ffd-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="29ffd-125">Ceny te będą miały zastosowanie tylko do tej wyceny projektu.</span><span class="sxs-lookup"><span data-stu-id="29ffd-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="29ffd-126">Cenniki na umowie projektowej</span><span class="sxs-lookup"><span data-stu-id="29ffd-126">Price lists on a project contract</span></span>

<span data-ttu-id="29ffd-127">W kontrakcie projektu cena projektu zawsze jest domyślnie ustawiona jako cennik niestandardowy z nazwą kontraktu i sygnaturą czasową utworzenia dołączaną do nazwy.</span><span class="sxs-lookup"><span data-stu-id="29ffd-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="29ffd-128">Jest to prawdą, czy kontrakt został utworzony w czasie, gdy oferta została wykorzystana lub kiedy kontrakt został utworzony od podstaw.</span><span class="sxs-lookup"><span data-stu-id="29ffd-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="29ffd-129">Jeśli jest to konieczne, można usunąć to skojarzenie z cennika niestandardowego i zamiast niego skojarzyć cennik standardowy z kontraktem dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="29ffd-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="29ffd-130">Po skojarzeniu standardowego cennika z cennikami dotyczącymi oferty lub kontraktu wszelkie zmiany cen w cenniku będą miały wpływ na wszystkie oferty i kontrakty, w których jest używany cennik.</span><span class="sxs-lookup"><span data-stu-id="29ffd-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]