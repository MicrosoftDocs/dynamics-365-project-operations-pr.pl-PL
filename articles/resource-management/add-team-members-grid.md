---
title: Dodawanie członków zespołu z siatki członków zespołu
description: W tym temacie zamieszczono informacje dotyczące sposobu zarządzania zasobami członków zespołu.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 0f975d295b4c0ccef9827767beabd32ffd761faa
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897734"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Dodawanie członków zespołu z siatki członków zespołu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations zawiera pulpit nawigacyjny menedżera zasobów umożliwiający graficzne przeglądy popytu i wykorzystania zasobów w całej organizacji. Korzystając z wykresów na tym pulpicie nawigacyjnym, można wizualizować następujące informacje:

- **Zapotrzebowanie na zasoby**: na wykresie **Aktywne żądania zasobów** przedstawiono zasoby, które zostały przesłane. Zasoby są agregowane według ról lub projektów.
- **Nieprzesłane zapotrzebowanie na zasoby**: wykres **Nieprzydzielone zapotrzebowanie na zasoby** pokazuje wszystkie wymagania zasobu, które nie zostały przesłane. Ten wykres ułatwia to menedżerom zasobów wyświetlanie zapotrzebowania, które nie jest firmą i może być przesłane za pośrednictwem żądania zasobu.
- **Wykorzystanie do rozliczenia za ubiegły tydzień**: wykres **Wykorzystanie według roli** pokazuje procent rzeczywistego wykorzystania zasobu do rozliczenia według roli względem docelowego wykorzystania według roli, które podlega rozliczeniu.

    > [!NOTE]
    > Aby wykres **Wykorzystanie według roli** był dostępny, należy utworzyć zadanie, które uruchamia przepływ pracy **UpdateRoleUtilization**. To zadanie cykliczne jest uruchamiane co siedem dni w celu obliczenia wykorzystania do zafakturowania przez ostatnie siedem dni. Wyniki są agregowane według ról.

## <a name="manage-project-team-members"></a>Członkowie zespołu zarządzania projektem

Menedżerowie projektów mogą używać pulpitu nawigacyjnego menedżera zasobów do zarządzania zasobami w projektach. Na przykład użytkownicy mogą dodawać członków zespołu bezpośrednio do projektu i rezerwować członków zespołu, aby spełnić wymagania dotyczące zasobów przechwycone przez zasób ogólny.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodawanie członka zespołu bezpośrednio do projektu

Aby dodać członka zespołu bezpośrednio do projektu, w formularzu **projekty** na karcie **zespół** wybierz opcję **nowy**. Zostanie wyświetlone okno dialogowe **szybkie tworzenie: członek zespołu projektu**. W tym oknie dialogowym można wykonać następujące zadania:

- **Zarezerwowanie nazwanego zasobu**: w polu **Zasób, który można zarezerwować** wybierz nazwę zasobu. Następnie wybierz rolę, ustaw okres i wybierz metodę alokacji. Wybrany nazwany zasób jest dodawany do projektu przy użyciu wybranej metody alokacji i kalendarza zasobów.
- **Dodaj zasób ogólny**: pozostaw puste pole **zasobu, który można zarezerwować**, a następnie wybierz rolę, ustaw okres i wybierz preferowaną metodę alokacji. Zasób ogólny jest dodawany do zespołu jako element zastępczy. Element zastępczy zawiera wzorzec popytu, który jest używany do tworzenia ksiąg nazwanych zasobów w zespole. Wymóg jest składany zgodnie z kalendarzem projektu.
- **Dodaj nazwany zasób do zespołu bez zużywania dyspozycyjności zasobu**: w polu **zasobu, który można zarezerwować** wybierz zasób. Wybierz okres i zaznacz **Brak** jako metodę alokacji. Zasób jest dodawany do zespołu, ale jego dyspozycyjność nie jest wykorzystywana poprzez rezerwację.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezerwowanie członka zespołu w celu spełnienia wymagań dotyczących zasobów dla zasobu ogólnego

