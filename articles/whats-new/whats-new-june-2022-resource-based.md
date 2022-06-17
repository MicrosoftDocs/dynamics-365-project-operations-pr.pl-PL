---
title: Co nowego w czerwcu 2022 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z czerwca 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959465"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego w czerwcu 2022 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.43.0.77
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W poniższej tabeli przedstawiono mapy podwójnego zapisu , które zostały zmodyfikowane lub dodane w aplikacji Project Operations z czerwca 2022 r.

| Mapowanie encji | Wersja zaktualizowana | Komentarze |
| --- | --- | --- |
| Integracja w Project Operations encji eksportu faktury dostawcy projektu (msdyn_projectvendorinvoices) | 1.0.0.1 | Starsze pole uznane za przestarzałe i zmapowane na nowe pole śledzenia stanu faktury od dostawcy. |

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Podwykonawstwo | 2708885 | Poprawiono komunikat o błędzie wyświetlany podczas tworzenia przez użytkownika rekordu nagłówka rezerwacji zasobu do zarezerwowania, w którym wypełniono danych takiego rekordu. |
| Planowanie i śledzenie projektu | 2629441 | Poprawiono logikę wyzwalania przepływu pracy, aby zapobiec nieskończonej pętli podczas aktualizowania zadań projektu. |
| Czas i wydatek | 2641209 | Importy czasu z przypisań/rezerwacji muszą zachowywać odwołanie do zasobów, które można zarezerwować. |
| Planowanie i śledzenie projektu | 2651148 | Nagłówek dokumentu projektu musi być chroniony.|
| Planowanie i śledzenie projektu | 2653145 | Dodano walidacje, aby upewnić się, że nie można utworzyć rekordu projektu z nieprawidłowymi znakami w nazwie. |
| Czas i wydatek | 2654710 | Poprawiono filtrowanie na stronie **Zatwierdzenia**. |
| Rozliczenia i ceny | 2667805 | Dodano walidacje ułatwiające zapobieganie tworzeniu wartości rzeczywistych sprzedaży rozliczonej, jeśli nie istnieją kopie wartości rzeczywistych sprzedaży nierozliczonej. |
| Rozliczenia i ceny | 2668378 | Dodano walidacje uniemożliwiające dodanie niestandardowego wymiaru cen, o ile nie zostanie podana nazwa logiczna i nazwa pola. |
| Podwykonawstwo | 2677485 | Zaktualizowano docelową mapę podwójnego zapisu wierszy faktury od dostawcy. |
| Czas i wydatek | 2700428 | Poprawiono logikę zatwierdzeń, aby upewnić się, że inne zestawy zatwierdzeń dla projektu mogą być przetwarzane nawet w przypadku, gdy jeden z zestawów zatwierdzeń został zablokowany w obrębie zadań systemowych. |

### <a name="project-management-and-accounting-in-finance"></a>Zarządzanie projektami i księgowanie w Finance

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services (LCS) i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
