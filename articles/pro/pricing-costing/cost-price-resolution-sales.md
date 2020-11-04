---
title: Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych
description: W tym temacie przedstawiono informacje na temat sposobu rozwiązywania kosztów kosztu na szacunkach i wartościach rzeczywistych.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bad8f4b95ac5803d3f334e1b306d2a9d27a6645d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081922"
---
# <a name="resolving-cost-prices-on-estimates-and-actuals"></a>Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W celu rozpoznania cennika i listy kosztów własnych na potrzeby oszacowań i wartości rzeczywistych,, system używa informacji zawartych w polach **Data** , **Waluta** i **Jednostka kontraktująca** z powiązanego projektu. Po rozpoznaniu listy kosztów aplikacja rozpoznaje stawkę kosztów.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Czas

Szacowane wiersze dla wartości Czas odnoszą się do oferty i pozycji kontraktu oraz do przydziałów zasobów w projekcie.

Po rozwiązaniu listy cennika, system korzysta z pól **Rola** oraz **Jednostka kontraktująca** z wiersza szacowania dla czasu, w celu dopasowania do wierszy cennika ról. To dopasowanie zakłada, że używasz przygotowanych wymiarów kalkulacji cen, aby uzyskać koszty wykonanej pracy. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał polom **Rola** i **Jednostka zasobów** lub odpowiadał także tym polom, w celu pobrania pasującego cennika ról zostanie wykorzystana inna kombinacja. Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola** oraz **Jednostką zamawiająca** , to będzie domyślna stawka kosztu. Jeśli aplikacja nie może dopasować pól **Rola** i **Jednostka zamawiająca** , program pobiera pasujące wiersze z rolą, ale ustawiane są wartości null **Jednostki zamawiającej**. Po dopasowaniu odpowiedniego rekordu ceny roli, stawka kosztu pobierana jest domyślnie z tego rekordu. 

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji **Roli** i **Jednostki zamawiającej** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie odpowiednio się zmieni. System pobiera rekordy cen ról wraz z wartościami odpowiadającymi poszczególnym wartościom wymiarów kalkulacji cen w kolejności według priorytetu. Wiersze, które mają wartości null dla tych wymiarów są ostatnie.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek

Szacowane wiersze dla wartości Wydatek odnoszą się do oferty i pozycji kontraktu dla wydatku oraz do wierszy oszacowania wydatku w projekcie.

Po rozwiązaniu listy cennika, system korzysta z połączenia pól **Kategoria** , **Firma zasobów** z wiersza szacowania dla Wydatku, w celu dopasowania do wiersza **Cena kategorii** znajdującego się w rozwiązanym cenniku. Jeśli system znajdzie wiersz ceny kategorii, który ma stawkę kosztu dla połączenia pól **Kategoria** oraz **Jednostką zasobów** , to będzie to domyślna stawka kosztu. Jeśli system nie może dopasować wartości **Kategoria** i **Jednostka** albo jeśli jest w stanie znaleźć pasujący wiersz cena kategorii, ale metoda kalkulacji cena nie jest ustawiona na wartość **Ceną jednostkową** , stawka kosztów jest domyślnie ustawiona na zero (0).
