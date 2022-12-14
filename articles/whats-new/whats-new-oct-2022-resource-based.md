---
title: Co nowego, październik 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z października 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806629"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego, październik 2022 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.57.0.176
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.30

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

| Obszar funkcji | Nazwa funkcji | Więcej informacji |
| --- | --- | --- |
| Planowanie i śledzenie projektu | **Zewnętrzne planowanie Project Operations**<br>Tryb planowania zewnętrznego pozwala klientom na natywne tworzenie, aktualizowanie i usuwanie encji powiązanych ze strukturami podziału pracy (WBS), używając natywnych interfejsów API Dataverse, ale bez bieżących ograniczeń wymuszanych przez program Project for the Web. | [Planowanie zewnętrzne](/dynamics365/project-operations/project-management/external-scheduling) |
| Wdrażanie i konfiguracja | <p>**Zezwalaj klientom na wybieranie typu wdrożenia**<br>Aktualizacje (PDU) oparte na produktach używane w Project Operations są używane do automatycznego instalowania rozwiązania podwójnego zapisu Project Operations, gdy rdzeń podwójnego zapisu i rozwiązania orkiestracji są zainstalowane w środowisku.</p><p>Ta funkcja wprowadza nowy parametr **Zachowania aktualizacji rozwiązania** w parametrach projektu. Gdy ten parametr jest ustawiona na **Tylko wersja uproszczona**, PUD oparte na produktach używane w Project Operations są używane do automatycznego instalowania rozwiązania podwójnego zapisu Project Operations, nawet jeśli rdzeń podwójnego zapisu i rozwiązania orkiestracji są zainstalowane w środowisku. Z tego zachowania korzystają klienci, którzy planują używanie rozwiązań podwójnego zapisu do integrowania zamówień sprzedaży z aplikacjami finansowymi i operacyjnymi, ale chcą używać Project Operations w trybie uproszczonym (czyli bez integracji z aplikacjami finansowymi i operacyjnymi).</p> | |
| Rozliczenia i ceny | <p>**Konwersja walut w transakcjach sprzedaży nierozliczonych w środowiskach zintegrowanych**<br>W przypadku klientów korzystających z Project Operations zintegrowanych z aplikacjami finansowymi i operacyjnymi (czyli w typie wdrożenia zasobów / nieobejmujących magazynowania) kursy wymiany są zazwyczaj opanowane w aplikacjach finansowych i operacyjnych. Jeśli jednak kategoria wydatków powinna być wyceniona przy użyciu metody obliczania ceny „po kosztach” lub „marża ponad kosztem” w momencie rozliczenia klienta, kurs wymiany używany do obliczania kwoty sprzedaży stosuje kursy wymiany w Dataverse, a nie kursy wymiany stosowane w aplikacjach finansowych i operacyjnych.</p><p>Ta funkcja wprowadza nowy parametr **Zachowania konwersji walut** w parametrach projektu. Jeśli parametr ten ma ustawienie **Rozszerzone z wartością rezerwową**, nierozliczone kwoty sprzedaży w transakcjach wydatków są obliczane na podstawie kursów wymiany kursów aplikacji finansowych i operacyjnych.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations. Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2316317 | System umożliwia tworzenie faktur, które nie są transakcjami płatnymi. |
| Rozliczenia i ceny | 2737300 | Przed dostępem do formularza można sprawdzić dostępność pola **Klient**. |
| Rozliczenia i ceny | 2744948 | Dodaj sprawdzanie null dla metody rozliczania. |
| Rozliczenia i ceny | 2763515 | W przypadku braku kontraktu sprzedaży faktury jest obsługiwany błąd odwołania null. |
| Rozliczenia i ceny | 2844301 | Utworzenie faktury partii kończy się niepowodzeniem z powodu błędu. |
| Rozliczenia i ceny | 2845869 | Niepoprawny magazyn usługi organizacji. |
| Rozliczenia i ceny | 2853729 | Szczegóły roli i ceny są aktualizowane po modyfikacji typu rozliczania. |
| Rozliczenia i ceny | 2940350 | Podczas wyceniania wartości rzeczywistych należy automatycznie wprowadzać tylko aktywne cenniki. |
| Wdrażanie i konfiguracja | 3001206 | Encja msdyn\_replaylogheader uniemożliwia uaktualnienie organizacji klientów. |
| Zarządzanie szansami sprzedaży | 2755582 | Wyjątki odwołania null obsługiwane z pomocy reguły podziału rozliczeń. |
| Zarządzanie szansami sprzedaży | 2761477 | Po użyciu podziału rozliczenia usunięcie punktu kontrolnego (nagłówka) pozostawia oddzielone punkty kontrolne. |
| Zarządzanie szansami sprzedaży | 2767595 | Po otwarciu rekordu zużycia materiałów w formularzu głównym zasób dostępny do rezerwacji dla rekordu zostanie zmieniony na właśnie zalogowanego użytkownika. |
| Planowanie i śledzenie projektu | 2790384 | Limit czasu oczekującej OperationSet jest zbyt krótki. |
| Planowanie i śledzenie projektu | 2957840 | Nie można zapisać zadań i kolumn nie można dodać do strony **Zadania** w zintegrowanym rozwiązaniu Project Operations. |
| Zarządzanie zasobami | 2751560 | Niespójne preferowane jednostki organizacji w wymaganiach zasobów. |
| Podwykonawstwo | 2853245 | Dopasowanie wartości rzeczywistych wiersza faktury od dostawcy nie aktualizuje stanu weryfikacji, jeśli pozycja kontraktu jest już połączona z wierszem faktury od dostawcy. |
| Podwykonawstwo | 2907231 | Etapu procesu faktury od dostawcy nie można kontynuować. |
| Czas i wydatek | 2867363 | Rekordy nie są ujmowane w widoku Nieobecności/Urlopy w celu zatwierdzenia, gdy są kolejkowane do zatwierdzenia. |
| Czas i wydatek | 2894405 | TESA: nieużywany katalog POC powoduje problemy ze zgodnością. |

### <a name="project-management-and-accounting-in-finance"></a>Zarządzanie projektami i księgowanie w Finance

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
