---
title: Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych — wersja uproszczona
description: W tym temacie przedstawiono informacje na temat sposobu rozwiązywania kosztów kosztu na szacunkach i wartościach rzeczywistych.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176804"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W celu rozpoznania cennika i listy kosztów własnych na potrzeby oszacowań i wartości rzeczywistych,, system używa informacji zawartych w polach **Data**, **Waluta** i **Jednostka kontraktująca** z powiązanego projektu. Po rozpoznaniu listy kosztów aplikacja rozpoznaje stawkę kosztów.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Czas

Szacowane wiersze dla wartości Czas odnoszą się do oferty i pozycji kontraktu oraz do przydziałów zasobów w projekcie.

Po rozwiązaniu listy cennika, system korzysta z pól **Rola** oraz **Jednostka kontraktująca** z wiersza szacowania dla czasu, w celu dopasowania do wierszy cennika ról. To dopasowanie zakłada, że używasz przygotowanych wymiarów kalkulacji cen, aby uzyskać koszty wykonanej pracy. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał polom **Rola** i **Jednostka zasobów** lub odpowiadał także tym polom, w celu pobrania pasującego cennika ról zostanie wykorzystana inna kombinacja. Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola** oraz **Jednostką zamawiająca**, to będzie domyślna stawka kosztu. Jeśli aplikacja nie może dopasować pól **Rola** i **Jednostka zamawiająca**, program pobiera pasujące wiersze z rolą, ale ustawiane są wartości null **Jednostki zamawiającej**. Po dopasowaniu odpowiedniego rekordu ceny roli, stawka kosztu pobierana jest domyślnie z tego rekordu. 

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji **Roli** i **Jednostki zamawiającej** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie odpowiednio się zmieni. System pobiera rekordy cen ról wraz z wartościami odpowiadającymi poszczególnym wartościom wymiarów kalkulacji cen w kolejności według priorytetu. Wiersze, które mają wartości null dla tych wymiarów są ostatnie.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek

Szacowane wiersze dla wartości Wydatek odnoszą się do oferty i pozycji kontraktu dla wydatku oraz do wierszy oszacowania wydatku w projekcie.

Po rozwiązaniu listy cennika, system korzysta z połączenia pól **Kategoria**, **Firma zasobów** z wiersza szacowania dla Wydatku, w celu dopasowania do wiersza **Cena kategorii** znajdującego się w rozwiązanym cenniku. Jeśli system znajdzie wiersz ceny kategorii, który ma stawkę kosztu dla połączenia pól **Kategoria** oraz **Jednostką zasobów**, to będzie to domyślna stawka kosztu. Jeśli system nie może dopasować wartości **Kategoria** i **Jednostka** albo jeśli jest w stanie znaleźć pasujący wiersz cena kategorii, ale metoda kalkulacji cena nie jest ustawiona na wartość **Ceną jednostkową**, stawka kosztów jest domyślnie ustawiona na zero (0).
