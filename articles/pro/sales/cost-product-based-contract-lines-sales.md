---
title: Wycena pozycji kontraktu opartego na produkcie - wersja uproszczona
description: Ten temat zawiera informacje o tworzeniu
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177254"
---
# <a name="cost-product-based-contract-lines---lite"></a>Wycena pozycji kontraktu opartego na produkcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_


Pozycje kontraktu oparte na produktach dostępne w Dynamics 365 Project Operations to pole **Koszt własny**, w którym są przechowywane koszty własne produktu w celu realizacji obliczeń opłacalności podrzędnej.

W przypadku tworzenia wiersza kontraktu opartego na produkcie dotyczącego produktu z katalogu, cena w wierszu kontraktu opartym na produkcie jest domyślnie określana na podstawie pola **Koszt normatywny** w katalogu produktów. Pole **Koszt normatywny** w katalogu produktów jest podawane w walucie podstawowej organizacji. Kiedy koszt jednostkowy jest domyślnie związany z pozycją kontraktu, jest konwertowany na walutę sprzedaży dotyczącą kontraktu.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Koszt jednostkowy w wierszu kontraktu opartej na produkcie

Dysponowanie kosztami jednostkowymi w wierszu kontraktu opartego na produkcie pozwala na zastosowanie różnych kosztów produktu w danej sprzedaży jednostki. Choć nie zawsze jest to konieczne, istnieje kilka scenariuszy, w których koszt produktu może być zredukowany na rzecz klienta. Rozważmy następujący scenariusz:

Firma Fabrikam Robotics instaluje robotyczne ramiona na liniach montażowych w fabryce należącej do Adatum Corporation. Firma Fabrikam oferuje usługi instalacyjne, ale ramiona są wytwarzane przez inną firmę — Trey Research. Jeśli instalacja ramion w Adatum Corporation otworzy nową branżę przemysłu dla robotycznych ramion firmy Trey Research, ta druga firma może chcieć odwdzięczyć się Fabrikam za pomocą zniżki. W tym przypadku w firmie Fabrikam zostanie utworzona pozycja kontraktu oparta na produktach dla ramion robotycznych, w której podana jest cena jednostkowa dla tego kontraktu, różniąca się od standardowego kosztu ramion robotycznych od Trey Research.
