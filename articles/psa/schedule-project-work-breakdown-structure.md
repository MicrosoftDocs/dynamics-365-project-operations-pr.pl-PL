---
title: Zaplanuj projekt ze strukturą podziału pracy
description: Planowanie projektu ze strukturą podziału pracy w Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 24e13642ac1fb9e90daab6d8aa9b16ed9c2defbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587369"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Zaplanuj projekt ze strukturą podziału pracy (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Harmonogram projektu komunikuje, co jest niezbędne do wykonania pracy, które zasoby będą za to odpowiedzialne, i w jakich ramach czasowych praca musi zostać zrealizowana. Harmonogram projektu odzwierciedla wszystkie prace związane z dostarczeniem projektu na czas. Jednym z pierwszych kroków w początkowej fazie projektu jest opracowanie harmonogramu projektu. Aby opracować harmonogram projektu musisz utworzyć strukturę podziału pracy.  
  
 Utwórz strukturę projektu ze strukturą podziału pracy, co pomoże w:  
  
- Dokonaniu podziału pracy na zadania, którymi można zarządzać  
  
- Szacowaniu czasu wymaganego do wykonania zadania  
  
- Ustawieniu czasu trwania zadania i współzależności między zadaniami  
  
- Określeniu ról wymaganych do wykonania każdego zadania  
  
  Harmonogram projektu w strukturze podziału pracy ma znany wygląd i styl i jest uzupełniany interaktywnym wykresem Gantta.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Utwórz strukturę podziału pracy dla projektu  
 Utwórz strukturę podziału pracy, aby ukazać sekwencję zadań w projekcie. Struktura podziału pracy obejmuje zadania, wymogi dla każdego zadania i informacje o przychodach i kosztach. W swojej strukturze podziału pracy możesz dodać poniższe informacje:  
  
-   Sekwencja zadań w hierarchii  
  
-   Inne zadania, jeśli istnieją takie, które należy wykonać przed rozpoczęciem zadania  
  
-   Data rozpoczęcia, data zakończenia i czas trwania zadania  
  
-   Liczba godzin wymagana do wykonania zadania  
  
-   Wymagane kwalifikacje pracownika i jego wykształcenie  
  
-   Nazwiska pracowników przypisanych do zadania  
  
-   Szacowany przychód i koszty  
  
## <a name="task-types"></a>Typy zadań  
Tworząc swoje struktury podziału pracy, będziesz używać następujących typów zadań:  

| Zadanie | Description | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Węzeł główny projektu** | Najwyższy poziom podsumowania dla projektu. Wszystkie inne zadania projektu są tworzone na jego podstawie. Nazwa zadania głównego jest nazwą projektu. Nakład pracy, daty i czas trwania węzła głównego wynikają z wartości w hierarchii znajdującej się pod nim. Nie możesz edytować właściwości węzła głównego ani go usunąć. | 
| **Zadania sumaryczne lub zadania typu kontener** | Zadanie sumaryczne to zadanie, które składa się z podzadań. Zadanie sumaryczne nie wiąże się z żadnym nakładem pracy, ani nie posiada kosztów własnych. Jego nakład pracy i koszt są podsumowaniem jego podzadań. Można zmienić nazwę zadania sumarycznego, ale nie można zmienić nakładu pracy, dat ani czasu trwania, ponieważ te są obliczane automatycznie. Usunięcie zadania sumarycznego usuwa zadanie i wszystkie jego podzadania.|  
| **Zadania węzła liścia** | Zadanie węzła liścia reprezentuje najbardziej szczegółowe prace związane z projektem. Ma szacunkowe nakłady pracy, planowaną liczbę zasobów, planowaną datę rozpoczęcia i zakończenia oraz czas trwania.|

  
## <a name="task-hierarchy"></a>Hierarchia zadania  
 Podczas tworzenia hierarchii zadania masz dostępne następujące opcje:  
  
- **Dodaj zadanie**.   W wybranym miejscu w hierarchii zadania możesz dodać zadanie. Jeśli nie wybierzesz miejsca, nowe zadanie pojawi się na końcu.  
  
- **Zwiększ wcięcie zadania**.   Utwórz wcięcie zadania, aby stało się ono elementem podrzędnym zadania znajdującego się bezpośrednio nad nim.  
  
- **Zmniejsz wcięcie zadania**.   Zmniejsz wcięcie zadania, aby nie było już ono podzadaniem oryginalnego zadania nadrzędnego.  
  
- **Przenieś w górę i w dół**.   Przenoszenie zadań w górę i w dół w hierarchii jego zadania nadrzędnego. Przenoszenie zadania w górę lub w dół nie wpływa na związany z nim nakład pracy, koszt, daty i czas trwania.  
  
## <a name="task-attributes"></a>Atrybuty zadania  
 Nazwa zadania opisuje czynności, które należy wykonać. Różne atrybuty zadań służą do opisywania harmonogramu i wymagań dotyczących personelu dla zadania.  
  
### <a name="schedule-attributes"></a>Zaplanuj atrybuty

 - Przypisz wartości do **Nakład pracy w godzinach**, **Liczba zasobów**, **Data rozpoczęcia**, **Data zakończenia**, i **Czas trwania**, aby ustalić harmonogram dla zadania. 
 - **Nakład pracy** to przybliżona liczba godzin potrzebnych do wykonania zadania.
 - **Liczba zasobów** to oszacowanie, które menedżer projektu umieszcza w zadaniu, aby pomóc opracować najlepszy możliwy harmonogram. 
 - **Czas trwania** (w dniach) wskazuje liczbę dni pracy niezbędnych do ukończenia zadania.  
  
