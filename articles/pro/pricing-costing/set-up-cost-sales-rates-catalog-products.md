---
title: Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona
description: Ten temat zawiera informacje na temat konfigurowania kosztów i stawek sprzedaży dla towarów w katalogu produktów.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176714"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="45cad-103">Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="45cad-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="45cad-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="45cad-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="45cad-105">Konfigurowanie kalkulacji cen dla elementów katalogu produktów w programie Dynamics 365 Project Operations działa tak samo jak w przypadku Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="45cad-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="45cad-106">Ponieważ produkty nie są szacowane ani używane w projektach w ramach Project Operations, nie trzeba ustawiać cen katalogu produktów na cennikach projektów dla ofert i kontraktów.</span><span class="sxs-lookup"><span data-stu-id="45cad-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="45cad-107">Ceny katalogu produktów należy ustawić w polu **Cena produktu** w ofercie, kontrakcie lub koncie.</span><span class="sxs-lookup"><span data-stu-id="45cad-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="45cad-108">Nie należy konfigurować cen katalogu produktów w cennikach projektów dla tych encji.</span><span class="sxs-lookup"><span data-stu-id="45cad-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="45cad-109">Cenniki projektu są dostępne wyłącznie w ramach Project Operations.</span><span class="sxs-lookup"><span data-stu-id="45cad-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="45cad-110">Istnieją specyficzne dla aplikacji reguły biznesowe, które polegają na kopiowaniu cenników z oferty do kontraktu.</span><span class="sxs-lookup"><span data-stu-id="45cad-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="45cad-111">W wyniku takiego działania powstaje cennik specyficzny dla danego kontraktu.</span><span class="sxs-lookup"><span data-stu-id="45cad-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="45cad-112">Dzięki operacji kopiowania można opóźnić licytację oferty, jeśli cennik projektu w ofercie stanie się za duży.</span><span class="sxs-lookup"><span data-stu-id="45cad-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="45cad-113">Cenniki produktu nie są kopiowane w celu utworzenia cenników niestandardowych na potrzeby kontraktów.</span><span class="sxs-lookup"><span data-stu-id="45cad-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="45cad-114">Oznacza to, że cenniki produktów nie wpływają na wydajność procesu sprzedaży z licytacją oferty.</span><span class="sxs-lookup"><span data-stu-id="45cad-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
