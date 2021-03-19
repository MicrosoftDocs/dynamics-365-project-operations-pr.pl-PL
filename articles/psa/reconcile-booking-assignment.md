---
title: Uzgadnianie rezerwacji i przypisań
description: Ten temat zawiera informacje o wartościach rzeczywistych.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 30af3cca9b4c3dc3f1a9412de7380c963bde88f0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283426"
---
# <a name="reconcile-bookings-and-assignments"></a>Uzgadnianie rezerwacji i przypisań

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rezerwacje w projekcie i przypisania zadań projektu dla członka zespołu projektu są z sobą luźno powiązane. W efekcie zasób może mieć przypisania zadań, które nie odpowiadają rezerwacjom, oraz rezerwacje, które nie odpowiadają przypisaniom zadań. Najlepiej, kiedy rezerwacje i przypisania w projekcie są zgodne, bo wtedy zasoby mają zatwierdzoną dyspozycyjność do wykonania przypisanych im zadań. Jednak w rzeczywistość rezerwacje są często dokonywane na podstawie dostępności, a czasy wykonywania zadań mogą ulegać zmianie wraz z postępami projektu. Luźne powiązanie umożliwia elastyczność potrzebną w takich sytuacjach.

Ze względu na luźne powiązanie między rezerwacjami w projektach i przypisaniami zadań encja Projekt zawiera kartę **Uzgadnianie**. Na tej karcie menedżerowie projektów mogą uzgadniać rezerwacje członków zespołu oraz ich przypisania do zespołu projektu.

Dla każdego nazwanego członka zespołu na karcie **Uzgadnianie** są wyświetlane rezerwacje i przypisania na wszystkich poziomach szczegółowości, aż do poszczególnych zadań. W komórkach widać godziny, które mogą reprezentować okresy od miesięcy aż po dni.

W polu **Skala czasu** można wybrać wartość **Miesiąc**, **Tydzień** lub **Dzień**. Domyślnie jest zaznaczony okres **Tydzień**. Można jednak zmienić tę wartość domyślną, naciskając przycisk **Ustawienia**. Po otwarciu karty **Uzgadnianie** jest na niej wyświetlana bieżąca data, ale za pomocą kontrolki kalendarza można przejść do przodu lub do tyłu w czasie. Kiedy projekt ma datę rozpoczęcia przypadającą w przyszłości, po otwarciu karty będzie na niej wyświetlana ta data. Kontrolka kalendarza zawiera też opcje umożliwiające przechodzenie do dat rozpoczęcia i zakończenia projektu.

Za pomocą kontrolek rozwinięcia przy każdym zasobie można wyświetlić szczegółowe informacje o rezerwacjach danego zasobu. Można również rozwinąć przypisania każdego zasobu aż do poziomu szczegółowości konkretnych zadań.

U dołu karty **Uzgadnianie** jest wyświetlana łączna suma netto projektu, a karta zawiera również kolumnę sumy. Dla każdego zasobu karta oblicza różnicę między rezerwacjami członka zespołu w projekcie a zestawieniem zadań przypisanych temu członkowi zespołu. Najlepiej, aby różnica wynosiła 0 (zero). Innymi słowy nie powinno być żadnej różnicy między rezerwacjami zasobu a jego przypisaniami zadań. Wszelkie różnice są oznaczane kolorami i cieniowaniem w celu zasygnalizowania dwóch sytuacji:

- **Niedobór rezerwacji** — niedobory rezerwacji powstają wtedy, gdy zasób ma więcej przypisań, niż rezerwacji. Ponieważ dyspozycyjność nie została zarezerwowana, menedżer projektu może naprawić tę sytuację poprzez rozszerzenie rezerwacji zasobu w sposób pokrywający niedobór.
- **Nadmiarowe rezerwacje** — nadmierne rezerwacje występują, gdy zasób zarezerwowano do projektu, ale nie przypisano go do zadań. Ta sytuacja może być akceptowalna, jeśli na przykład zasób zarezerwowano przed przypisaniem zadań. Jednak w innych przypadkach być może nie jest planowane przypisanie zasobu. Wtedy menedżer projektu powinien rozważyć anulowanie rezerwacji zasobu, tak aby jego dyspozycyjność można było wykorzystać w innym projekcie.

> [!NOTE]
> Legenda tych sytuacji może być ukryta, aby zostawić więcej miejsca na siatkę. Jeżeli tak jest, w celu wyświetlenia legendy należy kliknąć przycisk **Ustawienia**.

W niektórych przypadkach gdy w polu **Skala czasu** jest ustawiony poziom wyższy niż **Dzień**, różnice mogą być obliczane jako 0 (zero). Na przykład na poziomie **Miesiąc** różnica netto zasobu może wynosić 0 (zero) w celu wskazania, że rezerwacje są równe przypisaniom. Natomiast w poziomie **Tydzień** można zauważyć, że istnieją przypisania równe 0 (zero) godzin i rezerwacje 40 godzin w pierwszym tygodniu miesiąca oraz przypisania 40 godzin i rezerwacje równe 0 (zero) godzin w drugim tygodniu miesiąca. Mimo że łączne rezerwacje i przypisania w miesiącu są równe, różnią się w zależności od tygodnia.

Po wyświetleniu wyższych poziomów czasu na karcie **Uzgadnianie** widać wskaźnik komórki informujący o różnicach na niższych poziomach czasu. Na przykład na ilustracji poniżej w komórce jest wyświetlany wskaźnik dla miesiąca Październik 2018 dla zasobu o nazwie Kaja Lewandowska. Dlatego mimo iż rezerwacje i przypisania zasobu są równe po zagregowaniu na poziomie **Miesiąc**, nie pasują do siebie na niższych poziomach.

