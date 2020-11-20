---
title: Co nowego w listopadzie 2020 r. — Wdrażanie w wersji uproszczonej Project Operations Lite — od okazji do faktury pro forma
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w wydaniu Project Operations Lite z listopada 2020 r. - dotyczy fakturowania proforma.
author: sigitac
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa95406a27e6d32d2be75303904547b59f24c8b2
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367189"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Co nowego w listopadzie 2020 r. — Wdrażanie w wersji uproszczonej Project Operations Lite — od okazji do faktury pro forma

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W poniższej tabeli wymieniono aktualizacje operacji projektu w środowisku CDS w wersji 4.4.0.70.

| Obszar funkcji                 | Numer referencyjny | Aktualizacja dotycząca jakości                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Zarządzanie szansami sprzedaży       | 2036993          | Wiersze szacowania i wiersze kontraktu przydziału zasobów są aktualizowane w przypadku zwycięskich ofert, gdy typem wiersza oferty jest **Wszystkie zadania**.                                                 |
|   Zarządzanie szansami sprzedaży       | 2071514          | Nie może utworzyć faktury na punkt kontrolny stałej ceny dotyczący kontraktu, na którym włączono funkcję fakturowania opartego na zadaniach.                                                                          |
| Rozliczenia i ceny          | 2070392          | Pozycje kontraktu projektu na fakturze wzrastają po każdym wybraniu **Odśwież transakcje faktury**.                                                                       |
| Planowanie projektu             | 2043336          | Nie można usunąć rekordu członka zespołu projektu.                                                                                                                                    |
| Planowanie projektu             | 2046013          | Niespójne zachowanie dotyczące oszacowań kolumn znaczników podczas ładowania i przy zmianie typu fazy czasu.                                                                                   |
| Planowanie projektu             | 2046647          | Godziny rozpoczęcia i zakończenia są na godzinę wypadane w czasie, gdy wymagania dotyczące zasobów są generowane przez członków zespołu projektu.                                                                      |
| Planowanie projektu             | 2053879          | (Zgodnie z nadchodzącym wdrożeniem CDS) PublishUnassignedAssignments przerywa próbę zapisania zadania, gdy błąd „Wartość przekazana dla elementu ConditionOperator.In jest pusta”. |
| Planowanie projektu             | 2055501          | Pozostawienie pustej **Daty rozpoczęcia projektu** powoduje niepowodzenie w harmonogramie.                                                                                                      |
| Planowanie projektu             | 2066817          | Nie może utworzyć zasobu generycznego przy użyciu selektora osób na karcie **Zadania**.                                                                                               |
| Planowanie projektu             | 2067034          | Przycisk **Pokaż szczegóły** jest niedostępny na stronie **Szczegóły zadania**.                                                                                                         |
| Zarządzanie zasobami          | 2046667          | Członkowie zespołu generycznego nie są usuwani nawet po spełnieniu wszystkich zasobów.                                                                                                     |
| Czas i szybki wpis wydatków | 2047499          | Przycisk **Nowy** na stronie wprowadzania czasu otwiera stronę **Nowy podpis wiadomości e-mail**.                                                                                               |
| Czas i szybki wpis wydatków | 2059859          | Nieoczekiwane podręczne otwieranie podczas tworzenia wpisu wydatku.                                                                                                                         |
| Inny powód                        | 2044181          | [PO odinstalowania programu] — Podczas próby odinstalowania podstawowych rozwiązań   **msdyn_ProjectServiceCore_Patch** i msdyn Project service pojawia się błąd „Rekord jest niedostępny”.        |