WProject Operations można zarezerwować zasób ogólny względem zespołu projektu. Użytkownik może również określić rolę, wymaganą wydajność i sposób jej dystrybuowania. W zapotrzebowaniu na zasoby można określić atrybuty, które są skojarzone z zasobem ogólnym. Do atrybutów tych zalicza się wymagane kwalifikacje, preferowaną jednostkę organizacyjną i preferowane zasoby.

Wykonaj następujące kroki, aby określić wymagane kwalifikacje dla zasobu ogólnego w przypadku dewelopera.

1. W formularzu **projekty** na karcie **zespół** wybierz opcję **nowy**, aby zarezerwować zasób ogólny.
2. W widoku **wszyscy członków zespołu** w kolumnie **wymagania dotyczące zasobu** wybierz łącze, aby dodać wymagane umiejętności dla zasobu ogólnego.
3. W wyświetlonym formularzu **Wymagania dotyczące zasobu** w siatce **umiejętności** wybierz wielokropek (**...**), a następnie wybierz opcję **Dodaj nową cechę wymagania**, aby dodać wymagane umiejętności dla swojego dewelopera.
4. W wyświetlonym formularzu **szybkie tworzenie: cecha**, w polu **cecha** wybierz wymagane umiejętności.
5. W polu **Wartość klasyfikacji** wybierz poziom biegłości dla tej umiejętności. 
6. W polu **Wymaganie zasobu** należy ustawić wymagania dotyczące zasobów źródłowych z jednostek organizacyjnych lub nawet nazwanych zasobów. Kiedy skończysz, wybierz **Zapisz**.
7. W formularzu **Zapotrzebowania zasobu** wybierz pozycję **Rezerwuj**, aby spełnić wymagania dotyczące zasobu. Można też wybrać zasób ogólny w siatce **wszystkie członków zespołu**, a następnie wybrać opcję **Rezerwuj**.

    > [!NOTE]
    > W tym przykładzie jest 40 wymaganych godzin, ale nie ma rzeczywistych zarezerwowanych godzin, ponieważ zasoby ogólne nie mają rezerwacji. Oprócz tego nie ma przydzielonych godzin, ponieważ zasób ogólny został dodany bezpośrednio do zespołu, zamiast dodania w ramach przypisania zadania.

    W formularzu **asystent planowania** można filtrować dostępne zasoby według wymagań określonych w zapotrzebowaniu zasobu. Zasoby są sortowane zgodnie z parametrami sortowania określonymi na tablicy harmonogramu.

   Oto niektóre z najczęściej używanych filtrów:

    - **Charakterystyki wraz z oceną**: Filtruj według kwalifikacji, certyfikatów i innych cech zasobów, a także oceny biegłości.
    - **Role**: Filtruj według ról domyślnych przypisanych do zasobów, które można rezerwować.
    - **Jednostki organizacyjne**: Filtruj zasoby możliwe do zarezerwowania według jednostek organizacyjnych, do których są przypisane.

8. Jeśli wyniki pierwszego wyszukiwania wymagania nie są zadowalające, można zmienić kryteria filtrowania. Rozwiń okienko **widoku filtra** po lewej stronie, a następnie wybierz pozycję **Wyszukaj** w celu wyszukania dodatkowych zasobów. Aby zmienić sposób sortowania wyników, wybierz **Sortuj**.
9. Wybierz zasoby według zapotrzebowania określonego w zapotrzebowaniu, tak jak to pokazano u górnej części siatki. Użytkownik może wyczyścić wybrane komórki siatki i zostawić otwartą dyspozycyjność zasobu. Tylko jeden zasób jednocześnie może być zaznaczony jako zarezerwowany.
10. Wybierz **Rezerwuj**, aby zarezerwować wybrany zasób i pozostaw otwartą tablicę harmonogramu, aby mieć możliwość wybrania dodatkowych zasobów. Możesz również wybrać opcję **Zarezerwuj i wyjdź**, aby zarezerwować wybrany zasób i zamknąć tablicę harmonogramu.
11. Powróć do widoku **wszystkich członków zespołu**. W siatce zauważ, że zasób ogólny został zastąpiony przez nazwany zasób, a 40 godzin zostało zarezerwowanych dla tego zasobu.

    > [!NOTE]
    > Nie są wyświetlane przypisane godziny, ponieważ są one zarezerwowane bezpośrednio w zespole. Nie zostały one zarezerwowane przy użyciu przypisania zadania.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Przypisywanie zasobów ogólnych do zadań i generowanie wymagań zasobów

