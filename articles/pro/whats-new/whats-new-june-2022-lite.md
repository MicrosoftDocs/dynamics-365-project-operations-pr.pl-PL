---
title: Co nowego w czerwcu 2022 r. — wdrażanie wersji uproszczonej aplikacji Project Operations
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z czerwca 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations lite.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959444"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Co nowego w czerwcu 2022 r. — wdrażanie wersji uproszczonej aplikacji Project Operations

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.43.0.77

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Podwykonawstwo | 2708885 | Poprawiono komunikat o błędzie wyświetlany podczas tworzenia przez użytkownika rekordu nagłówka rezerwacji zasobu do zarezerwowania, w którym wypełniono danych takiego rekordu. |
| Planowanie i śledzenie projektu | 2629441 | Poprawiono logikę wyzwalania przepływu pracy, aby zapobiec nieskończonej pętli podczas aktualizowania zadań projektu. |
| Czas i wydatek | 2641209 | Importy czasu z przypisań/rezerwacji muszą zachowywać odwołanie do zasobów, które można zarezerwować. |
| Planowanie i śledzenie projektu | 2651148 | Nagłówek dokumentu projektu musi być chroniony.|
| Planowanie i śledzenie projektu | 2653145 | Dodano walidacje, aby upewnić się, że nie można utworzyć rekordu projektu z nieprawidłowymi znakami w nazwie. |
| Czas i wydatek | 2654710 | Poprawiono filtrowanie na stronie **Zatwierdzenia**. |
| Rozliczenia i ceny | 2667805 | Dodano walidacje ułatwiające zapobieganie tworzeniu wartości rzeczywistych sprzedaży rozliczonej, jeśli nie istnieją kopie wartości rzeczywistych sprzedaży nierozliczonej. |
| Rozliczenia i ceny | 2668378 | Dodano walidacje uniemożliwiające dodanie niestandardowego wymiaru cen, o ile nie zostanie podana nazwa logiczna i nazwa pola. |
| Czas i wydatek | 2700428 | Poprawiono logikę zatwierdzeń, aby upewnić się, że inne zestawy zatwierdzeń dla projektu mogą być przetwarzane nawet w przypadku, gdy jeden z zestawów zatwierdzeń został zablokowany w obrębie zadań systemowych. |
