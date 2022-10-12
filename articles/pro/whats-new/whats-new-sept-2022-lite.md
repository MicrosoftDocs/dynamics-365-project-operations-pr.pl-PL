---
title: Co nowego we wrześniu 2022 r. — Project Operations — wersja uproszczona
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z września 2022 r. wdrożenia wersji uproszczonej Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621295"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Co nowego we wrześniu 2022 r. — Project Operations — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.46.0.60

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

| Obszar funkcji | Nazwa funkcji | Więcej informacji |
| --- | --- | --- |
| Zarządzanie szansami sprzedaży | **Poprawki i aktywacja ofert**<br>Project Operations zapewnia pełną pomoc w procesie sprzedaży. Oferty projektu można aktywować w celu reprezentowania stanu, w którym oferta jest tylko do odczytu i jest przeglądana. Aktywowane oferty można poprawić, aby tworzyć nowe oferty z przyrostem numeru poprawki. Aktywowane oferty projektu lub poprawki ofert można zamknąć jako wykorzystane lub utracone. | [Aktywowanie i poprawianie oferty projektu](/dynamics365/project-operations/sales/activation-and-revision) |
| Rozliczenia i ceny | **Domyślne ceny niezależne od strefy czasowej**<br>W programie Project Operations we wszystkich wartościach rzeczywistych projektu wprowadzono pojęcie daty strefy czasowej. Nowe pole o wartościach **Data transakcji** jest teraz dostępne w wierszach i wartościach rzeczywistych i będzie używane do przechowywania daty wystąpienia transakcji, ale bez konwertowania tej daty na Uniwersalny czas koordynowany. Ta data będzie używana w procesach, takich jak domyślne ceny i tworzenie faktury. | <p>[Określanie stawek kosztów dla oszacowań i wartości rzeczywistych projektu](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Określanie kosztów sprzedaży dla oszacowań i wartości rzeczywistych projektu](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Rozliczenia i ceny | **Zastępowanie cen z datą wejścia w życie w Project Operations**<br>Zastąpienia ceny z datą wejścia w życie stanowi sposób zastępowania lub zmieniania określonych cen w cenniku. | [Zastąpienia ceny z datą wejścia w życie](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Czas i wydatek | **Globalna osoba zatwierdzająca**<br>Funkcja ta włącza niezależnych dostawców oprogramowania (ISV) i scentralizowane zatwierdzanie, niezależnie od stanu członków projektu lub zespołu w projekcie. | [Zabezpieczenia i zatwierdzenia](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2754422 | Szacowanie materiałów i wydatków nie jest przepływem do usługi Dynamics 365 Finance podczas kopiowania projektów w programie Dataverse. |
| Czas i wydatek | 2787409 | Nieprawidłowa osoba zatwierdzająca może zatwierdzić wpis niezwiązany z projektem. |
| Zarządzanie szansami sprzedaży | 2788907 | Zaktualizowany komunikat o błędzie informujący o sprawdzaniu poprawności unikatowości wierszy zamówienia, które zawierają flagi. |
| Czas i wydatek | 2842253 | Obsługa wyjątków null dla zatwierdzania czasu. |
| Rozliczenia i ceny | 2844181 | Niepowodzenie uzyskania identyfikatorów korelacji blokuje tworzenie faktur. |
| Rozliczenia i ceny | 2876628 | QLD, CLD — rozwiązanie cennika szacowanego powinno używać starszych pól z zakresu dat cennika. |
| Podwykonawstwo | 2893222 | Jeśli dla wiersza podumowy nie zostanie podana żadna rola, należy wybrać ten wiersz w członkach zespołu dla dowolnej roli. |
