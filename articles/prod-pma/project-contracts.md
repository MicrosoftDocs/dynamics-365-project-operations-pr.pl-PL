---
title: Kontrakty projektów
description: W tym temat przedstawiono przykłady kontraktów dotyczących projektów, które można tworzyć dla różnych typów projektów i źródeł finansowania oraz sposób zarządzania kontraktami i klientami projektu fakturowania.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289562"
---
# <a name="project-contracts"></a><span data-ttu-id="3ad35-103">Kontrakty projektów</span><span class="sxs-lookup"><span data-stu-id="3ad35-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ad35-104">W tym artykule przedstawiono przykłady kontraktów dotyczących projektów, które można tworzyć dla różnych typów projektów i źródeł finansowania oraz sposób zarządzania kontraktami i klientami projektu fakturowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="3ad35-105">Typ projektu utworzonego dla umowy dotyczącej projektu określa metodę używaną do fakturowania odbiorców projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="3ad35-106">Istnieje możliwość zmodyfikowania kontraktu projektu i powiązanego z nim projektu, ale nie można zmienić typu projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="3ad35-107">Korzystając z kontraktu projektu, można zafakturować jeden lub więcej projektów jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="3ad35-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="3ad35-108">Kontrakt dotyczący projektu ułatwia również zagwarantowanie spójnej procedury fakturowania dla każdego podprojektu w strukturze projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="3ad35-109">Każdy projekt, który ma zostać wystawiony, musi być skojarzony z kontraktem dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="3ad35-110">Ustawienia kontraktu dotyczącego projektu mają zastosowanie do wszystkich projektów i podprojektów skojarzonych z danym kontraktem dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="3ad35-111">Kontrakt dotyczący projektu może określać jeden lub więcej źródeł finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="3ad35-112">Z tego względu można podzielić rozliczanie na wielu funduszach, skonfigurować limity finansowania, aby źródła finansowania nie były wystawiane więcej niż określona kwota, a także skonfigurować reguły finansowania dotyczące ładowania wydatków.</span><span class="sxs-lookup"><span data-stu-id="3ad35-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="3ad35-113">Finansowanie kontraktów dotyczących projektów</span><span class="sxs-lookup"><span data-stu-id="3ad35-113">Funding for project contracts</span></span>
<span data-ttu-id="3ad35-114">Niektóre kontrakty dotyczące projektów określają, że w przypadku finansowania kosztów projektu wiele stron ma obowiązek podzielić się obowiązkiem.</span><span class="sxs-lookup"><span data-stu-id="3ad35-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="3ad35-115">Oto kilka przykładów:</span><span class="sxs-lookup"><span data-stu-id="3ad35-115">Here are some examples:</span></span>

