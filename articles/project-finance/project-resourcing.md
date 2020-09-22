---
title: Pozyskiwanie zasobów do projektu
description: Ten temat zawiera informacje o pozyskiwaniu zasobów do projektów.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754262"
---
# <a name="project-resourcing"></a>Pozyskiwanie zasobów do projektu

[!include [banner](../includes/banner.md)]

Ten temat zawiera informacje o pozyskiwaniu zasobów do projektów.

Jednym ze sposobów na menedżerowie projektów i menedżerowie zasobów na etapie planowania projektów jest alokacja zasobów, gdzie muszą określić i zarezerwować poprawny zasób, aby pozostały do pracy nad projektem. W Dynamics 365 Finance funkcje zasobów dla projektów pozwalają zdefiniować role, które są traktowane jako zasoby tymczasowe, które można zarezerwować dla określonego zadania lub części zlecenia. Menedżerowie projektów tego typu i menedżerowie zasobów mogą wykonać następujące zadania:

- Zdefiniować rolę z wymaganymi kompetencjami, tak aby można było łatwo dopasować zasoby.
- Role umożliwiają zdefiniowanie początkowego harmonogramu zakontraktowań, który jest oparty na zastrzeżonych zasobach.
- Oszacuj koszty i określ budżet wstępny na podstawie przydzielonych ról i zasobów dla projektu.
- Korzystając z ról, można oszacować liczbę rezerwacji zasobów wymaganych dla każdego zakontraktowania.
- Oszacuj liczbę zasobów wymaganych przez pełny cykl życia projektu.
- Wersja robocza struktury podziału pracy (SPP) została wykorzystana przez początkowe przydziały zasobów.

