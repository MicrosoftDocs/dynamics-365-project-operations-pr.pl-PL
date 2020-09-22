---
title: Zamówienie sprzedaży projektów dotyczące projektów typu Czas i materiały
description: W tym temat wyjaśniono, jak tworzyć oparte na projektach zamówienia sprzedaży na potrzeby projektów typu czasu i materiałów.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754280"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Zamówienie sprzedaży projektów dotyczące projektów typu Czas i materiały

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

W tym temat opisano sposób tworzenia zamówienia sprzedaży dla projektu. Zamówienia sprzedaży można tworzyć tylko dla projektów typu **czas i materiały**.

Jeśli projekt typu czas i materiały ma wiele źródeł finansowania w kontrakcie projektu, należy włączyć parametr **Zezwalaj na zamówienia sprzedaży dla projektów z wieloma źródłami finansowania** na stronie **Parametry Zarządzanie projektami i księgowanie**. 

> [!NOTE]
> - Obsługa zamówień sprzedaży projektów z wieloma źródłami finansowania jest dostępna od wersji aplikacji 10.0.2 i nowszych.
> - Parametr umożliwiający obsługę zamówień sprzedaży projektów z wieloma źródłami finansowania zostanie usunięty w fali wydań z kwietnia 2020 r., Po czym funkcja będzie zawsze włączona.

Zamówienia sprzedaży oparte na projektach można tworzyć na dwa sposoby:

- Przejść do projektu. W okienku akcji wybierz pozycję **Zarządzaj > Zadania towarów > Zamówienie sprzedaży**. Informacje o projekcie będą domyślnie zamówione na zamówienie sprzedaży z projektu. Jeśli kontrakt projektu zawiera więcej niż jedno źródło finansowania, należy wybrać źródło finansowania, aby ustawić klienta dla danego zamówienia sprzedaży. Jeśli dla danego projektu istnieje tylko jedno źródło finansowania, klient zostanie ustawiony na automatyczny.
- Przejdź do strony listy **Wszystkie zamówienia sprzedaży** i utwórz nowe zamówienie sprzedaży. Konieczne będzie wybranie projektu dla zamówienia sprzedaży. Po wybraniu projektu klient zostanie ustawiony ze źródła finansowania lub konieczne będzie wybranie źródła finansowania, jeśli kontrakt projektu zawiera wiele źródeł finansowania.

