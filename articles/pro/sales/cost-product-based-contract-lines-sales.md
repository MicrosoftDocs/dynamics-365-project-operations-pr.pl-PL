---
title: Wycena pozycji kontraktu opartego na produkcie - wersja uproszczona
description: Ten temat zawiera informacje o tworzeniu
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273706"
---
# <a name="cost-product-based-contract-lines---lite"></a>Wycena pozycji kontraktu opartego na produkcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Wiersze kontraktu oparte na produkcie w Dynamics 365 Project Operations zawierają pole **Koszt własny**, w którym przechowywana jest cena własna produktu na potrzeby obliczeń rentowności na dalszych etapach.

Po utworzeniu pozycji umowy opartej na produktach dla produktu z katalogu, koszt wiersza jest ustawiany domyślnie w polu **Koszt normatywny** w katalogu produktów. Pole **Koszt normatywny** w katalogu produktów jest podawane w walucie podstawowej organizacji. Kiedy koszt jednostkowy jest domyślnie związany z pozycją kontraktu, jest konwertowany na walutę sprzedaży dotyczącą kontraktu.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Koszt jednostkowy w wierszu kontraktu opartej na produkcie

Dysponowanie kosztami jednostkowymi w wierszu kontraktu opartego na produkcie pozwala na zastosowanie różnych kosztów produktu w danej sprzedaży jednostki. Choć nie zawsze jest to konieczne, istnieje kilka scenariuszy, w których koszt produktu może być zredukowany na rzecz klienta. Rozważmy następujący scenariusz:

Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Adatum Corporation. Firma Fabrikam świadczy usługi instalacyjne, ale ramiona robotów pochodzą z firmy Trey Research. Jeśli instalacja ramion w Adatum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey Research, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki. W takim przypadku firma Fabrikam tworzy linię kontraktową opartą na produktach dla ramion robotów. W przypadku kontraktu jest wprowadzany koszt jednostkowy. Koszt jest inny niż koszt zakupu od firmy Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]