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
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274471"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Konfigurowanie cen dla pozycji katalogu produktów w Dynamics 365 Project Operations jest takie samo jak w Dynamics 365 Sales.

W Project Operations produktów nie można szacować ani używać w projektach, więc cen katalogowych produktów nie trzeba ustawiać w cennikach projektów dla ofert i umów.

Użyj pola **Cena produktu** oferty, umowy lub konta, aby skonfigurować ceny katalogu produktów. Nie ustawiaj cen katalogowych produktów w cennikach projektu. Cenniki projektu są dostępne wyłącznie w ramach Project Operations. Logika biznesowa specyficzna dla aplikacji kopiuje cenniki z oferty do kontraktu. W wyniku takiego działania powstaje cennik specyficzny dla danego kontraktu. Dzięki operacji kopiowania można opóźnić licytację oferty, jeśli cennik projektu w ofercie stanie się za duży. Cenniki produktu nie są kopiowane w celu utworzenia cenników niestandardowych na potrzeby kontraktów. Ponieważ nie jest wymagane kopiowanie, nie ma to wpływu na wydajność procesu wyceny.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]