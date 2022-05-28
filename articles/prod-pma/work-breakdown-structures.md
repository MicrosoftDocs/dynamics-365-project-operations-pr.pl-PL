---
title: Omówienie struktur podziału pracy
description: Struktura podziału pracy (SPP) to opis pracy, która zostanie wykonana w ramach projektu. Jest hierarchią zadań, która reprezentuje zrozumienie struktury prac zespołu projektu oraz wielkości, kosztów i czasu trwania każdego ze składników i zadań.
author: Yowelle
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e69d7cc97e3a7a59bdba387282fe19d12f5780
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683413"
---
# <a name="work-breakdown-structures-overview"></a>Omówienie struktur podziału pracy

[!include [banner](../includes/banner.md)]

Struktura podziału pracy (SPP) to opis pracy, która zostanie wykonana w ramach projektu. Jest hierarchią zadań, która reprezentuje zrozumienie struktury prac zespołu projektu oraz wielkości, kosztów i czasu trwania każdego ze składników i zadań. W przypadku struktury SPP są trzy podstawowe cele:

-   Opis podziału lub składu pracy w zadaniach.
-   Zaplanuj prace projektowe.
-   Oszacuj koszty poszczególnych zadań.

Stopień szczegółowości struktury SPP jest uzależniony od wymaganego poziomu dokładności dla oszacowań oraz poziomu śledzenia, który jest wymagany w odniesieniu do tych oszacowań. Projekty, które mają bardzo niską tolerancję na odchylenia harmonogramu lub kosztów, zwykle wymagają bardziej szczegółowego SPP i wymagają starannego śledzenia postępu prac i kosztów w porównaniu z SPP. Ten rodzaj projektów jest wspólny w przemyśle budownictwa i inżynierii. 

Z drugiej strony projekty w branżach takich jak media i reklama, oprogramowanie i infrastruktura IT wydają się być jedyne w swoim rodzaju, a produktywność zależy od doświadczenia i kompetencji osoby wykonującej zadanie. Dlatego branże te używają SPP do uzyskania przybliżonej wielkości projektu, a nie do szczegółowego śledzenia postępu tego projektu. 

Konstruowanie SPP jest procesem intensywnie wykonywanym na czas dłuższym niż długi czas, który wymaga współpracy i informacji z wielu różnych osób. Niniejsza temat opisuje sposób korzystania z ulepszeń SPP w celu spełnienia wymagań dotyczących oszacowań i śledzenia.

## <a name="prerequisites-for-creating-a-wbs"></a>Wymagania wstępne dla tworzenia zasad SPP
Aby utworzyć SPP, należy utworzyć harmonogram pracy i oszacować koszt pracy.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Wymagania wstępne dotyczące tworzenia harmonogramu pracy

Aby korzystać z pełnych możliwości planowania funkcji SPP, należy wykonać następujące czynności konfiguracyjne:

1.  Skonfiguruj kalendarz domyślny i kalendarz projektu:
    1.  Przejdź do **Zarządzanie projektami i księgowanie** &gt; **Ustawienia** &gt; **Parametry Zarządzanie projektami i księgowanie** &gt; **Planowanie**. W polu **Domyślny kalendarz pracy** określ kalendarz domyślny. Będzie to domyślny kalendarz pracy dla każdego tworzonego nowego projektu.
    2.  Użytkownik może zmienić kalendarz domyślny dla określonego projektu. Kliknij stronę szczegółów projektu, a następnie na skróconej karcie **Zespół projektowy i planowanie** zaktualizuj pole **Kalendarz planowania**, wybierając inny kalendarz.

2.  Konfigurowanie standardowych dni roboczych i godzin pracy. Kalendarz ustawiony jako kalendarz roboczy w projekcie zostanie użyty w SPP w celu określenia następujących informacji:

-   Dni robocze i święta
-   Liczba godzin pracy w ciągu doby

Aby skonfigurować dni robocze i godzin pracy w kalendarzu albo utworzyć nowy kalendarz, kliknij **Administracja organizacji** &gt; **Wspólne** &gt; **Kalendarz**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Wymagania wstępne dotyczące oceny kosztu pracy

Aby korzystać z funkcji szacowania kosztów w pełnym zakresie, należy skonfigurować koszty i ceny sprzedaży dla pracowników, kategorii robocizny, kosztów i opłat oraz towarów.

