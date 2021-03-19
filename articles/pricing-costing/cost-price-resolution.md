---
title: Rozwiązywanie kosztów własnych dla oszacowań i wartości rzeczywistych
description: W tym temacie przedstawiono informacje na temat sposobu rozwiązywania kosztów kosztu na szacunkach i wartościach rzeczywistych.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275686"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Rozwiązywanie kosztów własnych dla oszacowań i wartości rzeczywistych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W celu rozpoznania cennika i listy kosztów własnych na potrzeby oszacowań i wartości rzeczywistych,, system używa informacji zawartych w polach **Data**, **Waluta** i **Jednostka kontraktująca** z powiązanego projektu. Po rozpoznaniu listy kosztów aplikacja rozpoznaje stawkę kosztów.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Czas

Szacowane wiersze dla wartości Czas odnoszą się do oferty i pozycji kontraktu oraz do przydziałów zasobów w projekcie.

Po rozwiązaniu listy cennika, system korzysta z pól **Rola**, **Firma zasobów** oraz **Jednostka zasobów** z wiersza szacowania dla czasu, w celu dopasowania do wierszy cennika ról. To dopasowanie zakłada, że używasz przygotowanych wymiarów kalkulacji cen, aby uzyskać koszty wykonanej pracy. Jeśli system został skonfigurowany w taki sposób, aby odpowiadał polom **Rola**, **Firma zasobów** i **Jednostka zasobów** lub odpowiadał także tym polom, w celu pobrania pasującego cennika ról zostanie wykorzystana inna kombinacja. Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola**, **Firma zasobów** oraz **Jednostką zasobów**, to będzie to domyślna stawka kosztu. Jeśli aplikacja nie może dopasować pól **Rola**, **Firma zasobów** i **Jednostka zasobów**, program pobiera pasujące wiersze z rolą, ale ustawiane są wartości null **Jednostki zasobów**. Po dopasowaniu odpowiedniego rekordu ceny roli, stawka kosztu pobierana jest domyślnie z tego rekordu. 

> [!NOTE]
> W przypadku skonfigurowania innej prioretyzacji **Roli**, **Firmy zasobów** i **Jednostki zasobów** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie odpowiednio się zmieni. System pobiera rekordy cen ról wraz z wartościami odpowiadającymi poszczególnym wartościom wymiarów kalkulacji cen w kolejności według priorytetu. Wiersze, które mają wartości null dla tych wymiarów są ostatnie.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek

Szacowane wiersze dla wartości Wydatek odnoszą się do oferty i pozycji kontraktu dla wydatku oraz do wierszy oszacowania wydatku w projekcie.

Po rozwiązaniu listy cennika, system korzysta z połączenia pól **Kategoria**, **Firma zasobów** z wiersza szacowania dla Wydatku, w celu dopasowania do wiersza **Cena kategorii** znajdującego się w rozwiązanym cenniku. Jeśli system znajdzie wiersz ceny kategorii, który ma stawkę kosztu dla połączenia pól **Kategoria** oraz **Jednostką zasobów**, to będzie to domyślna stawka kosztu. Jeśli system nie może dopasować wartości **Kategoria** i **Jednostka** albo jeśli jest w stanie znaleźć pasujący wiersz cena kategorii, ale metoda kalkulacji cena nie jest ustawiona na wartość **Ceną jednostkową**, stawka kosztów jest domyślnie ustawiona na zero (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]