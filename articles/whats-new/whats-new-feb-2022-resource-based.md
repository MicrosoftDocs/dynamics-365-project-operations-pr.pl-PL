---
title: 'Nowości: luty 2022 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów'
description: Ten temat zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu Project Operations z lutego 2022 r. dla scenariuszy opartych na zasobach/niemagazynowanych.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600847"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości: luty 2022 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów

*Dotyczy: Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu*

Ten temat dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.28.0.120
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.24

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

- W tym wydaniu można dodać do 300 członków zespołu do jednego projektu. Wcześniej limit liczby członków zespołu wynosi 150. Aby uzyskać więcej informacji, zobacz [Ograniczenia projektu](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Aktualizacje map podwójnego zapisu aplikacji Project Operations

Na poniższej liście przedstawiono mapy z podwójnym zapisem, które zostały zmodyfikowane lub dodane w wersji Project Operations z lutego 2022 r.

| Mapowanie encji | Wersja zaktualizowana | Komentarze |
| --- | --- | --- |
| Encja integracji wydatków projektowych Project Operations (msdyn\_expenses) | 1.0.0.3 | Rozszerzone o synchronizację działań projektu z Dataverse. |

Aktualną listę i wersje map dwuepisania Project Operations można znaleźć w części [Project Operations w wersji podwójnego zapisu](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2415109 | Wartość domyślna w polu Warunki **płatności Operacje** musi być rekordem klienta kontraktu projektu i rekordem faktury proforma. |
| Rozliczenia i ceny | 2497369 | Poprawianie materiałów musi być zgodne z wartością daty w parametrach **Poprawianie**. |
| Rozliczenia i ceny | 2498697 | Poprawiono konfigurację zabezpieczeń dla czasowego **wpisu**. |
| Rozliczenia i ceny | 2513824 | W przypadku scenariuszy opartych na zasobach identyfikator kategorii transakcji nie może przekraczać 28 znaków w Project Operations. |
| Rozliczenia i ceny | 2517455 | W przypadku tej samej faktury nie można wyzwalać jednoczesnego aktywowania akcji **Odśwież wiersz faktury**. |
| Rozliczenia i ceny | 2517465 | Akcja **Dezaktywowanie szczegółów wiersza** faktury jest blokowana, ponieważ nie jest obsługiwana. |
| Rozliczenia i ceny | 2556660 | Stałe sprawdzenie czeków efektowalności dat, które są wykonywane w cenniku dołączonym do rekordu parametrów projektu. |
|   Zarządzanie szansami sprzedaży | 2369202 | Poprawiono logikę biznesową, która pozwala sprawdzić, czy cenniki z nakładającymi się datami ważności można dołączyć do tego samego kontraktu projektu. |
|   Zarządzanie szansami sprzedaży | 2385965 | Poprawiono zachowanie na karcie **Klienci** na stronie **Kontraktu Projektu** po wybraniu opcji **Zapisz i zamknij**. |
| Czas i wydatek | 2538503 | Po opublikujeniu raportu wydatków zadanie projektu musi być dostępne w encji **Wartości rzeczywiste projektu**. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Zarządzanie projektami i księgowanie | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Podczas importowania not kredytowych dostawcy pojawia się błąd. Komunikat o błędzie stwierdza: „Kwota zatrzymania nie może przekraczać pozostałej kwoty netto”. |
| Zarządzanie projektami i księgowanie | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jeśli propozycje na fakturze zawierają transakcje opłat z zerową kwotą, które są wartościami rzeczywistymi niesprzedajnych sprzedaży, nie można fakturowania. |
| Zarządzanie projektami i księgowanie | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Zaksięgowany koszt jest nieprawidłowy po zaktualizowaniu ceny zakupu i włączeniu **Aktywuj zarządzanie zmianami**.|
| Zarządzanie projektami i księgowanie | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Oszacowanie księgowania dla projektu o stałej cenie używa nieprawidłowej waluty i kwoty w załączniku oszacowania, nawet jeśli włączona jest funkcja **Włącz walutę umowy dotyczącej projektu do obliczania oszacowania**. |
| Zarządzanie projektami i księgowanie | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** nie powinien dzwonić w celu włączenia śledzenia zmian bez przyciągania wyjątków dla encji, które mają klucze konfiguracji, które nie są włączone. |
| Zarządzanie projektami i księgowanie | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Zadanie wsadowe jest stałe, gdy jest opublikowanych wiele zaawansowanych aplikacji i pojawia się błąd. |
| Podróże i wydatki | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Ze względu na problem związanym z rozliczeniami pieniężnmi za raporty o wydatkach kwota podatku nie jest stanowi część kwoty pieniężnej. |
| Podróże i wydatki | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informacje o podatku od sprzedaży nie są uwzględniane w **raporcie Koszty — Opublikowane transakcje**. |
| Podróże i wydatki | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Naruszenie **zasad zasad dotyczących wymaganych** wydatków dotyczących pokwitowania jest niepoprawnie wyświetlane ostrzeżenie w raportach dotyczących wydatków. |
| Podróże i wydatki | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transakcja projektu nie obejmuje w łącznej kwocie sprzedaży podatku, który nie można odzyskać, gdy transakcja jest wynikiem wydatku na sprzedaż. |
| Podróże i wydatki | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kiedy pozycja pozycja zawiera podatek, nie można zmienić daty wiersza pozycji i pojawia się błąd stanu dokumentu źródłowego. |

## <a name="removed-and-deprecated-features"></a>Usunięte i przestarzałe funkcje

Funkcje [Usunięte lub przestarzałe w programie Project Operations](removed-depreciated-features-project.md) temat opisano funkcje, które zostały usunięte lub przestarzałe w programie Dynamics 365 Project Operations.

- Usunięta funkcja nie jest już dostępna w produkcie.
- Przestarzała funkcja nie jest aktywnie tworzona i może zostać usunięta w przyszłej aktualizacji.

Ogłoszenie o wycofaniu pojawi się w temacie [Usunięte lub wycofane funkcje w Project Operations](removed-depreciated-features-project.md) 12 miesięcy przed usunięciem jakiejkolwiek funkcji z produktu .

W przypadku zmian, które wpływają tylko na czas kompilacji, ale są zgodne z trybem piaskownicy i środowiskami produkcyjnymi, czas niezgodności będzie krótszy niż 12 miesięcy. Zazwyczaj te zmiany są aktualizacjami funkcjonalnymi, które należy wprowadzić w kompilatorze.
