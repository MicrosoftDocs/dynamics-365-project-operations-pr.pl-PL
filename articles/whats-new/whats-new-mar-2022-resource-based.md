---
title: 'Nowości: marzec 2022 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów'
description: Ten temat zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu Project Operations z marca 2022 r. dla scenariuszy opartych na zasobach/niemagazynowanych.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600755"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości: marzec 2022 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów

*Dotyczy: Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu*

Ten temat dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.30.0.99
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.25

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

Per e-ry są teraz obsługiwane w nowym i od nowa nowym, nowym obszarze roboczym wydatków. Firmy, które korzystają z tej funkcji na każdy koszt, mogą włączyć tę funkcję, aby ułatwić użytkownikom przesyłanie danych i korzystanie z nich za koszty za każdy koszt. Aby uzyskać więcej informacji, zobacz [Wydatki dzienne](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

Na poniższej liście przedstawiono mapy z podwójnym zapisem, które zostały zmodyfikowane lub dodane w wersji Project Operations z marca 2022 r.

| **Mapowanie encji** | **Wersja zaktualizowana** | **Komentarze** |
| --- | --- | --- |
| Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapowania zaktualizowane w celu wyrównania z encją wiersza faktury dostawcy w programie Dataverse. <br>Nie aktywuj mapowania w 1.0.0.4. Będzie on gotowy do użycia w połączeniu ze środowiskiem Finance w wersji 10.0.26 w następnej aktualizacji miesięcznej. |

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Czas i wydatek | 2388011 | Pokazywać komentarze dotyczące przesyłania informacji o czasie podczas zatwierdzania zbiorczego. |
| Planowanie i śledzenie projektu | 2495294 | Szczegółów projektu nie można edytować na stronie **Szczegóły zadania**. |
| Rozliczenia i ceny | 2499605 | Punkty kontrolny kontraktu utworzone na podstawie punktów kontrolnych oferty są niepoprawnie oznaczane jako tylko do odczytu. |
| Planowanie i śledzenie projektu | 2506050 | Zestaw operacji pozostaje oczekujący na jedną godzinę, jeśli nie ma możliwości zapisania zmiany. Następnie zestaw jest fałszowany oznaczony jako **Niepowodzenie**, podczas gdy powinien zostać ukończony natychmiast. |
| Rozliczenia i ceny | 2507401 | Domyślne jednostki kontraktów są niepoprawnie wprowadzane w projektach z powodu niepoprawnego buforowania. |
| Rozliczenia i ceny | 2541660 | **Sprawdzanie poprawności tworzenia zamówienia sprzedaży** w trybie podwójnym powinna być dostępna tylko dla zamówień opartych na projektach. |
| Rozliczenia i ceny | 2552745 | Podatku nie jest rozdzielany między klientów, którzy ustawili podzielone reguły fakturowania. |
| Rozliczenia i ceny | 2558859 | Udoskonalone komunikaty o błędach w przypadku skonfigurowania rozmiarów kalkulacji cen. |
| Rozliczenia i ceny | 2558933 | **Importowanie z szacowania projektu** kończy się niepowodzeniem, gdy zostanie dodany projekt **msdyn\_project** jako aspekt kalkulacji cen. |
| Rozliczenia i ceny | 2559101 | Usuwanie parametrów projektu nie jest blokowane i powoduje problemy. |
|   Zarządzanie szansami sprzedaży | 2570390 | Dwue write plug-in. typ konta w ofertach, zamówieniach i szansach sprzedaży ma być **Klientem**, nawet jeśli ten typ konta jest poprawny. |
| Rozliczenia i ceny | 2586097 | Podział wartości rzeczywistych kosztów fakturowanych nie jest cofany, gdy projekt jest usuwany z wiersza kontraktu projektu. |
| Rozliczenia i ceny | 2589619 | Podatek od materiałów do zapisu jest propagowany do wartości rzeczywistych sprzedaży i faktury. |
|   Zarządzanie szansami sprzedaży | 2594015 | Oferty nie mogą zostać zamknięte jako woni dla klientów, którzy mają warunki płatności za pomocą usługi **Net60**. |
| Planowanie i śledzenie projektu | 2595841 | W Project for the Web użytkownicy otrzymują komunikat o błędzie informujący o braku danych **msdyn\_actualstart** po utworzeniu nowego żądania zasobu. |
| Czas i wydatek | 2602511 | Pole **Odrzucone przez czas** zawiera **nazwę System** zamiast nazwanego użytkownika jako osoby odrzucanej. |
| Czas i wydatek | 2602528 | Osoba zatwierdzająca projekt może zatwierdzać czas w projektach, w których nie jest wymieniona jako osoba zatwierdzająca. |
| Rozliczenia i ceny | 2608550 | Fakturę korekty można potwierdzić nawet w przypadku brak zmian w oryginalnym. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Zarządzanie projektami i księgowanie | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Istnieje niezgodność między Finance a Project Operations w zakresie dozwolonej długości pola **Category ID**. |
| Zarządzanie projektami i księgowanie | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projektów cen nie można usuwać, gdy w polu **Fakturowanie konta** ustawiono wartość **Zysku i utraty**, a stosowana jest podstawowa **wartość procentowa zakończona**. |
| Zarządzanie projektami i księgowanie | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | W konfiguracji projektu wprowadzono nieprawidłową domyślną grupę podatku sprzedaży w wierszach wydatków w integracji Project Operations. |
| Zarządzanie projektami i księgowanie | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Nie można edytować rozmiarów nagłówka nagłówka propozycji projektu na fakturze w zintegrowanym wdrożeniu z Project Operations. |
| Zarządzanie projektami i księgowanie | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Faktury dostawcy międzyfirmowego nie mogą być zintegrowane z usługą Dataverse. |
| Zarządzanie projektami i księgowanie | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Istnieje niezgodność w walucie równoważenia salda klienta i walucie raportowania. |
| Zarządzanie projektami i księgowanie | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Fakturę projektu można opublikować nawet wtedy, gdy klient jest wstrzymany dla wszystkich faktur. |
| Zarządzanie projektami i księgowanie | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Przycisk **Usuń wszystkie wiersze nie** zawiera ofert dotyczących faktur projektów z widokami **Nagłówek** i **Wiersze**. |
| Zarządzanie projektami i księgowanie | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Podczas księgowania faktury od dostawcy występuje następujący błąd: „Data księgowania faktury musi być w tym samym roku księgowym, co powiązane zamówienie zakupu. Należy uruchomić proces na koniec roku zamówienia zakupu lub zmienić datę na bieżący rok obrachunkowy". |
| Podróże i wydatki | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Zaangażowany koszt projektu nie jest zwalniany po ukazały się po ukazały się powiązany koszt zakupu podróży. |
| Podróże i wydatki | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Podczas przesyłania raportu wydatków występuje następujący błąd: „Ślad stosu: firma nie istnieje”. |
| Podróże i wydatki | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Domyślny **identyfikator projektu** nie jest wprowadzany w raportach dotyczących wydatków po wybraniu parametru **Wymagaj działania dla parametru projektowego**. |
| Podróże i wydatki | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Przycisk **Opublikuj koszty** nie działa poprawnie w Project Operations w scenariuszach niezaadowodowanych zasobów. |
| Podróże i wydatki | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Istnieje problem z raportem o kosztach, który zawiera błąd **Stawka za milę** w raporcie z wydatkami. |
| Podróże i wydatki | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Stawki wydatków na kilometraż dla pracowników nie są poprawnie sumowane, gdy w kategorii wydatków **Poziomy stawek milowych** używane są dwa różne typy pojazdów. |
| Podróże i wydatki | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Pole **Projekt** w wierszu requisition podróży nie zwraca poprawnej listy projektów. |
| Podróże i wydatki | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Przebieg w trakcie sprawdzania** wyświetla ostrzeżenie w raportach z wydatków. |
| Podróże i wydatki | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Usługa rozpoznawania znaków potwierdzenia (OCR) nie działa z powodu problemu z adresem URL usługi OCR wydatków. |
| Podróże i wydatki | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Jeśli funkcja **Szybkie itemize** cyklicznych wydatków jest włączona, kwoty w wierszach itemization w raportach dotyczących wydatków zmieniają się przy każdym otwarciu strony **Podziel na pozycje**. |
| Podróże i wydatki | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Nie można usunąć raportu z wydatkami, gdy lista tymczasowa ma więcej niż jednego osoby zatwierdzającej. |

## <a name="removed-and-deprecated-features"></a>Usunięte i przestarzałe funkcje

Funkcje [Usunięte lub przestarzałe w programie Project Operations](removed-depreciated-features-project.md) temat opisano funkcje, które zostały usunięte lub przestarzałe w programie Dynamics 365 Project Operations.

- Usunięta funkcja nie jest już dostępna w produkcie.
- Przestarzała funkcja nie jest aktywnie tworzona i może zostać usunięta w przyszłej aktualizacji.

Ogłoszenie o wycofaniu pojawi się w temacie [Usunięte lub wycofane funkcje w Project Operations](removed-depreciated-features-project.md) 12 miesięcy przed usunięciem jakiejkolwiek funkcji z produktu .

W przypadku zmian, które wpływają tylko na czas kompilacji, ale są zgodne z trybem piaskownicy i środowiskami produkcyjnymi, czas niezgodności będzie krótszy niż 12 miesięcy. Zazwyczaj te zmiany są aktualizacjami funkcjonalnymi, które należy wprowadzić w kompilatorze.