-   <span data-ttu-id="3ad35-116">Duża wartość klienta mającego wielu działów wynosi zażądania podziału finansowania danego projektu na dział.</span><span class="sxs-lookup"><span data-stu-id="3ad35-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="3ad35-117">Firma współużytkuje koszty dużego projektu z zewnętrzną organizacją.</span><span class="sxs-lookup"><span data-stu-id="3ad35-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="3ad35-118">Projekt drogowy jest współfinansowany przez dwie gminy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="3ad35-119">Projekt mostkowy jest finansowany przez władzę rządową i organizację prywatną.</span><span class="sxs-lookup"><span data-stu-id="3ad35-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="3ad35-120">W Dynamics 365 Finance można podzielić rozliczenia dla jednej transakcji lub całego projektu między wiele klientów, dotacji lub organizacji.</span><span class="sxs-lookup"><span data-stu-id="3ad35-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="3ad35-121">W projektach mających wielu funduszach wszystkie strony, które przynoszą finansowanie zaawansowanego projektu finansowania, noszą nazwę źródeł finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="3ad35-122">Jeśli klient, organizacja lub dotacja została zdefiniowana jako źródło finansowania, może zostać przypisana do jednej lub więcej reguł finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="3ad35-123">Reguły finansowania zawierają kryteria określające sposób przydzielania kosztów na różne źródła finansowania dotyczące danego projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="3ad35-124">Ze względu na fakt, że towary magazynowane, takie jak te, które są wyświetlane w założeniach zakupu i zamówieniach zakupu, nie mogą zostać podzielone, nie można ich podzielić na wiele źródeł finansowania w czasie dystrybucji.</span><span class="sxs-lookup"><span data-stu-id="3ad35-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="3ad35-125">Dlatego wartość źródła finansowania pozostaje 0 (zero) do momentu zaksięgowania wydania magazynu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="3ad35-126">Po zaksięgowaniu rozchodu magazynowego koszt jest dystrybuowany zgodnie z regułami dystrybucji klientów dotyczącymi projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="3ad35-127">Oto kilka kroków, które można podjąć w celu ułatwienia podziału rozliczenia między wiele źródeł finansowania:</span><span class="sxs-lookup"><span data-stu-id="3ad35-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="3ad35-128">Określa, że wszystkie transakcje wprowadzone dla projektu korzystają z tej samej waluty sprzedaży, co kontrakt dotyczący projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="3ad35-129">Skonfiguruj limity finansowania, aby źródło finansowania nie było fakturowane na więcej niż określoną kwotę w ramach projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="3ad35-130">Konfigurowanie reguł finansowania i ograniczeń finansowania dla każdego pracownika, elementu, kategorii, grupy kategorii i typu transakcji (lub we wszystkich typach transakcji).</span><span class="sxs-lookup"><span data-stu-id="3ad35-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="3ad35-131">Wybierz opcjonalne daty rozpoczęcia i zakończenia, aby zdefiniować okres, w którym każda reguła finansowania będzie ważna.</span><span class="sxs-lookup"><span data-stu-id="3ad35-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="3ad35-132">Podaj procent, za który jest odpowiedzialny każde źródło finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="3ad35-133">Określ, które źródło finansowania jest odpowiedzialne za różnice zaokrągleń wynikające z obliczeń alokacji finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="3ad35-134">Skonfiguruj reguły, które określają, w jaki sposób koszty projektu są fakturowane dla klientów zewnętrznych i naliczane organizacjom wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="3ad35-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="3ad35-135">Rejestruj transakcje na koncie ze środkami wstrzymanymi do czasu uzyskania dodatkowego finansowania lub do czasu, gdy zdecydujesz się pokryć koszty wewnętrznie.</span><span class="sxs-lookup"><span data-stu-id="3ad35-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="3ad35-136">Aby określić, która grupa podatkowa ma zostać powiązana z transakcją, w projekcie wyszukiwane jest przypisanie do grupy podatkowej.</span><span class="sxs-lookup"><span data-stu-id="3ad35-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="3ad35-137">Jeśli na poziomie projektu nie dokonano przypisania grupy podatkowej, przeszukiwana jest umowa dotycząca projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="3ad35-138">Przykład: wiele źródeł finansowania (proste)</span><span class="sxs-lookup"><span data-stu-id="3ad35-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="3ad35-139">W poniższej tabeli przedstawiono scenariusze zarządzania alokacją środków na wiele źródeł finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="3ad35-140">Te scenariusze są oparte na następujących założeniach:</span><span class="sxs-lookup"><span data-stu-id="3ad35-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="3ad35-141">Ustawienia priorytetów są uwzględniane przy alokacji środków przed zastosowaniem innych kryteriów reguły finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="3ad35-142">Nie podano zakresu dat w celu zdefiniowania okresu d, kiedy reguła finansowania jest prawidłowa.</span><span class="sxs-lookup"><span data-stu-id="3ad35-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ad35-143"><strong>Scenariusz</strong></span><span class="sxs-lookup"><span data-stu-id="3ad35-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="3ad35-144"><strong>Źródło finansowania</strong></span><span class="sxs-lookup"><span data-stu-id="3ad35-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="3ad35-145"><strong>Procent alokacji</strong></span><span class="sxs-lookup"><span data-stu-id="3ad35-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="3ad35-146"><strong>Priorytet alokacji</strong></span><span class="sxs-lookup"><span data-stu-id="3ad35-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad35-147">Chcesz przypisać koszty do jednego źródła finansowania aż do wyczerpania jego środków, przypisać koszty do drugiego źródła finansowania, aż do wyczerpania jego środków, a na koniec alokować pozostałe koszty do trzeciego źródła finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="3ad35-148">Źródło　finansowania　1</span><span class="sxs-lookup"><span data-stu-id="3ad35-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="3ad35-149">Źródło　finansowania　2</span><span class="sxs-lookup"><span data-stu-id="3ad35-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="3ad35-150">Źródło　finansowania　3</span><span class="sxs-lookup"><span data-stu-id="3ad35-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-151">100%</span><span class="sxs-lookup"><span data-stu-id="3ad35-151">100%</span></span></li>
<li><span data-ttu-id="3ad35-152">100%</span><span class="sxs-lookup"><span data-stu-id="3ad35-152">100%</span></span></li>
<li><span data-ttu-id="3ad35-153">100%</span><span class="sxs-lookup"><span data-stu-id="3ad35-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-154">1</span><span class="sxs-lookup"><span data-stu-id="3ad35-154">1</span></span></li>
<li><span data-ttu-id="3ad35-155">2</span><span class="sxs-lookup"><span data-stu-id="3ad35-155">2</span></span></li>
<li><span data-ttu-id="3ad35-156">3</span><span class="sxs-lookup"><span data-stu-id="3ad35-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad35-157">Alokacja 75 procent kosztów do jednego źródła finansowania i 25 procent ma zostać zaalokowana do drugiego źródła finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="3ad35-158">W przypadku wyczerpania któregokolwiek z tych źródeł finansowania użytkownik chce zapłacić pozostałe koszty w trzecim źródle finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="3ad35-159">Źródło　finansowania　1</span><span class="sxs-lookup"><span data-stu-id="3ad35-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="3ad35-160">Źródło　finansowania　2</span><span class="sxs-lookup"><span data-stu-id="3ad35-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="3ad35-161">Źródło　finansowania　3</span><span class="sxs-lookup"><span data-stu-id="3ad35-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-162">75%</span><span class="sxs-lookup"><span data-stu-id="3ad35-162">75%</span></span></li>
<li><span data-ttu-id="3ad35-163">25%</span><span class="sxs-lookup"><span data-stu-id="3ad35-163">25%</span></span></li>
<li><span data-ttu-id="3ad35-164">100%</span><span class="sxs-lookup"><span data-stu-id="3ad35-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-165">1</span><span class="sxs-lookup"><span data-stu-id="3ad35-165">1</span></span></li>
<li><span data-ttu-id="3ad35-166">1</span><span class="sxs-lookup"><span data-stu-id="3ad35-166">1</span></span></li>
<li><span data-ttu-id="3ad35-167">2</span><span class="sxs-lookup"><span data-stu-id="3ad35-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad35-168">Alokacja 75 procent kosztów do jednego źródła finansowania i 25 procent ma zostać zaalokowana do drugiego źródła finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="3ad35-169">Gdy jedno z tych źródeł finansowania zostanie wyczerpane, chcesz podzielić pozostałe koszty między trzecie i czwarte źródło finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="3ad35-170">Źródło　finansowania　1</span><span class="sxs-lookup"><span data-stu-id="3ad35-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="3ad35-171">Źródło　finansowania　2</span><span class="sxs-lookup"><span data-stu-id="3ad35-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="3ad35-172">Źródło　finansowania　3</span><span class="sxs-lookup"><span data-stu-id="3ad35-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="3ad35-173">Źródło　finansowania　4</span><span class="sxs-lookup"><span data-stu-id="3ad35-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-174">75%</span><span class="sxs-lookup"><span data-stu-id="3ad35-174">75%</span></span></li>
<li><span data-ttu-id="3ad35-175">25%</span><span class="sxs-lookup"><span data-stu-id="3ad35-175">25%</span></span></li>
<li><span data-ttu-id="3ad35-176">50%</span><span class="sxs-lookup"><span data-stu-id="3ad35-176">50%</span></span></li>
<li><span data-ttu-id="3ad35-177">50%</span><span class="sxs-lookup"><span data-stu-id="3ad35-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-178">1</span><span class="sxs-lookup"><span data-stu-id="3ad35-178">1</span></span></li>
<li><span data-ttu-id="3ad35-179">1</span><span class="sxs-lookup"><span data-stu-id="3ad35-179">1</span></span></li>
<li><span data-ttu-id="3ad35-180">2</span><span class="sxs-lookup"><span data-stu-id="3ad35-180">2</span></span></li>
<li><span data-ttu-id="3ad35-181">2</span><span class="sxs-lookup"><span data-stu-id="3ad35-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad35-182">Chcesz przeznaczyć pierwsze 25% kosztów na jedno źródło finansowania, a resztę na drugie źródło finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="3ad35-183">Źródło　finansowania　1</span><span class="sxs-lookup"><span data-stu-id="3ad35-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="3ad35-184">Źródło　finansowania　2</span><span class="sxs-lookup"><span data-stu-id="3ad35-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-185">25%</span><span class="sxs-lookup"><span data-stu-id="3ad35-185">25%</span></span></li>
<li><span data-ttu-id="3ad35-186">100%</span><span class="sxs-lookup"><span data-stu-id="3ad35-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ad35-187">1</span><span class="sxs-lookup"><span data-stu-id="3ad35-187">1</span></span></li>
<li><span data-ttu-id="3ad35-188">2</span><span class="sxs-lookup"><span data-stu-id="3ad35-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="3ad35-189">Przykład: wiele źródeł finansowania (złożone)</span><span class="sxs-lookup"><span data-stu-id="3ad35-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="3ad35-190">Istnieją trzy źródła finansowania, które mają zostać użyte w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="3ad35-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="3ad35-191">Źródła finansowania 2 i źródło finansowania 3 należy stosować po równo do wyczerpania źródła finansowania 2.</span><span class="sxs-lookup"><span data-stu-id="3ad35-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="3ad35-192">Kontynuuj korzystanie ze źródła finansowania 3, aż zostanie wyczerpane.</span><span class="sxs-lookup"><span data-stu-id="3ad35-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="3ad35-193">Użyj źródła finansowania 1 po wyczerpaniu źródła finansowania 3.</span><span class="sxs-lookup"><span data-stu-id="3ad35-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="3ad35-194">Aby osiągnąć ten cel, musisz wykonać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="3ad35-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="3ad35-195">Ustal limity finansowania dla źródła finansowania 2 i źródła finansowania 3 dla ich odpowiednich kwot.</span><span class="sxs-lookup"><span data-stu-id="3ad35-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="3ad35-196">Utwórz następujące zasady finansowania:</span><span class="sxs-lookup"><span data-stu-id="3ad35-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="3ad35-197">Reguła 1 (priorytet 1): Alokacja 50 procent transakcji do źródła finansowania 2 i 50 procent do źródła finansowania 3.</span><span class="sxs-lookup"><span data-stu-id="3ad35-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="3ad35-198">Reguła 2 (priorytet 2): alokowanie 100 procent transakcji dla źródła finansowania 3.</span><span class="sxs-lookup"><span data-stu-id="3ad35-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="3ad35-199">Reguła 3 (priorytet 3): alokowanie 100 procent transakcji dla źródła finansowania 1.</span><span class="sxs-lookup"><span data-stu-id="3ad35-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="3ad35-200">Ta instalacja działa, ponieważ sprawdzanie transakcji względem reguł i ograniczeń polega na określeniu, czy którykolwiek z nich ma zastosowanie do transakcji.</span><span class="sxs-lookup"><span data-stu-id="3ad35-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="3ad35-201">Jeśli do transakcji nie są stosowane żadne konkretne reguły lub ograniczenia, stosowana jest reguła Wszystkie transakcje.</span><span class="sxs-lookup"><span data-stu-id="3ad35-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="3ad35-202">Reguła Wszystkich transakcji jest zgodna ze wszystkimi transakcjami.</span><span class="sxs-lookup"><span data-stu-id="3ad35-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="3ad35-203">Jeśli zostanie znaleziona reguła, która pasuje do transakcji, wartość procentowa, która została przydzielona w tej regule, jest stosowana jako pierwsza, ale dopiero po sprawdzeniu zgodności z wszelkimi ustawionymi limitami.</span><span class="sxs-lookup"><span data-stu-id="3ad35-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="3ad35-204">Jeśli limit został osiągnięty, a środki źródła finansowania są wyczerpane, reguła finansowania powiązana z limitem finansowania jest ignorowana, a program sprawdza następną regułę, która ma zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="3ad35-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="3ad35-205">W niektórych przypadkach tylko część transakcji może zostać zaalokowana na regułę.</span><span class="sxs-lookup"><span data-stu-id="3ad35-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="3ad35-206">Powodem może być to, że podczas alokowania transakcji został osiągnięty limit.</span><span class="sxs-lookup"><span data-stu-id="3ad35-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="3ad35-207">W tym przypadku tylko pewna kwota jest alokowana według tej reguły, na przykład do 50 procent dla każdego źródła finansowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="3ad35-208">Tak jest w zasadzie 1, która jest opisana we wcześniejszej części tej sekcji.</span><span class="sxs-lookup"><span data-stu-id="3ad35-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="3ad35-209">Pozostała część jest alokowana według następnej reguły w sekwencji.</span><span class="sxs-lookup"><span data-stu-id="3ad35-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="3ad35-210">Poniższa tabela zawiera szczegółowe informacje o tym scenariuszu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ad35-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="3ad35-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="3ad35-212"><strong>Szczegóły</strong></span><span class="sxs-lookup"><span data-stu-id="3ad35-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad35-213">Reguły finansowania</span><span class="sxs-lookup"><span data-stu-id="3ad35-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="3ad35-214">Reguła 1 (priorytet 1): wszystkie transakcje.</span><span class="sxs-lookup"><span data-stu-id="3ad35-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="3ad35-215">Przydziel źródło finansowania 2 na 50% i źródło finansowania 3 na 50%.</span><span class="sxs-lookup"><span data-stu-id="3ad35-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="3ad35-216">Reguła 2 (priorytet 2): wszystkie transakcje.</span><span class="sxs-lookup"><span data-stu-id="3ad35-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="3ad35-217">Przydziel Źródło finansowania 3 na 100%.</span><span class="sxs-lookup"><span data-stu-id="3ad35-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="3ad35-218">Reguła 3 (priorytet 2): wszystkie transakcje.</span><span class="sxs-lookup"><span data-stu-id="3ad35-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="3ad35-219">Przydziel Źródło finansowania 1 na 100%.</span><span class="sxs-lookup"><span data-stu-id="3ad35-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad35-220">Limity finansowania</span><span class="sxs-lookup"><span data-stu-id="3ad35-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="3ad35-221">Limit źródła finansowania 1 = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="3ad35-222">Limit źródła finansowania 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="3ad35-223">Limit źródła finansowania 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad35-224">Transakcja 1</span><span class="sxs-lookup"><span data-stu-id="3ad35-224">Transaction 1</span></span></td>
<td><span data-ttu-id="3ad35-225"><strong>Kwota transakcji:</strong> 100,00<strong>Fundusze:</strong> Transakcja jest płatna zgodnie z regułą 1, ponieważ transakcja jest całkowicie zapłacona po zastosowaniu reguły 1.</span><span class="sxs-lookup"><span data-stu-id="3ad35-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="3ad35-226">Transakcja jest finansowana równo między źródłem finansowania 2 a źródłem finansowania 3.</span><span class="sxs-lookup"><span data-stu-id="3ad35-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="3ad35-227">Źródło finansowania 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="3ad35-228">Źródło finansowania 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ad35-229">Transakcja 2</span><span class="sxs-lookup"><span data-stu-id="3ad35-229">Transaction 2</span></span></td>
<td><span data-ttu-id="3ad35-230"><strong>Kwota transakcji:</strong> 5 000,00<strong>Finansowanie:</strong> Transakcja jest wypłacana według wszystkich trzech reguł.</span><span class="sxs-lookup"><span data-stu-id="3ad35-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="3ad35-231"><strong>Reguła 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="3ad35-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="3ad35-232">Źródło finansowania 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="3ad35-233">Źródło finansowania 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="3ad35-234">
<strong>Reguła 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="3ad35-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="3ad35-235">Źródło finansowania 3: 250,00 (= 750,00 - 50,00 - 450,00)</span><span class="sxs-lookup"><span data-stu-id="3ad35-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="3ad35-236">
<strong>Reguła 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="3ad35-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="3ad35-237">Źródło finansowania 1: 3850,00 (= 5000,00 - 450,00 - 450,00 - 250,00)</span><span class="sxs-lookup"><span data-stu-id="3ad35-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ad35-238">Suma środków dystrybuowanych na każde źródło finansowania</span><span class="sxs-lookup"><span data-stu-id="3ad35-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="3ad35-239">Źródło finansowania 1: 3 850,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="3ad35-240">Źródło finansowania 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="3ad35-241">Źródło finansowania 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="3ad35-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="3ad35-242">Reguły fakturowania</span><span class="sxs-lookup"><span data-stu-id="3ad35-242">Billing rules</span></span>
<span data-ttu-id="3ad35-243">Podczas negocjowania kontraktu dotyczącego projektu z klientem użytkownik określa, jak i kiedy można zafakturować klienta w celu wykonania prac nad projektem.</span><span class="sxs-lookup"><span data-stu-id="3ad35-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="3ad35-244">Po skonfigurowaniu kontraktu projektu i projektu można skonfigurować reguły fakturowania dla projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="3ad35-245">Reguły fakturowania są tworzone na podstawie terminów projektu określonych w kontrakcie dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="3ad35-246">Reguły fakturowania, które można utworzyć, zależą od warunków umowy dotyczącej projektu i typu projektu, takiego jak czas i materiał lub stała cena, który jest skojarzony z regułą fakturowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="3ad35-247">Dla kontraktu dotyczącego projektu można utworzyć więcej niż jedną regułę fakturowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="3ad35-248">Możesz również przypisać regułę fakturowania do wielu projektów, które są skojarzone z tą samą umową dotyczącą projektu i mają podobne warunki płatności.</span><span class="sxs-lookup"><span data-stu-id="3ad35-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="3ad35-249">Użytkownik może zdefiniować następujące typy reguł fakturowania:</span><span class="sxs-lookup"><span data-stu-id="3ad35-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="3ad35-250">**Jednostka dostawy** — Faktura dla klienta po wykonaniu jednostki dostawy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="3ad35-251">Jednostki dostawy są definiowane w kontrakcie.</span><span class="sxs-lookup"><span data-stu-id="3ad35-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="3ad35-252">**Postęp** — wystawianie faktury dla klienta po wykonaniu określonej wartości procentowej projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="3ad35-253">Użytkownik może skonfigurować regułę fakturowania, aby automatycznie obliczać procent wykonanej pracy, lub ręcznie obliczyć procent wykonania pracy oraz kwotę, aby zafakturować klienta.</span><span class="sxs-lookup"><span data-stu-id="3ad35-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="3ad35-254">**Punkt kontrolny** — Faktura dla klienta w celu uzyskania pełnej kwoty punktów kontrolnych projektu, gdy zostanie osiągnięty punkt kontrolny.</span><span class="sxs-lookup"><span data-stu-id="3ad35-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="3ad35-255">**Opłata** — Faktura klienta dla usługi wraz z opłatą za zarządzanie, czyli zazwyczaj procent kosztu usług.</span><span class="sxs-lookup"><span data-stu-id="3ad35-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="3ad35-256">**Czas i materiały** — Faktura klienta dla wartości czasu i materiałów używanych w projekcie.</span><span class="sxs-lookup"><span data-stu-id="3ad35-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="3ad35-257">W przypadku wszystkich typów reguł rozliczeniowych można określić procent zatrzymania, który jest odejmowany od faktur klientów, dopóki projekt nie osiągnie uzgodnionego etapu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="3ad35-258">Procent zatrzymania płatności jest określany w kontrakcie projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="3ad35-259">Kwota jest obliczana na podstawie i odjęta od wartości łącznej wierszy na fakturze dla klienta.</span><span class="sxs-lookup"><span data-stu-id="3ad35-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="3ad35-260">Aby zmienić reguły fakturowania **Czasu i materiału** oraz **Postępu**, można przypisać kategorie wymagalności.</span><span class="sxs-lookup"><span data-stu-id="3ad35-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="3ad35-261">Kategorie podlegające opłacie wskazują transakcje, które powinny być uwzględnione na fakturach odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="3ad35-262">Gdy jesteś gotowy do wystawienia faktury na klienta, kwota do faktury za projekt jest obliczana na podstawie reguł fakturowania i generowana jest propozycja faktury za projekt.</span><span class="sxs-lookup"><span data-stu-id="3ad35-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="3ad35-263">Poniższe sekcje zawierają przykłady dotyczące konfigurowania reguł fakturowania i zarządzania nimi.</span><span class="sxs-lookup"><span data-stu-id="3ad35-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="3ad35-264">Przykład: Tworzenie reguły fakturowania opartej na liczbie dostarczonych jednostek</span><span class="sxs-lookup"><span data-stu-id="3ad35-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="3ad35-265">Organizacja wejdzie w umowę w celu udzielenia łącznej liczby pięciu sesji szkoleniowych pracownikom klienta z kosztem 10 000 na sesję szkoleniową.</span><span class="sxs-lookup"><span data-stu-id="3ad35-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="3ad35-266">Klient otrzymuje wystawioną fakturę po każdej sesji szkoleniowej.</span><span class="sxs-lookup"><span data-stu-id="3ad35-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="3ad35-267">Konfigurując reguły fakturowania dla kontraktu, należy użyć następujących wartości:</span><span class="sxs-lookup"><span data-stu-id="3ad35-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="3ad35-268">Jednostką z dostawy jest jedna sesja szkoleniowa.</span><span class="sxs-lookup"><span data-stu-id="3ad35-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="3ad35-269">Cena jednostkowa wynosi 10 000 na sesję szkoleniową.</span><span class="sxs-lookup"><span data-stu-id="3ad35-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="3ad35-270">Łączna liczba jednostek wynosi pięć sesji szkoleniowych.</span><span class="sxs-lookup"><span data-stu-id="3ad35-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="3ad35-271">Po ukończeniu jednej sesji szkoleniowej możesz utworzyć fakturę na 10 000 za pierwszą dostarczoną jednostkę i wysłać fakturę do klienta.</span><span class="sxs-lookup"><span data-stu-id="3ad35-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="3ad35-272">Przykład: Utwórz regułę rozliczeniową opartą na określonym odsetku ukończenia projektu (obliczenie ręczne)</span><span class="sxs-lookup"><span data-stu-id="3ad35-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="3ad35-273">Twoja organizacja, firma konsultingowa w zakresie oprogramowania, zawiera umowę z klientem na opracowanie części produktu, który ten klient opracowuje.</span><span class="sxs-lookup"><span data-stu-id="3ad35-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="3ad35-274">Twoja organizacja zgadza się dostarczać kod oprogramowania przez okres sześciu miesięcy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="3ad35-275">Klient zgadza się zapłacić za tę pracę organizacji sumę 100 000.</span><span class="sxs-lookup"><span data-stu-id="3ad35-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="3ad35-276">Tworzysz regułę fakturowania, aby fakturować klienta na podstawie procentu pracy wykonanej w projekcie, zgodnie z umową.</span><span class="sxs-lookup"><span data-stu-id="3ad35-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="3ad35-277">Pod koniec pierwszego miesiąca spotykasz się z klientem, aby określić procent wykonanej pracy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="3ad35-278">Po przejrzeniu projektu z klientem decydujesz, że projekt został ukończony w 15%.</span><span class="sxs-lookup"><span data-stu-id="3ad35-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="3ad35-279">Tworzysz fakturę na 15 000 (15% ze 100 000) i wysyłasz ją do klienta.</span><span class="sxs-lookup"><span data-stu-id="3ad35-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="3ad35-280">Przykład: Utwórz regułę rozliczeniową opartą na określonym odsetku ukończenia projektu (obliczenie automatyczne)</span><span class="sxs-lookup"><span data-stu-id="3ad35-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="3ad35-281">Twoja organizacja, firma programistyczna, zgadza się opracować pakiet rozliczeń płac dla klienta za 30 000.</span><span class="sxs-lookup"><span data-stu-id="3ad35-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="3ad35-282">Klient zgadza się zapłacić Twojej organizacji na podstawie procentu wykonanej pracy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="3ad35-283">Szacujemy, że koszty projektów są 20 000.</span><span class="sxs-lookup"><span data-stu-id="3ad35-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="3ad35-284">Kontrakt dotyczący projektu określa kategorie pracy używane w procesie fakturowania.</span><span class="sxs-lookup"><span data-stu-id="3ad35-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="3ad35-285">Skonfigurujesz reguły rozliczeniowe, które automatycznie obliczają kwoty faktur dla procentu pracy wykonanej dla każdej kategorii.</span><span class="sxs-lookup"><span data-stu-id="3ad35-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="3ad35-286">Użytkownik konfiguruje budżet dla każdej kategorii.</span><span class="sxs-lookup"><span data-stu-id="3ad35-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="3ad35-287">**Opracowywanie** — koszt 15 000 i przychód 20 000</span><span class="sxs-lookup"><span data-stu-id="3ad35-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="3ad35-288">**Instalacja** — koszt 5 000 i przychód 10 000</span><span class="sxs-lookup"><span data-stu-id="3ad35-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="3ad35-289">Podczas tworzenia faktury dla odbiorcy po raz pierwszy kwota faktury jest obliczana automatycznie na podstawie następujących informacji:</span><span class="sxs-lookup"><span data-stu-id="3ad35-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="3ad35-290">Po upływie miesiąca pracownik projektu przesyła grafik do projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="3ad35-291">Koszt godzin pracy pracownika wynosi 5 000 w przypadku opracowania i 1 000 instalacji.</span><span class="sxs-lookup"><span data-stu-id="3ad35-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="3ad35-292">Prace rozwojowe ukończono w 33% (5000 kosztów rzeczywistych/15000 kosztów budżetowych), a prace instalacyjne ukończono w 20% (1000 kosztów rzeczywistych/5000 kosztów budżetowych).</span><span class="sxs-lookup"><span data-stu-id="3ad35-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="3ad35-293">Kwota faktury 8 667 jest obliczana automatycznie (33 procent z 20 000 + 20 procent z 10 000).</span><span class="sxs-lookup"><span data-stu-id="3ad35-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="3ad35-294">Tworzysz fakturę na 8667 i wysyłasz ją do klienta.</span><span class="sxs-lookup"><span data-stu-id="3ad35-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="3ad35-295">Przykład: Tworzenie reguły fakturowania opartej na uzgodnionych punktach kontrolnych</span><span class="sxs-lookup"><span data-stu-id="3ad35-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="3ad35-296">Twoja organizacja, firma konsultingowa w zakresie zarządzania, zgadza się na przeprowadzenie badań rynkowych produktu konsumenckiego, który klient planuje sprzedać.</span><span class="sxs-lookup"><span data-stu-id="3ad35-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="3ad35-297">Klient zgadza się korzystać z Twoich usług przez okres trzech miesięcy, począwszy od marca, i zgadza się zapłacić Twojej organizacji 50 000.</span><span class="sxs-lookup"><span data-stu-id="3ad35-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="3ad35-298">Projekt ma trzy punkty kontrolne:</span><span class="sxs-lookup"><span data-stu-id="3ad35-298">The project has three milestones:</span></span>

