---
title: Co nowego w czerwcu 2021 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania
description: To temat zawiera informacje o istotnych aktualizacjach dostępnych w wydaniu aplikacji Project Operations z czerwca 2021 r. dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 21a446fdb9526c1a2b110c5368516dafb64b5e01
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600801"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego w czerwcu 2021 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

- Aplikacja Project Operations w środowisku usługi Dynamics 365 Dataverse w wersji 4.11.0.156 lub 4.11.0.164.
- Zarządzanie projektami i księgowymi w środowiskach aplikacji finansowe i operacyjne wersja 10.0.19.

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- Możliwość usuwania [wierszy propozycji faktury projektu dla scenariuszy korekty](../invoicing/correct-project-invoice-proposals.md).
- Elementy pozycji wydatków odzwierciedlają nazwy podkategorii w raporcie wydatków [Przeprojektowane raporty wydatków — nowe funkcje](../expense/expense-reports-reimagined.md#new-features).
- Metoda płatności jest dostępna w nowym okienku wydatków podczas tworzenia nowego wydatku.
- Ogólna dostępność interfejsów API harmonogramu projektów. Ta nowa funkcja umożliwia klientom programowe wykonywanie operacji tworzenia, aktualizowania i usuwania zadań projektu, przydziałów zasobów, zależności zadań i rekordów członków zespołu projektowego. Aby uzyskać więcej informacji, zobacz [Użyj interfejsów API harmonogramu projektu do wykonywania operacji z encjami planowania](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations. 

Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w swoim środowisku i włączaj wszystkie powiązane mapy tabelaryczne podczas aktualizacji rozwiązania Project Operations Dataverse i wersji rozwiązania aplikacji finansowych i operacyjnych. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli najnowsza wersja mapy nie zostanie aktywowana. Aktywna wersja mapy jest dostępna na stronie **Podwójny zapis** w kolumnie **Wersja**. Aktywuj nową wersję mapowania, wybierając **Wersje mapowania tabeli**, wybierając najnowszą wersję, a następnie zapisując wybraną wersję. Jeśli dostosowałeś niestandardową mapę tabeli, będziesz trzeba ponownie zastosować zmiany. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami na mapie w tabeli](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) w przewodniku rozwiązywania problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2281417 | Rozwiązano problem dotyczący niepowodzenia akcji automatycznego tworzenia faktury w harmonogramie faktur. |
| Rozliczenia i ceny | 2287835 | Lepsza wydajność potwierdzenia faktury. |
| Zarządzanie szansami sprzedaży | 2222555 | Możliwość obciążania wartości szacunkowych materiałów trzeba poprawnie skopiować do szczegółów wierszy oferty w przypadku używania opcji **Importuj z szacowania projektu**. |
| Zarządzanie szansami sprzedaży | 2223427 | Dostosowania są teraz dozwolone w ramach akcji **GenerateRetainersFromRetainerScheduleOptions**. |
| Zarządzanie szansami sprzedaży | 2277528 | Obliczanie stałych wartości kamieni milowych rozliczania dla wierszy kontraktu projektu z wieloma klientami. |
| Planowanie i śledzenie projektu | 2226110 | Rozwiązano sporadyczny problem z funkcję **generowania wymagań** w siatce **zespołu projektu**. |
| Planowanie i śledzenie projektu | 2208109 | Użytkownicy nie mogą tworzyć projektu w jednej walucie z zadaniami pokrewnymi w innej walucie. |
| Planowanie i śledzenie projektu | 2258228 | Lista pól, które można modyfikować za pomocą encji **Planowanie** przy użyciu interfejsu API harmonogramu planowania, została zaktualizowana. |
| Planowanie i śledzenie projektu | 2293989 | Do siatki **Zadania projektu** muszą być przekazywane odpowiednie ustawienia językowe i regionalne. |
| Zarządzanie zasobami | 2220493 | Poprawiono sposób pracy w siatce **Zadanie** podczas szybkiego oznaczania żądania zasobu jako zakończonego. |
| Zarządzanie zasobami | 2330496 | Rozwiązano problem z ładowaniem **tablicy harmonogramu**. (Aktualizacja jakości jest dostępna w wersji 4.11.0.164) |
| Czas i wydatek | 2194431 | Siatka **wprowadzania czasu** musi uznawać początek tygodnia zgodnie z **ustawieniami systemowymi**. |
| Czas i wydatek | 2277311 | Po usunięciu wartości w komórce w siatce **wprowadzania czasu** kursor pozostaje w siatce. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Zarządzanie projektami i księgowanie | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notatki formularza** i **Konfiguracja formularza** nie są widoczne w obszarze **konfiguracji zarządzania projektami** w firmach finansowych, które są zintegrowane z aplikacją Project Operations. |
| Zarządzanie projektami i księgowanie | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Domyślny opis dla podatku VAT jest pusty, gdy **typ księgowania** = **Podatek** dla załączników faktur projektów. |
| Zarządzanie projektami i księgowanie | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Podwójne transakcje są księgowane, gdy rozliczanie oparte na zadaniach jest używane w usłudze Dataverse z integracją z aplikacją Project Operations. |
| Zarządzanie projektami i księgowanie | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Podczas korzystania z integracji z aplikacją Project Operations wartość procentowa wykonania w uznaniu przychodu jest nieprawidłowa. |
| Zarządzanie projektami i księgowanie | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Naliczany przychód jest podwojony w oczekującej fakturze dostawcy w zintegrowanym scenariuszu aplikacji Project Operations. |
| Zarządzanie projektami i księgowanie | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Nie można zaksięgować arkusza integracji, jeśli regułę profilu przychodu ustawiono na konfigurację **Grupa**. |
| Zarządzanie projektami i księgowanie | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Nie można zaksięgować faktury zakupu w zamówieniach zakupu dla projektu z wierszami z wieloma jednostkami miary. |
| Zarządzanie projektami i księgowanie | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Nie można zaktualizować domyślnego wymiaru finansowego projektu, korzystając z encji danych Projekty **(wersja 2)**. |
| Zarządzanie projektami i księgowanie | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Proces wsadowy tworzenia szacowań projektu trwa zbyt długo, aby można go było zakończyć. |
| Zarządzanie projektami i księgowanie | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Usunięcie kontraktu powoduje również usunięcie adresu skojarzonego z klientem. |
| Podróże i wydatki | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Warunek przepływu pracy zatwierdzania raportu wydatków jest oceniany nieprawidłowo. |
| Podróże i wydatki | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Zasady dotyczące raportu wydatków nie są poprawnie oceniane według identyfikatora projektu. |
| Podróże i wydatki | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Akcja **Podział na wartości osobiste dla transakcji wydatków międzyfirmowych** nie działa poprawnie. |
| Podróże i wydatki | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Uzasadnienia wiersza raportu wydatków są przypadkowo usuwane po usunięciu niektórych zapotrzebowań dotyczących podróży. Taka sytuacja ma miejsce, gdy identyfikator zapotrzebowania dla raportu wydatków i zapotrzebowanie dotyczące podróży są takie same. |
| Podróże i wydatki | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Występuje problem z aplikacją mobilną Wydatki, gdy pole **Identyfikator projektu** jest wymagane w zasadach raportu wydatków. |
| Podróże i wydatki | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Nie można edytować wydatków międzyfirmowych skojarzonych z projektem. Zamiast tego jest wyświetlany następujący komunikat o błędzie: „Odwołanie do obiektu nie jest ustawione na wystąpienie obiektu”. |
| Podróże i wydatki | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Po opublikowaniu raportu wydatków nieprawidłowa waluta i kwota są wyświetlane w bankowej księdze podrzędnej. |
| Podróże i wydatki | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Wprowadzono udoskonalenia funkcji *usuwania transakcji kartą kredytową*.  |
| Podróże i wydatki | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Podatek zawarty w raporcie wydatków nie jest obliczany w sposób spójny, gdy w firmie jest określona inna waluta raportowania. |
| Podróże i wydatki | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Dodanie nowego wydatku gotówkowego dla podróży wpływa na wydajność. |
| Podróże i wydatki | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Reguły zasad wydatków nie są wyzwalane w raporcie wydatków. |
| Podróże i wydatki | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Przekazanie nowej kategorii udostępnionej za pomocą struktury zarządzania danymi powoduje usunięcie wszystkich podkategorie dla wszystkich kategorii udostępnionych. |
| Podróże i wydatki | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Podczas tworzenia pozycji wydatków i wybierania kategorii jest wyświetlany następujący błąd: „Kombinacja grupy podatków DOM i grupy podatku pozycji STD jest nieprawidłowa”. |
| Podróże i wydatki | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Występują problemy z synchronizacją w aplikacji mobilnej do obsługi wydatków. |
