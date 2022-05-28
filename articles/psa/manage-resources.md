---
title: Zarządzaj zasobami
description: W tym temacie zamieszczono informacje dotyczące sposobu zarządzania zasobami.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5788a457c888bd2ab945fa52df82157a7c17d56b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589853"
---
# <a name="manage-resources"></a>Zarządzaj zasobami

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation zawiera pulpit nawigacyjny Menedżer zasobów umożliwiający graficzne przeglądy popytu i wykorzystania zasobów w całej organizacji. Korzystając z wykresów na tym pulpicie nawigacyjnym, można wizualizować następujące informacje:

- **Zapotrzebowanie na zasoby** — na wykresie **Aktywne żądania zasobów** przedstawiono zasoby, które zostały przesłane. Zasoby są agregowane według ról lub projektów.
- **Nieprzesłane zapotrzebowanie na zasoby** — wykres **Nieprzydzielone zapotrzebowanie na zasoby** pokazuje wszystkie wymagania zasobu, które nie zostały przesłane. Ułatwia to menedżerom zasobów wyświetlanie zapotrzebowania, które nie jest firmą i może być przesłane za pośrednictwem żądania zasobu.
- **Wykorzystanie do rozliczenia za ubiegły tydzień** — wykres **Wykorzystanie według roli** pokazuje procent rzeczywistego wykorzystania zasobu do rozliczenia według roli względem docelowego wykorzystania według roli, które podlega rozliczeniu.

    > [!NOTE]
    > Aby wykres **Wykorzystanie według roli** był dostępny, należy utworzyć zadanie, które uruchamia przepływ pracy UpdateRoleUtilization. To zadanie cykliczne jest uruchamiane co siedem dni w celu obliczenia wykorzystania do zafakturowania przez ostatnie siedem dni. Wyniki są agregowane według ról.

## <a name="manage-project-team-members"></a>Członkowie zespołu zarządzania projektem

Menedżerowie projektów mogą używać pulpitu nawigacyjnego Menedżer zasobów do zarządzania zasobami w projektach. Na przykład użytkownicy mogą dodawać członków zespołu bezpośrednio do projektu i rezerwować członków zespołu, aby spełnić wymagania dotyczące zasobów przechwycone przez zasób ogólny.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodawanie członka zespołu bezpośrednio do projektu

Aby dodać członka zespołu bezpośrednio do projektu, na stronie **projekty** na karcie **zespół** wybierz opcję **nowy.** Zostanie wyświetlone okno dialogowe **szybkie tworzenie: członek zespołu projektu**. W tym oknie dialogowym można wykonać następujące zadania:

- **Zarezerwowanie nazwanego zasobu** – w polu **Zasób, który można zarezerwować** wybierz nazwę zasobu. Następnie wybierz rolę, ustaw okres i wybierz metodę alokacji. Wybrany nazwany zasób jest dodawany do projektu przy użyciu wybranej metody alokacji i kalendarza zasobów.
- **Dodaj zasób ogólny** — pozostaw puste pole **zasobu, który można zarezerwować**, a następnie wybierz rolę, ustaw okres i wybierz preferowaną metodę alokacji. Zasób ogólny jest dodawany do zespołu jako symbol zastępczy w celu przechowywania wzorca popytu używanego do rezerwowania nazwanych zasobów w zespole. Wymóg jest składany zgodnie z kalendarzem projektu.
- **Dodaj nazwany zasób do zespołu bez zużywania dyspozycyjności zasobu** — w polu **zasobu, który można zarezerwować** wybierz zasób. Następnie wybierz okres i zaznacz **Brak** jako metodę alokacji. Zasób jest dodawany do zespołu, ale jego dyspozycyjność nie jest wykorzystywana poprzez rezerwację.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezerwowanie członka zespołu w celu spełnienia wymagań dotyczących zasobów dla zasobu ogólnego

W usłudze PSA można zarezerwować zasób ogólny w zespole projektu i określić jego rolę, wymaganą dyspozycyjność i sposób dystrybucji tej dyspozycyjności. W zapotrzebowaniu na zasoby można określić atrybuty, które są skojarzone z zasobem ogólnym. Do atrybutów tych zalicza się wymagane kwalifikacje, preferowaną jednostkę organizacyjną i preferowane zasoby.

