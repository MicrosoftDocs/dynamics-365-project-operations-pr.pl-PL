---
title: Szacowania zasobu
description: W tym temat zamieszczono informacje dotyczące sposobu obliczania zasobów w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127386"
---
# <a name="resource-estimates"></a>Szacowania zasobu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Oszacowania zasobów pochodzą z nakładu pracy faz czasowych, określonego w strukturze podziału pracy oraz w zakresie odpowiednich wymiarów kalkulacji cen. Zazwyczaj obliczenia dokonywane są na podstawie następującego schematu: **współczynnik/h dla każdej roli x liczba godzin.** Nakłady pracy faz czasowych na każdy zasób są przechowywane w rekordzie przydziału zasobu. Cena jest przechowywana we wstępnie zdefiniowanym cenniku. Przeliczanie jednostek jest stosowane na podstawie odpowiednich cenników.

![Szacowania zasobu](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Wartości domyślne kosztów własnych i waluty kosztów

Koszty własne są domyślnie pobierane z jednostki organizacyjnej.

## <a name="default-bill-rate-and-sales-currency"></a>Domyślna stawka rozliczenia i waluta sprzedaży

Ceny sprzedaży są stosowane raz dla każdej transakcji. Hierarchia domyślna dla cennika sprzedaży zawiera następujące dane:

1. Organizacja
2. Klient
3. Oferta / kontrakt


[!INCLUDE[footer-include](../includes/footer-banner.md)]