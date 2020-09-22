---
title: Postępu projektu i poniesione koszty
description: W tym temat zamieszczono informacje dotyczące śledzenia postępu i zużycia kosztów w programie project.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754384"
---
# <a name="project-progress-and-cost-consumption"></a>Postępu projektu i poniesione koszty

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Konieczność śledzenia postępu w harmonogramie zależy od branży. Niektóre branże są śledzone na niższym poziomie szczegółowości, podczas gdy inne branże śledzone są na wyższym poziomie. W tym temat pokazano, jak planować w celu spełnienia wymagań organizacji.

## <a name="effort-tracking-view"></a>Widok Śledzenie nakładu pracy

W widoku **Śledzenie nakładu pracy** są śledzone postępy zadań w harmonogramie. Porównuje rzeczywisty nakład godzin pracy spędzonych nad zadaniem z planowanym nakładem pracy w godzinach dla zadania. Korzystając z poniższych formuł, program PSA obliczy metryki śledzenia:

- Procent postęp = rzeczywisty nakład pracy do dnia dzisiejszego ÷ planowany nakład pracy dla zadania 
- Szacowane do zakończenia (ETC) = planowany nakład pracy — rzeczywisty nakład pracy do dnia dzisiejszego 
- Szacowane przy zakończeniu (SPZ) = pozostały nakład pracy + rzeczywisty nakład pracy do dnia dzisiejszego 
- Przewidywane odchylenie nakładu pracy = planowany nakład pracy — SPZ

W programie PSA jest wyświetlona projekcja odchylenia danego zadania. Jeśli wartość SPZ przekracza planowany nakład pracy, zadanie jest rzutowane na czas dłuższy niż planowano. Z tego powodu nie mieści się w harmonogramie. Jeśli wartość SPZ jest mniejsza niż planowany nakład pracy, zadanie jest rzutowane na czas krótszy niż planowano. Z tego powodu zadanie wyprzedza harmonogram.

## <a name="re-projecting-effort"></a>Ponowne prognozowanie nakładu pracy

Menedżerowie projektu często rewidują oryginalne wartości szacunkowe zadania. Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu. Niemniej n ie zalecamy, aby menedżerowie projektu zmieniali liczby podstawowe, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.

Istnieją dwa sposoby ponownego prognozowania nakładu pracy na zadania:

- Zastąpienie domyślnej wartości ETC nową wartością szacunkową rzeczywistego pozostałego nakładu pracy na zadanie. 
- Zastąpienie domyślnej wartości procentowej postępu nową wartością rzeczywistego postępu.

Każda z tych metod powoduje ponowne obliczenie wartości ETC zadania, SPZ i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem. Wartości SPZ, ETC i procent postępu w zadaniach sumarycznych są również obliczane ponownie i dają nową projekcję odchylenia.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Ponowna projekcja nakładów na zadania sumaryczne

Nakład pracy na zadania sumaryczne lub zadania kontenera można zaprojektować ponownie. Bez względu na to, czy użytkownik ponownie pracuje nad projektami przy użyciu pozostałego nakładu lub procentu postępu w zadaniach sumarycznych, zaczyna się następujący zestaw obliczeń:

- Wartości SPZ, ETC i procent postępu są obliczane względem zadania.
- Nowe wartości SPZ są rozkładane w dół na zadania podrzędne w takiej samej proporcji jak w oryginalnym elemencie SPZ w ramach danego zadania.
- Obliczana jest nowa wartość SPZ w każdym z zadań w dół względem poszczególnych węzłów typu liść. 
- Następuje ponowne przeliczenie ETC i procenta postępu zadań podrzędnych do węzła liścia na podstawie wartości SPZ. W wyniku tego powstaje nowa projekcja odchylenia nakładu pracy nad zadaniem. 
- System ponownie oblicza EAC zadań sumarycznych na całej drodze do węzła głównego.

### <a name="cost-tracking-view"></a>Widok śledzenia kosztów 

W widoku **śledzenia kosztów** jest porównywany koszt rzeczywisty, który został wydany na wykonanie zadania według planowanego kosztu. 

> [!NOTE]
> W tym widoku są wyświetlane tylko koszty robocizny i nie są uwzględniane koszty szacunków kosztów. 

Korzystając z poniższych formuł, program PSA obliczy metryki śledzenia:

- Procent zużytego kosztu = koszt rzeczywisty poniesiony do dnia ÷ planowany koszt zadania
- Koszt do zakończenia (CTC) = planowany koszt — rzeczywisty koszt poniesiony do dnia
- SPZ = CTC + koszt rzeczywisty poniesiony do dnia
- Prognozowane odchylenie kosztu = koszt planowany – SPZ

Prognoza odchylenia kosztu jest widoczna w zadaniu. Jeśli wartość SPZ przekracza planowany koszt, zadaniu jest przypisywany koszt wyższy niż planowano na początku. Z tego powodu ma ono tendencję do przekroczenia budżetu. Jeśli wartość SPZ jest mniejsza od planowanego kosztu, zadaniu jest przypisywany koszt niższy niż planowano na początku. Z tego powodu ma ono tendencję do niewykorzystania budżetu.

## <a name="project-managers-re-projection-of-cost"></a>Ponowne prognozowanie kosztów przez menedżera projektu

W przypadku ponownego prognozowanego nakładu pracy CTC, SPZ, procent zużytego kosztu i przewidywane odchylenie kosztów są ponownie obliczane w widoku **śledzenia kosztów**.

## <a name="project-status-summary"></a>Podsumowanie statusu projektu

Śledzenie danych w widokach **śledzenie nakładu pracy** i **śledzenie kosztów** wskazuje postępy i zużycie kosztów na poziomach zadań w głównym węźle projektu, zadania sumaryczne i węzły liścia. Sekcja **stan** na stronie **encja projektu** zawiera podsumowanie stanu na poziomie projektu.

## <a name="status-summary-fields"></a>Pola podsumowania stanu

Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu. Używa kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko. Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu. Pole **Stan zaktualizowany w dniu** nie jest edytowalne, a wartość jest sygnaturą czasową wskazującą datę ostatniej aktualizacji stanu.

Pola **wydajność planowania** i **wydajność kosztów** są ustawiane na podstawie daty śledzenia. Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, można ustawić te pola na**mieści się**. Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne, można ustawić je na wartość **nie mieści się**.
