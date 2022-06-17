---
title: Dostosowywanie wpisu czasu tygodniowego
description: Ten artykuł zawiera informacje na temat implementowania niestandardowych reguł biznesowych, które wspierają praktyki stosowane w organizacjach.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: bdc8df4050d895504fa126e2ee55fcd3b4de123f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918969"
---
# <a name="customize-weekly-time-entry"></a>Dostosowywanie wpisu czasu tygodniowego 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

W Microsoft Dynamics 365 Project Service Automation w wersji 3.3 firma Microsoft wprowadziła nowoczesne siatki, dzięki którym zasoby projektów mogą szybko wprowadzać czas maksymalnie do jednego tygodnia jednocześnie. Nowa siatka tygodniowego wpisu czasu może pokazywać łączne wpisy według daty, wiersza lub tygodnia. Zasoby mogą kopiować wpisy czasu w tygodniu oraz zbiorczo kopiować z poprzednich tygodni. Konfiguratorzy systemu mogą dostosować widok, dodając pola, dodając wyszukiwania do innych encji i implementując niestandardowe reguły biznesowe w celu zapewnienia pomocy w stosowaniu praktyk swoich organizacji.

Dostęp do wpisu czasu i nowej siatki czasu tygodniowego jest uzyskiwany za pośrednictwem mapy witryny. Nierozszerzalny niestandardowy wpis czasu należący do wcześniejszych wersji PAS został zastąpiony rozszerzalnym tygodniowym wpisem czasu i również przez alternatywne środowisko siatki i kalendarza tylko do odczytu. Z powodu tej zmiany użytkownicy mogą wprowadzać czas w wartościach tygodniowych.

## <a name="page-layout"></a>Układ strony
Nowa tygodniowa siatka wpisów czasu jest niestandardową kontrolką, która ma pasek narzędzi i dwie główne sekcje, **Wymiary** oraz **Czas trwania**. Pasek narzędzi zawiera przycisk, który ma zastosowanie tylko do tej kontrolki niestandardowej do siatki wpisu czasu. W odróżnieniu przyciski w okienku akcji u góry strony mają zastosowanie do trzech typów kontrolek obsługiwanych w przypadku wpisu czasu: kontrolka tygodniowego wpisu czasu, kontrolka tylko do odczytu oraz kontrolka kalendarza.

### <a name="dimensions"></a>Wymiary
Sekcja **Wymiary** zawiera nagłówki kolumn, w których wszystkie wymiary mogą być wprowadzane względem danego czasu. Poniższe wymiary są obsługiwane standardowo:

- Projekt
- Zadanie projektu
- Rola
- Typ
- Stan wpisu

W sekcji **Wymiary** niedozwolona jest edycja w tekście. Ta sekcja jest oparta na widoku, który umożliwia dodawanie niestandardowych pól do tygodniowej siatki wpisów czasu. Aby uzyskać informacje na temat dodawania pól niestandardowych, zobacz sekcję „Możliwości rozszerzania” dalej w tym artykule.

### <a name="duration"></a>Duration
Sekcja Czas trwania pokazuje dni tygodnia jako nagłówki kolumn. Ta sekcja zezwala na edycję w tekście. Po utworzeniu wiersza wpisu o odpowiednich wymiarach użytkownicy mogą szybko wprowadzić i edytować w tekście czas spędzony na tych wymiarach.

## <a name="create-a-new-time-entry"></a>Tworzenie nowego wpisu czasu
Aby utworzyć nowy wpis czasu na siatce wpisów czasu, wybierz **Nowy**. Pojawi się okno dialogowe **Szybkie tworzenie wpisu czasu**. W tym oknie dialogowym użytkownicy mogą wybrać datę wpisu czasu, a następnie wpisać datę wymiarów **Projekt**, **Zadanie projektu**, **Rola** oraz **Czas trwania** w minutach, godzinach lub dniach, wpisując **h**, **m** lub **d** wraz z liczbą. Użytkownicy mogą również wprowadzić opis i komentarze, które mogą być udostępniane zewnętrznie dla danego wpisu czasu. W chwili zapisywania zmian wartości, które zostały wpisane w wymiarach zostaną wyświetlone w sekcji **Wymiary**. Informacje o czasie trwania wprowadzone w polu **Czas trwania** są wyświetlane w dniu, w którym utworzono wpis czasu.

Pola wyszukiwania są obsługiwane w widokach systemowych. Na przykład po wejściu do projektu, pole **Zadanie projektu** jest domyślnie ustawione na widok **Kopia**. Aby utworzyć wpisy czasu dla zadań, które nie są przypisane do użytkownika, wybierz **Zmień widok** w oknie dialogowym wyszukiwania i wybierz widok **Wszystkie aktywne zadania projektu**.