Wykonaj te kroki, aby określić wymagane kwalifikacje dla zasobu ogólnego w przypadku dewelopera.

1. Na stronie **projekty** na karcie **zespół** wybierz opcję **nowy**, aby zarezerwować zasób ogólny.

    ![Zasób ogólny zarezerwowany w zespole.](media/Resource-Management-image9.png)

2. W widoku **wszyscy członków zespołu** w kolumnie **wymagania dotyczące zasobu** wybierz łącze, aby dodać wymagane umiejętności dla zasobu ogólnego.

    ![Łącze do wymagań.](media/Resource-Management-image10.png)

3. Na wyświetlonej stronie **Wymagania dotyczące zasobu** w siatce **umiejętności** wybierz wielokropek (**...**), a następnie wybierz opcję **Dodaj nową cechę wymagania**, aby dodać wymagane umiejętności dla swojego dewelopera.

    ![Polecenie dodawania nowej cechy wymagania.](media/Resource-Management-image11.png)

4. W oknie dialogowym **szybkie tworzenie: cecha**, które zostanie wyświetlone, w polu **cecha** wybierz wymagane umiejętności. Następnie w polu **Wartość klasyfikacji** wybierz poziom biegłości dla tej umiejętności. Na koniec w polu **Wymaganie zasobu** należy ustawić wymagania dotyczące zasobów źródłowych z jednostek organizacyjnych lub nawet nazwanych zasobów. Kiedy skończysz, wybierz **Zapisz**.

    ![Okno dialogowe Szybkie tworzenie: cecha wymagania.](media/Resource-Management-image12.png)

5. Na stronie **Zapotrzebowania zasobu** wybierz pozycję **Rezerwuj**, aby spełnić wymagania dotyczące zasobu.

    ![Przycisk Rezerwuj na stronie zapotrzebowanie zasobu.](media/Resource-Management-image13.png)

    Można też wybrać zasób ogólny w siatce **wszystkie członków zespołu**, a następnie wybrać opcję **Rezerwuj**.

    ![Przycisk Rezerwuj nad siatką wszystkich członków zespołu.](media/Resource-Management-image14.png)

    > [!NOTE]
    > W tym przykładzie jest 40 wymaganych godzin, ale nie ma rzeczywistych zarezerwowanych godzin, ponieważ zasoby ogólne nie mają rezerwacji. Oprócz tego nie ma przydzielonych godzin, ponieważ zasób ogólny został dodany bezpośrednio do zespołu. Nie został dodany przy użyciu przypisania zadania.

    Na stronie **asystent planowania** można filtrować dostępne zasoby według wymagań określonych w zapotrzebowaniu zasobu. Zasoby są sortowane zgodnie z parametrami sortowania określonymi na tablicy harmonogramu.

    ![Strona Asystent planowania.](media/Resource-Management-image15.png)

    Oto kilka często używanych filtrów:

    - **Charakterystyki wraz z oceną** — Filtruj według kwalifikacji, certyfikatów i innych cech zasobów, a także oceny biegłości.
    - **Role** — Filtruj według ról domyślnych przypisanych do zasobów, które można rezerwować.
    - **Jednostki organizacyjne** — Filtruj zasoby możliwe do zarezerwowania według jednostek organizacyjnych, do których są przypisane.

6. Jeśli wyniki pierwszego wyszukiwania wymagania nie są zadowalające, można zmienić kryteria filtrowania. Rozwiń okienko **widoku filtra** po lewej stronie, a następnie wybierz pozycję **Wyszukaj** w celu wyszukania dodatkowych zasobów.

    ![Okienko widoku filtra.](media/Resource-Management-image16.png)

7. Aby zmienić sposób sortowania wyników, wybierz **Sortuj**.

    ![Polecenie Sortuj.](media/Resource-Management-image17.png)

8. Wybierz zasoby według zapotrzebowania określonego w zapotrzebowaniu, tak jak to pokazano u górnej części siatki. Użytkownik może wyczyścić wybrane komórki siatki i zostawić otwartą dyspozycyjność zasobu. Tylko jeden zasób jednocześnie może być zaznaczony jako zarezerwowany.

