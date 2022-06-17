---
title: Nowości z maja 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten artykuł zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations w maju 2021 r. dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930423"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości z maja 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse Dynamics 365 w wersji 4.10.0.186
- Zarządzanie projektami i księgowymi w środowiskach aplikacji finansowe i operacyjne wersja 10.0.18

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- [Tryby planowania](../project-management/scheduling-modes.md): Kierownicy projektów mogą zdefiniować, czy projekt powinien być zarządzany w trybie harmonogramu stałego czasu trwania, stałej pracy lub stałych jednostek.
- [Ustawianie przebiegu przy użyciu poziomów stawek kilometrowych](../expense/set-up-mileage.md): Aktualizacja poziomów stawek kilometrowych dla raportów wydatków pracowników.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

Następująca lista zawiera mapowania podwójnego zapisu, które zostały zmodyfikowane lub dodane w wydaniu Project Operations z maja 2021 roku.

| Mapowanie encji | Wersja zaktualizowana | Komentarze |
| --- | --- | --- |
| Źródło danych projektu (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synchronizacja umowy projektowej z warunkami płatności klienta. |
| Propozycja faktury za projekt V2 (faktury) | 1.0.0.3 | Synchronizacja terminów płatności faktur proforma. |
| Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Aktualizacje dotyczące jakości |
| Projekty V2 (msdyn\_projects) | 1.0.0.2 | Aktualizacje dotyczące jakości |

Zawsze uruchamiaj najnowszą wersję mapy w swoim środowisku i włączaj wszystkie powiązane mapy tabelaryczne podczas aktualizacji rozwiązania Project Operations Dataverse i wersji rozwiązania aplikacji finansowych i operacyjnych. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli najnowsza wersja mapy nie zostanie aktywowana. Aktywną wersję mapy można zobaczyć w kolumnie  **Wersja**  na stronie  **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś niestandardową mapę tabeli, będziesz trzeba ponownie zastosować zmiany. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem brakujących kolumn tabeli na mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) w przewodniku rozwiązywania problemów związanych z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2227635 | Wartości w polach **Grupa jednostek** i **Jednostki** są domyślnie przypisane do produktu w **Oszacowania materiału**. |
| Rozliczenia i ceny | 2234127 | Pole **Identyfikator zadania** jest teraz poprawnie integrowane z wartościami rzeczywistymi projektu Dataverse po zaksięgowaniu faktury dostawcy. |
| Rozliczenia i ceny | 2235564 | Zapisanie wiersza dziennika zapewnia, że waluta wyświetlana w pozycji wiersza dziennika jest zgodna z walutą domyślną dla wiersza po zapisaniu. |
| Rozliczenia i ceny | 2246671 | Uczynienie transakcji nieobciążalnej podczas fakturowania powoduje odwrócenie pierwotnego rekordu sprzedaży nieobciążonej i utworzenie nowego rekordu sprzedaży nieobciążonej jako nieobciążalnej. |
| Rozliczenia i ceny | 2264042 | Poprawna korekta faktury nie może zostać zablokowana, jeżeli w środowisku istnieje nieważny szczegół korekty faktury. |
| Rozliczenia i ceny | 2146367 | Mapowanie nagłówka faktury projektu z podwójnym zapisem zostało rozszerzone o warunki płatności. |
|   Zarządzanie szansami sprzedaży | 2086888 | Nie dodawaj ról i kategorii, które są nieaktywne przed skopiowaniem oferty do ról i kategorii płatnych w nowo skopiowanej ofercie. |
|   Zarządzanie szansami sprzedaży | 2234376 | Pola tylko do odczytu są wyszarzone w siatce **Oszacowania materiałów**. |
|   Zarządzanie szansami sprzedaży | 2238337 | Wycena oparta na kontakcie może zostać zapisana, nawet jeśli nie jest powiązana z cennikiem projektu. |
|   Zarządzanie szansami sprzedaży | 2239810 | Zamknięcie oferty jako straconej zamyka również powiązany z nią projekt i anuluje wszelkie rezerwacje. |
| Planowanie i śledzenie projektu | 2099559 | Dodano dodatkowe sprawdzanie poprawności stanu systemu przed otwarciem siatki **Zadania projektu**. |
| Planowanie i śledzenie projektu | 2178987 | Naprawiono przejściowy błąd występujący podczas wybierania **Następnego etapu** na stronie **Projektu**. |
| Zarządzanie zasobami | 2224817 | Funkcjonalność rozszerzania rezerwacji domyślnie ustawia prawidłowy status rezerwacji. |
| Wpis czasu | 2202476 | Strona **Wpis czasowy** wykorzystuje teraz kontrolę siatki reaktywnej i naprawia takie problemy, jak nieprawidłowe wyrównanie siatki. |
| Wpis czasu | 2223377 | Wprowadzanie czasu pracy jest ukryte w sekcji **Powiązane** na stronie **Zasoby możliwe do zarezerwowania**, aby uniknąć zamieszania z użytecznością. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Zarządzanie projektami i księgowanie | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations dla scenariuszy opartych na zasobach: Nie można przekonwertować oferty na wygraną z powodu błędu integracji. |
| Zarządzanie projektami i księgowanie | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: pojawia się komunikat o błędzie podczas próby skojarzenia wiersza kontraktu z identyfikatorem projektu z powodu sprawdzenia nakładających się wierszy kontraktu i typów transakcji. |
| Zarządzanie projektami i księgowanie | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** ustawia adres faktury źródła finansowania od innego klienta. |
| Podróże i wydatki | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Może wystąpić błąd księgowania związany z ustawieniem przebiegu. |
| Podróże i wydatki | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Ta funkcja, **Podział na osobiste** w transakcjach wydatków walutowych, nie działa. |
| Podróże i wydatki | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | W rozwijanych wartościach kategorii wydatków wyświetlane są nieprawidłowe kategorie dla delegatów, niezależnie od tego, czy są oni zasobami. |
| Podróże i wydatki | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Nie można zapisać raportu wydatków międzyfirmowych z powodu błędu **sprawdzania poprawności zasobu/kategorii**. |
| Podróże i wydatki | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Nieprawidłowa metoda obliczania kursu podziału w raporcie z wydatkami zawiera wiersze podziału. |
| Podróże i wydatki | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Nie można zaksięgować raportu wydatków między firmami, gdy uwzględniony jest podatek od sprzedaży, a typ konta kompensacyjnego w metodzie płatności to **Pracownik**. |
| Podróże i wydatki | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Encja danych **TrvRequisitionLine** i unikalny indeks są powiązane. |
| Podróże i wydatki | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Raport wydatków obsługuje tworzenie i aktualizację linii dokumentów źródłowych. |
| Podróże i wydatki | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Nieprawidłowy arkusz księgi podrzędnej jest wyświetlany w scenariuszu międzyfirmowym, jeśli podatek od sprzedaży jest księgowany w docelowej firmie. |
| Podróże i wydatki | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: szacowania wydatków nie są usuwane z Finance po ich usunięciu w Dataverse. |
| Podróże i wydatki | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Gdy kategoria wydatków jest kategorią niezwiązaną z projektem, wymiary finansowe wybrane na stronie **Wydatki** nie są kopiowane do raportu kosztów. |
