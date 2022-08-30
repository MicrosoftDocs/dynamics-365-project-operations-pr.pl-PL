---
title: Co nowego w sierpniu 2022 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z sierpnia 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/niemagazynowanych.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348025"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego w sierpniu 2022 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.45.0.53
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations. Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli nie jest aktywowana najnowsza wersja mapy. Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś domyślną mapę tabeli, zastosuj zmiany ponownie. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
|   Zarządzanie szansami sprzedaży | 2762089 | Obsługa błędów podczas zamykania kontraktu jako utraconego, jeśli funkcja automatycznego zapisywania jest wyłączona w organizacji.|

### <a name="project-management-and-accounting-in-finance"></a>Zarządzanie projektami i księgowanie w Finance

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services (LCS) i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
