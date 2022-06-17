---
title: Co nowego w czerwcu 2021 r. — wdrażanie wersji uproszczonej aplikacji Project Operations
description: Ten artykuł zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations — wersja uproszczona w czerwcu 2021 r.
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 16fffb06ebb72ac25982374bff27a015eccfae1b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913955"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>Co nowego w czerwcu 2021 r. — wdrażanie wersji uproszczonej aplikacji Project Operations

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.11.0.156 lub 4.11.0.164.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2281417 | Rozwiązano problem dotyczący niepowodzenia akcji automatycznego tworzenia faktury w harmonogramie faktur. |
| Rozliczenia i ceny | 2287835 |   Lepsza wydajność potwierdzenia faktury. |
| Zarządzanie szansami sprzedaży | 2222555 | Możliwość obciążania wartości szacunkowych materiałów trzeba poprawnie skopiować do szczegółów wierszy oferty w przypadku używania opcji **Importuj z szacowania projektu**. |
| Zarządzanie szansami sprzedaży | 2223427 | Dostosowania są teraz dozwolone w ramach akcji **GenerateRetainersFromRetainerScheduleOptions**. |
| Zarządzanie szansami sprzedaży | 2277528 | Obliczanie stałych wartości kamieni milowych rozliczania dla wierszy kontraktu projektu z wieloma klientami. |
| Planowanie i śledzenie projektu | 2226110 | Rozwiązano sporadyczny problem z funkcję **generowania wymagań** w siatce **zespołu projektu**. |
| Planowanie i śledzenie projektu | 2208109 | Użytkownicy nie mogą tworzyć projektu w jednej walucie z zadaniami pokrewnymi w innej walucie. |
| Planowanie i śledzenie projektu | 2258228 | Lista pól, które można modyfikować za pomocą encji **Planowanie** przy użyciu interfejsu API harmonogramu planowania, została zaktualizowana. |
| Planowanie i śledzenie projektu | 2293989 | Do siatki **Zadania projektu** muszą być przekazywane odpowiednie ustawienia językowe i regionalne.|
| Zarządzanie zasobami | 2220493 | Poprawiono sposób pracy w siatce **Zadanie** podczas szybkiego oznaczania żądania zasobu jako zakończonego. |
| Zarządzanie zasobami | 2330496 | Rozwiązano problem z ładowaniem **tablicy harmonogramu**. (Aktualizacja jakości jest dostępna w wersji 4.11.0.164) |
| Czas i wydatek | 2194431 | Siatka **wprowadzania czasu** musi uznawać początek tygodnia zgodnie z **ustawieniami systemowymi**. |
| Czas i wydatek | 2277311 | Po usunięciu wartości w komórce w siatce **wprowadzania czasu** kursor pozostaje w siatce. |
