---
title: Co nowego w kwietniu 2021 r. — wdrażanie wersji uproszczonej Project Operations
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w wersji uproszczonej Project Operations z kwietnia 2021 r.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009409"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Co nowego w kwietniu 2021 r. — wdrażanie wersji uproszczonej Project Operations

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

  - Project Operations w środowisku Dataverse w wersji 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- Materiały niezabędowe do projektów. Kluczowe możliwości to:
  - Kalkulacji i kalkulacji cen materiałów niezabędowych w cyklu sprzedaży projektu. Więcej informacji można znaleźć w: [Konfigurowanie kosztów i stawek sprzedaży dla katalogu produktów — wersja uproszczona](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Śledzenie wykorzystania materiałów niezamagazynowanych podczas realizacji projektu. Aby uzyskać więcej informacji, zobacz [Rejestrowanie użycia materiałów w projektach i zadaniach projektów](../../material/material-usage-log.md).
  - Fakturowanie kosztów materiałów niezamagazynowanych. Aby uzyskać więcej informacji, zobacz [Zarządzanie zaległością rozliczenia — wersja uproszczona](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Nowe interfejsy API w Dynamics 365 Dataverse umożliwiają tworzenie, aktualizowanie i usuwanie operacji za pomocą **Encji planowania**. Aby uzyskać więcej informacji, zobacz [Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2224568 | Dodano logikę umożliwiającą dostosowania, które obejmują wywoływanie wtyczki potwierdzającej fakturę. |
| Rozliczenia i ceny | 2101098 | Ulepszono logikę domyślnych pól faktury proforma: **Adres rozliczeniowy**, **Nazwa płatnika** i **Warunki płatności** są teraz domyślnie ustawione w odpowiednim rekordzie klienta umowy projektu. |
| Rozliczenia i ceny | 2021413 | Zaktualizowanie pól **Koszt rzeczywisty** i **Sprzedaż** w encji **Zadanie** w celu dołączyć do zadań wartości sprzedaży z nierozliczonych i rozliczonych kosztów. |
| Rozliczenia i ceny | 2182110 | Podczas kopiowania kontraktu dotyczącego projektu identyfikator wiersza kontraktu jest ponownie generowany w docelowej umowie dotyczącej projektu, aby zapewnić jego unikalność. |
| Zarządzanie szansami sprzedaży | 2186741 | Dodano sprawdzanie poprawności, aby upewnić się, że nie można zaktualizować pola **Pochodzenia** i **Typu transakcji** na istniejących szczegółach wiersza oferty. |
| Zarządzanie szansami sprzedaży | 2191353 | Nie można tworzyć punktów kontrolnych dla czasowej i istotnej linii kontraktu. |
| Zarządzanie szansami sprzedaży | 2216956 | Rozwiązane problemy dotyczące **Aktualizowania cen**. |
| Planowanie i śledzenie | 2182979 | Udoskonalono funkcję kopiowania projektu, aby zapewnić kopiowanie wierszy kosztorysu z oryginalnego projektu. |
| Planowanie i śledzenie | 2184144 | Udoskonalono funkcję kopiowania projektu, aby zapewnić kopiowanie nazwy pozycji zasobu z oryginalnego projektu. |
| Planowanie i śledzenie | 2184799 | Kopia projektu: zaostrzono kontrolę, aby nie można było zmienić szacowanej daty rozpoczęcia podczas kopiowania. |
| Planowanie i śledzenie | 2185134 | Kopia projektu: Szacunkowa data rozpoczęcia projektu docelowego to dzisiejsza data. |
| Planowanie i śledzenie | 2196373 | Kopia projektu: upewnij się, że rekordy kierownika projektu i członka zespołu nie są zduplikowane w zespole projektowym. |
| Planowanie i śledzenie | 2211833 | Kopia projektu: przydziały zasobów są kopiowane ze źródłowego zadania projektu do projektu docelowego. |
| Planowanie i śledzenie | 2186541 | Rozwiązane problemy w siatce **Szacowanie** podczas grupowania według zasobu. |
| Planowanie i śledzenie | 2166906 | Kategoria transakcji z zadania musi być skopiowana do encji **Przypisanie zasobów**. |
| Zarządzanie zasobami | 2125362 | Rozwiązano problemy z tworzeniem ogólnego członka zespołu przy użyciu metody alokacji opartej na godzinach. |
| Czas i wydatek | 2113603 | Naprawiono problem związany z dostosowywaniem, polegający na usuwaniu atrybutów ze strony **Wpis czasu**. System sprawdza teraz, czy atrybut istnieje na stronie przed uzyskaniem do nich dostępu za pomocą skryptu. |
| Czas i wydatek | 2204377 | Skopiowane czaskopiki muszą być wyświetlane automatycznie po wybraniu opcji **Kopiuj tydzień** podczas wprowadzania czasu. |
| Czas i wydatek | 2209059 | Pole **Stan** można edytować dla wpisów czasu Dynamics 365 Field Service. |
