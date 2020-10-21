---
title: Konfigurowanie zautomatyzowanego tworzenia faktury
description: W tym temat zamieszczono informacje na temat pracy z systemem na żywo w celu automatycznego generowania faktur.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898139"
---
# <a name="configure-automated-invoice-creation"></a>Konfigurowanie zautomatyzowanego tworzenia faktury

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Wykonaj następujące kroki, aby skonfigurować zautomatyzowany przebieg fakturowania w Project Operations.

1. Przejdź do **Ustawienia** \> **Zadania wsadowe**.
2. Utwórz zadanie przetwarzania wsadowego i nazwij je **Tworzenie faktur w Project Operations**. Nazwa zadania wsadowego musi zawierać termin „Tworzenie faktur”.
3. W polu **typ zadania** wybierz **Brak**. Domyślnie opcje **Częstotliwość dzienna** i **Jest aktywne** są ustawione na **Tak.**
4. Wybierz **Uruchom przepływ pracy**. W oknie dialogowym **wyszukiwania rekordu** zostaną wyświetlone trzy przepływy pracy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wybierz **ProcessRunCaller**, a następnie wybierz opcję **Dodaj**.
6. W następnym oknie dialogowym wybierz **OK**. Po wykonaniu przepływu pracy **Uśpienie** następuje przepływ pracy **Proces**.

    Możesz również wybrać opcję **ProcessRunner** w kroku 5. Następnie po wybraniu opcji **OK**przepływ pracy **Proces** jest zastępowany przepływem pracy **Uśpienie**.

Przepływy pracy **ProcessRunCaller** i **ProcessRunner** tworzą faktury. **ProcessRunCaller** wywołuje **ProcessRunner**. **ProcessRunner** to przepływ pracy, który w rzeczywistości tworzy faktury. Przechodzi między wszystkimi pozycjami kontraktu, dla których muszą zostać utworzone faktury i tworzy faktury dla tych pozycji. W celu określenia pozycji kontraktu, dla których mają zostać utworzone faktury, zadanie będzie znajdzie daty rozpoczęcia fakturowania w pozycjach kontraktu. Jeśli pozycje kontraktu należące do jednego kontraktu mają taką samą datę rozpoczęcia fakturowania, transakcje zostaną połączone na jedną fakturę zawierającą dwa wiersze faktury. W przypadku braku transakcji do utworzenia faktur dla zadania program pominie tworzenie faktur.

Kiedy **ProcessRunner** zakończy działanie, wywołuje **ProcessRunCaller**, dostarcza godzinę zakończenia i następuje zamknięcie. **ProcessRunCaller** następnie uruchamia zegar, który trwa 24 godziny od określonego czasu końcowego. Po upływie tego czasu program **ProcessRunCaller** jest zamknięty.

Zadanie przetwarzania wsadowego umożliwiającego tworzenie faktur jest zadaniem powtarzanym. Jeśli ten proces wsadowy jest wykonywany wiele razy, system tworzy wiele wystąpień zadania i powoduje to wystąpienie błędów. Z tego powodu proces przetwarzania wsadowego powinien być uruchamiany tylko raz. Aby uruchomić go tylko wtedy, gdy zakończy się jego działanie.

> [!NOTE]
> Fakturowanie wsadowe jest wykonywane tylko dla wierszy kontraktu projektu, które są konfigurowane przez harmonogramy faktur. Pozycja kontraktu z metodą fakturowania przy stałej cenie musi mieć skonfigurowany punkt kontrolny. Pozycja kontraktu projektu z metodą rozliczania czasu i materiału będzie wymagała konfiguracji harmonogramu fakturowania opartego na datach. To samo dotyczy pozycji kontraktu opartej na projektach.     
