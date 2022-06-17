---
title: Konfigurowanie kosztów i stawek sprzedaży na potrzeby materiałów
description: W tym artykule przedstawiono informacje na temat konfigurowania kosztów i stawek sprzedaży dla materiałów użytych w projektach.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911793"
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
