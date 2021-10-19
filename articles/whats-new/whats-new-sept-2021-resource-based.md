---
title: Co nowego, wrzesień 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: To temat zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations we wrześniu 2021 r. dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547167"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego, wrzesień 2021 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

*Dotyczy: Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu*

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

   - Project Operations w środowisku Microsoft Dataverse w wersji 4.14.0.99.
   - Zarządzanie projektami i ich księgowanie w wersji 10.0.20 środowiska Dynamics 365 Finance.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations. Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli najnowsza wersja mapy nie zostanie aktywowana. Aktywna wersja mapy jest dostępna na stronie **Podwójny zapis** w kolumnie **Wersja**. Aby uaktywnić nową wersję mapy, wybierz **Wersję mapowania tabeli**, a następnie zapisz wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś niestandardową mapę tabeli, będziesz trzeba ponownie zastosować zmiany. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami tabeli w mapach](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) przewodnika po rozwiązywaniu problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Czas i wydatek | 1811407 | Dostosowana rola zabezpieczeń osoby zatwierdzające projekt dla zatwierdzeń wpisów wydatków. |
| Czas i wydatek | 1811438 | Dostosowana rola zabezpieczeń osoby zatwierdzające projekt dla anulowania zatwierdzeń wpisów czasu. |
| Czas i wydatek | 2370126 | Zaktualizowane ikony **Zadanie projektu** i **Rola** w encji **Wpis czasu**. |
| Czas i wydatek | 2379879 | Poprawiono funkcję **Kopiuj tydzień** we wpisie czasu podczas korzystania z aplikacji Dynamics 365 na telefony. |
| Rozliczenia i ceny | 2371906 | W przypadku Project Operations dla wdrożeń opartych na zasobach nie można dostosowywać łącznej kwoty na fakturze proforma. |
| Rozliczenia i ceny | 2385802 | Naprawiony błąd, który występuje przy ujemnych godzinach rzeczywistych, gdy są odświeżane łączne wartości projektu. |
| Rozliczenia i ceny | 2389675 | Udoskonalone zachowanie potwierdzenia faktury proforma. Encja długotrwałego zadania musi uwzględniać działanie wymagane do zapisu wyników potwierdzenia dla księgowania. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Omówienie zarządzania projektami i księgowania w Dynamics 365 Finance

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Podróże i wydatki | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kwoty w transakcjach z dostawcami i podatkowych, które są księgowane z wydatku tworzonego z transakcji karty kredytowej, są nieprawidłowe. |
| Podróże i wydatki | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Nieprawidłowe wiersze rozliczenia są tworzone podczas generowania arkusza płatności. |
| Podróże i wydatki | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kwoty w transakcjach podatkowych, które są księgowane z wydatku tworzonego z transakcji karty kredytowej, są nieprawidłowe. |
| Podróże i wydatki | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Usunięcie wiersza wydatku może zająć dużo czasu. |
| Księgowanie projektu | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Po zastosowaniu bazy danych 4619395 zmiana sekwencji numerów na **Ciągłe** nie jest obsługiwana i podczas księgowania szacowania pojawia się następujący błąd: „System nie obsługuje konfiguracji «ciągłe» z sekwencją Proj_X”. |
| Księgowanie projektu | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Księgowanie faktury od dostawcy może się nie powieść, gdy zostanie wyświetlony następujący komunikat o błędzie „Transakcje w załącznika z dnia 17.05.2021 nie są zrównoważone. (waluta rozliczeniowa: 0,00 — waluta raportowania: 0,01).” |