9. Wybierz **Rezerwuj**, aby zarezerwować wybrany zasób i pozostaw otwartą tablicę harmonogramu, aby mieć możliwość wybrania dodatkowych zasobów. Możesz również wybrać opcję **Zarezerwuj i wyjdź**, aby zarezerwować wybrany zasób i zamknąć tablicę harmonogramu.

    ![Zasób do zarezerwowania.](media/Resource-Management-image19.png)

    Otrzymujesz powiadomienie dotyczące zarezerwowanych godzin. Wskaźniki popytu pokazują, w jakim stopniu zapotrzebowanie na rezerwację zostało spełnione oraz jaka część pozostaje. Użytkownik może również sprawdzić, jaka część dyspozycyjności wybranego zasobu jest zużywana. Wybierz opcję **rozwiń**, aby wyświetlić więcej szczegółów dotyczących rezerwacji zasobów.

9. Powróć do widoku **wszystkich członków zespołu**. W siatce zauważ, że zasób ogólny został zastąpiony przez nazwany zasób, a 40 godzin zostało zarezerwowanych dla tego zasobu.

    ![Zaktualizowanie siatki wszystkich członków zespołu.](media/Resource-Management-image20.png)

    > [!NOTE]
    > Nie są wyświetlane przypisane godziny, ponieważ są one zarezerwowane bezpośrednio w zespole. Nie zostały one zarezerwowane przy użyciu przypisania zadania.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Przypisywanie zasobów ogólnych do zadań i generowanie wymagań zasobów

W PSA można tworzyć zadania i przypisywać im zasoby ogólne. W ten sposób zapotrzebowanie zasobu może być reprezentowane przez symbole zastępcze podczas szacowania harmonogramu i kwot. Następnie można wygenerować zapotrzebowania zasobów dla zasobów ogólnych i zrealizować je.

1. Na stronie **projekty** na karcie **harmonogram** wybierz pozycję **Dodaj**, aby utworzyć zadanie.

    ![Utworzono nowe zadanie.](media/Resource-Management-image21.png)

2. W polu **zasoby** wybierz symbol **selektora zasobów**. Zostanie wyświetlony selektor zasobów zawierający listę istniejących członków zespołu danego projektu.

    ![Selektor zasobów.](media/Resource-Management-image22.png)

3. Wprowadź nazwę nowego zasobu ogólnego i wybierz pozycję **Utwórz.**

    ![Wprowadzona nazwa nowego zasobu ogólnego.](media/Resource-Management-image23.png)

4. W oknie dialogowym **szybkie tworzenie: członek zespołu projektu**, które zostanie wyświetlone, w polu **Rola** wybierz rolę dla zasobu ogólnego. W polu **Jednostka zasobów** wybierz jednostkę organizacyjną dla zasobu ogólnego. Następnie wybierz opcję **Zapisz**.

    ![Zostanie wyświetlone okno dialogowe szybkie tworzenie: członek zespołu projektu.](media/Resource-Management-image24.png)

    Ogólny członek zespołu teraz jest przypisany do zadania.

    ![Ogólny członek zespołu przypisany do zadania.](media/Resource-Management-image25.png)

    Na karcie **zespół** zobaczysz nowego ogólnego członka zespołu. Zauważ, że ma on tylko przypisane godziny. Te godziny to suma wszystkich zadań przydzielonych do ogólnego członka zespołu. Ogólny członek zespołu nie ma jeszcze wymaganych godzin ani wymagania zasobu.

    ![Ogólny członek zespołu na karcie Zespół.](media/Resource-Management-image26.png)

5. Teraz możesz przypisać ogólnego członka zespołu do innych zadań za pomocą selektora zasobów.

    ![Ogólny członek zespołu w selektorze zasobów.](media/Resource-Management-image27.png)

    Po zakończeniu przypisywania ogólnego zasobu do zadań można wygenerować zapotrzebowanie zasobu dla zasobu ogólnego.