W Project Operations można tworzyć zadania i przypisywać im zasoby ogólne. Zapotrzebowanie zasobu może być następnie reprezentowane przez symbole zastępcze podczas szacowania harmonogramu i kwot. Następnie można wygenerować zapotrzebowania zasobów dla zasobów ogólnych i zrealizować je.

1. W formularzu **projekty**, na karcie **harmonogram** wybierz pozycję **Dodaj**, aby utworzyć zadanie.
2. W polu **zasoby** wybierz symbol **selektora zasobów**. Zostanie wyświetlony selektor zasobów zawierający listę istniejących członków zespołu danego projektu.
3. Wprowadź nazwę nowego zasobu ogólnego i wybierz pozycję **Utwórz.**
4. W oknie dialogowym **szybkie tworzenie: członek zespołu projektu**, które zostanie wyświetlone, w polu **Rola** wybierz rolę dla zasobu ogólnego. 
5. W polu **Jednostka zasobów** wybierz jednostkę organizacyjną dla zasobu ogólnego. Następnie wybierz opcję **Zapisz**. Ogólny członek zespołu teraz jest przypisany do zadania.

   Na karcie **zespół** zobaczysz nowego ogólnego członka zespołu. Zauważ, że ma on tylko przypisane godziny. Te godziny to suma wszystkich zadań przydzielonych do ogólnego członka zespołu. Ogólny członek zespołu nie ma jeszcze wymaganych godzin ani wymagania zasobu.

6. Teraz możesz przypisać ogólnego członka zespołu do innych zadań za pomocą selektora zasobów.

   Po zakończeniu przypisywania ogólnego zasobu do zadań można wygenerować zapotrzebowanie zasobu dla zasobu ogólnego.

7. Na karcie **zespół** wybierz zasób ogólny i wybierz opcję **Generuj zapotrzebowanie.** Kiedy zapotrzebowanie jest generowane, ogólny członek zespołu będzie dysponować godzinami i łączem dotyczącym wymagania zasobu.

  Po zarezerwowaniu nazwanego zasobu zasób ogólny jest usuwany z zespołu i zastępowany zasobem o nazwie. Na karcie **harmonogram** przydział zasobu ogólnego zostanie usunięty i zastąpiony nazwanym zasobem.

  > [!NOTE]
  > To zachowanie występuje tylko wtedy, gdy nazwany zasób jest w pełni zarezerwowany dla wymagania zasobu ogólnego. Gdy zasób o nazwie częściowo zastępuje zapotrzebowanie na zasób ogólny lub wiele nazwanych zasobów zastępuje zapotrzebowanie na zasób ogólny, zasób ogólny pozostaje przydzielony do zadania.

Project Operations nie przypisuje obu zasobów do zadania, ponieważ to zachowanie mogłoby spowodować wygenerowanie mniej przewidywalnego harmonogramu. W tym prostym przykładzie łatwo podzielić godziny równo na dwa zasoby. Jednak w bardziej złożonych scenariuszach obejmujących wiele zadań i wiele zasobów, PSA musi wprowadzić założenia dotyczące alokacji rezerwacji odbieranych przez wiele zasobów na wiele zadań.

W tym scenariuszu menedżer projektu jest odpowiedzialny za analizowanie wielu rezerwacji i przypisywanie ich według potrzeb. Aby alokować rezerwacje, menedżer projektu przypisuje zadania z zasobów ogólnych do nazwanych zasobów, a następnie korzysta z widoku **uzgodnienie** w celu upewnienia się, że alokacja jest zgodna z rezerwacjami.

### <a name="edit-a-resource-requirement"></a>Edycja wymagania zasobu