-   Aby skonfigurować koszt i cenę sprzedaży, kategorie kosztów i robocizny, kliknij opcję **Zarządzanie projektami i księgowanie** &gt; **Ustawienia** &gt; **Ceny**.
-   Aby ustawić koszt i cenę sprzedaży towarów, użyj strony **Umowy handlowe** dla każdego towaru na stronie listy **Zwolnione produkty** w sekcji Zarządzanie informacjami o produktach.

## <a name="creating-a-wbs"></a>Tworzenie WBS
Tworząc kody SPP, składają się z trzech działań:

1.  **Rozkład pracy** — Tworzenie podziału pracy w odbudowanych fragmentach lub zadaniach.
2.  **Harmonogram pracy** — Oszacuj czas wymagany do wykonania zadania, ustaw wzajemne zależności zadań i wybierz daty rozpoczęcia i zakończenia zadań.
3.  **Szacowanie kosztów** — szacowanie kosztów poszczególnych zadań.

W poniższych sekcjach opisano, jak funkcje SPP mogą pomóc w każdym z tych działań.

### <a name="work-decomposition"></a>Rozkład pracy

Tworzenie podziału lub rozkładu nad pracą zazwyczaj jest pierwszym krokiem w procesie tworzenia SPP. Funkcja SPP obsługuje następujące podstawowe konstrukcje podziału pracy i rozkładu. 

**Zadanie główne projektu** Zadanie główne projektu jest zadaniem sumarycznym najwyższego poziomu dla projektu. Wszystkie inne zadania projektu są tworzone pod nim. Nazwa głównego zadania jest zawsze nazwą projektu. W zakresie nakładów pracy, dat i czasu trwania węzła głównego są sumowane wartości zadań znajdujących się poniżej zadania głównego. Nie możesz modyfikować właściwości węzła głównego ani go usuwać.

**Zadania sumaryczne lub dotyczące kontenera** Zadanie sumaryczne to zadanie, które znajduje się poniżej podzadań i zadań składowych. Zadanie sumaryczne nie wiąże się z żadnym nakładem pracy, ani nie posiada kosztów własnych. Zamiast tego nakład pracy i koszt zadania sumarycznego są sumą nakładu pracy i kosztu zadań składowych. Najwcześniejsza data rozpoczęcia zadań składowych jest używana jako data rozpoczęcia zadania sumarycznego, a najpóźniejsza data zakończenia zadań składowych jest używana jako data zakończenia. Możesz zmienić nazwę zadania sumarycznego, ale nie możesz zmodyfikować właściwości planowania dla nakładu pracy, dat i czasu trwania. Usunięcie zadania sumarycznego powoduje również usunięcie wszystkich jego zadań składowych. 

**Zadania węzłów typu liść** zadanie węzła typu liść reprezentuje w projekcie najbardziej szczegółowy pakiet roboczy. Węzeł typu liść ma szacowany wysiłek, zaplanowaną liczbę zasobów, planowaną datę rozpoczęcia i datę zakończenia oraz czas trwania. 

Można wykonać poniższe operacje na hierarchiach, aby umożliwić utworzenie hierarchii pracy lub jej rozkładu. 

**Nowe zadanie** Każde nowe zadanie, które utworzysz, jest automatycznie dodawane w węźle głównym, a do zadania jest automatycznie przypisywany numer SPP. Numer SPP reprezentuje poziom zadania w hierarchii. W przypadku zadań znajdujących się na pierwszym poziomie w obszarze zadania głównego projektu jest używany schemat numerowania 1, 2, 3 itd. W przypadku zadań znajdujących się poniżej pierwszego poziomu jest używany schemat numerowania 1.1, 1.2, 1.3 itd. Do każdego poziomu dodawanego pod poprzednim poziomem dodawany jest nowy ciąg liczb kropkowany. 

Obecnie nie można dostosować numeracji SPP. 

**Wcięcie zadania** Kiedy wprowadzasz wcięcie do zadania, staje się ono elementem podrzędnym zadania, które je poprzedza. Numer SPP nowego zadania podrzędnego jest automatycznie obliczany ponownie na podstawie numeru SPP jego nowego elementu nadrzędnego. Zadanie nadrzędne jest teraz zadaniem sumarycznym lub kontenerowym, dlatego staje się zestawieniem jego zadań składowych. 

