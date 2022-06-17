---
title: Tworzenie i potwierdzanie dzienników wpisów
description: Ten temat zawiera informacje na temat tworzenia i potwierdzenia wpisów w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912345"
---
# <a name="create-and-confirm-entry-journals"></a>Tworzenie i potwierdzanie dzienników wpisów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Oprogramowanie Entry umożliwia rejestrowanie wartości rzeczywistych bezpośrednio w Microsoft Dynamics 365 Project Operations. W przypadku korzystania z plików dziennika wpisów nie jest wprowadzanie dzienników czasu, wydatków i materiałów w Project Operations.

Pojedyncza arkusza pozwala na tworzenie wielu wierszy siatki. Po potwierdzeniem daty w programie Wpis jest rejestrowa wartość rzeczywista dla następujących szczegółów:

- Koszt lub przychód w zależności od wybranego typu transakcji.
- Wybrana klasa transakcji. Dostępne klasy to **Czas**, **Koszt**, **Materiał**, **Zatrzymanie**, **Punkt kontrolny** i **Podatek**.
- Projekt i/lub zadanie wybrane w wierszu dziennika.

Wykonaj następujące kroki, aby utworzyć arkusz wpisów w Project Operations.

1. Przejdź do **Sprzedaż** \> **Transakcje** \> **Arkusze**.
2. Na stronie listy **Wpisy arkusza** w okienku akcji wybierz opcję **Nowy**, aby utworzyć wpis.
3. Na stronie **Nowy arkusz** w polu **Opis** wprowadź opis arkusza.
4. Upewnij się, że pole **Typ arkusza** jest ustawione na **Wpis**, a następnie wybierz opcję **Zapisz**. Po zapisaniu nowego Dziennika wpisów na stronie dziennika powinna pojawić się karta **Wiersz arkusza**.
5. Na karcie **Wiersz arkusza** na pasku narzędzi nad siatką wybierz opcję **Nowy**, aaby utworzyć wiersz wpisów.
6. W oknie dialogowym **Szybkie tworzenie** nowego wiersza tworzenia ustaw pola zgodnie z opisem w poniższej tabeli.

    | Pole | Description | Wpływ funkcjonalny |
    | --- | --- | --- |
    | Klasa transakcji | Ten wiersz można zakwalifikować do jednego z sześciu klas transakcji: **Czas**, **Koszt**, **Materiał**, **Zatrzymanie**, **Punkt kontrolny** lub **Podatek**. | Klasa **transakcji Podatku** została przestarzała w Project Operations. <br> W przypadku tworzenia klasy transakcji **podatku** nie będzie ona przetwarzana przez fakturowanie, obliczenia kosztów i przychodów. **Punkt** kontrolny to klasa transakcji dostępna tylko dla przychodów. <br>Klasa **transakcji Zatrzymanie** reprezentuje informację o postępie otrzymanym od klienta. Powinna ona być zawsze tworzona jako para za fakturowanych sprzedaży i niedosyłanych wierszy sprzedaży. |
    | Typ transakcji | Do rejestrowania kosztów należy używać typów transakcji **Koszt**, **Sprzedaż wewnątrzzakładowa** oraz **Koszt jednostki zaopatrzenia**.<br> Do rejestrowania przychodów należy stosować typy transakcji **Sprzedaż niefakturowana** i **Sprzedaż fakturowana**. | Klasa **transakcji Zatrzymanie** działa tylko z typami **transakcji Sprzedaż** bez rozliczenia i **Sprzedaż zafakturowana**.<br> Klasa transakcji **Kamien milowy** działa tylko z typem transakcji **Rozliczana sprzedaż**. <br>Typy transakcji **Sprzedaż Interorg** i **Koszt jednostkowy zasobów** mają zastosowanie tylko do klasy transakcji **Czas** i są dostępne tylko w dziennikach wejściowych w scenariuszu wdrożenia Lite, a nie podczas wdrażania Project Operations w scenariuszach dotyczących zasobów / niemagazynowanych. |
    | Wybierz produkt | Po wybraniu **klasy** transakcji Materiały to pole pozwala określić, czy dla transakcji materiałowej, dla których jest tworzymy wiersz transakcji, jest istniejącym produktem czy produktem do zapisu. | W przypadku wybrania **opcji Produkt do zapisu** można wprowadzić nazwę tego produktu. |
    | Produkt | Odniesienie do produktu z katalogu. | |
    | Description | Opis wiersza najechań w celu ułatwiający identyfikację. | W przypadku niepowiązywianych wierszy sprzedaży ta wartość będzie używana jako opis podczas tworzenia szczegółów wiersza faktury. |
    | Opis zewnętrzny | Opis wiersza połączenia, który może być używany do udostępniania innym interesariuszom. | W przypadku wierszy arkusza sprzedaży nierozliczonych wartość będzie używana jako opis zewnętrzny podczas tworzenia szczegółów wiersza faktury. Faktura wysłana do klienta może być również wyświetlana na fakturze. |
    | Typ rozliczeń | Wartość wskazująca, czy wiersz będzie liczony jako składnik nieodpłatny, nieodpłatny czy nieodpłatny w projekcie. | W typowym przepływie typ rozliczeń jest uzyskiwany z terminów ustawionych w kontrakcie. Jednak podczas rekordu wiersza rekordu można wprowadzić wartość w tym polu. |
    | Data dokumentu | Użyj daty, kiedy transakcja miała miejsce. | |
    | Data rozpoczęcia | Użyj daty, kiedy transakcja miała miejsce. | To pole służy do porównywania daty utworzenia faktury dla transakcji **typu Sprzedaż nierozliczona**. To porównanie pomoże określić, czy transakcja jest datą przyszła, czy datą z przeszłości. Do faktury będą dodawane tylko transakcje z datą przeszłości. |
    | Data zakończenia | Użyj daty, kiedy transakcja miała miejsce. | |
    | Data księgowania | Użyj daty, w momencie, gdy zostanie zarejestrowany wpływ na rozliczanie. | |
    | Klient pozycji kontraktu | Domyślnie, jeśli w wierszu kontraktu jest tylko jeden klient, to pole jest ustawiane na klienta w tej kolejce po zapisaniu linii kontraktu. Jeśli w wierszu kontraktu znajduje się wielu klientów, należy wybrać prawidłowego klienta w tej kolejce. | Jeśli system nie może określić klienta linii kontraktowej w linii dziennika i jeśli jest ona pusta na fakturze typu **Sprzedaż niefakturowana**, która jest tworzona na podstawie linii dziennika, faktura nie zostanie wystawiona. |
    | Project | Wybierz projekt, w ramach który ma być zarejestrowanym wartością rzeczywistą. | Na podstawie wybranego projektu, klasy transakcji i zadania system spróbuje określić kontrakt, linią kontraktu i klienta linii kontraktu. |
    | Zadanie | Wybierz zadanie, które ma być rejestrowane w czasie rzeczywistym. | Jeśli podczas konfigurowania kontraktu zadania zostaną skojarzone z działem kontraktu, system użyje wybranego zadania wraz z klasą projektu i transakcji w celu określenia klienta kontraktu, wiersza kontraktu i listy kontraktu. |
    | Kategoria transakcji | Wybierz kategorię transakcji, w której chcesz rejestrować rzeczywiste wydatki. | W przypadku wydatków wybrana kategoria transakcji określa cenę domyślną, która zostanie wprowadzona w wierszu sprzedaży po jej zapisaniu. |
    | Rola | To pole jest związane z wierszami linii czasowej. Wybierz rolę zasobu, który spędzał czas na projekcie i/lub zadaniu. | W przypadku wierszy dziennika czasowego, jeśli korzystasz z niestandardowej konfiguracji wprowadzania domyślnych kosztów zasobów i stawek rachunku, wybrana rola jest używana wraz z jednostką zasobów do określenia domyślnej ceny, która zostanie wprowadzona w wierszu dziennika po jego zapisaniu. Jeśli do wprowadzania cen domyślnych jest używana konfiguracja niestandardowa, należy przejrzeć tę konfigurację w celu określenia, czy do wprowadzania domyślnych wartości ceny jest używane pole **Rola**. |
    | Podumowa | Jeśli wiersz aktualnego reprezentuje wydajność podwykonawców albo koszty lub materiały podwykonawców, wybierz odpowiedni kontrakt podrzędny. | Gdy zostaną zarejestrowane wiersze kosztów, wybrany podwykonawca określi cennik używany do wprowadzania domyślnego kosztu jednostkowego. |
    | Wiersz podumowy | Jeśli wiersz aktualnego reprezentuje wydajność podwykonawców albo koszty lub materiały podwykonawców, wybierz odpowiedni wiersz kontraktu podrzędnego. | Po rekordzie wierszy kosztów i kontraktów wybrana linia kontraktu podrzędnego zapewnia poprawne obliczenie wydajności dostępnej na wierszu kontraktu podrzędnego. |
    | Sposób obliczania kwoty | Domyślnie w tym polu jest ustawiona wartość **Pomnóż ilość przez cenę**. Gdy ta metoda zostanie użyta, kwota będzie obliczana jako *Ilość* × *Cena*. Inna obsługiwana metoda to **Cena stała**. Gdy ta metoda zostanie użyta, cena zostanie ustawiona na kwotę, a ilość nie zostanie użyta w obliczeniach. | |
    | Harmonogram jednostek i jednostka | Razem harmonogram jednostek i jednostka identyfikują jednostkę ilości. | Kombinacja jednostki i kategorii transakcji służy do wprowadzania domyślnych cen wydatków. W domyślnej konfiguracji Project Operations kombinacja jednostki, roli i jednostki ponownego wprowadzania cen domyślnych jest używana do wprowadzania cen domyślnych dla czasu. Jeśli do wprowadzania cen domyślnych stosowana jest konfiguracja niestandardowa, będzie ona używana razem z jednostką. Połączenie produktu i jednostki służy do wprowadzenia domyślnych cen materiałów. |
    | Ilość | Wprowadź ilość. | |
    | Cena | Jeśli cena pozostaje pusta podczas tworzenia wiersza rygorów, do wprowadzania cen domyślnych zostaną użyte odpowiednie wartości w zależności od klasy transakcji. Jeśli cena jest wprowadzana podczas tworzenia wiersza metra, zostanie ona użyta. | |
    | Podatek | Wprowadź dowolną kwotę podatku. | W zależności od wprowadzonej kwoty podatku rozszerzona kwota będzie obliczana jako *Kwota* + *Podatek*. |

