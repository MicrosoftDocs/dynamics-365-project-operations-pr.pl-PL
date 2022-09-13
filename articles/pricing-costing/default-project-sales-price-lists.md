---
title: Cenniki domyślne
description: W tym artykule zamieszczono informacje na temat domyślnych cenników sprzedaży i kosztów w aplikacji Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410276"
---
# <a name="default-price-lists"></a>Cenniki domyślne

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

## <a name="sales-price-lists"></a>Cenniki sprzedaży

Każda oferta projektu i umowa w rozwiązaniu Dynamics 365 Project Operations zawiera domyślny cennik sprzedaży. 

### <a name="price-list-default-on-project-quotes"></a>Domyślny cennik dla ofert projektu
System ukończy następujący proces w celu określenia, które cenniki są obowiązujące w ofercie:

1. System wyszukuje cenniki dołączone do cenników danego konta. 
1. Jeśli do rekordu klienta nie są dołączone cenniki projektu, system wyszukuje w zestawie ceny sprzedaży dołączone do parametrów projektu pasujących do waluty oferty projektu.
1. Następnie system sprawdza datę wejścia w życie cenników odpowiadającą zakresowi dat oferty projektu. Sprawdza datę utworzenia oferty.
1. Jeśli istnieje wiele cenników, które są wiążące dla oferty projektu, wszystkie cenniki dla oferty projektu są domyślne.
1. Jeśli brak obowiązujących cenników w ofercie projektu, nie ma żadnych domyślnych cenników projektu dla oferty. W ofercie projektu zostanie wyświetlone ostrzeżenie. Wiadomość ta zawiera informację, że z powodu braku dołączonych cenników projektu, szacunkowa i rzeczywista praca nad projektem i koszty nie będą wyceniane.

### <a name="price-list-default-on-project-contracts"></a>Domyślny cennik dla kontraktów projektu 
System ukończy następujący proces w celu określenia, które cenniki są obowiązujące w kontrakcie:

1. Jeśli z poziomu oferty utworzono kontrakt, cenniki projektu dotyczące oferty są kopiowane oddzielnie i załączane do kontraktu projektu.
1. Jeżeli kontrakt jest tworzony od podstaw, system wyszukuje cenniki dołączone do cenników projektu klienta na koncie. Jeśli do rekordu konta nie są dołączone cenniki projektu, system wyszukuje cenników sprzedaży dołączonych do parametrów projektu, które pasują do waluty kontraktu projektu.
1. Następnie system sprawdza datę wejścia w życie cenników odpowiadającą zakresowi dat kontraktu projektu. Sprawdza datę utworzenia kontraktu.
1. Jeśli istnieje wiele cenników, które są wiążące dla kontraktu, wszystkie cenniki dla kontraktu są domyślne.
1. Jeśli brak obowiązujących cenników dla kontraktu, nie ma żadnych domyślnych cenników projektu dla kontraktu. W kontrakcie zostanie wyświetlone ostrzeżenie. Wiadomość ta zawiera informację, że z powodu braku dołączonych cenników projektu, szacunkowa i rzeczywista praca nad projektem i koszty nie będą wyceniane.

## <a name="cost-price-lists"></a>Listy kosztów własnych

Listy kosztów własnych nie są domyślnymi obiektami w Project Operations. Ustalanie listy kosztów własnych dla kosztów projektów jest zawsze wykonywane w oparciu o poszczególne transakcje. System ukończy następujący proces w celu określenia, które cenniki są obowiązujące dla kosztów:

1. Platforma wyszukuje cenniki dołączone do jednostki organizacji kontraktującej dla danego projektu.
1. Następnie platforma analizuje datę obowiązywania cenników odpowiadającą dacie kontekstu nachodzącego oszacowania lub kontekstu wartości rzeczywistych.

    - *Kontekst szacowania* odnosi się do dowolnych z trzech kontekstów w aplikacji Project Operations:

        - Wiersz szacowania projektu
        - Szczegóły wiersza oferty
        - Szczegóły pozycji kontraktu

    - *Kontekst wartości rzeczywistych* odnosi się do dowolnych z trzech źródeł wartości rzeczywistych w aplikacji Project Operations:

       - Wprowadzanie wierszy arkusza, które są tworzone ręcznie, lub poprawianie wierszy arkuszy utworzonych w arkuszu korekt
       - Wiersze arkusza utworzone podczas przesyłania dzienników użycia dla czasu, wydatków lub materiałów
       - Szczegóły wiersza faktury

    Gdy aplikacja Project Operations dopasuje obowiązywanie daty dla nadchodzącego wiersza arkusza lub szczegółu wiersza faktury w *kontekście rzeczywistym*, użyje pola **Data transakcji**.

    - Jeśli wiele cenników obowiązuje dla daty nachodzącego kontekstu szacowania lub kontekstu rzeczywistego, wybierany jest cennik utworzony jako ostatni.
    - Jeśli do zamawiającej jednostki organizacyjnej w projekcie nie dołączono cenników projektu, platforma wyszukuje listy kosztów własnych dołączone do parametrów projektu pasujących do waluty projektu.

## <a name="enable-multi-currency-cost-price-list"></a>Włącz wielowalutową listę kosztów własnych

To ustawienie można znaleźć w obszarze **Ustawienia** \> **Parametry**. Wartością domyślną jest **Nie**.

Jeśli to ustawienie jest włączone (czyli ta wartość jest ustawiona na **Tak**), platforma zachowuje się w następujący sposób:

- Zezwala ona na skojarzenie cenników kosztów własnych z jednostką organizacyjną. Na przykład cennik kosztów własnych w walucie EUR można dołączyć do jednostki organizacyjnej w walucie USD. Platforma nadal będzie sprawdzać, czy cenniki kosztów własnych dołączone do jednostki organizacyjnej nie mają nakładających się dat obowiązywania.
- Sprawdza, czy cenniki kosztów własnych dołączone do parametrów projektu nie mają nakładających się dat obowiązywania, nawet jeśli są w różnych walutach. To zachowanie różni się od zachowania domyślnego (czyli zachowania, gdy wartość jest ustawiona na **Nie**). W przypadku zachowania domyślnego sprawdzane są tylko cenniki kosztów własnych, które mają **tę samą** walutę pod kątem nienakładających się dat obowiązywania.
- W przypadku kontekstu transakcji przychodzących cennik kosztów własnych jest określany wyłącznie na podstawie daty obowiązywania. To zachowanie różni się od zachowania domyślnego, w którym platforma wybiera cennik kosztów własnych z dopasowaną walutą projektu i datą obowiązywania.

Z powodu tych zmian zachowań klienci aplikacji Project Operations będą w stanie obsługiwać globalny cennik kosztów własnych, który będzie dotyczył całej firmy. Nie będą oni musieli mieć cenników w każdej walucie operacji. Cennik globalny będzie miał wpływ na datę obowiązywania i umożliwi ustawienie stawek kosztów w dowolnej walucie w przypadku określonej kombinacji wartości wymiarów cen. Waluta cennika kosztów własnych jest używana tylko do wprowadzania wartości domyślnych, gdy tworzone są rekordy elementów **Ceny ról**, **Ceny kategorii** i **Cennik**. Nie będzie ona używana do określania cennika.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
