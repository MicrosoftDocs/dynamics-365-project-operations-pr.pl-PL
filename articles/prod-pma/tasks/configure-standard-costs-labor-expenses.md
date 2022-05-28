---
title: Konfigurowanie kosztów standardowych na robociznę i koszty
description: W tym temat opisano sposób konfigurowania kosztów standardowych dla robocizny i kosztów projektu.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd74da69986a73e933f8cfedce40158555c2ac60
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685345"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurowanie kosztów standardowych na robociznę i koszty

[!include [banner](../../includes/banner.md)]

W tym temat opisano sposób konfigurowania kosztów standardowych dla robocizny i kosztów projektu. W tym zadaniu jest używany zestaw danych USSI.

1. W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Koszty własne (godziny)**.
2. Wybierz **Nowy**.
3. W polu **Data wejścia w życie** wprowadź datę.
4. W polu **Koszt własny** wprowadź liczbę. Użytkownik może skonfigurować standardowy koszt własny dla danej kategorii projektu lub zdefiniować koszty własne według numeru pracownika, numeru projektu, kategorii, daty lub dowolnej kombinacji tych elementów. Koszt własny jest kosztem własnym o najwyższym poziomie szczegółowości.  
5. Wybierz pozycję **Zapisz**.
6. W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Cena sprzedaży (godziny)**.
7. Wybierz **Nowy**.
8. W polu **Data wejścia w życie** wprowadź datę.
9. W polu **Ważne przez** wybierz opcję.
10. W polu **Ceny** wprowadź liczbę. Użytkownik może skonfigurować standardową cenę sprzedaży dla transakcji godzinowych lub dla kategorii projektu. Można również skonfigurować ceny sprzedaży według numerów pracowników, numerów projektów, kategorii, dat transakcji lub dowolnej kombinacji tych elementów. Rzeczywista cena sprzedaży stosowana w momencie, gdy pracownik wprowadza transakcję w arkuszu godzinowym, to cena sprzedaży zawierająca najwyższy poziom szczegółowości. Jeśli na przykład została ustawiona zarówno cena ogólna, jak i cena sprzedaży określona przez pracownika, jest używana cena sprzedaży właściwa dla danego procesu.  
11. Wybierz pozycję **Zapisz**.
12. Zamyknij stronę.
13. W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Koszty własne (wydatki)**.
14. Wybierz **Nowy**.
15. W polu **Data wejścia w życie** wprowadź datę.
16. W polu **Koszt własny** wprowadź liczbę. W programie można wypełnić wiele pól, ale jest to minimalny format wymagany do zapisania rekordu.  
17. Wybierz pozycję **Zapisz**.
18. W okienku nawigacji wybierz kolejno pozycje **Moduły > Zarządzanie projektami i księgowanie > Ustawienia > Ceny > Cena sprzedaży (wydatki)**.
19. Wybierz **Nowy**.
20. W polu **Data wejścia w życie** wprowadź datę.
21. W polu **Ważne przez** wybierz opcję.
22. W polu **Ceny** wprowadź liczbę. Rzeczywista cena sprzedaży stosowana w momencie, gdy pracownik wprowadza transakcje w arkuszu wydatków, to cena sprzedaży zawierająca najwyższy poziom szczegółowości. Na przykład, jeśli skonfigurowano zarówno cenę sprzedaży ogólną, jak i cenę sprzedaży dla konkretnego pracownika, używana jest cena sprzedaży dla konkretnego pracownika.  
23. Wybierz pozycję **Zapisz**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]