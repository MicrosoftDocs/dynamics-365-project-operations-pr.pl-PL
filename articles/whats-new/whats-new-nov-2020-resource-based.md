---
title: Nowości Listopad 2020 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w wersji Project Operations z listopada 2020 r. w scenariuszach dotyczących zasobów/braku zapasów.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f8e9bce6612e617785264470b7946ffc4795a621
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291857"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości Listopad 2020 r. — Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

- Project Operations w środowisku CDS w wersji 4.4.0.70
- Zarządzanie projektami i ich księgowanie w wersji 10.0.14 środowiska Dynamics 365 Finance

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Aktualizacje Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu

### <a name="project-operations-on-cds"></a>Project Operations w CDS

| Obszar funkcji                 | Numer referencyjny | Aktualizacja dotycząca jakości                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Zarządzanie szansami sprzedaży       | 2036993          | Wiersze szacowania i wiersze kontraktu przydziału zasobów są aktualizowane w przypadku zwycięskich ofert, gdy typem wiersza oferty jest **Wszystkie zadania**.                                                 |
| Rozliczenia i ceny          | 2070392          | Pozycje kontraktu projektu na fakturze wzrastają po każdym wybraniu **Odśwież transakcje faktury**.                                                                         |
| Planowanie projektu             | 2043336          | Nie można usunąć rekordu członka   zespołu projektu.                                                                                                                                  |
| Planowanie projektu             | 2046013          | Niespójne zachowanie dotyczące oszacowań kolumn znaczników podczas ładowania i przy zmianie typu fazy czasu.                                                                                   |
| Planowanie projektu             | 2046647          | Godziny rozpoczęcia i zakończenia są na godzinę wypadane w czasie, gdy wymagania dotyczące zasobów są generowane przez członków zespołu projektu.                                                                      |
| Planowanie projektu             | 2053879          | (Zgodnie z nadchodzącym wdrożeniem CDS) PublishUnassignedAssignments przerywa próbę zapisania zadania, gdy błąd „Wartość przekazana dla elementu ConditionOperator.In jest pusta”.                       |
| Planowanie projektu             | 2055501          | Pozostawienie pustej **Daty rozpoczęcia projektu** powoduje niepowodzenie w harmonogramie.                                                                                                      |
| Planowanie projektu             | 2066817          | Nie może utworzyć zasobu generycznego przy użyciu selektora osób na karcie **Zadania**.                                                                                                   |
| Planowanie projektu             | 2067034          | Przycisk **Pokaż szczegóły** jest niedostępny na stronie **Szczegóły zadania**.                                                                                                       |
| Zarządzanie zasobami          | 2046667          | Członkowie zespołu generycznego nie są usuwani nawet po spełnieniu wszystkich zasobów.                                                                                                    |
| Czas i szybki wpis wydatków | 2047499          | Przycisk **Nowy** na stronie wprowadzania czasu otwiera stronę **Nowy podpis wiadomości e-mail**.                                                                                               |
| Czas i szybki wpis wydatków | 2059859          | Nieoczekiwane podręczne otwieranie podczas tworzenia wpisu wydatku.                                                                                                                         |
| Inny powód                        | 2044181          | (Odinstalowywanie zamówienia zakupu) Podczas próby odinstalowania msdyn_ProjectServiceCore_Patch i msdyn Project Service core rozwiązań pojawia się błąd „Rekord jest niedostępny”.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Omówienie zarządzania projektami i księgowania w Dynamics 365 Finance

| Obszar funkcji        | Numer referencyjny | Aktualizacja dotycząca jakości                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ujmowanie przychodów | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Szacowana wartość procentu wykonania projektu jest niewłaściwa w przypadku, gdy w kontrakcie jest używana waluta obca, a wartość procentowa postępu pracowania dla metody całkowitej.                     |
| Ujmowanie przychodów | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Nie można opublikować oszacowań z metodą zakończenia **Rzeczywisty koszt**.                                                                                                    |
| Ujmowanie przychodów | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminacja kończy się niepowodzeniem z powodu błędu niezbilansowania kuponu, gdy waluta firmy i waluta transakcji są różne.                                              |
| Zarządzanie wydatkami  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | W przypadku użytkowników innych niż administrator wartości wyszukiwania kolumn wierszy wydatku, takich jak **Identyfikator projektu** i **Kategoria wydatków**, nie są poprawnie wyświetlane w ramce łącznika danych. |
| Zarządzanie wydatkami  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Domyślna właściwość wiersza nie jest wyświetlana dla kategorii wydatków.                                                                                                         |
| Zarządzanie wydatkami  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integracja z wydatkami musi zawierać właściwość wiersza z raportu o wydatkach.                                                                                             |
| Fakturowanie           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Nie można ogłosić propozycji faktur projektu z powodu komunikatu o błędzie z informacją, że kombinacja FD nie została sprawdzona.                                                    |
| Fakturowanie           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Nie można wyświetlać transakcji na stronie z informacjami szczegółowymi **faktury**.                                                                                                              |
| Fakturowanie           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Można usunąć wiersze propozycji faktury.                                                                                                                                  |
| Księgowanie projektu  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Elementy menu **Prognozy** nie są widoczne na stronie listy **Projektów**.                                                                                                   |
| Księgowanie projektu  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nie można otworzyć **Oświadczenie projektu**   > **Transakcje i prognoza**.                                                                                                       |
| Księgowanie projektu  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Koryguj Księgowanie** nie jest włączone dla zafakturowanych transakcji projektu.                                                                                                  |
| Księgowanie projektu  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Szczegóły księgowania nie są uwzględniane w tabeli **ProjCDSActualsImport** podczas księgowania arkusza **Integracji**.                                                  |
| Księgowanie projektu  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Po usunięciu, a następnie poodczycie przydziału zasobu wpis prognozy projektu jest podwójny.                                                                            |
| Księgowanie projektu  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Wybranie linku do identyfikatora projektu nie powoduje otwarcia adresu URL precyzyjnego linku CDS.                                                                                                         |
| Księgowanie projektu  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nie można zaktualizować daty rozpoczęcia zadania w CDS.                                                                                                                           |
| Księgowanie projektu  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Włączenie tej funkcji, Wiele linii kontraktu nie jest możliwe bez integracji CDS.                                                                                   |

### <a name="regulatory-updates"></a>Aktualizacje dotyczące regulacji
Aby uzyskać więcej informacji na temat aktualizacji dotyczących aplikacji Finance and Operations, zobacz artykuł dotyczący [Aktualizacje dotyczące regulacji](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Można również zalogować się w LCS i wyświetlić planowane aktualizacje ustawodawcze, korzystając z narzędzia do wyszukiwania problemów. Funkcja wyszukiwanie problemów umożliwia wyszukiwanie według kraju, typu funkcji oraz wydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]