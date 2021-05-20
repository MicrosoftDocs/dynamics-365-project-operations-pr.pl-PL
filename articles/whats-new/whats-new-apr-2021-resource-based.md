---
title: Nowości z kwietnia 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w wydaniu Project Operations z kwietnia 2021 r. dla scenariuszy obejmujących zasoby/niemagazynowanie.
author: sigitac
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 339a488908add09c5e4f62568bb83b78450e7082
ms.sourcegitcommit: 69fadd3ce475d6aed2e1ed81a15becb28f020eb9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935487"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości z kwietnia 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.9.0.221
- Zarządzanie projektami i ich księgowanie w wersji 10.0.17 środowiska Dynamics 365 Finance

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- Materiały niezabędowe do projektów. Kluczowe możliwości to:
  - Kalkulacji i kalkulacji cen materiałów niezabędowych w cyklu sprzedaży projektu. Więcej informacji można znaleźć w: [Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Śledzenie wykorzystania materiałów niezamagazynowanych podczas realizacji projektu. Aby uzyskać więcej informacji, zobacz [Rejestrowanie użycia materiałów w projektach i zadaniach projektów](../material/material-usage-log.md).
  - Fakturowanie kosztów materiałów niezamagazynowanych. Aby uzyskać więcej informacji, zobacz [Zarządzanie zaległością rozliczenia](../proforma-invoicing/manage-billing-backlog.md).
  - Aby uzyskać informacje na temat konfigurowania tej funkcji, zobacz [Konfigurowanie materiałów niemagazynowanych i oczekujących faktur od dostawcy](../procurement/configure-materials-nonstocked.md)
- Fakturowanie oparte na zadaniach: Dodano możliwość kojarzenia zadań projektu z wierszami umowy w sprawie projektu, tym samym poddając je tej samej metodzie rozliczenia, częstotliwości fakturowania i klientom, co w wierszu umowy. To skojarzenie zapewnia dokładne fakturowanie, księgowanie, szacowanie przychodów i uznawanie, aby działały zgodnie z tą konfiguracją w zadaniach projektu.
- Nowe interfejsy API w Dynamics 365 Dataverse umożliwiają tworzenie, aktualizowanie i usuwanie operacji za pomocą **Encji planowania**. Aby uzyskać więcej informacji, zobacz [Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

Następująca lista zawiera mapowania podwójnego zapisu, które zostały zmodyfikowane lub dodane w wydaniu Project Operations z kwietnia 2021 roku.

| **Mapowanie encji** | **Wersja zaktualizowana** | **Komentarze** |
| --- | --- | --- |
| Wartości rzeczywiste integracji Project Operations (msdyn\_actuals) | 1.0.0.14 | Mapowanie zmodyfikowane w celu zsynchronizowania rzeczywistych wartości projektu materiałów. |
| Encja integracji Project Operations na potrzeby oszacowania kosztów (msdyn\_estimateslines) | 1.0.0.2 | Dodano synchronizację wiersza kontraktu projektu do aplikacji Finance and Operations w celu do obsługi rozliczeń w oparciu o zadania. |
| Encja integracji Project Operations na potrzeby oszacowania godzinowego (msdyn\_resourceassignments) | 1.0.0.5 | Dodano synchronizację wiersza kontraktu projektu do aplikacji Finance and Operations w celu do obsługi rozliczeń w oparciu o zadania. |
| Tabela integracji Project Operations dla szacowania materiałów (msdyn\_estimatelines) | 1.0.0.0 | Nowe mapowanie tabel służące do synchronizowania szacowania materiałów z Dataverse do aplikacji Finance and Operations. |
| Integracja w Project Operations encji eksportu faktury dostawcy projektu (msdyn\_projectvendorinvoices) | 1.0.0.0 | Nowe mapowanie tabel służące do synchronizowania nagłówków faktur dostawców z aplikacji Finance and Operations do Dataverse. |
| Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Nowe mapowanie tabel służące do synchronizowania wierszy faktur dostawców z aplikacji Finance and Operations do Dataverse. |

Zawsze należy uruchomić najnowszą wersję mapy w środowisku i włączyć wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance and Operations. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli najnowsza wersja mapy nie zostanie aktywowana. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, należy wybrać **Wersję mapowania tabeli**, a następnie zapisać wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś niestandardową mapę tabeli, będziesz trzeba ponownie zastosować zmiany. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem brakujących kolumn tabeli na mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) w przewodniku rozwiązywania problemów związanych z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations w Dynamics 365 Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2124532 | Przycisk **Korekta faktury** jest wyświetlany na fakturze proforma, gdy kwota zaliczki lub zastosowana kwota zaliczki jest obecna na oryginalnej fakturze. Przycisk będzie wyświetlany tylko w środowiskach z Finance w wersji 10.0.19 lub nowszej. |
| Rozliczenia i ceny | 2224568 | Dodano logikę umożliwiającą dostosowania, które obejmują wywoływanie wtyczki potwierdzającej fakturę. |
| Rozliczenia i ceny | 2101098 | Ulepszono logikę domyślnych pól faktury proforma: **Adres rozliczeniowy**, **Nazwa płatnika** i **Warunki płatności** są teraz domyślnie ustawione w odpowiednim rekordzie klienta umowy projektu. |
| Rozliczenia i ceny | 2021413 | Zaktualizowanie pól **Koszt rzeczywisty** i **Sprzedaż** w encji **Zadanie** w celu dołączyć do zadań wartości sprzedaży z nierozliczonych i rozliczonych kosztów. |
| Rozliczenia i ceny | 2182110 | Podczas kopiowania kontraktu dotyczącego projektu identyfikator wiersza kontraktu jest ponownie generowany w docelowej umowie dotyczącej projektu, aby zapewnić jego unikalność. |
| Zarządzanie szansami sprzedaży | 2186741 | Dodano sprawdzanie poprawności, aby upewnić się, że nie można zaktualizować pola **Pochodzenia** i **Typu transakcji** na istniejących szczegółach wiersza oferty. |
| Zarządzanie szansami sprzedaży | 2191353 | Nie można tworzyć punktów kontrolnych dla czasowej i istotnej linii kontraktu. |
| Zarządzanie szansami sprzedaży | 2216956 | Rozwiązane problemy dotyczące **Aktualizowania cen**. |
| Planowanie i śledzenie | 2182979 | Udoskonalono funkcję kopiowania projektu, aby zapewnić kopiowanie wierszy kosztorysu z oryginalnego projektu. |
| Planowanie i śledzenie | 2184144 | Udoskonalono funkcję kopiowania projektu, aby zapewnić kopiowanie nazwy pozycji zasobu z oryginalnego projektu. |
| Planowanie i śledzenie | 2184799 | Kopia projektu: zaostrzono kontrolę, aby nie można było zmienić szacowanej daty rozpoczęcia podczas kopiowania. |
| Planowanie i śledzenie | 2185134 | Kopia projektu: Szacunkowa data rozpoczęcia projektu docelowego to dzisiejsza data. |
| Planowanie i śledzenie | 2196373 | Kopia projektu: upewnij się, że rekordy kierownika projektu i członka zespołu nie są zduplikowane w zespole projektowym. |
| Planowanie i śledzenie | 2211833 | Kopia projektu: przydziały zasobów są kopiowane ze źródłowego zadania projektu do projektu docelowego. |
| Planowanie i śledzenie | 2186541 | Rozwiązane problemy w siatce **Szacowanie** podczas grupowania według zasobu. |
| Planowanie i śledzenie | 2166906 | Kategoria transakcji z zadania musi być skopiowana do encji **Przypisanie zasobów**. |
| Zarządzanie zasobami | 2125362 | Rozwiązano problemy z tworzeniem ogólnego członka zespołu przy użyciu metody alokacji opartej na godzinach. |
| Czas i wydatek | 2113603 | Naprawiono problem związany z dostosowywaniem, polegający na usuwaniu atrybutów ze strony **Wpis czasu**. System sprawdza teraz, czy atrybut istnieje na stronie przed uzyskaniem do nich dostępu za pomocą skryptu. |
| Czas i wydatek | 2204377 | Skopiowane czaskopiki muszą być wyświetlane automatycznie po wybraniu opcji **Kopiuj tydzień** podczas wprowadzania czasu. |
| Czas i wydatek | 2209059 | Pole **Stan** można edytować dla wpisów czasu Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Omówienie zarządzania projektami i księgowania w Dynamics 365 Finance

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Zarządzanie projektami i księgowanie | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminacja szacowania wstecznego nie działa w sekcji **Okresowe**.  |
| Zarządzanie projektami i księgowanie | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funkcja **Korekta księgowa** powoduje problem z kontami księgi, dla których nie wybrano opcji **Nie zezwalaj na ręczne wprowadzanie**. |
| Zarządzanie projektami i księgowanie | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Dodano logikę biznesową do przetwarzania faktur korygujących, w tym kwoty zaliczki lub zastosowanej kwoty zaliczki. |
| Zarządzanie projektami i księgowanie | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Księgowanie PWT wartości sprzedaży podczas międzyfirmowego fakturowania projektu wybiera nieoczekiwane konto. |
| Zarządzanie projektami i księgowanie | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Podczas pracy z retainerami w ramach Project Operations zmiana domyślnego projektu w umowie po zafakturowaniu przedpłat powoduje problemy z przychodzącymi potrąceniami. |
| Zarządzanie projektami i księgowanie | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | W Project Operations usunięcie projektu z umowy powinno w razie potrzeby zresetować domyślny projekt umowy. |
| Zarządzanie projektami i księgowanie | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | W Project Operations niewłaściwe wiersze wydatków są wyświetlane na liście **Dodaj wiersz** na fakturze międzyfirmowej. |
| Zarządzanie projektami i księgowanie | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | W Project Operations strona **Umowa zakupu** nie jest widoczna w firmach Finance, które są zintegrowane z Project Operations. |
| Zarządzanie projektami i księgowanie | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Z powodu błędu integracji Dataverse nie można przekonwertować oferty na wygraną w Project Operations. |
| Zarządzanie projektami i księgowanie | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** może ustawić adres faktury źródła finansowania od innego klienta.  |
| Zarządzanie projektami i księgowanie | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | W Project Operations żadne wymiary nie są wybierane podczas tworzenia faktury księgowania dla transakcji. |
| podróż i wydatki | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Saldo zaliczki gotówkowej nie jest aktualizowane dla raportu z wydatków, jeśli zostało zatwierdzone i zaksięgowane wiersz po wierszu. |
| Podróże i wydatki | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Podatki dla szczegółowych raportów wydatków międzyfirmowych nie są obliczane poprawnie. |
| Podróże i wydatki | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Dodatkowe pola związane z projektami są wyświetlane na przeprojektowanej stronie **Raporty z wydatków międzyfirmowych**. |
| Podróże i wydatki | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | W nagłówkach pokwitowań raportów z wydatków pojawia się niepoprawny komunikat o błędzie. |
| Podróże i wydatki | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Raport z wydatków jest nieprawidłowo księgowany w scenariuszu międzyfirmowym, jeśli podatek od sprzedaży jest księgowany w docelowej firmie. |
| Podróże i wydatki | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Daty składania raportów nie są drukowane w zatwierdzonych raportach z wydatków. |
| Podróże i wydatki | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Pola **Data zaakceptowana** i **Data odrzucenia** nie są wypełniane po zatwierdzeniu wydatku. |
| Podróże i wydatki | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Zapotrzebowanie na wyjazd utworzone dla jednego pracownika można wykorzystać do sporządzenia raportu z wydatków innego pracownika. |
| Podróże i wydatki | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorie wydatków są zablokowane podczas dodawania nowego wiersza wydatku. |
| Podróże i wydatki | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Wyszczególnienie już podzielonych wierszy raportu z wydatków powoduje niekompletne zaksięgowanie załącznika Rozrachunki z dostawcami \ Księga główna i przerywa Eksplorator źródeł księgowania, ponieważ **TRVEXPTRANS.SOURCEDOCUMENTLINE** jest zduplikowane. |
| Podróże i wydatki | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Zasady dotyczące zapotrzebowania na podróż nie działają zgodnie z oczekiwaniami. |
| Podróże i wydatki | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Nazwa konta dostawcy nie jest wyświetlana w zaksięgowanych transakcjach projektu dla raportów z wydatków. |
| Podróże i wydatki | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | W Project Operations nie można zatwierdzać czasu za pomocą zadania dla projektu międzyfirmowego. |
| Podróże i wydatki | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategoria zwrotu zaliczki gotówkowej nie aktualizuje sald zaliczek gotówkowych po zaksięgowaniu. |
| Podróże i wydatki | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Cena sprzedaży jest obliczana nieprawidłowo w raportach z wydatków, które zostały utworzone w walucie obcej przy użyciu zaimportowanych transakcji kart kredytowych i są skojarzone z projektem. |
| Podróże i wydatki | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Wycofano encję danych **TrvRequisitionLine** i skojarzony unikatowy indeks. |
| Podróże i wydatki | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Dodano instrumentację do generowania **SOURCEDOCUMENTLINE**. |
| Podróże i wydatki | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Nieprawidłowy arkusz księgi podrzędnej jest wyświetlany w scenariuszu międzyfirmowym, jeśli podatek od sprzedaży jest księgowany w docelowej firmie. |
| Podróże i wydatki | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | W Project Operations szacowania wydatków nie są usuwane z Finanse po ich usunięciu w Dataverse. |
| Podróże i wydatki | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Gdy kategoria wydatków jest kategorią niezwiązaną z projektem, wymiary finansowe wybrane na stronie **Koszt** nie są kopiowane do raportu kosztów. |
