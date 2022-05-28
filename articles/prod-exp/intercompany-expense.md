---
title: Wydatki międzyfirmowe
description: Ten temat zawiera informacje o tym, jak używać wydatków międzyfirmowych do przypisywania wydatków pracownika do podmiotu prawnego, dla którego praca została wykonana.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684247"
---
# <a name="intercompany-expenses"></a>Wydatki międzyfirmowe

Pracownik zatrudniony przez jeden podmiot prawny w organizacji może wykonywać działania dla innego podmiotu prawnego w danej organizacji. Możesz użyć wydatków międzyfirmowych, aby przypisać wydatki pracownika do podmiotu prawnego, dla którego praca została wykonana. Podmiot prawny, który jest zatrudniony przez pracownika, jest nazywany firmą wypożyczającą. Podmiot prawny, na rzecz którego pracownik ponosi koszty, nosi nazwę podmiotu pożyczającego. 

Zanim pracownik będzie mógł tworzyć i przesyłać wydatki międzyfirmowe, należy włączyć międzyfirmowe linie wydatków. W encji prawnej, na stronie **Parametry zarządzania wydatkami** wybierz opcję **Zezwalaj na międzyfirmowe wiersze wydatków**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Księgowanie podatku na potrzeby kosztów międzyfirmowych

[!include [banner](../includes/banner.md)]

Zanim będzie można użyć grup podatków, które są skojarzone z firmą wypożyczającą (źródłową) zamiast firmy pożyczającej (docelowej) w raporcie z wydatków, należy włączyć tę funkcję w konfiguracji podatku od sprzedaży księgi głównej. Gdy parametr **Firma dla księgowania podatku międzyfirmowego** jest ustawiony na **Źródło**, a **Reguły opodatkowania podatku** są ustawione na **Nie**, używana jest kombinacja podatków dla firmy wypożyczającej. Jeśli ten sam parametr ma ustawioną wartość **Docelowy**, będzie używana kombinacja podatku dla podmiotu prawnego wypożyczającego. W przypadku podmiotów prawnych w Stanach Zjednoczonych, gdy parametr jest ustawiony na wartość **Źródło**, to w polu **Należny podatek od sprzedaży** musi być skonfigurowana nowa strona **Grup księgowania w rejestrze**. Silnik do księgowania użyje informacji z tego pola do prowadzania rachunków związanych z podatkami.   
Zachowanie to jest spójne w przypadku wierszy wydatków zaksięgowanych z użyciem projektu lub bez niego.  

## <a name="new-expense-expression-builder"></a>Nowy konstruktor wyrażenia wydatków

Nowy Konstruktor wyrażeń wydatków rozwiązuje problemy ze scenariuszami wydatków międzyfirmowych, które korzystają z projektów. Ta funkcja zapewnia, że podczas tworzenia wydatku międzyfirmowego zasady wydatków są prawidłowo sprawdzane względem projektu wybranego w wierszu wydatków, a raport z wydatków może zostać pomyślnie przesłany.

Aby funkcja konstruktora wyrażeń wydatków działała, musi być włączona. Ponadto należy skonfigurować politykę wydatków, która ma identyfikator projektu.

Jeśli masz już skonfigurowane zasady, które weryfikują identyfikator projektu w wierszu wydatków, te zasady muszą zostać wycofane. Następnie możesz włączyć tę funkcję i ponownie skonfigurować zasady.

Aby włączyć tę funkcję, wykonaj następujące kroki.

1. Wybierz kolejno pozycje **Obszary robocze** \> **Zarządzanie funkcjami**.
2. Na liście wybierz **Nowy konstruktor wyrażeń wydatków, aby rozwiązać problemy ze scenariuszami wydatków międzyfirmowych, które korzystają z projektów**. Następnie wybierz opcję **Włącz teraz**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
