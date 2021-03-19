---
title: Harmonogramy projektów
description: W tym temacie zamieszczono informacje dotyczące tworzenia harmonogramu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 8f1a0b0ed610ade094546782a1fa517682a390e4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284010"
---
# <a name="project-schedules"></a>Harmonogramy projektów 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Harmonogram projektu komunikuje, co jest niezbędne do wykonania pracy, które zasoby będą za to odpowiedzialne, i w jakich ramach czasowych praca musi zostać zrealizowana. Harmonogram projektu odzwierciedla wszystkie prace związane z dostarczeniem projektu na czas. W Dynamics 365 Project Service Automation harmonogram projektu jest rozdzielany na zadania zarządzane, dzięki czemu można oceniać czas wymagany do wykonania każdego zadania, ustawiając zależności zadań, ustawiając czas trwania zadań i wykonując oszacowania zasobów ogólnych, które będą wykonywać te zadania. Harmonogram projektu jest tworzony na karcie **harmonogram** na stronie projektu.
 
## <a name="tasks"></a>Zadania

Pierwszym krokiem podczas tworzenia harmonogramu projektu jest przerwanie pracy w rozwiązaniu z zarządzanymi porcjami. W harmonogramie PSA są obsługiwane następujące funkcje:

- Węzeł główny projektu
- Zadania sumaryczne lub zadania typu kontener
- Zadania węzła liścia

### <a name="project-root-node"></a>Węzeł główny projektu

Główny węzeł projektu to zadanie sumaryczne najwyższego poziomu dotyczące projektu. Wszystkie inne zadania projektu są tworzone na jego podstawie. Nazwa głównego węzła jest zawsze nazwą projektu. Nakład pracy, daty i czas trwania węzła głównego są sumowane z wartości w hierarchii znajdującej się pod nim. Nie można edytować węzła głównego. Nie można również usunąć węzła głównego.

### <a name="summary-or-container-tasks"></a>Zadania sumaryczne lub zadania typu kontener 

Zadania sumaryczne zawierają zadania podrzędne lub zadania kontenera pod nimi. Nie mają własnych nakładów pracy ani kosztów. Zamiast tego ich nakład pracy i koszt stanowią zestawienie nakładu pracy i kosztu ich zadań kontenera. Data rozpoczęcia zadania sumarycznego to data rozpoczęcia zadań kontenera, a data końcowa to data zakończenia zadań kontenera. Nazwę zadania sumarycznego można edytować, ale nie można edytować właściwości jego planowania (nakład pracy, daty i czas trwania). Usunięcie zadania sumarycznego powoduje również usunięcie wszystkich jego zadań kontenera.

### <a name="leaf-node-tasks"></a>Zadania węzła liścia

Zadania węzła liścia reprezentują najbardziej szczegółowe prace związane z projektem. Mają szacunkowe nakłady pracy, zasoby, planowaną datę rozpoczęcia i zakończenia oraz czas trwania.
 
## <a name="creating-a-task-hierarchy"></a>Tworzenie hierarchii zadań

Można tworzyć hierarchię zadań przy użyciu następujących opcji:

- Przycisk **Dodaj zadanie**
- Przycisk **Wcięcie zadania**
- Przycisk **Anuluj wcięcie zadania**
- Przyciski **Przenieś w górę** i **Przenieś w dół**
- Skróty klawiaturowe i ułatwienia dostępu

### <a name="add-task"></a>Dodaj zadanie

Przycisk **Dodaj zadanie** umożliwia utworzenie nowego zadania w hierarchii. Jeśli nie wybierzesz miejsca, nowe zadanie zostanie wstawione na końcu. 

Do każdego zadania jest przypisywany identyfikator harmonogramu. Identyfikator harmonogramu reprezentuje głębokość i pozycję zadania w hierarchii. Korzysta z numerowania konspektu. W przypadku zadań znajdujących się na pierwszym poziomie w obszarze głównym węzła projektu jest używany schemat numerowania 1, 2, 3 itd. W przypadku zadań znajdujących się poniżej pierwszego poziomu jest używany schemat numerowania 1.1, 1.2, 1.3 itd.

