---
title: Importowanie szacowania do pozycji kontraktu opartego na projekcie
description: W tym temacie zamieszczono informacje dotyczące sposobu importowania szacunków z projektu do wiersza kontraktu.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f8d9637e4a8bd09664c43ccc2b02514dc825997e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010259"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importowanie szacowania do pozycji kontraktu opartego na projekcie

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W rozwiązaniu Dynamics 365 Project Operations można importować szacowania z projektu do pozycji kontraktu opartego na projekcie.

1. Sprawdź, czy pole **Projekt** w pozycji kontraktu opartej na projekcie jest wypełnione.
2. Na karcie **Szczegóły pozycji kontraktu karty**, w podsiatce wybierz pozycję **Importuj z oszacowania projektu**. Zostanie wyświetlona strona dialogu z opcjami podsumowania. Dostępne opcje podsumowania to **Klasa transakcji**, **Kategoria**, **Rola** i **Zadanie projektu**. W zależności od dokonanego wyboru do podsumowania, oszacowania projektu dotyczące wszystkich klas transakcji zawartych w tym wierszu oferty są kopiowane. 
3. Aby sprawdzić, jakie klasy transakcji są uwzględnione, wybierz kartę **Ogólne** w wierszu kontraktu opartego na projekcie i sprawdź wartości pól **Uwzględnij godzinę**, **Uwzględnij koszty** i **Uwzględnij opłaty**.

Podczas importowania oszacowań w systemie jest ustawiana domyślna cena oparta na cennikach projektów dołączonych do oferty, a typ rozliczenia ustawiony jest na wartość w wierszu kontraktu opartego na projekcie. Jeśli rola lub kategoria została ustawiona w wierszu kontraktu opartego na projekcie jako nieodpłatna, zaimportowana pozycja szacowania dla tej roli będzie ustawiona jako nieodpłatna i nie zostanie dodana do wartości w wierszu kontraktu.

Kiedy wiersz kontraktu zawiera szczegółowe informacje o wierszach, pola **Wartość kontraktu** oraz **Szacowany podatek** w wierszu kontraktu są sumowane i nie można ich edytować.

W przypadku wybrania wielu opcji, system próbuje dokonać podsumowania według wszystkich wybranych opcji. W wynikach podsumowania zaimportowano więcej pozycji kontraktu niż w przypadku wybrania tylko jednej opcji podsumowania.

Na przykład jeśli w projekcie istnieją poniższe wiersze szacowane dotyczące wydatków:

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| Zadanie B | Hotel | 10.01.2020 | 100 | 200 | 800 |
| Zadanie C | Hotel | 11.01.2020 | 2 | 200 | 400 |

Kiedy użytkownik wybierze opcję podsumowania według **klas transakcji**, zostaną zaimportowane poniższe informacje:

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10.01.2020 | 3.34 | 840 | 2800 |

Kiedy użytkownik wybierze opcję podsumowania według **klas transakcji** i **kategorii**, zostaną zaimportowane poniższe informacje:

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| &nbsp;  | Hotel | 10.01.2020 | 6 | 200 | 1200 |

Kiedy użytkownik wybierze opcję podsumowania według **klas transakcji**, **kategorii** i **zadania węzła liścia**, zostaną zaimportowane poniższe informacje. Zauważ, że taki wynik jest taki sam, jak w projekcie:

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| Zadanie B | Hotel | 10.01.2020 | 100 | 200 | 800 |
| Zadanie C | Hotel | 11.01.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]