---
title: Transakcje biznesowe w Project Operations
description: Ten artykuł zawiera przegląd pojęcia transakcji biznesowych w Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923293"
---
# <a name="business-transactions-in-project-operations"></a>Transakcje biznesowe w Project Operations

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W Microsoft Dynamics 365 Project Operations *transakcja biznesowa* to abstrakcyjne pojęcie, które nie jest reprezentowane przez żadną encję. Jednak niektóre typowe pola i procesy wykonywane na encjach zaprojektowano tak, aby korzystały z koncepcji transakcji biznesowych. To abstrakcyjne pojęcie jest używane w następujących encjach:

- Szczegóły wiersza oferty
- Szczegóły pozycji kontraktu
- Wiersze szacowania
- Wiersze arkusza
- Wartości rzeczywiste

Spośród tych encji Szczegóły wiersza oferty, Szczegóły pozycji kontraktu i Wiersze szacowania są mapowane na *fazę oszacowania* w cyklu życia projektu. Encje Wiersze arkusza i Wartości rzeczywiste są mapowane na *fazę wykonywania* w cyklu życia projektu.

Project Operations traktuje rekordy w tych pięciu encjach jako transakcje biznesowe. Jedyną różnicą jest to, że rekordy w jednostkach, które są mapowane na fazę szacowania (Szczegóły linii wyceny, Szczegóły linii kontraktu i Wiersze szacowania) są uważane za *prognozy finansowe*, podczas gdy rekordy w jednostkach, które są mapowane na fazę wykonania ( Wiersze dziennika i dane rzeczywiste) są uważane za *fakty finansowe*, które już wystąpiły.

Aby uzyskać więcej informacji, zobacz [Szacunki](../project-management/estimating-projects-overview.md) i [Wartości rzeczywiste](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Pojęcia unikatowe dla transakcji biznesowych

Poniższe pojęcia są unikatowe dla koncepcji transakcji biznesowych:

- Typ transakcji
- Klasa transakcji
- Początkowy rekord transakcji
- Połączenie transakcji

### <a name="transaction-type"></a>Typ transakcji

Typ transakcji reprezentuje czas i kontekst wpływu aspektów finansowych w projekcie. Jest zdefiniowany przez zestaw opcji, który ma następujące obsługiwane wartości w Project Operations:

- Koszt
- Kontrakt projektu
- Nierozliczona sprzedaż
- Rozliczona sprzedaż
- Sprzedaż międzyorganizacyjna
- Koszt jednostkowy zasobów

### <a name="transaction-class"></a>Klasa transakcji

Klasa transakcji reprezentuje różne typy kosztów ponoszonych w projektach. Jest zdefiniowany przez zestaw opcji, który ma następujące obsługiwane wartości w Project Operations:

- Czas
- Wydatek
- Materiał
- Opłata
- Punkt kontrolny
- Podatek

> [!NOTE]
> Wartość **Punkt kontrolny** jest zwykle używana w logice biznesowej do rozliczania transakcji ze stałą ceną w Project Operations.

### <a name="transaction-origin"></a>Początkowy rekord transakcji

Pochodzenia transakcji to encja przechowuje pochodzenia każdej transakcji biznesowej w celu ułatwić raportowanie i śledzenie. Gdy rozpoczyna się wykonywanie projektu, każda transakcja biznesowa tworzy inną transakcję biznesową, która z kolei tworzy inną transakcję biznesową itp.

### <a name="transaction-connection"></a>Połączenie transakcji

Połączenie transakcji to encja, która przechowuje relację między dwoma podobnymi transakcjami biznesowymi, takimi jak koszt i powiązane wartości rzeczywiste dotyczące sprzedaży, lub między wycofaniami transakcji wyzwalanymi przez działania fakturowania, takie jak potwierdzenie faktury lub korekty faktury.

Jednostki Pochodzenie transakcji i Połączenie transakcji pomagają razem śledzić relacje między transakcjami biznesowymi i działaniami, które spowodowały utworzenie określonej transakcji biznesowej.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
