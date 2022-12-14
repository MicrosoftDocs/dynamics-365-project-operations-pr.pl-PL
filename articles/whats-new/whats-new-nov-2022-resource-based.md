---
title: Nowości Listopad 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z listopada 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831099"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości Listopad 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.58.0.119
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations. Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2781818 | Nie znaleziono błędu podczas domyślnego ustawiania ceny dla dziennika użycia materiałów. |
| Rozliczenia i ceny | 2922373 | Nie można połączyć wiersza oferty z projektem, który został zamknięty jako utracona oferta. |
| Rozliczenia i ceny | 2943206 | Pole **Pozycja kontraktu** w encji projektu powinno być opcjonalne. |
| Rozliczenia i ceny | 2953182 | Usprawnij komunikat o błędzie podczas poprawiania faktur.|
| Rozliczenia i ceny | 2959500 | Nie można powiązać wiersza oferty z zadaniem projektu, które jest już skojarzone z utraconą ofertą.|
| Rozliczenia i ceny | 2959560 | „Ten klient znajduje się już w kontrakcie projektu”, który został odebrany podczas zamykania oferty jako określonej wygranej w określonych lokalizacjach. |
| Rozliczenia i ceny | 3031727 | Przypisanie zasobów nie powiedzie się, a pole „msdyn_Company” nie zawiera błędu. |
| Rozliczenia i ceny | 3036905 | Firma będąca właścicielem nigdy nie jest inicjowana w ProjectTeamMember. |
| Zarządzanie szansami sprzedaży | 2763519 | Błąd odwołania null w aktualizacjach EnsureProjectContractAllowsUpdates. |
| Zarządzanie szansami sprzedaży | 2783798 | Podczas importowania szacowań projektów w wierszu oferty nie są dostępne opisy zadań dla szacowań kosztów i materiałów.|
| Zarządzanie szansami sprzedaży | 2988635 | Udoskonalanie opisu msg błędu podczas usuwania klienta w ofercie. |
| Zarządzanie szansami sprzedaży | 3001191 | Nie można utworzyć oferty z szansy sprzedaży, w której metoda rozliczania jest podana jako null. |
| Uaktualnienie | 3012324 | Konwersja projektu nie powiodła się w przypadku projektu, który ma w nazwie znaki kontrolne, takie jak karta. || Planowanie i śledzenie projektu | 2790384 | Limit czasu oczekującej OperationSet jest zbyt krótki. |
| Planowanie i śledzenie projektu | 3044275 | Brak lokalizacji dla: missingProjectSchedulerErrorMessage. |
| Planowanie i śledzenie projektu | 3044277 | Siatka rozpoznania projektu nie jest ładowana, gdy harmonogram nie jest ustawiony.|
| Zarządzanie zasobami | 2943153 | Aktualizacja karty Śledzenie w celu pokazania dwóch miejsc dziesiętnych dla ustawienia Czas trwania.|
| Podwykonawstwo | 2932774 | Błąd tylko do odczytu wiersza faktury od dostawcy zgłaszany niepoprawnie. |
| Podwykonawstwo | 2939556 | Stan nagłówka faktury od dostawcy nie powinien mieć ustawienia Wersja robocza w wierszu, jeśli nie jest aktywny. |
| Czas i wydatek | 2939998 | Wprowadź nową wersję TESA w wersji ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Zarządzanie projektami i księgowanie w Finance

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