## <a name="confirm-an-entry-journal"></a>Potwierdzanie daty wprowadzenia

Po wprowadzeniu wszystkich wierszy wszystkich wierszy w arkuszach programowych można potwierdzić dane. Ten proces spowoduje rejestrowanie poszczególnych wierszy jako wartości rzeczywistych w odpowiednich projektach.

Po potwierdzeniem jest, że nie można już go edytować ani żadnego z jego wierszy.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Wartości rzeczywiste utworzone przez potwierdzenie wpisu

Istnieje kilka kluczowych różnic między wartościami rzeczywistymi tworzonymi przez potwierdzenie wpisu a wartościami rzeczywistymi tworzonymi podczas zatwierdzania czasu, wydatków i dzienników użycia materiałów oraz potwierdzenia faktury w Project Operations:

- W wpisuch nie są używa się połączeń transakcji do łączenia kosztu rzeczywistego z wartością rzeczywistą sprzedaży niedosyłaną. Wartości rzeczywiste tworzone w dziennikach użycia czasu, wydatków i materiałów są zawsze zatwierdzone za pomocą połączeń transakcji w celu łączenia kosztów i wartości rzeczywistych sprzedaży niedosyłanych.
- Arkusze zapisów nie używają źródeł transakcji do łączenia rzeczywistych kosztów i nierozliczonych wartości rzeczywistych sprzedaży z dowolnym rekordem źródłowym. Rzeczywiste wartości, które są tworzone podczas zatwierdzania dzienników wykorzystania czasu, wydatków i materiałów, zawsze wykorzystują źródła transakcji do łączenia rzeczywistych kosztów i nierozliczonej sprzedaży z początkowym wpisem czasu.
- W przypadku fakturowania nierozliczonych wartości rzeczywistych sprzedaży utworzonych przez potwierdzenie arkusza zapisów, zafakturowane wartości rzeczywiste sprzedaży utworzone podczas potwierdzania faktury są połączone z nierozliczonymi rzeczywistymi wartościami sprzedaży, w podobny sposób do nierozliczonych wartości rzeczywistych sprzedaży, które są tworzone, gdy czas, koszt i Rejestry wykorzystania materiałów są zatwierdzane.
- Wiersze dziennika wpisów, które są tworzone dla czasu wprowadzonego przez zasoby międzyorganizacyjne, nie powodują automatycznego tworzenia wartości rzeczywistych typów **Koszt jednostkowy zasobów** i **Sprzedaż Interorg**. Te wartości rzeczywiste muszą być tworzone ręcznie. To zachowanie różni się od zachowania wpisów czasu rejestrowanych przez zasoby między organizacyjne. W takim przypadku po zatwierdzeniu godzin aplikacja automatycznie tworzy wartości rzeczywiste typu **Koszt** dla projektu oraz wartości rzeczywiste **kosztu jednostki ponownego zakupu** i typów **sprzedaży typu Interorg** w jednostce pracownika. Następnie połączenia transakcji są używane do łączenia tych wartości rzeczywistych oraz pochodzenia transakcji w celu połączenia ich z wprowadzeniem czasu początkowego.
- Po potwierdzeniach wpisu są dla nich tworzyć wartości rzeczywiste. Nie można jednak użyć poprawek do poprawienia tych wartości rzeczywistych. To zachowanie różni się od zachowania wartości rzeczywistych tworzyć podczas zatwierdzonego dziennika użycia czasu, wydatku i materiałów. W takim przypadku aplikacja pozwala na używanie poprawek do poprawiania wartości rzeczywistych w celu naprawienia błędów, o ile wartości rzeczywiste nie zostały jeszcze zafakturowane. Jeśli faktury zostały już zafakturowane, wartości rzeczywiste nadal można poprawić, jeśli przetwarzasz pełny kredyt z tych wartości do klienta.

> [!NOTE]
> Reguły domyślne wprowadzania nie są wymuszane. Dlatego należy używać tych plików w jak najwyższym możliwym terminie i zachować ostrożność, aby nie tworzyć w systemie uszkodzonych danych finansowych. Kiedy tylko można użyć dzienników użycia materiałów, czasu, wydatków i materiałów, punktów kontrolnych i ustawień kontraktów projektów, a następnie procesu potwierdzenia faktury projektu zamiast aplikacji Entry, można tworzyć wartości rzeczywiste.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
