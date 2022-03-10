---
title: Omówienie uzgadniania zasobów
description: Ten temat zawiera informacje, które pomogą Ci upewnić się, że rezerwacje zasobów i przydziały dla projektów są wyrównane.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1542e97955902486d22ca637514e4e121fae70e2b227cafc7020c031061b5f98
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994784"
---
# <a name="resource-reconciliation-overview"></a>Omówienie uzgadniania zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Członkowie zespołu, rezerwacje i przydziały są luźno sprzężone. Innymi słowy, zasoby mogą mieć przydziały i mogą nie mieć rezerwacji lub mogą mieć rezerwacje bez przypisań. Najlepiej, kiedy rezerwacje i przypisania w projekcie są zgodne, bo wtedy zasoby mają zatwierdzoną dyspozycyjność do wykonania przypisanych im zadań. Jednak rezerwacje mogą być oparte na dostępności, a czasy zadań mogą ulec zmianie w miarę kontynuowania projektu. Z tego względu swobodne powiązanie rezerwacji i przypisań zapewnia elastyczność.

Karta **Uzgadnianie** na stronie **Projekty** pozwala menedżerom projektu uzgadniać rezerwacje członków zespołu i ich przypisania w zespołach projektów.

Na karcie **Uzgadnianie** są wyświetlane rezerwacje i przypisania na wszystkich poziomach szczegółowości, aż do poszczególnych zadań. Godziny są wyświetlane w komórkach, które reprezentują okresy od miesięcy do dni. Na karcie przedstawiono również ogólną sumę netto projektu wraz z kolumną **Suma**.

Dla każdego zasobu karta **Uzgadnianie** oblicza różnicę między rezerwacjami członka zespołu w projekcie a zestawieniem zadań przypisanych temu członkowi zespołu. Najlepiej, aby różnica wynosiła 0 (zero). Innymi słowy nie powinno być żadnej różnicy między rezerwacjami zasobu a jego przypisaniami zadań. Różnice są oznaczone kolorami i zacienione, aby zwrócić uwagę na dwa warunki:

- **Niedobór rezerwacji** — niedobory rezerwacji powstają wtedy, gdy zasób ma więcej przypisań, niż rezerwacji. Ponieważ dyspozycyjność nie została zarezerwowana, menedżer projektu może naprawić tę sytuację poprzez rozszerzenie rezerwacji zasobu w sposób pokrywający niedobór.
- **Nadmiarowe rezerwacje** — nadmierne rezerwacje występują, gdy zasób zarezerwowano do projektu, ale nie przypisano go do zadań. Ten warunek może być akceptowalny w przypadkach, gdy zasób został zarezerwowany w projekcie przed przydziałem zadania. Jednak w innych przypadkach, gdy nie ma planu przypisania zasobu do zadań, menedżer projektu powinien rozważyć anulowanie rezerwacji zasobu. W ten sposób pojemność można wykorzystać na inny projekt.

W niektórych przypadkach, kiedy oglądasz czas na wyższym poziomie niż poziom dnia (np. na poziomie miesiąca), może się pojawić różnica netto zasobu równa zero (innymi słowy, rezerwacje równają się przydziałom). Natomiast w poziomie Tydzień można zauważyć, że istnieją przypisania równe 0 (zero) godzin i rezerwacje 40 godzin w pierwszym tygodniu miesiąca oraz przypisania 40 godzin i rezerwacje równe 0 (zero) godzin w drugim tygodniu miesiąca. Ogólnie rzecz biorąc, rezerwacje i przydziały są uzgadniane, ale różnią się od siebie między tygodniami.

Po wyświetleniu wyższych poziomów czasu na karcie **Uzgadnianie** widać wskaźnik komórki informujący o różnicach na niższych poziomach czasu. Dwukrotne dotknięcie lub kliknięcie komórki umożliwia powiększenie i wyświetlenie różnicy. Następnie możesz wybrać i przytrzymać (lub kliknąć prawym przyciskiem myszy), aby pomniejszyć. Zaznaczając zasób, a następnie korzystając z przycisku **Następna różnica** z paska narzędzi siatki można przejść do następnej różnicy między rezerwacjami a przydziałami danego zasobu. Następnie można skorzystać z opcji **Poprzednia różnica**, aby wrócić. Istnieje również możliwość wyłączenia wskaźnika różnic i zachowania nawigacji w obszarze **ustawienia.**

W sytuacjach, gdy istnieją przypisania zadań dla zasobu, ale nie ma rezerwacji, wybierz niedobór rezerwacji na karcie **Uzgadnianie** na stronie **Projekty** można wybrać niedobór rezerwacji, a następnie kliknąć przycisk **Rozszerz rezerwację**. Zostanie wyświetlone okno dialogowe **Rozszerz rezerwację**, w którym przedstawiono rezerwację potrzebną do wyeliminowania problemu niedoboru zasobu. To okno dialogowe pokazuje również istniejące rezerwacje zasobu we wszystkich projektach lub innych encjach zaplanowania. W przypadku wybrania opcji **OK**, aby utworzyć rezerwację zasobu niezależnie od dostępności tego zasobu, może wystąpić rezerwacja ponad dyspozycyjność.

Rezerwacje tworzone w ramach akcji **Rozszerzanie rezerwacji** są związane z podstawowymi wymaganiami projektu. Po zainicjowaniu rozszerzenia nie można określić konkretnego wymagania, które musi zostać rozszerzone, ponieważ zasób może być powiązany z więcej niż jednym wymaganiem projektu.

Następnie menedżer projektu lub menedżer zasobów może za pomocą tablicy harmonogramu rozwiązać sytuację, w której zasób został zarezerwowany ponad jego dyspozycyjność.


[!INCLUDE[footer-include](../includes/footer-banner.md)]