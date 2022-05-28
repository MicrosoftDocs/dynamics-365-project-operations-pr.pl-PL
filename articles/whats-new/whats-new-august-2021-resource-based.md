---
title: Co nowego w sierpniu 2021 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania
description: To temat zawiera informacje o istotnych aktualizacjach dostępnych w wydaniu aplikacji Project Operations z sierpnia 2021 r. dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 144a8c0d5ac47ad6fee54850c149a349f1698049
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594177"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co nowego w sierpniu 2021 r. — Project Operations dla scenariuszy obejmujących zasoby/nieobejmujących magazynowania

*Dotyczy: Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu*

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

   - Project Operations w środowisku Microsoft Dataverse w wersji 4.13.0.152.
   - Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.20.

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- **Zestawy zatwierdzeń**: zestawy zatwierdzeń grupują żądania zatwierdzenia użycia czasu, wydatków i materiałów razem w mniejsze podzestawy operacji. Takie grupowanie umożliwia przetwarzanie zatwierdzeń w określonej kolejności w ramach projektu oraz umożliwia ponowne przetwarzanie i sekwencjonowanie. Grupowanie żądań poprawia niezawodność i możliwość śledzenia przetwarzania zatwierdzeń w przypadku dużej liczby zatwierdzeń. Aby uzyskać więcej informacji, zobacz [Zestawy zatwierdzeń](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations — mapy podwójnego zapisu — aktualizacje

W tym wydaniu nie ma żadnych aktualizacji map podwójnego zapisu w aplikacji Project Operations.

Aktualną listę i wersje map podwójnego zapisu w aplikacji Project Operations można znaleźć w części [Wersje map podwójnego zapisu aplikacji Project Operations](../environment/resource-dual-write-maps.md).

Zawsze uruchamiaj najnowszą wersję mapy w środowisku i włącz wszystkie mapowania tabel pokrewnych podczas aktualizowania rozwiązania Project Operations Dataverse i wersji rozwiązania Finance. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli najnowsza wersja mapy nie zostanie aktywowana. Aktywna wersja mapy jest dostępna na stronie **Podwójny zapis** w kolumnie **Wersja**. Aktywuj nową wersję mapowania, wybierając **Wersje mapowania tabeli**, wybierając najnowszą wersję, a następnie zapisując wybraną wersję. Jeśli dostosowałeś niestandardową mapę tabeli, będziesz trzeba ponownie zastosować zmiany. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jeśli wystąpi problem z uruchomieniem mapy, postępuj zgodnie z instrukcjami w sekcji [Problem z brakującymi kolumnami na mapie w tabeli](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) w przewodniku rozwiązywania problemów z podwójnym zapisem.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2295625 | Nazwa punktu kontrolnego musi być skopiowana z harmonogramu faktur do szczegółów wiersza faktury. |
| Rozliczenia i ceny | 2316323 | Nie można edytować rabatu na fakturze proforma w aplikacji Project Operations w scenariuszach opartych na zasobach. |
|   Zarządzanie szansami sprzedaży | 2338619 | Reguły biznesowe **Szansa sprzedaży** i **Oferta** muszą być wywoływane tylko na stronach. |
| Zarządzanie zasobami | 2316523 | Użycie polecenia **Wyślij żądanie** z poziomu wymagania zasobu, który ma załączona rolę, nie powinno powodować wyświetlenia błędu. |
| Zarządzanie zasobami | 2326885 | Utworzenie wymagania zasobu w ramach projektu nie powinno powodować wyświetlenia błędu. |
| Czas i wydatek | 2335584 | Przestarzałe przepływy zadań są przepływami we wpisie czasu. |
| Czas i wydatek | 2336884 | Przycisk wpisu czasu **Kopiuj tydzień** musi działać dla więcej niż tylko bieżącego użytkownika. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Podróże i wydatki | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nieprawidłowe kwoty transakcji dostawcy i transakcji podatku są publikowane w momencie utworzenia wydatku na podstawie transakcji kartą kredytową. |
| Podróże i wydatki | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Nieprawidłowe wiersze rozliczenia są tworzone podczas generowania arkusza płatności. |
| Podróże i wydatki | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nieprawidłowe kwoty transakcji podatku są publikowane w momencie utworzenia wydatku na podstawie transakcji kartą kredytową. |
| Podróże i wydatki | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Usunięcie wiersza wydatku może zająć dużo czasu. |
| Księgowanie projektu | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | System nie obsługuje konfiguracji ciągłego sekwencjonowania liczb podczas księgowania szacowania po zastosowaniu artykułu bazy wiedzy KB 4619395. |
| Księgowanie projektu | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Księgowanie faktury dostawcy może się nie powieść, gdy zostanie wyświetlony komunikat o błędzie „Transakcje w załączniku nie są bilansowane na dzień 17.05.2021. (waluta rozliczeniowa: 0,00 — waluta raportowania: 0,01)" |
