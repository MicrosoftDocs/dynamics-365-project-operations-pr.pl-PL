---
title: 'Nowości: styczeń 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów'
description: Ten artykuł zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations w styczniu 2021 r. dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cd20ba47a45593e7694234b4f58aecd79b1c3736
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910689"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości: styczeń 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


Ten artykuł dotyczy następujących składników i wersji oprogramowania Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.6.0.154
  - Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.16

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| **Wdrażanie i konfiguracja** | 2106818 | Poprawiono nazwę witryny webresource, która powoduje problemy związane z dostosowywaniem strony. |
| **Rozliczenia i ceny** | 2091908 | Poprawiono widoczność **Zablokuj kalkulację cen** i opcji **Użyj bieżącej kalkulacji cen** na stronie **Faktura**, gdy Project Operations są instalowane razem z Dynamics 365 Field Service. |
| **Rozliczenia i ceny** | 2103058 | Odświeżone **Sumy projektu** w celu obsługi wartości null dla kosztu rzeczywistego zadania. |
| **Rozliczenia i ceny** | 2116100 | Udoskonalone komunikaty o błędach używane z funkcjonalnością, **Poprawianie wpisów w wartościach rzeczywistych**. |
| **Rozliczenia i ceny** | 2116129 | Ulepszony wgląd w szacowanie kosztów na karcie **Szacowanie** na stronie **Projekty**. |
| **Rozliczenia i ceny** | 2119112 | Stałe agregowanie rzeczywistej sprzedaży i kosztu rzeczywistego przy różnych kursach wymiany walut. |
| **Rozliczenia i ceny** | 2134705 | Poprawiono błąd „Nie można odczytać właściwości **getResourceString** niezdefiniowanego” po otwarciu strony **Faktura** i zainstalowaniu usługi Field Service. |
| **Zarządzanie szansami sprzedaży** | 2022195 | Na stronie **Projekt** siatka rozliczeń oparta na zadaniach zawiera ikonę wskazującą, że z tym zadaniem jest połączony kontrakt lub wiersz oferty. |
| **Zarządzanie szansami sprzedaży** | 2029135 | Naprawiono błąd procesu biznesowego, który występuje, gdy użytkownik próbuje otworzyć wiersz faktury na potwierdzonej fakturze z zafakturowaną kwotą z góry. |
| **Zarządzanie szansami sprzedaży** | 2040713 | Rozwiązano błąd skryptu wyświetlany podczas tworzenia faktury z kontraktu i zainstalowanej usługi Field Service. |
| **Planowanie i śledzenie projektu** | 2090202 | Oznaczone reguły biznesowe, które nie są już używane jako **Przestarzałe**. |
| **Czas i wydatek** | 2091249 | Kontrolki z przechowanem widać, że użytkownicy nie mogą zmieniać zadania w przesłanym lub zatwierdzonym wpisie czasu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| **Zarządzanie projektami i księgowanie** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Nieprawidłowa kwota kontraktu na stronie **Dla klienta** dla projektu o stałej cenie z wieloma źródłami źródeł. |
| **Zarządzanie projektami i księgowanie** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Symbol zastępczy **Invoiceproposal.PSArefProjId** nie wyświetla identyfikatora projektu dla przepływu pracy. **Przeglądanie ofert na fakturze projektu**. |
| **Zarządzanie projektami i księgowanie** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Podczas księgowania propozycji faktur projektu jest używana niewłaściwa data rabatu gotówkowego. |
| **Zarządzanie projektami i księgowanie** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Usunięcie i odczytanie przydziałów zasobów w Project Operations podwaja wpisy prognozy projektu w programie Finance. |
| **Zarządzanie projektami i księgowanie** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | W Project Operations nie można tworzyć szacunków projektu w Dataverse bez wiersza umowy w projekcie. |
| **Zarządzanie projektami i księgowanie** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Wymiar finansowy transakcji wydatku projektu nie jest zsynchronizowany z powiązanym załącznikiem i dystrybucją księgową raportu z wydatków, gdy koszty są księgowane w Saldzie. |
| **Zarządzanie projektami i księgowanie** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filtrowanie **Stan faktury** w zaksięgowanych transakcjach projektów dotyczących projektów o stałej cenie nie działa. |
| **Zarządzanie projektami i księgowanie** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminacja szacowania wstecznego nie działa w sekcji **Okresowe**. |
| **Zarządzanie projektami i księgowanie** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Wiersze propozycji faktury można usunąć w Project Operations po zintegrowaniu z Dataverse. |
| **Zarządzanie projektami i księgowanie** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Uniemożliwia włączanie funkcji wielu pozycji kontraktu bez integracji usługi Dataverse. |
| **Zarządzanie projektami i księgowanie** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Gdy fakturowanie na koncie jest równe zyskom i stratom, zafakturowany przychód jest wyświetlany jako zero na stronie Szacunki. |
| **Zarządzanie projektami i księgowanie** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Korekty faktur nie działają w środowiskach zintegrowanych. |
| **Zarządzanie projektami i księgowanie** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Podczas księgowania PWT - wartość sprzedaży w międzyfirmowym fakturowaniu projektu, wybierane jest niewłaściwe konto. |
| **Zarządzanie projektami i księgowanie** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | W Project Operations nie można aktualizować zależności od zadań szacowania w Dataverse. |
| **Zarządzanie projektami i księgowanie** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Wielokrotne usuwanie dzienników integracji Project Operations w programie Finance prowadzi do utraty danych. |
| **Zarządzanie projektami i księgowanie** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Następujący błąd występuje podczas księgowania propozycji faktury projektu: „Transakcja nie jest równoważona w walucie raportowania po dodaniu potrąconej faktury zaliczkowej”. |
| **Zarządzanie projektami i księgowanie** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Niewłaściwy identyfikator projektu jest uwzględniany w odliczeniach po zaktualizowaniu domyślnej umowy dotyczącej projektu w Project Operations. |
| **Zarządzanie projektami i księgowanie** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Szacowania i rozpoznawania przychodów nie można ukończyć po włączeniu Project Operations. |
| **Zarządzanie projektami i księgowanie** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | W Project Operations usunięcie projektu z umowy nie powoduje zresetowania domyślnego projektu w umowie. |
| **Zarządzanie projektami i księgowanie** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | W Project Operations na fakturze międzyfirmowej na liście **Dodaj wiersz** pojawiają się nieprawidłowe wiersze wydatków. |
| **Podróże i wydatki** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Nie można zaksięgować wierszy wydatków, ponieważ w wierszu umowy brakuje ustawienia godziny. |
| **Podróże i wydatki** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Gdy walidacja projektu / kategorii jest obowiązkowa, kategorie wydatków skojarzone z projektem nie są widoczne w raporcie z wydatków. |
| **Podróże i wydatki** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Saldo zaliczki gotówkowej nie jest aktualizowane, gdy raport z wydatków jest księgowany według wiersza. |
| **Podróże i wydatki** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Zadanie **Zaktualizuj informacje o płatności** kończy się niepowodzeniem po cofnięciu rozliczeń, w których faktura została rozliczona z co najmniej dwoma transakcjami płatniczymi. |
| **Podróże i wydatki** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Występuje problem z obliczeniem obniżki za ostatni dzień posiłku dla kategorii wydatków dziennych. |
| **Podróże i wydatki** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Raport **Koszt na pracownika** nie pokazuje wyszczególnionych wydatków, jeśli pierwsze połączenie użytkownika było w języku es-MX. |
| **Podróże i wydatki** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Płatność dostawcy dla faktury raportu z wydatków używa niewłaściwego podsumowującego do księgowania rozliczenia. |
| **Podróże i wydatki** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Kiedy raport wydatków jest księgowany z włączoną opcją **Zezwalaj na grupowanie transakcji na podstawie przeciwstawnego konta płatności** i **Poprawianie daty księgowania przy włączonym księgowaniu** zawiera daty księgowania, które nie są zgrupowane w tabeli **zasad podziału księgowań**, co ma wpływ na rekordy podatku. |
| **Podróże i wydatki** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Mapowanie podkategorii wydatków jest usuwane, gdy pole wyboru Użyj w wydatku jest wyczyszczone, a następnie ponownie wybrane. |
| **Podróże i wydatki** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Nie można utworzyć raportu z wydatków międzyfirmowych, jeśli identyfikator projektu został dodany na poziomie nagłówka. |
| **Podróże i wydatki** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Występuje problem z płatnościami z tytułu wydatków, gdy kwota wydatku przekracza kwotę zaliczki gotówkowej. |
| **Podróże i wydatki** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Pole **Identyfikator projektu** w ramach międzyfirmowego raportu o wydatkach są puste, jeśli rola użytkownika jest przypisana do określonej organizacji. |
| **Podróże i wydatki** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategoria wydatków jest blokowana podczas dodawania nowej linii wydatków. |
| **Podróże i wydatki** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Wyszczególnienie wierszy raportu z wydatków, które zostały już podzielone, skutkuje niekompletnym zaksięgowaniem rozrachunków z dostawcami\Załącznikiem księgi głównej. Z powodu powielenia **TRVEXPTRANS.SOURCEDOCUMENTLINE**, Eksplorator źródeł rozliczeń również jest uszkodzony. |
| **Podróże i wydatki** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indeks dodany do tabeli **TRVREQUISITIONLINE**, dla której klient ma duplikaty, powoduje błąd podczas aktualizacji. |
| **Podróże i wydatki** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | W Project Operations nie można tworzyć ani zatwierdzać czasu z zadaniami międzyfirmowymi w Dataverse. |

## <a name="regulatory-updates"></a>Aktualizacje dotyczące regulacji

Aby uzyskać informacje na temat aktualizacji przepisów prawnych dotyczących aplikacji finansowych i operacyjnych, zobacz [Aktualizacje prawne](/dynamics365/finance/localizations/regulatory-updates). Można również zalogować się w LCS i wyświetlić planowane aktualizacje ustawodawcze, korzystając z narzędzia do wyszukiwania problemów. Funkcja wyszukiwanie problemów umożliwia wyszukiwanie według kraju, typu funkcji oraz wydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]