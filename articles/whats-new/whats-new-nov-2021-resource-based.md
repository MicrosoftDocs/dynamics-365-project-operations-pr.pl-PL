---
title: Nowości Listopad 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: To temat zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations we listopadzie 2021 r. dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827339"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości Listopad 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

*Dotyczy: Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu*

Ten temat dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.26.0.145, 4.26.0.148, or 4.26.0.150
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance wersja 10.0.22

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- Interfejsy programowania aplikacji (API) harmonogramu projektu obsługują teraz możliwość tworzenia i usuwania zasobników projektu.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations. Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-in-dataverse"></a>Project Operations w Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2240080 | Pole **Terminy płatności** nie może być duplikowane na fakturze pro forma. |
| Rozliczenia i ceny | 2358236 | Korekta faktury musi pozwalać na korekty, które mają zerowe wiersze cenowe. |
| Zarządzanie zasobami | 2410072 | Umożliwia ustawienie zasobu, który jest przypisany do zadania jako kierownik projektu. |
| Rozliczenia i ceny | 2430234 | Rozwiązywanie problemu z obliczeniami wydajności kosztów. |
| Czas i wydatek | 2436978 | Umożliwia wprowadzenie czasu w formacie hh:mm. |
| Rozliczenia i ceny | 2448623 | Zezwalaj na aktualizację cenników po ich powiązaniu z jednostką organizacyjną. |
| Czas i wydatek | 2460396 | Umożliwia usunięcie wpisu czasowego poprzez wyczyszczenie komórki. |
| Rozliczenia i ceny | 2467386 | Umożliwić usunięcie projektu z zadaniem, nawet jeśli zadanie jest powiązane z wygraną wyceną. |
| Czas i wydatek | 2461744 | Widok **Moje nieudane zatwierdzenie** zawiera tylko zatwierdzenie projektu o stanie **Przesłane**. |
| Czas i wydatek | 2464082 | Usuń powiązanie z zatwierdzeń projektu do zestawu zatwierdzeń, gdy dopasowany jest status docelowy. |
| Czas i wydatek | 2468108 | Zadanie Harmonogram nie powinno ustawiać statusu **Przetwarzanie** dla zestawu zatwierdzeń. |
| Czas i wydatek | 2471503 | Usuń zestawy zatwierdzeń, które mają siedem dni. |
| Rozliczenia i ceny | 2480687 | Odniesienie do wiersza cytatu nie może zostać usunięte, gdy tworzony jest kamień milowy wiersza cytatu. |

### <a name="project-management-and-accounting-in-finance"></a>Zarządzanie projektami i księgowanie w Finance

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Zarządzanie projektami i księgowanie | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zatrzymane kwoty sprzedawcy w transakcjach kosztów projektu nie są wyświetlane na liście transakcji. |
| Zarządzanie projektami i księgowanie | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Po włączeniu integracji z fakturą sprzedawcy, faktura sprzedawcy dla firmy jest uszkodzona. |
| Zarządzanie projektami i księgowanie | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Warunki płatności na fakturach projektowych nie działają zgodnie z oczekiwaniami. |
| Zarządzanie projektami i księgowanie | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Gdy zachowanie sprzedawcy zostaje zwolnione, księgowanie załączników zawiera dodatkowe wiersze, które są nieprawidłowe. |
| Zarządzanie projektami i księgowanie | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Gdy dziennik integracji Project Operations jest księgowany, nie udaje się go zaksięgować z powodu brakujących wymiarów dla konta, które nie jest księgowane. |
| Zarządzanie projektami i księgowanie | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Karta **Projekt** nie jest edytowalna na oczekującej fakturze sprzedawcy, gdy do pozycji przypisana jest kategoria zamówienia. |
| Zarządzanie projektami i księgowanie | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Brak okienka nawigacji, jeśli użytkownik nie jest zalogowany w witrynie Project Operations Dataverse. |
| Zarządzanie projektami i księgowanie | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Podczas księgowania przychodu z faktury za projekt w przypadku stosowanego zatrzymania pojawia się problem, ponieważ transakcje na kuponie nie bilansują się. |
| Zarządzanie projektami i księgowanie | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Utworzenie kosztorysu po wysłaniu propozycji faktury blokuje możliwość importu linii korekty. |
| Zarządzanie projektami i księgowanie | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modyfikacja w pełni zafakturowanego zapisu przebiegu nie powinna być możliwa. |
| Podróże i wydatki | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Wszystkie raporty wydatków są widoczne po wyszukaniu kategorii w aplikacji mobilnej wydatki. |
| Podróże i wydatki | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nieprawidłowe kwoty na transakcjach ze sprzedawcami i transakcjach podatku od sprzedaży są księgowane z wydatku, który jest tworzony z transakcji kartą kredytową. |
| Podróże i wydatki | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Nieistotne ostrzeżenie pojawia się po odświeżeniu strony **Raportu wydatków**. |
| Podróże i wydatki | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nieprawidłowy zatwierdzający tymczasowy jest używany w przypadku usunięcia zatwierdzającego tymczasowego, a następnie ponownego przesłania raportu wydatków przez przepływ pracy. |
| Podróże i wydatki | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojawia się błąd księgowania związany z ustawieniem przebiegu. |
