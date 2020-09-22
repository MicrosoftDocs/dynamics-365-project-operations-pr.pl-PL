---
title: Nowości i zmiany w programie Project Service Automation w wersji 3
description: Niniejszy temat zawiera informacje dotyczące nowości i zmian w programie Project Service Automation w wersji 3.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 8a4f3c98-063a-4db8-8645-06b0fbe1b5db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ad0ef8cdac2990716baff27f86a5473bc0b031fe
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754328"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Nowości i zmiany w programie Project Service Automation w wersji 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

W tym temat zamieszczono informacje dotyczące zmian w interfejsie użytkownika (UI), funkcji i terminologii w programie Project Service Automation między wersją 2 lub wersją 1 i wersją 3.

## <a name="project-scheduling"></a>Harmonogram projektu
Zmieniono nazwę harmonogramu projektu, który w poprzednich wersjach programu był znany jako Struktura podziału pracy (SPP), na Harmonogram i teraz jest on dostępny po kliknięciu karty **Harmonogram**. 

![Harmonogram projektu](media/psa-schedule-01.png)

Obecnie harmonogram zawiera nową powierzchnię interakcji, która jest zarówno nowoczesna, jak i łatwo dostępna. Jednak podstawowy silnik planowania usługi Project Service Automation nie uległ zmianie. Przyciski sterujące na wstążce siatki harmonogramu umożliwiają interakcję z harmonogramem podobnie jak w poprzedniej wersji Project Service Automation. Do dodatkowych zmian w harmonogramie zalicza się:

- **Wykres Gantta** — wykres Gantta nie jest już dostępny. Nowa Wizualizacja Gannta będzie znowu dostępna w kolejnej aktualizacji.
- **Nagłówki kolumn** — aby ukryć nagłówki kolumn w siatce, kliknij wskaźnik w dół znajdujący się obok tytułu kolumny. 
- **Kolumny** — ukryte kolumny można wyświetlić, klikając opcję **Dodaj kolumnę**. 
- **Kategoria transakcji** — wyszukiwanie **kategorii transakcji** zostało dodane do siatki harmonogramu i domyślnie jest wyświetlane. 
 
## <a name="project-templates"></a>Szablony projektów
W ramach funkcji szablonu projektu wprowadzono następujące zmiany.

### <a name="create-a-project-template"></a>Tworzeniu szablonu projektu 
Szablon projektu można utworzyć w wersji 3, podobnie jak w przypadku poprzednich wersji Project Service Automation. Szablon może zawierać tylko harmonogram, a harmonogram może zawierać przypisania, ale nie jest to wymagane. Jeśli harmonogram zawiera przypisania, mogą one dotyczyć tylko zasobów ogólnych. Istnieje możliwość generowania wymagań zasobów dla zasobów ogólnych, ale nie można ich rezerwować za pomocą rzeczywistych zasobów w szablonie. Zasób rzeczywisty nie może być zarezerwowany dla zespołu w szablonie. 

### <a name="create-a-template-from-an-existing-template"></a>Tworzenie szablonu na podstawie istniejącego szablonu
Kiedy nowy szablon projektu jest tworzony na podstawie istniejącego szablonu w programie Project Service Automation w wersji 3, mają miejsce następujące zdarzenia: 

- Harmonogram projektu źródłowego jest kopiowany do szablonu. 
- Zasoby ogólne są kopiowane do zespołu i są kopiowane wszystkie przypisania zasobów ogólnych. Wymagania dotyczące zasobów ogólnych nie są kopiowane. 

### <a name="create-a-template-from-an-existing-project"></a>Tworzenie szablonu na podstawie istniejącego projektu
Kiedy nowy szablon projektu jest tworzony na podstawie istniejącego projektu, mają miejsce następujące zdarzenia: 

- Harmonogram projektu źródłowego jest kopiowany do szablonu. 
- Zasoby ogólne są kopiowane do zespołu i są zachowywane wszystkie przypisania zasobów ogólnych. Wymagania dotyczące zasobów ogólnych nie są kopiowane.    
- Nazwane zasoby, zarówno przypisane, jak i nieprzypisane, są usuwane z zespołu i zastępowane zasobami ogólnymi.
- Obecne informacje o klientach są usuwane. 
- Obecne odniesienia do ofert i kontaktów są usuwane. 

