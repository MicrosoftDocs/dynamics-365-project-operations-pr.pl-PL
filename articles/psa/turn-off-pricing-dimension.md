---
title: Wyłączanie wymiaru kalkulacji cen
description: Ten temat zawiera informacje na temat konfigurowania wymiarów kalkulacji cen w rozwiązaniu Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147306"
---
# <a name="turn-off-a-pricing-dimension"></a>Wyłączanie wymiaru kalkulacji cen

[!include [banner](../includes/psa-now-project-operations.md)]

Co kilka lat może zaistnieć konieczność przejrzenia i zaktualizowania strategii kalkulacji cen. Wszelkie aktualizacje wprowadzone przez użytkownika mogą wymagać wyłączenia istniejącego wymiaru kalkulacji cen i utworzenia nowego. Na przykład uprzednio cena mogła być ustalana według kryterium **Rola**, ale obecnie użytkownik zdecydował się wyceniać według kryterium **Doświadczenie zawodowe**. Może to wymagać wyłączenia encji **Rola** jako wymiaru kalkulacji cen i utworzenia encji **Doświadczenie zawodowe** jako nowego wymiaru kalkulacji cen. 

Wyłączenia wymiaru kalkulacji cen, bez względu na to, czy jest on gotowy czy niestandardowy, można dokonać, ustawiając w wymiarze kalkulacji cen w polach **Ma zastosowanie do kosztu** i **Ma zastosowanie do sprzedaży** wartość **Nie**.

Podczas wykonywania tej czynności może jednak zostać wyświetlony następujący komunikat o błędzie.

![Błąd procesu biznesowego prawdopodobny podczas wyłączania wymiaru kalkulacji cen](media/Business-Process-Error.png)


Ten komunikat o błędzie oznacza, że istnieją rekordy cen, które uprzednio skonfigurowano dla wyłączanego wymiaru. Wszystkie rekordy **Cena roli** i **Narzut na cenę dla roli** odwołujące się do wymiaru muszą zostać usunięte, zanim dla wymiaru będzie można ustawić stosowalność **Nie**. Ta reguła ma zastosowanie zarówno do gotowych wymiarów kalkulacji cen, jak i wszelkich niestandardowych wymiarów kalkulacji cen utworzonych przez użytkownika. To sprawdzanie poprawności wynika z faktu, że usługa Project Service ma ograniczenie, że każdy rekord **Cena roli** musi mieć unikatową kombinację wymiarów. Na przykład w cenniku zatytułowanym **Stawki kosztów US 2018** istnieją poniższe wiersze **Cena roli**. 

| Standardowe stanowisko         | Jednostka organizacyjna    |Jednostka   |Cena  |Waluta  |
| -----------------------|-------------|-------|-------|----------|
| Inżynier systemów|Contoso US|Hour| 100|USD|
| Starszy inżynier systemów|Contoso US|Hour| 150| USD|


Gdy wyłączysz encję **Standardowe stanowisko** jako wymiar kalkulacji, aparat kalkulacji cen w usłudze Project Service podczas wyszukiwania ceny będzie z kontekstu wejściowego używał tylko wartości **Jednostka organizacyjna**. Jeśli element **Jednostka organizacyjna** w kontekście wejściowym ma wartość „Contoso US”, wynik będzie niedeterministyczny, ponieważ oba wiersze będą pasowały. Aby uniknąć tego scenariusza, podczas tworzenia rekordów **Cena roli** program Project Service sprawdza, czy kombinacja wymiarów jest unikatowa. Jeśli wymiar zostanie wyłączony po utworzeniu rekordów **Cena roli**, może nastąpić naruszenie tego ograniczenia. Z tego powodu przed wyłączeniem wymiaru trzeba koniecznie usunąć wszystkie wiersze **Cena roli** i **Narzut na cenę dla roli**, które mają wypełnioną tę wartość wymiaru.



[!INCLUDE[footer-include](../includes/footer-banner.md)]