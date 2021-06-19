---
title: Szacowania finansowe dotyczące czasu zasobów w projektach
description: Ten temat zawiera informacje o sposobie obliczania szacunków finansowych dotyczących czasu.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010799"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Szacowania finansowe dotyczące czasu zasobów w projektach

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Szacowanie finansowe czasu jest obliczane na podstawie trzech czynników: 

- Typ ogólnego lub nazwanego członka zespołu przypisanego do każdego zadania węzła-liścia w planie projektu. 
- Typ lub złożoność pracy.
- Rozkład nakładu pracy przy przypisywaniu zasobu do zadania. 

Pierwsze dwa czynniki wpływają na koszt jednostkowy lub stawkę faktury przydziału zasobu. Koszt jednostkowy lub stawka opłaty przydziału zasobu jest określana przez atrybuty przypisanego zasobu. Te atrybuty obejmują jednostkę organizacyjną, do której należy zasób, oraz standardową rolę zasobu. Możesz również dodać atrybuty niestandardowe odpowiednie dla Twojej firmy dla zasobu, takie jak standardowy tytuł lub poziom doświadczenia, i sprawić, by wpływały na koszt jednostkowy lub stawkę opłaty przydziału.
Oprócz atrybutów zasobu atrybuty pracy, takie jak zadanie, mogą również wpływać na stawkę jednostkową lub stawkę kosztów przydziału. Na przykład, gdy niektóre zadania są bardziej złożone, przypisanie zasobu do tych konkretnych zadań skutkuje wyższym kosztem jednostkowym lub stawką opłat niż zadania, które są mniej złożone.   

Trzeci współczynnik dostarcza liczbę godzin po tej stawce. W przypadkach, gdy zadanie obejmuje dwa okresy cenowe, jest prawdopodobne, że pierwsza część przydziału zasobów dla tego zadania jest wyceniana i wyceniana inaczej niż druga część zadania. Oszacowanie nakładu pracy dla każdego przydziału zasobu to złożona wartość przechowywana wraz z dziennym rozkładem wysiłku na dzień.

Aby uzyskać szczegółowe instrukcje dotyczące konfigurowania niestandardowych atrybutów pracy i zasobów jako wymiarów wyceny i cen, zobacz [Omówienie wymiarów wyceny](../pricing-costing/pricing-dimensions-overview.md).

Szacunek finansowy każdego przydziału zasobów jest obliczany jako **stawka / godz. Za przydział pomnożona przez liczbę godzin.**  Podobnie jak w przypadku oszacowania nakładu pracy, oszacowanie finansowe kosztów i przychodów dla każdego przydziału zasobów jest złożoną wartością przechowywaną wraz z dzienną dystrybucją kwoty pieniężnej. 

## <a name="summarizing-financial-estimates-for-time"></a>Podsumowanie szacowania finansowego dla czasu
Szacunek finansowy czasu wykonywania zadania węzła-liścia to suma oszacowań finansowych wszystkich przydziałów zasobów dla tego zadania.

Szacunek finansowy czasu poświęconego zadaniu sumarycznemu lub nadrzędnemu to suma oszacowań finansowych wszystkich jego zadań podrzędnych. Jest to szacowany koszt pracy w projekcie. 

![Szacowania zasobu](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Wartości domyślne kosztów własnych i waluty kosztów

Domyślna cena kosztów pochodzi z cenników dołączonych do jednostki kontraktu projektu. Walutą kosztu projektu jest zawsze waluta jednostki zamawiającej projektu. W przypadku przypisania zasobu szacowanie kosztów jest przechowywane w walucie kosztów projektu. Czasami waluta, w której stawka kosztów jest ustawiona w cenniku, różni się od waluty kosztu projektu. W tych przypadkach aplikacja konwertuje walutę, w której jest ustawiana cena kosztów dla waluty projektu. Na siatce **Szacowane** wszystkie szacowane koszty są wyświetlane i sumowane w walucie kosztów projektu. 

## <a name="default-bill-rate-and-sales-currency"></a>Domyślna stawka rozliczenia i waluta sprzedaży

Domyślna cena sprzedaży pochodzi z cenników projektu dołączonych do powiązanej umowy dotyczącej projektu, jeśli transakcja zostanie wygrana, lub z oferty związanej z projektem, jeśli transakcja jest nadal na etapie przedsprzedażowym. Walutą sprzedaży projektu jest zawsze waluta oferty projektu lub umowy dotyczącej projektu. W przypadku przydziału zasobu oszacowanie finansowe sprzedaży jest przechowywane w walucie sprzedaży projektu. W przeciwieństwie do kosztu cena sprzedaży ustawiona w cenniku nigdy nie może różnić się od waluty sprzedaży projektu. Nie ma scenariusza, w którym potrzebna jest konwersja walut. Na siatce **Szacowane** wszystkie szacunki sprzedaży są wyświetlane i podsumowywane w walucie sprzedaży projektu. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