## <a name="edit-a-time-entry"></a>Edycja wpisu czasu
Szczegóły z niektórych pól na stronie wprowadzania godzin, takie jak **Opis** i **Komentarze zewnętrzne**, nie są wyświetlane w siatce zapisu czasu tygodniowego. Zamiast tego w komórkach czasu trwania jest wyświetlany niewielki trójkątny wskaźnik, który zawiera te dodatkowe informacje. Zaznacz komórkę, a następnie wybierz **Edytuj szczegóły**, aby wyświetlić dane w okienku **Szybka edycja**. Aby edytować lub zaktualizować szczegóły dotyczące konkretnego wpisu czasu, który nie jest częścią siatki wpisu czasu tygodniowego, należy otworzyć okienko **Szybka edycja**.

## <a name="copy-a-time-entry-row"></a>Kopiowanie wiersza wpisu czasu
Po utworzeniu wiersza pierwszego wpisu można wybrać opcję **Kopiuj wiersz**, aby skopiować cały wiersz do nowego wiersza. Po skopiowaniu wiersza w ten sposób, wymiary i czas trwania również są kopiowane. Użytkownicy mogą również wybrać opcję **Edytuj wiersz**, w celu zaktualizowania wartości wymiarów i czasów trwania w sekcji **Czas trwania**.

## <a name="open-a-time-entry"></a>Otwieranie wpisu czasu
Aby zapewnić optymalne i szybkie wpisywanie w najbardziej widocznych polach, siatka tygodniowego wpis czasu pokazuje podzbiór wybranych wymiarów i czasów trwania. Aby wyświetlić wszystkie szczegółowe informacje dotyczące pojedynczego wpisu czasu, w obszarze **Edytuj wpis** wybierz polecenie **Otwórz.**

## <a name="submit-a-time-entry"></a>Przesyłanie wpisu czasu
Użytkownicy mogą przesyłać pojedyncze wpisy czasu lub jako grupy wpisów czasu, wybierając blok komórek lub cały wiersz wpisu czasu, a następnie wybierając opcję **Prześlij.** Przesłane wpisy czasu pojawiają się jako wpisy oczekujące na zatwierdzenie na stronie **Zatwierdzenie** osób zatwierdzających. Po pomyślnym przesłaniu wpisów czasu nie one mogą być edytowane.

## <a name="recall-a-time-entry"></a>Odwoływanie wpisu czasu
Przesłane wpisy czasu można odwoływać. Możesz odwołać pojedynczy wpis czasu, blok wpisów czasu lub cały wiersz wpisów czasu. Odwołane wpisy czasu są dostępne dla zasobów do edycji.

## <a name="time-entry-status"></a>Stan wpisu czasu
Nowe wpisy czasu automatycznie otrzymują status **Wersja robocza**. Po przesłaniu wpisu czasu status jest aktualizowany na **Przesłany**. Po zatwierdzeniu przesłanego wpisu czasu status jest aktualizowany na **Zatwierdzony**. W przypadku odrzucenia wpisu czasu stan zostanie zaktualizowany na **Zwrócony**, a wpis będzie dostępny do poprawiania i ponownego wysyłania. Usunąć można tylko wpisy czasu ze stanem **Wersja robocza**.

## <a name="view-rejection-comments"></a>Wyświetlanie komentarzy dotyczących odrzucenia
Po odrzuceniu przez osobę zatwierdzającą wpisu czasu osoba zatwierdzająca może dodać komentarze dotyczące odrzucenia, aby ułatwić zasobowi zrozumienie przyczyny odrzucenia. Aby wyświetlić komentarze dotyczące odrzucenia dla wpisu czasu, wybierz **Otwórz wpis**. Komentarze dotyczące odrzucenia będą widoczne na osi czasu. Na osi czasu zasób może odpowiedzieć na komentarze dotyczące odrzucenia, zanim ponownie prześle wpis.

## <a name="copy-week"></a>Kopiowanie tygodnia
Po utworzeniu kilku wpisów czasu można wybrać opcję **Skopiuj tydzień**, aby zbiorczo sposób tworzyć dodatkowe wpisy czasu. Zostanie otwarte okno dialogowe **Kopia**. W sekcji **Z okresu** użyj pól **Data rozpoczęcia** i **Data zakończenia**, aby zdefiniować zakres dat, z którego mają zostać skopiowane wpisy czasu. W sekcji **Do okresu** w polu **Data rozpoczęcia** określ dzień, dla którego mają zostać utworzone wpisy czasu. Następnie wybierz opcję **Kopiuj**. Dla określonej daty w okresie „do” tworzona jest kopia wpisów czasu dla odpowiadającego dnia tygodnia w okresie „od”. Na przykład wpis czasu dla poniedziałku z poprzedniego tygodnia jest kopiowany do poniedziałku tygodnia określonego w grupie pól okresu „do”.

