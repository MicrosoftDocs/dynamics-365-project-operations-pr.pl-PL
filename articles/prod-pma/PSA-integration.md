---
title: Omówienie Project Service Automation
description: W tym temat zamieszczono informacje dotyczące Dynamics 365 Project Service Automation do integracji z rozwiązaniem Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082153"
---
# <a name="project-service-automation-overview"></a>Omówienie Project Service Automation

[!include[banner](../includes/banner.md)]

Rozwiązanie do integracji Project Service Automation to Finance wykorzystuje funkcję integracji danych do synchronizowania danych między wystąpieniami Dynamics 365 Finance i Dynamics 365 Project Service Automation za pośrednictwem Common Data Service. Szablony integracji, które są dostępne z funkcją integracji danych, umożliwiają przepływ projektów, umów dotyczących projektów, wierszy umów dotyczących projektów, punktów kontrolnych wierszy umów dotyczących projektów, zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych i szacunków wydatków z Project Service Automation do Finance.

> [!NOTE]
> - Jeśli jest używany program version 7.3.0, należy zainstalować 4074835 KB. Następnie będzie można zintegrować projekty o stałej cenie.
> - Jeśli używasz wersji 7.3.0 i przenosisz transakcje opłat z Project Service Automation, musisz zainstalować KB 4345320, aby uwzględnić te opłaty na fakturze za projekt.
> - Jeśli używasz wersji 8.0, będziesz mógł korzystać z integracji zadań projektowych, kategorii transakcji wydatków, szacunków godzinowych, szacunków wydatków i blokowania funkcji.
> - Jeśli używasz wersji 8.0.1 lub nowszej, będziesz mieć możliwość synchronizacji danych rzeczywistych.

Przed integracją Project Service Automation Finance należy skonfigurować parametry integracji Project Service Automation. Więcej informacji znajdziesz w [Parametry integracji usługi Project Service Automation](PSA-parameters.md).

To rozwiązanie integracji umożliwia bezpośrednią synchronizację w następujących sytuacjach:

- Utrzymuj kontrakty projektowe w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.
- Twórz projekty w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.
- Utrzymuj pozycje kontraktu w projekcie w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.
- Utrzymuj punkty kontrolne pozycji kontraktu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.
- Utrzymuj zadania projektu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.
- Utrzymuj kategorie transakcji wydatków w Finance i synchronizuj je bezpośrednio z Finance do Project Service Automation.
- Twórz oszacowania godzin projektu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.
- Twórz oszacowania wydatków projektu w Project Service Automation i synchronizuj je bezpośrednio z Project Service Automation do Finance.
- Twórz wartości rzeczywiste czasu, wydatków i opłat projektu w Project Service Automation i utwórz transakcje projektu w arkuszu integracji Project Service Automation, aby można je było zaksięgować w Finance.

## <a name="data-synchronization"></a>Synchronizacja danych

Na poniższej ilustracji przedstawiono sposób synchronizowania danych w ramach integracji między Project Service Automation a Finance.

> [!NOTE]
> Nie wszystkie szablony są obecnie dostępne. Szablony będą wydawane po zakończeniu.

[![Integracja Project Service Automation z Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Wymagania systemowe dotyczące Finance

Aby korzystać z rozwiązania integracji Project Service Automation z Finance, należy zainstalować wersję Enterprise Edition 7.3 z aktualizacją platformy 12 lub nowszą.

## <a name="system-requirements-for-project-service-automation"></a>Wymagania systemowe dla Project Service Automation

Aby użyć rozwiązania integracji Project Service Automation z Finance, należy zainstalować następujące składniki:

- Dynamics 365 Project Service Automation wersja 9.0.0.0 lub nowsza
- Rozwiązanie od potencjalnego klienta do otrzymania gotówki dla Dynamics 365 Sales w wersji 1.14.0.0 (v14) lub nowszej
- Rozwiązanie Project Service Automation do Finance dla Dynamics 365 Project Service Automation w wersji 1.0.0.0 lub nowszej

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Zainstaluj rozwiązanie integracji Project Service Automation z Finance w swoim wystąpieniu Project Service Automation

Pobierz rozwiązanie integracji Project Service Automation do Finance z [Centrum pobierania Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) i wykonaj instrukcje zawarte w rozwiązaniu.
