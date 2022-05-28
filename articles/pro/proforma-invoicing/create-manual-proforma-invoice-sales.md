---
title: Faktury proforma projektu
description: Ten temat zawiera informacje na temat faktur proforma projektu w Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f2ce672a412f7ad73b072854590cd423a3499fc1
ms.sourcegitcommit: 650a84add65588defdd2ac2c4524806baab070e0
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2022
ms.locfileid: "8628867"
---
# <a name="proforma-project-invoices"></a>Faktury proforma projektu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Fakturowanie Proforma projektu daje kierownikom projektów drugi poziom zatwierdzenia przed utworzeniem faktur dla klientów. Pierwszy poziom zatwierdzania jest zakończony po zatwierdzeniu czasu, wydatków i pozycji materiałowych przesłanych przez członków zespołu projektowego.

Dynamics 365 Project Operations we wdrożeniu uproszczonym nie jest przeznaczone do generowania faktur przeznaczonych dla klienta. Poniższa lista pokazuje, dlaczego nie można wygenerować faktur:

- Nie zawiera informacji o podatkach.
- Nie można przekonwertować innych walut na walutę fakturowania.
- Nie można poprawnie sformatować faktur do drukowania.

Zamiast tego można użyć systemu finansowego lub księgowego do tworzenia faktur dla klientów, które wykorzystują informacje z wygenerowanych propozycji faktur.

## <a name="creating-project-invoices"></a>Tworzenie faktur projektów

Faktury projektów można tworzyć pojedynczo lub zbiorczo. Użytkownik może utworzyć je ręcznie lub skonfigurować je w taki sposób, aby były generowane w zautomatyzowanym działaniu.

### <a name="manually-create-project-invoices"></a>Ręczne tworzenie faktur projektów 

Na stronie listy **kontrakty projektu** można tworzyć faktury projektu oddzielnie dla każdego kontraktu dotyczącego projektu albo można tworzyć faktury zbiorczo dla wielu kontraktów projektów.

   - Aby utworzyć fakturę dla określonej umowy dotyczącej projektu, na stronie listy **Umowy dotyczące projektu** otwórz umowę dotyczącą projektu, a następnie wybierz opcję **Utwórz fakturę**.

   Faktura jest generowana dla wszystkich transakcji w ramach wybranego kontraktu dotyczącego projektu mających status **gotowe do zafakturowania**. Transakcje te obejmują czas, wydatki, materiały, kamienie milowe, wiersze kontraktu oparte na produktach i inne niezafakturowane wiersze arkusza sprzedaży, które mogły zostać potwierdzone.

Aby zbiorczo tworzyć faktury:

1. Na stronie listy **kontrakty projektów** wybierz co najmniej jeden kontrakt projektu, dla którego chcesz utworzyć fakturę, a następnie wybierz pozycję **Utwórz faktury projektu**.
2. Komunikat ostrzegawczy informuje, że podczas tworzenia faktur może nastąpić opóźnienie. Proces również jest widoczny. Wybierz **OK**, aby zamknąć okno komunikatu.

   Faktura jest generowana dla wszystkich transakcji w ramach pozycji kontraktu mających status **gotowe do zafakturowania**. Transakcje te obejmują czas, wydatki, materiały, kamienie milowe, wiersze kontraktu oparte na produktach i inne niezafakturowane wiersze arkusza sprzedaży, które mogły zostać potwierdzone.

3. Aby wyświetlić wygenerowane faktury, należy przejść do obszaru **Sprzedaż** \> **Rozliczenia** \> **Faktury**. Zobaczysz jedną fakturę dla każdego kontraktu projektu.

### <a name="set-up-automated-creation-of-project-invoices"></a>Konfigurowanie zautomatyzowanego tworzenia faktur projektu 

Wykonaj te kroki, aby skonfigurować zautomatyzowany przebieg fakturowania.

1. Przejdź do **Ustawienia** \> **Zadania wsadowe**.
2. Utwórz zadanie przetwarzania wsadowego i nazwij je **Tworzenie faktur w Project Operations**. Nazwa zadania wsadowego musi zawierać termin "Tworzenie faktur".
3. W polu **typ zadania** wybierz **Brak**. Domyślnie opcje **Częstotliwość dzienna** i **Jest aktywne** są ustawione na **Tak.**
4. Wybierz **Uruchom przepływ pracy**. W oknie dialogowym **wyszukiwania rekordu** zostaną wyświetlone następujące przepływy pracy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wybierz **ProcessRunCaller**, a następnie wybierz opcję **Dodaj**.
6. W następnym oknie dialogowym wybierz **OK**. Po wykonaniu przepływu pracy **Uśpienie** następuje przepływ pracy **Proces**.

    Możesz również wybrać opcję **ProcessRunner** w kroku 5. Następnie po wybraniu opcji **OK** przepływ pracy **Proces** jest zastępowany przepływem pracy **Uśpienie**.