![Niedopasowania zaksięgowań i przydziałów na poziomie miesięcznym](media/reconcile-assignments-01.JPG)

Kliknij dwukrotnie komórkę, aby przybliżyć następny niższy poziom i zobaczyć różnicę. Na przykład dwukrotne kliknięcie różnicy w miesiącu Październik 2018 dla Kai Lewandowskiej spowoduje przejście do bardziej szczegółowego poziomu **Tydzień**. Wtedy widać, że w pierwszych dwóch tygodniach października zasób ma rezerwacje na 16 godzin, ale żadnych przypisań, natomiast w trzecim tygodniu października ma 16 godzin przypisań, ale żadnych rezerwacji.

![Niedopasowania zaksięgowań i przydziałów na poziomie tygodniowym](media/reconcile-assignments-02.JPG)

Można kliknąć komórkę prawym przyciskiem myszy, aby oddalić widok do następnego wyższego poziomu. Można również wyłączyć wskaźnik komórki, klikając przycisk **Ustawienia**. 

Za pomocą przycisków **Wstecz** i **Dalej** umieszczonych nad siatką można przechodzić między wszelkimi różnicami w projekcie. Aby użyć tych przycisków, należy najpierw zaznaczyć zasób. Kliknij przycisk **Dalej**, aby przejść do następnej różnicy między rezerwacjami a przypisaniami dla wybranego zasobu. Kliknij przycisk **Wstecz**, aby przejść do poprzedniej różnicy.

W sytuacjach, gdy istnieją przypisania zadań dla zasobu, ale nie ma rezerwacji, można wybrać niedobór rezerwacji, a następnie kliknąć przycisk **Rozszerz rezerwację**. Zostanie wtedy wyświetlona rezerwacja, której trzeba dokonać w celu rozwiązania problemu z niedoborem zasobu. Można również wyświetlać rezerwacje zasobów w bieżącym projekcie i innych projektach. Kliknij przycisk **OK**, aby utworzyć rezerwację zasobu bez względu na jego aktualną dostępność. Następnie menedżer projektu lub menedżer zasobów może za pomocą tablicy harmonogramu rozwiązać sytuację, w której zasób został zarezerwowany ponad jego dyspozycyjność wskutek rozszerzenia rezerwacji.

## <a name="managing-with-time-zones"></a>Zarządzanie ze strefami czasowymi
Aby zapewnić dokładne i przewidywalne wyniki podczas stosowania opcji Rozszerz rezerwację, należy spełnić dwa podstawowe wymagania wstępne:  

- Użytkownik musi skonfigurować strefę czasową swojego urządzenia, aby odpowiadała strefom czasowym określonym w ustawieniach personalizacji systemu.
 
  ![Ustawienia strefy czasowej w systemie Windows 10](media/reconcile-assignments-03.png)

  ![Ustawienia strefy czasowej w ustawieniach personalizacji](media/reconcile-assignments-04.png)
 
- Zasób obsługujący rezerwacje musi mieć co najmniej jedną minutę czasu pracy, który pokrywa się z rozkładem używanym do definiowania żądanego rozszerzenia. Na przykład w poniższym przykładzie przedstawiono przegląd zasobów z godzinami pracy wypadających między 9:00 i 19:00. 

  ![Porównanie rozkładów zasobów](media/reconcile-assignments-05.png)

W poniższej tabeli przedstawiono:

- Szablon kalendarza projektu.
- Zasób A: ten zasób ma ten sam kalendarz i znajduje się w tej samej strefie czasowej, co projekt. Godziną rozpoczęcia rezerwacji będzie 9:00.
- Zasób B: ten zasób znajduje się w innej strefie czasowej niż projekt i dlatego zaczyna się o godzinie 7:00 w swojej strefie czasowej. Jednak rezerwacje zaczynają się od godziny 9:00, która jest najwcześniejszym czasem rozpoczęcia rozkładu przydziału.
- Zasoby C i D: zasoby są również zlokalizowane w różnych strefach czasowych, różnią się między sobą i projektem, a ich rezerwacje zaczynają nie wcześniej niż ich odpowiednio dostępne godziny rozpoczęcia.

|Encja  |Kalendarz  |
|-|-|
|Szablon kalendarza projektu   | ![kalendarz projektu](media/reconcile-assignments-06.png) |
|Zasób A  | ![Kalendarz zasobu A](media/reconcile-assignments-06.png) |
|Zasób B  |  ![Kalendarz zasobu B](media/reconcile-assignments-07.png) |
|Zasób C  |  ![Kalendarz zasobu C](media/reconcile-assignments-08.png) |
|Zasób D  | ![Kalendarz zasobu D](media/reconcile-assignments-09.png)  |
 
Po przejściu do widoku uzgodnienie zostaną wyświetlone przydziały zasobów i skojarzone niedobory rezerwacji.
 ![Uzgadnianie widoku przed rozszerzeniem](media/reconcile-assignments-10.png)

Po wykonaniu na każdym z zasobów funkcji Rozszerz rezerwację rezerwacje dla każdego zasobu są pomyślnie rozszerzane. Wynika to z faktu, że godziny pracy poszczególnych zasobów pokrywają się z rozkładem niedoboru.
 ![Widok Uzgodnienie po rozszerzeniu rezerwacji](media/reconcile-assignments-11.png) 

Ściślejsze zapoznanie się z szczegółowymi informacjami dotyczącymi rezerwacji pokazuje różnice w czasie rozpoczęcia rezerwacji. Rezerwacje będą zaczynać się nie wcześniej, niż godzina rozpoczęcia rozkładu przydziału i nie wcześniej, niż jest dostępna godzina rozpoczęcia danego zasobu.
 ![Nowe rezerwacje zasobów na tablicy harmonogramu](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]