### <a name="indent-task"></a>Wcięcie zadania

Kiedy zadanie jest wcięte, staje się podrzędne względem zadania, które znajduje się bezpośrednio nad nim. Identyfikator harmonogramu zadania jest następnie przeliczany w taki sposób, aby był oparty na identyfikatorze harmonogramu nowego obiektu nadrzędnego i podążał za schematem numerowania konspektu. Zadanie nadrzędne to teraz zadanie sumaryczne lub zadanie kontenera. Z tego powodu staje się zestawieniem jego zadań podrzędnych.

### <a name="outdent-task"></a>Zmniejsz wcięcie zadania 

W przypadku zmniejszenia wcięcia zadania nie jest już ono podrzędne względem zadania, które było dla niego nadrzędne. Identyfikator harmonogramu jest następnie przeliczany w taki sposób, aby odzwierciedlał zaktualizowane wcięcie i pozycję zadania w hierarchii. Nakłady pracy, koszty i daty poprzedniego zadania nadrzędnego są obliczane ponownie, tak aby nie obejmowały tego zadania.

### <a name="move-up-and-move-down"></a>Przenieś w górę i Przenieś w dół 

Przyciski **Przenieś w górę** i **Przenieś w dół** zmieniają pozycję zadania w hierarchii nadrzędnej. Zmiany tego typu nie wpływają na nakład pracy, koszty, daty lub czas trwania zadania. Mają wpływ tylko na identyfikator harmonogramu zadania. Identyfikator harmonogramu jest następnie przeliczany w taki sposób, aby odzwierciedlał nową pozycję zadania w nadrzędnej liście zadań.

### <a name="accessibility-and-keyboard-shortcuts"></a>Skróty klawiaturowe i ułatwienia dostępu

Siatka **harmonogramu** jest w pełni dostępna i może być używana z czytnikami ekranu, takimi jak Narrator, JAWS lub NVDA. Aby przechodzić między obszarem siatki za pomocą klawiszy strzałek (jak w Microsoft Excel), można użyć klawisza Tab w celu przechodzenia między elementami interaktywnego interfejsu użytkownika i można użyć klawisza strzałki w dół, klawisza Enter lub klawisza spacji w celu wybrania i przywołania menu rozwijanego. Nagłówki kolumn są również interaktywne. Istnieje możliwość ukrycia i wyświetlenia kolumn, użycia kluczy tabulacji i klawiszy strzałek w celu poruszania się po nagłówkach kolumn oraz używania przycisków akcji na pasku narzędzi. Oprócz tego można używać następujących skrótów klawiaturowych:

- **Odśwież**: Alt + Shift + F5
- **Dodaj**: Alt + Shift + Insert
- **Usuń**: Alt + Shift + Delete
- **Przenieś w górę/dół**: Alt + Shift + strzałki w górę i w dół
- **Wcięcie/wysunięcie**: ALT_SHIFT + strzałki w lewo i w prawo
- **Rozwiń/Zwiń hierarchie**: Alt + Shift + klawisze plus/minus

## <a name="task-attributes"></a>Atrybuty zadania

Nazwa zadania opisuje czynności, które należy wykonać. W usłudze PSA atrybuty skojarzone z zadaniem opisują harmonogram zadania i wymagania dotyczące jego personelu.

> ![Atrybuty zadania](media/project-2.png)
 
### <a name="schedule-attributes"></a>Zaplanuj atrybuty

Atrybuty **nakład pracy**, **Data rozpoczęcia**, **Data zakończenia** i **czas trwania** określają harmonogram zadania.

Dodatkowe atrybuty harmonogramu są następujące:

- **Godziny pracy**: należy wprowadzić wartość szacunkową godzin wymaganych do wykonania zadania. 
- **Czas trwania**: Określ liczbę dni pracy wymaganych do wykonania zadania.
- **Identyfikator harmonogramu**: ten automatycznie generowany identyfikator jest używany do porządkowania zadań w hierarchii. Współzależności między zadaniami zarządzają rzeczywistą kolejnością pracy nad zadaniami.
 
### <a name="staffing-attributes"></a>Atrybuty personelu

