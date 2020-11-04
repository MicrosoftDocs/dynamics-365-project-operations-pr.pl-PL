---
title: Raporty wydatków i różne osoby zatwierdzające
description: Ta temat zawiera informacje na temat raportów z wydatków, które wymagają zatwierdzenia przez więcej niż jedną osobę.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082015"
---
# <a name="expense-reports-and-multiple-approvers"></a>Raporty wydatków i różne osoby zatwierdzające

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W zależności od zasad zatwierdzania wydatków w danej organizacji, czasem więcej niż jedna osoba musi zatwierdzić przesłany raport o wydatkach. Podczas konfigurowania procesu przepływu pracy na potrzeby zatwierdzania raportów z wydatków można dodać elementy przepływu pracy zawierające zadania lub kroki dla jednej lub więcej osób zatwierdzających raporty o wydatkach. Na przykład może zaistnieć konieczność zatwierdzania wszystkich raportów z wydatków przez dwóch pracowników — kierownika pracownika, który je przedstawił i koordynatora ds. rozrachunków z dostawcami.

Jeśli zachodzi konieczność pracy przez wiele osób zatwierdzających raporty z wydatków, elementy przepływu pracy można dodać następującymi sposobami:

- Dodaj jeden element zatwierdzający zawierający jeden krok. Na przykład może zaistnieć konieczność przypisania do grupy użytkowników raportu o wydatkach i jego zaakceptowanie przez 50 procent członków grupy użytkowników.
- Dodaj jeden element zatwierdzający zawierający wiele kroków. Element zatwierdzania może na przykład zawierać następujące kroki:

    1. Kierownik pracownika, który składa raport, zatwierdza go.
    2. Pracownik ds. rozrachunków z dostawcami weryfikuje paragony i zapisy z raportów z wydatków.
    3. Właściciel budżetu zatwierdza raport o wydatkach.

- Dodaj wiele elementów zatwierdzania, z których każdy zawiera jeden krok. Można na przykład dodać osobny element zatwierdzania dla każdego z następujących kroków:

    1. Kierownik pracownika zatwierdza raport o wydatkach.
    2. Właściciel budżetu zatwierdza raport o wydatkach.
