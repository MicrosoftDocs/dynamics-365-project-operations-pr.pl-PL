---
title: Nowości z kwietnia 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z kwietnia 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912391"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości z kwietnia 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.41.0.45
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.26

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

W zamówieniach zakupu projektu i oczekujących fakturach od dostawcy mogą być używane kategorie kategorii. Aby uzyskać więcej informacji, zobacz [Używanie kategorii zaopatrzenia z zamówieniami zakupu projektu i oczekującymi fakturami od dostawców](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W poniższej tabeli przedstawiono mapowania dwurdzeniowe, które zostały zmodyfikowane lub dodane w wersji programu Project Operations z marca 2022 r.

| Mapowanie encji | Wersja zaktualizowana | Komentarze |
| -------------- | ------------------- | ------------|
| Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu msdyn\_projectvendorinvoicelines | 1.0.0.4 | Ta mapa obsługuje użycie kategorii zaopatrzenia z zamówieniami zakupu i oczekującymi fakturami od dostawców. |

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| ------------ | ---------------- | -------------- |
| Czas i wydatek | 2573900 | Funkcja **Zatwierdzanie** nowoczesne musi być domyślnie włączona. |
| Rozliczenia i ceny | 2603313 | Poprawiono błąd zduplikowanego rekordu, który uniemożliwił dodanie oferty i linii kontraktu z dodanym produktem. |
| Wdrażanie i konfiguracja | 2611368 | Klienci mogą dodać do rozwiązania maksymalnie pięć encji niestandardowych, używając nowoczesnego projektanta aplikacji. |
| Czas i wydatek | 2628285 | Rozwiązano problem, który wpływał na możliwość ustawienia poprawnej kategorii zasobu podczas importu. |
|   Zarządzanie szansami sprzedaży| 2628815 | Zaktualizuj limit znaków opisu szczegółów wiersza oferty, tak aby był zgodne z ograniczeniem znaków w temacie zadania, tak aby importowanie było wykonywane pomyślnie w zadaniach, których temat jest dłuższy niż 100 znaków. |
| Czas i wydatek| 2629547 | Pole **Przesłane przez** zatwierdzenie projektu musi wskazać użytkownika, który przesłał rekord. |
| Czas i wydatek| 2629865 | Pole **Kopiowanie kategorii** do zadań podczas kopiowania projektów. |
| Czas i wydatek| 2636463 | Stałe filtry dla zatwierdzeń w nowoczesnych formularzach zatwierdzeń. |
| Planowanie i śledzenie projektu | 2648300 | Rozwiązano problem uniemożliwiający zmiany właściciela projektu. |
| Rozliczenia i ceny | 2563000 | Nie można przyznać linii sprzedaży, w których waluta różni się od waluty kontraktu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services (LCS) i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
