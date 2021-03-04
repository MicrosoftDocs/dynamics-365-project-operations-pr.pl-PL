---
title: Rezerwacje zasobów i ich powiązania z przypisaniami zadań
description: W tym temacie zamieszczono informacje dotyczące sposobu zarządzania nazwanymi zasobami, rezerwacjami zasobów i przypisaniami zadań oraz relacji między tymi encjami.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0e4eea87bfb059a3c0be8ccbd2914a4d6c3cf46b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149961"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Rezerwacje zasobów i ich powiązania z przypisaniami zadań

[!include [banner](../includes/psa-now-project-operations.md)]

Istnieją dwa sposoby rezerwowania nazwanych zasobów do zespołu projektu oraz przypisywania im zadań projektu:

- Zasób może być bezpośrednio rezerwowany dla projektu i następnie przypisywany do zadań projektu.
- Zadania można przypisywać do zasobu ogólnego, który następnie służy do znajdowania i zastępowania zasobu ogólnego rzeczywistym. 

W obu przypadkach czynność rezerwowania zasobu rezerwuje dyspozycyjność zasobu.

Menedżer projektu planujący projekt jest właścicielem planu projektu i harmonogramu. Używając zasobu ogólnego dla przypisania, a następnie generując żądanie zasobu z niego, menedżer projektu może rezerwować zasoby dla projektu z rozkładami określonymi w planie projektu. Może on rezerwować zasoby dla projektu, a następnie przypisywać je do zadań, ale nie może dopasowywać rozkładu rezerwacji do rozkładu zadań. Rezerwacje nie wpływają na harmonogram projektu.

Pomyśl o projekcie złożonym z wielu nakładających się na siebie zadań, w którym liczne zasoby tego samego typu muszą pracować równocześnie. Jeśli zasób otrzymuje zarys, który różni się od zbiorczych przydziałów, trudno jest modyfikować zadania tak, aby dopasować je do potrzeb zarysu rezerwacji do ich zadań zindywidualizowanych i ich oryginalnych zarysów.

W poniższym przykładzie łączny nakład wymagany przez ten sam zasób od zestawu czterech zadań to 62 godziny w okresie dwóch tygodni co daje konkretny zarys. Jeśli zasób Robert jest zarezerwowany na 62 godziny w ciągu tych samych dwóch tygodni, ale dla innego zarysu, wymagania i rezerwacje są wyrównane.

| **Zarys zadania**    | **Suma godzin** | Pn, 4 czerwca | Wt, 5 czerwca | Śr, 6 czerwca | Cz, 7 czerwca | Pt, 8 czerwca | Sob, 9 czerwca | Nd, 10 czerwca | Pn, 11 czerwca | Wt, 12 czerwca | Śr, 13 czerwca | Cz, 14 czerwca | Pt, 15 czerwca |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Zadanie 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Zadanie 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Zadanie 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Zadanie 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Sumy**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Dyspozycyjność Roberta
| **Rezerwacja zasobów** | **Suma godzin** | Pn, 4 czerwca | Wt, 5 czerwca | Śr, 6 czerwca | Cz, 7 czerwca | Pt, 8 czerwca | Sob, 9 czerwca | Nd, 10 czerwca | Pn, 11 czerwca | Wt, 12 czerwca | Śr, 13 czerwca | Cz, 14 czerwca | Pt, 15 czerwca |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Robert                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Nie ma systematycznego sposobu przypisywania zarysu zarezerwowanych godzina do zadań każdego dnia. Jeśli Menedżer projektu chce zmienić harmonogram projektu, aby dopasować do dostępności zasobu, niezbędne będzie usunięcie przypisania i poprawienie wszystkich zadań, aby pasowały do zarysu rezerwacji.

W przypadku, gdy organizacja dała zadanie planowania projektu zarówno menedżerowi projektu jak i menedżerowi zasobów, menedżer projektu ustawia harmonogram a to obejmuje zarys wymaganej pracy. Menedżer zasobów nie powinien być w stanie zmienić harmonogramu bez wiedzy menedżera projektu, zmieniając zarys nakładu pracy podczas rezerwowania zasobów rzeczywistych. Jeśli menedżer zasobów realizuje coś innego niż żądania menedżera projektu, muszą oni uzgodnić, jakie zmiany są potrzebne w harmonogramie projektu.

Ponieważ rezerwacje i przypisania nie są ściśle powiązane, istnieje możliwość rezerwacji rozkładów, które są inne niż rozkłady zadań, lub zmienienia przypisań, co powoduje sytuacje, że rezerwacje i przypisania rozmijają się.

**Widok Uzgadnianie** umożliwia menedżerowi projektu zobaczenie rezerwacji i przypisań dla każdego z członków zespołu projektu. Widok korzysta z kolorów i cieniowania, aby wyświetlać niezgodność między rezerwacjami i przydziałami dla członków zespołu. Na podstawie tych informacji, menedżer projektu może podejmować działań naprawcze i rozszerzyć rezerwacje zasobów dla spraw, dla których istnieją przypisania i rezerwacje lub anulować rezerwacje, w których zasoby są zarezerwowane, ale nie dokonano przydziałów.

> [!NOTE]
> Po przeniesieniu zadania, dla którego użytkownik sam sporządził rozkład, rozkłady nie zostaną zachowane. Zarysy są generowane według kalendarza projektu, aby uwzględniać zmiany wprowadzone w godzinach pracy i dniach wolnych od pracy. Jest to ustawienie fabryczne, ponieważ system nie zna przeznaczenia oryginalnego rozkładu i nie może określić, czy warto zachować ten rozkład dla nowego przedziału czasu. Ponieważ rezerwacje i przypisania nie są połączone, rezerwacje zachowują oryginalne rozkłady rezerwacji. W tym przypadku będziesz musiał anulować i ponownie zarezerwować dla nowego zarysu przypisania.



[!INCLUDE[footer-include](../includes/footer-banner.md)]