[![Cykl życia projektu](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

W miarę postępu planowania projektów planowane zasoby mogą zostać zamienione na zasoby personelu. Menedżer projektu może również wycofać i zaktualizować zastrzeżenia, które można pozyskać na etapie projektu.

## <a name="set-up-project-resources"></a>Skonfiguruj zasoby projektu
Należy skonfigurować kalendarz i skojarzyć go z pracownikiem lub robotnikiem. Kalendarz jest używany do zaplanowania projektu i czasu pracy zasobów, które są zarezerwowane dla projektu. Podczas konfigurowania kalendarza kierownicy projektów mogą przeprowadzać bilansowanie zasobów w ramach optymalizacji zasobów. Na podstawie harmonogramu kalendarza można przystąpić do umieszczania ograniczeń zasobów. Kalendarz można skonfigurować na stronie **Kalendarze**.

Po skonfigurowaniu pracownika jako zasobu projektu możesz wybrać spośród pracowników pracujących w firmie, dla której konfigurujesz zasoby. Alternatywnie można wybrać pracowników z innych firm należących do organizacji. Ci pracownicy są określani jako zasoby międzyfirmowe.

Poniższe procedury wyjaśniają, jak skonfigurować pracownika jako zasób projektu w firmie i jak skonfigurować zasób projektu międzyfirmowego.

### <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurowanie pracownika jako zasobu projektu

1. Na stronie **Pracownicy** na liście **Pracownicy** wybierz pracownika, który ma być dodawany jako zasób projektu, i otwórz rekord pracownika.
2. W okienku akcji wybierz **Projekt** &gt; **Ustawienia** &gt; **Ustawienia projektu**.
3. Zaznacz kalendarz i zamknij stronę.

Można również określić domyślne projekty zasobu jako typ przypisywania wstępnego. Przypisań wstępnych można użyć, gdy menedżer zasobów lub kierownik projektu wie z wyprzedzeniem, nad którymi projektami będzie pracował zasób. Przypisania wstępne mogą być również oparte na żądaniu sponsora lub klienta projektu. Aby wstępnie przydzielić projekt, na stronie **Przypisywanie projektów**, na karcie **Projekty**, na liście **Pozostałe projekty** wybierz odpowiedni projekt.

### <a name="set-up-an-intercompany-resource"></a>Konfigurowanie zasobu międzyfirmowego

W przypadku konfigurowania pracownika jako zasobu międzyfirmowego należy przeprowadzić konfigurację zarówno w firmie pożyczającej, jak i firmie pożyczającej.

**W firmie pożyczkowej**

1. W Finance sprawdź, czy wybrano firmę pożyczkową, a następnie wykonaj procedurę opisaną w poprzedniej sekcji „Konfigurowanie pracownika jako zasobu projektu”.
2. Na stronie **Księgowość międzyfirmowa** kliknij przycisk **Nowy**.
3. W polu **Identyfikator firmy** wybierz firmę pożyczkową. Wypełnij odpowiednio pozostałe pola, a następnie wybierz **Zapisz**.
4. Na stronie **Cena przeniesienia** kliknij przycisk **Nowy**.
5. W polu **Firma pożyczająca** wybierz odpowiednią firmę.
6. Aby pożyczyć firmie pożyczającej tylko zasób utworzony na początku tej sekcji, w polu **Zasób** wybierz nazwę utworzonego zasobu. Aby udostępnić wszystkim zasobom w firmie wypożyczanie spółce zażyczania, pole **Zasobu** powinno pozostać puste.
7. Na stronie **Parametry Zarządzanie projektami i księgowanie** na karcie **Międzyfirmowe** ustaw opcję **Włącz Międzyfirmowe planowanie zasobów i grafiki** na **Tak**.

**W firmie pożyczającej**

- Na stronie **Lista zasobów** w filtrze wyszukiwania wprowadź nazwę zasobu utworzonego dla firmy służącej do wypożyczania, aby sprawdzić, czy nazwa znajduje się na liście zasobów dla firmy, która jest pożyczana.

## <a name="manage-resource-competencies"></a>Zarządzaj kwalifikacjami zasobów
Kwalifikacje zasobów są zasadniczą częścią zarządzania zasobami. Kwalifikacje mogą pełnić rolę linii bazowej w celu określenia zasobów mających odpowiedni bilans umiejętności, edukacji, certyfikacji i doświadczenia w projekcie. W tym celu należy skonfigurować te informacje dla każdego zasobu i regularnie je aktualizować. W ten sposób można zmaksymalizować możliwości, gdy określone kompetencje zasobów są dopasowywane podczas przypisywania zasobów do projektu.

[![Przykłady kwalifikacji, certyfikacji, wykształcenia i doświadczenia w projekcie](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Poniższe procedury opisują sposób konfigurowania niektórych kompetencji danego zasobu.

Aby skonfigurować kompetencje pracownika, można użyć strony listy **Pracowników** w zasobach ludzkich lub na stronie lista **Zasobów** w Zarządzanie projektami i księgowanie. Do wykonania poniższych procedur jest używana strona listy **Pracownicy** w zasobach ludzkich.

### <a name="set-up-competencies-certificates"></a>Konfigurowanie kompetencji: certyfikaty

1. Na stronie listy **Pracownicy** wybierz wiersz, dla którego pracownik ma dodać informacje o certyfikacie.
2. W okienku akcji na karcie **Pracownik** w grupie **Kwalifikacje** kliknij opcję **Certyfikaty**.
3. Wybierz **Nazwa** w polu **Typ certyfikatu**, a następnie wybierz **PMP**.
4. W polu **Data rozpoczęcia** wybierz opcję **10/1/2015** i wybierz pozycję **Zapisz**.

### <a name="set-up-competencies-skills"></a>Konfigurowanie kompetencji: umiejętności

1. Upewnij się, że na stronie listy **Pracowników** jest wybrany pracownik użyty w poprzedniej procedurze. W okienku akcji na karcie **Pracownik** w grupie **Kwalifikacje** kliknij opcję **Umiejętności**.
2. Wybierz **Nowy**.
3. W polu **Umiejętności** wybierz opcję **Zarządzanie projektem**.
4. W polu **Poziom** wybierz pozycję **5 ekspertów**.
5. W polu **Data poziomu** wybierz pozycję **1-/14/2014**.
6. W polu **Lata doświadczenia** wprowadź liczbę **10**.
7. Wybierz **Zapisz**, a następnie zamknij stronę.

## <a name="create-a-new-project"></a>Tworzenie nowego projektu
1. Na stronie **Zarządzanie projektem** wybierz **Nowy projekt**, a następnie wprowadź następujące wartości:

    - **Typ projektu:** czas i materiały
    - **Nazwa projektu:** faza uaktualniania w XYZ 2
    - **Grupa projektów:** TM\_WIP
    - **Identyfikator kontraktu projektu:** 00000002

2. Wybierz pozycję **Utwórz projekt**.

### <a name="assign-a-resource-to-a-project"></a>Przypisywanie zasobu do projektu

1. Na stronie **Pracownicy** na liście **Pracownicy** wybierz rekord pracownika, dla którego wcześniej skonfigurowano kompetencje, i otwórz rekord pracownika.
2. W okienku akcji na karcie **Projekt** w grupie **Ustawienia** kliknij opcję **Przypisz projekty**.
3. Na stronie **Przypisania projektów walidacji zasobów**, na karcie **Projekty**, w polu **Dodaj projekt do wybranych projektów** wybierz Filtr w projekcie **XYZ faza aktualizacji 2**.
4. W okienku **Pozostałe projekty** wybierz projekt, a następnie wybierz przycisk strzałki, aby dodać go do okienka **Wybrane projekty**.

Kategorie zasobu można również przypisać w zależności od potrzeb. Kategoria typu to albo **Koszt**, albo **Przychód**. Typ kategorii jest określany przez organizację. Jeśli do zasobu nie są przypisane żadne kategorie, Finance wyszukuje domyślną kategorię według cen godzinowych dla kosztów i przychodów.

### <a name="set-up-project-resource-and-role-characteristics"></a>Skonfiguruj zasoby projektu i cechy roli

Menedżer projektu może używać funkcji zasobów projektu do tworzenia ról wymaganych w projekcie. Role mogą być używane, jeśli potwierdzone zasoby są nadal nieznane podczas rezerwowania zasobów. Role mogą być tymczasowo rezerwowane jako planowane zasoby, aby można było kontynuować etapy planowania projektów.

[![Przykład roli](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenariusz:** Contoso zostało zatrudnione w celu ukończenia projektu typu czas i materiały, dla którego istnieje zatwierdzona karta projektu. Młodszy kierownik projektu nadal kończy zakres projektu. Menedżer zasobów obecnie identyfikuje konkretne zasoby, które będą zastrzeżone do pracy nad nowym projektem. Ze względu na krytyczny charakter projektu, sponsor projektu poprosił starszego kierownika projektu jako jedną z ról. Menedżer zasobów musi nabyć nowy zasób i zdefiniować rolę w systemie na wypadek, gdyby młodszy kierownik projektu potrzebował informacji o zasobach podczas planowania projektu.

Poniższe kroki pokazują, jak menedżer zasobów może skonfigurować rolę starszego kierownika projektu i skojarzyć z nią cechy zasobu. Później roli można użyć do wyszukiwania dostępnych zasobów, które pasują do wymaganych kompetencji zasobów.

1. Na stronie **Role ustawień** wybierz **Nowy**, a następnie wprowadź następujące wartości:

    - **Identyfikator roli:** starszy kierownik projektu
    - **Opis:** starszy kierownik projektu

2. Wybierz pozycję **Utwórz**.
3. Zaznacz rolę **Starszy kierownik projektu**, a następnie wybierz pozycję **Konfigurowanie charakterystyki**.
4. W polu **Typ charakterystyki** wybierz opcję **Umiejętności**.
5. W polu **Dostępne charakterystyki** wprowadź umiejętność, która ma zostać wyszukana.
6. W polu **Typ charakterystyki** wybierz opcję **Certyfikat**.
7. W polu **Dostępne charakterystyki** wprowadź typ certyfikatu, który ma zostać wyszukany.

### <a name="assign-a-project-resource-to-a-project"></a>Przypisz zasób projektu do projektu

1. Na stronie **Wszystkie projekty** wybierz projekt **XYZ uaktualnianie faza 2**.
2. Na karcie **Zespół projektowy i planowanie** wybierz opcję **Dodaj**.
3. W polu **Rola** wybierz pozycję **Członek zespołu**.
4. Wybierz **Rezerwuj z kalendarza**.
5. Na stronie **Dostępność zasobów** wybierz **Ustawienia widoku**.
6. Na stronie **Dostosowywanie ustawień widoku** wprowadź następujące wartości:

    - **Format widoku zakresu dat:** Dzień
    - **Wyświetlanie opisów dostępności:** Tak
    - **Wyświetl wydajność pozostałą:** Tak

7. Na liście zasobów wybierz zasób.
8. Wybierz opcję **Ostateczna rezerwacja** i **Pełna dyspozycyjność**.


### <a name="assign-a-resource-to-a-default-role"></a>Przypisz zasób do roli domyślnej

Aby pomóc menedżerom projektów lub zasobów, można dokładniej przeanalizować zasoby, które można zarezerwować dla projektu. Możesz skojarzyć rolę domyślną z istniejącym zasobem lub nowo nabytym zasobem. Na przykład, kiedy Daniel został zatrudniony, posiadał doświadczenia i umiejętności umożliwiające wypełnienie roli analityka biznesowego. Kierownik zasobów przypisał tę rolę jako domyślną rolę Daniela. Dlatego kierownik ds. zasobów dodał Daniela do puli analityków biznesowych, którzy są dostępni do pracy nad projektami.

Podczas rezerwacji zasobów kierownicy projektów mogą filtrować zasoby ról, które są dostępne do pracy nad projektami. Mogą one wykorzystywać te informacje jako kryterium podczas wykonywania wielokryteriówowych analiz decyzji podczas realizacji zasobów. W celu wyszukania zasobów z określonymi umiejętnościami, edukacją i doświadczeniem dla danego projektu mogą również dodać inne charakterystyki zasobów.

**Scenariusz:** Rozpoczął się zatwierdzony projekt, a rola starszego kierownika projektu została zarezerwowana jako planowany zasób na etapie planowania projektu. Kierownik zasobów uzyskał teraz zasób do pełnienia roli starszego kierownika projektu.

1. Na stronie **Lista zasobów** wybierz pozycję **Daniel Goldschmidt**.
2. Na stronie **Rola zasobu** wybierz **Nowy**, a następnie wprowadź następujące wartości:

    - **Efektywność:** wprowadź aktualną datę.
    - **Data wygaśnięcia:** wprowadź **nigdy**.
    - **Rola:** Wpisz **starszy kierownik projektu**.

3. Wybierz **Zapisz**, a następnie zamknij stronę.
4. Na karcie **kompetencje** dodaj umiejętność **ProjectMgmt** i certyfikat **PMP**.

## <a name="set-up-role-based-pricing"></a>Skonfiguruj ceny oparte na rolach
Wszystkie ceny kosztów, sprzedaży i przeniesienia można skonfigurować dla ról.

1. Na stronie **Cena sprzedaży (godzina)** wybierz opcję **Nowa** i wprowadź datę wejścia w życie.
2. W kolumnie **Rola** wybierz rolę.
3. W kolumnie **Ceny** wprowadź cenę wybranej roli zasobu.

## <a name="form-a-project-team"></a>Stwórz zespół projektowy
Aby użyć ról, które zostały wcześniej skonfigurowane w projekcie, kierownik projektu musi skojarzyć role z projektem. Do danego projektu można przypisać wiele ról. W celu uniknięcia niejasności te role są automatycznie oznaczane podczas rezerwacji. Na przykład, jeśli kierownik projektu wymaga trzech inżynierów oprogramowania, trzy role inżyniera oprogramowania, których etykiety mają **inżyniera oprogramowania 1**, **inżyniera oprogramowania 2** i **inżyniera oprogramowania 3**, są generowane automatycznie. Jeśli właściwości roli zostały wcześniej ustawione dla roli, są one stosowane jako filtr podczas wyszukiwania zasobu. Dodatkowe charakterystyki można dodać w zależności od potrzeb, aby dokładniej uściślić wyszukiwanie.

Ustawienia widoku mogą być również dostosowywane w celu lepszego wyświetlenia dostępności zasobów. Dostępne są opcje umożliwiające pokazanie godzinowych, dziennych, tygodniowych, miesięcznych i rocznych oraz rocznej dostępności. Istnieje również możliwość wyświetlenia dostępnej i pozostałej wydajności zasobów. Ta opcja jest przydatna przy szacowaniu czasu dostępności, kiedy oceniany jest dostępny czas na działania lub dostępność zasobów.

Kierownik projektu może wybrać rolę na stronie, a następnie, jeśli dostępny jest zasób, który spełnia wymagania, może zarezerwować zasób do wypełnienia roli. Należy pamiętać, że zasoby nie muszą być rezerwowane w tym punkcie etapu planowania. Podczas tworzenia SPP można zastępować role przy użyciu zasobów pracowniczych dla danego projektu. Jeśli role zostaną zamienione na zasoby służbowe w SPP, konfiguracja zasobu powoduje automatyczne zaktualizowanie listy i harmonogramu planowania zespołu projektu.

[![Lista zespołu projektowego zawierająca zarówno role, jak i rzeczywiste zasoby](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Menedżer projektu ma różne opcje rezerwacji zasobu, takie jak **Wydajność pozostała**, **Pełna wydajność**, **Procent wydajności** i **Określona liczba godzin**. Te opcje rezerwacji można anulować w dowolnym momencie, jeśli zmienią się przydziały zasobów. Obsługiwane są dwa typy rezerwacji:

- **Rezerwacja ostateczna** — Rezerwacja zasobów została zatwierdzona i potwierdzona do pracy nad zaangażowaniem przez określony czas.
- **Wstępna rezerwacja** — Rezerwacje zasobów zostały wstępnie ustawione do pracy nad zaangażowaniem przez określony czas.

Poniższa procedura wyjaśnia, jak utworzyć zespół projektowy.

### <a name="create-a-project-team"></a>Tworzenie zespołu projektu

1. Na stronie lista **Wszystkie projekty** wybierz projekt, a następnie wybierz pozycję **Edytuj**.
2. Na karcie **Zespół projektowy i planowanie** w polu **Data zakończenia harmonogramu** wprowadź datę rozpoczęcia harmonogramu plus jeden miesiąc. Jeśli na przykład Data rozpoczęcia planowania wynosi 24 czerwca 2017 (24/06/2017), wprowadź **24/07/2017**.
3. Wybierz **Dodaj**.
4. W okienku **Dodaj role do projektu**, w polu **Rola** wybierz pozycję **Starszy kierownik projektu**.
5. Wybierz **Wymagane kompetencje**.
6. Na stronie **Wybierz cechy** cechy, które zostały wcześniej ustawione dla roli starszego kierownika projektu, są zaznaczone domyślnie. Wybierz pozycję **OK**.
7. Na stronie **Dodawanie ról do projektu**, w polu **Liczba zasobów**, wprowadź wartość **1**.
8. W polu **Zasób** jest wyświetlane wszystkie zasoby o wymaganych kwalifikacjach. Wybierz opcję **Daniel Goldschmidt**, a następnie wybierz pozycję **Utwórz**.
9. Na stronie **Projekt** wybierz opcję **Dodaj**.
10. W okienku **Dodaj role do projektu**, w polu **Rola** wybierz pozycję **Członek zespołu**. W polu **Liczba zasobów** wprowadź liczbę **5**.
11. Wybierz pozycję **Utwórz**.
12. Na stronie **Projekty** wybierz pozycję **Spełniaj zasoby**.

## <a name="resource-capacity-synchronization"></a>Synchronizacja pojemności zasobów
Procesy synchronizacji zasobów pomagają zagwarantować, że informacje z kalendarza i kalendarza podstawowego trafiają do planowania zasobów projektu. Jeśli zostanie zmieniony kalendarz, procesy będą wymagały aktualizacji planowania zasobów projektów. Procesy pomagają również zwiększyć wydajność, ponieważ informacje o zasobach kalendarza są z góry synchronizowane. Z tego powodu aktualizacje informacji o harmonogramach zasobów są wykonywane szybciej. Zaleca się, aby zamiast pojedynczych procesów zaplanować przetwarzanie w postaci partii. W przeciwnym razie istnieje ryzyko, że użytkownik zapamiętał datę utworzenia ostatniej synchronizacji informacji. Jeśli nie są używane daty łączne, podczas synchronizacji między datami mogą następować przerwy.

![Synchronizacja kalendarza](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizuj podsumowania pojemności zasobów

Proces synchronizacji ma na celu zsynchronizowanie wszystkich informacji kalendarza zasobów. Te informacje obejmują informacje kalendarza podstawowego o wszelkich zmianach w tabeli pojemności kalendarza zasobów projektu. Jeśli w projekcie zostaną dodane nowe zasoby, synchronizacja pomaga zagwarantować, że dostępne są zaktualizowane informacje w kalendarzu. Tę synchronizację można wykonać w dowolnym momencie.

Zalecamy użycie partii. Te opcje są dostępne podczas synchronizowania rezerwacji wydajności.

1. Wybieranie **Zarządzanie projektami i księgowanie** &gt; **Okresowe** &gt; **Synchronizacja pojemności** &gt; **Synchronizuj podsumowania pojemności zasobów**.
2. Ustaw opcje w poniższej tabeli.

    | Opcja      | Opis |
    |-------------|-------------|
    | Kod okresu | Opcjonalnie wybierz kod interwału dat księgi głównej, aby ustawić daty rozpoczęcia i zakończenia procesu synchronizacji dla zbiorczych pojemności zasobów. |
    | Data rozpoczęcia  | Wprowadź datę rozpoczęcia procesu synchronizacji dotyczącego zestawienia wydajności zasobów. |
    | Data zakończenia    | Wprowadź datę zakończenia procesu synchronizacji dotyczącego zestawienia wydajności zasobów. |

[![Proces synchronizacji](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Konfigurowanie ról w szablonach SPP
Menedżerowie projektów mogą konfigurować szablony SPP, które mogą stosować podczas tworzenia SPP dla nowych projektów. Menedżerowie projektów mogą dodawać role, tworząc szablon. Poniższa procedura służy do przypisywania ról do szablonów SPP.

1. Wybierz **Zarządzanie projektami i księgowanie** &gt; **Ustawienia** &gt; **Projekty** &gt; **Szablony struktury podziału pracy**.
2. Wybierz **Szczegóły** wybranego szablonu SPP.
3. Wybierz zadanie z listy, a następnie w polu **Rola** wybierz rolę, która ma zostać przypisana do zadania.

### <a name="work-with-a-wbs"></a>Praca z SPP

Istnieje możliwość utworzenia nowego SPP lub skopiowania SPP z istniejącego szablonu SPP. Menedżer projektu może łatwo zarządzać zasobami, przypisując role do nowych zadań w SPP. Role można zamieniać po uzyskaniu zasobu lub po zidentyfikowaniu potwierdzonego zasobu, który posłuży do jego poprawnego wykonania. Ta elastyczność umożliwia kierownikom projektów wykonywanie następujących zadań:

- Określ liczbę zasobów wymaganych przez pakiety pracy spp.
- Oszacuj koszty projektu.
- Ustalenie wstępnego budżetu.
- Szacowana wartość czasu trwania działania oparta na rolach i zasobach.
- Opracowywanie planów zarządzania projektami na podstawie dostępnych informacji o projekcie.

W SPP dodano dodatkowe opcje, aby lepiej wykorzystać funkcję pozyskiwania zasobów.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcja</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Przypisania zasobów</td>
<td>Wyświetl przydzielone zasoby, daty, liczbę godzin i typ rezerwacji dla zadań w SPP.</td>
</tr>
<tr class="even">
<td>Automatycznie generuj zespół</td>
<td>Zaplanowano automatyczne dodanie zasobów za pomocą ról skojarzonych z zadaniem. Finance automatycznie sugeruje planowane zasoby, korzystając z wielokryterialnej analizy decyzji opartej na rolach. Po ustawieniu ról i wysiłku (godzin) dla zadań w SPP i po zwolnieniu struktury wybierz opcję <strong>Automatycznie generuj zespół</strong>. Wymagana liczba zaplanowanych zasobów jest dodawana do listy SPP oraz na karcie <strong>Planowanie projektów i zespołów</strong>.</td>
</tr>
<tr class="odd">
<td>Zasób (lista rozwijana)</td>
<td>Na stronie <strong>Uruchom przypisanie zasobów</strong> można wybrać zasoby do rezerwacji ostatecznych lub wstępnych zależnie od określonego czasu trwania. Można dostosować ustawienia widoku w celu wyświetlenia i ustawienia czasu trwania działań zasobu. Możesz wybrać i przypisać zasoby na poziomie pakietu roboczego, korzystając z następujących opcji:
<ul>
<li><strong>Zaakceptuj</strong> — Potwierdzanie zmian zasobu przydzielonego do zadania.</li>
<li><strong>Anuluj</strong> — Anulowanie zmian zasobu przydzielonego do zadania.</li>
<li><strong>Automatyczne przypisywanie</strong> — dostępny zasób pracowniczy, który ma zgodną rolę, jest automatycznie wybierany i przypisywany wybranemu zadaniu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stronie **Wszystkie projekty** wybierz projekt **XYZ uaktualnianie faza 2**.
2. Wybieranie **Plan** &gt; **Działania** &gt; **Struktura podziału pracy**.
3. Wybierz opcję **Nowy**, aby dodać następujące działania poziomu pierwszego do WBS:

    - Inicjowanie
    - Planowanie
    - Wykonywanie
    - Monitorowanie i kontrolowanie
    - Zamykanie

4. Ustaw daty i nakład pracy (godziny), tak jak to pokazano na poniższej ilustracji.

    [![Ustawianie dat i wysiłku](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Zaznacz wiersz zadania **Inicjowanie**, a następnie w polu **Rola** wybierz pozycję **Starszy kierownik projektu**.
6. Wybierz **Publikuj**.
7. W tym samym wierszu w polu **Zasób** wybierz opcję **Daniel Goldschmidt**, a następnie wybierz opcję **Zaakceptuj**.
8. Wybierz wiersz zadania **Planowania**, a następnie w polu **Rola** wybierz pozycję **Analityk biznesowy**.
9. Wybierz opcję **Opublikuj**, a następnie wybierz opcję **Automatyczne generowanie zespołu**.
10. W oknie z komunikatem potwierdzenia wyświetlany wybierz **Tak**.
11. W polu **Zasób** sprawdź, czy wartość jest **Analitykiem biznesowym 1**.
12. W przypadku zasobu **Analityk biznesowy 1** otwórz wyszukiwanie i wybierz opcję **Uruchom przydziały zasobów**. Następnie wybierz pracownika do wykonania zadania.
13. Wybierz opcję **Wstępne przypisanie** &gt; **Pełna wydajność**.

    > [!NOTE] 
    > Nie otrzymasz ostrzeżenia, że określony zasób wynosi teraz 2, ponieważ liczba zasobów pozostaje 1.

14. Na stronie **Struktura podziału pracy** sprawdź poprawność przydziału zasobu w SPP, a następnie wybierz pozycję **Zapisz**.

## <a name="resource-fulfillment-for-planned-resources"></a>Realizacja zasobów dla planowanych zasobów
Kierownik projektu może zaplanować wymagane role zasobów dla projektu. Kierownik zasobów będzie widział te planowane zasoby jako żądania na stronie **Realizacja zasobów** i będzie mógł przypisywać rzeczywiste zasoby.

1. Na stronie **Wszystkie projekty** wybierz projekt **XYZ uaktualnianie faza 2**.
2. Wybierz **Projekt**, a następnie wybierz **Edytuj**.
3. Na karcie **Zespół projektowy i planowanie** wybierz opcję **Dodaj**.
4. W oknie dialogowym **Dodawanie ról** wybierz rolę **dewelopera oprogramowania**.
5. Wybierz **Utwórz**, a następnie zamknij stronę projektu.
6. Na stronie dotyczącym **Realizacji zasobów** wybierz **deweloper oprogramowania 1** w projekcie **XYZ aktualizacja projektu faza 2**.
7. Wybierz pracownika, a następnie opcję **Przypisz**.
8. Sprawdź, czy wiersz dotyczący **Dewelopera oprogramowania 1** został usunięty z projektu **XYZ aktualizacja projektu faza 2**.
9. Na karcie **Zespół projektowy i planowanie**, w odniesieniu do projektu **XYZ aktualizacja faza 2**, należy sprawdzić, czy pracownik wybrany w poprzednim kroku został dodany jako **Deweloper oprogramowania**.

## <a name="requests-for-project-resources"></a>Żądania dotyczące zasobów projektu
Funkcjonalność planowania zasobów projektu pozwala tylko menedżerom zasobów na dystrybucję zasobów personelu w ramach zleceń lub projektów. Aby włączyć tę funkcję, należy wykonać następujące zadania lub sprawdzić, czy zostały wykonane:

- Konfigurowanie sekwencji numerów.
- Konfigurowanie przepływu pracy dotyczącego zarządzania projektami i księgowań.
- Włączanie przepływu pracy żądania zasobu.

Po wykonaniu powyższych czynności można wykonać następujące zadania, które są wymagane:

- Utwórz zlecenie zasobu na podstawie wstępnie zarezerwowanego zasobu pracowniczego.
- Monitoruj żądania zasobów.
- Realizowanie żądań zasobów.
- Zażądanie zasobu pracowniczego z SPP.
- Zarezerwuj zasoby do projektu bez żądania zasobu pracowniczego.

## <a name="monitor-project-teams"></a>Monitoruj zespoły projektów
1. Na stronie **Wszystkie projekty** wybierz łącze **Identyfikator projektu** dla projektu **XYZ uaktualnianie faza 2**.
2. Na skróconej karcie **Zespół projektowy i planowanie** sprawdź, czy wymienione zasoby projektu są poprawne.
