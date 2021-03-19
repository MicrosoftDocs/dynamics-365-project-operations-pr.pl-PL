---
title: Wydatki międzyfirmowe
description: Ten temat zawiera informacje o tym, jak używać wydatków międzyfirmowych do przypisywania wydatków pracownika do podmiotu prawnego, dla którego praca została wykonana.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271546"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="1332d-103">Wydatki międzyfirmowe</span><span class="sxs-lookup"><span data-stu-id="1332d-103">Intercompany expenses</span></span>

<span data-ttu-id="1332d-104">Pracownik zatrudniony przez jeden podmiot prawny w organizacji może wykonywać działania dla innego podmiotu prawnego w danej organizacji.</span><span class="sxs-lookup"><span data-stu-id="1332d-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="1332d-105">Możesz użyć wydatków międzyfirmowych, aby przypisać wydatki pracownika do podmiotu prawnego, dla którego praca została wykonana.</span><span class="sxs-lookup"><span data-stu-id="1332d-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="1332d-106">Podmiot prawny, który jest zatrudniony przez pracownika, jest nazywany firmą wypożyczającą.</span><span class="sxs-lookup"><span data-stu-id="1332d-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="1332d-107">Podmiot prawny, na rzecz którego pracownik ponosi koszty, nosi nazwę podmiotu pożyczającego.</span><span class="sxs-lookup"><span data-stu-id="1332d-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="1332d-108">Zanim pracownik będzie mógł tworzyć i przesyłać wydatki międzyfirmowe, należy włączyć międzyfirmowe linie wydatków.</span><span class="sxs-lookup"><span data-stu-id="1332d-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="1332d-109">W encji prawnej, na stronie **Parametry zarządzania wydatkami** wybierz opcję **Zezwalaj na międzyfirmowe wiersze wydatków**.</span><span class="sxs-lookup"><span data-stu-id="1332d-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="1332d-110">Księgowanie podatku na potrzeby kosztów międzyfirmowych</span><span class="sxs-lookup"><span data-stu-id="1332d-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1332d-111">Zanim będzie można użyć grup podatków, które są skojarzone z firmą wypożyczającą (źródłową) zamiast firmy pożyczającej (docelowej) w raporcie z wydatków, należy włączyć tę funkcję w konfiguracji podatku od sprzedaży księgi głównej.</span><span class="sxs-lookup"><span data-stu-id="1332d-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="1332d-112">Gdy parametr **Firma dla księgowania podatku międzyfirmowego** jest ustawiony na **Źródło**, a **Reguły opodatkowania podatku** są ustawione na **Nie**, używana jest kombinacja podatków dla firmy wypożyczającej.</span><span class="sxs-lookup"><span data-stu-id="1332d-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="1332d-113">Jeśli ten sam parametr ma ustawioną wartość **Docelowy**, będzie używana kombinacja podatku dla podmiotu prawnego wypożyczającego.</span><span class="sxs-lookup"><span data-stu-id="1332d-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="1332d-114">W przypadku podmiotów prawnych w Stanach Zjednoczonych, gdy parametr jest ustawiony na wartość **Źródło**, to w polu **Należny podatek od sprzedaży** musi być skonfigurowana nowa strona **Grup księgowania w rejestrze**.</span><span class="sxs-lookup"><span data-stu-id="1332d-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="1332d-115">Silnik do księgowania użyje informacji z tego pola do prowadzania rachunków związanych z podatkami.</span><span class="sxs-lookup"><span data-stu-id="1332d-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="1332d-116">Zachowanie to jest spójne w przypadku wierszy wydatków zaksięgowanych z użyciem projektu lub bez niego.</span><span class="sxs-lookup"><span data-stu-id="1332d-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]