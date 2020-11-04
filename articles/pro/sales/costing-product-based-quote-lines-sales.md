---
title: Wycena wierszy oferty opartej na produkcie
description: Ta temat zawiera informacje o stosowaniu kosztu własnego w wierszu oferty opartej na produktach.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081915"
---
# <a name="costing-product-based-quote-lines"></a>Wycena wierszy oferty opartej na produkcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Wiersze oferty opartej na produkcie w Dynamics 365 Project Operations są również dostępne jako pole **Kosztu własnego**. To pole jest używane do śledzenia kosztu własnego produktu w wierszu oferty oraz na potrzeby obliczeń opłacalności na niższych poziomach.

W przypadku tworzenia wiersza oferty opartej na produkcie dotyczącego produktu z katalogu, cena w wierszu oferty opartej na produkcie jest domyślnie określana na podstawie pola **Koszt normatywny** w katalogu produktów. Pole Koszt normatywny w katalogu produktów jest podawane w walucie podstawowej organizacji. Domyślny koszt jednostkowy w wierszu oferty opartej na produkcie jest konwertowany na walutę sprzedaży z oferty.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Koszt jednostkowy w wierszu oferty opartej na produkcie

Celem dysponowania kosztami jednostkowymi w wierszu oferty opartej na produkcie jest zezwolenie na zastosowanie różnych kosztów produktu w danej sprzedaży. Nie jest to typowy scenariusz użycia, ale czasami koszt produktu może być obniżony przez dostawcę w zależności od klienta.

Na przykład:

Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Datum Corporation. Firma Fabrikam oferuje usługi instalacyjne, ale ramiona są wytwarzane przez inną firmę — Trey robotics. Jeśli instalacja ramion w Datum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki.

W takiej sytuacji Fabrikam będzie tworzył wiersz oferty opartej na produkcie dla ramion robotycznych i skorzystać ze specjalnego kosztu jednostkowego dla takiej oferty. Koszty różnią się od kosztów normatywnych ramion robotycznych Trey.
