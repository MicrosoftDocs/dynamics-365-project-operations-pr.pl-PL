---
title: Wyłączanie wymiaru kalkulacji cen
description: Ten temat zawiera informacje na temat wyłączenia niestandardowych wymiarów kalkulacji cen.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: cba1f9915087f7910a9aa93378cb861983ca36ab
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600341"
---
# <a name="turning-off-a-pricing-dimension"></a>Wyłączanie wymiaru kalkulacji cen

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Co kilka lat może zaistnieć konieczność przejrzenia i zaktualizowania strategii kalkulacji cen. Wszelkie aktualizacje wprowadzone przez użytkownika mogą wymagać wyłączenia istniejącego wymiaru kalkulacji cen i utworzenia nowego. Na przykład uprzednio cena mogła być ustalana według kryterium **Rola**, ale obecnie użytkownik zdecydował się wyceniać według kryterium **Doświadczenie zawodowe**. Może to wymagać wyłączenia encji **Rola** jako wymiaru kalkulacji cen i utworzenia encji **Doświadczenie zawodowe** jako nowego wymiaru kalkulacji cen. 

Wyłączenia wymiaru kalkulacji cen, bez względu na to, czy jest on gotowy czy niestandardowy, można dokonać, ustawiając w wymiarze kalkulacji cen w polach **Ma zastosowanie do kosztu** i **Ma zastosowanie do sprzedaży** wartość **Nie**.

Po wykonaniu tej czynności może jednak zostać wyświetlony komunikat o błędzie pt. **Wymiar kalkulacji cen nie może być aktualizowany ani usuwany, jeśli istnieją rekordy skojarzonych rekordów cen**.

![Błąd procesu biznesowego prawdopodobny podczas wyłączania wymiaru kalkulacji cen.](media/Business-Process-Error.png)

Ten komunikat o błędzie oznacza, że istnieją rekordy cen, które uprzednio skonfigurowano dla wyłączanego wymiaru. Wszystkie rekordy **Cena roli** i **Narzut na cenę dla roli** odwołujące się do wymiaru muszą zostać usunięte, zanim dla wymiaru będzie można ustawić stosowalność **Nie**. Ta reguła ma zastosowanie zarówno do gotowych wymiarów kalkulacji cen, jak i wszelkich niestandardowych wymiarów kalkulacji cen utworzonych przez użytkownika. To sprawdzanie poprawności wynika z faktu, że każdy rekord **Cena roli** musi mieć unikatową kombinację wymiarów. Na przykład w cenniku zatytułowanym **Stawki kosztów US 2018** istnieją poniższe wiersze **Cena roli**. 

| Standardowe stanowisko         | Jednostka organizacyjna    |Jednostka   |Cena  |Waluta  |
| -----------------------|-------------|-------|-------|----------|
| Inżynier systemów|Contoso US|Hour| 100|USD|
| Starszy inżynier systemów|Contoso US|Hour| 150| USD|


Gdy wyłączysz encję **Standardowe stanowisko** jako wymiar kalkulacji, aparat kalkulacji cen podczas wyszukiwania ceny będzie z kontekstu wejściowego używał tylko wartości **Jednostka organizacyjna**. Jeśli element **Jednostka organizacyjna** w kontekście wejściowym ma wartość „Contoso US”, wynik będzie niedeterministyczny, ponieważ oba wiersze będą pasowały. Aby uniknąć tego scenariusza, podczas tworzenia rekordów **Cena roli** program sprawdza, czy kombinacja wymiarów jest unikatowa. Jeśli wymiar zostanie wyłączony po utworzeniu rekordów **Cena roli**, może nastąpić naruszenie tego ograniczenia. Z tego powodu przed wyłączeniem wymiaru trzeba koniecznie usunąć wszystkie wiersze **Cena roli** i **Narzut na cenę dla roli**, które mają wypełnioną tę wartość wymiaru.


[!INCLUDE[footer-include](../includes/footer-banner.md)]