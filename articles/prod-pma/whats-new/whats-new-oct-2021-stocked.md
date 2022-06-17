---
title: Co nowego i zmienionego w październiku 2021 r. — Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne
description: Ten artykuł zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations w październiku 2021 r. dla scenariuszy opartych na inwentarzu/produkcji.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933689"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Co nowego i zmienionego w październiku 2021 r. — Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne

_**Dotyczy:** Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.22
 
## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
|--------------|------------------|----------------|
| Zarządzanie projektami i księgowanie | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Kwoty produkcji w toku (WIP) i rozliczeń międzyokresowych przychodów nie są prawidłowo odwracane po zaksięgowaniu faktury klienta firmy. |
| Zarządzanie projektami i księgowanie | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Nie działa funkcjonalność **Zapobiegaj zamknięciu projektu, jeśli istnieją otwarte transakcje**. |
| Zarządzanie projektami i księgowanie | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasyfikacja rozliczeniowa na fakturze tekstowej nie wypełnia automatycznie wymiarów z projektów, gdy ta funkcjonalność jest włączona. |
| Zarządzanie projektami i księgowanie | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | W scenariuszach innych niż wewnątrzfirmowe kwoty WIP i naliczonych przychodów nie są prawidłowo odwracane po zaksięgowaniu faktury za projekt. |
| Zarządzanie projektami i księgowanie | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Wartości debetowe i kredytowe są zamieniane, gdy dodatek Microsoft Excel jest używany z dziennikiem wydatków projektu, a pole **Typ konta rozliczeniowego** jest ustawione na **Projekt**. |
| Zarządzanie projektami i księgowanie | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Kwota, która jest księgowana w transakcjach projektu, jest zawyżona w zamówieniu zakupu projektu, które zawiera pozycje magazynowe i ma kwoty podatku niepodlegające odliczeniu, gdy zaznaczony jest **UseTax**. |
| Zarządzanie projektami i księgowanie | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | System rozdziela tę kwotę pomiędzy raporty zysków i strat projektu oraz raporty WIP projektu. |
| Zarządzanie projektami i księgowanie | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Stan magazynu podręcznego jest nieprawidłowy po skorygowaniu zapotrzebowania na częściowo zwróconą pozycję. |
| Zarządzanie projektami i księgowanie | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nazwy zasobów są powielane w Project Operations, gdy są edytowane w programie Microsoft Project. |
| Zarządzanie projektami i księgowanie | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Raporty wydatków wewnątrzfirmowych, które mają koszty z tytułu faktury oczekującej na zaksięgowanie są najpierw księgowane w typie księgowania **Koszt WIP projektu**. Jednak podczas przetwarzania koszty związane z szacunkami są księgowane w typie księgowania **Koszt projektu** zamiast w oczekiwanym typie księgowania **Koszt wewnętrzny**. |
| Zarządzanie projektami i księgowanie | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zatrzymanie dostawcy powoduje, że transakcje wydatków projektowych nie są pokazywane. |
| Zarządzanie projektami i księgowanie | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Arkusz czasu pracy musi zaokrąglać kwotę transakcji w walucie transakcji do określonej liczby miejsc po przecinku we wszystkich podziałach księgowych i wpisach alokacji dziennika ogólnego. |
| Zarządzanie projektami i księgowanie | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Ilości zapotrzebowania na pozycje projektu są automatycznie aktualizowane w momencie firmowania planowanych zamówień. |
| Zarządzanie projektami i księgowanie | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Numer bonu, typ transakcji, saldo sprzedawcy i numer konta nie mogą zostać cofnięte na fakturze zaliczkowej zamówienia zakupu. |
| Zarządzanie projektami i księgowanie | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Po włączeniu integracji z fakturą sprzedawcy, faktura sprzedawcy dla firmy jest uszkodzona. |
| Zarządzanie projektami i księgowanie | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Podczas tworzenia dziennika wydatków projektu, kwota kosztu jest wyświetlana w polu **Kredyt**. |
| Zarządzanie projektami i księgowanie | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Warunki płatności na fakturach projektowych nie działają zgodnie z oczekiwaniami. |
| Zarządzanie projektami i księgowanie | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Vouchery arkusza czasu mogą być ponownie wykorzystane, jeśli sekwencja numerów jest ustawiona jako ciągła. |
| Zarządzanie projektami i księgowanie | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCJA: Logika **Ręcznej kwoty zatrzymania** nie jest zgodna z logiką **Automatycznej kwoty zatrzymania** w propozycji faktury do umowy projektu. |
| Zarządzanie projektami i księgowanie | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Po zwolnieniu zatrzymania sprzedawcy, księgowanie bonów ma nieprawidłowe dodatkowe wiersze. |
| Zarządzanie projektami i księgowanie | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | W przypadku zmiany pola **Data faktury** na stronie **Utwórz propozycję faktury** może wystąpić następujący błąd: „Odwołanie do obiektu nie jest ustawione na instancję obiektu”. |
| Zarządzanie projektami i księgowanie | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Pojawia się błąd podczas próby zatwierdzenia arkusza czasu z poziomu przepływu pracy **TSLine**, gdy istnieje zasada arkusza dla soboty i niedzieli. |
| Zarządzanie projektami i księgowanie | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Typ pozycji projektu z saldem początkowym jest wyłączony z **Podsumowania transakcji propozycji faktury** podczas obliczania sumy faktury propozycji faktury. |
| Zarządzanie projektami i księgowanie | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Jeśli koszt szacowany w zamówieniu produkcyjnym projektu wynosi 0 (zero), podczas próby oszacowania występuje następujący błąd: „Próbowano podzielić według zera”. |
| Zarządzanie projektami i księgowanie | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikacja Project Timesheet Mobile dla systemu Android przestaje odpowiadać. Problem jest związany z **TimeEntryDataManager ArgumentNullException**. |
| Zarządzanie projektami i księgowanie | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Dziennik integracji Project Operations nie działa podczas księgowania, ponieważ na koncie brakuje wymiarów. Jednak konto, na którym brakuje wymiarów, nie jest kontem, na które piszesz. |
| Zarządzanie projektami i księgowanie | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filtr **ToDate** w wyszukiwaniach nie jest usuwany po usunięciu go z okna dialogowego **Wybierz** na stronie **Koszt księgowania**. |
| Zarządzanie projektami i księgowanie | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Resetuj całą dystrybucję** nie działa i pokazuje błąd dla arkuszy czasu, które są tworzone dla projektu typu **Tylko czas**. |
| Zarządzanie projektami i księgowanie | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Karta **Projekt** nie jest edytowalna na oczekującej fakturze sprzedawcy, gdy do pozycji przypisana jest kategoria zamówienia. |
| Zarządzanie projektami i księgowanie | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Brak okienka nawigacji, jeśli użytkownik nie jest zalogowany w witrynie Project Operations Dataverse. |
| Zarządzanie projektami i księgowanie | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | W przypadku międzyfirmowych transakcji korekty projektu, w spółce docelowej występują problemy. |
| Zarządzanie projektami i księgowanie | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Zaangażowane koszty dla projektu wyliczają błędną ilość i cenę kosztorysową, jeżeli zamówienie zakupu zostało zrealizowane przez **Proces roczny zamówienia zakupu** w Księdze głównej. |
| Zarządzanie projektami i księgowanie | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Gdy zlecenie produkcyjne projektu, które posiada zlecenia jakościowe, jest zgłaszane jako zakończone, pojawia się następujący błąd: „Brak transakcji wirtualnej oznaczonej transakcją inwentaryzacyjną”. |
| Zarządzanie projektami i księgowanie | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Podczas księgowania faktury rozrachunki z dostawcami związanej z projektem pojawia się następujący błąd: „Tekst enumeratywny Projekt - koszt - pozycja nie istnieje”. |
| Zarządzanie projektami i księgowanie | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Koszty pośrednie są podwajane podczas ręcznego naliczania przychodów. |
| Zarządzanie projektami i księgowanie | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Naliczanie przychodów i księgowanie WIP nie powoduje powstania transakcji. |
| Zarządzanie projektami i księgowanie | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktywacja ceny oczekującej nie powiodła się dla standardowej pozycji kosztowej, gdy istnieje otrzymane zlecenie zakupu projektu. |
| Zarządzanie projektami i księgowanie | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Odwrócona wartość WIP z księgowania faktury różni się od pierwotnie zaksięgowanej wartości WIP z wpisu czasowego. |
| Zarządzanie projektami i księgowanie | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Występuje problem z księgowaniem przychodów z faktur za projekt w stosowanych przypadkach zatrzymania, w których transakcje na voucherze nie bilansują się. |
| Zarządzanie projektami i księgowanie | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Utworzenie kosztorysu po zaksięgowaniu propozycji faktury blokuje import linii korekty w Project Operations. |
| Zarządzanie projektami i księgowanie | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modyfikacja w pełni zafakturowanego zapisu przebiegu nie powinna być możliwa. |
| Zarządzanie projektami i księgowanie | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | W przypadku korzystania z automatycznych obciążeń nie można zaksięgować faktury klienta firmy dla arkusza czasu pracy i wyświetlany jest komunikat o błędzie. |
| Zarządzanie projektami i księgowanie | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adres na podprojekcie nie jest poprawnie aktualizowany. |
| Zarządzanie projektami i księgowanie | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Cena zakupu na zapotrzebowaniu na pozycję jest aktualizowana ceną zakupu dla skonsolidowanych zamówień zakupu. |
| Zarządzanie projektami i księgowanie | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Zaksięgowany koszt nie jest poprawny po aktualizacji ceny zakupu i włączeniu parametru **Aktywuj zarządzanie zmianami**. |
| Podróże i wydatki | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Wszystkie wydatki użytkownika można zobaczyć po wyszukaniu kategorii w aplikacji mobilnej wydatków. |
| Podróże i wydatki | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nieprawidłowe kwoty na transakcjach ze sprzedawcami i transakcjach podatku od sprzedaży są księgowane z wydatku, który jest tworzony z transakcji kartą kredytową. |
| Podróże i wydatki | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Podczas odświeżania stron raportu wydatków wyświetlany jest nieistotny komunikat ostrzegawczy. |
| Podróże i wydatki | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nieprawidłowy tymczasowy zatwierdzający jest używany, gdy usuniesz tymczasowego zatwierdzającego, a następnie ponownie prześlesz go przez przepływ pracy. |
| Podróże i wydatki | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojawia się błąd księgowania związany z ustawieniem przebiegu. |
| Podróże i wydatki | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Dystrybucja nie aktualizuje podmiotu prawnego, gdy niepołączona transakcja jest ponownie dodawana do raportu wydatków w ramach wydatku między firmami. |

### <a name="regulatory-updates"></a>Aktualizacje dotyczące regulacji

Aby uzyskać informacje na temat aktualizacji przepisów prawnych dotyczących aplikacji finansowych i operacyjnych, zobacz [Aktualizacje prawne](/dynamics365/finance/localizations/regulatory-updates). Można również zalogować się do Microsoft Dynamics Lifecycle Services (LCS) i skorzystać z narzędzia wyszukiwania zagadnień, aby wyświetlić planowane aktualizacje przepisów. Wyszukiwanie według zagadnień umożliwia wyszukiwanie według kraju lub regionu, typu elementu i wydania.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
