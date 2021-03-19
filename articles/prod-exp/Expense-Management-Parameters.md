---
title: Parametry zarządzania wydatkami
description: Poniższe parametry kontrolują zachowanie funkcji zarządzania wydatkami.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 498d597fe811192ce313a1b0384de81e7ef55c58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271931"
---
# <a name="expense-management-parameters"></a>Parametry zarządzania wydatkami


Parametry kontrolują ogólne zachowanie funkcji zarządzania wydatkami.

### <a name="general"></a>Ogólne

| **Pole**                                                | **Opis**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardowa stawka przebiegu**                             | Wprowadź stawkę zwrotu za koszty przebiegu. Ta stawka będzie pomnożona przez przebieg wprowadzany dla wydatku w celu obliczenia kwoty zwrotu za koszty podróży.                       |
|**Koszty osobiste płacone przez**                             | Wybierz osobę, która jest odpowiedzialna za zapłatę dowolnej kwoty transakcji kartą kredytową, klasyfikowaną jako osobista.                                                                                                     |
|**Wyświetlanie całego raportu z wydatków w ramach raportu szczegółowego**               | Wybierz tę opcję, aby pokazać wszystkie koszty z raportu z wydatków w momencie, gdy dane oryginalnego dokumentu są wyświetlane dla określonego załącznika, który został wygenerowany podczas księgowania raportu z wydatków.              |
|**Wstępna autoryzacja podróży jest obowiązkowa**                 | Wybierz tę opcję, aby wymagać przesyłania i zatwierdzania wniosku wyjazdowego, zanim pracownik będzie mógł przesłać raport o wydatkach.                                                                    |
|**Zezwalaj na edycję dystrybucji przed zaksięgowaniem**            | Umożliwia wskazanie, czy przed księgowaniem może być edytowana dystrybucja raportu z wydatkami.                                                                                                                 |
|**Ocena zasad zarządzania wydatkami**                     | Wybierz kiedy koszty są oceniane w celu ustalenia, czy zasady wydatkowania zostały naruszone. Koszty mogą być sprawdzane pod kątem naruszeń przy wprowadzaniu i zapisywaniu wpisu wydatku lub przy przekazywaniu kosztów do zatwierdzenia. Wymagane reguły dotyczące przyjęć będą sprawdzane przy zapisywaniu wiersza wydatku.                   |
|**Zezwalaj na wiersze wydatku międzyfirmowego**                         | Umożliwia określenie, czy w ramach raportu z wydatków można wprowadzać koszty dla innych firm.                                                                                                          |
|**Zezwalaj na edycję kursu wymiany wydatków na kartach kredytowych** | Wybierz tę opcję, aby zezwolić użytkownikowi na edycję kursu wymiany dla zaimportowanych kosztów karty kredytowej.                                                                        |
|**Pola hierarchii na wielu poziomach do wyświetlenia**                  | Wybierz które pola zatwierdzania mają być wyświetlane, jeśli typ przydziału przepływu pracy raportu z wydatków ma być hierarchią, a wybrana hierarchia jest ustawiona na używanie hierarchii wielopoziomowego zatwierdzania wydatku. Jeśli dla przepływu pracy jest używana wielopoziomowa hierarchia zatwierdzania, wybrane pola będą wyświetlane w raporcie z wydatków i mogą być edytowane. |
|**Podaj numer karty kredytowej pracownika (aktualizacja z lipca 2017 roku)**     | Należy wybrać, czy w polu **Identyfikator karty** na stronie **Karty kredytowej** pracownika ma być wprowadzany numer 15-znakowy czy 16-znakowy.                                                                          |

### <a name="financial"></a>Finanse

