---
title: Wydatki międzyfirmowe
description: Ten temat zawiera informacje o tym, jak używać wydatków międzyfirmowych do przypisywania wydatków pracownika do podmiotu prawnego, dla którego praca została wykonana.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271546"
---
# <a name="intercompany-expenses"></a>Wydatki międzyfirmowe

Pracownik zatrudniony przez jeden podmiot prawny w organizacji może wykonywać działania dla innego podmiotu prawnego w danej organizacji. Możesz użyć wydatków międzyfirmowych, aby przypisać wydatki pracownika do podmiotu prawnego, dla którego praca została wykonana. Podmiot prawny, który jest zatrudniony przez pracownika, jest nazywany firmą wypożyczającą. Podmiot prawny, na rzecz którego pracownik ponosi koszty, nosi nazwę podmiotu pożyczającego. 

Zanim pracownik będzie mógł tworzyć i przesyłać wydatki międzyfirmowe, należy włączyć międzyfirmowe linie wydatków. W encji prawnej, na stronie **Parametry zarządzania wydatkami** wybierz opcję **Zezwalaj na międzyfirmowe wiersze wydatków**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Księgowanie podatku na potrzeby kosztów międzyfirmowych

[!include [banner](../includes/banner.md)]

Zanim będzie można użyć grup podatków, które są skojarzone z firmą wypożyczającą (źródłową) zamiast firmy pożyczającej (docelowej) w raporcie z wydatków, należy włączyć tę funkcję w konfiguracji podatku od sprzedaży księgi głównej. Gdy parametr **Firma dla księgowania podatku międzyfirmowego** jest ustawiony na **Źródło**, a **Reguły opodatkowania podatku** są ustawione na **Nie**, używana jest kombinacja podatków dla firmy wypożyczającej. Jeśli ten sam parametr ma ustawioną wartość **Docelowy**, będzie używana kombinacja podatku dla podmiotu prawnego wypożyczającego. W przypadku podmiotów prawnych w Stanach Zjednoczonych, gdy parametr jest ustawiony na wartość **Źródło**, to w polu **Należny podatek od sprzedaży** musi być skonfigurowana nowa strona **Grup księgowania w rejestrze**. Silnik do księgowania użyje informacji z tego pola do prowadzania rachunków związanych z podatkami.   
Zachowanie to jest spójne w przypadku wierszy wydatków zaksięgowanych z użyciem projektu lub bez niego.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]