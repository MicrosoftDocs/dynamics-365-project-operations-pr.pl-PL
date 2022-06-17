---
title: Raporty wydatków i różne osoby zatwierdzające
description: Ten artykuł zawiera informacje dotyczące raportów z wydatków, które wymagają zatwierdzenia przez wiele osób.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae72ae578455a626c069c01552b3edf60df706a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933965"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Raporty wydatków i różne osoby zatwierdzające

W zależności od zasad zatwierdzania wydatków w danej organizacji, czasem więcej niż jedna osoba musi zatwierdzić przesłany przez pracownika raport o wydatkach. Podczas konfigurowania procesu przepływu pracy na potrzeby zatwierdzania raportów z wydatków można dodać elementy przepływu pracy zawierające zadania lub kroki dla jednej lub więcej osób zatwierdzających raporty o wydatkach. Na przykład może zaistnieć konieczność zatwierdzania wszystkich raportów z wydatków przez dwóch pracowników — najpierw przez kierownika pracownika, który je przedstawił, a potem przez koordynatora ds. rozrachunków z dostawcami.

Jeśli zachodzi konieczność pracy przez wiele osób zatwierdzających raporty z wydatków, elementy przepływu pracy można dodać następującymi sposobami:

- Dodaj jeden element zatwierdzający zawierający jeden krok. Na przykład może zaistnieć konieczność przypisania do grupy użytkowników raportu o wydatkach i jego zaakceptowanie przez 50 procent członków grupy użytkowników.
- Dodaj jeden element zatwierdzający zawierający wiele kroków. Element zatwierdzania może na przykład zawierać następujące kroki:

    1. Kierownik pracownika, który składa raport, zatwierdza go.
    2. Pracownik ds. rozrachunków z dostawcami weryfikuje paragony i zapisy z raportów z wydatków.
    3. Właściciel budżetu zatwierdza raport o wydatkach.

- Dodaj wiele elementów zatwierdzania, z których każdy zawiera jeden krok. Można na przykład dodać osobny element zatwierdzania dla każdego z następujących kroków:

    1. Kierownik pracownika zatwierdza raport o wydatkach.
    2. Właściciel budżetu zatwierdza raport o wydatkach.


[!INCLUDE[footer-include](../includes/footer-banner.md)]