5. Na karcie **zespół** wybierz zasób ogólny i wybierz opcję **Generuj zapotrzebowanie.**

    ![Polecenie Generuj wymaganie.](media/Resource-Management-image28.png)

    Kiedy zapotrzebowanie jest generowane, ogólny członek zespołu będzie dysponować godzinami i łączem dotyczącym wymagania zasobu.

    ![Łącze wymaganie zasobu.](media/Resource-Management-image29.png)

    Po zarezerwowaniu nazwanego zasobu zasób ogólny jest usuwany z zespołu i zastępowany zasobem o nazwie.

    ![Zasób ogólny zastąpiony zasobem nazwanym.](media/Resource-Management-image30.png)

    Na karcie **harmonogram** przydział zasobu ogólnego zostanie usunięty i zastąpiony nazwanym zasobem.

    ![Przypisania zasobu ogólnego zastąpione zasobem o nazwie na karcie harmonogramu.](media/Resource-Management-image31.png)

    > [!NOTE]
    > To zachowanie występuje tylko wtedy, gdy nazwany zasób jest w pełni zarezerwowany dla wymagania zasobu ogólnego. Gdy zasób o nazwie częściowo zastępuje zapotrzebowanie na zasób ogólny lub wiele nazwanych zasobów zastępuje zapotrzebowanie na zasób ogólny, zasób ogólny pozostaje przydzielony do zadania.

    Na poniższym rysunku zaplanowano 80-godzinne zadanie z czasem trwania 5 dni (16 godzin dziennie) i został przypisany do zasobu ogólnego o nazwie **"funkcjonalny**".

    ![80-godzinne, 5-dniowe zadanie przypisane do zasobu ogólnego Funkcjonalny.](media/Resource-Management-image32.png)

    W przypadku generowania wymagania będzie ono obejmowało 80 godzin w ciągu 5 dni.

    ![Wygenerowane zapotrzebowanie na 80 godzin w ciągu 5 dni.](media/Resource-Management-image33.png)

    Ponieważ dostępne zasoby pracują tylko po 8 godzin dziennie, do spełnienia zapotrzebowania potrzeba dwóch zasobów.

    ![Drugi zasób.](media/Resource-Management-image35.png)

    Na karcie **zespół** zobaczysz, że zasób ogólny nie ma wymaganych godzin, ale przydzielone godziny wciąż są wyświetlane razem z dwoma nazwanymi zasobami, które zrealizują zapotrzebowanie.

    ![Dwa nazwane zasoby na karcie zespół.](media/Resource-Management-image36.png)

    Na karcie **Harmonogram** zasób ogólny pozostaje przydzielony do zadania.

    ![Zasoby ogólne na karcie Harmonogram.](media/Resource-Management-image37.png)

PSA nie przypisuje obu zasobów do zadania, ponieważ to zachowanie mogłoby spowodować wygenerowanie mniej przewidywalnego harmonogramu. W tym prostym przykładzie łatwo podzielić godziny równo na dwa zasoby. Jednak w bardziej złożonych scenariuszach obejmujących wiele zadań i wiele zasobów, PSA musi wprowadzić założenia dotyczące alokacji rezerwacji odbieranych przez wiele zasobów na wiele zadań.

W tym scenariuszu menedżer projektu jest odpowiedzialny za analizowanie wielu rezerwacji i przypisywanie ich według potrzeb. Aby alokować rezerwacje, menedżer projektu przypisuje zadania z zasobów ogólnych do nazwanych zasobów, a następnie korzysta z widoku **uzgodnienie** w celu upewnienia się, że alokacja jest zgodna z rezerwacjami.

### <a name="edit-a-resource-requirement"></a>Edycja wymagania zasobu

Po utworzeniu wymagania zasobu menedżer projektu lub menedżer zasobów może edytować szczegóły, aby uściślić kryteria wyszukiwania podczas korzystania z tablicy harmonogramu. Aby edytować wymagania zasobu, wykonaj następujące kroki.

1. Na stronie **projekty** na karcie **zespół** wybierz łącze do dowolnego wymagania zasobu ogólnego.
2. Na stronie **wymaganie zasobu**, która zostanie wyświetlona, można zaktualizować kilka atrybutów. Oto kilka przykładów:

    - Nazwisko
    - Od daty
    - Do daty
    - Czas trwania
    - Typ zasobu

Na stronie **wymagania zasobu** menedżer projektu lub menedżer zasobów może również zdefiniować następujące informacje:

- Umiejętności
- Roles
- Preferencje dotyczące zasobu
- Preferowane jednostki organizacyjne

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aktualizacja rezerwacji zasobów po ich zarezerwowaniu w projekcie

Po dodaniu ogólnego lub nazwanego zasobu do zespołu projektu można zmienić rezerwacje zasobu.