| **Pole**                                                            | **Opis**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nazwa dziennego arkusza księgi głównej**                                         | Wybierz nazwę arkusza księgi głównej, w którym są księgowane zatwierdzone raporty o wydatkach.            |
|**Włączanie zwrotu podatku od wydatków**                                  | Wybierz tę opcję, aby umożliwić zwrot podatku za kwalifikujące się koszty. Nie można uruchomić tej opcji, jeśli jest włączone użycie podatku amerykańskiego i reguł podatkowych.      |
|**Księguj zaliczki gotówkowe natychmiast**                                     | Wybierz tę opcję, aby zaksięgować zatwierdzoną zaliczkę pieniężną po zakończeniu procesu płatności i transferu. Jeśli ta opcja nie jest zaznaczona, proces płatności i transferu spowoduje wygenerowanie niezaksięgowanego dziennika głównego. |
|**Poprawna data księgowania podczas księgowania**                             | Wybierz tę opcję, aby zaktualizować datę księgowania podczas księgowania kosztów, jeśli bieżący okres jest wstrzymany lub zamknięty. Data księgowania będzie ustawiona na następny otwarty okres.   |
|**Zezwalaj na grupowanie transakcji na podstawie konta rozliczeniowego określonego w metodzie płatności**      | Wybierz tę opcję, aby podsumować transakcje wydatków dla raportu z wydatków na podstawie konta rozliczeń określonego w polu opłaty za koszty.   
|**Uwzględniony podatek**                                                   | Zaznacz tę opcję, aby domyślnie uwzględnić podatek w kwocie wydatku.             |
|**Uwalnianie przyszłych zobowiązań wiążących podczas zamykania wniosków wyjazdowych**            | Wybierz tę opcję, aby zwolnić fundusze z procesu zatwierdzania po zamknięciu zatwierdzonego zapotrzebowania wyjazdowego.                                                                                   |
|**Zezwalaj na wysyłanie wniosków wyjazdowych po przekroczeniu budżetu w kasie i budżecie projektu** | Wybierz tę opcję, aby umożliwić pracownikom przesyłanie wniosków wyjazdowych do zatwierdzenia, mimo że przekroczony został dozwolony budżet ustalony w rejestrze budżetu lub dozwolony budżet projektu.            |
|**Zezwalaj na wysyłanie raportów wydatków po przekroczeniu budżetu w kasie i budżecie projektu**    | Wybierz tę opcję, aby umożliwić pracownikom przesyłanie raportów wydatków do zatwierdzenia, mimo że przekroczony został dozwolony budżet ustalony w rejestrze budżetu lub dozwolony budżet projektu.                |
|**Zezwalaj na zatwierdzanie raportów wydatków tylko po przekroczeniu budżetu w kasie**                | Wybierz tę opcję, aby zezwolić osobom zatwierdzającym na zatwierdzanie raportów o wydatkach przekraczających dozwolony budżet ustawiony w rejestrze budżetu.                                                                       |

### <a name="per-diem"></a>Dieta

| **Pole**                             | **Opis**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimalna liczba godzin na dzień**           | Wprowadź domyślną minimalną liczbę godzin, jaką pracownik musi przepracować w ciągu doby, aby uzyskać dostęp do diety na pokrycie kosztów związanych z podróżą.  Ta wartość jest używana tylko jako wartość domyślna tylko w polu Minimum godzin dla poziomów stawki diety.                                                                                      |
|**Procent wyżywienia**                          | Wprowadź domyślny procent diety na posiłki, używany podczas pierwszego i ostatniego dnia kosztów związanych z podróżą w przypadku, gdy pole **Oblicz redukcję posiłków o** ma wartość **Typ posiłku na dzień** lub **Liczba posiłków dziennie**. Dzień roboczy w ciągu pierwszego i ostatniego dnia może być krótszy niż standardowy dzień. Z tego względu kwota dzienna przypadająca na takie dni może się różnić od kwoty standardowej. Jeśli procent jest ustawiony na 0 (zero), wtedy potrącenia za pierwsze i ostatnie dni będą wynosić 0,00. |
|**Procent hotelu**                        | Wprowadź domyślny procent diety za hotele używane pierwszego i ostatniego dnia podróży związanej z wydatkiem. Dzień roboczy w ciągu pierwszego i ostatniego dnia może być krótszy niż standardowy dzień. Z tego względu kwota dzienna przypadająca na takie dni może się różnić od kwoty standardowej. Jeśli procent jest ustawiony na 0 (zero), wtedy potrącenia za pierwsze i ostatnie dni będą wynosić 0,00.                                              |
|**Inny procent**                        | Wprowadź domyślny procent diety za inne wydatki pierwszego i ostatniego dnia podróży związanej z wydatkiem. Dzień roboczy w ciągu pierwszego i ostatniego dnia może być krótszy niż standardowy dzień. Z tego względu kwota dzienna przypadająca na takie dni może się różnić od kwoty standardowej. Jeśli procent jest ustawiony na 0 (zero), wtedy potrącenia za pierwsze i ostatnie dni będą wynosić 0,00.                                                                                                     |
|**Obniżka w procentach za śniadanie** | Wprowadź kwotę, o którą dieta jest redukowana za śniadanie. Jeśli na przykład pracownik otrzymuje bezpłatne śniadanie, może zaistnieć konieczność zmniejszenia kwoty diety o 10 procent.                               |
|**Obniżka w procentach za lunch**    | Wprowadź kwotę, o której wysokość dieta jest redukowana za lunch. Jeśli na przykład pracownik otrzymuje bezpłatny lunch, może zaistnieć konieczność zmniejszenia kwoty diety o 15 procent.                                       |
|**Obniżka w procentach za obiad**   | Wprowadź kwotę, o której wysokość dieta jest redukowana za obiad. Jeśli na przykład pracownik otrzymuje bezpłatny obiad, może zaistnieć konieczność zmniejszenia kwoty diety o 25 procent.                                     |
|**Oblicz redukcję za pożywienie według**         | Wybierz, w jaki sposób system ma obliczać obniżkę diety za posiłki, określając, czy obniżka jest oparta na typie posiłku na podróż, czy na dzień, czy też redukcja jest oparta na liczbie dozwolonych posiłków dziennie.|
|**Zaokrąglenie diety dziennej**                  | Wybierz typ zaokrąglenia używanego do obliczania wydatków dziennych. W przypadku wybrania zwykłego zaokrąglania każdy z wydatków dziennych zawierający połówkę jednostki (kwotę 0,50), jest zaokrąglany w górę do kwoty jedności (1,00), a wydatek z kwotą kończącą się na mniej niż 0,50 jest zaokrąglany w dół do wartości 0,00.                                                                                              |
|**Obliczanie kalkulacji diety dziennej na podstawie**         | Umożliwia określenie, czy kwota na diety jest oparta na dniu kalendarzowym czy na okresie 24 godzinnym.       |

