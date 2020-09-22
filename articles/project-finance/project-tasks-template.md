---
title: Synchronizowanie zadań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations
description: Ta temat opisuje szablon i podstawowe zadanie używane do synchronizowania zadań projektu bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754390"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizowanie zadań projektu bezpośrednio z rozwiązania Project Service Automation do Finance and Operations

[!include[banner](../includes/banner.md)]

Ta temat opisuje szablon i podstawowe zadanie używane do synchronizowania zadań projektu bezpośrednio z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE]
> - W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.
> - Jeśli używasz wersji Enterprise 7.3.0, po zainstalowaniu KB 4132657 i KB 4132660 będziesz mógł używać szablonów do integracji zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych, szacunków wydatków i danych rzeczywistych oraz do konfigurowania funkcji zamykający. Jeśli musisz zresetować dystrybucje rozliczeń, zalecamy również zainstalowanie KB 4131710.
> - Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Przepływ danych dla Project Service Automation do Finance

Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Project Service Automation i Finance. Szablon integracji dostępny z funkcją integracji danych umożliwia przepływ danych o zadaniach projektowych z Project Service Automation do Finance.

Na poniższej ilustracji przedstawiono sposób synchronizowania danych między Project Service Automation a Finance.

[![Przepływ danych do integracji Project Service Automation z Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Szablon i zadanie

Aby uzyskać dostęp do szablonu, w centrum administracyjnym Microsoft Power Apps wybierz pozycję **Projekty**, a następnie w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać szablony publiczne.

Następujący szablon i podstawowe zadanie służą do synchronizowania zadań projektu z Project Service Automation do Finance:

- **Nazwa szablonu podczas integracji danych:** zadania projektu (PSA do Fin i Ops)
- **Nazwa zadania w projekcie:** Zadania projektu

Przed synchronizacją zadań projektu należy zsynchronizować umowy dotyczące projektów i projekty.

## <a name="entity-set"></a>Zestaw encji

| Project Service Automation | Finanse                             |
|----------------------------|-------------------------------------|
| Zadania projektu              | Encja integrująca dla zadania projektu |

## <a name="entity-flow"></a>Przepływ encji

Zadaniami projektu zarządza się w Project Service Automation i są one synchronizowane z Finance jako działania projektów.

## <a name="prerequisites-and-mapping-setup"></a>Wymagania wstępne i ustawienia mapowania

Przed synchronizacją zadań projektu należy zsynchronizować umowy dotyczące projektów i projekty.

## <a name="power-query"></a>Power Query

Aby filtrować dane po spełnieniu tego warunku, należy użyć programu Microsoft Power Query dla programu Excel.

- W zadaniu projektu są rekordy specyficzne dla zasobów.

Jeśli konieczne jest użycie Power Query, wykonaj następujące wytyczne:

- Szablon Zadania projektu (PSA do Fin and Ops) zawiera domyślny filtr, który wyklucza rekordy specyficzne dla zasobów z zadania projektu, ustawiając filtr na **IsLineTask** jako **False**. W przypadku utworzenia własnego szablonu należy dodać ten filtr.

## <a name="template-mapping-in-data-integration"></a>Mapowanie szablonów w integracji danych

Na poniższym rysunku pokazano przykład mapowania zadań szablonów w zakresie integracji danych. Mapowanie przedstawia informacje o polach, które zostaną zsynchronizowane z Project Service Automation do Finance.

[![Mapowanie szablonu](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