1. Na stronie **projekty** na karcie **zespół** wybierz opcję członka zespołu, a następnie wybierz **Obsługa rezerwacji**.

    ![Tablica harmonogramu otwarta dla wybranego członka zespołu.](media/Resource-Management-image40.png)

    Zostanie wyświetlona tablica harmonogramu, która pokazuje rezerwacje członków zespołu projektu. Rozwiń rekord członka zespołu w celu wyświetlenia godzin zarezerwowanych dla tego projektu i innych projektów, które zużywają dyspozycyjność członka zespołu.

2. Zaznacz i przeciągnij rezerwację, aby ją wydłużyć lub skrócić. Zostanie otwarte okno dialogowe **Utwórz rezerwację zasobu**, które umożliwia dostosowanie rezerwacji.

    ![Okno dialogowe Utwórz rezerwację zasobu.](media/Resource-Management-image41.png)

3. Kliknij prawym przyciskiem myszy rezerwację. Można użyć menu skrótów do wykonania następujących czynności:

    - Zmiana stanu rezerwacji.
    - Edycja rezerwacji.
    - Zastępowanie zasobu w zespole projektu.

### <a name="change-the-booking-status"></a>Zmiana stanu rezerwacji

Można zmienić domyślny lub niestandardowy stan rezerwacji.

![Polecenie Zmień stan.](media/Resource-Management-image42.png)

W PSA dostępne są trzy stany:

- **Anulowany** — ten stan powoduje anulowanie rezerwacji zasobu i zwolnienie dyspozycyjności zasobu.
- **Rezerwacja ostateczna** — ten stan zużywa dyspozycyjność zasobu. Rezerwacja zazwyczaj jest tym stanem po otworzeniu **Obsługa rezerwacji** w siatce **wszystkich członków zespołu** na stronie **projekty.**
- **Rezerwacja wstępna** — ten stan powoduje dodanie zasobu do zespołu, ale nie zużywa dyspozycyjności zasobu. Oznacza to, że zasób został zarezerwowany do potencjalnej pracy, ale jest nadal dyspozycyjny, gdyby był potrzebny do wykonywania innych zadań. W widoku ogólnej dostępności zasobu rezerwacje wstępne mają inny stan niż rezerwacje ostateczne.
- **Zaproponowano** — ten stan reprezentuje propozycję Menedżera zasobów lub projektu dotyczącą zasobu. Propozycje nie zużywają dyspozycyjności zasobu, a zasób nie jest dodawany do zespołu projektu. Aby ostatecznie zarezerwować zasób w zespole, menedżer projektu musi zaakceptować propozycję.

### <a name="submit-resource-requests"></a>Prześlij żądania zasobów

Żądania zasobu są używane do zgłaszania popytu (wymagania zasobu), który musi zostać zrealizowany przez menedżera zasobów. W przypadku zasobu ogólnego, który już znajduje się w zespole, można przesłać żądanie zasobu bezpośrednio. Żądanie zasobu może być zrealizowane na dwa sposoby:

- Menedżer zasobów bezpośrednio wypełnia żądanie. W tym przypadku zasób ogólny jest zastępowany rezerwacją ostateczną, która ma nazwany zasób.
- Menedżer zasobów proponuje zasób menedżerowi projektu, a Menedżer projektu zatwierdza lub odrzuca zaproponowany zasób.

#### <a name="direct-fulfillment-of-resource-requests"></a>Bezpośrednie zrealizowanie żądań zasobów

Po wygenerowaniu wymagania zasobu Menedżer projektu może przesłać żądanie zasobu ogólnego, wybierając zasób, a następnie wybierając opcję **przesyłania żądania.**

![Przycisk Prześlij żądanie.](media/Resource-Management-image45.png)

Komentarze dotyczące zasobu można podać menedżerowi zasobów, który realizuje realizację żądania. Po przesłaniu żądania pole **stanu** dla członka zespołu zostanie zmienione na **przesłane.**

![Wprowadzanie opcjonalnych komentarzy.](media/Resource-Management-image46.png)

Gdy Menedżer zasobów realizuje żądanie, ogólny członek zespołu zostaje zastąpiony zasobem nazwanym w siatce **wszystkich członków zespołu**.

