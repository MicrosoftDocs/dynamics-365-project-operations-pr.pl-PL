---
title: Konfiguracja kategorii wydatków
description: Ten temat zawiera informacje na temat konfigurowania kategorii wydatków i udostępnionych kategorii raportów z wydatków.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896699"
---
# <a name="set-up-expense-categories"></a>Konfiguracja kategorii wydatków

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Kiedy pracownicy tworzą raporty o wydatkach, każdy z tych rekordów musi być skojarzony z kategorią wydatku. Kategorie wydatków są pobierane z kategorii udostępnionych, które mogą być współużytkowane przez osoby prawne należące do organizacji. W zależności od sposobu definiowania organizacji te kategorie kosztów mogą być również udostępniane w innych obszarach. W zależności od definicji organizacji i wskazówek dotyczących zespołu implementacji należy określić, czy kategorie używane w zarządzaniu wydatkami będą używane tylko w zarządzaniu wydatkami, czy powinny być wspólne dla innych obszarów.

> [!NOTE]
> Kategorie te mogą być współużytkowane przez zarządzanie projektami oraz zarządzanie wydatkami i kosztami, a także między zarządzaniem projektami oraz ich księgowaniem i produkcją. Nie można ich jednak udostępniać pomiędzy zarządzaniem wydatkami i produkcją.

Przed rozpoczęciem procesu instalacji należy wykonać następujące decyzje dotyczące każdej kategorii wydatków:

- Jaka jest kategoria wydatków? Mogą to być np. kategorie dla lotów, hotelu lub trasy.
- Czy kategoria wydatków może być używana także w zarządzaniu projektami i księgowaniu? Jeśli tak, to należy także podjąć następujące decyzje:

    - Które konta kosztów będą używane w następujących wydatkach?

        - Koszt
        - Alokacja płac
        - PWT-koszt wartość
        - Koszt przedmiotu
        - PWT-koszt wartość-przedmiotu
        - Naliczona strata
        - PWT-naliczona strata

    - Które konta przychodu będą używane dla następujących źródeł przychodów?

        - Zafakturowany przychód
        - Naliczony przychód — wartość sprzedaży
        - PWT — wartość sprzedaży
        - Naliczony przychód — produkcja
        - PWT-produkcja
        - Naliczony przychód — zysk
        - PWT-zysk
        - Naliczony przychód — subskrypcja
        - PWT-subskrypcja

- Jaki jest typ wydatków?
- Jaka jest domyślna metoda płatności dla tej kategorii wydatków?
- Czy wydatki w tej kategorii muszą zostać wyszczególnione?
- Jaka jest główne domyślne konto dla tej kategorii wydatków?
- Jaka jest domyślna grupa podatków od sprzedaży w danej kategorii wydatku?
- Czy dla kategorii wydatków są dozwolone dodatkowe formy płatności? Jeśli tak, to jakie?
- Czy w tej kategorii wydatków znajdują się podkategorie? Jeśli tak, to należy także podjąć następujące decyzje:

    - Czy któraś z podkategorii jest wykluczona ze zwrotu podatku?
    - Jaka jest grupa podatku od sprzedaży w tych podkategoriach?
