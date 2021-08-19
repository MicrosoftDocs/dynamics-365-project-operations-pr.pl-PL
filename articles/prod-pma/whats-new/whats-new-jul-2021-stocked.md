---
title: Co nowego lub co się zmieniło w aplikacji Project Operations w lipcu 2021 r. dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne
description: To temat zawiera informacje o istotnych aktualizacjach dostępnych w wydaniu aplikacji Project Operations z lipca 2021 r. dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: dadcf3e9fa8432fb66f76b7c2f0fdb98bc00511d93984ea98fa30b4fc03fa426
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992714"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Co nowego lub co się zmieniło w aplikacji Project Operations w lipcu 2021 r. dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne

_**Dotyczy:** Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

- Zarządzanie projektami i ich księgowanie w wersji 10.0.20 środowiska Dynamics 365 Finance
 
### <a name="quality-updates"></a>Aktualizacje dotyczące jakości
                                                                                                                                                                                  
| Obszar funkcji                      | Numer referencyjny| Aktualizacja dotycząca jakości                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zarządzanie projektami i księgowanie | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Rekordy zobowiązań kosztowych z zapotrzebowania zakupu są czyszczone, gdy tylko zamówienie zakupu zostanie zwolnione z problemu z zapotrzebowaniem zakupu.                                                                           |
| Zarządzanie projektami i księgowanie | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Walidacja budżetu występuje dwa razy w przypadku zapotrzebowania zakupu. Ta duplikacja oznacza, że nie można zamknąć zapotrzebowania, a odpowiednie zamówienie zakupu nie jest tworzone.                                                                                                                        |
| Zarządzanie projektami i księgowanie | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Z powodu problemu z zaokrąglaniem nie można wykonać reguły rozliczeń **Procent do rozliczania**.                                                                              |
| Zarządzanie projektami i księgowanie | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Po dostosowaniu transakcji, gdy procent ma miejsca po przecinku, koszt i cena sprzedaży nie są prawidłowo korygowane.                                      |
| Zarządzanie projektami i księgowanie | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Eksplorator źródeł księgowania pokazuje godziny dla jednej linii grafiku w przypadku wielu wierszy grafiku z różnymi działaniami.                                      |
| Zarządzanie projektami i księgowanie | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Personalizacja zapisanych widoków i szczegółów wiersza grafiku powoduje, że system zawsze otwiera szczegóły dla pierwszego grafiku na liście podczas próby otwarcia grafiku.  |
| Zarządzanie projektami i księgowanie | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Węzeł główny projektu znika, a rekordy struktury podziału pracy są usuwane po imporcie.                                                                                             |
| Zarządzanie projektami i księgowanie | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Gdy elementy są odbierane i wydawane w części z wymagania dotyczącego pozycji, system aktualizuje nieprawidłowe saldo wykorzystania budżetu. |
| Zarządzanie projektami i księgowanie | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | W okienku **Sumy** lub w siatce **Faktura oczekująca** sumy pozostałych zamówień zakupu w projekcie nie są wyświetlane prawidłowo.                                                                  |
| Zarządzanie projektami i księgowanie | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Podczas zamykania zapasów korekty kosztów pozycji projektu są publikowane na koncie salda, a nie na koncie zysków i strat.                                                            |
| Zarządzanie projektami i księgowanie | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Załącznik zaksięgowanej transakcji projektu i załącznik wartości szacowanych używają USD jako waluty rozliczeniowej, ale kwota jest pokazywana jako równoważnik w CAD.              |
| Zarządzanie projektami i księgowanie | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Potwierdzone koszty z wymaganiem pozycji i zamówieniem zakupu są niewłaściwe w procesie faktury zamówienia zakupu z częściowym odbiorem produktu i częściowym fakturowaniem.       |
| Zarządzanie projektami i księgowanie | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Korekta projektu nie aktualizuje prawidłowo kwoty sprzedaży o koszty pośrednie.                                                                                    |
| Zarządzanie projektami i księgowanie | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | W tabeli **Grafik** brak zdefiniowanej relacji z widokiem **Proces roboczy/zasób**.                                                                                   |
| Zarządzanie projektami i księgowanie | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Nie można wypełnić pola **Numer działania** po wybraniu go z menu rozwijanego dla grafiku międzyfirmowego.                                                                 |
| Zarządzanie projektami i księgowanie | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Nie można dodać spersonalizowanego pola **Cel** lub **Opis działania** do następujących stron: **Zaksięgowana transakcja projektu**, **Tworzenie propozycji faktury** lub **Propozycja faktury**.  |
| Zarządzanie projektami i księgowanie | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Nieprawidłowa kontrola daty dostawy następuje po utworzeniu wymagań dotyczących pozycji przy użyciu funkcji zarządzania danymi (**ProjSalesItemRequirementEntity**).                                              |
| Zarządzanie projektami i księgowanie | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Po wybraniu identyfikatora kontraktu projektu w aplikacji Finance zintegrowane środowisko Project Operations otwiera stronę, aby utworzyć nowy rekord, a nie otworzyć istniejący kontrakt projektu.                                                                                                                 |
| Zarządzanie projektami i księgowanie | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Etykieta „@SYS4083080” („Nie można znaleźć unikatowego rekordu procesu roboczego odpowiadającego wprowadzonym wartościom”) nie jest tłumaczona na język duński.                                |
| Zarządzanie projektami i księgowanie | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Pola **Grupy podatku pozycji** nie można edytować w propozycji faktury.                                                                               |
| Zarządzanie projektami i księgowanie | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Koszt zatwierdzony jest zawyżony przy użyciu kwot podatku, których nie można odliczać.                                                                                                    |
| Zarządzanie projektami i księgowanie | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Opublikowanie grafiku międzyfirmowego z wieloma projektami i różnymi wymiarami finansowymi generuje nieoczekiwane wartości w księdze głównej.                             |
| Zarządzanie projektami i księgowanie | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Wiersze propozycji faktur są duplikowane z powodu wielokrotnych wystąpień procesów okresowych **Import z etapu przejściowego** uruchomionych w tym samym czasie.                                      |
| Zarządzanie projektami i księgowanie | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Podczas księgowania propozycji faktury z notą kredytową wystąpił błąd, dlatego transakcje w załączniku nie są bilansowane.    |
| Zarządzanie projektami i księgowanie | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Po zwalnianiu wstrzymanych oczekujących faktur potwierdzone koszty projektu stają się niepoprawne.                                                                             |
| Zarządzanie projektami i księgowanie | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Nie możesz utworzyć noty kredytowej dla zamówienia sprzedaży projektu, gdy podatek jest w innej walucie niż waluta firmy.                                      |
| Zarządzanie projektami i księgowanie | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Usunięcie kontraktu powoduje również usunięcie adresu skojarzonego z klientem.                                                                                     |
| Zarządzanie projektami i księgowanie | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Nie można księgować propozycji faktury wynikającej z ujemnej korekty transakcji czasowej.                                                                    |
| Podróże i wydatki                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Podatek jest obliczany w inny sposób w raportach wydatków.                                                                                                                  |
| Podróże i wydatki                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Aktualizacja wydania **DB72_Expense.updateTrvExpTransProjTransId()** nie zezwala elementowi **trvExpTrans.ReferenceDataAreaId** na tworzenie nowej sekwencji numerów.                    |
| Podróże i wydatki                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Wprowadzona kwota nie jest wyświetlana z polem obowiązkowym.                                                                                                             |
| Podróże i wydatki                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Ulepszenia w zakresie wydajności dołączania wydatku do raportu wydatków przy użyciu interfejsu użytkownika przeprojektowanych wydatków.                                                            |
| Podróże i wydatki                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Można usuwać zaksięgowane raporty wydatków.                                                                                           |
| Podróże i wydatki                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Komunikat dotyczący zasad wydatków jest wyświetlany wiele razy.                                                                                                       |
| Podróże i wydatki                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Pole **Metoda płatności** jest zawarte w okienku **Nowy wydatek**.                                                                                                      |
| Podróże i wydatki                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Jeśli stan przepływu pracy nie został znaleziony, narzędzie **Resetuj stan dokumentu wydatku** powinien zresetować stan raportu wydatków do stanu **Wersja robocza**. 

### <a name="regulatory-updates"></a>Aktualizacje dotyczące regulacji
Aby uzyskać więcej informacji na temat aktualizacji dotyczących aplikacji Finance and Operations, zobacz artykuł dotyczący [Aktualizacje dotyczące regulacji](/dynamics365/finance/localizations/regulatory-updates). Możesz również zalogować się w usługach Lifecycle Services (LCS) i wyświetlić planowane aktualizacje prawne, korzystając z narzędzia do wyszukiwania problemów. Funkcja wyszukiwanie problemów umożliwia wyszukiwanie według kraju, typu funkcji oraz wydania.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
