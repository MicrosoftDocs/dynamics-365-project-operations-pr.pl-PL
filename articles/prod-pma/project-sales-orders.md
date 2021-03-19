---
title: Zamówienie sprzedaży projektów dotyczące projektów typu Czas i materiały
description: W tym temat wyjaśniono, jak tworzyć oparte na projektach zamówienia sprzedaży na potrzeby projektów typu czasu i materiałów.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289067"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="82e1e-103">Zamówienie sprzedaży projektów dotyczące projektów typu Czas i materiały</span><span class="sxs-lookup"><span data-stu-id="82e1e-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82e1e-104">W tym temat opisano sposób tworzenia zamówienia sprzedaży dla projektu.</span><span class="sxs-lookup"><span data-stu-id="82e1e-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="82e1e-105">Zamówienia sprzedaży można tworzyć tylko dla projektów typu **czas i materiały**.</span><span class="sxs-lookup"><span data-stu-id="82e1e-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="82e1e-106">Jeśli projekt typu czas i materiały ma wiele źródeł finansowania w kontrakcie projektu, należy włączyć parametr **Zezwalaj na zamówienia sprzedaży dla projektów z wieloma źródłami finansowania** na stronie **Parametry Zarządzanie projektami i księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="82e1e-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="82e1e-107">Obsługa zamówień sprzedaży projektów z wieloma źródłami finansowania jest dostępna od wersji aplikacji 10.0.2 i nowszych.</span><span class="sxs-lookup"><span data-stu-id="82e1e-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="82e1e-108">Parametr umożliwiający obsługę zamówień sprzedaży projektów z wieloma źródłami finansowania zostanie usunięty w fali wydań z kwietnia 2020 r., Po czym funkcja będzie zawsze włączona.</span><span class="sxs-lookup"><span data-stu-id="82e1e-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="82e1e-109">Zamówienia sprzedaży oparte na projektach można tworzyć na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="82e1e-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="82e1e-110">Przejść do projektu.</span><span class="sxs-lookup"><span data-stu-id="82e1e-110">Go to the project itself.</span></span> <span data-ttu-id="82e1e-111">W okienku akcji wybierz pozycję **Zarządzaj > Zadania towarów > Zamówienie sprzedaży**.</span><span class="sxs-lookup"><span data-stu-id="82e1e-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="82e1e-112">Informacje o projekcie będą domyślnie zamówione na zamówienie sprzedaży z projektu.</span><span class="sxs-lookup"><span data-stu-id="82e1e-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="82e1e-113">Jeśli kontrakt projektu zawiera więcej niż jedno źródło finansowania, należy wybrać źródło finansowania, aby ustawić klienta dla danego zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="82e1e-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="82e1e-114">Jeśli dla danego projektu istnieje tylko jedno źródło finansowania, klient zostanie ustawiony na automatyczny.</span><span class="sxs-lookup"><span data-stu-id="82e1e-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="82e1e-115">Przejdź do strony listy **Wszystkie zamówienia sprzedaży** i utwórz nowe zamówienie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="82e1e-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="82e1e-116">Konieczne będzie wybranie projektu dla zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="82e1e-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="82e1e-117">Po wybraniu projektu klient zostanie ustawiony ze źródła finansowania lub konieczne będzie wybranie źródła finansowania, jeśli kontrakt projektu zawiera wiele źródeł finansowania.</span><span class="sxs-lookup"><span data-stu-id="82e1e-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]