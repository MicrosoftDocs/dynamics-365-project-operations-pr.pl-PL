---
title: Wydatki na diety
description: Ten temat zawiera informacje o tym, jak pracować z kosztami diet.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596063"
---
# <a name="per-diem-expenses"></a>Wydatki na diety

> [!IMPORTANT] 
> Funkcjonalność opisana w tym temacie jest dostępna dla wybranych użytkowników jako część wydania przedpremierowego.

Dodatek za każdy dzień to stały, wstępnie wstępnie przesąiony codzienne wydatki, które firma płaci pracownikom za pracę (hotele), koszty poniesione przez pracowników w czasie podróży służbowej. Firma płaci za ten koszt pracownikom zamiast płacić za faktyczne koszty podróży. Pracownicy mogą używać swoich **poświadczeń/** innych danych na potrzeby konserwacji w celu odpowiedzialności, obsługi pokoju, konserwacji lub oczyszczania podczas ważnych spotkań biznesowych. Cena jednostkowa może się różnić, w zależności od tego, czy pracodawca zdecyduje się na łączny koszt rezerwacji i rezerwacji, czy tylko na koszt rezerwacji i rezerwacji.

Stawki dzienne mogą być oparte na porze roku, miejscu podróży lub obydwu tych danych. Podczas tworzenia reguły obliczania diet można określić, że pewien procent stawki diety zostanie wstrzymany, jeśli pracownik otrzymuje bezpłatne posiłki lub usługi. Można także ustawić minimalną liczbę godzin i maksymalną liczbę godzin, dla których odsetek nie może być zastosowany w przypadku podróży pracownika.

Wartość perdyferyjna jest obliczana jako łączna liczba przydziałów dostępnych na dobę z ograniczeniem liczby osób (koszt całkowitej indyjnach) podawanej pracownikowi.

## <a name="configure-per-diems"></a>Konfiguracja na każdy dzień

Aby skonfigurować wydatki na diety, wykonaj poniższe kroki.

1. Przejdź do **Zarządzanie wydatkami** \> **Konfiguracja** \> **Ogólne** \> **Parametry zarządzania wydatkami**.
2. Na karcie **Dieta** wybierz **w polu Obliczanie obniżenia liczby** i wartości pola sposób obliczania zależności:

    - **Typ posiłku na podróż** — oblicza wartość per dem na podstawie typu wprowadzonego obniżenia ceny (przykładowa, lunch lub wichr), oraz zmniejszenie liczby dni trwania podróży określonych dla każdego typu pleratora.
    - **Typ posiłku na dzień** — Oblicz dietę na podstawie rodzaju wprowadzonego posiłku i obniżki posiłków określonej dla każdego rodzaju posiłku dla dziennej diety.
    - **Liczba posiłków dziennie** — Oblicz dzienną dietę na podstawie liczby posiłków podawanych w ciągu dnia oraz obniżki posiłków dla liczby posiłków podawanych każdego dnia.

3. Przejdź do **Zarządzanie wydatkami** \> **Ustawienia** \> **Obliczenia i kody** \> **Lokalizacje z dietami**.
4. Dodaj lokalizacje, w których można używać na każdy dzień.
5. Dla każdej dodawanej lokalizacji na karcie **Diety** wybierz stawkę diety i walutę, które obowiązują w określonych datach początkowych i końcowych dla noclegów, posiłków i innych wydatków. Aby skonfigurować jednostkowe wskaźniki i waluty, przejdź do **Zarządzanie wydatkami** \> **Ustawienia** \> **Obliczenia i kody** \> **Diety**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Diety w zmienionym interfejsie wydatków

Funkcja diet jest obsługiwana w zmodernizowanym obszarze roboczym **Zarządzanie wydatkami** w systemie Microsoft Dynamics 365 Finance w wersji 10.0.25 lub nowszej.

Aby włączyć naliczanie diet, wykonaj poniższe czynności.

1. W obszarze **roboczym zarządzania funkcjami** znajdź i wybierz **funkcję Raporty o wydatkach, która została ponownie wyświetlona** na liście, a następnie wybierz opcję **Włącz teraz**.
2. Znajdź i zaznacz na liście funkcję **Interfejs raportu o wydatkach na dietę został przeprojektowany**, a następnie wybierz **Włącz teraz**.

## <a name="how-the-feature-works"></a>Jak działa funkcja

W tej sekcji przedstawiono przykłady trzech scenariuszy konfiguracji. Dla każdego przykładu pole **Obliczaj zmniejszenie liczby pole** jest ustawione na inną wartość. W przypadku wszystkich trzech przykładów łączna kwota zobowiązania jest taka sama do momentu zmniejszenia liczby zobowiązania. Po tym momencie łączna kwota zobowiązania różni się w każdym przykładzie.

Aby utworzyć koszt zwrotu z wszystkich trzech przykładów, wykonaj następujące czynności.

1. Przejdź do **obszar roboczy** \> **zarządzania wydatkami**.
2. Wybierz opcję **Nowy raport wydatków** lub zaznacz istniejący raport z wydatków na liście.
3. Dodaj nowy wydatek. W polu **Kategoria** wybierz opcję **Dieta**. Wybierz lokalizację oraz daty rozpoczęcia i zakończenia podróży. Wartość "na dzień" dla osób, które zostały pochłone, odszukane i bezdomne (inne koszty) jest obliczana na podstawie codziennej zależności ustawionej dla wybranej lokalizacji.

    Na przykład jako lokalizację należy wybrać **Redmond (USA)**. Dzienny limit dla tej lokalizacji to 150 dolarów USA (150 USD) za USD 75 i dla USD 5 osób. Data rozpoczęcia to 10 stycznia, a data zakończenia to 14 stycznia. Z tego powodu wybrany czas trwania wynosi pięć dni, po wybraniu konfiguracji są dni kalendarzowe z godziną, a wybrana godzina rozpoczyna się i kończy o 12:00 w dniu rozpoczęcia i zakończenia. Oto obliczenia:

    - Łączna kwota zobowiązania = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
    - Różnych fragmentów kwoty = 5 × (75 + 5) = USD 400

Jeśli podczas podróży podano je podczas posiłku, lunchu i posiłku, należy uwzględnić je jako zmniejszenie liczby osób.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Przykład 1: Na każdy dzień, w którym zmniejszenie liczby osób jest oparte na typie blokowania na trasy

W tym przykładzie zmniejszenie ceny o 30 procent w przypadku posiłku, 30 procent w przypadku lunchu i 40 procent w przypadku posiłku. Na stronie **Parametry zarządzania wydatkami** w polu **Obliczanie obniżenia jakości usług według pola** jest ustawiana wartość **Typ grupy danych na trasę**. Oto obliczenia, jeśli dla pracownika zostały dostarczone trzy rodzaje walut, dwa obiady i zera:

- Zniżka na posiłek = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112,50
- Posiłki i inne wydatki = 400 – 112,50 = USD 287,50
- Całkowita kwota do zapłaty = całkowity zasiłek - zniżka na posiłek = 1 150 – 112,50 = USD 1037,50

![Wydatki na diety, w przypadku których zniżka na posiłek zależy od rodzaju posiłku na podróż.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Przykład 2: Na każdy dzień, w którym zmniejszenie liczby osób jest oparte na typie blokowania na dzień

W tym przykładzie zmniejszenie ceny o 30 procent w przypadku posiłku, 30 procent w przypadku lunchu i 40 procent w przypadku posiłku. Na stronie **Parametry zarządzania wydatkami** w polu **Obliczanie obniżenia jakości usług według pola** jest ustawiana wartość **Typ grupy danych na dzień**. W tym przypadku w siatce **Posiłki** w oknie dialogowym **Edytuj wydatek** użytkownik odznacza pola wyboru, aby wskazać, które posiłki zostały mu zapewnione podczas podróży.

Oto na przykład obliczenia, jeśli zostało podane w ciągu pierwszych trzech dni podróży:

- Dzienna zniżka na posiłek dla każdego z trzech pierwszych dni = 75 × 30% = 22,50 USD
- Całkowita zniżka na posiłek = 3 × 22,50 = 67,50 USD
- Posiłki i drobne wydatki za dni 1-3 = 75 - 22,50 = 57,50 USD
- Suma posiłków i drobnych wydatków = Suma posiłków i drobnych wydatków w ciągu pięciu dni = 400 - 67,50 = 332,50 USD
- Całkowita kwota do zapłaty = Całkowita kwota - Zniżka na posiłki = 1 150 - 67,50 = 1 082,50 USD

![Wydatki na diety, w przypadku których zniżka na posiłek zależy od rodzaju posiłku na dzień.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Przykład 3: Diety, w przypadku których zniżki na posiłki zależą od liczby posiłków w ciągu dnia

W tym przykładzie zniżka na posiłek jest obliczana na podstawie liczby posiłków dostarczonych w ciągu dnia (tzn. w polu **Oblicz zniżkę na posiłek według** na stronie **Parametry zarządzania kosztami** ustawiono wartość **Liczba posiłków dziennie**). W tym przypadku w siatce **Posiłki** w oknie dialogowym **Edytuj wydatek** użytkownik odznacza pola wyboru, aby wskazać, które posiłki zostały mu zapewnione.
W tym przypadku zniżka na posiłki zależy tylko od liczby zapewnionych posiłków, a nie od rodzaju zapewnionego posiłku (śniadanie/obiad/kolacja).

Oto sposób obliczania diet, gdy dzienna dieta wynosi 150 USD na zakwaterowanie, 75 USD na posiłki i 5 USD na drobne wydatki:

- **Łączna kwota zobowiązania** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
- **Jeden posiłek:** Zniżka na posiłek = 20% = USD 15
- **Dwa posiłki:** Zniżka na posiłek = 50% = USD 37,50
- **Trzy posiłki:** Zniżka na posiłek = 100% = USD 75

Oto obliczenia dla **dodatku na posiłki i drobne wydatki**, który obejmuje 5 USD na drobne wydatki:

- Dzień 1 - zapewnione dwa posiłki = (75 - 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dzień 2 - zapewnione dwa posiłki = (75 - 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dzień 3 - Zapewnienie jednego posiłku = (75 - 15) + 5 = 60 + 5 = 65 USD
- Dzień 4 - zero posiłków = (75-0) + 5 = 75 + 5 = 80 USD
- Dzień 5 - zapewnione trzy posiłki = (75 - 75) + 5 = 0 + 5 = 5 USD

- Posiłki i koszty dodatkowe ogółem = Posiłki i koszty dodatkowe za dzień 1+ dzień 2 + dzień 3+ dzień 4+ dzień 5 = 235 USD
- Całkowita redukcja liczby posiłków = redukcja liczby posiłków dla dnia 1+ dnia 2 + dnia 3+ dnia 4+ dnia 5= 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Całkowita kwota do zapłaty = Całkowity zasiłek - Całkowita zniżka na posiłki = 1 150 USD - 165 USD = 985 USD

![Wydatki na diety, w przypadku których zniżka na posiłki jest uzależniona od liczby posiłków w ciągu dnia.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od wersji 10.0.23 programu Finance, jeśli korzystasz ze zmienionego interfejsu wydatków, nie możesz tworzyć wydatków na diety, których daty się pokrywają. Jeśli spróbujesz, otrzymasz komunikat o błędzie.
