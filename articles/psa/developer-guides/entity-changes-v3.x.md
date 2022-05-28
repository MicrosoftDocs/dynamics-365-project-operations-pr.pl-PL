---
title: Zmiany dotyczące encji, kontrolek i interfejsu użytkownika (Project Service Automation wer. 3.x)
description: Ten temat opisuje zmiany wprowadzone w rozwiązaniu Microsoft Dynamics Project Service Automation w wersji 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: da43e0d15e655977c0c1be7348192a0189a56a6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597581"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Zmiany dotyczące encji, kontrolek i interfejsu użytkownika (Project Service Automation wer. 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Wraz z wydaniem wersji 3.x rozwiązania Microsoft Dynamics Project Service Automation (PSA) wprowadzono wiele zmian w encjach, kontrolkach, widokach i interfejsie użytkownika. Ten temat zawiera informacje o tych istotnych zmianach.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relacje nadrzędny-podrzędny dla encji Dokument sprzedaży, Wiersz dokumentu sprzedaży i Szczegóły wiersza dokumentu sprzedaży
W wersjach programu Dynamics 365 Project Service Automation (PSA) starszych niż 3.0 niektóre relacje między encjami Dokument sprzedaży, Wiersz dokumenty sprzedaży i Szczegółowy wiersza dokumentu sprzedaży zostały zaimplementowane za pośrednictwem pól ciągów, które zawierają ciąg reprezentujący identyfikator GUID pokrewnej encji. Wynikało to z ograniczeń platformy, które powodowały konieczność utworzenia rozbudowanego niestandardowego kodu na serwerze i kliencie rozwiązania, aby te relacje działały podobnie do typowych relacji między encjami w usłudze Dynamics CRM oraz aby pola ciągów działały jak pola wyszukiwania.

Rozwiązanie PSA w wersji 3.0 zostało unowocześnione i teraz wykorzystuje nowe relacje między encjami Dokument sprzedaży i Wiersz dokumentu sprzedaży.

Ponieważ teraz odwołania do encji można wskazywać za pomocą pól wyszukiwania, występujące w poprzedniej wersji pola zawierające wartości ciągów identyfikatorów GUID pokrewnych encji nie są już potrzebne i dlatego zostały wycofane. Niestandardowy kod po stronach klienta i serwera, który obsługiwał relacje zdefiniowane w starszych polach ciągów, również został wycofany.

### <a name="entity-schema-changes"></a>Zmiany w schemacie encji
Poniższa tabela zawiera listę wycofanych pól ciągów i odpowiadających im nowych pól wyszukiwania w encjach. 

 Encja |   Pole wycofane (ciąg) | Nowe pole (wyszukiwania)
--- | --- | ---
invoicedetail (Wiersz faktury) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Wartość rzeczywista) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Harmonogram fakturowania pozycji kontraktu projektu) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Punkt kontrolny pozycji kontraktu projektu) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Fakt) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Szczegóły wiersza faktury) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Wiersz arkusza) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Kategoria zasobu pozycji kontraktu projektu) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Szczegóły pozycji kontraktu projektu) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Kategoria transakcji pozycji kontraktu projektu) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Klasyfikacja transakcji pozycji kontraktu projektu) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Harmonogram fakturowania wierszy oferty) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Kategoria zasobów wiersza oferty) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Punkt kontrolny wiersza oferty) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Szczegóły wiersza oferty) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Kategoria transakcji wiersza oferty) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Klasyfikacja transakcji wiersza oferty) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Wiersz zamówienia) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Wycofane niestandardowe widoki i kontrolki
Poniższe niestandardowe widoki i kontrolki oraz powiązane z nimi artefakty zostały wycofane.

- Widok odpłatności.
- Niestandardowe kontrolki siatki do wyświetlania szczegółów wierszy ofert na stronie **Informacje o projekcie** dla wiersza oferty.
- Niestandardowe kontrolki siatki do wyświetlania szczegółów pozycji kontraktu projektu na stronie **Informacje o projekcie** dla wiersza zamówienia sprzedaży.

> [!NOTE]
> Aby zapoznać się z pełną listą wycofanych zasobów, zobacz [Wycofane zasoby internetowe w rozwiązaniu Project Service Automation w wersji 3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Moduł aplikacji ujednoliconego interfejsu klienta
Wraz z wprowadzeniem modułów aplikacji ujednoliconego interfejsu klienta (UCI) z systemu PSA usunięto wpisy mapy witryny.  
Funkcjonalność przełączania formularzy na Szansa sprzedaży, Oferta, Zamówienie i Faktura została wycofana jako niepotrzebna, ponieważ moduł aplikacji UCI zawiera tylko wersje formularzy istniejące w programie PSA.  

Następujące zasoby internetowe zostały wycofane:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Aby zapoznać się z pełną listą wycofanych zasobów, zobacz [Wycofane zasoby internetowe w rozwiązaniu Project Service Automation w wersji 3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
