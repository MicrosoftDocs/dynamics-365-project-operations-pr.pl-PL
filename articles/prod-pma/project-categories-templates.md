---
title: Synchronizacja kategorii wydatku projektu między Finance and Operations i Project Service Automation
description: W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania kategorii wydatków projektu między Microsoft Dynamics 365 Finance do Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 52c79f8b641d4b2df3b30964331633f2487402f8f8d229b540f9544c0f848557
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001129"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronizacja kategorii wydatku projektu między Finance and Operations i Project Service Automation

[!include[banner](../includes/banner.md)]

W tym temacie opisano szablony i podstawowe zadania, które są używane do synchronizowania kategorii wydatków projektu między Dynamics 365 Finance do Dynamics 365 Project Service Automation.

> [!NOTE]
> - W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.
> - Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.
> - Jeśli używasz wersji Enterprise 7.3.0, po zainstalowaniu KB 4132657 i KB 4132660 będziesz mógł używać szablonów do integracji zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych, szacunków wydatków i danych rzeczywistych oraz do konfigurowania funkcji zamykający. Jeśli musisz zresetować dystrybucje rozliczeń, zalecamy również zainstalowanie KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Przepływ danych dla Project Service Automation i Finance

Rozwiązanie do integracji Project Service Automation i Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance. Szablony integracji, które są dostępne z funkcją integracji danych, umożliwiają przepływ danych o kategoriach transakcji wydatków projektu między Finance i Project Service Automation.

Jeśli kategorie wydatków projektu są na pewno finansowane w finansach, przepływ integracji jest najpierw z Finance do rozwiązania Project Service Automation. Identyfikatory integracji kategorii wydatków projektu są następnie aktualizowane poprzez synchronizację z Project Service Automation do Finance.

Jeśli kategorie wydatków projektu są opanowane w Project Service Automation, przepływ integracji jest najpierw z Project Service Automation do Finance. Kategorie projektów muszą być już skonfigurowane w Finance przed synchronizacją z Project Service Automation. Następnie zsynchronizuj z Finance z powrotem do Project Service Automation, a następnie ponownie z Project Service Automation do Finance. W ten sposób pomagasz zagwarantować, że kategorie są połączone i że nie są tworzone żadne duplikaty.

> [!NOTE]
> Zazwyczaj kategorie wydatków projektu są opanowane w Finance. Jeśli jednak tak nie jest lub jeśli kategorie wydatków zostały już utworzone w programie Project Service Automation, należy najpierw zsynchronizować za pomocą szablonu Kategorie transakcji wydatków projektu (PSA do Fin i Ops). Następnie zsynchronizuj za pomocą szablonu Kategorie transakcji wydatków projektu (Fin i Ops do PSA). Następnie należy jeszcze raz uruchomić synchronizację z Project Service Automation do Finance.
>
> Jeśli synchronizujesz najpierw z Project Service Automation, przed uruchomieniem synchronizacji w Finance muszą być spełnione następujące wymagania:
>
> - Kategoria udostępniona, która jest zgodna z kategorią projektu skonfigurowaną w programie Project Service Automation, musi istnieć i musi być włączona zarówno dla **Projektu**, jak i dla **Wydatków**.
> - Dla każdej firmy finansowej, z którą należy zintegrować, muszą istnieć następujące kategorie projektów:
>
>     - **Kategoria projektu** istnieje. 
>     - **Użycie funkcji w wydatkach** jest włączone.
>     - **Aktywny w arkuszu** jest włączony.
>     - **Typ transakcji** jest ustawiony na **Koszt**.

Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.

[![Przepływ danych do integracji Project Service Automation z Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synchronizacja kategorii wydatków projektu z Finance do Project Service Automation

### <a name="template-and-task"></a>Szablon i zadanie

Aby uzyskać dostęp do szablonu, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty**, a następnie w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać szablony publiczne.

Następujący szablon i podstawowe zadanie służą do synchronizowania kategorii wydatków projektu z Finance do Project Service Automation:

- **Nazwa szablonu podczas integracji danych:** Kategorie transakcji wydatków projektu (od Fin i Ops do PSA)
- **Nazwa zadania w projekcie:** Synchronizacja kategorii do PSA

### <a name="entity-set"></a>Zestaw encji

| Finanse                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Encja integrująca dla kategorii | Kategorie transakcji     |

### <a name="entity-flow"></a>Przepływ encji

Kategorie wydatków projektów są zarządzane w Finance i są synchronizowane z Project Service Automation jako kategorie transakcji.

### <a name="power-query"></a>Power Query

Przy synchronizowaniu z Project Service Automation należy użyć Microsoft Power Query dla Excel w celu ustawienia typu fakturowania w kategorii transakcji. Kategoria transakcji wydatku projektu (Fin i Ops do PSA) zawiera domyślną kolumnę i mapowanie. Aby utworzyć własny szablon, należy w Power Query dodać kolumnę warunkową. Wykonaj poniższe kroki.

1. Kliknij strzałkę, aby otworzyć mapowanie zadania kategorii wydatków projektu w szablonie Kategorie transakcji wydatków w projekcie (Fin i Ops do PSA).
2. Kliknij łącze **Zaawansowane zapytania i filtrowania**, aby otworzyć Power Query.
2. Wybierz opcję **Dodaj kolumnę warunkową**.
3. Wprowadź nazwę nowej kolumny, na przykład nazwa **TypRozliczenia**.
4. Wprowadź następujący warunek: **Jeśli CATEGORYID nie jest równy zero, 19235001, w przeciwnym razie zero**.
5. Kliknij **OK** w kolumnie.
6. Należy pamiętać, aby zamapować tę nową kolumnę na stronie mapowania.

Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych. Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z rozwiązania Finance do Project Service Automation.

[![Synchronizacja kategorii wydatków projektu z mapowaniem szablonów Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synchronizacja kategorii wydatków projektu z Project Service Automation do Finance

### <a name="template-and-task"></a>Szablon i zadanie

Następujący szablon i podstawowe zadanie służą do synchronizowania kategorii wydatków projektu z Project Service Automation do Finance:

- **Nazwa szablonu podczas integracji danych:** Kategorie transakcji wydatków projektu (PSA do Fin i Ops)
- **Nazwa zadania w projekcie:** Synchronizacja kategorii do Fin Ops

### <a name="entity-set"></a>Zestaw encji

| Project Service Automation | Finanse                           |
|----------------------------|-----------------------------------|
| Kategorie transakcji     | Encja integrująca dla kategorii |

### <a name="entity-flow"></a>Przepływ encji

Kategorie wydatków projektów są zarządzane w Finance i są synchronizowane z Project Service Automation jako kategorie transakcji. Synchronizacja z powrotem do Finance aktualizuje kategorię projektu w Finance za pomocą identyfikatora integracji z Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapowanie szablonów w integracji danych

Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych.

> [!NOTE]
> Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.

[![Mapowanie szablonu Project Service Automation z Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]