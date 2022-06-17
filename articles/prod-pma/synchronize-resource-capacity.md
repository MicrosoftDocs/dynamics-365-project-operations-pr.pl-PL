---
title: Synchronizowanie dyspozycyjności zasobów
description: Ten artykuł zawiera informacje o sposobach synchronizowania zdolności produkcyjnych zasobu w kalendarzach i projektach.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920717"
---
# <a name="synchronize-resource-capacity"></a>Synchronizowanie dyspozycyjności zasobów

[!include [banner](../includes/banner.md)]

Procesy synchronizacji zasobów pomagają zagwarantować, że informacje z kalendarza i kalendarza podstawowego trafiają do planowania zasobów projektu. Jeśli zostanie zmieniony kalendarz, procesy będą wymagały aktualizacji planowania zasobów projektów. Procesy pomagają również zwiększyć wydajność, ponieważ informacje o zasobach kalendarza są z góry synchronizowane. Z tego powodu aktualizacje informacji o harmonogramach zasobów są wykonywane szybciej. Zaleca się, aby zamiast pojedynczych procesów zaplanować przetwarzanie w postaci partii. W przeciwnym razie istnieje ryzyko, że użytkownik zapamiętał datę utworzenia ostatniej synchronizacji informacji. Jeśli nie są używane daty łączne, podczas synchronizacji między datami mogą następować przerwy.

![Synchronizacja kalendarza.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizuj podsumowania pojemności zasobów

Proces synchronizacji ma na celu zsynchronizowanie wszystkich informacji kalendarza zasobów. Te informacje obejmują informacje kalendarza podstawowego o wszelkich zmianach w tabeli pojemności kalendarza zasobów projektu. Jeśli w projekcie zostaną dodane nowe zasoby, synchronizacja pomaga zagwarantować, że dostępne są zaktualizowane informacje w kalendarzu. Tę synchronizację można wykonać w dowolnym momencie.

Zalecamy użycie partii. Te opcje są dostępne podczas synchronizowania rezerwacji wydajności.

1. Wybieranie **Zarządzanie projektami i księgowanie** &gt; **Okresowe** &gt; **Synchronizacja pojemności** &gt; **Synchronizuj podsumowania pojemności zasobów**.
2. Ustaw opcje w poniższej tabeli.

    | Opcja      | Opis |
    |-------------|-------------|
    | Kod okresu | Opcjonalnie wybierz kod interwału dat księgi głównej, aby ustawić daty rozpoczęcia i zakończenia procesu synchronizacji dla zbiorczych pojemności zasobów. |
    | Data rozpoczęcia  | Wprowadź datę rozpoczęcia procesu synchronizacji dotyczącego zestawienia wydajności zasobów. |
    | Data zakończenia    | Wprowadź datę zakończenia procesu synchronizacji dotyczącego zestawienia wydajności zasobów. |

[![Proces synchronizacji.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]