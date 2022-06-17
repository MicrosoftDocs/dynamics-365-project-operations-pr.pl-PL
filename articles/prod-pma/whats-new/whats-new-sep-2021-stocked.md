---
title: Co nowego i zmienionego we wrześniu 2021 r. — Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne
description: Ten artykuł zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations we wrześniu 2021 r. dla scenariuszy opartych na inwentarzu/produkcji.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916531"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Co nowego i zmienionego we wrześniu 2021 r. — Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne

_**Dotyczy:** Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.21
 
## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
|---|---|---|
| Zarządzanie projektami i księgowanie | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jeśli rola Kierownik zakupów otrzyma dostęp do jednej osoby prawnej, uzyska również dostęp do wszystkich projektów we wszystkich osobach prawnych. |
| Zarządzanie projektami i księgowanie | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Problem z zaokrąglaniem podatku VAT pojawia się podczas rozliczania noty kredytowej z pierwotną fakturą projektu. |
| Zarządzanie projektami i księgowanie | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | W celu weryfikacji budżetu użyj alternatywnych budżetów projektów. |
| Zarządzanie projektami i księgowanie | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Grupa cenowa **Godzina sprzedaży** nie jest obliczana na strukturze podziału pracy dla ofert projektowych. |
| Zarządzanie projektami i księgowanie | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Eliminacja szacowania nie powiedzie się, gdy funkcja **Włącz walutę kontraktu projektu dla obliczania szacowania**. |
| Zarządzanie projektami i księgowanie | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktoryzacja podatku od sprzedaży według ilości jest dodawana do kwoty ceny sprzedaży, gdy podatek od sprzedaży jest stosowany w grupie podatku od sprzedaży w dzienniku wydatków projektu. |
| Zarządzanie projektami i księgowanie | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Podatek warunkowy nie jest obliczany poprawnie dla ostatniej płatności, gdy zatrzymanie sprzedawcy i przedpłata są stosowane do faktur zamówień zakupu. |
| Zarządzanie projektami i księgowanie | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Śledzenie korekt nie działa w przypadku dzienników Salda początkowego. |
| Zarządzanie projektami i księgowanie | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Rozdział zmian w budżecie projektu na okres** jest podzielony na wszystkie okresy budżetowe. Kiedy przydział jest składany, zapis nie jest czyszczony. |
| Zarządzanie projektami i księgowanie | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Księgowanie produkcji w toku (WIP) do księgi głównej ma nieprawidłową kwotę. |
| Zarządzanie projektami i księgowanie | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Zatwierdzenie dziennika godzin projektowych nie działa. |
| Zarządzanie projektami i księgowanie | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Cena sprzedaży korekty projektu nie jest aktualizowana o koszty pośrednie, gdy limit finansowania jest niezaznaczony. |
| Zarządzanie projektami i księgowanie | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Zapotrzebowanie na pozycję nie może być utworzone, gdy nagłówek tabeli Sprzedaż jest zafakturowany i sfinalizowane zostało rezerwowe zamówienie zakupu dla istniejących linii. |
| Zarządzanie projektami i księgowanie | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Kwota retencji dla reguły rozliczeniowej, która ma kamień milowy dla innego projektu, nie jest księgowana w odpowiednim identyfikatorze projektu, który został wybrany dla kamienia milowego. Zamiast tego jest on publikowany razem z pierwszym projektem. |
| Zarządzanie projektami i księgowanie | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Po wybraniu **Zestawu wymiarów finansowych** na propozycji faktury pojawia się następujący błąd: „Unable to cast object of type 'Dynamics.AX.Application.FormIntControl' na typ 'Dynamics.AX.Application.FormStringControl'.”. |
| Zarządzanie projektami i księgowanie | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Raport **Faktura za projekt** pomija wiersze. |
| Zarządzanie projektami i księgowanie | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Podczas obliczania kontroli kosztów dla projektu inwestycyjnego pojawia się błąd. |
| Zarządzanie projektami i księgowanie | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metoda **ProjTable::InitFromCustTable - canDeletePostalAddress** powoduje problem z wydajnością. |
| Zarządzanie projektami i księgowanie | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Komunikat o błędzie powinien być jaśniejszy niż „Nieoczekiwany błąd”. |
| Zarządzanie projektami i księgowanie | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Zadanie wsadowe księgowania faktur projektu przetwarza i księguje propozycję faktury, nawet jeśli linie faktur nie zostały wygenerowane. |
| Zarządzanie projektami i księgowanie | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Problem z zaokrąglaniem występuje, gdy klucz konfiguracji licencji sektora publicznego jest wyłączony. Nieprawidłowy koszt lub cena sprzedaży są generowane na godzin arkusza czasu dla umów, które mają wiele źródeł finansowania. |
| Zarządzanie projektami i księgowanie | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Cena sprzedaży projektu na zafakturowanym zleceniu zakupu projektu jest nieprawidłowo obliczana, gdy model ceny sprzedaży to **Stosunek wkładu**. |
| Zarządzanie projektami i księgowanie | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | System nie bierze pod uwagę aktywnych dni pomiędzy nimi, kiedy oblicza efektywną stawkę roboczą dla pracownika. |
| Zarządzanie projektami i księgowanie | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | W arkuszu czasu pracy między firmami występuje błąd księgowania z powodu następującego błędu walidacji: „Nie skonfigurowano partnera handlowego dla osoby prawnej”. |
| Zarządzanie projektami i księgowanie | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis z zamówienia zakupu, który ma kategorię wydatku nie jest pobierany na liście transakcji zaksięgowanego projektu. |
| Zarządzanie projektami i księgowanie | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Występuje nieprawidłowa konwersja w dziennikach pozycji, które są księgowane do projektu. |
| Zarządzanie projektami i księgowanie | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Możesz potwierdzić zlecenie zakupu, nawet jeśli limit środków został przekroczony. |
| Zarządzanie projektami i księgowanie | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Sekcja **Faktura korygująca/anulująca** na fakturze tekstowej znika po wybraniu identyfikatora projektu. |
| Zarządzanie projektami i księgowanie | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Występują problemy z wydajnością, gdy propozycja faktury projektowej jest księgowana na podstawie zamówienia sprzedaży projektu, które zawiera pozycję magazynową. |
| Zarządzanie projektami i księgowanie | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Faktury zakupu projektu nie można zaksięgować, ponieważ występuje następujący błąd: „Funkcja AccDistProcessorProjectExtension.createForProjectRevenueLine została niepoprawnie wywołana”. |
| Zarządzanie projektami i księgowanie | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Aktualizacja do tworzenia zadań wsadowych kosztorysu projektu w celu wsparcia realizacji wielu podzadań. |
| Zarządzanie projektami i księgowanie | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status arkusza nie może zostać zaktualizowany do **Wersji roboczej**, gdy przepływ pracy znajduje się w stanie **Zakończony**. |
| Zarządzanie projektami i księgowanie | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Kwoty zatrzymania nie są obliczane w propozycji faktury noty kredytowej, jeśli istnieje wiele linii. |
| Zarządzanie projektami i księgowanie | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Przy próbie zmiany kwoty na wygenerowanej fakturze z zamówienia zakupu pojawia się następujący błąd: „Transakcje na voucherze nie bilansują się wg stanu na dzień XX/XX/XXXX. (waluta rozliczeniowa: 0,00 — waluta raportowania: 0,01).” |
| Zarządzanie projektami i księgowanie | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Występuje problem z wydajnością, gdy propozycja faktury projektowej jest księgowana w trybie wsadowym, z powodu połączenia z **GeneralJournalAccountEntry**. |
| Zarządzanie projektami i księgowanie | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Występują problemy z wydajnością podczas księgowania arkusza czasu pracy. |
| Zarządzanie projektami i księgowanie | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarchia kosztorysów w strukturze podziału pracy nie jest prawidłowo wyrównana po rozwinięciu wszystkich zadań lub po ręcznym rozwinięciu pojedynczego zadania. |
| Zarządzanie projektami i księgowanie | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Szablon Excel z wyceną projektu nie może zostać dodany do menu **Otwórz w Excelu**. |
| Zarządzanie projektami i księgowanie | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Numer zwolnienia podatkowego dla osoby prawnej nie jest umieszczony na wydrukowanej fakturze za projekt. |
| Zarządzanie projektami i księgowanie | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | W przypadku korekty projektu w odniesieniu do linii kredytowych w błędzie jednostki inwentaryzacyjnej nie są aktualizowane żadne dane finansowe. |
| Zarządzanie projektami i księgowanie | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Po zastosowaniu KB 461935 nie można opublikować szacunków, jeśli przejdziesz na ciągłe sekwencje numerów. |
| Zarządzanie projektami i księgowanie | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** powoduje, że aplikacja mobilna Project timesheet dla systemu Android przestaje odpowiadać. |
| Zarządzanie projektami i księgowanie | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Odwrócona wartość WIP z księgowania faktury różni się od pierwotnie zaksięgowanej wartości WIP z wpisu czasowego. |
| Zarządzanie projektami i księgowanie | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | W stosowanych przypadkach zatrzymania transakcji, transakcje na voucherze nie bilansują się po zaksięgowaniu zafakturowanych przychodów z projektu. |
| Zarządzanie projektami i księgowanie | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Gdy włączona jest funkcja **Wzmocnienie wydajności planowania zasobów projektu**, wartości dziesiętne dla dostępności i pojemności zasobów są nieprawidłowo zaokrąglane. |
| Zarządzanie projektami i księgowanie | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Gdy włączona jest funkcja **Twórz oszacowania projektu przy użyciu wielu zadań wsadowych**, tworzenie oszacowań w wsadzie, który ma wiele podzadań, działa tylko dla bieżącego okresu. |
| Podróże i wydatki | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Polityka żądania podróży jest ignorowana, a przepływ pracy jest zatwierdzany bez błędów. |
| Podróże i wydatki | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobilna aplikacja wydatków nie zapisuje następujących informacji w wierszu wydatku:</p><ul><li>Identyfikator projektu</li><li>Czy koszt jest rozliczany</li><li>Numer działalności</li></ul> |
| Podróże i wydatki | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Pole **Dołączony dokument dostawy** jest ustawione na **Tak**, nawet jeśli w wierszu wydatku nie jest dołączony paragon. |
| Podróże i wydatki | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Podczas próby zmiany kategorii wydatków na **Osobiste** pojawia się komunikat o błędzie. |
| Podróże i wydatki | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Nie można dołączyć paragonu i edytować wydatku macierzystego po podzieleniu transakcji kartą kredytową na wydatek osobisty. |
| Podróże i wydatki | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Nie działa poprawnie polityka wydatków dla transakcji między firmami, które mają identyfikator projektu. |
| Podróże i wydatki | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | W przypadku zaksięgowanych raportów wydatków brakuje informacji o dacie zaksięgowania. |
| Podróże i wydatki | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | W aplikacji mobilnej wydatków występują problemy z formami płatności. |
| Podróże i wydatki | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Zapotrzebowanie na podróż, które zostało utworzone dla jednego pracownika, może zostać wykorzystane do raportu wydatków innego pracownika przed datą delegacji. |
| Podróże i wydatki | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Podczas tworzenia wydatku zmiany wartości wymiaru finansowego nie są prawidłowo aktualizowane na poziomie podziału księgowego w obszarze roboczym **Zarządzanie wydatkami**. |
| Podróże i wydatki | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Stan zatwierdzania głównego wiersza wydatków nie jest zsynchronizowany ze stanem zatwierdzania przepływu pracy wiersza pozycji. |
| Podróże i wydatki | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Błąd pojawia się, gdy księgujesz raport wydatków, a odzyskiwanie podatku jest włączone. |
| Podróże i wydatki | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Użytkownik delegowany nie może usuwać dokumentów dotyczących wydatków dla pracownika, który zakończył pracę. |
| Podróże i wydatki | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Usunięcie pozycji wydatków trwa dłużej niż oczekiwano i wpływa na wydajność. |
| Podróże i wydatki | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** powoduje oddzielenie rekordu **TaxUncommitted** z powodu usunięcia tylko **SourceDocumentLine**. |
| Podróże i wydatki | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** nie honoruje ciągu **trvExpTrans.ReferenceDataAreaId** do utworzenia nowej sekwencji numerów. |

## <a name="regulatory-updates"></a>Aktualizacje dotyczące regulacji

Aby uzyskać informacje na temat aktualizacji przepisów prawnych dotyczących aplikacji finansowych i operacyjnych, zobacz [Aktualizacje prawne](/dynamics365/finance/localizations/regulatory-updates). Można również zalogować się do Microsoft Dynamics Lifecycle Services (LCS) i skorzystać z narzędzia wyszukiwania zagadnień, aby wyświetlić planowane aktualizacje przepisów. Wyszukiwanie według zagadnień umożliwia wyszukiwanie według kraju lub regionu, typu elementu i wydania.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
