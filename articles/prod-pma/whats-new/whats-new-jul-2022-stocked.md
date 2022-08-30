---
title: Co nowego lub co się zmieniło w aplikacji Project Operations w lipcu 2022 r. dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne
description: Ten artykuł zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z lipca 2022 r. wdrożenia Microsoft Dynamics 365 Project Operations dla scenariuszy opartych na zasobach/produkcji.
author: ramagadu
ms.date: 8/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b1dc72f164202835a994935e479bca1ab23b7682
ms.sourcegitcommit: 6be13fc3d7e61a8f95ed200f418314135c7e5c2b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/17/2022
ms.locfileid: "9305929"
---
# <a name="whats-new-or-changed-in-project-operations-july-2022-for-stockedproduction-based-scenarios"></a>Co nowego lub co się zmieniło w aplikacji Project Operations w lipcu 2022 r. dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne

_**Dotyczy:** Project Operations dla scenariuszy obejmujących magazynowanie/zlecenia produkcyjne_

Ten artykuł dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Zarządzanie projektami i księgowość w środowisku Dynamics 365 Finance w wersji 10.0.28

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

Aby uzyskać informacje dotyczące poprawek usterek zawartych w tej aktualizacji, należy zalogować się do Microsoft Dynamics Lifecycle Services (LCS) i wyświetlić [artykuł z bazy wiedzy](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcje włączone domyślnie w nadchodzącym wydaniu

Poniższa tabela zawiera listę funkcji, które są domyślnie włączone w wersji 10.0.29. Większość funkcji, które zostały włączone, można wyłączyć w [zarządzaniu funkcjami](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). W przyszłości niektóre funkcje, które zostały automatycznie włączone, mogą zostać usunięte z zarządzania funkcjami i stać się obowiązkowe. Zmiana ta zapewnia, że klienci korzystają z aktualnych funkcji, dzięki czemu ulepszenia mogą opierać się na aktualnych funkcjach w miarę ich dodawania. Funkcje nigdy nie będą automatycznie włączane w okresie krótszym niż jeden rok, chyba że zostaną uznane za istotne.

| Nazwa funkcji | Włącz dane | Funkcja dodana | Stan funkcji | Moduł |
| --- | --- | --- |--- |--- |
| Umożliwienie korekty transakcji godzinowej w oparciu o zmianę alokacji zasady finansowania | 16 Wrzesień 2022 | 7 października 2020 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Funkcja cofnięcia faktury za zamówienie przedpłatowe projektu | 16 Wrzesień 2022 | 6 października 2021 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Usuń linie propozycji faktury podczas korzystania z programu Project Operations dla scenariuszy opartych na zasobach / brakach zasobów | 16 Wrzesień 2022 | 6 października 2021 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Dostosuj księgowość zaksięgowanej transakcji projektu | 16 Wrzesień 2022 | 10 maja 2020 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włączanie domyślnej konfiguracji księgowej projektu | 16 Wrzesień 2022 | 19 lutego 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włączanie wielu pozycji kontraktu dla projektu | 16 Wrzesień 2022 | 29 czerwca 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Ustaw godzinę projektu tylko do odczytu, jeśli bieżący stan zatwierdzania nie umożliwia edycji | 16 Wrzesień 2022 | 6 października 2021 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włącz synchronizację wierszy sprzedaży z wierszami zakupu, gdy wiersze zakupu są aktualizowane i parametr zarządzania zmianami zamówień zakupu jest włączony | 16 Wrzesień 2022 | 7 października 2020 | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Włączanie Project Operations w u klientach usługi Dynamics 365 Customer Engagement | 16 Wrzesień 2022 | 29 czerwca 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |
| Funkcja poprawiania błędów w transakcjach projektów | 16 Wrzesień 2022 | 13 lipca 2020 roku | Domyślnie włączona | Zarządzanie projektami i księgowanie |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcje, które w nadchodzącym wydaniu staną się obowiązkowe

W poniższej tabeli wymieniono funkcje, które są obowiązkowe od wersji 10.0.29 i nowszych.

| Nazwa funkcji | Włącz dane | Funkcja dodana | Stan funkcji | Moduł |
| --- | --- | --- | --- | --- |
| Obliczanie wartości zatwierdzonej w źródle danych bez zaokrąglania kursu wymiany | 16 Wrzesień 2022 | 14 czerwca 2020 roku | Obowiązkowy | Zarządzanie projektami i księgowanie |
| Włącz księgowanie korekt projektu na tym samym koncie księgowym, co pierwotna transakcja | 16 Wrzesień 2022 | 14 czerwca 2020 roku | Obowiązkowy | Zarządzanie projektami i księgowanie |
| Szczegóły kwoty zatwierdzonego kontraktu projektu | 16 Wrzesień 2022 | Sierpień 31, 2019 | Obowiązkowy | Zarządzanie projektami i księgowanie |
| Włączanie sortowania według zasobów podczas tworzenia propozycji sprzedaży na fakturze projektu | 16 Wrzesień 2022 | Sierpień 31, 2019 | Obowiązkowy | Zarządzanie projektami i księgowanie |
