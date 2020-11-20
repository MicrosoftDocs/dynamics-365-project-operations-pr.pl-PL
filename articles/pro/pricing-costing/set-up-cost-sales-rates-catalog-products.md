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
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Konfigurowanie kalkulacji cen dla elementów katalogu produktów w programie Dynamics 365 Project Operations działa tak samo jak w przypadku Dynamics 365 Sales.

Ponieważ produkty nie są szacowane ani używane w projektach w ramach Project Operations, nie trzeba ustawiać cen katalogu produktów na cennikach projektów dla ofert i kontraktów.

Ceny katalogu produktów należy ustawić w polu **Cena produktu** w ofercie, kontrakcie lub koncie. Nie należy konfigurować cen katalogu produktów w cennikach projektów dla tych encji. Cenniki projektu są dostępne wyłącznie w ramach Project Operations. Istnieją specyficzne dla aplikacji reguły biznesowe, które polegają na kopiowaniu cenników z oferty do kontraktu. W wyniku takiego działania powstaje cennik specyficzny dla danego kontraktu. Dzięki operacji kopiowania można opóźnić licytację oferty, jeśli cennik projektu w ofercie stanie się za duży. Cenniki produktu nie są kopiowane w celu utworzenia cenników niestandardowych na potrzeby kontraktów. Oznacza to, że cenniki produktów nie wpływają na wydajność procesu sprzedaży z licytacją oferty.
