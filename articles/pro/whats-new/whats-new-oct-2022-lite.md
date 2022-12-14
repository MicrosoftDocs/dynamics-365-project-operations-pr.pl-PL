---
title: Co nowego w październiku 2022 r. — Project Operations — wersja uproszczona
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z października 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations w wersji uproszczonej.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806644"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Co nowego w październiku 2022 r. — Project Operations — wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.57.0.176

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

| Obszar funkcji | Nazwa funkcji | Więcej informacji |
| --- | --- | --- |
| Planowanie i śledzenie projektu | **Zewnętrzne planowanie Project Operations**<br>Tryb planowania zewnętrznego pozwala klientom na natywne tworzenie, aktualizowanie i usuwanie encji powiązanych ze strukturami podziału pracy (WBS), używając natywnych interfejsów API Dataverse, ale bez bieżących ograniczeń wymuszanych przez program Project for the Web. | [Planowanie zewnętrzne](/dynamics365/project-operations/project-management/external-scheduling) |
| Wdrażanie i konfiguracja | <p>**Zezwalaj klientom na wybieranie typu wdrożenia**<br>Aktualizacje (PDU) oparte na produktach używane w Project Operations są używane do automatycznego instalowania rozwiązania podwójnego zapisu Project Operations, gdy rdzeń podwójnego zapisu i rozwiązania orkiestracji są zainstalowane w środowisku.</p><p>Ta funkcja wprowadza nowy parametr **Zachowania aktualizacji rozwiązania** w parametrach projektu. Gdy ten parametr jest ustawiona na **Tylko wersja uproszczona**, PUD oparte na produktach używane w Project Operations są używane do automatycznego instalowania rozwiązania podwójnego zapisu Project Operations, nawet jeśli rdzeń podwójnego zapisu i rozwiązania orkiestracji są zainstalowane w środowisku. Z tego zachowania korzystają klienci, którzy planują używanie rozwiązań podwójnego zapisu do integrowania zamówień sprzedaży z aplikacjami finansowymi i operacyjnymi, ale chcą używać Project Operations w trybie uproszczonym (czyli bez integracji z aplikacjami finansowymi i operacyjnymi).</p> | |

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Rozliczenia i ceny | 2316317 | System umożliwia tworzenie faktur, które nie są transakcjami płatnymi. |
| Rozliczenia i ceny | 2737300 | Przed dostępem do formularza można sprawdzić dostępność pola Klient. |
| Rozliczenia i ceny | 2744948 | Dodaj sprawdzanie null dla metody rozliczania. |
| Rozliczenia i ceny | 2763515 | W przypadku braku kontraktu sprzedaży faktury jest obsługiwany błąd odwołania null. |
| Rozliczenia i ceny | 2844301 | Utworzenie faktury partii kończy się niepowodzeniem z powodu błędu. |
| Rozliczenia i ceny | 2845869 | Niepoprawny magazyn usługi organizacji. |
| Rozliczenia i ceny | 2853729 | Szczegóły roli i ceny są aktualizowane po modyfikacji typu rozliczania. |
| Rozliczenia i ceny | 2940350 | Podczas wyceniania wartości rzeczywistych należy automatycznie wprowadzać tylko aktywne cenniki. |
| Wdrażanie i konfiguracja | 3001206 | Encja msdyn\_replaylogheader uniemożliwia uaktualnienie organizacji klientów. |
| Zarządzanie szansami sprzedaży | 2755582 | Wyjątki odwołania null obsługiwane z pomocy reguły podziału rozliczeń. |
| Zarządzanie szansami sprzedaży | 2761477 | Po użyciu podziału rozliczenia usunięcie punktu kontrolnego (nagłówka) pozostawia oddzielone punkty kontrolne. |
| Zarządzanie szansami sprzedaży | 2767595 | Po otwarciu rekordu zużycia materiałów w formularzu głównym zasób dostępny do rezerwacji dla rekordu zostanie zmieniony na właśnie zalogowanego użytkownika. |
| Planowanie i śledzenie projektu | 2790384 | Limit czasu oczekującej OperationSet jest zbyt krótki. |
| Zarządzanie zasobami | 2751560 | Niespójne preferowane jednostki organizacji w wymaganiach zasobów. |
| Podwykonawstwo | 2907231 | Etapu procesu faktury od dostawcy nie można kontynuować. |
| Czas i wydatek | 2867363 | Rekordy nie są ujmowane w widoku Nieobecności/Urlopy w celu zatwierdzenia, gdy są kolejkowane do zatwierdzenia. |
| Czas i wydatek | 2894405 | TESA: nieużywany katalog POC powoduje problemy ze zgodnością. |