> [!NOTE] 
> W przypadku tworzenia wcięć zadań w ramach zadania, które było węzłem liścia przed operacją wcięcia, nowo utworzone zadanie podsumowania utraci własne daty, nakład pracy i liczbę zasobów. Teraz jest używane podsumowanie wartości nowych zadań składowych. 

**Zmniejszenie wcięcia zadania** przy zmniejszeniu wcięcia zadania nie jest już zadaniem jego składnika względem jego elementu nadrzędnego. Numer SPP tego zadania jest automatycznie przeliczany, aby odzwierciedlić nowy poziom zadania w hierarchii. Nakład pracy, koszt i daty poprzedniego zadania nadrzędnego zadania są ponownie obliczane, aby wykluczyć to zadanie. 

**Przenieś w górę i Przenieś w dół** po kliknięciu pozycji **Przenieś w górę** i **Przenieś w dół** pozycja zadania jest zmieniana w hierarchię nadrzędną. Pozycja zadania nie wpływa na nakład pracy, koszt, daty ani czas trwania zadania. Jednak numer SPP zadania jest automatycznie ponownie obliczany, aby odzwierciedlić nową pozycję zadania.

### <a name="schedule-estimation"></a>Szacowanie harmonogramu

Planowanie planowania to zazwyczaj drugi krok w celu utworzenia struktury SPP. Zaleca się, aby po utworzeniu wszystkich zadań oszacować harmonogram został wykonany. Strona **Struktura podziału pracy** w rozwiązaniu Finance zawiera dwie sekcje. Panel górny jest przeznaczony do szacowania planowania, a w dolnym okienku są dostępne karty **Szacowane koszty i przychody**, które mogą być używane przy szacowaniu kosztów. 
**Współzależności zadań** W SPP można utworzyć poprzednią relację między zadaniami. Kiedy przypiszesz poprzednie zadania do zadania, to zadanie może zostać uruchomione dopiero po wykonaniu wszystkich poprzednich zadań. Planowana data rozpoczęcia zadania jest automatycznie ustawiana na ostatnią datę jej poprzednika. 

**Planowanie zadań** następujące czynniki określają planowanie zadań węzłów liścia:

-   Poprzedzające
-   Nakład pracy
-   Liczba zasobów
-   daty rozpoczęcia i zakończenia;

Data rozpoczęcia zadania węzła-liścia, które nie ma poprzedników, jest automatycznie ustawiana na datę rozpoczęcia planowania projektu. Czas trwania zadania węzła liścia jest zawsze obliczany jako liczba dni roboczych pomiędzy datą rozpoczęcia a datą zakończenia. 

*<strong><em>Reguły planowania</em></strong>* Gdy automatyczna pomoc w planowaniu jest włączona, do planowania zadań dla zadań węzła-liścia mają zastosowanie następujące reguły:

-   Daty rozpoczęcia i zakończenia zadania muszą być zawsze dniami roboczymi w kalendarzu planowania projektu.
-   Data rozpoczęcia zadania, które ma poprzedników, jest automatycznie ustawiana na najpóźniejszą datę zakończenia poprzedników.
-   Nakład pracy na zadanie jest obliczany automatycznie w następujący sposób:

Liczba osób × Czas trwania × Liczba godzin w standardowym dniu roboczym w kalendarzu projektu. 

W niektórych przypadkach możesz chcieć odstąpić od tych zasad. Automatyczne planowanie można wyłączyć, aby uniemożliwić Finance automatyczne ustawianie lub poprawianie wszystkich właściwości zadań węzłów liści. Po wprowadzeniu informacji dotyczących zadania powodującego naruszenie reguł planowania dla zadania jest wyświetlana ikona błąd planowania. Jeśli nie chcesz, aby były wyświetlane błędy planowania, kliknij opcję **Błędy planowania zostaną wyświetlone** w celu wyłączenia tej funkcji. 

> [!NOTE] 
> Wartości zadania sumarycznego lub kontenera są nadal obliczane jako suma wartości zadań składowych, niezależnie od tego, czy pomoc w automatycznym planowaniu jest włączona czy wyłączona. 

**Rozwiązywanie problemów dotyczących planowania** Gdy automatyczna pomoc w planowaniu jest włączona, błędy planowania prawdopodobnie nie wystąpią. Jeśli jednak automatyczne wyłączenie pomocy dotyczącej planowania zostanie wyłączone i ponownie włączone, ikony błędów planowania mogą pojawić się w SPP. 

