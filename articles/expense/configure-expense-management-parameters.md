---
title: Konfigurowanie parametrów zarządzania wydatkami
description: W tym temacie opisano parametry, które kontrolują ogólny sposób zarządzania wydatkami.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 09da0f4e0c6aec97c93c10eb686513e782189f77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121051"
---
# <a name="configure-expense-management-parameters"></a>Konfigurowanie parametrów zarządzania wydatkami

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym temacie opisano parametry, które kontrolują ogólny sposób zarządzania wydatkami.

## <a name="general"></a>Ogólne

| Pole                                                    | Opis |
|----------------------------------------------------------|-------------|
| Standardowa stawka przebiegu                                 | Wprowadź stawkę zwrotu za koszty przebiegu. Ta stawka jest pomnożona przez przebieg wprowadzany dla wydatku w celu obliczenia kwoty zwrotu za koszty podróży. |
| Potwierdź cel wydatku                                 | Tę opcję należy włączyć, aby ograniczyć wybór użytkowników do istniejącego zestawu wartości skonfigurowanych w polu **Cel raportu wydatków** podczas tworzenia raportów o wydatkach. |
| Koszty osobiste płacone przez                                | Wybierz osobę, która jest odpowiedzialna za zapłatę dowolnej kwoty transakcji kartą kredytową, które są klasyfikowane jako osobiste. |
| Wyświetlanie całego raportu z wydatków w ramach raportu szczegółowego               | Wybierz tę opcję, aby wyświetlić wszystkie koszty z raportu z wydatków w momencie, gdy dane oryginalnego dokumentu są wyświetlane dla określonego załącznika, który został wygenerowany podczas księgowania raportu z wydatków. |
| Wstępna autoryzacja podróży jest obowiązkowa                 | Wybierz tę opcję, aby wymagać przesyłania i zatwierdzania wniosku wyjazdowego, zanim pracownik będzie mógł przesłać raport o wydatkach. |
| Zezwalaj na edycję dystrybucji przed zaksięgowaniem            | Umożliwia wskazanie, czy podczas księgowania może być edytowana dystrybucja raportu z wydatkami. |
| Ocena zasad zarządzania wydatkami                     | Wybierz kiedy koszty są oceniane w celu ustalenia, czy zasady wydatkowania zostały naruszone. Koszty mogą być oceniane pod kątem naruszeń przy wprowadzaniu i zapisywaniu wpisu wydatku lub przy przekazywaniu kosztów do zatwierdzenia. Wymagane reguły dotyczące przyjęć będą oceniane przy zapisywaniu wiersza wydatku. |
| Zezwalaj na wiersze wydatku międzyfirmowego                         | Umożliwia określenie, czy w raporcie z wydatków można wprowadzać koszty dla innych firm. |
| Zezwalaj na edycję kursu wymiany wydatków na kartach kredytowych | Wybierz tę opcję, aby zezwolić użytkownikowi na edycję kursu wymiany dla zaimportowanych kosztów karty kredytowej. |
| Pola hierarchii na wielu poziomach do wyświetlenia                  | Wybierz które pola zatwierdzania mają być widoczne, jeśli typ przydziału przepływu pracy ma być hierarchią, a wybrana **Hierarchia** jest ustawiona na używanie hierarchii zatwierdzania, zatwierdzania wielopoziomowego wydatku. Jeśli dla przepływu pracy jest używana wielopoziomowa hierarchia zatwierdzania, wybrane pola będą widoczne w raporcie z wydatków i mogą być edytowane. |
| Podaj numer karty kredytowej pracownika                        | Należy wybrać, czy w polu **Identyfikator karty** na stronie **Karty kredytowej** pracownika ma być wprowadzany numer 15-znakowy czy 16-znakowy. |
| Sprawdzanie poprawności zapotrzebowania przejazdowego                      | Tę opcję należy włączyć, aby ograniczyć wybór użytkowników do istniejącego zestawu wartości skonfigurowanych w polu **Cel raportu wydatków** podczas tworzenia zapotrzebowań wyjazdowych. |

## <a name="financial"></a>Finanse