## <a name="import"></a>Import
Ten sam podstawowy proces jest przeznaczony do importowania z rezerwacji, przypisań i wymian. Użytkownicy mogą określać zakres dat, z którego są importowane rezerwacje. Następnie muszą wyraźnie wybrać rezerwacje, które mają zostać skopiowane do wersji roboczych wpisów czasu. W poprzedniej wersji sugerowane wpisy czasu pojawiały się w siatce i kalendarzu, a następnie były tracone po odświeżeniu sesji.

## <a name="extensibility"></a>Możliwości rozszerzania
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Dodawanie pól niestandardowych, które mają wyszukiwanie w innych encjach
Aby dodać pole niestandardowe do siatki jednotygodniowego zapisu czasu, należy wykonać trzy podstawowe kroki.

1.  Dodaj pole niestandardowe do okna dialogowego szybkie tworzenie.
2.  Skonfiguruj siatkę, tak aby pokazywała pole niestandardowe.
3.  Dodaj pole niestandardowe do przepływu zadań edycji wierszy albo przepływu zadań edycji komórki w zależności od potrzeb.

Należy się także upewnić, że nowe pole zawiera wymagane sprawdzanie poprawności w przepływie zadań edycji komórki lub wiersza. W ramach tego kroku należy zablokować pole na podstawie stanu wpisu czasu.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodaj pole niestandardowe do okna dialogowego szybkie tworzenie
Pole niestandardowe należy dodać do okna dialogowego szybkiego tworzenia wpisu czasu. dzięki temu użytkownicy mogą wprowadzać wartość dla niego podczas dodawania wpisów czasu, korzystając z przycisku **nowy**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Skonfiguruj siatkę, tak aby pokazywała pole niestandardowe
Istnieją dwa sposoby, aby dodać pole niestandardowe do siatki jednotygodniowego zapisu czasu. Pierwszą opcją jest dostosowanie widoku **Moje tygodniowe wpisy czasu** i dodanie do niego pola niestandardowego. Można wybrać pozycję i rozmiar pola niestandardowego w siatce, edytując te właściwości w widoku.

Druga opcja polega na utworzeniu nowego widoku niestandardowego wpisu czasu i skonfigurowaniu go jako widoku domyślnego. Ten widok powinien zawierać pola **opis** i **Komentarze zewnętrzne** oprócz kolumn, które mają być zawarte w siatce. Można wybrać pozycję, rozmiar i domyślną kolejność sortowania w siatce, edytując te właściwości w widoku. Następnie skonfiguruj formant niestandardowy dla tego widoku tak, aby był formantem **siatki wpisu czasu**. Dodaj ten formant do widoku i wybierz go dla sieci Web, telefonu i tabletu. Następnie skonfiguruj parametry siatki jednotygodniowego wpisu czasu. W polu **Data rozpoczęcia** wybierz wartość **msdyn_date**, ustaw pole **Czas trwania** jako **msdyn_duration**, a następnie w polu **Stan** ustaw wartość **msdyn_entrystatus**. W przypadku widoku domyślnego pole **listy stanu tylko do odczytu** ma wartość **192350002, 192350003, 192350004**, pole **przepływu zadań edycji wierszy** ma wartość **msdyn_timeentryrowedit**, a pole **przepływu zadań edycji komórki** ma ustawioną wartość **msdyn_timeentryedit**. Te pola można dostosować w taki sposób, aby dodać lub usunąć stan tylko do odczytu albo użyć innego sposobu opartego na zadaniu (TBX) podczas edycji wierszy lub komórek. Te pola powinny być ograniczone wartością statyczną.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Dodawanie pola niestandardowego do odpowiedniego przepływu zadań edycji
Strony TBX, które są używane do edycji, można znaleźć w sekcji **procesy**. Stronami domyślnymi są **Project Service — Edycja wiersza wpisu czasu** i **Usługa projektów — Edycja wpisu czasu** Użytkownik może edytować te strony domyślne lub tworzyć nowe, niestandardowe strony TBX.

> [!NOTE] 
> Obie opcje spowodują usunięcie gotowego filtrowania w encjach **Projekt** i **Zadania projektu**, dzięki czemu będą dostępne wszystkie widoki wyszukiwania encji. W gotowym rozwiązaniu są dostępne tylko odpowiednie widoki wyszukiwania.

Konieczne jest ustalenie odpowiedniego przepływu zadań dla pola niestandardowego. Najprawdopodobniej po dodaniu pola do siatki, powinno zostać uwzględnione w przepływie zadań edycji wiersza używanym dla pól dotyczących całego wiersza wpisów czasu. Jeśli w polu niestandardowym każdy dzień ma unikatową wartość, na przykład pole niestandardowe **Godzina zakończenia**, powinno zostać uwzględnione w przepływie zadań edycji komórki.

