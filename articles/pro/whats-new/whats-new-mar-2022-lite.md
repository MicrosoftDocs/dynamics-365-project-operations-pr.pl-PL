---
title: Co nowego w marcu 2022 r. — uproszczone wdrożenie Project Operations
description: Ten temat zawiera informacje o aktualizacjach jakości, które są dostępne w wydaniu z marca 2022 r. wdrożenia Project Operations lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583763"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Co nowego w marcu 2022 r. — uproszczone wdrożenie Project Operations

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten temat dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.30.0.99

## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

- Podwykonawca: tworzenie i dopasowywanie faktur dostawcy

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| Obszar funkcji | Numer referencyjny | Aktualizacja dotycząca jakości |
| --- | --- | --- |
| Czas i wydatek | 2388011 | Pokazywać komentarze dotyczące przesyłania informacji o czasie podczas zatwierdzania zbiorczego. |
| Planowanie i śledzenie projektu | 2495294 | Szczegółów projektu nie można edytować na stronie **Szczegóły zadania**. |
| Rozliczenia i ceny | 2499605 | Punkty kontrolny kontraktu utworzone na podstawie punktów kontrolnych oferty są niepoprawnie oznaczane jako tylko do odczytu. |
| Planowanie i śledzenie projektu | 2506050 | Zestaw operacji pozostaje oczekujący na jedną godzinę, jeśli nie ma możliwości zapisania zmiany. Następnie zestaw jest fałszowany oznaczony jako **Niepowodzenie**, podczas gdy powinien zostać ukończony natychmiast. |
| Rozliczenia i ceny | 2507401 | Domyślne jednostki kontraktów są niepoprawnie wprowadzane w projektach z powodu niepoprawnego buforowania. |
| Rozliczenia i ceny | 2541660 | **Sprawdzanie poprawności tworzenia zamówienia sprzedaży** w trybie podwójnym powinna być dostępna tylko dla zamówień opartych na projektach. |
| Rozliczenia i ceny | 2552745 | Podatku nie jest rozdzielany między klientów, którzy ustawili podzielone reguły fakturowania. |
| Rozliczenia i ceny | 2558859 | Udoskonalone komunikaty o błędach w przypadku skonfigurowania rozmiarów kalkulacji cen. |
| Rozliczenia i ceny | 2558933 | **Importowanie z szacowania projektu** kończy się niepowodzeniem, gdy zostanie dodany projekt **msdyn\_project** jako aspekt kalkulacji cen. |
| Rozliczenia i ceny | 2559101 | Usuwanie parametrów projektu nie jest blokowane i powoduje problemy. |
|   Zarządzanie szansami sprzedaży | 2570390 | Dwue write plug-in. typ konta w ofertach, zamówieniach i szansach sprzedaży ma być **Klientem**, nawet jeśli ten typ konta jest poprawny. |
| Rozliczenia i ceny | 2586097 | Podział wartości rzeczywistych kosztów fakturowanych nie jest cofany, gdy projekt jest usuwany z wiersza kontraktu projektu. |
| Rozliczenia i ceny | 2589619 | Podatek od materiałów do zapisu jest propagowany do wartości rzeczywistych sprzedaży i faktury. |
|   Zarządzanie szansami sprzedaży | 2594015 | Oferty nie mogą zostać zamknięte jako woni dla klientów, którzy mają warunki płatności za pomocą usługi **Net60**. |
| Planowanie i śledzenie projektu | 2595841 | W Project for the Web użytkownicy otrzymują komunikat o błędzie informujący o braku danych **msdyn\_actualstart** po utworzeniu nowego żądania zasobu. |
| Czas i wydatek | 2602511 | Pole **Odrzucone przez czas** zawiera **nazwę System** zamiast nazwanego użytkownika jako osoby odrzucanej. |
| Czas i wydatek | 2602528 | Osoba zatwierdzająca projekt może zatwierdzać czas w projektach, w których nie jest wymieniona jako osoba zatwierdzająca. |
| Rozliczenia i ceny | 2608550 | Fakturę korekty można potwierdzić nawet w przypadku brak zmian w oryginalnym. |

## <a name="removed-and-deprecated-features"></a>Usunięte i przestarzałe funkcje

Funkcje [Usunięte lub przestarzałe w programie Project Operations](../../whats-new/removed-depreciated-features-project.md) temat opisano funkcje, które zostały usunięte lub przestarzałe w programie Dynamics 365 Project Operations.

- Usunięta funkcja nie jest już dostępna w produkcie.
- Przestarzała funkcja nie jest aktywnie tworzona i może zostać usunięta w przyszłej aktualizacji.

Ogłoszenie o wycofaniu pojawi się w temacie [Usunięte lub wycofane funkcje w Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 miesięcy przed usunięciem jakiejkolwiek funkcji z produktu.
