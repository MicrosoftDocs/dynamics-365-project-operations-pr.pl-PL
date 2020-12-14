---
title: Omówienie wykorzystania zasobów
description: W tym temacie zamieszczono informacje dotyczące widoku wykorzystania zasobów w Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401389"
---
# <a name="resource-utilization-overview"></a>Omówienie wykorzystania zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Zasoby mogą mieć docelowe wykorzystanie podlegające rozliczeniu. To docelowe wykorzystanie jest zdefiniowane jako atrybut w domyślnej roli zasobu albo ustawione w rekordzie konkretnego zasobu możliwego do zarezerwowania. Obliczenia wykorzystania bazują na rzeczywistej liczbie godzin zaraportowanej przez zasoby przy użyciu zatwierdzonych wpisów czasu.

Poniższe wzory służą do obliczania wykorzystania:

  - Wykorzystanie podlegające rozliczeniu = odpłatne rzeczywiste godziny pracy ÷ dyspozycyjność zasobu
  - Wykorzystanie niepodlegające rozliczeniu = rzeczywisty czas o identyfikatorze typu rozliczania = nieodpłatne, uzupełniające lub niedostępne ÷ dyspozycyjność zasobu
  - Wewnętrzne = rzeczywisty czas bez kontraktu sprzedaży ÷ dyspozycyjności zasobu
  - Dyspozycyjności zasobu = godziny pracy zasobu – poza biurem — dni wolne od pracy

Widok **Wykorzystanie zasobów** jest dostępny z poziomu okienka **Zasoby**.

Każda komórka w siatce reprezentuje procent wykorzystania zasobu podlegający rozliczeniu w okresie, takim jak dzień, tydzień lub miesiąc. Poniższe wzory służą do kolorowania komórek:

  - **Zielony**: Wykorzystanie do rozliczenia >= docelowe wykorzystanie zasobów
  - **Żółty**: Docelowe wykorzystanie - 20 <= Wykorzystanie do rozliczenia < Docelowe wykorzystanie
  - **Czerwony**: Wykorzystanie do rozliczenia < Docelowe wykorzystanie - 20

Ponieważ widok **Wykorzystanie zasobów** jest oparty na tablicy harmonogramu, można używać funkcji filtrowania dostępnych w tablicy harmonogramu do filtrowania wyników.

Siatka wymaga skonfigurowania docelowego wykorzystania dla roli lub konkretnego zasobu. Aby wykonać te czynności konfiguracyjne, wybierz kolejno opcje **Zasoby** > **Role zasobu**.

Ponadto każdemu zasobowi możliwemu do zarezerwowania musi być przypisana rola domyślna. Wybierz kolejno opcje **Zasoby** > **Zasoby**. Na karcie **Project Service** sprawdź, czy została zdefiniowana rola zasobu, a pole **Jest domyślna** ma ustawioną wartość **Tak**. Można dodać kolejne role, w których **Jest domyślna** = **Nie**. Rola z atrybutem **Jest domyślna** = **Tak** jest używana do oceny wykorzystania zasobu w stosunku do wartości docelowej dla tej roli.

Na karcie **Project Service** można również skonfigurować konkretne docelowe wykorzystanie zasobu. Następnie aparat obliczania wykorzystania na podstawie docelowego wykorzystania ocenia wartość docelową dla zasobu, a nie dla jego domyślnej roli.

Wykorzystanie jest pokazywane dla zasobu tylko w przypadku, gdy zasób ma zatwierdzony czas odpłatny w okresie wyświetlanym w siatce.