---
title: Ustawianie cennika sprzedaży
description: Ta temat zawiera informacje na temat list cen sprzedaży w ramach cen projektowych.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896474"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="80e15-103">Ustawianie cennika sprzedaży</span><span class="sxs-lookup"><span data-stu-id="80e15-103">Sales price list setup</span></span>

<span data-ttu-id="80e15-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="80e15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="80e15-105">W przypadku ofert i kontraktów projektów cennik projektu zawiera inny wzorzec zastąpienia cen niż cennik produktu.</span><span class="sxs-lookup"><span data-stu-id="80e15-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="80e15-106">W przypadku wiersza oferty opartej na katalogu produktów można zmienić cenę na role i kategorie bezpośrednio w wierszu oferty, ponieważ każdy wiersz oferty wskazuje dokładnie jeden element katalogu.</span><span class="sxs-lookup"><span data-stu-id="80e15-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="80e15-107">Jednak w wierszu oferty opartej na projekcie nie można zamienić ceny na role i kategorie bezpośrednio w wierszu oferty.</span><span class="sxs-lookup"><span data-stu-id="80e15-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="80e15-108">Cennik projektu może służyć do pracy z dwoma różnymi wzorcami zastąpienia.</span><span class="sxs-lookup"><span data-stu-id="80e15-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="80e15-109">Zaleca się, aby w przypadku zasobów projektu i elementów katalogu można było korzystać z osobnego cennika z powodu różnic między nimi podczas ręcznej kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="80e15-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="80e15-110">Z poszczególnymi encjami może być związany jeden lub więcej cenników skojarzonych z ceną sprzedaży projektu:</span><span class="sxs-lookup"><span data-stu-id="80e15-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="80e15-111">Klient (konto)</span><span class="sxs-lookup"><span data-stu-id="80e15-111">Customer (account)</span></span> 
- <span data-ttu-id="80e15-112">Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="80e15-112">Opportunity</span></span> 
- <span data-ttu-id="80e15-113">Oferta</span><span class="sxs-lookup"><span data-stu-id="80e15-113">Quote</span></span> 
- <span data-ttu-id="80e15-114">Kontrakt projektu</span><span class="sxs-lookup"><span data-stu-id="80e15-114">Project Contract</span></span>

<span data-ttu-id="80e15-115">Skojarzenie tych encji z cennikiem jest wskazane przez cenniki projektu.</span><span class="sxs-lookup"><span data-stu-id="80e15-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="80e15-116">Istnieje możliwość skojarzenia jednego lub kilku cenników z encjami sprzedaży Klient, Szansa sprzedaży, Oferta i Kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="80e15-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="80e15-117">Domyślny cennik nie jest automatycznie wprowadzany w rekordzie klienta.</span><span class="sxs-lookup"><span data-stu-id="80e15-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="80e15-118">Można jednak ręcznie dołączyć Cennik projektu do rekordu klienta.</span><span class="sxs-lookup"><span data-stu-id="80e15-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="80e15-119">Jednak Cennik należy dołączać ręcznie tylko wtedy, gdy użytkownik ma zainstalowaną niestandardową umowę cenową z klientem.</span><span class="sxs-lookup"><span data-stu-id="80e15-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="80e15-120">Gdy Cennik projektu jest dołączony do encji sprzedaży, program sprawdza poprawność następujących informacji:</span><span class="sxs-lookup"><span data-stu-id="80e15-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="80e15-121">Cennik ma kontekst **Sprzedaż**.</span><span class="sxs-lookup"><span data-stu-id="80e15-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="80e15-122">Waluta cennika jest zgodna z walutą klienta.</span><span class="sxs-lookup"><span data-stu-id="80e15-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="80e15-123">W kontrakcie dotyczącym projektu, wykorzystywana jest następująca kolejność pierwszeństwa, aby automatycznie określać powiązane z nimi cenniki projektu:</span><span class="sxs-lookup"><span data-stu-id="80e15-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="80e15-124">Oferta</span><span class="sxs-lookup"><span data-stu-id="80e15-124">Quote</span></span>
2. <span data-ttu-id="80e15-125">Szansa sprzedaży</span><span class="sxs-lookup"><span data-stu-id="80e15-125">Opportunity</span></span>
3. <span data-ttu-id="80e15-126">Klient</span><span class="sxs-lookup"><span data-stu-id="80e15-126">Customer</span></span> 
4. <span data-ttu-id="80e15-127">Ustawienia globalne</span><span class="sxs-lookup"><span data-stu-id="80e15-127">Global settings</span></span> 

<span data-ttu-id="80e15-128">Kiedy Cennik projektu jest wprowadzany domyślnie, system sprawdza poprawność waluty odpowiadającej walucie klienta i, że wprowadzone cenniki domyślne mają kontekst **sprzedaży**.</span><span class="sxs-lookup"><span data-stu-id="80e15-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="80e15-129">Istnieje możliwość skojarzenia kilku cenników projektów z encjami sprzedaży Klient, Szansa sprzedaży, Oferta i Kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="80e15-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="80e15-130">Ta funkcja obsługuje specyficzne dla konkretnego kontraktu ceny domyślne na długo działającym kontrakcie projektu, w którym może zaistnieć potrzeba więcej niż jednego cennika w celu zaktualizowania cen ze względu na inflację.</span><span class="sxs-lookup"><span data-stu-id="80e15-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="80e15-131">Jeśli jednak cenniki skojarzone z encją klient, szansa sprzedaży, oferta lub kontrakt projektu mają nachodzącą na nią datę obowiązywania, cena domyślna może być nieprawidłowa.</span><span class="sxs-lookup"><span data-stu-id="80e15-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="80e15-132">Dlatego należy się upewnić, że cenniki z nakładającymi się datami nie są skojarzone z tymi encjami.</span><span class="sxs-lookup"><span data-stu-id="80e15-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
