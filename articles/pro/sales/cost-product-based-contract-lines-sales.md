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
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764472"
---
# <a name="cost-product-based-contract-lines---lite"></a>Wycena pozycji kontraktu opartego na produkcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Wiersze kontraktu oparte na produkcie w Dynamics 365 Project Operations zawierają pole **Koszt własny**, w którym przechowywana jest cena własna produktu na potrzeby obliczeń rentowności na dalszych etapach.

Po utworzeniu pozycji umowy opartej na produktach dla produktu z katalogu, koszt wiersza jest ustawiany domyślnie w polu **Koszt normatywny** w katalogu produktów. Pole **Koszt normatywny** w katalogu produktów jest podawane w walucie podstawowej organizacji. Kiedy koszt jednostkowy jest domyślnie związany z pozycją kontraktu, jest konwertowany na walutę sprzedaży dotyczącą kontraktu.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Koszt jednostkowy w wierszu kontraktu opartej na produkcie

Dysponowanie kosztami jednostkowymi w wierszu kontraktu opartego na produkcie pozwala na zastosowanie różnych kosztów produktu w danej sprzedaży jednostki. Choć nie zawsze jest to konieczne, istnieje kilka scenariuszy, w których koszt produktu może być zredukowany na rzecz klienta. Rozważmy następujący scenariusz:

Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Adatum Corporation. Firma Fabrikam świadczy usługi instalacyjne, ale ramiona robotów pochodzą z firmy Trey Research. Jeśli instalacja ramion w Adatum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey Research, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki. W takim przypadku firma Fabrikam tworzy linię kontraktową opartą na produktach dla ramion robotów. W przypadku kontraktu jest wprowadzany koszt jednostkowy. Koszt jest inny niż koszt zakupu od firmy Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]