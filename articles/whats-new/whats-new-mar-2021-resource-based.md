---
title: 'Nowości: marzec 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów'
description: Ten artykuł zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations w marcu 2021 r. dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932953"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości: marzec 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.8.0.91 
- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.16 

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse


| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2133873 | Poprawiono wyświetlanie symbolu waluty **Ceny sprzedaży jednostkowej** w siatce **Szacowania wydatków**. |
| Rozliczenia i ceny | 2174616 | Po wygraniu oferty do niestandardowy cennik kontraktu odwołuje się do szczegółów pozycji kontraktu, które są kopiowane z oferty. |
| Zarządzanie szansami sprzedaży | 2167475 | Stała kwota podatku na fakturze korygującej, która pochodzi z nierozliczonych wpisów rzeczywistych. |
| Zarządzanie szansami sprzedaży | 2176285 | Kwota podatku nie może być kopiowana ze szczegółów umowy sprzedaży/wiersza oferty do szczegółów wiersza umowy/wiersza oferty kosztów. |
| Zarządzanie szansami sprzedaży | 2188079 | Reguła podzielonego fakturowania nie może być tworzona dla umów, które nie są oparte na pracy. |
| Planowanie i śledzenie | 2125274 | Atrybut **Mapowania podwójnego zapisu projektu** dla **Mapowania daty rozpoczęcia projektu** zaktualizowany z **msdyn\_taskearlieststart** do **msdyn\_actualstart**. |
| Planowanie i śledzenie | 2138853 | Funkcja kopiowania projektu zaktualizowana w celu zapewnienia, że wiersze szacowania wydatków, które odwołują się do zadań, są kopiowane do projektu docelowego. |
| Planowanie i śledzenie | 2154306 | Rozwiązane problemy z usuwaniem oszacowań wydatków w programie Project Operations dla scenariuszy opartych na zasobach. |
| Planowanie i śledzenie | 2173259 | Funkcja kopiowania projektu została zaktualizowana, aby upewnić się, że nie wyświetla komunikatu o błędzie **Kopiowanie SPP** w niektórych scenariuszach. |
| Czas i wydatek | 2148910 | Naprawiono problem z wyświetlaniem strony **Edytuj wpis** w siatce **Wpis czasu**. |
| Czas i wydatek | 2159798 | Zaostrzona kontrola w celu zapewnienia, że zatwierdzone wpisy wydatków nie mogą być edytowane. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance

Aby uzyskać więcej informacji, zobacz [Co nowego w styczniu 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Aktualizacje dotyczące regulacji

Aby uzyskać informacje na temat aktualizacji przepisów prawnych dotyczących aplikacji finansowych i operacyjnych, zobacz [Aktualizacje prawne](/dynamics365/finance/localizations/regulatory-updates). Innym sposobem uzyskania informacji o aktualizacjach regulacyjnych jest zalogowanie się do LCS i wyświetlenie planowanych aktualizacji prawnych za pomocą narzędzia do wyszukiwania problemów. Funkcja wyszukiwanie problemów umożliwia wyszukiwanie według kraju, typu funkcji oraz wydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]