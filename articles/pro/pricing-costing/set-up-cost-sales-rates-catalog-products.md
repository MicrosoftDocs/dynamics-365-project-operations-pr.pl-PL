---
title: Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów
description: Ten temat zawiera informacje na temat konfigurowania kosztów i stawek sprzedaży dla towarów w katalogu produktów.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082079"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="1ca02-103">Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów</span><span class="sxs-lookup"><span data-stu-id="1ca02-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="1ca02-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="1ca02-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1ca02-105">Konfigurowanie kalkulacji cen dla elementów katalogu produktów w programie Dynamics 365 Project Operations działa tak samo jak w przypadku Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="1ca02-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="1ca02-106">Ponieważ produkty nie są szacowane ani używane w projektach w ramach Project Operations, nie trzeba ustawiać cen katalogu produktów na cennikach projektów dla ofert i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="1ca02-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="1ca02-107">Ceny katalogu produktów należy ustawić w polu **Cena produktu** w ofercie, kontrakcie lub koncie.</span><span class="sxs-lookup"><span data-stu-id="1ca02-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="1ca02-108">Nie należy konfigurować cen katalogu produktów w cennikach projektów dla tych encji.</span><span class="sxs-lookup"><span data-stu-id="1ca02-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="1ca02-109">Cenniki projektu są dostępne wyłącznie w ramach Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1ca02-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="1ca02-110">Istnieją specyficzne dla aplikacji reguły biznesowe, które polegają na kopiowaniu cenników z oferty do kontraktu.</span><span class="sxs-lookup"><span data-stu-id="1ca02-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="1ca02-111">W wyniku takiego działania powstaje cennik specyficzny dla danego kontraktu.</span><span class="sxs-lookup"><span data-stu-id="1ca02-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="1ca02-112">Dzięki operacji kopiowania można opóźnić licytację oferty, jeśli cennik projektu w ofercie stanie się za duży.</span><span class="sxs-lookup"><span data-stu-id="1ca02-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="1ca02-113">Cenniki produktu nie są kopiowane w celu utworzenia cenników niestandardowych na potrzeby kontraktów.</span><span class="sxs-lookup"><span data-stu-id="1ca02-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="1ca02-114">Oznacza to, że cenniki produktów nie wpływają na wydajność procesu sprzedaży z licytacją oferty.</span><span class="sxs-lookup"><span data-stu-id="1ca02-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
