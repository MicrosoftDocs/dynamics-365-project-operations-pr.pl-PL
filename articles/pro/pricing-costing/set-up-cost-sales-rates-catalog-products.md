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
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Konfigurowanie kalkulacji cen dla elementów katalogu produktów w programie Dynamics 365 Project Operations działa tak samo jak w przypadku Dynamics 365 Sales.

Ponieważ produkty nie są szacowane ani używane w projektach w ramach Project Operations, nie trzeba ustawiać cen katalogu produktów na cennikach projektów dla ofert i kontraktów.

Ceny katalogu produktów należy ustawić w polu **Cena produktu** w ofercie, kontrakcie lub koncie. Nie należy konfigurować cen katalogu produktów w cennikach projektów dla tych encji. Cenniki projektu są dostępne wyłącznie w ramach Project Operations. Istnieją specyficzne dla aplikacji reguły biznesowe, które polegają na kopiowaniu cenników z oferty do kontraktu. W wyniku takiego działania powstaje cennik specyficzny dla danego kontraktu. Dzięki operacji kopiowania można opóźnić licytację oferty, jeśli cennik projektu w ofercie stanie się za duży. Cenniki produktu nie są kopiowane w celu utworzenia cenników niestandardowych na potrzeby kontraktów. Oznacza to, że cenniki produktów nie wpływają na wydajność procesu sprzedaży z licytacją oferty.