### <a name="create-a-project-from-a-template"></a>Utwórz projekt na podstawie szablonu
W programie Project Service Automation w wersji 3, kiedy nowy szablon projektu jest tworzony na podstawie istniejącego szablonu, mają miejsce następujące zdarzenia:

- Harmonogram, zespół i przypisania są kopiowane do nowego projektu.   
- Data rozpoczęcia jest albo datą kopiowania, albo datą wybraną przez użytkownika.   
- W przypadku ogólnych członków zespołu mających wymagania dotyczące zasobów w szablonie, wymagania nie są kopiowane ani generowane automatycznie. Konieczne będzie ich wygenerowanie. 

## <a name="copy-a-project"></a>Kopiowanie projektu
W programie Project Service Automation w wersji 3, kiedy kopiowany jest projekt, mają miejsce następujące zdarzenia: 

- Szacowana data rozpoczęcia jest kopiowana, ale można ją zmienić.  
- Harmonogram i zadania projektu są kopiowane. 
- Zostaną skopiowane zasoby ogólne i ich przypisania. Wymagania zasobów ogólnych nie są kopiowane. Konieczne będzie ich ponowne wygenerowanie. 
- Rzeczywiste zasoby i ich przypisania nie są kopiowane. Zamiast tego są one zastępowane przez zasoby ogólne. 
- Wartości rzeczywiste nie są kopiowane do nowego projektu. 

## <a name="move-a-scheduled-project"></a>Przenoszenie zaplanowanego projektu
Po przeniesieniu harmonogramu istniejącego projektu do przodu maja miejsce następujące zdarzenia: 

- Daty zadania są automatycznie przenoszone, aby odpowiadały okresowi przesunięcia. 
- Przypisane zasoby ogólne pozostają przypisane.   
- Jeśli zostały utworzone przed przeniesieniem projektu, wymagania zasobu ogólnego pozostaną bez zmian i nie zostaną automatycznie wygenerowane ponownie. Konieczne będzie ich ponowne wygenerowanie w celu odzwierciedlenia nowych przypisań powstałych na skutek przesunięcia zadania. 
- Przypisania rzeczywistych zasobów zmieniają się, tak aby odpowiadały przesunięciu daty zadania. Rezerwacje rzeczywistych zasobów nie zmieniają się. Rezerwacje trzeba będzie modyfikować przy użyciu widoku uzgodnienia. 
- Zasoby zespołu z rezerwacjami, ale bez przypisań, nie zmienią się. 
- Wartości rzeczywiste nie są przenoszone. 

## <a name="estimates"></a>Szacunki
Szacunki zostały podzielone na dwie karty **Przypisania zasobów** i **oszacowania**. Na karcie **Przypisanie zasobu** są wyświetlane szacowane nakłady pracy oraz przydziały zasobów dla zadań w widoku z danymi okresowymi. Można edytować oszacowania w zależności od tego, co wygenerował aparat planowania.

![Karta przypisań zasobów pokazuje szacowane nakłady pracy i przypisania zasobów do zadań](media/resource-assignments-tab-02.png)

Na karcie **oszacowania** przedstawiono wyceny i kwoty sprzedaży dla przydziałów zasobów. Kwoty są tylko do odczytu. Wycena i cena sprzedaży są obecnie określane na podstawie przypisań członków zespołu w harmonogramie. Oznacza to, że jeśli użytkownik ma zadanie bez przypisania, będzie ono widoczne w nieprzypisanym zasobniku. Oznacza to również, że bez**roli**, która jest domyślnym wymiarem kalkulacji cen, koszt i sprzedaż nie będą szacowane, jeśli użytkownik ma klienta lub kontrakt/ofertę skojarzoną z danym projektem. 

![Karta oszacowania pokazuje koszty i kwoty sprzedaży](media/estimates-tab-03.png)
  
Kategoria jest również obsługiwana w zadaniach w widoku harmonogramu. Grupowanie według kategorii w widoku okresowym oszacowań będzie zapewniało lepsze doświadczenie, szczególnie wtedy, gdy w projekcie są również szacowane koszty. Oszacowania kosztów są wprowadzane przy użyciu siatki na osobnej karcie. 

