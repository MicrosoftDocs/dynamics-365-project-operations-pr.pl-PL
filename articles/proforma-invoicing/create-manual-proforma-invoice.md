---
title: Tworzenie ręcznej faktury proforma
description: Ta temat zawiera informacje na temat tworzenia faktury proforma.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d3c84664f1b0701db17f0c05654e0c99bb6c640
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128071"
---
# <a name="create-a-manual-proforma-invoice"></a>Tworzenie ręcznej faktury proforma

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Fakturowanie zapewnia menedżerom projektów drugi poziom zatwierdzania przed utworzeniem faktur dla klientów. Pierwszy poziom zatwierdzania jest wykonywany, gdy wpisy czasu i wydatku przesłane przez członków zespołu projektu zostaną zatwierdzone.

Dynamics 365 Project Operations nie służy do generowania faktur dostępnych dla klienta, z następujących powodów:

- Nie zawiera informacji o podatkach.
- Nie może dokonać konwersji innych walut na walutę fakturowania przy użyciu poprawnie skonfigurowanych kursów wymiany.
- Nie może poprawnie formatować faktur, aby mogły zostać wydrukowane.

Zamiast tego system finansowy lub księgowy może służyć do tworzenia faktur dostępnych dla klienta, które korzystają z informacji zawartych w propozycjach wygenerowanych faktur.

## <a name="creating-project-invoices"></a>Tworzenie faktur projektów

Faktury projektów można tworzyć pojedynczo lub zbiorczo. Użytkownik może utworzyć je ręcznie lub skonfigurować je w taki sposób, aby były generowane w zautomatyzowanym działaniu.

### <a name="manually-create-project-invoices"></a>Ręczne tworzenie faktur projektów 

Na stronie listy **kontrakty projektu** można tworzyć faktury projektu oddzielnie dla każdego kontraktu dotyczącego projektu albo można tworzyć faktury zbiorczo dla wielu kontraktów projektów.

Wykonaj ten krok, aby utworzyć fakturę dla konkretnego kontraktu dotyczącego projektu.

- Na stronie listy **kontrakty projektów** otwórz kontrakt projektu, a następnie wybierz pozycję **Utwórz fakturę**.

    Faktura jest generowana dla wszystkich transakcji w ramach wybranego kontraktu dotyczącego projektu mających status **gotowe do zafakturowania**. Do tych transakcji należą między innymi pozycje czas, wydatki, punkty kontrolne i wiersze kontraktu opartego na produktach.

Wykonaj te kroki, aby utworzyć zbiorczo faktury.

1. Na stronie listy **kontrakty projektów** wybierz co najmniej jeden kontrakt projektu, dla którego chcesz utworzyć fakturę, a następnie wybierz pozycję **Utwórz faktury projektu**.

    Komunikat ostrzegawczy informuje, że podczas tworzenia faktur może nastąpić opóźnienie. Proces również jest widoczny.

2. Wybierz **OK**, aby zamknąć okno komunikatu.

    Faktura jest generowana dla wszystkich transakcji w ramach pozycji kontraktu mających status **gotowe do zafakturowania**. Do tych transakcji należą między innymi pozycje czas, wydatki, punkty kontrolne i wiersze kontraktu opartego na produktach.

3. Aby wyświetlić wygenerowane faktury, należy przejść do obszaru **Sprzedaż** \> **Rozliczenia** \> **Faktury**. Zobaczysz jedną fakturę dla każdego kontraktu projektu.

### <a name="set-up-automated-creation-of-project-invoices"></a>Konfigurowanie zautomatyzowanego tworzenia faktur projektu 

Wykonaj te kroki, aby skonfigurować zautomatyzowany przebieg fakturowania.

1. Przejdź do **Ustawienia** \> **Zadania wsadowe**.
2. Utwórz zadanie przetwarzania wsadowego i nazwij je **Tworzenie faktur w Project Operations**. Nazwa zadania wsadowego musi zawierać termin "Tworzenie faktur".
3. W polu **typ zadania** wybierz **Brak**. Domyślnie opcje **Częstotliwość dzienna** i **Jest aktywne** są ustawione na **Tak.**
4. Wybierz **Uruchom przepływ pracy**. W oknie dialogowym **wyszukiwania rekordu** zostaną wyświetlone trzy przepływy pracy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wybierz **ProcessRunCaller**, a następnie wybierz opcję **Dodaj**.
6. W następnym oknie dialogowym wybierz **OK**. Po wykonaniu przepływu pracy **Uśpienie** następuje przepływ pracy **Proces**.

    Możesz również wybrać opcję **ProcessRunner** w kroku 5. Następnie po wybraniu opcji **OK** przepływ pracy **Proces** jest zastępowany przepływem pracy **Uśpienie**.

Przepływy pracy **ProcessRunCaller** i **ProcessRunner** tworzą faktury. **ProcessRunCaller** wywołuje **ProcessRunner**. **ProcessRunner** to przepływ pracy, który w rzeczywistości tworzy faktury. Przechodzi między wszystkimi pozycjami kontraktu, dla których muszą zostać utworzone faktury i tworzy faktury dla tych pozycji. W celu określenia pozycji kontraktu, dla których mają zostać utworzone faktury, zadanie będzie znajdzie daty rozpoczęcia fakturowania w pozycjach kontraktu. Jeśli pozycje kontraktu należące do jednego kontraktu mają taką samą datę rozpoczęcia fakturowania, transakcje zostaną połączone na jedną fakturę zawierającą dwa wiersze faktury. W przypadku braku transakcji do utworzenia faktur dla zadania program pominie tworzenie faktur.