**Naprawianie błędów planowania według zadania** kliknięcie dwukrotne ikony błędu harmonogramu dla określonego zadania powoduje wyświetlenie okna dialogowego z komunikatami dotyczącymi wszystkich błędów dotyczących harmonogramu danego zadania. Istnieje możliwość wybrania błędów planowania, które mają zostać naprawione dla danego zadania. 

**Trwa ustalanie wszystkich błędów planowania** Jeśli chcesz, aby Finance naprawiły wszystkie błędy planowania w WBS, w okienku akcji kliknij **Popraw wszystkie rozbieżności w harmonogramie**. 

> [!NOTE] 
> Ta funkcja może powodować znaczne modyfikacje struktury SPP. Błędy są poprawiane w następującej kolejności:

1.  Oszacowany nakład pracy na wszystkie zadania jest modyfikowany tak, że jego wartość jest równa wydajności zdefiniowanej w kalendarzu projektu.
2.  Data rozpoczęcia każdego zadania jest modyfikowana w taki sposób, aby zadanie rozpoczynało się po zakończeniu wszystkich zadań poprzedników.
3.  Data rozpoczęcia każdego zadania jest modyfikowana w celu usunięcia przerw w datach rozpoczęcia poprzedników.

### <a name="cost-estimation"></a>Oszacowanie kosztów

Jak wspomniano wcześniej w tym dokumencie, szacowanie kosztów dla każdego zadania węzła-liścia jest wprowadzane za pomocą karty **Szacowane koszty i przychody** w dolnym okienku strony **Struktura podziału pracy**. 

> [!NOTE] 
> Nie można modyfikować szacowania kosztów dla zadania sumarycznego i kontenera. Szacowane koszty zadania sumarycznego są równe sumie oszacowania kosztów zadań węzłów liścia. Szacowane koszty całkowite poszczególnych zadań są obliczane jako suma szacowanych kwot kosztów dla następujących typów transakcji:

-   Robocizna
-   Towar lub materiał
-   Wydatki

Typ transakcji **opłaty** jest używany do oszacowania przychodów opartych na opłatach. Taki typ transakcji nie ma składnika kosztów i dlatego nie jest brany pod uwagę przy oszacowaniu kosztów. 

Typ transakcji **akonto** jest używany do rejestrowania wartości sprzedaży z zakontraktowanym typem projektu o wartościach stałych. Ten typ transakcji nie jest również brany pod uwagę przy oszacowaniu kosztów. 

Kiedy szacujesz koszty robocizny, materiałowych i kosztów dla każdego zadania, należy przypisać kategorię projektu do kosztu szacowanego. 

**Szacowanie kosztów robocizny** W każdym zadaniu węzłów typu liść przypisujesz nakład pracy w godzinach i w kategorii domyślnej. Z tego powodu podczas konfigurowania harmonogramu dla zadania szacunek kosztów robocizny dla tego zadania jest automatycznie dodawany w domyślnej kategorii dla robocizny. Te oszacowania kosztów są wyświetlane na karcie **Szacowane koszty i przychód** w siatce **Szczegółów wierszy** danego zadania. W razie konieczności wykonania kolejnych oszacowań kosztów robocizny można dodać je na tej karcie. W przypadku zwiększania lub zmniejszania godzin w szacowaniu kosztów robocizny harmonogram zadania jest automatycznie przeliczany ponownie. 

**Szacunkowe koszty wydatku i materiałów** Na karcie **Szacowane koszty i przychód** można również oszacować koszt i koszty materialne zadania, jeśli wymagane są oszacowania. 

Koszt i cena sprzedaży w każdym wierszu oszacowania robocizny lub wydatku są oparte na ustawieniach zdefiniowanych dla każdej kategorii w tabelach kalkulacji cen w **Zarządzanie projektami i księgowanie** &gt; **Ustawienia** &gt; **Ceny**. W przypadku towarów koszt i cena sprzedaży są dodawane domyślnie z pozycji lub umów handlowych na stronie listy **Zwolnione produkty** w sekcji Zarządzanie informacjami o produktach.

## <a name="tracking-progress-on-the-wbs"></a>Śledzenie postępu w SPP
Niektóre branże śledzą postępy projektu względem struktury SPP na bardzo szczegółowym poziomie, podczas gdy inni użytkownicy śledzą postępy na wyższym poziomie SPP. W tej sekcji opisano sposób korzystania z śledzenia SPP w zakresie wymagań projektu. 

