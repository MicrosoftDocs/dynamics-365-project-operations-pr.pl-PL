---
title: Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych projektu
description: To temat zawiera informacje na temat sposobu rozwiązania kosztów w szacowaniach i wartościach rzeczywistych projektu.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997574"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych projektu 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rozwiązywanie problemów z kosztami w wierszach rzeczywistych i szacowanych dla materiałów

Wiersze szacowania materiałów odwołują się do szczegółów oferty i wiersza kontraktu dla materiałów i wierszy szacowania materiałów w projekcie.

Po ustaleniu cennika kosztów system wykorzystuje kombinację pól **Produkt** i **Jednostka** w wierszu szacowania, aby oszacować materiał w celu dopasowania do wiersze **Pozycje cennika** na ustalonym cenniku. Jeśli system znajdzie wiersz cen produktu z cennikem dla kombinacji pól **Produkt** i **Jednostka**, koszt własny jest domyślny. Jeśli system nie może dopasować wartości **Produkt** i **Jednostka** lub jeśli jest w stanie znaleźć pasującą pozycję pozycji cennika, ale metoda kalkulacji cen jest oparta na kosztach normatywnych lub koszcie bieżącym i żaden nie jest zdefiniowany dla produktu, koszt jednostkowy jest domyślnie równy zeru.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
