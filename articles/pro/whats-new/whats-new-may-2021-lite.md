---
title: Co nowego w maju 2021 r. — wdrażanie wersji uproszczonej Project Operations
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w wersji uproszczonej Project Operations z maja 2021 r.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 854a8c2290281b4d11a045321a334d8866806041
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583781"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Co nowego w maju 2021 r. — wdrażanie wersji uproszczonej Project Operations

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:

   - Project Operations w środowisku Dataverse w wersji 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

To wydanie zawiera następujące funkcje:

- [Tryby planowania](../../project-management/scheduling-modes.md): Kierownicy projektów mogą zdefiniować, czy projekt powinien być zarządzany w trybie harmonogramu stałego czasu trwania, stałej pracy lub stałych jednostek.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Rozliczenia i ceny | 2224568 | Dodano logikę umożliwiającą dostosowania, które obejmują wywoływanie wtyczki potwierdzającej fakturę. |
| Rozliczenia i ceny | 2101098 | Poprawiono logikę domyślnych pól do faktury proforma. Są to między innymi pola: **Adres-faktury**, **Nazwa na fakturze** i **Terminy płatności**. Pola są teraz domyślnie ustawione na podstawie odpowiedniego rekordu klienta umowy projektowej. |
| Rozliczenia i ceny | 2021413 | Zaktualizowanie pól **Koszt rzeczywisty** i **Sprzedaż** w encji **Zadanie** w celu dołączyć do zadań wartości sprzedaży z nierozliczonych i rozliczonych kosztów. |
| Rozliczenia i ceny | 2182110 | Podczas kopiowania kontraktu dotyczącego projektu identyfikator wiersza kontraktu jest ponownie generowany w docelowej umowie dotyczącej projektu, aby zapewnić jego unikalność. |
| Zarządzanie szansami sprzedaży | 2186741 | Dodano sprawdzanie poprawności, aby upewnić się, że nie można zaktualizować pola **Pochodzenia** i Typu transakcji na istniejących szczegółach wiersza oferty. |
| Zarządzanie szansami sprzedaży | 2191353 | Nie można pozwolić na tworzenie punktów kontrolnych dla czasowej i istotnej linii kontraktu. |
| Zarządzanie szansami sprzedaży | 2216956 | Rozwiązane problemy dotyczące **Aktualizowania cen**. |
| Planowanie i śledzenie | 2182979 | Udoskonalono funkcję kopiowania projektu, aby zapewnić kopiowanie wierszy kosztorysu z oryginalnego projektu. |
| Planowanie i śledzenie | 2184144 | Udoskonalono funkcję kopiowania projektu, aby zapewnić kopiowanie nazwy pozycji zasobu z oryginalnego projektu. |
| Planowanie i śledzenie | 2184799 | Zaostrzono kontrolę podczas kopiowania projektu, aby nie można było zmienić szacowanej daty rozpoczęcia podczas kopiowania. |
| Planowanie i śledzenie | 2185134 | Szacunkowa data rozpoczęcia projektu docelowego podczas kopiowania projektu to dzisiejsza data. |
| Planowanie i śledzenie | 2196373 | Upewnij się, że rekordy kierownika projektu i członków zespołu nie są powielane w zespole projektowym podczas kopiowania projektu. |
| Planowanie i śledzenie | 2211833 | Przydziały zasobów są kopiowane ze źródłowego zadania projektu podczas kopiowania do projektu docelowego. |
| Planowanie i śledzenie | 2186541 | Rozwiązane problemy w siatce **Szacowanie** podczas grupowania według **zasobu**. |
| Planowanie i śledzenie | 2166906 | Kategoria transakcji z zadania musi być skopiowana do encji **Przypisanie zasobów**. |
| Zarządzanie zasobami | 2125362 | Rozwiązano problemy z tworzeniem ogólnego członka zespołu przy użyciu metody alokacji opartej na godzinach. |
| Czas i wydatek | 2113603 | Naprawiono problem związany z dostosowywaniem, polegający na usuwaniu atrybutów ze strony **Wpis czasu**. System sprawdza teraz, czy atrybut istnieje na stronie przed uzyskaniem do niego dostępu za pomocą skryptu. |
| Czas i wydatek | 2204377 | Skopiowane arkusze czasu muszą być wyświetlane automatycznie po wybraniu **Kopiuj tydzień**. |
| Czas i wydatek | 2209059 | Pole **Stan** można edytować dla wpisów czasu Dynamics 365 Field Service. |
