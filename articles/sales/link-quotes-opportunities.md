---
title: Tworzenie ofert projektu na podstawie szans sprzedaży
description: Ta temat zawiera informacje na temat tworzenia ofert z poziomu szans sprzedaży.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898545"
---
# <a name="create-project-quotes-from-opportunities"></a>Tworzenie ofert projektu na podstawie szans sprzedaży

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Oferty mogą być tworzone na podstawie szans sprzedaży projektów w następujący sposób:

- Z poziomu karty **Oferty** na stronie **Szansa sprzedaży**
- Z poziomu procesu przepływu szansy sprzedaży
- Aktualizując odwołanie do szansy sprzedaży na istniejącej ofercie

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Z poziomu karty Oferty na stronie Szansa sprzedaży

Aby utworzyć ofertę projektu z szansy sprzedaży, należy wykonać następujące kroki.

1. Otworzyć stronę **Szansa sprzedaży** na karcie **Oferty**. 
2. W podsiatce **Oferty** wybrać opcję **+** w celu utworzenia nowej oferty projektu na podstawie szansy sprzedaży. Wszystkie wiersze szans sprzedaży i powiązane z nimi cenniki projektu są kopiowane do nowej oferty z szansy sprzedaży.

## <a name="from-the-opportunity-sales-process-flow"></a>Z poziomu procesu przepływu szansy sprzedaży

Aby utworzyć ofertę projektu z procesu przepływu szansy sprzedaży, należy wykonać następujące kroki.

1. Otwórz szansę sprzedaży z poziomu przepływu procesu.
2. Wybierz etap **Kwalifikacja**. 
3. Wybierz opcję **Dalej**, a następnie wybierz pozycję **+ Utwórz**, aby utworzyć nową ofertę. Większość informacji znajdujących się na karcie **Podsumowanie** tej nowej oferty będzie domyślnie wybierana na podstawie szansy sprzedaży. 
4. Wprowadź wymagane brakujące informacje lub zaktualizuj wartości domyślne zgodnie z wymaganiami na **karcie Podsumowanie**.
5. Wybierz pozycję **Zapisz**. Nowa oferta zostanie utworzona i skojarzona z szansą sprzedaży. Można teraz wyświetlić informacje o ofercie na karcie **Oferty** na stronie **Szansa sprzedaży**. 

   Proces sprzedaży dla szansy sprzedaży zostanie przesunięty do kolejnego etapu i **Zaproponowany**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Aktualizując odwołanie do szansy sprzedaży na istniejącej ofercie

Istniejącą ofertę można połączyć z szansą sprzedaży. Wykonaj poniższe kroki, aby zaktualizować informacje o szansie sprzedaży dla istniejącej oferty.

1. Otwórz stronę **Oferta** na karcie **Podsumowanie**.
2. W polu **Szansa sprzedaży** wybierz szansę sprzedaży, która ma zostać połączona z ofertą. Oferta jest widoczna w siatce **Ofert** w szansie sprzedaży. 
3. Korzystając z procesu sprzedaży szansy sprzedaży, szansa sprzedaży może zostać przeniesiona do kolejnego etapu i **Zaproponowana**. 

   Po przeniesieniu szansy sprzedaży do danego etapu można wybrać tę ofertę z listy ofert skojarzonych z daną szansą sprzedaży. Zaznaczenie tej oferty oznacza, że jest ona wybrana do dalszego przetwarzania.

   Wszystkie pozostałe oferty skojarzone z szansą sprzedaży będą nadal dostępne i aktywne do chwili wygrania jednej z nich. Użytkownik może przenieść proces sprzedaży z powrotem na poprzedni etap **Kwalifikowanie** i wybrać inną ofertę.
