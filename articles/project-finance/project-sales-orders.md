---
title: Zamówienie sprzedaży projektów dotyczące projektów typu Czas i materiały
description: W tym temat wyjaśniono, jak tworzyć oparte na projektach zamówienia sprzedaży na potrzeby projektów typu czasu i materiałów.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754280"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="b96fe-103">Zamówienie sprzedaży projektów dotyczące projektów typu Czas i materiały</span><span class="sxs-lookup"><span data-stu-id="b96fe-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="b96fe-104">W tym temat opisano sposób tworzenia zamówienia sprzedaży dla projektu.</span><span class="sxs-lookup"><span data-stu-id="b96fe-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="b96fe-105">Zamówienia sprzedaży można tworzyć tylko dla projektów typu **czas i materiały**.</span><span class="sxs-lookup"><span data-stu-id="b96fe-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="b96fe-106">Jeśli projekt typu czas i materiały ma wiele źródeł finansowania w kontrakcie projektu, należy włączyć parametr **Zezwalaj na zamówienia sprzedaży dla projektów z wieloma źródłami finansowania** na stronie **Parametry Zarządzanie projektami i księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="b96fe-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="b96fe-107">Obsługa zamówień sprzedaży projektów z wieloma źródłami finansowania jest dostępna od wersji aplikacji 10.0.2 i nowszych.</span><span class="sxs-lookup"><span data-stu-id="b96fe-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="b96fe-108">Parametr umożliwiający obsługę zamówień sprzedaży projektów z wieloma źródłami finansowania zostanie usunięty w fali wydań z kwietnia 2020 r., Po czym funkcja będzie zawsze włączona.</span><span class="sxs-lookup"><span data-stu-id="b96fe-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="b96fe-109">Zamówienia sprzedaży oparte na projektach można tworzyć na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="b96fe-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="b96fe-110">Przejść do projektu.</span><span class="sxs-lookup"><span data-stu-id="b96fe-110">Go to the project itself.</span></span> <span data-ttu-id="b96fe-111">W okienku akcji wybierz pozycję **Zarządzaj > Zadania towarów > Zamówienie sprzedaży**.</span><span class="sxs-lookup"><span data-stu-id="b96fe-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="b96fe-112">Informacje o projekcie będą domyślnie zamówione na zamówienie sprzedaży z projektu.</span><span class="sxs-lookup"><span data-stu-id="b96fe-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="b96fe-113">Jeśli kontrakt projektu zawiera więcej niż jedno źródło finansowania, należy wybrać źródło finansowania, aby ustawić klienta dla danego zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b96fe-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="b96fe-114">Jeśli dla danego projektu istnieje tylko jedno źródło finansowania, klient zostanie ustawiony na automatyczny.</span><span class="sxs-lookup"><span data-stu-id="b96fe-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="b96fe-115">Przejdź do strony listy **Wszystkie zamówienia sprzedaży** i utwórz nowe zamówienie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b96fe-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="b96fe-116">Konieczne będzie wybranie projektu dla zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b96fe-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="b96fe-117">Po wybraniu projektu klient zostanie ustawiony ze źródła finansowania lub konieczne będzie wybranie źródła finansowania, jeśli kontrakt projektu zawiera wiele źródeł finansowania.</span><span class="sxs-lookup"><span data-stu-id="b96fe-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