Oszacowania wydatków są wprowadzane w siatce na karcie **oszacowań kosztów**. 

![Karta oszacowania wydatków z siatką oszacowań wydatków](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Zarządzanie zasobami
W programie Project Service Automation w wersji 3, z nowym ujednoliconym interfejsem klienta i zmianami w relacjach między rezerwacjami a przypisaniami, w porównaniu z wersjami 1 i 2 znaczącym zmianom uległ proces obsadzania zespołu projektu zasobami ogólnymi lub rzeczywistymi. Natomiast pojęcia dotyczące zasobów, które można zarezerwować, zarówno **rzeczywistych**, jak i **ogólnych**, pozostają takie same, co w przypadku członków zespołu, wymagań, przypisań i rezerwacji.   

![Korzystanie z selektora zasobów](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Przypisywanie rzeczywistego zasobu, który można zarezerwować 
W programie Project Service Automation w wersji 3 rezerwacje i przydziały zadań nie są tak ściśle powiązane jak w poprzednich wersjach programu Project Service Automation. Można użyć siatki zespołu do rezerwowania **rzeczywistego** członka zespołu, podobnie jak w przypadku środowiska na rynku.

Korzystając z selektora zasobów w harmonogramie, można wybrać członka zespołu utworzonego w widoku zespołu, a następnie przypisać go do zadań. Można w dalszym ciągu przypisywać zadania do członków zespołu, nawet po ich zarezerwowaniu. Użyj karty **uzgodnienie**, aby uzgodnić członków zespołu z różnicami w rezerwacjach i przypisaniach.

W selektorze zasobów będą pokazywani członkowie zespołu projektu. Można również użyć selektora zasobów w celu wyszukania i wyświetlenia innych zasobów, które nie są częścią zespołu projektu. Użytkownik może przypisywać je do zadania, włączając w skład zespołu projektu. Konieczne będzie ich zarezerwowanie przy użyciu **tablicy harmonogramu** lub karty **uzgadnianie**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Przypisz ogólny zasób możliwy do zarezerwowania do zadania i zespołu projektu, a następnie zrealizuj zapotrzebowanie, przydzielając rzeczywisty zasób przy użyciu Tablicy harmonogramu. 
W programie Project Service Automation w wersji 3 funkcja generowania zespołu nie jest używana w przypadku zasobów ogólnych. Zamiast tego można utworzyć i bezpośrednio przypisać zasób ogólny z poziomu harmonogramu, wpisując nazwę stanowiska zasobu ogólnego w komórce zasobu w harmonogramie. Można też wybrać ikonę zasobu w komórce, a następnie przy użyciu selektora zasobów wpisać nazwę zasobu ogólnego, który ma zostać utworzony. Spowoduje to otwarcie panelu szybkiego tworzenia, dzięki któremu użytkownik może ustawić rolę i jednostkę organizacyjną członka zespołu zasobu ogólnego. Po utworzeniu zasobu jest on przypisywany do zadania i można go dalej przypisywać do innych zadań w harmonogramie.    
 
Po przypisaniu zasobu do wszystkich odpowiednich zadań można wygenerować wymaganie zasobu i zrealizować je poprzez bezpośrednie zarezerwowanie przy użyciu **tablicy harmonogramu** lub wysyłając żądanie zasobu. Istnieje również możliwość dodawania zasobów ogólnych bezpośrednio do siatki członków zespołu. 

Zasoby ogólne są dodawane do zespołu projektu bez wymagań zasobów oraz daty rozpoczęcia/zakończenia projektu do czasu jego wygenerowania. Aby wygenerować wymaganie, wybierz zasób ogólny i kliknij opcję **Generuj**. Łącze wymagania będzie teraz wyświetlane i wraz z wymaganymi godzinami zostanie wstawiona liczba godzin przypisanych do użytkownika. Klikając łącze, można otworzyć program i zaktualizować jego wymaganie.
  
Kiedy rezerwacja jest kompletna i w całości zrealizowana przez nazwany zasób, zasób ogólny jest zastępowany zasobem nazwanym, a przydział w harmonogramie jest aktualizowany za pomocą nazwanego zasobu. 

Proponowane zasoby dotyczące wymagań są teraz przechowywane na karcie, a nie w osobnej sekcji.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Wiele nazwanych zasobów dostarczających zasób ogólny
Jeśli wymagane jest realizowane przez wiele zasobów, zasób ogólny pozostaje w zespole i jest przypisany do zadania. Członkowie zespołu z nazwami, którzy są zarezerwowani, nie są przypisywani jako część stanowiska. Menedżer projektu może przypisywać pracę do rzeczywistych zasobów w zależności od potrzeb.  W widoku **uzgodnienia** jest podział rezerwacji między wiele zasobów do wielu przypisań zadań. Nie jest to wykonywane automatycznie, ponieważ w bardziej skomplikowanych scenariuszach, na przykład w przypadku, gdy użytkownik ma pakiet zadań składających się na wymaganie, należy przyjąć zamierzenia, w jaki sposób Menedżer projektu chce dokonywać przypisań. Ponieważ system nie jest w stanie zrozumieć zamierzeń, założenia mogą być inne niż zamierzone i może wystąpić nieprawidłowy lub nieprzewidywalny rezultat. Przewidywany wynik polega na tym, że zasób ogólny pozostaje przypisany do momentu celowego przypisania zasobów w widoku **uzgadniania**.

### <a name="reconciliation"></a>Uzgadnianie
Karta **Uzgadnianie**, w której są pokazywane wszystkie rezerwacje i przypisania dla każdego członka zespołu projektu. W komórkach widać godziny, które reprezentują okresy od miesięcy aż po dni. W tym widoku menedżerowie projektów mogą uzgadniać rezerwacje członków zespołu oraz ich przypisania do zespołu projektu. Jest to pomocne, ponieważ rezerwacje i przypisania zadań nie są ściśle sprzężone, co pozwala na większą elastyczność podczas planowania projektu. 

![Karta Uzgadnianie, w której są pokazywane rezerwacje i przypisania dla każdego członka zespołu.](media/resource-reconciliation-tab-06.png)

W przypadku każdego zasobu jest uwzględniana różnica między rezerwacją członka zasobu a zestawieniem jego przypisań zadań. Ponadto widok pokazuje następujące dwie różnice, które mogą wystąpić w przypadku rezerwacji i przypisań w projekcie: 

- **Niedobór rezerwacji** — niedobory rezerwacji powstają wtedy, gdy zasób ma więcej przypisań, niż rezerwacji. Ponieważ dyspozycyjność nie została zarezerwowana, menedżer projektu może naprawić tę sytuację poprzez rozszerzenie rezerwacji zasobu w sposób pokrywający niedobór. 
- **Nadmiarowe rezerwacje** — nadmierne rezerwacje występują, gdy zasób zarezerwowano do projektu, ale nie przypisano go do zadań.  Ta sytuacja może być akceptowalna, jeśli na przykład zasób zarezerwowano przed przypisaniem zadań. Jednak w innych przypadkach może nie być planowane przypisanie zasobu, a menedżer projektu powinien rozważyć anulowanie rezerwacji zasobu, tak aby zwolnić jego dyspozycyjność dla innego projektu. 

W sytuacjach, gdy istnieją przypisania zadań dla zasobu, ale nie ma rezerwacji (niedobór rezerwacji), można wybrać zagregowany niedobór rezerwacji, a następnie kliknąć przycisk **Rozszerz rezerwację**. W tym miejscu można wyświetlić rezerwację niezbędną do wyeliminowania problemu niedoboru i dostępności zasobu. 
 
## <a name="time-and-expense"></a>Czas i wydatek
W tej sekcji zamieszczono informacje dotyczące zmian czasu, wydatków i zatwierdzania w wersji 3 rozwiązania Project Service Automation. W ramach rozwiązania Dynamics 365 Project Service Automation funkcja **Wpis czasu** została odświeżona w celu wykorzystania struktury ujednoliconego interfejsu. Dzięki temu można dostarczać spójny, jednolity interfejs użytkownika, który jest łatwy w obsłudze i zapewnia dobra widoczność na wszystkich ekranach bez względu na ich wielkość. 

### <a name="landing-page"></a>Strona docelowa
Nierozszerzalny niestandardowy wpis czasu został wycofany w wersji 3. Zamiast tego wprowadzono rozszerzalne i dostępne funkcje siatki natywnej. Aby uzyskać dostęp do funkcji wpisu czasu, należy skorzystać z mapy witryny znajdującej się po lewej stronie. Wprowadzenie tej zmiany spowoduje, że użytkownik nie będzie mógł wprowadzić jednorazowo czasu dla jednego tygodnia. Zamiast tego konieczne będzie utworzenie wpisu czasu dla każdego dnia w siatce. Po utworzeniu kilku wpisów czasu użytkownicy mogą tworzyć zbiorczo wpisy czasu, korzystając z funkcji **Kopiuj** objaśnionej szerzej w dalszej części tego tematu. 

![Strona docelowa wpisu czasu](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Tworzenie nowych wpisów czasu 
Kliknij **Nowy** na wstążce, aby otworzyć stronę szybkiego tworzenia w celu wpisania czasu, gdzie można wpisywać okres trwania w minutach, godzinach lub dniach. W tym celu należy tylko rozpocząć wpisywanie h, m lub d wraz z ilością.  

![Szybkie tworzenie wpisu czasu](media/quick-create-time-entry-08.png)

Pola wyszukiwania są obsługiwane w widokach systemowych. Na przykład po wprowadzeniu informacji o projekcie pole **zadanie projektu** będzie domyślnie ustawione na wartość **Moje otwarte zadania projektu**. Aby utworzyć wpisy czasu dla zadań, które nie są przypisane do użytkownika, kliknij **Zmień widok** w obszarze wyszukiwania i wybierz pozycję **wszystkie aktywne zadania projektu**. Po utworzeniu i wyświetleniu danego wpisu czasu w siatce można edytować wartości wierszy bezpośrednio w siatce.  

### <a name="bulk-createcopy"></a>Zbiorcze tworzenie/kopiowanie 
Po utworzeniu kilku wpisów czasu można je kopiować i w ten sposób tworzyć dodatkowe wpisy czasu zbiorczo. Kliknij **Kopiuj**, aby otworzyć okno dialogowe **Kopiuj**. W polu **od okresu: Data rozpoczęcia** ustaw zakres dat, z którego okresy muszą zostać skopiowane. W polu **Do okresu: Data rozpoczęcia** określ datę utworzenia wpisów godzin. Kliknij przycisk **Kopiuj**, aby skopiować wpisy godzin do odpowiedniego dnia tygodnia wskazanego w polu **Do okresu**. Na przykład wpis czasu poniedziałek z ubiegłego tygodnia zostanie skopiowany na poniedziałek w tygodniu wskazanym w polu **do okresu**. 

![Zbiorcze kopiowanie wpisów czasu](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importowanie danych 
Przypisania i wymiana działają zgodnie ze wzorcem interfejsu użytkownika, co umożliwia użytkownikowi określenie zakresu dat, z którego należy zaimportować rezerwacje. Następnie należy wyraźnie wybrać rezerwacje, które mają zostać skopiowane do **wersji roboczych** wpisów czasu. W wersji 3 nie jest już widoczna struktura **sugerowanych** wpisów czasu w siatce i w kalendarzu.  

### <a name="change-in-calendar-control"></a>Zmiany w kalendarzu
W wersji 3 zrezygnowaliśmy z niestandardowej obsługi kalendarza i używamy teraz kalendarza UC do wyświetlania wpisów czasu dla tygodnia. W tym kalendarzu można wyświetlać dni, tygodnie i miesiące. 

> [!NOTE]
> Ograniczenie w kalendarzu polega na tym, że formant nie obsługuje działań na poszczególnych elementach kalendarza. Nie można na przykład wybrać jednego lub większej liczby elementów kalendarza, a także przesłać ani usunąć tych elementów. Kliknięcie elementu kalendarza spowoduje otwarcie strony **encja wpisu czasu** w celu wykonania dodatkowych akcji. 

### <a name="extensibility"></a>Możliwości rozszerzania
**Gromadzenie danych o polach niestandardowych tylko z poziomu encji dotyczącej czasu i wpisu wydatkowania** — w tym miejscu jest tylko edytowalna siatka, siatka tylko do odczytu i formanty kalendarza z platformy. Wszystkie te formanty są natywne i w związku z tym będą obsługiwały dostosowania. W programie Project Service Automation w wersji 3 można dodawać pola niestandardowe, konfigurować pola wyszukiwania i wykonywać kopie zapasowe tych pól przy użyciu widoków niestandardowych. Istnieje również możliwość ustawienia niestandardowej logiki biznesowej, która jest oparta na wartościach wybranych w polach niestandardowych.  

**Przechwytuj dane w polach niestandardowych z wpisu dotyczącego czasu i wydatku i propaguj je za pośrednictwem encji obsługujących przepływ przesyłania i zatwierdzania** — typowy sposób przetwarzania wpisów czasu jest podany na poniższym diagramie.

![Przepływ przetwarzania wpisu czasu](media/process-time-entries-10.png)

Jeśli wymagania biznesowe przewidują, że obiekty typu czas i wydatki muszą przechwytywać niestandardowe wymiary kalkulacji cen i propagować wartości ustawione przez zasób typu czas i wejście w niestandardowym wymiarze kalkulacji cen za pośrednictwem wszystkich encji z poprzedniej grafiki, zobacz [Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen](set-up-pricing-dimensions.md)

Aby sprostać wymaganiom biznesowym, podczas gdy encje czasu i wydatku muszą przechwytywać niestandardowe wymiary niepodlegające kalkulacji cen i propagować te wartości, można użyć konfiguracji wymiarów kalkulacji cen i przedstawić niestandardowe wymiary jako wymiary kalkulacji cen bez kosztów lub stawek. Innym scenariuszem może być dodanie pola niestandardowego do każdej encji, przy użyciu tej samej nazwy pola we wszystkich encjach. Można utworzyć wtyczki niestandardowe, aby powiązać rekordy w encjach uczestniczących w przepływie przesyłania/zatwierdzania przy użyciu encji źródłowej transakcji i połączenia transakcji.  

### <a name="delegate-time-and-expense-entry"></a>Delegowanie czasu lub wpisu dotyczącego wydatków
Platforma Common Data Service nie obsługuje jednego użytkownika, który uosabia drugiego, co oznacza, że w wersji 3 programu Project Service Automation nie ma obsługi delegowanego czasu i wpisu wydatku. Jednak partnerzy i klienci znaleźli obejście tego problemu, aby zapewnić pomoc techniczną dotyczącą delegowanego wpisu czasu w wersji 3. Jest to jedynie obejście, a nie rozwiązanie kompletne, więc ważne jest zrozumienie ograniczeń i użycie tego podejścia tylko wtedy, gdy ograniczenia są dopuszczalne. 

> [!IMPORTANT]
> Te informacje powinny być uznawane wyłącznie jako sugerowane wskazówki dotyczące niestandardowej implementacji partnera/klienta. Zespół produktu nie będzie oferować formalnej pomocy technicznej w zakresie tych funkcji za pośrednictwem żadnych kanałów pomocy technicznej.

### <a name="customization-details"></a>Szczegóły dostosowywania 
Dostosowanie umożliwia dodanie **Zasobu, który można rezerwować** w celu tworzenia i edytowania doświadczeń, co pozwala użytkownikowi pełnić rolę delegata, zmieniając pole **Rezerwacja zasobu** na innego użytkownika, dla którego wpisy czasu i wydatku muszą zostać zarejestrowane. Poniższe kroki obejmują delegację wpisu czasu. Te same informacje stosuje się do delegowania wpisów wydatków. 
 
1.  Upewnij się, że delegowany użytkownik ma globalny dostęp do projektów i zadań projektu. 
1.  Ponieważ **zasób z możliwością rezerwacji**, który jest polem w encji **Wpis czasu** nie jest widoczny na stronie **Szybkie tworzenie**, trzeba go dodać.

    -lub-

    Utwórz widok niestandardowy, który umożliwia wyświetlanie tylko wpisów czasu tworzonych dla zasobu. Opublikuj dostosowania w programie App module Designer, które będą wyświetlane w obszarze **Selektor widoków** na stronie **Wpisy czasu**. Istnieją dwa dodatki plug-in, które obsługują konfigurowanie menedżera dla wpisów czasu spoza projektu:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Utwórz nowy dodatek plug-in, aby zastąpić pole **Menedżer** menedżerem przypisanego użytkownika w polu **zasobu, który można zarezerwować**. Użyj tego samego **etapu wykonania** co plug-in OOB (walidacja wstępna) i użyj **Kolejności wykonania** wyższej niż plug-iny OOB (większej niż 1). Pozwoli to zagwarantować, że dodatek plug-in jest wykonywany po zastosowaniu dodatków plug-in typu OOB.  
 
### <a name="end-user-experience"></a>Środowisko użytkownika
1.  Po utworzeniu wpisu czasu na stronie szybkie tworzenie wprowadź szczegóły zadania projektu i projektu, a następnie wybierz użytkownika w polu **zasobu, który można zarezerwować**, dla którego mają zostać zarejestrowane wpisy czasu. 
2.  Domyślnie w tym polu jest domyślnie zalogowany użytkownik, ale biorąc pod uwagę, że użytkownik zastąpił to pole, wpis czasu jest teraz tworzony dla wybranego **zasobu możliwego do zarezerwowania**.
3.  Po przesłaniu przez użytkownika czasu utworzonych dla tych rekordów wpisy zostaną umieszczone w kolejce dla osoby zatwierdzającej w projekcie w oczekiwany sposób. 
4.  Po odwołaniu wpisów czasu utworzonych dla innego użytkownika wpisy czasu będą powracały do stanu **wersji roboczej** z polem **zasobu, który można zarezerwować** ustawionym dla innego użytkownika. 
5.  Można też przełączyć się do widoku niestandardowego, aby filtrować wpisy czasu utworzone dla innego użytkownika. 
 
### <a name="limitations"></a>Ograniczenia
Funkcje **kopiowania** i **importowania** działają tylko w kontekście użytkownika, który jest zalogowany. Oznacza to, że nie można kopiować ani importować wpisów czasu tworzonych dla użytkownika zalogowanego jako zasób możliwy do zarezerwowania.

Wpisy czasu, które nie są związane z projektem, będą przekierowywane celem zatwierdzenia do menedżera zasobu, który można zarezerwować, tylko wtedy, gdy krok 4 w sekcji **Szczegóły dostosowania** zostanie ukończony. W przeciwnym razie wpisy czasu spoza projektu dla innego użytkownika będą rozsyłane nieprawidłowo do menedżera zalogowanego użytkownika. 

### <a name="other-changes"></a>Inne zmiany 
Funkcja **Rezerwacje i zadania** została usunięta. 

## <a name="multidimensional-pricing"></a>Wielowymiarowe ceny
Aby zmaksymalizować elastyczność i zaspokoić różne wymagania biznesowe, wersja 3 rozwiązania Project Service Automation obsługuje autonomiczne stosowanie zestawów wymiarów kalkulacji cen względem kosztów i stawek. Wartości wymiaru mogą być ustawiane jako domyślne, a następnie propagowane w procesie kosztów i kalkulacji cen z profilowania zasobu do wpisu czasu do wartości rzeczywistych projektu. Specyficzne dla klienta ustawienia i modyfikacje lub rozszerzenia są oparte na standardowej infrastrukturze dostosowywania.

Program Project Service Automation jest dostarczany z domyślnym zestawem wymiarów kalkulacji cen, rolami i encjami zasobów oraz zezwala na konfigurowanie cen i kosztów dla każdej kombinacji roli i jednostki organizacyjnej.

W przypadku klientów korzystających z Project Service Automation, którzy chcą w dalszym ciągu używać wymienionych na liście gotowych pól jako wymiarów kalkulacji cen w wersji 3, nie będzie żadnych zauważalnych zmian. Można nadal korzystać z usługi Project Service Automation w zwykły sposób. Jeśli jednak trzeba ustalić cenę lub koszt dla zasobów za pomocą innych dodatkowych atrybutów, wersja 3 pozwala na dodawanie własnych wymiarów kalkulacji cen do programu Project Service Automation. Rozszerzenie niestandardowych wymiarów cenowych jest skomplikowanym środowiskiem konfiguracyjnym. 

## <a name="quotes-and-contracts"></a>Oferty i kontrakty
W wersji 3 Project Service Automation wprowadzono zmiany w aspektach konfiguracji i zarządzania ofertami i kontraktami. W poniższych sekcjach przedstawiono więcej szczegółowych informacji.

### <a name="set-up-chargeability-options"></a>Konfigurowanie opcji naliczania opłat
W wersjach 1 i 2, konfiguracja odpłatności dla ról i kategorii w określonych ofertach i kontraktach była wykonywana przy użyciu widoku **Odpłatność**, który był umieszczony w górnej części funkcji nawigacji wiersza oferty lub pozycji kontraktu. W tym miejscu można było również skonfigurować ceny dla tych ról i kategorii wydatków.

Od wersji 3 konfiguracja opcji odpłatności według roli i kategorii kosztów będzie możliwa na poziomie oferty lub pozycji kontraktu. Ustawienia kalkulacji cen są zależne od konfiguracji odpłatności. Użytkownik będzie miał do dyspozycji **płatne role** i **płatne kategorie** jako karty **w wierszu oferty** i **w pozycji kontraktu** bez konieczności korzystania z nawigacji u góry.

![Odpłatne role](media/chargeable-12.png)
 
Konfigurowanie ról odpłatnych i kategorii odpłatnych powoduje również korzystanie z edytowalnej siatki. Dla każdej roli i kategorii obsługiwane opcje dotyczące typu rozliczenia podczas faz oferty i umowy pozostają niezmienione: **Odpłatne** i **Nieodpłatne**. **Uzupełnienie** nie jest obsługiwanym typem w fazach przedstawiania oferty lub kontraktu. **Uzupełnienie** jest obsługiwane tylko podczas zatwierdzania czasu lub wydatku.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Tworzenie i edytowanie niestandardowych cenników dla ofert Project Service Automation i kontraktu dotyczącego projektu
W wersjach 1 i 2 przy używanie cennika niestandardowego dotyczącego ofert i kontraktów było dostępne w widoku **Odpłatność** > **Edycja cen**. Widok **Odpłatność** był umieszczony w górnej nawigacji między wierszami oferty lub pozycjami kontraktu. W tym miejscu można było również skonfigurować opcje odpłatności dla kategorii ról lub wydatków.

W wersji 3 tworzenie i używanie niestandardowego cennika oferty Project Service Automation i kontraktu projektu Project Service Automation zostało oddzielone od konfiguracji odpłatności. Oferta programu Project Service Automation oraz kontrakty projektów programu Project Service Automation zawierają nową kartę o nazwie **cenniki projektów**. Na tej karcie jest wyświetlany widok skojarzony wszystkich cenników projektu dołączonych do oferty Project Service Automation lub kontraktu projektu. Aby utworzyć Cennik niestandardowy na podstawie istniejącego cennika, który jest już skojarzony z ofertą lub kontraktem projektu, kliknij opcję **Utwórz niestandardowy cennik**. Spowoduje to utworzenie kopii wszystkich skojarzonych z nim cenników i dołączenie ich do oferty lub kontraktu. Możesz teraz otworzyć cennik i zmodyfikować rolę lub cenę kategorii wydatków, tak aby zmiany cen dotyczyły tylko tej oferty lub tego kontraktu. 
  
Poniższy rysunek przedstawia sytuację przed utworzeniem cenników niestandardowych.

![Przepływ przetwarzania wpisu czasu](media/before-custom-price-lists-13.png)

Poniższy rysunek przedstawia sytuację po utworzeniu cenników niestandardowych.

![Przepływ przetwarzania wpisu czasu](media/after-custom-price-lists-14.png)

> [!NOTE]
> Podczas tworzenia cennika może następować krótka zwłoka między kliknięciem przycisku **Utwórz niestandardowy cennik** a utworzeniem niestandardowego cennika. Zalecamy odświeżenie siatki zamiast wielokrotnego klikania. Niestandardowy cennik został utworzony, jeśli skojarzona z nim nazwa cennika zawiera nazwę oferty lub nazwę kontraktu projektu.
