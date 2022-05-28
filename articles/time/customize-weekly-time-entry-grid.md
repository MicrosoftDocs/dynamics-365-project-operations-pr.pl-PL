---
title: Rozszerzanie wpisów czasu
description: W tym temacie przedstawiono informacje na temat sposobu, w jaki deweloperzy mogą rozszerzyć kontrolę wpisów czasu.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582999"
---
# <a name="extending-time-entries"></a>Rozszerzanie wpisów czasu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rozwiązaniu Dynamics 365 Project Operations zawiera rozszerzaną kontrolę niestandardową wpisu czasu. Obejmuje on następujące funkcje:

- Wprowadzanie czasu w ciągu tygodnia
- Podsumowanie według dni, wierszy lub tygodni
- Kopiowanie wierszy lub tygodni
- Wpis czasu jako HH:mm lub HH.hh (automatycznie konwertowane na HH.hh)
- Importowanie z przydziałów, rezerwacji lub terminów

Rozszerzanie wpisów czasu jest możliwe w dwóch obszarach:
- [Dodawanie niestandardowych wpisów czasu do użytku własnego](#add)
- [Dostosowywanie formantu kontroli wpisu czasu](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodawanie niestandardowych wpisów czasu do użytku własnego

Wpisy czasu są obiektami podstawowymi używanymi w wielu scenariuszach. W 1. wydaniu kwietniowym 2020 wprowadzono rozwiązanie podstawowe TESA. TESA udostępnia encję **Ustawienia** oraz nową rolę zabezpieczeń **Użytkownika wpisu czasu**. Zawarte są także nowe pola **msdyn_start** oraz **msdyn_end**, które mają bezpośrednią relację z **msdyn_duration**. Nowa encja, rola zabezpieczeń i pola umożliwiają bardziej zunifikowany sposób podejścia do czasu w ramach różnych produktów.


### <a name="time-source-entity"></a>Encja źródła czasu
| Pole | Opis | 
|-------|------------|
| Nazwa/nazwisko  | Nazwa wpisu źródła czasu używana jako wartość wyboru podczas tworzenia wpisów czasu. |
| Domyślne źródło czasu [źródło czasu: IsDefault] | Domyślnie tylko jedno źródło czasu może być oznaczone jako domyślne. Dzięki temu wpisy mogą domyślnie określić źródło czasu, jeśli nie zostało ono określone. |
|Typ źródła czasu [źródło czasu: sourcetype] | Typ źródła to opcja (typ źródła wpisu czasu), która umożliwia skojarzenie źródła czasu z aplikacją. Firma Microsoft rezerwuje wartości większe niż 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Wpisy czasu i encja źródła czasu
Każdy wpis czasu jest skojarzony z rekordem źródła czasu. Ten rekord określa, które aplikacje powinny przetwarzać wprowadzanie czasu i jak to zrobić.

Wpisy czasu są zawsze jednym ciągłym blokiem czasowym z połączonym początkiem, końcem i czasem trwania.

W ramach tej reguły rekord wpisu czasu będzie automatycznie aktualizowany w następujących sytuacjach:

- Jeśli zostanie podane będą dwa z trzech następujących pól, trzecie jest obliczane automatycznie: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Pola **msdyn_start** i **msdyn_end** są strefy czasowej.
- Wpisy godzin utworzone tylko z określonymi wartościami **msdyn_date** i **msdyn_duration** zaczynają się od północy. Pola **msdyn_start** i **msdyn_end** zostaną odpowiednio zaktualizowane.

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

1. Dodaj pole niestandardowe do okna dialogowego **szybkie tworzenie**.
2. Skonfiguruj siatkę, tak aby pokazywała pole niestandardowe.
3. Dodaj pole niestandardowe do strony **edycji wiersza** lub **edycji wpisu czasu**.

Upewnij się, że nowe pole ma wymagane walidacje na stronie **Edycja wiersza** lub **Edycja wpisu czasu**. W ramach tego zadania zablokuj pole na podstawie statusu wpisu czasu.

Po dodaniu pola niestandardowego do siatki **wprowadzania czasu** i utworzeniu wpisów czasu bezpośrednio w siatce pole niestandardowe tych pozycji jest automatycznie ustawiane tak, aby odpowiadało wierszowi. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodaj pole niestandardowe do okna dialogowego szybkie tworzenie
Dodaj pole niestandardowe do okna dialogowego **Szybkie tworzenie: Utwórz wpis czasu**. Użytkownicy mogą następnie wprowadzić wartość podczas dodawania wpisów czasu, wybierając opcję **Nowy**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Skonfiguruj siatkę, tak aby pokazywała pole niestandardowe
Istnieją dwa sposoby, aby dodać pole niestandardowe do siatki **jednotygodniowego zapisu czasu**.

- Dostosuj widok **Moje tygodniowe wpisy czasu** i dodaj do niego pole niestandardowe. Możesz określić położenie i rozmiar pola niestandardowego w siatce, edytując właściwości w widoku.
- Utwórz nowy niestandardowy widok wprowadzania czasu i ustaw go jako widok domyślny. Ten widok powinien zawierać pola **opis** i **Komentarze zewnętrzne** oprócz kolumn, które mają być zawarte w siatce. Możesz określić położenie, rozmiar i domyślną kolejność sortowania siatki, edytując właściwości w widoku. Następnie skonfiguruj formant niestandardowy dla tego widoku tak, aby był formantem **siatki wpisu czasu**. Dodaj ten formant do widoku i wybierz go dla sieci **Web**, **telefonu** i **tabletu**. Następnie skonfiguruj parametry siatki **jednotygodniowego wpisu czasu**. W polu **Data rozpoczęcia** wybierz wartość **msdyn\_date**, ustaw pole **Czas trwania** jako **msdyn\_duration**, a następnie w polu **Stan** ustaw wartość **msdyn\_entrystatus**. W **polu Lista stanu tylko do odczytu** jest ustawiona wartość **192350002 (Zatwierdzony)**, **192350003 (Przesłane)** lub **192350004 (Prośba o cofnięcie)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Dodaj pole niestandardowe do odpowiedniej strony edycji
Strony używane do edycji wpisów czasu lub wiersza czasu można znaleźć w obszarze **Formularze**. Przycisk **Edytuj wpis w** siatce otwiera **stronę wprowadzania edycja**, a przycisk **Edytuj wiersz** otwiera stronę **edycji** wiersza. Strony te można edytować w taki sposób, aby zawierały pola niestandardowe.

Obie opcje spowodują usunięcie gotowego filtrowania w encjach **Projekt** i **Zadania projektu**, dzięki czemu będą dostępne wszystkie widoki wyszukiwania encji. W gotowym rozwiązaniu są dostępne tylko odpowiednie widoki wyszukiwania.

Należy określić odpowiednią stronę dla pola niestandardowego. Najprawdopodobniej po dodaniu pola do siatki, powinno zostać uwzględnione w przepływie zadań **edycji wiersza** używanym dla pól dotyczących całego wiersza wpisów czasu. Jeśli pole niestandardowe ma unikalną wartość w wierszu każdego dnia (na przykład jeśli jest to pole niestandardowe dla godziny zakończenia), powinno znaleźć się na stronie **Edycja wpisu czasowego**.

Aby dodać pole niestandardowe do strony, przeciągnij element **pola** na odpowiednie miejsce na stronie, a następnie ustaw jego właściwości.

### <a name="add-new-option-set-values"></a>Dodawanie wartości nowego zestawu opcji
Aby dodać wartości zestawu opcji do pola nieobsługiwanego, wykonaj poniższe kroki.

1. Otwórz stronę edycji pola, a następnie w obszarze **typ** wybierz opcję **edycja** obok zestawu opcji.
2. Dodaj nową opcję o niestandardowej etykiecie i kolorze. Jeśli chcesz dodać nowy stan wpisu czasu, gotowe pole jest nazwane **Stan wpisu**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Oznaczanie nowego stanu wpisu czasu jako tylko do odczytu
Aby wyznaczyć nowy stan wpisu czasu jako tylko do odczytu, należy dodać nową wartość wpisu czasu do właściwości **lista tylko do odczytu**. Należy dodać numer, a nie etykietę. Edytowalna część siatki wpisu czasu zostanie teraz zablokowana w przypadku wierszy mających nowy stan. Aby ustawić właściwość **Lista stanu tylko do odczytu** inaczej dla różnych widoków **wprowadzania czasu**, dodaj siatkę **wprowadzania czasu** w sekcji **Niestandardowe formanty** widoku i skonfiguruj odpowiednie parametry.

Następnie dodaj reguły biznesowe, aby zablokować wszystkie pola na stronach **Edycja wiersza** i **Edycja wpisu czasu**. Aby uzyskać dostęp do reguł biznesowych dla tych stron, otwórz edytor formularzy dla każdej strony, a następnie wybierz **reguły biznesowe**. Nowy stan można dodać do warunku w istniejących regułach biznesowych lub dodać nową regułę biznesową dla nowego stanu.

### <a name="add-custom-validation-rules"></a>Dodawanie niestandardowych reguł sprawdzania poprawności
Dla siatki wprowadzania **tygodniowego wpisu** można dodać dwa typy reguł sprawdzania poprawności:

- Reguły biznesowe po stronie klienta, które działają na stronach.
- Sprawdzanie poprawności dodatków plug-in po stronie serwera, które dotyczą wszystkich aktualizacji wpisów czasu

#### <a name="client-side-business-rules"></a>Reguły biznesowe po stronie klienta
Używaj reguł biznesowych do blokowania i odblokowywania pól, wprowadzania wartości domyślnych w polach i definiowania sprawdzania poprawności wymagającego informacji tylko z bieżącego rekordu wpisu czasu. Aby uzyskać dostęp do reguł biznesowych dla strony, otwórz edytor formularzy, a następnie wybierz **reguły biznesowe**. Następnie można dokonać edycji istniejących reguł biznesowych lub dodać nową regułę biznesową.

#### <a name="server-side-plug-in-validations"></a>Sprawdzanie poprawności dodatku plug-in po stronie serwera
Sprawdzania poprawności plug-inów należy używać do wszystkich walidacji, które wymagają więcej kontekstu niż jest do dyspozycji w pojedynczym wpisie czasu. Należy ich także używać do sprawdzania poprawności, które mają być uruchamiane na aktualizacjach w tekście w siatce. Aby ukończyć walidacje, należy utworzyć niestandardowy plug-in dla encji **Wpis czasu**.

### <a name="limits"></a>Limity
Obecnie siatka **wprowadzania godziny** ma ograniczenie rozmiaru do 500 wierszy. Jeśli jest więcej niż 500 wierszy, nie zostaną one pokazywane. Nie można zwiększyć tego limitu rozmiaru.

### <a name="copying-time-entries"></a>Kopiowanie wpisów czasu
Użyj widoku **Kopiuj kolumny wpisów czasu** w celu zdefiniowania listy pól, które mają zostać skopiowane podczas wpisywania czasu. Pola **Data** oraz **Czas trwania** są wymagane i nie można ich usunąć z widoku.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
