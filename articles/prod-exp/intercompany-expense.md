---
title: Wydatki międzyfirmowe
description: Pracownik zatrudniony przez jeden podmiot prawny w organizacji może wykonywać działania dla innego podmiotu prawnego w danej organizacji. W takiej sytuacji można skorzystać z funkcji wydatek międzyfirmowy, aby przypisać koszty pracownika firmie, dla której rzeczywiście wykonano pracę.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082163"
---
# <a name="intercompany-expenses"></a>Wydatki międzyfirmowe

[!include [banner](../includes/banner.md)]

Pracownik zatrudniony przez jeden podmiot prawny w organizacji może wykonywać działania dla innego podmiotu prawnego w danej organizacji. W takiej sytuacji można skorzystać z funkcji wydatek międzyfirmowy, aby przypisać koszty pracownika firmie, dla której rzeczywiście wykonano pracę. Podmiot prawny, który jest zatrudniony przez pracownika, jest nazywany firmą wypożyczającą. Podmiot prawny, na rzecz którego pracownik ponosi koszty, nosi nazwę podmiotu pożyczającego. 

Aby pracownik mógł tworzyć i składać wydatki dotyczące pracy wykonywanej w odniesieniu do innej osoby prawnej, na stronie **Parametry zarządzania wydatkami** w firmie wypożyczającej wybierz opcję **Zezwalaj na wiersze kosztów międzyfirmowych**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Księgowanie podatku na potrzeby kosztów międzyfirmowych

[!include [banner](../includes/banner.md)]

Aby użyć grup podatku skojarzonych z wypożyczającym (źródłowym) podmiotem, zamiast podmiotu pożyczającego (docelowego) w raporcie z wydatków należy skonfigurować odpowiednią opcję w konfiguracji podatku na potrzeby księgi głównej. Kiedy parametr księgi głównej **Podmiot prawny na potrzeby międzyfirmowego księgowania podatkowego** jest ustawiony na wartość **Źródło** i wartość **Zastosuj reguły opodatkowania** ustawiona jest na **Nie** , stosowana będzie kombinacja podatku z wypożyczającego podmiotu prawnego. Jeśli ten sam parametr ma ustawioną wartość **Docelowy** , będzie używana kombinacja podatku dla podmiotu prawnego wypożyczającego. W przypadku podmiotów prawnych w Stanach Zjednoczonych, gdy parametr jest ustawiony na wartość **Źródło** , to w polu **Należny podatek od sprzedaży** musi być skonfigurowana nowa strona **Grup księgowania w rejestrze**. Silnik do księgowania użyje informacji z tego pola do prowadzania rachunków związanych z podatkami.   
Zachowanie to jest spójne w przypadku wierszy wydatków zaksięgowanych z użyciem projektu lub bez niego.  
