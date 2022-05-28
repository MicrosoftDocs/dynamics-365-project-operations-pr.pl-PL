---
title: Importowanie szacowań dla projektu do wiersza oferty projektu
description: Ten temat zawiera informacje na temat importowania szacunków z projektu do wiersza oferty projektu.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 24869ccc0c08470805a01dafc25f44ee12359d93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600479"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Importowanie szacowań dla projektu do wiersza oferty projektu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_


Jeśli projekt jest tworzony podczas etapu przed sprzedażą, można wybrać opcję importowania oszacowań finansowych z projektu do wiersza oferty opartej na projekcie.

1. Upewnij się, że wiersz oferty opartej na projekcie zawiera informacje o projekcie w polu **Projekt**.
2. Na karcie **Szczegóły wiersza oferty** wybierz opcję **Importuj z szacowań projektu**.
3. W oknie dialogowym, które się otworzy, wybierz jedną z następujących opcji podsumowania:

  - **Klasa transakcji**
  - **Kategoria**
  - **Rola** 
  - **Zadanie projektu**

W zależności od dokonanego wyboru oszacowania projektu dotyczące wszystkich klas transakcji zawartych w tym wierszu oferty są kopiowane. Aby sprawdzić, jakie klasy transakcji są uwzględnione, wybierz kartę **Ogólne** w wierszu oferty opartej na projekcie i sprawdź wartości opcji **Uwzględnij godzinę**, **Uwzględnij koszty** i **Uwzględnij opłaty**.

Podczas importowania oszacowań w systemie jest ustawiana domyślna cena oparta na cennikach projektów dołączonych do oferty, a typ rozliczenia ustawiony jest na wartość w wierszu oferty opartej na projekcie. Jeśli rola lub kategoria została ustawiona w wierszu oferty opartej na projekcie jako nieodpłatna, zaimportowana pozycja szacowania będzie ustawiona jako nieodpłatna i nie zostanie dodana do wartości w wierszu oferty.

Kiedy wiersz oferty zawiera szczegółowe informacje o wierszach, pola **Wartość oferty** oraz **Szacowany podatek** w wierszu oferty są sumowane i nie można ich edytować.

W przypadku wybrania wielu opcji, system próbuje dokonać podsumowania według wszystkich wybranych opcji. Oznacza to, że dane wyjściowe z zaimportowanych wierszy oferty będą większe niż w przypadku wybrania tylko jednej opcji podsumowania.

Na przykład jeśli w projekcie istnieją poniższe wiersze szacowane dotyczące wydatków.

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| Zadanie B | Hotel | 10.01.2020 | 100 | 200 | 800 |
| Zadanie C | Hotel | 11.01.2020 | 2 | 200 | 400 |

Kiedy użytkownik wybierze opcję podsumowania według klas transakcji, zostaną zaimportowane poniższe informacje.

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| | | 10.01.2020 | 3.34 | 840 | 2800 |

Kiedy użytkownik wybierze opcję podsumowania według klas transakcji i kategorii, zostaną zaimportowane poniższe informacje.

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| | Hotel | 10.01.2020 | 6 | 200 | 1200 |

Kiedy użytkownik wybierze opcję podsumowania według klas transakcji, kategorii i zadania węzła liścia, zostaną zaimportowane poniższe informacje. Zauważ, że taki wynik jest taki sam, jak w projekcie.

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| Zadanie B | Hotel | 10.01.2020 | 100 | 200 | 800 |
| Zadanie C | Hotel | 11.01.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
