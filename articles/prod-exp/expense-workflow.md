---
title: Przepływ pracy zarządzania wydatkami
description: W tym temacie przedstawiono sposób korzystania z systemu przepływu pracy w Microsoft Dynamics 365 Finance w celu skonfigurowania procesu przeglądu raportów o wydatkach w zarządzaniu wydatkami.
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
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960575"
---
# <a name="expense-management-workflow"></a>Przepływ pracy zarządzania wydatkami

Sposób korzystania z systemu przepływu pracy można dostosować w celu skonfigurowania procesu przeglądu raportów o wydatkach w zarządzaniu wydatkami. Użytkownik może skonfigurować przepływ pracy, który korzysta z następujących kryteriów w celu określenia, kto zatwierdza raporty o wydatkach:

- Hierarchia raportowania pracowników i wstępnie zdefiniowane ograniczenia zatwierdzania
- Zatwierdzanie na wielu poziomach, które obsługuje zatwierdzanie tymczasowe i ostateczną osobę zatwierdzającą
- Zakres finansowy i zakres odpowiedzialności projektu
- Przypisywanie do określonych użytkowników lub grup użytkowników

Zatwierdzanie przepływu pracy można utworzyć na potrzeby raportów z wydatków, wniosków wyjazdowych, zaliczek w gotówce oraz zwrotu podatku VAT.

**Przykład**

Poniższy proces stanowi przykład przepływu pracy Zarządzanie wydatkami w ramach raportu z wydatków.

1. Pracownik tworzy i zapisuje raport wydatków.
2. Pracownik przesyła raport do zatwierdzenia. Osoba zatwierdzająca jest identyfikowana na podstawie reguł zdefiniowanych podczas konfigurowania przepływu pracy.
3. Osoba zatwierdzająca otrzymuje powiadomienie o przygotowaniu raportu o wydatkach do zatwierdzenia. Sprawdza, a następnie zatwierdza raport z wydatków i potwierdza, że są spełnione następujące warunki:

    - Koszty nie naruszają żadnych zasad dotyczących wydatków. Jeśli wydatek narusza zasadę, osoba zatwierdzająca weryfikuje, czy raport z wydatków zawiera prawidłowe uzasadnienie biznesowe.
    - Do raportu z wydatków są dołączone paragony w wersji cyfrowej.

4. Osoba zatwierdzająca zatwierdza raport o wydatkach.
5. Raport o wydatkach jest przypisywany do koordynatora rozrachunków z klientami w celu zaksięgowania.
6. W zależności od tego, czy skonfigurowane jest automatyczne księgowanie, czy nie, ma miejsce jedno z następujących:

    - Jeśli skonfigurowano automatyczne księgowanie, raport o wydatkach jest przetwarzany w celu dokonania płatności, a stan raportu o wydatkach jest zaktualizowany.
    - Jeśli automatyczne księgowanie nie jest skonfigurowane, wtedy koordynator ds. rozrachunków z dostawcami weryfikuje, że wszystkie oryginalne paragony zostały przesłane i że zgadzają się z kosztami w raporcie z wydatków. Wszystkie kody podatków wprowadzone w raporcie z wydatkami również muszą zostać sprawdzone pod kątem poprawności.

Dopiero po sprawdzeniu tych wymagań raport jest księgowany.

Po zaksięgowaniu raportu o wydatkach płatność jest zatwierdzana, a pracownik otrzymuje zwrot.