### <a name="fax-cover-pages"></a>Strony tytułowe faksu

| **Pole**                      | **Opis**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instrukcje**                   | Wprowadź instrukcje, jakich muszą przestrzegać pracownicy tworząc stronę tytułową faksu, który jest używany do wysyłania potwierdzeń powiązanych z raportem o wydatkach. Aby wprowadzić odpowiedni dla języka tekst, który będzie widoczny na podstawie języka użytkownika, wybierz pozycję **Tłumaczenia**. |
|**Identyfikator użytkownika (informacje o kodzie kreskowym)** | Wybierz tę opcję, aby przechowywać unikatowy identyfikator pracownika w kodzie kreskowym, który jest używany na stronie tytułowej faksu.                 |
|**Kod kreskowy**                      | Wybierz kod kreskowy używany na stronie tytułowej faksu. Kody kreskowe 39 i 128 są obsługiwane w zarządzaniu wydatkami.               |

### <a name="anti-corruption"></a>Zapobieganie korupcji

|                 <strong>Pole</strong>                 |                                                                                                                                                                                            <strong>Opis</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Wyświetlanie zaświadczeń przeciwdziałających korupcji</strong>  | Wybierz tę opcję, aby podczas tworzenia nowego raportu z wydatkami był wyświetlany tekst antykorupcyjny. Następnie można włączyć określoną kategorię wydatków, która wymagać będą złożenia w raporcie oświadczeń antykorupcyjnych. Na przykład kategoria upominkowa powiązana z oficjalnymi wydatkami dla urzędnika administracji rządowej może wymagać, aby pracownik zatwierdził, że wydatek przestrzega zasad firmy dotyczących urzędników administracji rządowej. |
| <strong>Komunikat antykorupcyjny dla osoby przesyłającej</strong> |                                                                                             Wprowadź tekst, który będzie wyświetlany pracownikiem podczas tworzenia nowego raportu dotyczącego wydatków. Aby wprowadzić odpowiedni dla języka tekst, który będzie widoczny na podstawie języka użytkownika, wybierz pozycję <strong>Tłumaczenia</strong>.                                                                                             |
| <strong>Komunikat antykorupcyjny dla osoby zatwierdzającej</strong>  |                                                                                             Wprowadź tekst, który będzie wyświetlany pracownikom zatwierdzającym podczas tworzenia nowego raportu dotyczącego wydatków. Aby wprowadzić odpowiedni dla języka tekst, który będzie widoczny na podstawie języka użytkownika, wybierz pozycję <strong>Tłumaczenia</strong>.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]