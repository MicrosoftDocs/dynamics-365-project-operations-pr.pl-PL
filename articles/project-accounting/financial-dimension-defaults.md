---
title: Wartości domyślne wymiaru finansowego
description: W tym artykule podano informacje dotyczące konfigurowania domyślnych wartości wymiarów finansowych.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9e0d739ac1b7681e2e77ec651daf3da8316ff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931067"
---
# <a name="financial-dimension-defaults"></a>Wartości domyślne wymiaru finansowego

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_



Dynamics 365 Project Operations używa [Dynamics 365 financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework Dynamics 365 Finance w celu zapewnienia dodatkowych prognoz na temat transakcji sprzedaży podrzędnej i księgowej projektów.

W przypadku klienta, źródła finansowania projektu, punktu kontrolnego, pozycji kontraktu projektu lub projektu można ustawić domyślne wymiary finansowe.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definiowanie domyślnych wymiarów finansowych dla klienta

Wartości domyślne wymiarów klientów są określane w Finance. Wykonaj następujące kroki, aby ustawić domyślne wymiary.

1. W tym celu należy przejść do **Rozrachunki z odbiorcami** > **Klienci** > **Wszyscy klienci**.
2. Na stronie **Klienci** na karcie **Wymiary finansowe** ustaw wartości wymiarów finansowych dla określonego klienta.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Zdefiniuj domyślne wymiary finansowe dla umów dotyczących projektów

Kontrakty projektów są tworzone i konserwowane w Common Data Service (CDS). Atrybuty obsługi kont dla kontraktów projektów są ustawiane w module **Zarządzanie projektami i ich księgowanie** w Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Ustawianie wymiarów finansowych dla źródła finansowania projektu

1. Przejdź do **Zarządzanie projektami i księgowanie** > **Projekty** > **Kontrakty projektu**.
2. Zaznacz rekord, który chcesz zaktualizować, a następnie na karcie **Kontrakt projektu** wybierz pozycję **Pokaż domyślne księgowanie**.
3. Rozwiń **Pokrewne informacje** i wybierz kartę **Źródła finansowania**.
4. Ustaw wartości domyślne wymiaru finansowego. Należy zwrócić uwagę, że wymiar finansowy jest typem domyślnym na podstawie konta klienta.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Ustawianie wymiarów finansowych dla projektu pozycji kontraktu

1. Przejdź do **Zarządzanie projektami i księgowanie** > **Projekty** > **Kontrakty projektu**.
2. Zaznacz rekord, który chcesz zaktualizować, a następnie na karcie **Kontrakt projektu** wybierz pozycję **Pokaż domyślne księgowanie**.
3. Rozwiń **Pokrewne informacje** i wybierz kartę **Pozycje kontraktu**.
4. Ustaw wartości domyślne wymiaru finansowego. Wartości domyślne wymiarów finansowych są stosowane i mogą być używane tylko z pozycjami kontraktu z ustalonymi cenami (punktów kontrolnych).

Te wartości domyślne są używane w pokrewnych transakcjach i wierszach faktur dotyczących danego projektu.

## <a name="define-default-financial-dimensions-for-projects"></a>Zdefiniuj domyślne wymiary finansowe dla projektów

Kontrakty projektów są tworzone i utrzymywane w (CDS). Atrybuty obsługi kont dla projektów są ustawiane w module **Zarządzanie projektami i ich księgowanie** w Finance.

1. Przejdź do **Zarządzanie projektami i księgowanie** > **Projekty** > **Wszystkie projekty**.
2. Zaznacz rekord, który chcesz zaktualizować, a następnie na karcie **Projekt** wybierz pozycję **Pokaż domyślne księgowanie**.
3. Rozwiń **Pokrewne informacje** i wybierz kartę **Ustawienia**.
4. Ustaw wartości domyślne wymiaru finansowego. Należy zwrócić uwagę, że wymiar finansowy jest typem domyślnym na podstawie konta klienta. Jeśli projekt jest skojarzony z pozycją kontraktu, która ma wielu klientów kontraktów projektów, jest używany podstawowy klient z domyślnymi wymiarami finansowymi.

Domyślne wymiary finansowe projektu służą do ustawiania wartości domyślnych wierszy arkusza dla transakcji dotyczących czasu, wydatków i opłat w **Arkusz integracji aplikacji Project Operations** oraz w powiązanych wierszach faktur projektu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
