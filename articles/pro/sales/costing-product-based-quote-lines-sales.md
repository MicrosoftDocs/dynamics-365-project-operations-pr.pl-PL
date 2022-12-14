---
title: Wycena wierszy oferty opartej na produkcie
description: W tym artykule przedstawiono informacje na temat stosowania kosztu własnego do wiersza oferty opartej na produktach.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825625"
---
# <a name="costing-product-based-quote-lines"></a>Wycena wierszy oferty opartej na produkcie

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Wiersze oferty opartej na produkcie w rozwiązaniu Dynamics 365 Project Operations mają również pole **Koszt własny**. To pole jest używane do śledzenia kosztu własnego produktu w wierszu oferty oraz na potrzeby obliczeń opłacalności na niższych poziomach.

W przypadku tworzenia wiersza oferty opartej na produkcie dotyczącego produktu z katalogu, cena w wierszu oferty opartej na produkcie jest domyślnie określana na podstawie pola **Koszt normatywny** w katalogu produktów. Pole Koszt normatywny w katalogu produktów jest podawane w walucie podstawowej organizacji. Domyślny koszt jednostkowy w wierszu oferty opartej na produkcie jest konwertowany na walutę sprzedaży z oferty.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Koszt jednostkowy w wierszu oferty opartej na produkcie

Celem dysponowania kosztami jednostkowymi w wierszu oferty opartej na produkcie jest zezwolenie na zastosowanie różnych kosztów produktu w danej sprzedaży. Nie jest to typowy scenariusz użycia, ale czasami koszt produktu może być obniżony przez dostawcę w zależności od klienta.

Na przykład:

Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Datum Corporation. Firma Fabrikam oferuje usługi instalacyjne, ale ramiona są wytwarzane przez inną firmę — Trey robotics. Jeśli instalacja ramion w Datum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki.

W takiej sytuacji Fabrikam będzie tworzył wiersz oferty opartej na produkcie dla ramion robotycznych i skorzystać ze specjalnego kosztu jednostkowego dla takiej oferty. Koszty różnią się od kosztów normatywnych ramion robotycznych Trey.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
