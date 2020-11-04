---
title: Omówienie śledzenia projektu
description: W tym temat zamieszczono informacje dotyczące śledzenia postępu i zużycia kosztów w programie project.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081863"
---
# <a name="project-tracking-overview"></a>Omówienie śledzenia projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Konieczność śledzenia postępu w harmonogramie zależy od branży. Niektóre branże są śledzone na niższym poziomie szczegółowości, podczas gdy inne branże śledzone są na wyższym poziomie. W tym temat pokazano, jak planować w celu spełnienia wymagań organizacji.

## <a name="effort-tracking-view"></a>Widok Śledzenie nakładu pracy

W widoku **Śledzenia nakładów** są śledzone postępy zadań w harmonogramie. Polega to na porównaniu rzeczywistych nakładów pracy na zadanie z planowanymi godziny nakładu pracy danego zadania. Dynamics 365 Project Operations korzysta z poniższych formuł do obliczania metryk śledzenia:

- **Procent postępu** : rzeczywisty nakład pracy do dnia dzisiejszego ÷ szacowane przy zakończeniu (SPZ) 
- **Szacowane do zakończenia (ETC)** : planowany nakład pracy — rzeczywisty nakład pracy do dnia dzisiejszego 
- **SPZ** : pozostały nakład pracy + rzeczywisty nakład pracy do dnia dzisiejszego 
- **Przewidywane odchylenie nakładu pracy** : planowany nakład pracy — SPZ

W programie Project Operations jest wyświetlona projekcja odchylenia danego zadania. Jeśli wartość SPZ przekracza planowany nakład pracy, zadanie jest rzutowane na czas dłuższy niż planowano i jest opóźnienie. Jeśli wartość SPZ jest mniejsza niż planowany nakład pracy, zadanie jest rzutowane na czas krótszy niż planowano i praca posuwa się do przodu szybciej niż zaplanowano.

## <a name="reprojecting-effort"></a>Ponowne prognozowanie nakładu pracy

Menedżerowie projektu czasem rewidują oryginalne wartości szacunkowe zadania. Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu. Nie zaleca się jednak, aby menedżerowie projektów zmieniali liczby w planie bazowym. Dzieje się tak, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.

Istnieją dwa sposoby ponownego prognozowania nakładu pracy na zadania:

- Zastąpienie domyślnej wartości ETC nową wartością szacunkową rzeczywistego pozostałego nakładu pracy na zadanie. 
- Zastąpienie domyślnej wartości procentowej postępu nową wartością rzeczywistego postępu.

Każda z tych metod powoduje ponowne obliczenie wartości ETC zadania, SPZ i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem. Wartości SPZ, ETC i procent postępu w zadaniach sumarycznych są również obliczane ponownie i dają nową projekcję odchylenia.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ponowna projekcja nakładów na zadania sumaryczne

Nakład pracy na zadania sumaryczne lub zadania kontenera można zaprojektować ponownie. Bez względu na to, czy użytkownik ponownie pracuje nad projektami przy użyciu pozostałego nakładu lub procentu postępu w zadaniach sumarycznych, zaczyna się następujący zestaw obliczeń:

- Wartości SPZ, ETC i procent postępu są obliczane względem zadania.
- Nowe wartości SPZ są rozkładane w dół na zadania podrzędne w takiej samej proporcji jak w oryginalnym elemencie SPZ w ramach danego zadania.
- Obliczana jest nowa wartość SPZ w każdym z zadań w dół względem poszczególnych węzłów typu liść. 
- Następuje ponowne przeliczenie ETC i procenta postępu zadań podrzędnych do węzła liścia na podstawie wartości SPZ. W wyniku tego powstaje nowa projekcja odchylenia nakładu pracy nad zadaniem. 
- System ponownie oblicza EAC zadań sumarycznych na całej drodze do węzła głównego.

### <a name="cost-tracking-view"></a>Widok śledzenia kosztów 

W widoku **śledzenia kosztów** jest porównywany koszt rzeczywisty, który został wydany na wykonanie zadania według planowanego kosztu. 

> [!NOTE]
> W tym widoku są wyświetlane tylko koszty robocizny i nie są uwzględniane koszty szacunków kosztów. Project Operations korzysta z poniższych formuł do obliczania metryk śledzenia:

- **Procent zużytego kosztu** : koszt rzeczywisty poniesiony do dnia ÷ szacowany koszt przy zakończeniu
- **Koszt do zakończenia (CTC)** : planowany koszt — rzeczywisty koszt poniesiony do dnia
- **EAC** : pozostały koszt + rzeczywisty koszt poniesiony do tej pory
- **Prognozowane odchylenie kosztu** : koszt planowany – SPZ

Prognoza odchylenia kosztu jest widoczna w zadaniu. Jeśli wartość SPZ przekracza planowany koszt, zadaniu jest przypisywany koszt wyższy niż planowano na początku. Z tego powodu ma ono tendencję do przekroczenia budżetu. Jeśli wartość SPZ jest mniejsza od planowanego kosztu, zadaniu jest przypisywany koszt niższy niż planowano na początku. Z tego powodu ma ono tendencję do niewykorzystania budżetu.

## <a name="project-managers-reprojection-of-cost"></a>Ponowne prognozowanie kosztów przez menedżera projektu

W przypadku ponownie prognozowanego nakładu pracy CTC, SPZ, procent zużytego kosztu i przewidywane odchylenie kosztów są ponownie obliczane w widoku **śledzenia kosztów**.

## <a name="project-status-summary"></a>Podsumowanie statusu projektu

Śledzenie danych w widokach **śledzenie nakładu pracy** i **śledzenie kosztów** wskazuje postępy i zużycie kosztów na poziomach zadań w głównym węźle projektu, zadania sumaryczne i węzły liścia. Sekcja **stan** na stronie **encja projektu** zawiera podsumowanie stanu na poziomie projektu.

## <a name="status-summary-fields"></a>Pola podsumowania stanu

Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu. Używa kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko. Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu. Pole **Stan zaktualizowany w dniu** nie jest edytowalne, a wartość jest sygnaturą czasową wskazującą datę ostatniej aktualizacji stanu.

Pola **wydajność planowania** i **wydajność kosztów** są ustawiane na podstawie daty śledzenia. Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, można ustawić te pola na **mieści się**. Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne, można ustawić je na wartość **nie mieści się**.
