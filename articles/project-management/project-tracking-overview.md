---
title: Śledzenie nakładu pracy projektu
description: Ten temat zawiera informacje dotyczące śledzenia nakładu pracy i postępu pracy w ramach projektu.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 037118714cf01ba2fb91cdd94345495d12ccb645
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593809"
---
# <a name="project-effort-tracking"></a>Śledzenie nakładu pracy projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Konieczność śledzenia postępu w harmonogramie zależy od branży. Niektóre branże są śledzone na niższym poziomie szczegółowości, podczas gdy inne branże śledzone są na wyższym poziomie. W tym temat pokazano, jak planować w celu spełnienia wymagań organizacji.

## <a name="effort-tracking-view"></a>Widok Śledzenie nakładu pracy

W widoku **Śledzenia nakładów** są śledzone postępy zadań w harmonogramie. Polega to na porównaniu rzeczywistych nakładów pracy na zadanie z planowanymi godziny nakładu pracy danego zadania. Rozwiązanie Dynamics 365 Project Operations korzysta z poniższych formuł do obliczania metryk śledzenia:

- **Procent postępu**: rzeczywisty nakład pracy do dnia dzisiejszego ÷ szacowane przy zakończeniu (SPZ) 
- **Pozostały nakład pracy**: Szacowany wysiłek po zakończeniu - rzeczywisty wysiłek wydany do tej pory 
- **SPZ**: pozostały nakład pracy + rzeczywisty nakład pracy do dnia dzisiejszego 
- **Przewidywane odchylenie nakładu pracy**: planowany nakład pracy — SPZ

W programie Project Operations jest wyświetlona projekcja odchylenia danego zadania. Jeśli wartość SPZ przekracza planowany nakład pracy, zadanie jest rzutowane na czas dłuższy niż planowano i jest opóźnienie. Jeśli wartość SPZ jest mniejsza niż planowany nakład pracy, zadanie jest rzutowane na czas krótszy niż planowano i praca posuwa się do przodu szybciej niż zaplanowano.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Ponowne projektunie nakładu pracy w zadaniach węźle liścia

Menedżerowie projektu czasem rewidują oryginalne wartości szacunkowe zadania. Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu. Nie zalecamy jednak, aby kierownicy projektów zmieniali planowane liczby nakładów. Dzieje się tak, ponieważ planowane wysiłki w ramach projektu stanowią ustalone źródło prawdziwości harmonogramu projektu i szacunku kosztów, a wszyscy interesariusze projektu wyrazili na to zgodę.

Menedżer projektu może ponownie zaplanować nakłady pracy na zadaniach, aktualizując domyślny **Pozostały nakład pracy** o nowe oszacowanie zadania. Ta aktualizacja powoduje ponowne obliczenie oszacowania zadania przy ukończeniu (SPZ), procentu postępu i przewidywanej wariancji nakładu pracy w zadaniu. Wartości SPZ, ETC i procent postępu w zadaniach sumarycznych są również obliczane ponownie i dają nową projekcję odchylenia.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ponowna projekcja nakładów na zadania sumaryczne

Nakład pracy na zadania sumaryczne lub zadania kontenera można zaprojektować ponownie. Menedżerowie projektów mogą aktualizować pozostałe nakłady pracy związane z zadaniami podsumowania. Aktualizacja pozostałego nakładu pracy powoduje wyzwolenie następującego zestawu obliczeń w aplikacji:

- Wartości SPZ i procent postępu są obliczane względem zadania.
- Nowe wartości SPZ są rozkładane w dół na zadania podrzędne w takiej samej proporcji jak w oryginalnym elemencie SPZ w ramach danego zadania.
- Obliczana jest nowa wartość SPZ w każdym z zadań w dół względem poszczególnych węzłów typu liść. 
- Zadania podrzędne, których dotyczy problem, aż do węzłów liści, pozostały wysiłek i procent postępu są ponownie obliczane na podstawie wartości SPZ. W wyniku tego powstaje nowa projekcja odchylenia nakładu pracy nad zadaniem. 
- System ponownie oblicza EAC zadań sumarycznych na całej drodze do węzła głównego.
- Zatwierdzony nakład pracy w zakresie zadania podsumowującego jest sumą zatwierdzonych działań dla wszystkich zadań podrzędnych oraz zatwierdzonym nakładem pracy w przypadku zadania podsumowującego.
- Pozostały nakład pracy na zadanie sumaryczne to suma pozostałego nakładu pracy na wszystkie zadania podrzędne minus zatwierdzony nakład pracy na zadanie sumaryczne.

## <a name="project-status-summary"></a>Podsumowanie statusu projektu

Śledzenie danych w widokach **śledzenie nakładu pracy** i **śledzenie kosztów** wskazuje postępy i zużycie kosztów na poziomach zadań w głównym węźle projektu, zadania sumaryczne i węzły liścia. Sekcja **stan** na stronie **encja projektu** zawiera podsumowanie stanu na poziomie projektu.

## <a name="status-summary-fields"></a>Pola podsumowania stanu

Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu. Używa kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko. Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu. Pole **Stan zaktualizowany w dniu** nie jest edytowalne, a wartość jest sygnaturą czasową wskazującą datę ostatniej aktualizacji stanu.

Pola **wydajność planowania** i **wydajność kosztów** są ustawiane na podstawie daty śledzenia. Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, można ustawić te pola na **mieści się**. Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne, można ustawić je na wartość **nie mieści się**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
