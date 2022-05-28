---
title: Importowanie szacowania do pozycji kontraktu opartego na projekcie - wersja uproszczona
description: W tym temacie zamieszczono informacje dotyczące sposobu importowania szacunków finansowych z projektu do wiersza kontraktu.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 52abaa785b50b914e7813aaf4660504ee99129d6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582079"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importowanie szacowania do pozycji kontraktu opartego na projekcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W rozwiązaniu Dynamics 365 Project Operations można importować szacowania z projektu do pozycji kontraktu opartego na projekcie.

1. Sprawdź, czy pole **Projekt** w pozycji kontraktu opartej na projekcie zostało wypełnione.
2. Na karcie **Szczegóły pozycji kontraktu karty**, w podsiatce wybierz pozycję **Importuj z oszacowania projektu**. Zostanie wyświetlona strona dialogu z opcjami podsumowania. Dostępne opcje podsumowania to: **Klasa transakcji**, **Kategoria**, **Rola** i **Zadanie projektu**.
3. W zależności od dokonanego wyboru podsumowania, oszacowania projektu dotyczące wszystkich klas transakcji i zadań zawartych w tym wierszu oferty są kopiowane. Aby sprawdzić, jakie klasy transakcji są uwzględnione, wybierz kartę **Ogólne** z wierszu kontraktu opartego na projekcie i sprawdź wartości pól **Uwzględnij godzinę**, **Uwzględnij koszty** i **Uwzględnij opłaty**. 
4. Aby sprawdzić, jakie zadania są uwzględnione, wybierz kartę **Zadania odpłatne** w pozycji kontraktu. W zależności od zadań, które mają ustawioną w polu **Zawiera klasy transakcji** wartość **Tak**, wszystkie oszacowania dotyczące tych kombinacji klas i transakcji są importowane do pozycji kontraktu.

Podczas importowania oszacowań w systemie jest ustawiana domyślna cena oparta na cennikach projektów dołączonych do oferty, a typ rozliczenia w systemie ustawiony jest na wartość w wierszu kontraktu opartego na projekcie. Jeśli zadanie, rola lub kategoria została ustawiona w wierszu kontraktu opartego na projekcie jako nieodpłatna, zaimportowana pozycja szacowania dla tej roli będzie ustawiona jako nieodpłatna i nie zostanie dodana do wartości w wierszu kontraktu.

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
| &nbsp; | &nbsp; | 10.01.2020 | 3.34 | 840 | 2800 |

Kiedy użytkownik wybierze opcję podsumowania według **klas transakcji** i **kategorii**, zostaną zaimportowane poniższe informacje:

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| &nbsp;| Hotel | 10.01.2020 | 6 | 200 | 1200 |

Kiedy użytkownik wybierze opcję podsumowania według **klas transakcji**, **kategorii** i **zadania węzła liścia**, zostaną zaimportowane poniższe informacje. Zauważ, że taki wynik jest taki sam, jak w projekcie:

| Zadanie | Kategoria | Data | Ilość | Cena jednostkowa | Kwota |
| --- | --- | --- | --- | --- | --- |
| Zadanie A | Opłata za przelot | 10.01.2020 | 100 | 400 | 1600 |
| Zadanie B | Hotel | 10.01.2020 | 100 | 200 | 800 |
| Zadanie C | Hotel | 11.01.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]