Finansowanie ma trzy widoki dla struktury SPP projektu: widok planowania, widok śledzenia nakładów i widok śledzenia kosztów.

### <a name="planning-view"></a>Widok planowania

W widoku planowania jest wyświetlane planowane i szacowane według planu bazowego informacje o harmonogramie i koszcie. Mimo że nie istnieją żadne funkcje umożliwiające śledzenie wersji i planu bazowego projektu SPP, wartości w tym widoku są przeznaczone do reprezentowania wersji planu bazowego. Sekcje szacowanie i szacowanie kosztów w tym temat opisują ten widok oraz sposób jego użycia w celu tworzenia SPP.

### <a name="effort-tracking-view"></a>Widok Śledzenie nakładu pracy

Widok Śledzenie wysiłku wyświetla śledzenie postępu zadań w SPP. Porównuje skumulowane rzeczywiste godziny pracy dla zadania z planowanymi godzinami pracy. Poniższe formuły zadają wartości w widoku śledzenia nakładów pracy:

-   Procent postęp = rzeczywisty nakład pracy do dnia dzisiejszego ÷ planowany nakład pracy dla zadania
-   Pozostały nakład pracy (określany również jako Prognoza do ukończenia \[PDU\]) = planowane wysiłki - rzeczywisty nakład pracy na dany dzień
-   Szacowane przy zakończeniu (SPZ) = pozostały nakład pracy + rzeczywisty nakład pracy do dnia dzisiejszego
-   Przewidywane odchylenie nakładu pracy = planowany nakład pracy — SPZ

W widoku śledzenia nakładu pracy jest wyświetlana projekcja odchylenia dla zadania w zależności od tego, czy wartość SPZ jest większa czy mniejsza od planowanego nakładu pracy:

-   Jeśli wartość SPZ przekracza planowany nakład pracy, zadanie jest rzutowane na czas dłuższy niż planowano i jest opóźnienie.
-   Jeśli wartość SPZ jest mniejsza niż planowany nakład pracy, zadanie jest rzutowane na czas krótszy niż planowano i praca posuwa się do przodu szybciej niż zaplanowano.

**Ponowna projekcja wysiłku kierownika projektu** Czasami kierownik projektu lub inna osoba, która śledzi postęp projektu, będzie musiała skorygować pierwotne oszacowania zadania. Zadanie może przyśpieszyć lub wydłużyć czas wolniejszy niż jest pierwotnie przewidziane z różnych powodów. Na przykład zakres został zmniejszony lub pracownicy z mniejszym doświadczeniem niż planowana pierwotnie. Prognozy to sposób postrzegania szacunków przez kierownika projektu na podstawie bieżącego stanu projektu. Zasadniczo nie należy zmieniać numerów według planu bazowego, ponieważ plan bazowy projektu stanowi dobrze opublikowany dokument zawierający harmonogram projektu i kosztorys, na który zgodzili się wszyscy interesariusze projektu. 

Istnieją dwa sposoby, w jakie kierownicy projektów mogą modyfikować nakład pracy związany z zadaniami:

-   Zmodyfikuj pozostały nakład pracy, który jest automatycznie ustawiany, aby zaktualizować rzeczywisty pozostały nakład pracy w zadaniu.
-   Zmodyfikuj procent postępu, który jest automatycznie ustawiany, aby zaktualizować rzeczywisty postęp zadania.

Obie z tych metod powoduje ponowne obliczenie wartości PDU zadania, SPZ i wartości procentowej postępu oraz przewidywane odchylenie nakładu pracy nad zadaniem. SPZ, PDU i procent postępu w zadaniach sumarycznych są również ponownie obliczane, a ich przewidywana wariancja nakładu pracy jest aktualizowana. 

**Zmodyfikowany nakład pracy na zadania sumaryczne** Możesz modyfikować nakład pracy związany z zadaniami sumarycznymi lub kontenerami. Niezależnie od tego, czy zmodyfikujesz te wartości, używając pozostałego wysiłku, czy procentu postępu w zadaniach sumarycznych, obliczenia są wykonywane automatycznie w następującej kolejności:

