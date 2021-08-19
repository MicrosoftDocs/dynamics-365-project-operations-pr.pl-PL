---
title: Synchronizowanie szacowań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations
description: W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania szacunków godzin projektu i szacunków kosztów projektu bezpośrednio z Microsoft Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6696449d80e0915a0c878dbe75cfdf6e268b98ad9f6453bcfc4b424db68021e4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988214"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizowanie szacowań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations

[!include[banner](../includes/banner.md)]

W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania szacunków godzin projektu i szacunków kosztów projektu bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE]
> - W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.
> - Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Przepływ danych dla Project Service Automation do Finance

Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance. Szablony integracji, które są dostępne z funkcją integracji danych, umożliwiają przepływ danych o szacunkach godzin projektu i szacunkach kosztów projektu z Project Service Automation do Finance.

Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.

[![Przepływ danych do integracji Project Service Automation z Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Szacowania godzin projektu

### <a name="template-and-tasks"></a>Szablon i zadania

Aby uzyskać dostęp do dostępnych szablonów, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty**, a następnie w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać szablony publiczne.

Następujący szablon i podstawowe zadania są używane do synchronizowania szacowań godzin projektu z Project Service Automation do Finance:

- **Nazwa szablonu podczas integracji danych:** szacowania godzin projektu (PSA do Fin i Ops)
- **Nazwa zadań w projekcie:**

    - Relacje transakcji
    - Szacowanie wydatków

### <a name="entity-set"></a>Zestaw encji

| Project Service Automation | Finanse                                       |
|----------------------------|-----------------------------------------------|
| Zadania projektu              | Encja integrująca dla oszacowań godzin projektu |

### <a name="entity-flow"></a>Przepływ encji

Szacunkami godzin projektu można zarządzać w Project Service Automation i synchronizować je z Finance jako prognozy godzin projektu.

### <a name="prerequisites"></a>Wymagania wstępne

Zanim będzie można synchronizować oszacowania godzin projektu, należy zsynchronizować projekty, zadania projektów i kategorie transakcji z wydatkami projektu.

### <a name="power-query"></a>Power Query

W szablonie szacunków godzin projektu należy użyć dodatku Microsoft Power Query dla programu Excel, aby wykonać następujące zadania:

- Ustaw domyślny identyfikator modelu prognozy, który będzie używany podczas integracji tworzenia nowych prognoz godzinowych.
- Odfiltruj wszystkie rekordy specyficzne dla zasobów w zadaniu, których integracja nie powiedzie się, do prognoz godzinowych.
- Umożliwia odfiltrowanie pustych wierszy kategorii transakcji. Niepowodzenie wykonania tego zadania może spowodować nieprawidłową prognozę godzinową.

#### <a name="set-the-default-forecast-model-id"></a>Ustaw domyślny identyfikator modelu prognozy

Aby zaktualizować domyslny identyfikator modelu prognozy w szablonie, kliknij strzałkę na **mapie**, aby otworzyć mapowanie. Zaznacz łącze **Zaawansowane zapytania i filtrowania**.

- Jeśli używasz domyślnego szablonu szacowania godzin projektu (PSA do Fin i Ops), wybierz opcję **Wstawiony warunek** z listy **zastosowanych kroków**. We wpisie **Funkcja** zamień **O\_forecast** na nazwę identyfikatora modelu prognozy, która ma być używana podczas integracji. Szablon domyślny ma identyfikator modelu prognozy z danych demonstracyjnych.
- Jeśli tworzysz nowy szablon, musisz dodać tę kolumnę. W Power Query wybierz opcję **Dodaj kolumnę warunkową** i wprowadź nazwę nowej kolumny, na przykład **ModelID**. Wprowadź warunek dla kolumny, gdzie, jeśli zadanie projektowe nie ma wartości null, wtedy \<enter the forecast model ID\>. W przeciwnym razie ma wartość null.

#### <a name="filter-out-resource-specific-records"></a>Filtrowanie rekordów specyficznych dla zasobu

Szablon szacowania godzin projektu (PSA do Fin i Ops) zawiera domyślny filtr, który usuwa wszelkie rekordy specyficzne dla zasobów. W przypadku utworzenia własnego szablonu należy dodać ten filtr. Zaznacz łącze **Zaawansowane zapytania i filtrowania**, aby filtrować kolumnę **msdyn\_islinetask** tak, aby zawierała tylko **Fałszywe** rekordy.

#### <a name="filter-out-empty-transaction-category-rows"></a>Odfiltruj puste wiersze kategorii transakcji

Aby usunąć wiersze, które mają puste kategorie transakcji, należy dodać filtr. To zadanie jest wymagane, bez względu na to, czy jest używany szablon domyślny, czy też użytkownik tworzy własny szablon. Ten filtr usuwa wszystkie wiersze podsumowania z usługi Project Service Automation, które mogą powodować niepoprawne prognozy godzinowe w Finance. Wybierz łącze **Zaawansowane zapytania i filtrowania** w celu odfiltrowania pustych rekordów w kolumnie **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapowanie szablonów w integracji danych

Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych. Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.

[![Mapowanie szablonów zadań w integracji danych.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Szacunki kosztów projektu

### <a name="template-and-tasks"></a>Szablon i zadania

Następujący szablon i podstawowe zadania są używane do synchronizowania szacowań wydatków projektu z Project Service Automation do Finance:

- **Nazwa szablonu podczas integracji danych:** szacowania wydatków projektu (PSA do Fin i Ops)
- **Nazwa zadań w projekcie:**

    - Relacje transakcji 
    - Szacowanie wydatków

### <a name="entity-set"></a>Zestaw encji

| Project Service Automation | Finanse                                                  |
|----------------------------|----------------------------------------------------------|
| Połączenia transakcji    | Encja integrująca dla transakcji projektu relacje |
| Wiersze szacowania             | Encja integrująca dla oszacowań wydatków projektu         |

### <a name="entity-flow"></a>Przepływ encji

Szacunkami wydatków projektu można zarządzać w Project Service Automation i synchronizować je z Finance jako prognozy wydatków projektu.

### <a name="prerequisites"></a>Wymagania wstępne

Zanim będzie można synchronizować oszacowania wydatków projektu, należy zsynchronizować projekty, zadania projektów i kategorie transakcji z wydatkami projektu.

### <a name="power-query"></a>Power Query

W szablonie szacowania wydatków projektu należy użyć dodatku Power Query do wykonania następujących zadań:

- Filtr, w którym znajdują się tylko rekordy wierszy szacowanego wydatku.
- Ustaw domyślny identyfikator modelu prognozy, który będzie używany podczas integracji tworzenia nowych prognoz godzinowych.
- Przekształć typy fakturowania.
- Przekształć typy transakcji.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtr, w którym znajdują się tylko wiersze szacowanego wydatku.

Szablon Szacunki wydatków projektu (PSA do Fin i Ops) ma domyślny filtr, który obejmuje tylko wiersze wydatków w integracji. W przypadku utworzenia własnego szablonu należy dodać ten filtr. Zaznacz zadanie **Relacje transakcyjne**, a następnie kliknij strzałkę **Mapa**, aby otworzyć mapowanie. Wybierz łącze **Zaawansowane zapytania i filtrowania**. Przefiltruj kolumnę **msdyn\_transactiontype1**, tak aby zawierała tylko **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Ustaw domyślny identyfikator modelu prognozy

Aby zaktualizować domyslny identyfikator modelu prognozy w szablonie, wybierz zadanie **Szacowanie wydatków**, a potem kliknij strzałkę **Mapa**, aby otworzyć mapowanie. Wybierz łącze **Zaawansowane zapytania i filtrowania**.

- Jeśli są używane szablony domyślne szacowania wydatków projektów (PSA do Fin i Ops), w Power Query wybierz najpierw **Wstawiony warunek** z sekcji **Zastosowane kroki**. We wpisie **Funkcja** zamień **O\_forecast** na nazwę identyfikatora modelu prognozy, która ma być używana podczas integracji. Szablon domyślny ma identyfikator modelu prognozy z danych demonstracyjnych.
- Jeśli tworzysz nowy szablon, musisz dodać tę kolumnę. W Power Query wybierz opcję **Dodaj kolumnę warunkową** i wprowadź nazwę nowej kolumny, na przykład **ModelID**. Wprowadź warunek dla kolumny, gdzie, jeśli identyfikator linii oszacowania nie ma wartości null, wtedy \<enter the forecast model ID\>. W przeciwnym razie ma wartość null.

#### <a name="transform-the-billing-types"></a>Przekształć typy fakturowania

Szablon Szacunki kosztów projektu (od PSA do Fin i Ops) zawiera kolumnę warunkową używaną do przekształcania typów rozliczeń otrzymywanych z Project Service Automation podczas integracji. Jeśli tworzysz własny szablon, musisz dodać tę kolumnę warunkową. Wybierz łącze **Zaawansowane zapytania i filtrowania**, a następnie wybierz opcję **Dodaj kolumnę warunkową**. Wprowadź nazwę nowej kolumny, na przykład nazwa **TypRozliczenia**. Następnie wprowadź następujący warunek:

Jeśli **msdyn\_billingtype** = 192350000, to **NonChargeable**  
inaczej jeśli **msdyn\_billingtype** = 192350001, to **Chargeable**  
inaczej jeśli **msdyn\_billingtype** = 192350002, to **Complimentary**  
inaczej **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Przekształć typy transakcji

Szablon Szacunki kosztów projektu (od PSA do Fin i Ops) zawiera kolumnę warunkową używaną do przekształcania typów transakcji otrzymywanych z Project Service Automation podczas integracji. Jeśli tworzysz własny szablon, musisz dodać tę kolumnę warunkową. Wybierz łącze **Zaawansowane zapytania i filtrowania**, a następnie wybierz opcję **Dodaj kolumnę warunkową**. Wprowadź nazwę nowej kolumny, na przykład nazwa **TypTransakcji**. Następnie wprowadź następujący warunek:

Jeśli **msdyn\_transactiontypecode** = 192350000, **Koszt**  
inaczej jeśli **msdyn\_transactiontypecode** = 192350005, **Sprzedaż**  
inaczej **null**

### <a name="template-mapping-in-data-integration"></a>Mapowanie szablonów w integracji danych

Poniższe ilustracje przedstawiają przykłady odwzorowań zadań szablonu w integracji danych. Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.

[![Mapowanie szablonów transakcji szacowania wydatków.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapowanie szablonów szacowania wydatków.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]