| Pole                                                                                    | Opis |
|------------------------------------------------------------------------------------------|-------------|
| Nazwa dziennego arkusza księgi głównej                                                                | Wybierz nazwę arkusza księgi głównej, w którym są księgowane zatwierdzone raporty o wydatkach. |
| Włączanie zwrotu podatku od wydatków                                                        | Wybierz tę opcję, aby umożliwić zwrot podatku za kwalifikujące się koszty. Nie można wybrać tej opcji, jeśli jest włączone użycie podatku amerykańskiego i reguł podatkowych. |
| Księguj zaliczki gotówkowe natychmiast                                                           | Wybierz tę opcję, aby zaksięgować zatwierdzoną zaliczkę pieniężną po zakończeniu procesu płatności i transferu. Jeśli ta opcja nie jest zaznaczona, proces płatności i transferu powoduje wygenerowanie niezaksięgowanego dziennika głównego. |
| Poprawna data księgowania podczas księgowania                                                   | Wybierz tę opcję, aby zaktualizować datę księgowania podczas księgowania kosztów, jeśli bieżący okres jest wstrzymany lub zamknięty. Data księgowania będzie ustawiona na następny otwarty okres. |
| Zezwalaj na grupowanie transakcji na podstawie konta rozliczeniowego określonego w metodzie płatności       | Wybierz tę opcję, aby podsumować transakcje wydatków dla raportu z wydatków na podstawie konta rozliczeń określonego w polu opłaty za koszty. |
| Uwzględniony podatek                                                                             | Zaznacz tę opcję, aby domyślnie uwzględnić podatek w kwocie wydatku. |
| Uwalnianie przyszłych zobowiązań wiążących podczas zamykania wniosków wyjazdowych                                      | Wybierz tę opcję, aby zwolnić fundusze z procesu zatwierdzania po zamknięciu zatwierdzonego zapotrzebowania wyjazdowego. |
| Zezwalaj na wysyłanie wniosków wyjazdowych po przekroczeniu budżetu w kasie i budżecie projektu | Wybierz tę opcję, aby umożliwić pracownikom przesyłanie wniosków wyjazdowych do zatwierdzenia, mimo że przekroczony został dozwolony budżet ustalony w rejestrze budżetu lub dozwolony budżet projektu. |
| Zezwalaj na wysyłanie raportów wydatków po przekroczeniu budżetu w kasie i budżecie projektu     | Wybierz tę opcję, aby umożliwić pracownikom przesyłanie raportów wydatków do zatwierdzenia, mimo że przekroczony został dozwolony budżet ustalony w rejestrze budżetu lub dozwolony budżet projektu. |
| Zezwalaj na zatwierdzanie raportów wydatków tylko po przekroczeniu budżetu w kasie                 | Wybierz tę opcję, aby zezwolić osobom zatwierdzającym na zatwierdzanie raportów o wydatkach przekraczających dozwolony budżet ustawiony w rejestrze budżetu. |

## <a name="per-diem"></a>Dieta

