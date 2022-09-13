---
title: Co nowego w lipcu 2022 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z lipca 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403965"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego w lipcu 2022 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.44.0.22
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations. Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Wdrażanie i konfiguracja | 2761472 | Błąd instalacji Project Operations jest obsługiwany. |
| Rozliczenia i ceny | 2746940 | Nazwa wiersza umowy podwykonawczej powinna mieć maksymalną długość 100 znaków. |
| Rozliczenia i ceny | 2739162 | Klienci muszą widzieć przyciski wstążki w widoku siatki wartości rzeczywistych. |
| Planowanie i śledzenie projektu | 2730318 | Zaktualizowano walidację nieobsługiwanych znaków w temacie projektu. |
| Rozliczenia i ceny | 2705361 | Rzeczywiste wartości sprzedaży rozliczanych w kamieniu milowym muszą być uwzględnione w polach śledzenia projektu. |
| Rozliczenia i ceny | 2675880 | Zapobiegaj łączeniu projektu z wierszem umowy, który nie jest oparty na pracy. |
| Rozliczenia i ceny | 2664396 | Jeśli cennik ofertowy zostanie zapisany bez wyceny, musi wystąpić błąd informujący, że oferta nie może być pusta. |
| Rozliczenia i ceny | 2184019 | Karta **Rozliczenia na zadaniach** nie powinna być wyświetlana w przypadku projektów, które nie mają kontraktu ani kontraktu dotyczącego zapasów. |
| Czas i wydatek | 2754459 | Gdy cykliczny przepływ planowania w chmurze jest nieaktywny, wyświetl baner i pomiń przetwarzanie asynchroniczne. |
| Rozliczenia i ceny | 2724391 | Zły wyjątek jest zgłaszany, gdy reguła rozliczania podziału kontraktu projektu nie zawiera wartości klienta. |
| Rozliczenia i ceny | 2708638 | Podczas przeszukiwania siatki w obszarach Użycie materiałów i Zatwierdzenia użycia materiałów nie znaleziono rekordu.|
| Rozliczenia i ceny | 2686977 | Zapobieganie weryfikacji wiersza faktury podczas tworzenia faktury. |
| Rozliczenia i ceny | 2683032 | Kopiowanie odpłatnych ról i kategorii nie jest skalowalne powyżej 5000 rekordów.|
| Rozliczenia i ceny | 2673363 | Opcja Zużycie kosztów (%) w projekcie nie działa prawidłowo, jeśli istnieją szacowania oraz wartości rzeczywiste nakładów i wydatków dla projektu. |

### <a name="project-management-and-accounting-in-finance"></a>Zarządzanie projektami i księgowanie w Finance

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services (LCS) i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcje włączone domyślnie w nadchodzącym wydaniu

Poniższa tabela zawiera listę funkcji, które są domyślnie włączone w wersji 10.0.29. Większość funkcji, które zostały włączone, można wyłączyć w [zarządzaniu funkcjami](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). W przyszłości niektóre funkcje, które zostały automatycznie włączone, mogą zostać usunięte z zarządzania funkcjami i stać się obowiązkowe. Zmiana ta zapewnia, że klienci korzystają z aktualnych funkcji, dzięki czemu ulepszenia mogą opierać się na aktualnych funkcjach w miarę ich dodawania. Funkcje nigdy nie będą automatycznie włączane w okresie krótszym niż jeden rok, chyba że zostaną uznane za istotne.

| Nazwa funkcji | Włącz dane | Funkcja dodana | Stan funkcji | Moduł |
| --- | --- | --- |--- |--- |
| Umożliwienie korekty transakcji godzinowej w oparciu o zmianę alokacji zasady finansowania | 16 Wrzesień 2022 | 7 października 2020 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Funkcja cofnięcia faktury za zamówienie przedpłatowe projektu | 16 Wrzesień 2022 | 6 października 2021 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Usuń linie propozycji faktury podczas korzystania z programu Project Operations dla scenariuszy opartych na zasobach / brakach zasobów | 16 Wrzesień 2022 | 6 października 2021 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Dostosuj księgowość zaksięgowanej transakcji projektu | 16 Wrzesień 2022 | 10 maja 2020 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włączanie domyślnej konfiguracji księgowej projektu | 16 Wrzesień 2022 | 19 lutego 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włączanie wielu pozycji kontraktu dla projektu | 16 Wrzesień 2022 | 29 czerwca 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Ustaw godzinę projektu tylko do odczytu, jeśli bieżący stan zatwierdzania nie umożliwia edycji | 16 Wrzesień 2022 | 6 października 2021 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włącz synchronizację wierszy sprzedaży z wierszami zakupu, gdy wiersze zakupu są aktualizowane i parametr zarządzania zmianami zamówień zakupu jest włączony | 16 Wrzesień 2022 | 7 października 2020 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włączanie Project Operations w u klientach usługi Dynamics 365 Customer Engagement | 16 Wrzesień 2022 | 29 czerwca 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Funkcja poprawiania błędów w transakcjach projektów | 16 Wrzesień 2022 | 13 lipca 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcje, które w nadchodzącym wydaniu staną się obowiązkowe

W poniższej tabeli wymieniono funkcje, które są obowiązkowe od wersji 10.0.29 i nowszych.

| Nazwa funkcji | Włącz dane | Funkcja dodana | Stan funkcji | Moduł |
| --- | --- | --- | --- | --- |
| Obliczanie wartości zatwierdzonej w źródle danych bez zaokrąglania kursu wymiany | 16 Wrzesień 2022 | 14 czerwca 2020 roku | Obowiązkowy | Zarządzanie projektami i księgowanie |
| Włącz księgowanie korekt projektu na tym samym koncie księgowym, co pierwotna transakcja | 16 Wrzesień 2022 | 14 czerwca 2020 roku | Obowiązkowy | Zarządzanie projektami i księgowanie |
| Szczegóły kwoty zatwierdzonego kontraktu projektu | 16 Wrzesień 2022 | Sierpień 31, 2019 | Obowiązkowy | Zarządzanie projektami i księgowanie |
| Włączanie sortowania według zasobów podczas tworzenia propozycji sprzedaży na fakturze projektu | 16 Wrzesień 2022 | Sierpień 31, 2019 | Obowiązkowy | Zarządzanie projektami i księgowanie |
