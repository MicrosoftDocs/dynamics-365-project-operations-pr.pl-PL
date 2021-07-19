---
title: Wydajność propozycji faktury projektu
description: Ten temat zawiera informacje o ulepszeniach wydajności propozycji faktur projektu.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269803"
---
# <a name="project-invoice-proposal-performance"></a>Wydajność propozycji faktury projektu

[!include [banner](../includes/banner.md)]

Podczas tworzenia nowej propozycji faktury możesz napotkać problemy z wydajnością, ponieważ wzrasta liczba projektów i podprojektów. Aby poprawić wydajność, dostępna jest funkcja, która skraca czas potrzebny do utworzenia nowej propozycji faktury dla zaksięgowanych transakcji projektu.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Włącz poprawę wydajności propozycji faktury za projekt
Aby włączyć funkcję poprawy wydajności propozycji faktury za projekt, wykonaj następujące kroki.

1.  Przejdź do opcji **Zarządzanie funkcjami** > **Wszystkie**. Na liście funkcji znajdź **Poprawa wydajności propozycji faktury za projekt**.
2.  Wybierz opcję **Włącz teraz**.
3.  Odśwież przeglądarkę i utwórz nową fakturę.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Wyłącz poprawę wydajności propozycji faktury za projekt
Wykonaj następujące kroki, aby wyłączyć poprawę wydajności propozycji faktury za projekt.

1.  Przejdź do opcji **Zarządzanie funkcjami** > **Wszystkie**. Na liście funkcji znajdź **Poprawa wydajności propozycji faktury za projekt**.
2.  Wybierz opcję **Wyłącz**.
3.  Odśwież przeglądarkę.

> [!NOTE]
> Wydajności propozycji faktury nie można zastosować, jeśli włączono reguły fakturowania.
> 
> Podczas procesu przetwarzania wsadowego w celu utworzenia propozycji faktury liczba zadań podrzędnych będzie dzielić zadania na maksymalną liczbę w zależności od liczby kontraktów z transakcjami możliwymi do zafakturowania, niezależnie od tego, co wprowadzono. Jeśli na przykład wprowadzisz wartość **3** dla liczby zadań podrzędnych na potrzeby tworzenia propozycji faktury w partii i istnieją tylko dwa kontrakty z transakcjami do fakturowania, tworzone są tylko dwa zadania podrzędne.
