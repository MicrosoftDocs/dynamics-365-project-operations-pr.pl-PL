---
title: Konfigurowanie konwersji walut w celu obliczania cen sprzedaży na podstawie współczynnika kosztów
description: W tym artykule wyjaśniono sposób konfigurowania zachowania konwersji walut, które będzie używane w rozwiązaniu Microsoft Dynamics 365 Project Operations podczas generowania transakcji sprzedaży na podstawie transakcji kosztów.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816674"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Konfigurowanie konwersji walut w celu obliczania cen sprzedaży na podstawie współczynnika kosztów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W rozwiązaniu Microsoft Dynamics 365 Project Operations ceny sprzedaży w kategoriach wydatków mogą być ustawione jako wartości liczbowe lub można je skonfigurować w taki sposób, aby były obliczane na podstawie poniesionego kosztu.

Podczas konfiguracji do obliczania na podstawie poniesionego kosztu są dostępne następujące opcje:

- Po kosztach
- Procent marży nad kosztem

W scenariuszach, w których wydatek kosztów jest ponoszony w walucie innej niż waluta sprzedaży kontraktu projektu, do obliczenia ceny sprzedaży w oparciu o koszt jest wymagana konwersja walut.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Zachowanie konwersji walut wykorzystujące macierzyste kursy wymiany walut Dataverse

Domyślnie Project Operations wykorzystuje kursy wymiany walut przechowywane w tabeli Waluta w programie Dataverse. Aby skonfigurować Project Operations tak, aby do kalkulacji cen sprzedaży używały macierzystych kursów wymiany, wykonaj następujące kroki.

1. Przejdź do **Project Operations \> Ustawienia \> Parametry**.
1. Otwórz stronę szczegółów **Parametru projektu**.
1. Ustaw pole **Logiki konwersji walut** na pustą wartość.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Zachowanie konwersji walut wykorzystujące kursy wymiany walut z aplikacji finansowych i operacyjnych

Kursy wymiany w tabeli waluty, która jest macierzyste w Dataverse, nie są skuteczne. Dlatego nie zawsze mogą być one skalowane do wymagań obliczania cen sprzedaży z cenników kosztów.

Może użyć kursów wymiany walut ze środowiska finansowego i operacyjnego w celu obliczania cen sprzedaży w walucie sprzedaży ze współczynnika kosztów w walucie kosztów. Aby skonfigurować to zachowanie konwersji walut, wykonaj następujące kroki.

1. Na stronie **Parametry projektu** dodaj pole logiki **konwersji walut**. Następnie zapisz i opublikuj dostosowanie.
1. Przejdź do **Project Operations \> Ustawienia \> Parametry**.
1. Otwórz stronę szczegółów **Parametru projektu**. 
1. Ustawienie pola **Zachowania konwersji walut** na **Rozszerzone z wartością domyślną**.
1. Nadaj roli zabezpieczeń **Użytkownikowi aplikacji podwójny zapis** uprawnienia **Globalne do odczytu** do następujących tabel:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. W środowisku finansowym i operacyjnym uruchom następujące mapowania podwójnego zapisu z początkową synchronizacją:

    - Typ kursu wymiany (msdyn\_exchangeratetypes)
    - Para kursu wymiany (msdyn\_currencyexchangeratepairs)
    - Kursy wymiany CDS (msdyn\_currencyexchangerates)

Po zakończeniu tych zmian podwójny zapis udostępni kursy wymiany ze środowiska finansowego i operacyjnego do Dataverse. Project Operations będzie następnie używać tych kursów wymiany do konwertowania kursów kosztów na walutę sprzedaży kontraktu.

> [!NOTE]
> Takie zachowanie dotyczące konwersji walut ma zastosowanie tylko do obliczania cen sprzedaży ze współczynnika kosztów. Nie będzie on używany do ogólnego obliczania wartości waluty podstawowej. Wartości waluty podstawowej zawsze będą stosować macierzyste kursy wymiany Dataverse, niezależnie od tego, czy ta procedura zostanie ukończona.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