1.  Wartości SPZ, ETC i procent postępu są obliczane względem zadania.
2.  Nowe wartości SPZ są rozkładane na zadania podrzędne w takiej samej proporcji jak w oryginalnej ilości SPZ.
3.  Nowe zadanie SPZ w każdym węźle typu liść jest obliczane.
4.  Współczynnik pozostałego czasu i procent postępu jest przeliczany na wszystkie przydziały, których dotyczy zadanie podrzędne, na podstawie nowej wartości SPZ. Różnica nakładów pracy jest również przeliczana.
5.  SPZ zadań sumarycznych również zostanie ponownie obliczona z poziomu węzłów liści.

Kliknij opcję **Rozwiń do poziomu** w widoku śledzenie nakładów pracy, aby ustawić poziom śledzenia i utrzymywania struktury SPP. Kody SPP są automatycznie rozwijane na tym poziomie w widoku śledzenie nakładów pracy po jego otwarciu.

### <a name="cost-tracking-view"></a>Widok śledzenia kosztów

W widoku śledzenie kosztów jest wyświetlane Śledzenie zużycia kosztów dla określonego zadania. W tym widoku koszt rzeczywisty, który został zaspędzony względem daty rozpoczęcia zadania, jest porównywany z planowanym kosztem zadania. Poniższe formuły zadają wartości w widoku śledzenia kosztów:

-   Procent zużytego kosztu = koszt rzeczywisty poniesiony do dnia ÷ planowany koszt zadania
-   Koszt do zakończenia (CTC) = planowany koszt — rzeczywisty koszt poniesiony do dnia
-   Szacowana z zakończeniem (SPZ) = CTC + koszt rzeczywisty do dnia
-   Prognozowane odchylenie kosztu = koszt planowany – SPZ

Widok Śledzenie kosztów wyświetla prognozę odchylenia kosztu zadania na podstawie tego, czy SPZ jest większy, czy mniejszy niż planowany koszt:

-   Jeśli SPZ jest wyższy niż planowany koszt, przewiduje się, że zadanie zużyje więcej pieniędzy niż pierwotnie planowano i przekracza budżet.
-   Jeśli SPZ jest niższy niż planowany koszt, przewiduje się, że zadanie zużyje mniej pieniędzy niż pierwotnie planowano i nie przekracza budżetu.

**Ponowna prognoza kosztów kierownika projektu** Kierownicy projektów muszą używać CTC, aby skorygować pierwotny kosztorys zadania. Menedżer projektu może zmodyfikować wartość CTC na koszt wymagany do wykonania zadania. W przypadku zmodyfikowania wartości CTC, CTC, SPZ i procent zużytego kosztu i przewidywane odchylenie kosztów dla zadania są ponownie obliczane. SPZ, PDU i procent kosztów zużytych w zadaniach sumarycznych są również ponownie obliczane, a ich przewidywane odchylenie kosztów jest aktualizowane. 

> [!NOTE] 
> W przypadku modyfikowania zadania SPP w widoku śledzenia nakładów pracy CTC, SKZ, procent zużytego kosztu i przewidywane odchylenie kosztów są ponownie obliczane w widoku śledzenia kosztów. Jednak korekty kosztów nie wpływają na wartości w widoku Śledzenie nakładu pracy, ponieważ koszt według typu transakcji (robocizna, materiał lub wydatek) lub kategorii projektu nie jest korygowany. 

**Rewizja prognozy kosztów zadań sumarycznych** Możesz skorygować koszty zadań sumarycznych, a obliczenia są wykonywane automatycznie w następującej kolejności:

1.  SPZ, CTC i procent kosztów zużytych na zadanie są ponownie obliczane.
2.  Nowy SPZ jest rozdzielany do zadań podrzędnych w takiej samej proporcji, jak oryginalny SPZ dotyczący zadań.
3.  Nowe SPZ dla każdego zadania są obliczane.
4.  CTS i procent zużytych kosztów są ponownie obliczane dla zaatakowanych zadań podrzędnych na podstawie wartości SPZ. Różnica kosztów jest również przeliczana.
5.  Dla wszystkich zadań sumarycznych SPZ jest przeliczana na podstawie tej zmiany.

Kliknij opcję **Rozwiń do poziomu** w widoku śledzenie kosztów, aby ustawić poziom śledzenia i utrzymywania struktury SPP. SPP jest rozwijany do tego poziomu w widoku Śledzenie kosztów po każdym otwarciu.

### <a name="earned-value-management"></a>Zarządzanie wartościami wypracowanymi