Dostęp do atrybutów obsługi personelu jest możliwy za pośrednictwem pola **zasoby** w harmonogramie. Użytkownik może wyszukać istniejący zasób lub kliknąć pozycję **Utwórz**, a następnie w okienku **szybkie tworzenie** dodać członka zespołu projektu jako nowy zasób.

Pola **rola**, **jednostka zasobów** i **nazwa stanowiska** są używane do opisywania wymagań dotyczących personelu dla zadania. Te atrybuty personelu wraz z harmonogramem zadań są używane do znajdowania dostępnych zasobów w celu wykonania tego zadania.

**Role** — określa typ zasobu wymagany do wykonania zadania.

**Jednostka zasobów** — należy podać jednostkę, z której mają zostać przypisane zasoby dla zadania. Ten atrybut wpływa na koszt i oszacowania sprzedaży danego zadania, jeśli koszt i stawka za dany zasób są ustawiane na podstawie jednostek, które należy pozyskać.

**Nazwa stanowiska** — wprowadź przyjazną nazwę zasobu ogólnego służącą jako symbol zastępczy zasobu, który ostatecznie wykona prace.

W polu **zasoby** znajduje się nazwa pozycji zasobu ogólnego lub nazwanego zasobu.

Pole **Kategoria** zawiera wartości wskazujące szerszy typ pracy, do której może zostać zgrupowane zadanie. To pole nie ma wpływu na planowanie ani na kadrę. Jest używane wyłącznie podczas raportowania.

### <a name="task-dependencies"></a>Zależności między zadaniami 

Harmonogram w PSA może służyć do tworzenia relacji poprzedników między zadaniami. Pole **poprzednika** w obszarze **zadania** zawiera jedną lub kilka wartości, które wskazuje zadania, które są zależne od zadania. Podczas przypisywania wartości poprzednika do zadania, zadanie może się rozpocząć po zakończeniu wszystkich zadań poprzedników. Z powodu zależności planowana data rozpoczęcia zadania jest ustawiana na dzień, w którym wykonane zostaną zadania poprzednika.

Tryb zadania nie ma wpływu na aktualizacje wprowadzane do dat rozpoczęcia i zakończenia zadań poprzednika/zależnych.

## <a name="task-mode"></a>Tryb zadania 

Tryb zadania określa sposób planowania zadań węzłów liścia. PSA obsługuje dwa tryby zadania dla każdego zadania: tryb planowania automatycznego i tryb planowania ręcznego.

### <a name="auto-scheduling"></a>Automatyczne planowanie 
 
Po ustawieniu trybu zadania na **Automatyczne planowanie** aparat planowania zadania używa reguł planowania na poniższych atrybutach zadania, aby ustalić harmonogram dla zadania.

#### <a name="scheduling-rules"></a>Reguły planowania

Domyślnie, jeśli zadanie węzła liścia nie ma poprzedników, jego data rozpoczęcia jest zaplanowaną datą rozpoczęcia projektu. Czas trwania zadania węzła liścia jest zawsze obliczany jako liczba dni roboczych pomiędzy datą rozpoczęcia a datą zakończenia. Gdy zadanie jest planowane automatycznie, aparat planowania kieruje się poniższymi regułami:

- Daty rozpoczęcia i zakończenia zadania muszą być zawsze dniami roboczymi w kalendarzu planowania projektu. 
- Data rozpoczęcia zadania, które ma poprzedników, staje się domyślnie najpóźniejszą datą zakończenia poprzedników.
- Nakład pracy jest obliczany za pomocą następującej formuły: liczba osób × czas trwania × godziny w standardowym dniu pracy w kalendarzu projektu.

### <a name="manual-scheduling"></a>Planowanie ręczne

Jeśli reguły automatycznego planowania nie spełniają wymagań użytkownika, można ustawić tryb zadania na **ręczne planowanie.** Powstrzymuje to aparat planowania przed obliczaniem wartości dla innych atrybutów planowania. Bez względu na tryb zadania ustawienie poprzedników zawsze ma wpływ na datę rozpoczęcia zadania zależnego.


[!INCLUDE[footer-include](../includes/footer-banner.md)]