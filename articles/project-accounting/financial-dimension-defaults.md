---
title: Wartości domyślne wymiaru finansowego
description: Ta temat zawiera informacje na temat konfigurowania wartości domyślnych wymiarów finansowych.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950142"
---
# <a name="financial-dimension-defaults"></a>Wartości domyślne wymiaru finansowego

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Aplikacja Dynamics 365 Project Operations używa struktury [wymiarów finansowych](/dynamics365/finance/general-ledger/financial-dimensions) w aplikacji Dynamics 365 Finance w celu uzyskiwania dodatkowych informacji na temat ksiąg i transakcji księgi głównej projektu.

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