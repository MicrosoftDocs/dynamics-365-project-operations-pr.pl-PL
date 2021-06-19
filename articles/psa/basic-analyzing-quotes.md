---
title: Analiza ofert projektów
description: Ten temat zawiera informacje na temat analizowania ofert w projektach.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012464"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="a8876-103">Analiza ofert projektów</span><span class="sxs-lookup"><span data-stu-id="a8876-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a8876-104">Program Dynamics 365 Project Service Automation analizuje oferty do projektów w celu oszacowania rentowności.</span><span class="sxs-lookup"><span data-stu-id="a8876-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="a8876-105">Analizuje również, w jakim stopniu oferta jest dopasowana do oczekiwań klienta w kwestii daty dostawy lub wykonania oraz oczekiwań budżetowych.</span><span class="sxs-lookup"><span data-stu-id="a8876-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="a8876-106">Analiza rentowności</span><span class="sxs-lookup"><span data-stu-id="a8876-106">Profitability analysis</span></span>

<span data-ttu-id="a8876-107">Rozwiązanie Project Service Automation analizuje rentowność, korzystając z kryteriów marży brutto i skorygowanej marży brutto.</span><span class="sxs-lookup"><span data-stu-id="a8876-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="a8876-108">Marża brutto jest obliczana za pomocą poniższego wzoru:</span><span class="sxs-lookup"><span data-stu-id="a8876-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="a8876-109">Skorygowana marża brutto jest obliczana za pomocą poniższego wzoru:</span><span class="sxs-lookup"><span data-stu-id="a8876-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="a8876-110">Jeśli wartości marży brutto i skorygowanej marży brutto różnią bardzo się różnią, duża część pracy w ofercie jest klasyfikowana jako niepłatna.</span><span class="sxs-lookup"><span data-stu-id="a8876-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="a8876-111">Analiza oczekiwań klienta</span><span class="sxs-lookup"><span data-stu-id="a8876-111">Analysis of customer expectations</span></span>

<span data-ttu-id="a8876-112">Można analizować oferty oraz generować wykresy oczekiwań klientów w odniesieniu do harmonogramu i budżetu po wprowadzeniu wartości w następujących polach:</span><span class="sxs-lookup"><span data-stu-id="a8876-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="a8876-113">Pole **Żądana data dostawy** w nagłówku oferty.</span><span class="sxs-lookup"><span data-stu-id="a8876-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="a8876-114">Pole **Budżet klienta** dla każdego wiersza oferty (w przypadku wierszy opartych na projektach i na wierszy opartych na produktach).</span><span class="sxs-lookup"><span data-stu-id="a8876-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="a8876-115">Analiza oczekiwań klienta w kwestii harmonogramu polega na porównaniu najpóźniejszej daty zakończenia w szczegółach wiersza oferty z żądaną datą dostawy we wszystkich wierszach oferty.</span><span class="sxs-lookup"><span data-stu-id="a8876-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="a8876-116">Analiza oczekiwań klientów w kwestii budżetu polega na porównaniu sumy całkowitego budżetu klienta z kwotą oferty we wszystkich wierszach oferty.</span><span class="sxs-lookup"><span data-stu-id="a8876-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]