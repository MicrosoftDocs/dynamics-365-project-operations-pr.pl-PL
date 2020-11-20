---
title: Omówienie uzgadniania zasobów
description: Ten temat zawiera informacje o sprawdzaniu, czy rezerwazcje zasobów i przypsiania do projektów zawierają zgodne dane.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125731"
---
# <a name="resource-reconciliation-overview"></a>Omówienie uzgadniania zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Członkowie zespołu, rezerwacje i przydziały są luźno sprzężone. Innymi słowy, zasoby mogą mieć przydziały, ale mogą nie mieć rezerwacji lub mogą mieć rezerwacje bez przypisań. Najlepiej, kiedy rezerwacje i przypisania w projekcie są zgodne, bo wtedy zasoby mają zatwierdzoną dyspozycyjność do wykonania przypisanych im zadań. Jednak rezerwacje mogą być oparte na dostępności, a czasy zadań mogą ulec zmianie w miarę kontynuowania projektu. Z tego względu swobodne powiązanie rezerwacji i przypisań zapewnia elastyczność.

Karta **Uzgadnianie** w formularzu **Projekt** pozwala menedżerom projektu uzgadniać rezerwacje członków zespołu i ich przypisania w zespołach projektów.

Na karcie **Uzgadnianie** są także wyświetlane rezerwacje i przypisania na wszystkich poziomach szczegółowości, aż do poszczególnych zadań. Widać także godziny, które reprezentują okresy od miesięcy aż po dni.

Na karcie przedstawiono również ogólną sumę netto projektu wraz z kolumną **Suma**.

Dla każdego zasobu karta oblicza różnicę między rezerwacjami członka zespołu w projekcie a zestawieniem zadań przypisanych temu członkowi zespołu. Najlepiej, aby różnica wynosiła 0 (zero). Innymi słowy nie powinno być żadnej różnicy między rezerwacjami zasobu a jego przypisaniami zadań. Różnice są oznaczone kolorami i zacienione, aby zwrócić uwagę na dwa warunki:

- **Niedobór rezerwacji** — niedobory rezerwacji powstają wtedy, gdy zasób ma więcej przypisań, niż rezerwacji. Ponieważ dyspozycyjność nie została zarezerwowana, menedżer projektu może naprawić tę sytuację poprzez rozszerzenie rezerwacji zasobu w sposób pokrywający niedobór.
- **Nadmiarowe rezerwacje** — nadmierne rezerwacje występują, gdy zasób zarezerwowano do projektu, ale nie przypisano go do zadań. Ten warunek może być akceptowalny w przypadkach, gdy zasób został zarezerwowany w projekcie przed przydziałem zadania. Jednak w innych przypadkach być może nie jest planowane przypisanie zasobu do zadań. Wtedy menedżer projektu powinien rozważyć anulowanie rezerwacji zasobu, tak aby jego dyspozycyjność można było wykorzystać w innym projekcie.

W niektórych przypadkach, kiedy oglądasz czas na wyższym poziomie niż poziom dnia (np. na poziomie miesiąca), może się pojawić różnica netto zasobu równa zero (innymi słowy, rezerwacje = przydziały). Natomiast w poziomie Tydzień można zauważyć, że istnieją przypisania równe 0 (zero) godzin i rezerwacje 40 godzin w pierwszym tygodniu miesiąca oraz przypisania 40 godzin i rezerwacje równe 0 (zero) godzin w drugim tygodniu miesiąca. Ogólnie rzecz biorąc, rezerwacje i przydziały są uzgadniane, ale różnią się od siebie między tygodniami.

Po wyświetleniu wyższych poziomów czasu na karcie **Uzgadnianie** widać wskaźnik komórki informujący o różnicach na niższych poziomach czasu. Dwukrotne kliknięcie komórki umożliwia powiększenie i wyświetlenie różnicy. Następnie kliknij prawym przyciskiem myszy, aby pomniejszyć. Zaznaczając zasób, a następnie korzystając z przycisku **Następna różnica** z paska narzędzi siatki można przejść do następnej różnicy między rezerwacjami a przydziałami danego zasobu. Następnie można skorzystać z opcji **Poprzednia różnica**, aby wrócić. Istnieje również możliwość wyłączenia wskaźnika różnic i zachowania nawigacji w obszarze **ustawienia.**


W sytuacjach, gdy istnieją przypisania zadań dla zasobu, ale nie ma rezerwacji, na stronie **Projekty** na karcie **Uzgadnianie** można wybrać niedobór rezerwacji, a następnie kliknąć przycisk **Rozszerz rezerwację**. Zostanie wyświetlone okno dialogowe **Rozszerz rezerwację**, w którym przedstawiono rezerwację potrzebną do wyeliminowania problemu niedoboru zasobu. Okno to pokazuje również istniejące rezerwacje zasobu we wszystkich projektach lub innych encjach zaplanowania. W przypadku wybrania opcji **OK**, aby utworzyć rezerwację zasobu niezależnie od dostępności tego zasobu, może wystąpić rezerwacja ponad dyspozycyjność.

Następnie menedżer projektu lub menedżer zasobów może za pomocą tablicy harmonogramu rozwiązać sytuację, w której zasób został zarezerwowany ponad jego dyspozycyjność.

