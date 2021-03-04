---
title: Co nowego w grudniu 2020 r. — Wdrażanie w wersji uproszczonej Project Operations — od okazji do faktury pro forma
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w uproszczonym wdrożeniu Project Operations Lite z grudnia 2020 r. — od okazji do faktury proforma.
author: sigitac
manager: Annbe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bfa13ab74031eb52c128fed16a31e3a8167e8bde
ms.sourcegitcommit: ec8ab099a03725de9f61edfdeb90fbefae54cd4e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/09/2020
ms.locfileid: "4707686"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Co nowego w grudniu 2020 r. — Wdrażanie w wersji uproszczonej Project Operations — od okazji do faktury pro forma

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.5.0.134 

W poniższej tabeli wymieniono aktualizacje aplikacji Project Operations w środowisku usługi Dataverse w wersji 4.5.0.134.

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 1986009 | Ręcznie utworzone wiersze arkusza mają niespójną wydajność, jeśli zostały potwierdzone przed połączeniem lub odłączeniem projektu od pozycji kontraktu. |
| Rozliczenia i ceny | 2014153 | Produkty nie są fakturowane, jeśli są wykonywane z poziomu harmonogramu faktur. |
| Rozliczenia i ceny | 2014159 | Produkty nie są ściągane, kiedy faktura jest odświeżana na potrzeby transakcji. |
| Rozliczenia i ceny | 2028174 | Aktualizacje szczegółów wiersza faktury powinny być zgodne z logiką arkusza korekt. |
| Rozliczenia i ceny | 2028315 | Poprawki zachowania edytowalnej siatki zagnieżdżonej. |
| Rozliczenia i ceny | 2031070 | Korygowanie szczegółów wiersza faktury korygującej musi być zgodne z logiką arkusza korekt. |
| Rozliczenia i ceny | 2034186 | Aktualizacja projektu w pozycji kontraktu musi być możliwa. |
| Rozliczenia i ceny | 2034206 | Podczas wycofywania wartości rzeczywistej w trakcie odłączania projektu od pozycji kontraktu musi być ustawiony stan korekty. |
| Rozliczenia i ceny | 2040871 | Zezwalanie na aktualizacje komórek jednostki i grupy jednostek w ramach siatki szacowań wydatków. |
| Rozliczenia i ceny | 2053754 | Wartości rzeczywiste utworzone na podstawie edytowanych faktur nie są oznaczane przy użyciu stanu korekty oraz stanu fakturowania. |
| Rozliczenia i ceny | 2057874 | Poprawianie połączenia transakcji utworzonego podczas edycji szczegółów wiersza faktury. |
| Rozliczenia i ceny | 2057875 | Poprawianie źródeł transakcji utworzonych podczas edycji szczegółów wiersza faktury. |
| Rozliczenia i ceny | 2057944 | Stan nieprzekraczalnego limitu ustawiony jako zatwierdzony dla wartości rzeczywistych, które nie są gotowe do fakturowania przy korekcie na fakturze. |
| Rozliczenia i ceny | 2057963 | Oddzielono uprawnienie Create\_Product od uprawnienia Create\_ProjectContract. |
| Rozliczenia i ceny | 2067622 | Podczas generowania punktów kontrolnych powinna zostać wyświetlona ikona przetwarzania. |
| Rozliczenia i ceny | 2067624 | W przypadku generowania punktów kontrolnych zakontraktowana kwota powinna zostać oznaczona jako zalecana ze względów biznesowych. |
| Rozliczenia i ceny | 2086880 | Ukrywanie przycisku **Sugestia** na wstążce dla wierszy oferty opartej na projektach. |
| Wdrażanie i konfiguracja | 2101152 | Nowe środowisko utworzone przy użyciu szablonu Project Operations z centrum administracyjnego Power Platform musi mieć wykonane operacje po instalacji. |
|   Zarządzanie szansami sprzedaży | 2022204 | Siatka fakturowania oparta na projektach na karcie **Fakturowanie zadań** na stronie **Projekt** powinna ukrywać siatkę opartą na projekcie, jeśli nie ma pozycji oferty/kontrakty z opcją **Wszystkie zadania** i na odwrót. |
|   Zarządzanie szansami sprzedaży | 2086601 | Dezaktywowane role i kategorie nie powinny być kopiowane do ról Odpłatne i listy kategorii odpłatnych w wierszach oferty i pozycjach kontraktu. |
| Planowanie i śledzenie projektu | 1949065 | Widoczność danych działa poprawnie przy powiększeniu 200% |
| Planowanie i śledzenie projektu | 2046317 | Możliwość zmiany nazwy encji projektu w aplikacji Project Operations |
| Planowanie i śledzenie projektu | 2057171 | Zaktualizowany komunikat o błędzie, gdy pole **Data rozpoczęcia projektu** na stronie **Projekt** jest puste. |
| Planowanie i śledzenie projektu | 2057197 | Kopiowanie wiersza oszacowania za pomocą odwołania do zadania nie jest obsługiwane. |
| Planowanie i śledzenie projektu | 2060687 | Ostrzeżenie dotyczące strefy czasowej będzie teraz znikać po określonym czasie trwania. |
| Zarządzanie zasobami | 1832887 | Aby można było ładować powtarzalne dane dla środowisk usług Dataverse i Finance, domyślny identyfikator kategorii zasobów musi być statyczny. |
| Czas i wydatek | 2034882 | Przycisk **Nowy** jest wyświetlany dwukrotnie na pasku poleceń w przypadku wpisów czasu po zainstalowaniu aplikacji Dynamics 365 Field Service. |
| Czas i wydatek | 2056028 | Aktualizacja strony **edytowania czasu** w celu dołączenia osi czasu. |
| Czas i wydatek | 1983747 | Na wykresie wpisów czasu są wyświetlane dodatkowe dane. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]