![Ogólny członek zespołu został zastąpiony przez nazwany zasób na siatce wszystkich członków zespołu.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Korzystanie z propozycji zasobów na potrzeby żądań zasobów

Zamiast bezpośredniego zarezerwowania zasobu dla żądania zasobu Menedżer zasobów może zaproponować zasób menedżerowi projektu. Menedżer zasobów może użyć tej opcji, jeśli dokładne dopasowania dotyczące zapotrzebowań nie są dostępne. Gdy Menedżer zasobów proponuje dany zasób, Menedżer projektu widzi, że pole **stanu** dla ogólnego członka zespołu jest zmienione na **Wymaga weryfikacji**.

![Stan ogólnego członka zespołu zmieniono na Wymaga weryfikacji.](media/Resource-Management-image48.png)

Aby wyświetlić zaproponowany zasób wraz z wizualizacją skutków rezerwacji proponowanego zasobu, kliknij dwukrotnie członka zespołu o stanie **Wymaga weryfikacji**. Następnie wybierz kartę **proponowane zasoby**.

![Karta Proponowane zasoby.](media/Resource-Management-image49.png)

Zaznacz pole wyboru **Zaakceptuj wszystkie propozycje**, aby zaakceptować wszystkie proponowane zasoby, lub **Odrzuć wszystkie propozycje**, aby je odrzucić. Jeśli zaakceptujesz zaproponowane zasoby, są one zarezerwowane w projekcie jako członkowie zespołu i zastępują zasoby ogólne.

> [!NOTE]
> Użytkownik musi akceptować lub odrzucać wszystkie proponowane zasoby. Nie można częściowo zaakceptować lub odrzucić.

### <a name="substitute-a-resource-on-the-project-team"></a>Zastępowanie zasobu w zespole projektu

Czasami Menedżer projektu musi zastąpić zarezerwowanego członka zespołu w projekcie.

1. Na stronie **projekty** na karcie **zespół** wybierz zasób, który wymaga zastąpienia, a następnie wybierz **Obsługa rezerwacji**.
2. Rozwiń zasób, aby wyświetlić projekty, do których jest przypisany.

    ![Zasób rozwinięty w celu pokazania przydzielonych projektów.](media/Resource-Management-image50.png)

3. Kliknij prawym przyciskiem myszy projekt, a następnie wybierz polecenie **Zastąp zasób**.
4. Jeśli znasz zasób, którym chcesz zastąpić bieżący zasób, wybierz lub wpisz nazwę, a następnie wybierz opcję **ponowne przypisanie.**

    ![Określanie zastępstwa zasobu.](media/Resource-Management-image51.png)

    Można również wykonać następujące kroki, aby wyszukać zasób:

    1. Wybierz pozycję **Znajdź zastępstwo**.

        ![Wyszukiwanie zastępstwa zasobu.](media/Resource-Management-image52.png)

        Asystent harmonogramu zwraca listę dostępnych zastępców. W Asystencie planowania można dalej filtrować dostępne zasoby, aby znaleźć odpowiednie zastępstwo.

        ![Lista dostępnych zastępców.](media/Resource-Management-image53.png)

    2. Aby zastąpić zasób, wybierz żądany zasób, a następnie wybierz **Zastąp**.

        ![Wybrany zasób na zastępstwo.](media/Resource-Management-image54.png)

    Rezerwacje i przypisania są zastępowane nowym zasobem.

    ![Rezerwacje i przypisania są zastępowane nowym zasobem.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Uzgadnianie rezerwacji i przypisań członka zespołu

Członkowie zespołu, rezerwacje i przydziały są luźno sprzężone. Innymi słowy, zasoby mogą mieć przydziały, ale mogą nie mieć rezerwacji lub mogą mieć rezerwacje bez przypisań. Najlepiej, kiedy rezerwacje i przypisania w projekcie są zgodne, bo wtedy zasoby mają zatwierdzoną dyspozycyjność do wykonania przypisanych im zadań. Jednak rezerwacje mogą być oparte na dostępności, a czasy zadań mogą ulec zmianie w miarę kontynuowania projektu. Z tego względu swobodne powiązanie rezerwacji i przypisań zapewnia elastyczność.

PSA oferuje kartę **Uzgadnianie**, która pozwala menedżerom projektu uzgadniać rezerwacje członków zespołu i ich przypisania w zespołach projektów.

![Karta Uzgadnianie.](media/Resource-Management-image56.png)

Na karcie **Uzgadnianie** są wyświetlane rezerwacje i przypisania na wszystkich poziomach szczegółowości, aż do poszczególnych zadań. W komórkach widać godziny, które reprezentują okresy od miesięcy aż po dni.

Na karcie przedstawiono również ogólną sumę netto projektu wraz z kolumną sumy.

Dla każdego zasobu karta oblicza różnicę między rezerwacjami członka zespołu w projekcie a zestawieniem zadań przypisanych temu członkowi zespołu. Najlepiej, aby różnica wynosiła 0 (zero). Innymi słowy nie powinno być żadnej różnicy między rezerwacjami zasobu a jego przypisaniami zadań. Różnice są oznaczone kolorami i zacienione, aby zwrócić uwagę na dwa warunki:

- **Niedobór rezerwacji** — niedobory rezerwacji powstają wtedy, gdy zasób ma więcej przypisań, niż rezerwacji. Ponieważ dyspozycyjność nie została zarezerwowana, menedżer projektu może naprawić tę sytuację poprzez rozszerzenie rezerwacji zasobu w sposób pokrywający niedobór.
- **Nadmiarowe rezerwacje** — nadmierne rezerwacje występują, gdy zasób zarezerwowano do projektu, ale nie przypisano go do zadań. Ten warunek może być akceptowalny w przypadkach, gdy zasób został zarezerwowany w projekcie przed przydziałem zadania. Jednak w innych przypadkach być może nie jest planowane przypisanie zasobu do zadań. Wtedy menedżer projektu powinien rozważyć anulowanie rezerwacji zasobu, tak aby jego dyspozycyjność można było wykorzystać w innym projekcie.

W niektórych przypadkach, kiedy oglądasz czas na wyższym poziomie niż poziom dnia (np. na poziomie miesiąca), może się pojawić różnica netto zasobu równa zero (innymi słowy, rezerwacje = przydziały). Natomiast w poziomie Tydzień można zauważyć, że istnieją przypisania równe 0 (zero) godzin i rezerwacje 40 godzin w pierwszym tygodniu miesiąca oraz przypisania 40 godzin i rezerwacje równe 0 (zero) godzin w drugim tygodniu miesiąca. Ogólnie rzecz biorąc, rezerwacje i przydziały są uzgadniane, ale różnią się od siebie między tygodniami.

Po wyświetleniu wyższych poziomów czasu na karcie **Uzgadnianie** widać wskaźnik komórki informujący o różnicach na niższych poziomach czasu. Dwukrotne kliknięcie komórki umożliwia powiększenie i wyświetlenie różnicy. Następnie kliknij prawym przyciskiem myszy, aby pomniejszyć. Zaznaczając zasób, a następnie korzystając z przycisku **Następna różnica** z paska narzędzi siatki można przejść do następnej różnicy między rezerwacjami a przydziałami danego zasobu. Następnie można skorzystać z opcji **Poprzednia różnica**, aby wrócić. Istnieje również możliwość wyłączenia wskaźnika różnic i zachowania nawigacji w obszarze **ustawienia.**

![Wskaźnik różnic.](media/Resource-Management-image57.png)

W sytuacjach, gdy istnieją przypisania zadań dla zasobu, ale nie ma rezerwacji, na stronie **Projekty** na karcie **Uzgadnianie** można wybrać niedobór rezerwacji, a następnie kliknąć przycisk **Rozszerz rezerwację**. Zostanie wyświetlone okno dialogowe **Rozszerz rezerwację**, w którym przedstawiono rezerwację potrzebną do wyeliminowania problemu niedoboru zasobu. Okno to pokazuje również istniejące rezerwacje zasobu we wszystkich projektach lub innych encjach zaplanowania. W przypadku wybrania opcji **OK**, aby utworzyć rezerwację zasobu niezależnie od dostępności tego zasobu, może wystąpić rezerwacja ponad dyspozycyjność.

![Okno dialogowe Rozszerz rezerwację.](media/Resource-Management-image58.png)

Następnie menedżer projektu lub menedżer zasobów może za pomocą tablicy harmonogramu rozwiązać sytuację, w której zasób został zarezerwowany ponad jego dyspozycyjność.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