Przepływy pracy **ProcessRunCaller** i **ProcessRunner** tworzą faktury. **ProcessRunCaller** wywołuje **ProcessRunner**. **ProcessRunner** to przepływ pracy, który tworzy faktury. Ten przepływ pracy przechodzi przez wszystkie wiersze umowy, dla których muszą zostać utworzone faktury, i tworzy faktury. Aby określić wiersze kontraktu, dla których należy utworzyć faktury, przepływ pracy sprawdza daty uruchomienia faktur dla wierszy kontraktu. Jeśli pozycje kontraktu należące do jednego kontraktu mają taką samą datę rozpoczęcia fakturowania, transakcje zostaną połączone na jedną fakturę zawierającą dwa wiersze faktury. Jeśli nie ma transakcji, dla których można utworzyć faktury, nie są tworzone żadne faktury.

Kiedy **ProcessRunner** zakończy działanie, wywołuje **ProcessRunCaller**, dostarcza godzinę zakończenia i następuje zamknięcie. **ProcessRunCaller** następnie uruchamia zegar, który trwa 24 godziny od określonego czasu końcowego. Po upływie tego czasu program **ProcessRunCaller** jest zamknięty.

Zadanie przetwarzania wsadowego umożliwiającego tworzenie faktur jest zadaniem powtarzanym. Jeśli ten proces wsadowy jest wykonywany wiele razy, system tworzy wiele wystąpień zadania i może powodować to wystąpienie błędów. Aby obejść ten problem, uruchom proces wsadowy tylko raz i uruchom go ponownie tylko wtedy, gdy przestanie działać.

> [!NOTE]
> Fakturowanie wsadowe jest wykonywane tylko dla wierszy kontraktu projektu, które są konfigurowane przez harmonogramy faktur. Pozycja kontraktu z metodą fakturowania przy stałej cenie musi mieć skonfigurowany punkt kontrolny. Pozycja kontraktu projektu z metodą rozliczania czasu i materiału będzie wymagała konfiguracji harmonogramu fakturowania opartego na datach. To samo dotyczy pozycji kontraktu opartej na projektach.      
 
### <a name="edit-a-draft-invoice"></a>Edytuj fakturę roboczą

Podczas tworzenia wersji roboczej faktury projektu wszystkie niezafakturowane transakcje sprzedaży utworzone podczas zatwierdzania wpisów czasu i wydatku są pobierane na fakturę. W czasie, gdy faktura będzie wciąż w etapie roboczym, można wprowadzać następujące zmiany:

- Usuń lub Edytuj szczegóły wiersza faktury.
- Edytowanie i korygowanie ilości oraz typu fakturowania.
- Dodaj bezpośrednio czas, wydatki, materiały i opłaty jako transakcje na fakturze. Z tej funkcji można skorzystać, jeśli wiersz faktury jest mapowany na pozycję kontraktu, która umożliwia korzystanie z tych klas transakcji.

Kliknij przycisk **Potwierdź**, aby potwierdzić fakturę. Akcja jest akcją jednokierunkową. Po wybraniu opcji **Potwierdź** faktura zapisana jest jako tylko do odczytu i tworzy wartości rzeczywiste dotyczące sprzedaży z poszczególnych wierszy faktury dla każdego wiersza faktury. Jeśli szczegóły wiersza faktury odwołują się do faktycznej sprzedaży niezafakturowanej, rzeczywista sprzedaż niezafakturowana jest wycofywana. Wszelkie szczegóły wiersza faktury, które zostały utworzone na podstawie wpisu czasu, wydatków lub zużycia materiałów, będą odnosić się do faktycznej sprzedaży niezafakturowanej. Systemy integracji księgi głównej mogą używać tego odwrócenia w celu wycofania pracy w toku (WIP) projektu do celów księgowych.

### <a name="correct-a-confirmed-invoice"></a>Korygowanie potwierdzonej faktury

Potwierdzone faktury w PSA można korygować. W przypadku skorygowania potwierdzonej faktury jest tworzona nowa faktura poprawna. Ponieważ założono, że mają zostać wyzerowane wszystkie transakcje i ilości z oryginalnej faktury, ta faktura korygująca zawiera wszystkie transakcje z oryginalnej faktury, a wszystkie jej ilości są równe zero.

Jeśli są transakcje, które nie wymagają korekty, możesz je usunąć z projektu faktury korygującej. Aby odwrócić lub dokonać zwrotu tylko ilości częściowej, można edytować pole **ilość** w szczegółach wiersza. Po otwarciu szczegółów wiersza faktury jest wyświetlana oryginalna ilość faktury. Następnie można edytować bieżącą ilość na fakturze, tak aby była mniejsza lub większa niż oryginalna ilość na fakturze.

Po potwierdzeniu faktury korygującej oryginalna rozliczona wartość rzeczywista sprzedaży jest cofana i system tworzy nową wartość rzeczywistą rozliczonej sprzedaży. Jeśli ilość została zmniejszona, różnica spowoduje utworzenie nowej nierozliczonej wartości rzeczywistej sprzedaży. Jeśli na przykład oryginalna rozliczona sprzedaż trwała 8 godzin, a wiersz faktury korygującej ograniczył ilość do sześciu godzin, oryginalny wiersz wyliczonych transakcji jest wycofany i utworzone są dwie nowe wartości rzeczywiste:

- Rozliczona wartość rzeczywista za sześć godzin.
- Nierozliczona sprzedaż za pozostałe dwie godziny. Ta transakcja może być rozliczona później lub oznakowana jako niepłatna, w zależności od ustaleń z klientem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
