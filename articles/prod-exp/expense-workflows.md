---
title: Konfigurowanie przepływu pracy do zarządzania wydatkami
description: Użytkownik może skonfigurować proces przepływu pracy do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd5c56fff62b737e1277e491b07f0139075444fc
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685253"
---
# <a name="set-up-expense-management-workflows"></a>Konfigurowanie przepływu pracy do zarządzania wydatkami

Użytkownik może skonfigurować proces przepływu pracy służący do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków. Dokumenty, dla których można zdefiniować przepływy pracy to raporty z wydatków, wnioski wyjazdowe i żądania zaliczek na poczet wydatków.

Przepływ pracy reprezentuje proces biznesowy. Definiuje sposób przepływu dokumentu za pośrednictwem systemu oraz wskazuje, kto musi zakończyć zadanie lub zatwierdzić dokument. Istnieje szereg korzyści płynących z korzystania z systemu przepływu pracy w organizacji:

-   **Spójność procesu** — można zdefiniować proces zatwierdzania dla określonych dokumentów, takich jak zapotrzebowania na zakup i raporty o wydatkach. Korzystanie z systemu przepływu pracy pomaga zagwarantować, że dokumenty zostaną przetwarzane i będą zatwierdzone w sposób spójny i skuteczny.

-   Widoczność procesu — można śledzić stan, historię i metryki wydajności dotyczące konkretnego wystąpienia przepływu pracy. Pomaga to w określeniu, czy w celu zwiększenia efektywności należy wprowadzić zmiany w przepływie pracy.

-   Scentralizowana lista pracy — użytkownicy mogą wyświetlać scentralizowaną listę zadań w celu wyświetlenia przydzielonych im zadań i zatwierdzeń. 

**Typy relacji między obiektami do utworzenia**

W poniższej tabeli przedstawiono typy przepływów pracy, które można tworzyć w module **Wydatków**.


|              <strong>Typ</strong>              |                   <strong>Tego typu należy używać, aby przeprowadzić</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Raport z wydatków</strong>         |            Tworzenie przepływów pracy zatwierdzania raportów o wydatkach.             |
|  <strong>Automatyczne księgowanie raportów wydatków</strong>   |        Tworzenie przepływów pracy automatycznego księgowania raportów o wydatkach.        |
|       <strong>Pozycja wydatku</strong>        |     Tworzenie przepływów pracy zatwierdzania raportów dla elementów wiersza w raportach dotyczących wydatków.      |
| <strong>Automatyczne księgowanie pozycji wiersza wydatków</strong> | Tworzenie przepływów pracy automatycznego księgowania elementów wiersza w raportach dotyczących wydatków. |
|       <strong>Wnioski wyjazdowe</strong>       |          Tworzenie przepływów pracy dla zatwierdzania wniosków wyjazdowych.           |
|      <strong>Zaliczka gotówkowa — anulowanie</strong>      |         Tworzenie przepływów pracy zatwierdzania dla wniosków o zaliczkę w gotówce.          |
|        <strong>Zwrot podatku VAT</strong>        | Utwórz przepływy pracy zatwierdzenia w celu odzyskania podatku VAT.  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]