Po utworzeniu wymagania zasobu menedżer projektu lub menedżer zasobów może edytować szczegóły, aby uściślić kryteria wyszukiwania podczas korzystania z tablicy harmonogramu. Aby edytować wymagania zasobu, wykonaj następujące kroki.

1. W formularzu **projekty**, na karcie **zespół** wybierz łącze do dowolnego wymagania zasobu ogólnego.
2. W wyświetlonym formularzu **Wymaganie zasobów** wprowadź informacje w niezbędnych polach

   W formularzu **Wymagania zasobów** menedżer projektu lub menedżer zasobu może także zdefiniować umiejętności, role i preferencje dotyczące zasobów, a także preferowaną jednostkę organizacyjną.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aktualizacja rezerwacji zasobów po ich zarezerwowaniu w projekcie

Po dodaniu ogólnego lub nazwanego zasobu do zespołu projektu można zmienić rezerwacje zasobu.

1. W formularzu **projekty**, na karcie **zespół**, wybierz opcję członka zespołu, a następnie wybierz **Obsługa rezerwacji**.
 
   Zostanie wyświetlona tablica harmonogramu, która pokazuje rezerwacje członków zespołu projektu. Rozwiń rekord członka zespołu w celu wyświetlenia godzin zarezerwowanych dla tego projektu i innych projektów, które zużywają dyspozycyjność członka zespołu.

2. Zaznacz i przeciągnij rezerwację, aby ją wydłużyć lub skrócić. Zostanie otwarte okno dialogowe **Utwórz rezerwację zasobu**, które umożliwia dostosowanie rezerwacji.
3. Kliknij prawym przyciskiem myszy rezerwację. Można użyć menu skrótów do wykonania następujących czynności:

    - Zmiana stanu rezerwacji
    - Edycja rezerwacji
    - Zastępowanie zasobu w zespole projektu

### <a name="change-the-booking-status"></a>Zmiana stanu rezerwacji

Można zmienić domyślny lub niestandardowy stan rezerwacji.

W Project Operations dostępne są trzy stany:

- **Anulowany**: ten stan powoduje anulowanie rezerwacji zasobu i zwolnienie dyspozycyjności zasobu.
- **Ostateczna rezerwacja**: zużywa dyspozycyjność zasobu. Rezerwacja zazwyczaj jest tym stanem po otworzeniu **Obsługa rezerwacji** w siatce **wszystkich członków zespołu** w formularzu **projekty**.
- **Rezerwacja wstępna**: dodaje zasobu do zespołu, ale nie zużywa dyspozycyjności zasobu. Ten stan oznacza, że zasób został zarezerwowany do potencjalnej pracy, ale jest nadal dyspozycyjny, gdyby był potrzebny do wykonywania innych zadań. W widoku ogólnej dostępności zasobu rezerwacje wstępne mają inny stan niż rezerwacje ostateczne.
- **Zaproponowano**: reprezentuje propozycję menedżera zasobów lub projektu dotyczącą zasobu. Propozycje nie zużywają dyspozycyjności zasobu, a zasób nie jest dodawany do zespołu projektu. Aby ostatecznie zarezerwować zasób w zespole, menedżer projektu musi zaakceptować propozycję.

### <a name="submit-resource-requests"></a>Przesyłanie żądań zasobu

Żądania zasobu są używane do zgłaszania popytu lub wymagania zasobu, które musi zostać zrealizowane przez menedżera zasobów. W przypadku zasobu ogólnego, który już znajduje się w zespole, można przesłać żądanie zasobu bezpośrednio. Żądanie zasobu może być zrealizowane na dwa sposoby:

- Menedżer zasobów bezpośrednio wypełnia żądanie. W tym przypadku zasób ogólny jest zastępowany rezerwacją ostateczną, która ma nazwany zasób.
- Menedżer zasobów proponuje zasób menedżerowi projektu, a Menedżer projektu zatwierdza lub odrzuca zaproponowany zasób.

#### <a name="direct-fulfillment-of-resource-requests"></a>Bezpośrednie zrealizowanie żądań zasobów

