---
title: Rozwiązywanie kosztów własnych dla oszacowań i wartości rzeczywistych
description: W tym temacie przedstawiono informacje na temat sposobu rozwiązywania kosztów kosztu na szacunkach i wartościach rzeczywistych.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d81b521acbfd97127cf056bd41a3249c01108374
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001394"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Rozwiązywanie kosztów własnych dla oszacowań i wartości rzeczywistych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W celu rozpoznania cennika i listy kosztów własnych na potrzeby oszacowań i wartości rzeczywistych,, system używa informacji zawartych w polach **Data**, **Waluta** i **Jednostka kontraktująca** z powiązanego projektu. Po rozpoznaniu listy kosztów aplikacja rozpoznaje stawkę kosztów.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Czas

Szacowane wiersze dla wartości Czas odnoszą się do oferty i pozycji kontraktu oraz do przydziałów zasobów w projekcie.

Po rozwiązaniu listy cennika, system korzysta z pól **Rola**, **Firma zasobów** oraz **Jednostka zasobów** z wiersza szacowania dla czasu, w celu dopasowania do wierszy cennika ról. To dopasowanie zakłada, że używasz przygotowanych wymiarów kalkulacji cen, aby uzyskać koszty wykonanej pracy. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał polom **Rola**, **Firma zasobów** i **Jednostka zasobów** lub odpowiadał także tym polom, w celu pobrania pasującego cennika ról zostanie wykorzystana inna kombinacja. Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola**, **Firma zasobów** oraz **Jednostką zasobów**, to będzie to domyślna stawka kosztu. Jeśli aplikacja nie może dokładnie dopasować kombinacji wartości **Rola**, **Firma zasobów** i **Jednostka zasobów**, spowoduje to pobranie wierszy cen ról o pasującej wartości roli, ale wartości null dla **Jednostka zasobów** i **Firma zasobów**. Po znalezieniu pasującego rekordu ceny roli z pasującą wartością ceny roli, domyślna stawka kosztów z tego rekordu. 

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji **Roli**, **Firmy zasobów** i **Jednostki zasobów** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie odpowiednio się zmieni. System pobiera rekordy cen ról z wartościami, które pasują do każdej z wartości wymiarów wyceny w kolejności priorytetu, z wierszami, które mają wartości null dla tych wymiarów, które są ostatnie w kolejności priorytetu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek

Szacowane wiersze dla wartości Wydatek odnoszą się do oferty i pozycji kontraktu dla wydatku oraz do wierszy oszacowania wydatku w projekcie.

Po rozwiązaniu listy cennika, system korzysta z połączenia pól **Kategoria**, **Firma zasobów** z wiersza szacowania dla Wydatku, w celu dopasowania do wiersza **Cena kategorii** znajdującego się w rozwiązanym cenniku. Jeśli system znajdzie wiersz ceny kategorii, który ma stawkę kosztu dla połączenia pól **Kategoria** oraz **Jednostką zasobów**, to będzie to domyślna stawka kosztu. Jeśli system nie może dopasować wartości **Kategoria** i **Jednostka** albo jeśli jest w stanie znaleźć pasujący wiersz cena kategorii, ale metoda kalkulacji cena nie jest ustawiona na wartość **Ceną jednostkową**, stawka kosztów jest domyślnie ustawiona na zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rozwiązywanie problemów z kosztami w wierszach rzeczywistych i szacowanych dla materiałów

Wiersze szacowania materiałów odwołują się do szczegółów oferty i wiersza kontraktu dla materiałów i wierszy szacowania materiałów w projekcie.

Po ustaleniu cennika kosztów system wykorzystuje kombinację pól **Produkt** i **Jednostka** w wierszu szacowania, aby oszacować materiał w celu dopasowania do wiersze **Pozycje cennika** na ustalonym cenniku. Jeśli system znajdzie wiersz cen produktu z cennikem dla kombinacji pól **Produkt** i **Jednostka**, koszt własny jest domyślny. Jeśli system nie jest w stanie dopasować wartości **Produkt** i **Jednostka**, koszt jednostki jest domyślnie równy zeru. Ta wartość domyślna wystąpi również, jeśli istnieje pasująca pozycja pozycji cennika, ale metoda wyceny jest oparta na koszcie standardowym lub koszcie bieżącym, który nie jest zdefiniowany w produkcie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