Możesz użyć metody wartości wypracowanej (EVM) do śledzenia postępu projektu. Możesz przeglądać wskaźniki wartości wypracowanej w Centrum ról kierownika projektu. Składnik wykresu wartości wypracowanej przedstawia rozłożone w czasie wartości planowanej wartości i rzeczywistego kosztu. Wartość wypracowana od bieżącej daty jest wyświetlana jako punkt. Dane wartości wypracowanej z danymi okresowymi nie są obecnie dostępne. 

Faza czasu na wykresie wartości wypracowanej jest wyświetlana według tygodni lub miesięcy. W tej sekcji opisano trzy filary EVM: wartość planowana, wartość wypracowana i koszt rzeczywisty. 

**Planowana wartość** Teoria EVM stwierdza, że wykres planowanej wartości przedstawia tempo, w jakim zespół projektu planował uzyskać wartość projektu. 

Finanse stosuje regułę zarobków 0: 100, kiedy kreśli planowaną wartość. Ta reguła powoduje, że wartość zadania jest księgowana w zadaniu na podstawie daty jego zakończenia. Wartość nie zostanie zaksięgowana do momentu wykonania zadania 100 procent. 

W przystawce Zarządzanie projektami i księgowanie wprowadź datę zakończenia węzłów liści i planowany koszt dla niego. Gdy wykres wartości planowanej jest wyświetlany według tygodni, wartość planowana jest podsumowywana według tygodni dla wszystkich zadań węzłów-liści na czas trwania projektu. 

**Wypracowana wartość** Teoria EVM stwierdza, że wykres wypracowanej wartości przedstawia tempo, w jakim zespół projektu w rzeczywistości uzyskuje wartość projektu. 

Finanse stosuje regułę zarabiania 0: 100, gdy jego wykresy uzyskały wartość. Ta reguła powoduje, że wartość zadania jest księgowana w zadaniu na podstawie daty jego zakończenia. Wartość nie zostanie zaksięgowana do momentu wykonania zadania 100 procent. 

Kiedy obliczana jest wartość wypracowana, jest brana pod uwagę współczynnik postępu każdego zadania. Zgodnie z regułą zarabiania 0: 100 do obliczenia wartości wypracowanej na koniec tego okresu brane są pod uwagę tylko zadania ukończone w danym okresie. Wartość wypracowana w projekcie jest obliczana dla wszystkich zadań wykonanych podczas tworzenia wykresu. 

> [!NOTE] 
> Obecnie system śledzenia SPP nie zawiera struktur danych służących do przechowywania wartości procentu historycznego postępu na każde zadanie. Z tego względu wartość wypracowana może być raportowana tylko od czasu przetwarzania kostki wielowymiarowej. Należy regularnie przetwarzać moduł w celu zaktualizowania danych wartości wypracowanej wyświetlanych w widoku role użytkownika. 

**Koszt rzeczywisty** Teoria EVM stwierdza, że wykres kosztów rzeczywistych przedstawia tempo, w jakim wydawane są pieniądze na projekt. 

Transakcje zaksięgowane w projekcie są używane do wykreślania wiersza kosztów rzeczywistych. Koszty są sumowane według daty. Te dane są następnie używane do grafowania rzeczywistych kosztów według tygodnia lub miesiąca na wykresie wartości wypracowanej.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Korzystanie z pojęć dotyczących planowanej wartości, wartości wypracowanej i kosztu rzeczywistego

**Odchylenie zaplanowania** Podczas planowania tworzysz prognozę pracy na osi czasu. Z tego względu planowana wartość to szybkość wykonywania zadań terminarza projektów, które mogą zostać wykonane w projekcie. Po zakończeniu projektu praca jest realizowana i realizowana jest wartość projektu. Porównując planowaną wartość z wartością wypracowaną, można wyświetlić informacje o postępie prac nad projektem. W wyniku tego porównania jest określane odchylenie planowanie. 

Jeśli planowana wartość dla okresu przekracza wartość wypracowaną, ilość pracy wykonanej w projekcie jest mniejsza niż planowana. Z tego powodu projekt jest opóźniony względem harmonogramu. Ponieważ planowana wartość i Wartość wypracowana są wyrażone w terminologii walutowej, na czas zwłoki w projekcie jest również nadana wartość pieniężna. 

Jeśli planowana wartość dla okresu nie przekracza wartości wypracowanej, ilość pracy wykonanej w projekcie jest większa niż planowana. Z tego powodu projekt jest wyprzedza harmonogram. Ten czas realizacji jest również podawany jako wartość pieniężna.

