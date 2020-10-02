---
title: Konfigurowanie przepływu pracy do zarządzania wydatkami
description: Użytkownik może skonfigurować proces przepływu pracy służący do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896564"
---
# <a name="set-up-workflows-for-expense-management"></a>Konfigurowanie przepływu pracy do zarządzania wydatkami

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Użytkownik może skonfigurować proces przepływu pracy do przeglądania i zatwierdzania dokumentów dotyczących wyjazdów i wydatków. Można zdefiniować przepływy pracy dla raportów wydatków, wniosków wyjazdowych i żądań zaliczek na poczet wydatków.

Przepływ pracy reprezentuje proces biznesowy i definiuje sposób przepływu dokumentu przez system. Przepływ pracy określa również, kto musi zakończyć zadanie lub zatwierdzić dokument. Istnieje szereg korzyści płynących z korzystania z systemu przepływu pracy w organizacji:

- **Spójność procesu**: można zdefiniować proces zatwierdzania dla określonych dokumentów, takich jak zapotrzebowania na zakup i raporty o wydatkach. Korzystanie z systemu przepływu pracy pomaga zagwarantować, że dokumenty zostaną przetwarzane i będą zatwierdzone w sposób spójny i skuteczny.
- **Widoczność procesu**: można śledzić stan, historię i metryki wydajności dotyczące konkretnego wystąpienia przepływu pracy. Pomaga to w określeniu, czy w celu zwiększenia efektywności należy wprowadzić zmiany w przepływie pracy.
- **Scentralizowana lista pracy**: użytkownicy mogą wyświetlać scentralizowaną listę zadań w celu wyświetlenia przydzielonych im zadań i zatwierdzeń. 

## <a name="workflow-types"></a>Typy przepływu pracy

W poniższej tabeli przedstawiono typy przepływów pracy, które można tworzyć w module **Zarządzanie wydatkami**.


|              <strong>Typ</strong>              |                   <strong>Tego typu należy używać, aby przeprowadzić</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatyczne zatwierdzanie raportów wydatków</strong> |            Tworzenie przepływów pracy zatwierdzania raportów o wydatkach.             |
|  <strong>Automatyczne księgowanie raportów wydatków</strong>   |        Tworzenie przepływów pracy automatycznego księgowania raportów o wydatkach.        |
|       <strong>Pozycja wydatku</strong>        |     Tworzenie przepływów pracy zatwierdzania raportów dla elementów wiersza w raportach dotyczących wydatków.      |
| <strong>Automatyczne księgowanie pozycji wiersza wydatków</strong> | Tworzenie przepływów pracy automatycznego księgowania elementów wiersza w raportach dotyczących wydatków. |
|       <strong>Wnioski wyjazdowe</strong>       |          Tworzenie przepływów pracy dla zatwierdzania wniosków wyjazdowych.           |
|      <strong>Zaliczka gotówkowa — anulowanie</strong>      |         Tworzenie przepływów pracy zatwierdzania dla wniosków o zaliczkę w gotówce.          |
|        <strong>Zwrot podatku VAT</strong>        | Utwórz przepływy pracy zatwierdzenia w celu odzyskania podatku VAT.  |
