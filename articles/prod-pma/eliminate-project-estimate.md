---
title: Eliminowanie oszacowania projektu
description: W tym temacie zamieszczono informacje dotyczące eliminowania oszacowania projektu po jego zakończeniu.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684103"
---
# <a name="eliminate-a-project-estimate"></a>Eliminowanie oszacowania projektu

[!include [banner](../includes/banner.md)]

Szacowania projektu zapewniają widok finansowy dla prac oszacowanych i zaplanowanych dla projektu. Aby pracować z oszacowaniami projektu, należy załączyć projekt do projektu szacowanego. Projekt szacowany jest zawsze oparty na projekcie istniejącym, ale wiele projektów może odwoływać się do jednego projektu szacowanego. Do projektów szacowanych można dołączać tylko projekty o stałej cenie i projekty inwestycyjne, a te projekty muszą należeć do tej samej grupy projektów jak projekt szacowany.

W celu wyeliminowania projektu szacowanego należy go zakończyć. Poniższe kroki opisują sposób eliminacji oszacowania.

1. Przejdź do **Zarządzanie projektami i księgowanie** > **Wszystkie projekty** i wybierz projekt. 
2. Na karcie **Zarządzanie** wybierz pozycję **Oszacowania** i na stronie **Oszacowania** wybierz pozycję **Eliminuj**.
3. Na stronie **Eliminowanie oszacowania** na karcie **Ogólne** ustaw następujące opcje:

   - **Kod okresu**: należy wybrać kod okresu, aby wybrać odpowiednie szacowanie projektu. 
   - **Data szacowania**: należy wybrać datę oszacowania dotyczącą eliminacji.
   - **Usuń z ostrzeżeniami PWT**: Włącz tę opcję, aby zapewnić powiadamianie w przypadku wyeliminowania oszacowania skojarzonego z pracą w toku (PWT). Jeśli ta opcja nie jest włączona, eliminacja nie może być kontynuowana, jeśli istnieje nieoszacowana transakcja. 
   > [!NOTE]
   > Ta opcja jest dostępna tylko wtedy, gdy do projektu szacowanego zastosowano eliminację. Nie jest ona dostępna, jeśli używane jest księgowanie okresowe. To ustawienie działa z ustawieniami na karcie **Szacowanie** na stronie **Parametry projektu**, w grupie pól **Zezwalaj na eliminację, kiedy istnieją nieoszacowane transakcje**.
   - **Ustaw etap jako gotowy**: włącz tę opcję, aby ustawić etap projektu szacowanego na **Zakończony** po przeprowadzeniu eliminacji.
   - **Drukuj listę oszacowań**: służy do wybierania informacji, które mają być uwzględnione podczas drukowania listy oszacowań.
   - **Pokaż dziennik informacyjny**: włącz tę opcję, aby wyświetlić dziennik informacyjny.
   - **Data księgowania**: należy wybrać datę księgowania w rejestrze.

4.  Wybierz pozycję **OK**.
5. Po zakończeniu procesu eliminacji dla wyeliminowanego projektu szacowanego jest wyświetlany element o ujemnych wartościach. 

Jeśli nie zachodzi potrzeba wyeliminowania oszacowania, można wybrać wyeliminowaną wartość szacunkową i wybrać pozycję **Cofnij eliminację**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]