---
title: Skonfiguruj automatyczne tworzenie faktur
description: Ten temat zawiera informacje o ustawianiu i konfigurowaniu automatycznego tworzenia faktur proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 027cc711d53c7dd8512e6ef416b54e320357dd26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584103"
---
# <a name="set-up-automatic-invoice-creation"></a>Skonfiguruj automatyczne tworzenie faktur 
 
_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_

Można skonfigurować automatyczne tworzenie faktury w rozwiązaniu Dynamics 365 Project Operations. System utworzy roboczą fakturę pro forma na podstawie harmonogramu fakturowania dla każdej umowy dotyczącej projektu i pozycji kontraktu. Harmonogramy faktur są konfigurowane na poziomie pozycji kontraktu. Każdy wiersz kontraktu może zawierać odrębny harmonogram fakturowania lub ten sam harmonogram fakturowania może być uwzględniany w każdym wierszu kontraktu.

Podczas tworzenia faktury system zawsze tworzy co najmniej jedną fakturę przypadającą na każdy kontrakt projektu. W niektórych przypadkach może być utworzonych wiele faktur. Jeśli na przykład kontrakt ma wielu klientów, zostanie utworzone tyle faktur, ilu klientów danego kontraktu projektu powinno być zafakturowanych w ramach rozliczanych transakcji.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Rozumienie sposobu uwzględniania transakcji na fakturze 

Czasami każdy wiersz kontraktu opartego na projektach określa osobny harmonogram faktur. Na przykład usługi implementacji dla kontraktu Adatum mają następujące pozycje kontraktu:

- Prototypowa praca zawierająca dwa ręcznie utworzone punkty kontrolne z ceną stałą.
- Praca wdrożeniowa obejmująca Czas będzie rozliczana co dwa tygodnie, w poniedziałek.
- Koszty poniesione, które muszą być rozliczane miesięcznie w pierwszy poniedziałek każdego miesiąca.

Harmonogramy faktur zdefiniowane dla każdego z tych dwóch wierszy wyglądają jak w poniższej tabeli.

| Pozycja kontraktu | Data przebiegu fakturowania | Ostateczny termin transakcji | Data punktu kontrolnego | Kwota punktu kontrolnego |
| --- | --- | --- | --- | --- |
| Praca w ramach prototypu | 5 października, poniedziałek | - | 5 października, poniedziałek | 5000 USD |
| - | 3 listopada, wtorek | - | 3 listopada, wtorek | 12,000 USD |
| Praca w ramach implementacji | 5 października, poniedziałek | 4 października, niedziela | - | - |
| - | 19 października, poniedziałek | 18 października, niedziela | - | - |
| - | 2 listopada, poniedziałek | 1 listopada, niedziela | - | - |
| - | 16 listopada, poniedziałek | 15 listopada, niedziela | - | - |
| Poniesione wydatki | 5 października, poniedziałek | 4 października, niedziela | - | - |
| - | 2 listopada, poniedziałek | 1 listopada, niedziela | - | - |

W tym przykładzie, gdy jest wykonywane automatyczne fakturowanie:

- **4 października lub dowolna wcześniejsza data**: dla niniejszego kontraktu nie jest generowana żadna faktura, ponieważ **Harmonogram fakturowania** dla każdej z tych pozycji kontraktu nie zawiera wartości niedziela, 4 października jako datę przebiegu faktury.
- **5 października, poniedziałek**: Jedna faktura jest generowana dla:

    - Prototypowej pracy obejmującej punkt kontrolny, jeśli jest on oznaczony jako **Gotowy do zafakturowania**.
    - Praca nad implementacją obejmująca wszystkie transakcje Czasu utworzone przed terminem końcowym w dniu 4 października, w niedzielę, które są oznaczone jako **Gotowe do zafakturowania**.
    - Poniesiony wydatek obejmujący wszystkie transakcje wydatków utworzone przed terminem końcowym w dniu 4 października, w niedzielę, które są oznaczone jako **Gotowe do zafakturowania**.
  