Po wygenerowaniu wymagania zasobu menedżer projektu może przesłać żądanie zasobu ogólnego, wybierając zasób, a następnie wybierając opcję **przesyłania żądania**. Komentarze dotyczące zasobu można podać menedżerowi zasobów, który realizuje realizację żądania. Po przesłaniu żądania pole **stanu** dla członka zespołu zostanie zmienione na **przesłane.** Gdy menedżer zasobów realizuje żądanie, ogólny członek zespołu zostaje zastąpiony zasobem nazwanym w siatce **wszystkich członków zespołu**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Korzystanie z propozycji zasobów na potrzeby żądań zasobów

Zamiast bezpośredniego zarezerwowania zasobu dla żądania zasobu menedżer zasobów może zaproponować zasób menedżerowi projektu. Menedżer zasobów może użyć tej opcji, jeśli dokładne dopasowania dotyczące zapotrzebowań nie są dostępne. Gdy menedżer zasobów proponuje dany zasób, menedżer projektu widzi, że pole **stanu** dla ogólnego członka zespołu jest zmienione na **Wymaga weryfikacji**.

Można wyświetlić zasób zaproponowany wraz z wizualizacją skutków rezerwacji propozycji. 

1. Kliknij dwukrotnie członka zespołu, który ma stan **Konieczny przegląd**. 
2. Wybierz kartę **proponowane zasoby**.
3. Zaznacz pole wyboru **Zaakceptuj wszystkie propozycje**, aby zaakceptować wszystkie proponowane zasoby, lub **Odrzuć wszystkie propozycje**, aby je odrzucić. Jeśli zaakceptujesz zaproponowane zasoby, są one zarezerwowane w projekcie jako członkowie zespołu i zastępują zasoby ogólne.

> [!NOTE]
> Użytkownik musi akceptować lub odrzucać wszystkie proponowane zasoby. Nie można częściowo zaakceptować lub odrzucić.

### <a name="substitute-a-resource-on-the-project-team"></a>Zastępowanie zasobu w zespole projektu

Czasami menedżer projektu musi zastąpić zarezerwowanego członka zespołu w projekcie.

1. W formularzu **projekty** na karcie **zespół** wybierz zasób, który wymaga zastąpienia, a następnie wybierz **Obsługa rezerwacji**.
2. Rozwiń zasób, aby wyświetlić projekty, do których jest przypisany.
3. Kliknij prawym przyciskiem myszy projekt, a następnie wybierz polecenie **Zastąp zasób**.
4. Jeśli znasz zasób, którym chcesz zastąpić bieżący zasób, wybierz lub wpisz nazwę, a następnie wybierz opcję **ponowne przypisanie**.

Lub , aby wyszukać zasób, należy wykonać następujące kroki.

1. Wybierz pozycję **Znajdź zastępstwo**.

   Asystent harmonogramu zwraca listę dostępnych zastępców. W Asystencie planowania można dalej filtrować dostępne zasoby, aby znaleźć odpowiednie zastępstwo.

2. Aby zastąpić zasób, wybierz żądany zasób, a następnie wybierz **Zastąp**.   

   Rezerwacje i przypisania są zastępowane nowym zasobem.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Uzgadnianie rezerwacji i przypisań członka zespołu

Członkowie zespołu, rezerwacje i przydziały są luźno sprzężone. Innymi słowy, zasoby mogą mieć przydziały, ale mogą nie mieć rezerwacji lub mogą mieć rezerwacje bez przypisań. Najlepiej, kiedy rezerwacje i przypisania w projekcie są zgodne, bo wtedy zasoby mają zatwierdzoną dyspozycyjność do wykonania przypisanych im zadań. Jednak rezerwacje mogą być oparte na dostępności, a czasy zadań mogą ulec zmianie w miarę kontynuowania projektu. Z tego względu swobodne powiązanie rezerwacji i przypisań zapewnia elastyczność.

Project Operations oferuje kartę **Uzgadnianie**, która pozwala menedżerom projektu uzgadniać rezerwacje członków zespołu i ich przypisania w zespołach projektów.