Aby dodać pole niestandardowe do przepływu zadań, przeciągnij element **pola** na odpowiednie miejsce na stronie, a następnie ustaw jego właściwości. Ustaw właściwość **Źródło** jako **wpis czasu** i ustaw właściwość **pole danych** jako pole niestandardowe. Właściwość **Pole** określa wyświetlana nazwa na stronie TBX. Wybierz pozycję **Zastosuj**, aby zapisać zmiany wprowadzone w polu. Wybierz pozycję **Zaktualizuj**, aby zapisać zmiany wprowadzone na stronie.

Aby zamiast tego skorzystać z nowej niestandardowej strony TBX, należy utworzyć nowy proces. Ustaw kategorię na **przepływ procesów biznesowych**, ustaw encję jako **wpis czasu** i ustaw typ procesu biznesowego jako **uruchom proces jako przepływ zadań**. W obszarze **właściwości** właściwość **nazwa strony** powinna być ustawiona jak wyświetlana nazwa strony. Dodaj wszystkie odpowiednie pola na stronie TBX. Zapisz i aktywuj proces, a następnie zaktualizuj właściwość niestandardowego formantu dla odpowiedniego przepływu zadań jako wartość **nazwy** w procesie.

### <a name="add-new-option-set-values"></a>Dodawanie wartości nowego zestawu opcji
Aby dodać wartości zestawu opcji do gotowego pola, otwórz stronę edycji pola, a następnie w obszarze **typ** wybierz opcję **edycja** obok zestawu opcji. Następnie dodaj nową opcję o niestandardowej etykiecie i kolorze. Jeśli chcesz dodać nowy stan wpisu czasu, gotowe pole jest nazwane **Stan wpisu**, a nie **Stan**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Oznaczanie nowego stanu wpisu czasu jako tylko do odczytu
Aby wyznaczyć nowy stan wpisu czasu jako tylko do odczytu, należy dodać nową wartość wpisu czasu (liczba, a nie etykieta) do właściwości **lista tylko do odczytu**. Edytowalna część siatki wpisu czasu zostanie zablokowana w przypadku wierszy mających nowy stan.
Następnie dodaj reguły biznesowe, aby zablokować wszystkie pola na stronach TBX **edycji wiersza wpisu czasu** i **edycji wpisu czasu**. Aby uzyskać dostęp do reguł biznesowych tych stron, należy otworzyć edytor przepływu procesów biznesowych strony, a następnie wybrać **reguły biznesowe**. Nowy stan można dodać do warunku w istniejących regułach biznesowych lub dodać nową regułę biznesową dla nowego stanu.

### <a name="add-custom-validation-rules"></a>Dodawanie niestandardowych reguł sprawdzania poprawności
Istnieją dwa typy reguł sprawdzania poprawności, które można dodać do siatki wpisu czasu tygodniowego: • Reguły biznesowe po stronie klienta, które są dostępne w oknach dialogowych szybkiego tworzenia oraz na stronach TBX • Sprawdzanie poprawności dodatków plug-in po stronie serwera, które dotyczą wszystkich aktualizacji wpisów czasu

#### <a name="business-rules"></a>Reguły biznesowe
Używaj reguł biznesowych do blokowania i odblokowywania pól, wprowadzania wartości domyślnych w polach i definiowania sprawdzania poprawności wymagającego informacji tylko z bieżącego rekordu wpisu czasu. Aby uzyskać dostęp do reguł biznesowych strony TBX, należy otworzyć edytor przepływu procesów biznesowych strony, a następnie wybrać **reguły biznesowe**. Następnie można dokonać edycji istniejących reguł biznesowych lub dodać nową regułę biznesową. Aby jeszcze bardziej dostosować sprawdzanie poprawności, można użyć reguły biznesowej w celu uruchomienia skryptów języka JavaScript.

#### <a name="plug-in-validations"></a>Sprawdzanie poprawności plug-inów
Sprawdzania poprawności plug-inów należy używać do wszystkich walidacji, które wymagają więcej kontekstu niż jest do dyspozycji w pojedynczym wpisie czasu lub do walidacji, które chcesz przeprowadzić na aktualizacjach w trakcie edycji w siatce. Aby ukończyć walidację, należy utworzyć niestandardowy plug-in dla encji **Wpis czasu**.

> [!IMPORTANT] 
> Obecnie znany problem na stronach TBX uniemożliwia użytkownikom poprawianie informacji i ponowne wybieranie opcji Gotowe, gdy aktualizacja zakończy się niepowodzeniem walidacji plug-inu. W ramach rozwiązania alternatywnego można skonfigurować sprawdzanie poprawności reguł biznesowych w celu zapobiegania tej sytuacji na ile to tylko możliwe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
