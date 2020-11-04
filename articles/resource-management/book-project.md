---
title: Rezerwacja do projektu
description: W tym temacie zamieszczono informacje dotyczące sposobu rezerwowania zasobów do projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081864"
---
# <a name="book-to-a-project"></a>Rezerwacja do projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Istnieją też sytuacje, w których menedżer projektu lub menedżer zasobów musi zaalokować zasób do projektu bez konieczności definiowania określonego wymagania od ogólnego członka zespołu. Można to osiągnąć na trzy sposoby.

- Rezerwacja na siatce członków zespołu
- Rezerwacja z tablicy harmonogramu
- Rezerwacja z poziomu formularza **Projekt**

## <a name="book-from-the-team-member-grid"></a>Rezerwacja na siatce członków zespołu

Jeśli organizacja działa w trybie hybrydowego przydziału zasobów, menedżer projektu może zarezerwować zasób bezpośrednio do projektu, wykonując następujące kroki.

1. W projekcie przejdź do siatki członka zespołu i wybierz pozycję **Nowy**.
2. Określ nazwę stanowiska i rolę zasobu.
3. W widoku menu wybierz odpowiedni zasób do zaksięgowania.
4. Po wybraniu zasobu należy zdefiniować w nim następujące informacje dotyczące zaksięgowania zasobu:

    - Data rozpoczęcia
    - Data zakończenia
    - Metoda alokacji
    - Liczba godzin, jeśli ma to zastosowanie
    - Osoba zatwierdzająca w projekcie

6. Wybierz pozycję **Zapisz i zamknij**

## <a name="book-from-the-schedule-board"></a>Rezerwacja z tablicy harmonogramu

Gdy menedżer zasobów musi zarezerwować zasób bezpośrednio do projektu, może użyć tablicy harmonogramu i wymagania projektu. Wymaganie projektu to zapotrzebowanie na zasoby, które jest zawsze dostępne do rezerwacji w programie. Wykonaj poniższe kroki, aby zarezerwować zasób z tablicy harmonogramu do projektu.

1. Przejdź do tablicy harmonogramu i na lewej stronie odfiltruj zasoby uwzględniane w zależności od wymagania.
2. W dolnym okienku wybierz kartę **Projekt** , aby wyświetlić listę zapotrzebowań na projekt.
3. Przeciągnij zapotrzebowanie na dany zasób i określ następujące informacje:

    - Data rozpoczęcia
    - Data zakończenia
    - Stan rezerwacji
    - Metoda rezerwacji
    - Czas trwania

## <a name="book-from-the-project-form"></a>Rezerwacja z poziomu formularza Projekt

Jako menedżer projektu być może będziesz musiał zarezerwować zasób do projektu, ale znać będziesz tylko kryteria a nie nazwę zasobu. Wykonaj poniższe kroki, aby za pomocą asystenta planowania znaleźć zasób na podstawie różnych dostępnych atrybutów zasobu. 

1. Przejdź do projektu i wybierz pozycję **Rezerwuj** , aby otworzyć Asystenta planowania.
2. Korzystając z filtrów po lewej stronie Asystenta planowania, zawęź kryteria i wybierz opcję **Wyszukaj.**
3. W ramach zasobów zwracanych w wyniku można przeprowadzić rezerwację.

> [!NOTE]
> W tej metodzie nie są tworzone żadne rezerwacje danego zasobu. Zamiast tego, rezerwacja dodaje go po prostu do zespołu projektu. Po dodaniu członka zespołu do projektu menedżer projektu może użyć funkcji utrzymania rezerwacji lub przedłużenia rezerwacji, aby dodać wymagane rezerwacje do zasobu.