**Odchylenie kosztów** Ponieważ wartość wypracowana używa kosztu własnego jako mnożnika, wartość wypracowana wskazuje koszt pracy wykonanej w projekcie. W miarę postępu projektu dziennik transakcji dostarcza zapis pieniędzy faktycznie wykorzystanych w tym projekcie. Porównując wartość wypracowaną z kosztem rzeczywistym, można wyświetlić ilość pieniężną, która jest naliczana w stosunku do wartości wypracowanej. W wyniku tego porównania jest określane odchylenie kosztu. 

Jeśli koszt rzeczywisty spędzony za dany okres jest większy niż wartość wypracowana, większa liczba pieniędzy została wydana niż zarobiono. Z tego powodu projekt przekracza budżet. 

Jeśli koszt rzeczywisty spędzony za dany okres jest mniejszy niż wartość wypracowana, większa liczba pieniędzy została zarobiona niż wydana. Z tego powodu projekt jest poniżej budżetu.

## <a name="wbs-templates"></a>Szablony SPP
Funkcja szablony SPP może służyć do tworzenia standardowych szablonów projektów. Jeśli projekty oferowane przez firmę pociągają za sobą dużą liczbę powtarzalnych prac, warto rozważyć utworzenie szablonu SPP. 

Użytkownik może utworzyć szablon SPP z poziomu SPP istniejącego projektu, dzięki czemu wiedzy i sprawdzone metody postępowania zebrane podczas planowania tego projektu mogą być ponownie użyte w podobnych projektach w przyszłości. Zdarza się jednak, że zapisanie całej struktury SPP jako szablonu jest niewskazane. Z tego powodu można również tworzyć szablony na podstawie części SPP danego projektu.

### <a name="saving-a-projects-wbs-as-a-template"></a>Zapisywanie SPP projektu jako szablonu

Po utworzeniu szablonu możesz zaimportować go do SPP nowego projektu w węźle głównym lub w dowolnym zadaniu w SPP projektu.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importowanie szablonu SPP do SPP projektu

Podczas importowania zadań zadania znajdujące się w szablonie są zorganizowane w zależności od daty rozpoczęcia zadania, na którym zostały zaimportowane. Podczas importu relacje poprzedników w zadaniach związanych z szablonami służy do obliczania dat rozpoczęcia importowanych zadań. Standardowy kalendarz pracy projektu docelowego jest stosowany do obliczania dat zakończenia zaimportowanych zadań, dzięki czemu dni robocze i standardowe godziny pracy zdefiniowane w kalendarzu pracy bieżącego projektu są zachowywane. 

Kwoty kosztów i ceny sprzedaży w wierszach szacowania są stosowane w celu zagwarantowania, że cena określona w projekcie lub kontrakcie projektu ma prawidłowe daty.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Różnice między SPP projektu a szablonem SPP

-   Zadania w szablonach SPP nie mają dat rozpoczęcia i zakończenia.

Dni robocze i inne niż robocze nie są ustawiane dla szablonów SPP.

-   Szablony SPP zawsze używają kalendarza planowania, który jest skonfigurowany jako domyślny kalendarz dla wszystkich projektów.

Domyślny kalendarz planowania jest używany wyłącznie w celu wyszukania godzin w standardowym dniu roboczym.

-   Relacje poprzedników nie jest kopiowany do szablonu SPP.

Ponieważ szablony SPP nie mają dat, logika daty rozpoczęcia oparta na dacie końcowej poprzedników nie jest wymagana.

-   Wiersz szacowania kosztów robocizny jest tworzony automatycznie w momencie utworzenia zadania w szablonie SPP. Cena sprzedaży i kwota kosztu są kopiowane z wybranego pracownika.

Koszty wydatkowe i towarowe można tworzyć ręcznie, tak jak w przypadku, gdy mogą ono zawierać kody SPP projektu.

-   Błędy planowania są wyświetlane, gdy w poniższym wzorze istnieją odstępstwa:

Nakład pracy = liczba zasobów × czas trwania × liczba godzin w standardowym dniu roboczym 

Możesz poprawić wszystkie błędy harmonogramu w tym samym czasie, klikając przycisk **Popraw wszystkie błędy planowania**. 

Błędy planowania można również skorygować osobno, klikając ikonę ostrzeżenia dla każdego zadania.





[!INCLUDE[footer-include](../includes/footer-banner.md)]