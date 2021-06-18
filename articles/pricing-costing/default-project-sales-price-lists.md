---
title: Cenniki domyślne
description: Ten temat zawiera informacje na temat domyślnych cenników sprzedaży i kosztów w Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c204a8f0364a4be39974b101e834d4465b99f769
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000494"
---
# <a name="default-price-lists"></a>Cenniki domyślne

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

## <a name="sales-price-lists"></a>Cenniki sprzedaży

Każda oferta projektu i umowa w rozwiązaniu Dynamics 365 Project Operations zawiera domyślny cennik sprzedaży. 

### <a name="price-list-default-on-project-quotes"></a>Domyślny cennik dla ofert projektu
System ukończy następujący proces w celu określenia, które cenniki są obowiązujące w ofercie:

1. System wyszukuje cenniki dołączone do cenników danego konta. 
2. Jeśli do rekordu klienta są dołączone cenniki projektu, system wyszukuje w zestawie ceny sprzedaży dołączone do parametrów projektu pasujących do waluty oferty projektu.
3. Następnie system sprawdza datę wejścia w życie cenników odpowiadającą zakresowi dat oferty projektu. Sprawdza datę utworzenia oferty.
4. Jeśli istnieje wiele cenników, które są wiążące dla oferty projektu, wszystkie cenniki dla oferty projektu są domyślne.
5. Jeśli brak obowiązujących cenników w ofercie projektu, nie ma żadnych domyślnych cenników projektu dla oferty. W ofercie projektu zostanie wyświetlone ostrzeżenie. Wiadomość ta zawiera informację, że z powodu braku dołączonych cenników projektu, szacunkowa i rzeczywista praca nad projektem i koszty nie będą wyceniane.

### <a name="price-list-default-on-project-contracts"></a>Domyślny cennik dla kontraktów projektu 
System ukończy następujący proces w celu określenia, które cenniki są obowiązujące w kontrakcie:

1. Jeśli z poziomu oferty utworzono kontrakt, cenniki projektu dotyczące oferty są kopiowane oddzielnie i załączane do kontraktu projektu.
2. Jeżeli kontrakt jest tworzony od podstaw, system wyszukuje cenniki dołączone do cenników projektu klienta na koncie. Jeśli do rekordu konta nie są dołączone cenniki projektu, system wyszukuje cenników sprzedaży dołączonych do parametrów projektu, które pasują do waluty kontraktu projektu.
4. Następnie system sprawdza datę wejścia w życie cenników odpowiadającą zakresowi dat kontraktu projektu. Sprawdza datę utworzenia kontraktu.
5. Jeśli istnieje wiele cenników, które są wiążące dla kontraktu, wszystkie cenniki dla kontraktu są domyślne.
6. Jeśli brak obowiązujących cenników dla kontraktu, nie ma żadnych domyślnych cenników projektu dla kontraktu. W kontrakcie zostanie wyświetlone ostrzeżenie. Wiadomość ta zawiera informację, że z powodu braku dołączonych cenników projektu, szacunkowa i rzeczywista praca nad projektem i koszty nie będą wyceniane.

## <a name="cost-price-lists"></a>Listy kosztów własnych

Listy kosztów własnych nie są domyślnymi obiektami w Project Operations. Ustalanie listy kosztów własnych dla kosztów projektów jest zawsze wykonywane na żywo. System ukończy następujący proces w celu określenia, które cenniki są obowiązujące dla kosztów:

1. Najpierw system wyszukuje cenniki dołączone do jednostki organizacji zmawiającej dla danego projektu.
2. Następnie program analizuje datę obowiązywania cenników odpowiadającą dacie nachodzącego oszacowania lub rzeczywistego wiersza. W takiej sytuacji w *wierszu oszacowania* istnieją odwołania do wszystkich trzech kontekstów w Project Operations:

    - Wiersz szacowania projektu
    - Szczegóły wiersza oferty
    - Szczegóły pozycji kontraktu
  
3. Jeśli istnieje wiele cenników, które obowiązują dla daty oszacowania przychodzącego lub wartości rzeczywistej, wybierany jest cennik utworzony jako ostatni.
4. Jeśli do zamawiającej jednostki organizacyjnej w projekcie nie są dołączone cenniki projektu, system wyszukuje listy kosztów własnych dołączone do parametrów projektu pasujących do waluty projektu.
5. Następnie program analizuje datę obowiązywania cenników odpowiadającą dacie nachodzącego oszacowania lub rzeczywistego wiersza. 
6. Jeśli istnieje wiele cenników, które obowiązują dla daty oszacowania przychodzącego lub wartości rzeczywistej, wybierany jest cennik utworzony jako ostatni.
7. Jeśli nie dołączono żadnych list kosztów własnych do parametrów projektu, które pasowałyby do waluty i daty obowiązywania, system domyślnie ustawia stawkę kosztu na zero (0) dla wiersza rzeczywistego lub przychodzącego oszacowania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]