### <a name="staffing-attributes"></a>Atrybuty personelu

 - **Rola**, **Jednostka organizacyjna zasobu**, **Liczba zasobów**, i **Zasoby** opisują wymagania dotyczące personelu dla zadania. 
 - **Rola** opisuje typ zasobu potrzebnego do wykonania zadania. 
 - **Jednostka organizacyjna zasobu** wskazuje jednostkę organizacyjną, z której ma pochodzić zasób dla tego zadania; wpływa to również na koszt i prognozy sprzedaży dla zadania, ponieważ jest uwzględniane przy określaniu jednostkowej ceny sprzedaży dla zasobu. 
 - **Zasoby** to zasób rodzajowy lub zasób posiadający nazwę, jeśli taki zostanie znaleziony.  
  
## <a name="task-dependencies"></a>Zależności między zadaniami  
 Możesz tworzyć relacje poprzednika między jednym lub kilkoma zadaniami w strukturze podziału pracy. Możesz ustawić jedną lub więcej wartości dla pola poprzednika dla zadań, aby wskazać zadania, od których będzie to zależne. Podczas przypisywania wartości poprzednika do zadania, zadanie może się rozpocząć po zakończeniu wszystkich zadań poprzedników. Ustawienie tej współzależności dla zadania spowoduje ponowne obliczenie planowanej daty rozpoczęcia zadania jako najnowszego zakończenia wszystkich poprzedników. Wpływy na harmonogram związane z poprzednikiem nie są ograniczone przez tryb zadania zdefiniowany dla zadania.  
  
## <a name="task-mode"></a>Tryb zadania  
 Tryb zadania jest jednym z najważniejszych czynników określających planowanie zadań węzła liścia. Istnieją dwa tryby zadania dla każdego zadania: tryb planowania automatycznego i tryb planowania ręcznego.  
  
-   **Automatyczne planowanie**.   Po ustawieniu trybu zadania na Automatyczne planowanie aparat planowania zadania używa reguł planowania na poniższych atrybutach zadania, aby ustalić harmonogram dla zadania:  
  
    -   Elementy poprzedzające  
  
    -   Nakład pracy  
  
    -   Liczba zasobów  
  
    -   daty rozpoczęcia i zakończenia;  
  
-   **Reguły planowania**.   Data rozpoczęcia zadania węzła liścia, które nie ma poprzedników daje domyślnie zaplanowaną datę rozpoczęcia projektu. Czas trwania zadania węzła liścia jest zawsze obliczany jako liczba dni roboczych pomiędzy datą rozpoczęcia a datą zakończenia. Gdy zadanie jest planowane automatycznie, aparat planowania kieruje się poniższymi regułami:  
  
    -   Daty rozpoczęcia i zakończenia zadania muszą być zawsze dniami roboczymi w kalendarzu planowania projektu  
  
    -   Data rozpoczęcia zadania, które ma poprzedników, staje się domyślnie najpóźniejszą datą zakończenia poprzedników  
  
    -   Nakład pracy = Liczba osób * Czas trwania * godziny w standardowym dniu pracy kalendarza projektu  
  
-   **Planowanie ręczne**.   W niektórych przypadkach możesz chcieć odstąpić od tych zasad. W takich przypadkach możesz ustawić, aby tryb zadania dla zadania był planowany ręcznie. Zatrzymuje to aparat planowania przed obliczaniem wartości dla innych atrybutów planowania. Ustawienie poprzedników zadań zawsze wpływa na datę rozpoczęcia zadania zależnego.  
  
## <a name="create-a-work-breakdown-structure"></a>Utwórz strukturę podziału pracy  
  
1.  Przejdź do **Project Service > Projekty**.  
  
2.  Kliknij projekt, nad którym chcesz pracować.  
  
3.  Na pasku u góry ekranu, wybierz strzałkę w dół obok nazwy projektu, a następnie kliknij Struktura podziału pracy.  
  
4.  Aby dodać zadanie, kliknij **Dodaj zadanie**. Wypełnij pola dla zadania, a następnie kliknij **Zapisz**.  
  
5.  Kontynuuj dodawanie zadań do momentu ukończenia struktury podziału pracy. Podczas tworzenia struktury podziału pracy, możesz wykonać następujące czynności w celu uporządkowania zadań:  
  
    -   Zaznacz zadanie, a następnie kliknij **Wcięcie**, aby przesunąć je pod inne zadanie lub kliknij Zmniejsz wcięcie, aby wyprowadzić je spod innego zadania.  
  
    -   Zaznacz zadanie, a następnie kliknij **Przenieś w górę** lub **Przenieś w dół**, aby przenieść je w górę lub w dół na liście.  
  
    -   Kliknij **Ukryj wykres Gantta**, aby ukryć wykres Gantta, a następnie kliknij **Pokaż wykres Gantta**, aby wyświetlić go ponownie.  
  
    -   Wybierz inny okres czasu dla wykresu Gantta w **Skala czasu**.  
  
6.  Aby dodać role określone w strukturze podziału pracy do członków zespołu projektu, kliknij **Generuj zespół projektu**.  
  
7.  Po zakończeniu wprowadzania zmian kliknij **Zapisz** w prawym dolnym rogu ekranu.  
  
### <a name="see-also"></a>Zobacz także  
 [Przewodnik menedżera projektu](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
