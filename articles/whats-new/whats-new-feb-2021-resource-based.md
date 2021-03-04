---
title: 'Nowości: luty 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów'
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w wersji Project Operations ze luty 2021 r. w scenariuszach dotyczących zasobów/braku zapasów.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141339"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nowości: luty 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse 4.7.0.95
- Zarządzanie projektami i ich księgowanie w wersji 10.0.16 środowiska Dynamics 365 Finance 

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

### <a name="project-operations-on-dataverse"></a>Project Operations w usłudze Dataverse

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| **Rozliczenia i ceny** | 2053736 | Szczegółowe informacje o wierszu faktury są teraz dostępne, przechodząc do **Faktura** > **Pokrewne informacje**. |
| **Rozliczenia i ceny** | 2122613 | Akcje **Aktywowanie** i **Dezaktywowanie** zostały usunięte z encji skojarzenia **Cennik**. |
| **Rozliczenia i ceny** | 2128606 | Rozwiązano problem **ullReferenceException** w dodatku plug-in **GetEferenceatesForProject**. |
| **Wdrażanie i konfiguracja** | 2139346 | Rozwiązano problem z importowaniem niezaimportowanego rozwiązania **Dynamics365ProjectOperationsDualWrite**. |
| **Wdrażanie i konfiguracja** | 2140569 | Rozwiązanie projektu nie może być zainstalowane w środowiskach Dataverse Teams. |
| **Wdrażanie i konfiguracja** | 2086991 | Ograniczone dostosowywanie lokalizacji zasobów sieci Web. |
| **Zarządzanie szansami sprzedaży** | 2136794 | Wyświetl poprawny komunikat o błędzie, gdy nie powiedzie się proces **Potwierdź fakturę** lub **Oznacz fakturę jako zapłaconą**. |
| **Zarządzanie szansami sprzedaży** | 2139330 | Zmiana menedżera projektu w projekcie nie może zresetować firmy, która jest właścicielem, do wartości domyślnej. |
| **Zarządzanie szansami sprzedaży** | 2146376 | Skorygowana kwota podatku w kwocie niepodlegającej obciążeniu jest tworzona z potwierdzenia faktury. |
| **Planowanie i śledzenie projektu** | 2099879 | Wdrożenie środowiska Dataverse musi utworzyć domyślną kategorię transakcji z identyfikatorem statycznym i nie może losowo wygenerować jednej kategorii dla każdego środowiska. |
| **Planowanie i śledzenie projektu** | 2128577 | Naprawiono uprawnienia użytkownika usługi Project Service, aby zaktualizować kategorię transakcji w przypisaniu zasobu. |
| **Planowanie i śledzenie projektu** | 2164035 | Rozwiązano problemy z funkcją **Kopiowanie projektu**. |
| **Wpis czasu** | 2129161 | Stosuje się bardziej ścisłe ograniczenia, aby zagwarantować, że użytkownicy nie mogą zmienić ani zaktualizować wpisu czasu przesłanego lub zatwierdzonego. |
| **Wpis czasu** | 2103572 | Zatwierdzenie przez czas wpisów czasu, które nie dotyczącą projektu, nie może być szukane przez rolę osoby zatwierdzającej projekt. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Omówienie zarządzania projektami i księgowania w Dynamics 365 Finance 

Aby uzyskać więcej informacji o zarządzaniu projektami i księgowością w Dynamics 365 Finance, zobacz [Nowości: styczeń 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Aktualizacje dotyczące regulacji

Aby uzyskać więcej informacji na temat aktualizacji dotyczących aplikacji Finance and Operations, zobacz artykuł dotyczący [Aktualizacje dotyczące regulacji](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Innym sposobem uzyskania informacji o aktualizacjach regulacyjnych jest zalogowanie się do Lifecycle Services (LCS) i wyświetlenie planowanych aktualizacji prawnych za pomocą narzędzia do wyszukiwania problemów. Funkcja wyszukiwanie problemów umożliwia wyszukiwanie według kraju, typu funkcji oraz wydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]