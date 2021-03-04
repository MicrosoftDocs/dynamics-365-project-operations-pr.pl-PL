---
title: Metody dotyczące kosztów wykonania
description: Ten temat zawiera informacje o metodach używanych do obliczania kosztu wykonania projektu.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531514"
---
# <a name="cost-to-complete-methods"></a>Metody dotyczące kosztów wykonania

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat zawiera informacje o metodach używanych do obliczania kosztu wykonania projektu. Istnieje wiele metod, których można użyć do obliczenia kosztu wykonania projektu. 

Podczas tworzenia szacowania dla projektu, na stronie **Tworzenie szacowania** w polu **Metoda kosztu wykonania** można wybrać jedną z następujących metod obliczania kosztów wykonania.

| Metoda dotycząca kosztów wykonania    | Opis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koszt całkowity — rzeczywisty            | Wprowadź koszty ręcznie w polach **Koszt całkowity** lub **Ilość całkowita** przy użyciu przycisku **Szacowanie kosztów** na stronie **Szacowanie**. System odejmuje koszty rzeczywiste od wprowadzonych sum. Suma to koszt wykonania projektu. Ta metoda nie używa szacowań wydatków ani przypisań zasobów wprowadzonych w aplikacji Project Operations skompilowanej przy użyciu usługi Microsoft Dataverse. Całkowity koszt lub całkowitą ilość można w razie potrzeby zaktualizować ręcznie.  |
| Prognoza całkowita — wartość rzeczywista        | Przypisania zasobów i szacowania wydatków są używane do określania całkowitej kwoty prognozy projektu. Koszty rzeczywiste są porównywane z tą prognozą, aby obliczyć koszt wykonania.                                                                                                                                                                                                                                                                          |
| Jako poprzednie oszacowanie         | W tym miejscu używane są te same metody szacowania, które zostały użyte w poprzednim okresie. Ta metoda wymaga modelu prognozy w przypadku, gdy poprzedni okres wymaga modelu prognozy.                                                                                                                                                                                                                                                                                                                           |
| Ustaw koszt do ukończenia na wartość zero | Ta metoda, używana przeważnie przed wyeliminowaniem szacowania projektu, dopasowuje sumę szacowań do zaksięgowanych transakcji rzeczywistych i czyści kolumnę **kosztu wykonania**. Po zakończeniu wynik zawsze wynosi 100 procent. Dla każdego utworzonego wiersza kosztu pole wyboru **Prognozowanie** jest czyszczone, a szacowanie całkowite jest kopiowane z poprzedniego szacowania kosztów. Rzeczywista konsumpcja dla okresu szacowanego jest odejmowana od kosztu wykonania projektu.              |
| Z szablonu kosztów           | Metoda kosztu wykonania, która jest skonfigurowana w szablonie kosztu skojarzonym z wybranym szacowanym projektem.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]