Na karcie **Uzgadnianie** są wyświetlane rezerwacje i przypisania na wszystkich poziomach szczegółowości, aż do poszczególnych zadań. W komórkach widać godziny, które reprezentują okresy od miesięcy aż po dni.

Na karcie przedstawiono również ogólną sumę netto projektu wraz z kolumną sumy.

Dla każdego zasobu karta oblicza różnicę między rezerwacjami członka zespołu w projekcie a zestawieniem zadań przypisanych temu członkowi zespołu. Najlepiej, aby różnica wynosiła 0 (zero). Innymi słowy nie powinno być żadnej różnicy między rezerwacjami zasobu a jego przypisaniami zadań. Różnice są oznaczone kolorami i zacienione, aby zwrócić uwagę na dwa warunki:

- **Niedobór rezerwacji**: powstaje wtedy, gdy zasób ma więcej przypisań, niż rezerwacji. Ponieważ dyspozycyjność nie została zarezerwowana, menedżer projektu może naprawić tę sytuację poprzez rozszerzenie rezerwacji zasobu w sposób pokrywający niedobór.
- **Nadmiarowe rezerwacje**: nadmierne rezerwacje występują, gdy zasób zarezerwowano do projektu, ale nie przypisano go do zadań. Ten warunek może być akceptowalny w przypadkach, gdy zasób został zarezerwowany w projekcie przed przydziałem zadania. Jednak w innych przypadkach być może nie jest planowane przypisanie zasobu do zadań. Wtedy menedżer projektu powinien rozważyć anulowanie rezerwacji zasobu, tak aby jego dyspozycyjność można było wykorzystać w innym projekcie.

W niektórych przypadkach, kiedy oglądasz czas na wyższym poziomie niż poziom dnia (np. na poziomie miesiąca), może się pojawić różnica netto zasobu równa zero. Innymi słowy, rezerwacje = przydziały. Natomiast w poziomie Tydzień można zauważyć, że istnieją przypisania równe 0 (zero) godzin i rezerwacje 40 godzin w pierwszym tygodniu miesiąca oraz przypisania 40 godzin i rezerwacje równe 0 (zero) godzin w drugim tygodniu miesiąca. Ogólnie rzecz biorąc, rezerwacje i przydziały są uzgadniane, ale różnią się od siebie między tygodniami.

Po wyświetleniu wyższych poziomów czasu na karcie **Uzgadnianie** widać wskaźnik komórki informujący o różnicach na niższych poziomach czasu. Dwukrotne kliknięcie komórki umożliwia powiększenie i wyświetlenie różnicy. Następnie kliknij prawym przyciskiem myszy, aby pomniejszyć. Zaznaczając zasób, a następnie klikając **Następna różnica** na pasku narzędzi siatki można przejść do następnej różnicy między rezerwacjami a przydziałami danego zasobu. Wybierz **Poprzednia różnica**, aby się cofnąć. Istnieje również możliwość wyłączenia wskaźnika różnic i zachowania nawigacji w obszarze **ustawienia.**

W sytuacjach, gdy istnieją przypisania zadań dla zasobu, ale nie ma rezerwacji, w formularzu **Projekty** na karcie **Uzgadnianie** można wybrać niedobór rezerwacji, a następnie kliknąć przycisk **Rozszerz rezerwację**. Zostanie wyświetlone okno dialogowe **Rozszerz rezerwację**, w którym przedstawiono rezerwację potrzebną do wyeliminowania problemu niedoboru zasobu. To okno dialogowe pokazuje również istniejące rezerwacje zasobu we wszystkich projektach lub innych encjach zaplanowania. W przypadku wybrania opcji **OK**, aby utworzyć rezerwację zasobu niezależnie od dostępności tego zasobu, może wystąpić rezerwacja ponad dyspozycyjność.

Następnie menedżer projektu lub menedżer zasobów może za pomocą tablicy harmonogramu rozwiązać sytuację, w której zasób został zarezerwowany ponad jego dyspozycyjność.
