---
title: Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych — wersja uproszczona
description: W tym temacie przedstawiono informacje na temat sposobu rozwiązywania kosztów kosztu na szacunkach i wartościach rzeczywistych.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764607"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W celu rozpoznania cennika i listy kosztów własnych na potrzeby oszacowań i wartości rzeczywistych,, system używa informacji zawartych w polach **Data**, **Waluta** i **Jednostka kontraktująca** z powiązanego projektu. Po rozpoznaniu listy kosztów aplikacja rozpoznaje stawkę kosztów.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Czas

Szacowane wiersze dla wartości Czas odnoszą się do oferty i pozycji kontraktu oraz do przydziałów zasobów w projekcie.

Po rozpoznaniu cennika kosztów pola **Rola** i **Jednostka ponownego zakupu** w wierszu szacowania czasu są dopasowane do wierszy cen roli w cenniku. To dopasowanie zakłada, że używasz standardowych wymiarów cenowych dla kosztów pracy. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał polom **Rola** i **Jednostka zasobów** lub odpowiadał także tym polom, w celu pobrania pasującego cennika ról zostanie wykorzystana inna kombinacja. Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola** oraz **Jednostką zamawiająca**, to będzie domyślna stawka kosztu. Jeśli aplikacja nie może dopasować pól **Rola** i **Jednostka zamawiająca**, program pobiera pasujące wiersze z rolą, ale ustawiane są wartości null **Jednostki zamawiającej**. Po dopasowaniu odpowiedniego rekordu ceny roli, stawka kosztu pobierana jest domyślnie z tego rekordu. 

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji **Roli** i **Jednostki zamawiającej** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie odpowiednio się zmieni. System pobiera rekordy cen ról wraz z wartościami odpowiadającymi poszczególnym wartościom wymiarów kalkulacji cen w kolejności według priorytetu. Wiersze, które mają wartości null dla tych wymiarów są ostatnie.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek

Szacowane wiersze dla wartości Wydatek odnoszą się do oferty i pozycji kontraktu dla wydatku oraz do wierszy oszacowania wydatku w projekcie.

Po rozwiązanie cennika kosztów system używa kombinacji pól **Kategoria** i **Jednostka** w wierszu szacowania wydatku w celu dopasowania do wierszy **Ceny kategorii** na cenniku rozwiązanym. Jeśli system znajdzie wiersz ceny kategorii, który ma stawkę kosztu dla połączenia pól **Kategoria** oraz **Jednostką zasobów**, to będzie to domyślna stawka kosztu. Jeśli system nie może dopasować wartości **Kategoria** i **Jednostka** lub jeśli jest w stanie znaleźć pasującą linią cen kategorii, ale metoda kalkulacji cen nie to **Cena jednostkowa**, koszt jest domyślny do zera(0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]