- **6 października lub dowolna wcześniejsza data przed 19 października**: dla niniejszego kontraktu nie jest generowana żadna faktura, ponieważ **Harmonogram fakturowania** dla każdej z tych pozycji kontraktu nie zawiera wartości 6 października lub daty przed 19 października jako daty przebiegu faktury.
- **19 października, poniedziałek**: Praca nad implementacją obejmująca wszystkie transakcje Czasu utworzone przed terminem końcowym w dniu 18 października, w niedzielę, które są oznaczone jako **Gotowe do zafakturowania**.
- **2 listopada, poniedziałek**: Jedna faktura jest generowana dla:

    - Praca nad implementacją obejmująca wszystkie transakcje Czasu utworzone przed terminem końcowym w dniu 1 listopada, w niedzielę, które są oznaczone jako **Gotowe do zafakturowania**.
    - Poniesiony wydatek obejmujący wszystkie transakcje wydatków utworzone przed terminem końcowym w dniu 1 listopada, w niedzielę, które są oznaczone jako **Gotowe do zafakturowania**.

- **3 listopada, wtorek**: jedna faktura jest generowana na potrzeby zadania prototypowego zawierającego punkt kontrolny 12 000 USD, jeśli jest on oznaczony jako **Gotowy do zafakturowania**.

## <a name="configure-automatic-invoicing"></a>Konfiguruj automatyczne fakturowanie

Wykonaj poniższe kroki, aby skonfigurować zautomatyzowany przebieg fakturowania.

1. W **Project Operations** wybierz kolejno **Ustawienia** > **Ustawienia faktur cyklicznych**.
2. Utwórz zadanie przetwarzania wsadowego i nazwij je **Tworzenie faktur w Project Operations**. Nazwa zadania wsadowego musi zawierać słowa „Tworzenie faktur”.
3. W polu **Typ zadania** wybierz **Brak**. Domyślnie pola **Częstotliwość dzienna** i **Jest aktywne** są ustawione na **Tak**.
4. Wybierz **Uruchom przepływ pracy**. W oknie dialogowym **wyszukiwania rekordu** zostaną wyświetlone trzy przepływy pracy:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Wybierz **ProcessRunCaller**, a następnie wybierz opcję **Dodaj**.
6. W następnym oknie dialogowym wybierz **OK**. Po wykonaniu przepływu pracy **Uśpienie** następuje przepływ pracy **Proces**. 

> [!NOTE]
> Możesz również wybrać opcję **ProcessRunner** w kroku 5. Następnie po wybraniu opcji **OK** przepływ pracy **Proces** jest zastępowany przepływem pracy **Uśpienie**.

Przepływy pracy **ProcessRunCaller** i **ProcessRunner** tworzą faktury. **ProcessRunCaller** wywołuje **ProcessRunner**. **ProcessRunner** to przepływ pracy, który w rzeczywistości tworzy faktury. Przepływ pracy przechodzi między wszystkimi pozycjami kontraktu, dla których muszą zostać utworzone faktury i tworzy faktury dla tych pozycji. W celu określenia pozycji kontraktu, dla których mają zostać utworzone faktury, zadanie będzie znajdzie daty rozpoczęcia fakturowania w pozycjach kontraktu. Jeśli pozycje kontraktu należące do jednego kontraktu mają taką samą datę rozpoczęcia fakturowania, transakcje zostaną połączone na jedną fakturę zawierającą dwa wiersze faktury. W przypadku braku transakcji do utworzenia faktur dla zadania program pominie tworzenie faktury.

Kiedy **ProcessRunner** zakończy działanie, wywołuje **ProcessRunCaller**, dostarcza godzinę zakończenia i następuje zamknięcie. **ProcessRunCaller** następnie uruchamia zegar, który trwa 24 godziny od określonego czasu końcowego. Po upływie tego czasu program **ProcessRunCaller** jest zamknięty.

Zadanie przetwarzania wsadowego umożliwiającego tworzenie faktur jest zadaniem powtarzanym. Jeśli ten proces wsadowy jest wykonywany wiele razy, system tworzy wiele wystąpień zadania i powoduje to wystąpienie błędów. Z tego powodu proces przetwarzania wsadowego powinien być uruchamiany i zrestartowany tylko raz, gdy zakończy się jego działanie.

> [!NOTE]
> Fakturowanie wsadowe w Project Operations jest wykonywane tylko dla wierszy kontraktu projektu, które są konfigurowane przez harmonogramy faktur. Pozycja kontraktu z metodą fakturowania przy stałej cenie musi mieć skonfigurowany punkt kontrolny. Pozycja kontraktu projektu z metodą rozliczania czasu i materiału będzie wymagała konfiguracji harmonogramu fakturowania opartego na datach.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
