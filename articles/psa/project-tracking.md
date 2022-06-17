---
title: Postęp projektu i poniesione koszty
description: W tym artykule zamieszczono informacje dotyczące śledzenia postępu projektu i zużycia kosztów.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: afcac5e6fbb7ed8a5a5f7f5876c6035b59eebcc2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921775"
---
# <a name="project-progress-and-cost-consumption"></a>Postęp projektu i poniesione koszty

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Konieczność śledzenia postępu w harmonogramie zależy od branży. Niektóre branże są śledzone na niższym poziomie szczegółowości, podczas gdy inne branże śledzone są na wyższym poziomie. W tym artykule pokazano, jak planować w celu spełnienia wymagań organizacji.

## <a name="effort-tracking-view"></a>Widok Śledzenie nakładu pracy

W widoku **Śledzenie nakładu pracy** są śledzone postępy zadań w harmonogramie. Porównuje rzeczywistą liczbę godzin pracy poświęconą na zadanie z zaplanowanymi godzinami nakładu pracy. Project Service Automation korzysta z poniższych formuł do obliczania metryk śledzenia:

Początkowo w tworzeniu zadania: koszt planowany zostanie ustawiony na szacowany koszt podczas zakończenia. Po zarejestrowaniu wartości rzeczywistych dla zadania w widoku śledzenia będą wykonywane obliczenia dotyczące nakładów pracy

- Procent postępu = rzeczywisty nakład pracy do dnia dzisiejszego ÷ szacowane przy zakończeniu (SPZ) 
- Szacowana wartość końcowa (ETC) = szacowane przy zakończeniu (SPZ) – rzeczywisty nakład pracy wyświęconej na tę datę 
- SPZ = pozostały nakład pracy + rzeczywisty nakład pracy do dnia dzisiejszego 
- Przewidywane odchylenie nakładu pracy = planowany nakład pracy — SPZ

W programie Project Service Automation jest wyświetlona projekcja odchylenia danego zadania. Jeśli wartość SPZ przekracza planowany nakład pracy, zadanie jest rzutowane na czas dłuższy niż planowano. Z tego powodu nie mieści się w harmonogramie. Jeśli wartość SPZ jest mniejsza niż planowany nakład pracy, zadanie jest rzutowane na czas krótszy niż planowano. Z tego powodu zadanie wyprzedza harmonogram.

## <a name="reprojecting-effort"></a>Ponowne prognozowanie nakładu pracy

Menedżerowie projektu często rewidują oryginalne wartości szacunkowe zadania. Ponowne prognozy to oszacowania menedżera projektu z uwzględnieniem bieżącego stanu projektu. Niemniej n ie zalecamy, aby menedżerowie projektu zmieniali liczby podstawowe, ponieważ podstawa projektu reprezentuje ustalone źródło prawdziwych wartości dla harmonogramu i szacunkowego kosztu projektu, na które wyrazili zgodę wszyscy udziałowcy.

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
> W tym widoku są wyświetlane tylko koszty robocizny i nie są uwzględniane koszty szacunków kosztów. 

Project Service Automation korzysta z poniższych formuł do obliczania metryk śledzenia:

Po utworzeniu zadania planowany koszt jest równa kosztowi szacowanemu przy zakończeniu. Po zarejestrowaniu wartości rzeczywistych dla zadania w widoku **śledzenia** będą wykonywane obliczenia dotyczące kosztów:

 - Procent zużytego kosztu = koszt rzeczywisty poniesiony do dnia ÷ szacowany koszt przy zakończeniu dla zadania
 - Koszt do zakończenia (CTC) = szacowany koszt przy zakończeniu – rzeczywisty koszt poniesiony do bieżącej daty
 - Szacowany koszt przy zakończeniu = CTC + rzeczywisty koszt poniesiony do bieżącej daty
 - Odchylenie kosztu prognozowanego = koszt planowany – szacowany koszt przy zakończeniu

Prognoza odchylenia kosztu jest widoczna w zadaniu. Jeśli wartość szacowany koszt przy zakończeniu przekracza planowany koszt, zadaniu jest przypisywany koszt wyższy niż planowano na początku. Z tego powodu ma ono tendencję do przekroczenia budżetu. Jeśli szacowany koszt przy zakończeniu jest mniejszy niż planowany koszt, zadaniu jest przypisywany koszt niższy niż planowano i który jest popularny według budżetu.

## <a name="project-managers-reprojection-of-cost"></a>Ponowne prognozowanie kosztów przez menedżera projektu

W przypadku przewidywanego nakładu pracy CTC, szacowany koszt przy zakończeniu, procent zużytego kosztu i przewidywane odchylenie kosztów są ponownie obliczane w widoku **śledzenia kosztów**.

## <a name="project-status-summary"></a>Podsumowanie statusu projektu

Śledzenie danych w widokach **śledzenie nakładu pracy** i **śledzenie kosztów** wskazuje postępy i zużycie kosztów na poziomach zadań w głównym węźle projektu, zadania sumaryczne i węzły liścia. Sekcja **stan** na stronie **encja projektu** zawiera podsumowanie stanu na poziomie projektu.

## <a name="status-summary-fields"></a>Pola podsumowania stanu

Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu. Używa kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko. Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu. Pole **Stan zaktualizowany w dniu** nie jest edytowalne, a wartość jest sygnaturą czasową wskazującą datę ostatniej aktualizacji stanu.

Pola **wydajność planowania** i **wydajność kosztów** są ustawiane na podstawie daty śledzenia. Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, można ustawić te pola na **mieści się**. Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne, można ustawić je na wartość **nie mieści się**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