-   <span data-ttu-id="3ad35-299">Punkt kontrolny 1: zbieranie danych o klientach – 31 marca</span><span class="sxs-lookup"><span data-stu-id="3ad35-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="3ad35-300">Punkt kontrolny 2: analizowanie danych o klientach — 30 Kwiecień</span><span class="sxs-lookup"><span data-stu-id="3ad35-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="3ad35-301">Punkt kontrolny 3: Przedstaw propozycję opłacalności produktu — 31 maja</span><span class="sxs-lookup"><span data-stu-id="3ad35-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="3ad35-302">Klient zgadza się zapłacić Twojej organizacji 10 000 za pierwszy kamień milowy, 20 000 za drugi i 20 000 za trzeci.</span><span class="sxs-lookup"><span data-stu-id="3ad35-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="3ad35-303">Podczas konfigurowania kontraktu dotyczącego projektu użytkownik zgadza się wystawić fakturę na podstawie spełnionego punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="3ad35-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="3ad35-304">Konfiguracja reguły fakturowania obejmuje następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="3ad35-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="3ad35-305">Definiowanie punktów kontrolnych projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-305">Define the project milestones.</span></span>
-   <span data-ttu-id="3ad35-306">W tym polu należy zdefiniować kwotę, która ma zostać zafakturowana dla klienta po zakończeniu poszczególnych punktów kontrolnych.</span><span class="sxs-lookup"><span data-stu-id="3ad35-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="3ad35-307">Gdy pierwszy kamień milowy zostanie ukończony 31 marca, oznaczasz go jako ukończony, a następnie tworzysz fakturę na 10 000 i wysyłasz ją do klienta.</span><span class="sxs-lookup"><span data-stu-id="3ad35-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="3ad35-308">Nie możesz utworzyć faktury za kamień milowy, dopóki nie oznaczysz go jako ukończonego.</span><span class="sxs-lookup"><span data-stu-id="3ad35-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="3ad35-309">Przykład: Utwórz regułę rozliczeń opartą na usługach plus opłata za zarządzanie</span><span class="sxs-lookup"><span data-stu-id="3ad35-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="3ad35-310">Twoja organizacja, firma konsultingowa w zakresie zarządzania, zgadza się na przeprowadzenie badań rynkowych w celu oceny rentowności produktu opracowywanego przez klienta, firmę zajmującą się sprzedażą detaliczną.</span><span class="sxs-lookup"><span data-stu-id="3ad35-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="3ad35-311">Warunki umowy określają, że będziesz świadczył usługi trzech najlepszych konsultantów ds. Zarządzania, którzy przeprowadzą badanie na podstawie czasu i materiałów.</span><span class="sxs-lookup"><span data-stu-id="3ad35-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="3ad35-312">Klient zgadza się zapłacić 100 za godzinę plus 10 procent opłaty za zarządzanie za godziny konsultacji naliczane w ramach projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="3ad35-313">Podczas konfigurowania umowy dotyczącej projektu utwórz regułę fakturowania, aby dodać 10-procentową opłatę za zarządzanie do godzin konsultacji naliczanych w ramach projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="3ad35-314">Kiedy tworzysz fakturę dla klienta, klient jest obciążany 10-procentową opłatą za zarządzanie plus koszt godzin konsultacji.</span><span class="sxs-lookup"><span data-stu-id="3ad35-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="3ad35-315">Na przykład, jeśli trzech konsultantów przepracowało łącznie 200 godzin nad projektem, faktura na 22 000 jest tworzona na podstawie następujących obliczeń:</span><span class="sxs-lookup"><span data-stu-id="3ad35-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="3ad35-316">200 godzin za 100 na godzinę = 20 000</span><span class="sxs-lookup"><span data-stu-id="3ad35-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="3ad35-317">10 procent opłaty za zarządzanie = 2 000</span><span class="sxs-lookup"><span data-stu-id="3ad35-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="3ad35-318">Łączna kwota na fakturze = 22 000</span><span class="sxs-lookup"><span data-stu-id="3ad35-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="3ad35-319">Jeśli opłaty podlegają opodatkowaniu dla odbiorcy i wybierzesz grupę podatków w umowie dotyczącej projektu, grupa podatków zostanie automatycznie wprowadzona do reguły rozliczeniowej dla opłat.</span><span class="sxs-lookup"><span data-stu-id="3ad35-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="3ad35-320">Przykład: Utwórz regułę rozliczeniową dla wartości czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="3ad35-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="3ad35-321">Twoja organizacja, firma konsultingowa w zakresie oprogramowania, zgadza się zapewnić pięciu konsultantów technicznych do pracy nad projektem rozwoju oprogramowania dla klienta przez następne sześć miesięcy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="3ad35-322">Klient zgadza się na płatę kwoty 150 za każdą godzinę konsultacji, a także koszt materiałów biurowych.</span><span class="sxs-lookup"><span data-stu-id="3ad35-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="3ad35-323">Na koniec każdego miesiąca organizacja wysyła fakturę do klienta.</span><span class="sxs-lookup"><span data-stu-id="3ad35-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="3ad35-324">Konfigurując umowę dotyczącą projektu, zgadzasz się co miesiąc wystawiać klientowi fakturę za czas i materiały związane z projektem.</span><span class="sxs-lookup"><span data-stu-id="3ad35-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="3ad35-325">Użytkownik tworzy regułę fakturowania zawierającą następujące informacje:</span><span class="sxs-lookup"><span data-stu-id="3ad35-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="3ad35-326">Okres objęty umową wynosi sześć miesięcy.</span><span class="sxs-lookup"><span data-stu-id="3ad35-326">The contract period is six months.</span></span>
-   <span data-ttu-id="3ad35-327">Czas konsultacji jest obliczany na podstawie stawki 150 na godzinę.</span><span class="sxs-lookup"><span data-stu-id="3ad35-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="3ad35-328">Materiały biurowe są fakturowane po kosztach, a całkowity koszt projektu nie może przekraczać 10 000.</span><span class="sxs-lookup"><span data-stu-id="3ad35-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="3ad35-329">Tworzysz fakturę dla klienta na koniec każdego miesiąca kalendarzowego w trakcie trwania projektu.</span><span class="sxs-lookup"><span data-stu-id="3ad35-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="3ad35-330">W pierwszym miesiącu konsultanci projektu rejestrują łącznie 800 godzin.</span><span class="sxs-lookup"><span data-stu-id="3ad35-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="3ad35-331">Koszt materiałów biurowych obciążających projekt wynosi 2000.</span><span class="sxs-lookup"><span data-stu-id="3ad35-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="3ad35-332">Dlatego na koniec miesiąca tworzysz fakturę na 122 000, która jest obliczana jako 800 godzin przy 150 na godzinę plus 2 000 na materiały biurowe.</span><span class="sxs-lookup"><span data-stu-id="3ad35-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]