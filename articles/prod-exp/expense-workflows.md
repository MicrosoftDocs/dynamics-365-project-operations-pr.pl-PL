---
title: Konfigurowanie przepływu pracy do zarządzania wydatkami
description: Użytkownik może skonfigurować proces przepływu pracy do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960530"
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