| Pole                                 | Opis |
|---------------------------------------|-------------|
| Minimalna liczba godzin na dzień            | Wprowadź domyślną minimalną liczbę godzin, jaką pracownik musi przepracować w ciągu doby, aby uzyskać dostęp do diety na pokrycie kosztów związanych z podróżą. Ta wartość jest używana jako wartość domyślna tylko w polu **Minimum godzin** dla poziomów stawki diety. |
| Procent wyżywienia                          | Wprowadź domyślny procent diety na posiłki, używany podczas pierwszego i ostatniego dnia kosztów związanych z podróżą w przypadku, gdy pole **Oblicz redukcję posiłków o** ma wartość **Typ posiłku na dzień** lub **Liczba posiłków dziennie**. Dzień roboczy w ciągu pierwszego i ostatniego dnia może być krótszy niż standardowy dzień roboczy. Z tego względu kwota dzienna przypadająca na te dni może się różnić od kwoty standardowej. Jeśli procent jest ustawiony na **0** (zero), to potrącenia za pierwsze i ostatnie dni będą wynosić 0,00. |
| Procent hotelu                         | Wprowadź domyślny procent diety za hotele używane pierwszego i ostatniego dnia podróży związanej z wydatkiem. Dzień roboczy w ciągu pierwszego i ostatniego dnia może być krótszy niż standardowy dzień roboczy. Z tego względu kwota dzienna przypadająca na te dni może się różnić od kwoty standardowej. Jeśli procent jest ustawiony na **0** (zero), to potrącenia za pierwsze i ostatnie dni będą wynosić 0,00. |
| Inny procent                         | Wprowadź domyślny procent diety za inne wydatki pierwszego i ostatniego dnia podróży związanej z wydatkiem. Dzień roboczy w ciągu pierwszego i ostatniego dnia może być krótszy niż standardowy dzień roboczy. Z tego względu kwota dzienna przypadająca na te dni może się różnić od kwoty standardowej. Jeśli procent jest ustawiony na **0** (zero), to potrącenia za pierwsze i ostatnie dni będą wynosić 0,00. |
| Obniżka w procentach za śniadanie | Wprowadź kwotę, o której wysokość dieta jest redukowana za śniadanie. Jeśli na przykład pracownik otrzymuje bezpłatne śniadanie, może zaistnieć konieczność zmniejszenia kwoty diety o 10 procent. |
| Obniżka w procentach za lunch     | Wprowadź kwotę, o której wysokość dieta jest redukowana za lunch. Jeśli na przykład pracownik otrzymuje bezpłatny lunch, może zaistnieć konieczność zmniejszenia kwoty diety o 15 procent. |
| Obniżka w procentach za obiad    | Wprowadź kwotę, o której wysokość dieta jest redukowana za obiad. Jeśli na przykład pracownik otrzymuje bezpłatny obiad, może zaistnieć konieczność zmniejszenia kwoty diety o 25 procent. |
| Oblicz redukcję za pożywienie według           | Określ, jak system ma obliczać obniżkę diety za posiłki, określając, czy obniżka jest oparta na typie posiłku na podróż, czy na dzień, czy też jest oparta na liczbie dozwolonych posiłków dziennie. |
| Zaokrąglenie diety dziennej                     | Wybierz typ zaokrąglenia używanego do obliczania wydatków dziennych. W przypadku wybrania zwykłego zaokrąglania każdy z wydatków dziennych zawierający połówkę jednostki (kwotę 0,50), jest zaokrąglany w górę do kwoty jedności (1,00), a wydatek z kwotą kończącą się na mniej niż 0,50 jest zaokrąglany w dół do wartości 0,00. |
| Obliczanie kalkulacji diety dziennej na podstawie          | Umożliwia określenie, czy kwota na diety jest oparta na dniu kalendarzowym czy na okresie 24 godzinnym. |

## <a name="fax-cover-pages"></a>Strony tytułowe faksu

| Pole                          | Opis |
|--------------------------------|-------------|
| Instrukcje                   | Wprowadź instrukcje, jakich muszą przestrzegać pracownicy tworząc stronę tytułową faksu, który jest używany do wysyłania potwierdzeń powiązanych z raportem o wydatkach. Aby wprowadzić odpowiedni dla języka tekst, który będzie widoczny na podstawie języka użytkownika, wybierz pozycję **Tłumaczenia**. |
| Identyfikator użytkownika (informacje o kodzie kreskowym) | Wybierz tę opcję, aby przechowywać unikatowy identyfikator pracownika w kodzie kreskowym, który jest używany na stronie tytułowej faksu. |
| Kod kreskowy                       | Wybierz kod kreskowy używany na stronie tytułowej faksu. Kody kreskowe 39 i 128 są obsługiwane w zarządzaniu wydatkami. |

## <a name="anti-corruption"></a>Zapobieganie korupcji

| Pole                                 | Opis |
|---------------------------------------|-------------|
| Wyświetlanie zaświadczeń przeciwdziałających korupcji   | Wybierz tę opcję, aby podczas tworzenia raportu z wydatkami był wyświetlany tekst antykorupcyjny. Następnie można włączyć określoną kategorię wydatków, która wymagać będą złożenia w raporcie oświadczeń antykorupcyjnych. Na przykład kategoria upominkowa powiązana z oficjalnymi wydatkami dla urzędnika administracji rządowej może wymagać, aby pracownik zatwierdził, że wydatek przestrzega zasad firmy dotyczących urzędników administracji rządowej. |
| Komunikat antykorupcyjny dla osoby przesyłającej | Wprowadź tekst, który ma być wyświetlany pracownikowi tworzącemu raport o wydatkach. Aby wprowadzić odpowiedni dla języka tekst, który będzie widoczny na podstawie języka użytkownika, wybierz pozycję **Tłumaczenia**. |
| Komunikat antykorupcyjny dla osoby zatwierdzającej  | Wprowadź tekst, który ma być wyświetlany pracownikowi zatwierdzającemu raport o wydatkach podczas tworzenia raportu. Aby wprowadzić odpowiedni dla języka tekst, który będzie widoczny na podstawie języka użytkownika, wybierz pozycję **Tłumaczenia**. |
