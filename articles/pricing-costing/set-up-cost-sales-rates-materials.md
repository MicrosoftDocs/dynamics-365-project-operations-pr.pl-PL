---
title: Konfigurowanie kosztów i stawek sprzedaży na potrzeby materiałów
description: Ten temat zawiera informacje dotyczące konfigurowania kosztów i stawek sprzedaży materiałów używanych w projektach.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1b1b679f15662d922804deefb6372adcdf4d4839
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576881"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Konfigurowanie kosztów i stawek sprzedaży na potrzeby materiałów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Możesz ustawić koszt i ceny sprzedaży dla produktów w Dynamics 365 Project Operations. Koszty i ceny sprzedaży produktów mogą być podane tylko w jednej walucie, która musi być walutą w nagłówku cennika.

Aby skonfigurować koszt i stawki sprzedaży dla produktów, wykonaj następujące kroki. 

1. Przejdź do **Sprzedaż** > **Klienci** > **Cenniki** i wybierz **Nowy**, aby utworzyć nowy cennik. 
2. W **Pozycje cennika** w menu podsiatki wybierz pozycję **Nowa pozycja cennika**. 
3. Na stronie **Szybkie tworzenie** wprowadź produkt i jednostkę, dla których tworzysz nową cenę.

Aby uzyskać więcej informacji na temat definiowania cen pozycji katalogu, zobacz [Definiowanie cen produktów za pomocą cenników i pozycji cenników](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) i [Dokładność dziesiętna w walucie i cenach](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations nie obsługuje wszystkich metod kalkulacji cen produktów jako Dynamics 365 Sales. Jedyna metoda kalkulacji cen obsługiwana w przypadku produktów używanych w projektach to *kwota w walucie*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
