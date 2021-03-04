---
title: Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona
description: Ten temat zawiera informacje na temat konfigurowania kosztów i stawek sprzedaży dla towarów w katalogu produktów.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764571"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="78e04-103">Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="78e04-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="78e04-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="78e04-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="78e04-105">Konfigurowanie cen dla pozycji katalogu produktów w Dynamics 365 Project Operations jest takie samo jak w Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="78e04-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="78e04-106">W Project Operations produktów nie można szacować ani używać w projektach, więc cen katalogowych produktów nie trzeba ustawiać w cennikach projektów dla ofert i umów.</span><span class="sxs-lookup"><span data-stu-id="78e04-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="78e04-107">Użyj pola **Cena produktu** oferty, umowy lub konta, aby skonfigurować ceny katalogu produktów.</span><span class="sxs-lookup"><span data-stu-id="78e04-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="78e04-108">Nie ustawiaj cen katalogowych produktów w cennikach projektu.</span><span class="sxs-lookup"><span data-stu-id="78e04-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="78e04-109">Cenniki projektu są dostępne wyłącznie w ramach Project Operations.</span><span class="sxs-lookup"><span data-stu-id="78e04-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="78e04-110">Logika biznesowa specyficzna dla aplikacji kopiuje cenniki z oferty do kontraktu.</span><span class="sxs-lookup"><span data-stu-id="78e04-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="78e04-111">W wyniku takiego działania powstaje cennik specyficzny dla danego kontraktu.</span><span class="sxs-lookup"><span data-stu-id="78e04-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="78e04-112">Dzięki operacji kopiowania można opóźnić licytację oferty, jeśli cennik projektu w ofercie stanie się za duży.</span><span class="sxs-lookup"><span data-stu-id="78e04-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="78e04-113">Cenniki produktu nie są kopiowane w celu utworzenia cenników niestandardowych na potrzeby kontraktów.</span><span class="sxs-lookup"><span data-stu-id="78e04-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="78e04-114">Ponieważ nie jest wymagane kopiowanie, nie ma to wpływu na wydajność procesu wyceny.</span><span class="sxs-lookup"><span data-stu-id="78e04-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
