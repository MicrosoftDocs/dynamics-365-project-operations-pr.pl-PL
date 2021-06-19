---
title: Konfigurowanie automatycznego tworzenia faktury
description: W tym temacie zamieszczono informacje na temat pracy z systemem na żywo w celu automatycznego generowania faktur.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005354"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurowanie automatycznego tworzenia faktury

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


Wykonaj następujące kroki, aby skonfigurować zautomatyzowany przebieg fakturowania w Dynamics 365 Project Operations.

1. Przejdź do **Ustawienia** > **Zadania wsadowe**.
2. Utwórz zadanie przetwarzania wsadowego i nazwij je **Tworzenie faktur w Project Operations**. Nazwa zadania wsadowego musi zawierać słowa „Tworzenie faktur”.
3. W polu **Typ zadania** wybierz **Brak**. Domyślnie opcje **Częstotliwość dzienna** i **Jest aktywne** są ustawione na **Tak.**
4. Wybierz **Uruchom przepływ pracy**. W oknie dialogowym **wyszukiwania rekordu** zostaną wyświetlone trzy przepływy pracy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wybierz **ProcessRunCaller**, a następnie wybierz opcję **Dodaj**.
6. W następnym oknie dialogowym wybierz **OK**. Po wykonaniu przepływu pracy **Uśpienie** następuje przepływ pracy **Proces**.

  > [!NOTE]
  > Możesz również wybrać opcję **ProcessRunner** w kroku 5. Następnie po wybraniu opcji **OK** przepływ pracy **Proces** jest zastępowany przepływem pracy **Uśpienie**.

Przepływy pracy **ProcessRunCaller** i **ProcessRunner** tworzą faktury. **ProcessRunCaller** wywołuje **ProcessRunner**. **ProcessRunner** to przepływ pracy, który w rzeczywistości tworzy faktury. Przechodzi między wszystkimi pozycjami kontraktu, dla których muszą zostać utworzone faktury i tworzy faktury dla tych pozycji. W celu określenia pozycji kontraktu, dla których mają zostać utworzone faktury, zadanie będzie znajdzie daty rozpoczęcia fakturowania w pozycjach kontraktu. Jeśli pozycje kontraktu należące do jednego kontraktu mają taką samą datę rozpoczęcia fakturowania, transakcje zostaną połączone na jedną fakturę zawierającą dwa wiersze faktury. W przypadku braku transakcji do utworzenia faktur dla zadania program pominie tworzenie faktur.

Kiedy **ProcessRunner** zakończy działanie, wywołuje **ProcessRunCaller**, dostarcza godzinę zakończenia i następuje zamknięcie. **ProcessRunCaller** następnie uruchamia zegar, który trwa 24 godziny od określonego czasu końcowego. Po upływie tego czasu program **ProcessRunCaller** jest zamknięty.

Zadanie przetwarzania wsadowego umożliwiającego tworzenie faktur jest zadaniem powtarzanym. Jeśli ten proces wsadowy jest wykonywany wiele razy, system tworzy wiele wystąpień zadania i powoduje to wystąpienie błędów. Z tego powodu proces przetwarzania wsadowego powinien być uruchamiany tylko raz. Aby uruchomić go tylko wtedy, gdy zakończy się jego działanie.

> [!NOTE]
> Fakturowanie wsadowe jest wykonywane tylko dla wierszy kontraktu projektu, które są konfigurowane przez harmonogramy faktur. Pozycja kontraktu z metodą fakturowania przy stałej cenie musi mieć skonfigurowany punkt kontrolny. Pozycja kontraktu projektu z metodą rozliczania czasu i materiału będzie wymagała konfiguracji harmonogramu fakturowania opartego na datach. To samo dotyczy pozycji kontraktu opartej na projektach.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]