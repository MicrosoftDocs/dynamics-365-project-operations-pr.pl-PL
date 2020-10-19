---
title: Rozszerzanie wpisów czasu
description: W tym temacie przedstawiono informacje na temat sposobu, w jaki deweloperzy mogą rozszerzyć kontrolę wpisów czasu.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930893"
---
# <a name="extending-time-entries"></a>Rozszerzanie wpisów czasu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Dynamics 365 Project Operations obejmuje formant niestandardowego wprowadzanego wpisu czasu. Obejmuje on następujące funkcje:

- Wprowadzanie czasu w ciągu tygodnia
- Podsumowanie według dni, wierszy lub tygodni
- Kopiowanie wierszy lub tygodni
- Wpis czasu jako HH:mm lub HH.hh (automatycznie konwertowane na HH.hh)
- Importowanie z przydziałów, rezerwacji lub terminów

Rozszerzanie wpisów czasu jest możliwe w dwóch obszarach:
- [Dodawanie niestandardowych wpisów czasu do użytku własnego](#add)
- [Dostosowywanie formantu kontroli wpisu czasu](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodawanie niestandardowych wpisów czasu do użytku własnego.

Wpisy czasu są obiektami podstawowymi przeznaczonymi do użytku w różnych scenariuszach. W 1. wydaniu z kwietnia 2020 roku wprowadzono rozwiązanie podstawowe TESA, które udostępnia encję **Ustawień** oraz nową rolę zabezpieczeń **Użytkownika wpisu czasu**. Zawarte są także nowe pola **msdyn_start** oraz **msdyn_end**, które mają bezpośrednią relację z **msdyn_duration**. Nowa encja, rola zabezpieczeń i pola umożliwiają bardziej zunifikowany sposób podejścia do czasu w ramach różnych produktów.


### <a name="time-source-entity"></a>Encja źródła czasu
| Pole | Opis | 
|-------|------------|
| Nazwa/nazwisko  | Nazwa wpisu źródła czasu używana jako wartość wyboru podczas tworzenia wpisu czasu. |
| Domyślne źródło czasu [źródło czasu: IsDefault] | Domyślnie tylko jedno źródło czasu może być oznaczone jako domyślne źródło czasu. Dzięki tej funkcji wpisy mogą domyślnie określić źródło czasu, jeśli nie zostało ono określone. |
|Typ źródła czasu [źródło czasu: sourcetype] | Typ źródła to opcja (typ źródła wpisu czasu), która umożliwia skojarzenie źródła czasu z aplikacją. Do tego zestawu opcji zostaną dodane dodatkowe wartości, ponieważ dodano dodatkowe aplikacje. Należy zwrócić uwagę, że firma Microsoft rezerwuje wartości większe niż 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Wpisy czasu i encja źródła czasu
Każdy wpis czasu jest skojarzony z rekordem źródła czasu. Ten rekord określa, które aplikacje mają przetwarzać wpis czasu i w jaki sposób.

Wpisy czasu są zawsze jednym ciągłym blokiem czasowym z połączonym początkiem, końcem i czasem trwania.

W ramach tej reguły rekord wpisu czasu będzie automatycznie aktualizowany w następujących sytuacjach:

- Jeśli zostanie podane będą dwa z trzech następujących pól, trzecie jest obliczane automatycznie 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Pola **msdyn_start** i **msdyn_end** są oparte na strefach czasowych.
- Wpisy czasowe utworzone z określonymi polami **msdyn_date** i **msdyn_duration** zaczynają się o północy, a pola **msdyn_start** i **msdyn_end** zostaną odpowiednio zaktualizowane.

#### <a name="time-entry-types"></a>Typy wpisu czasu

Rekordy wpisów czasu są powiązane ze skojarzonym typem, który definiuje zachowanie w przepływie przesyłania dla skojarzonej aplikacji.

|Etykieta | Wartość|
|-----|-----|
|W czasie przerwy   |192,355,000|
|Podróż | 192,355,001|
|Nadgodziny   | 192,354,320|
|Praca   | 192,350,000|
|Nieobecność    | 192,350,001|
|Urlop   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Dostosowywanie formantu kontroli wpisu czasu
Deweloperzy mogą dodawać dodatkowe pola i wyszukiwania do innych encji, a także implementować niestandardowe reguły biznesowe, które będą obsługiwały ich scenariusze biznesowe.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Dodawanie pól niestandardowych, posiadających wyszukiwania w innych encjach
Aby dodać pole niestandardowe do siatki jednotygodniowego zapisu czasu, należy wykonać trzy podstawowe kroki.

- Dodaj pole niestandardowe do okna dialogowego szybkie tworzenie.
- Skonfiguruj siatkę, tak aby pokazywała pole niestandardowe.
- Dodaj pole niestandardowe do przepływu zadań edycji wierszy albo przepływu zadań edycji komórki.

Należy się także upewnić, że nowe pole zawiera wymagane sprawdzanie poprawności w przepływie zadań edycji komórki lub wiersza. W ramach tego kroku należy zablokować pole na podstawie stanu wpisu czasu.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodaj pole niestandardowe do okna dialogowego szybkie tworzenie
Pole niestandardowe należy dodać do okna dialogowego **szybkiego tworzenia wpisu czasu**. Użytkownicy mogą następnie wprowadzić wartość podczas dodawania wpisów czasu, wybierając opcję **Nowy**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Skonfiguruj siatkę, tak aby pokazywała pole niestandardowe
Istnieją dwa sposoby, aby dodać pole niestandardowe do siatki jednotygodniowego zapisu czasu:

  - Dostosowywanie widoku i Dodawanie pola niestandardowego
  - Tworzenie nowego domyślnego wpisu czasu 


**Dostosowywanie widoku i Dodawanie pola niestandardowego**

Można dostosować widok **Moje tygodniowe wpisy czasu** i dodać do niego pole niestandardowe. Można wybrać pozycję i rozmiar pola niestandardowego w siatce, edytując te właściwości w widoku.

**Tworzenie nowego domyślnego wpisu czasu** 

Ten widok powinien zawierać pola **opis** i **Komentarze zewnętrzne** oprócz kolumn, które mają być zawarte w siatce. 

1. Wybierz pozycję, rozmiar i domyślną kolejność sortowania w siatce, edytując te właściwości w widoku. 
2. Skonfiguruj formant niestandardowy dla tego widoku tak, aby był formantem **siatki wpisu czasu**. 
3. Dodaj ten formant do widoku i wybierz go dla sieci Web, telefonu i tabletu. 
4. Skonfiguruj parametry siatki jednotygodniowego wpisu czasu. W polu **Data rozpoczęcia** wybierz wartość **msdyn_date**, ustaw pole **Czas trwania** jako **msdyn_duration**, a następnie w polu **Stan** ustaw wartość **msdyn_entrystatus**. 
5. W przypadku widoku domyślnego pole **listy stanu tylko do odczytu** ma wartość **192350002, 192350003, 192350004**, pole **przepływu zadań edycji wierszy** ma wartość **msdyn_timeentryrowedit**, a pole **przepływu zadań edycji komórki** ma ustawioną wartość**msdyn_timeentryedit**. 
6. Te pola można dostosować w taki sposób, aby dodać lub usunąć stan tylko do odczytu albo użyć innego sposobu opartego na zadaniu (TBX) podczas edycji wierszy lub komórek. Te pola powinny być ograniczone wartością statyczną.


> [!NOTE] 
> Obie opcje spowodują usunięcie gotowego filtrowania w encjach **Projekt** i **Zadania projektu**, dzięki czemu będą dostępne wszystkie widoki wyszukiwania encji. W gotowym rozwiązaniu są dostępne tylko odpowiednie widoki wyszukiwania.
Konieczne jest ustalenie odpowiedniego przepływu zadań dla pola niestandardowego. Najprawdopodobniej po dodaniu pola do siatki, powinno zostać uwzględnione w przepływie zadań edycji wiersza używanym dla pól dotyczących całego wiersza wpisów czasu. Jeśli w polu niestandardowym każdy dzień ma unikatową wartość, na przykład pole niestandardowe **Godzina zakończenia**, powinno zostać uwzględnione w przepływie zadań edycji komórki.

Aby dodać pole niestandardowe do przepływu zadań, przeciągnij element **pola** na odpowiednie miejsce na stronie, a następnie ustaw właściwości pola. Ustaw właściwość **Źródło** jako **wpis czasu** i ustaw właściwość **pole danych** jako pole niestandardowe. Właściwość **Pole** określa wyświetlana nazwa na stronie TBX. Wybierz opcję **Zastosuj**, aby zapisać zmiany w polu, a następnie wybierz pozycję **Aktualizuj**, aby zapisać zmiany na stronie.

Aby zamiast tego skorzystać z nowej niestandardowej strony TBX, należy utworzyć nowy proces. Ustaw kategorię na **przepływ procesów biznesowych**, ustaw encję jako **wpis czasu** i ustaw typ procesu biznesowego jako **uruchom proces jako przepływ zadań**. W obszarze **właściwości** właściwość **nazwa strony** powinna być ustawiona jak wyświetlana nazwa strony. Dodaj wszystkie odpowiednie pola na stronie TBX. Zapisz i aktywuj proces, a następnie zaktualizuj właściwość niestandardowego formantu dla odpowiedniego przepływu zadań jako wartość **nazwy** w procesie.

### <a name="add-new-option-set-values"></a>Dodawanie wartości nowego zestawu opcji
Aby dodać wartości zestawu opcji do gotowego pola, otwórz stronę edycji pola, a następnie w obszarze **typ**wybierz opcję **edycja** obok zestawu opcji. Następnie dodaj nową opcję o niestandardowej etykiecie i kolorze. Jeśli chcesz dodać nowy stan wpisu czasu, gotowe pole jest nazwane **Stan wpisu**, a nie **Stan**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Oznaczanie nowego stanu wpisu czasu jako tylko do odczytu
Aby wyznaczyć nowy stan wpisu czasu jako tylko do odczytu, należy dodać nową wartość wpisu czasu do właściwości **lista tylko do odczytu**. Edytowalna część siatki wpisu czasu zostanie zablokowana w przypadku wierszy mających nowy stan.
Następnie dodaj reguły biznesowe, aby zablokować wszystkie pola na stronach TBX **edycji wiersza wpisu czasu** i **edycji wpisu czasu**. Aby uzyskać dostęp do reguł biznesowych tych stron, należy otworzyć edytor przepływu procesów biznesowych strony, a następnie wybrać **reguły biznesowe**. Nowy stan można dodać do warunku w istniejących regułach biznesowych lub dodać nową regułę biznesową dla nowego stanu.

### <a name="add-custom-validation-rules"></a>Dodawanie niestandardowych reguł sprawdzania poprawności
Istnieją dwa typy reguł sprawdzania poprawności, które można dodać do siatki wpisu czasu tygodniowego:

- Reguły biznesowe po stronie klienta, które działają w szybkich oknach dialogowych i na stronach TBX.
- Sprawdzanie poprawności dodatków plug-in po stronie serwera, które dotyczą wszystkich aktualizacji wpisów czasu.

#### <a name="business-rules"></a>Reguły biznesowe
Używaj reguł biznesowych do blokowania i odblokowywania pól, wprowadzania wartości domyślnych w polach i definiowania sprawdzania poprawności wymagającego informacji tylko z bieżącego rekordu wpisu czasu. Aby uzyskać dostęp do reguł biznesowych strony TBX, należy otworzyć edytor przepływu procesów biznesowych strony, a następnie wybrać **reguły biznesowe**. Następnie można dokonać edycji istniejących reguł biznesowych lub dodać nową regułę biznesową. Aby jeszcze bardziej dostosować sprawdzanie poprawności, można użyć reguły biznesowej w celu uruchomienia skryptów języka JavaScript.

#### <a name="plug-in-validations"></a>Sprawdzanie poprawności plug-inów
Sprawdzania poprawności plug-inów należy używać do wszystkich walidacji, które wymagają więcej kontekstu niż jest do dyspozycji w pojedynczym wpisie czasu lub do walidacji, które chcesz przeprowadzić na aktualizacjach w trakcie edycji w siatce. Aby ukończyć walidację, należy utworzyć niestandardowy plug-in dla encji **Wpis czasu**.