Kiedy **ProcessRunner** zakończy działanie, wywołuje **ProcessRunCaller**, dostarcza godzinę zakończenia i następuje zamknięcie. **ProcessRunCaller** następnie uruchamia zegar, który trwa 24 godziny od określonego czasu końcowego. Po upływie tego czasu program **ProcessRunCaller** jest zamknięty.

Zadanie przetwarzania wsadowego umożliwiającego tworzenie faktur jest zadaniem powtarzanym. Jeśli ten proces wsadowy jest wykonywany wiele razy, system tworzy wiele wystąpień zadania i powoduje to wystąpienie błędów. Z tego powodu proces przetwarzania wsadowego powinien być uruchamiany tylko raz. Aby uruchomić go tylko wtedy, gdy zakończy się jego działanie.

> [!NOTE]
> Fakturowanie wsadowe jest wykonywane tylko dla wierszy kontraktu projektu, które są konfigurowane przez harmonogramy faktur. Pozycja kontraktu z metodą fakturowania przy stałej cenie musi mieć skonfigurowany punkt kontrolny. Pozycja kontraktu projektu z metodą rozliczania czasu i materiału będzie wymagała konfiguracji harmonogramu fakturowania opartego na datach. To samo dotyczy pozycji kontraktu opartej na projektach.      
 
### <a name="edit-a-draft-invoice"></a>Edytuj fakturę roboczą

Podczas tworzenia wersji roboczej faktury projektu wszystkie niezafakturowane transakcje sprzedaży utworzone podczas zatwierdzania wpisów czasu i wydatku są pobierane na fakturę. W czasie, gdy faktura będzie wciąż w etapie roboczym, można wprowadzać następujące zmiany:

- Usuń lub Edytuj szczegóły wiersza faktury.
- Edytowanie i korygowanie ilości oraz typu fakturowania.
- Bezpośrednie dodanie czasu, wydatku i opłaty jako transakcji na fakturze. Z tej funkcji można skorzystać, jeśli wiersz faktury jest mapowany na pozycję kontraktu, która umożliwia korzystanie z tych klas transakcji.

Kliknij przycisk **Potwierdź**, aby potwierdzić fakturę. Akcja Confirm jest akcją jednokierunkową. Po wybraniu opcji **Confirm** system dokona zapisze fakturę jako tylko do odczytu i tworzy wartości rzeczywiste dotyczące sprzedaży z poszczególnych wierszy faktury dla każdego wiersza faktury. Jeśli Szczegóły wiersza faktury odwołują się do wartości rzeczywistej niezafakturowanej sprzedaży, system cofnie również wartość rzeczywistą nienależną sprzedaż. (Wszystkie wiersze faktury utworzone z danego wpisu czasu lub wydatku będą dotyczyć niezafakturowanego poziomu sprzedaży). Systemy integracji księgi głównej umożliwiają wycofanie zmian w toku prac projektów (PWT) na potrzeby księgowania.

### <a name="correct-a-confirmed-invoice"></a>Korygowanie potwierdzonej faktury

Potwierdzone faktury można edytować (poprawiać). W przypadku skorygowania potwierdzonej faktury jest tworzona nowa faktura poprawna. Ponieważ założono, że mają zostać wyzerowane wszystkie transakcje i ilości z oryginalnej faktury, ta faktura korygująca zawiera wszystkie transakcje z oryginalnej faktury, a wszystkie jej ilości są równe 0 (zero).

Jeśli żadne transakcje nie wymagają korekty, można je usunąć z wersji roboczej faktury korygującej. Aby odwrócić lub dokonać zwrotu tylko ilości częściowej, można edytować pole **ilość** w szczegółach wiersza. Po otwarciu szczegółów wiersza faktury jest wyświetlana oryginalna ilość faktury. Następnie można edytować bieżącą ilość na fakturze, tak aby była mniejsza lub większa niż oryginalna ilość na fakturze.

Po potwierdzeniu faktury korygującej oryginalna rozliczona wartość rzeczywista sprzedaży jest cofana i system tworzy nową wartość rzeczywistą rozliczonej sprzedaży. Jeśli ilość została zmniejszona, różnica spowoduje utworzenie nowej nierozliczonej wartości rzeczywistej sprzedaży. Jeśli na przykład oryginalna rozliczona sprzedaż trwała 8 godzin, a wiersz faktury korygującej ograniczył ilość do sześciu godzin, oryginalny wiersz wyliczonych transakcji jest wycofany i utworzone są dwie nowe wartości rzeczywiste:

- Rozliczona wartość rzeczywista za sześć godzin.
- Nierozliczona sprzedaż za pozostałe dwie godziny. Ta transakcja może być rozliczona później lub oznakowana jako niepłatna, w zależności od ustaleń z klientem.
