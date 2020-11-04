---
title: Wydatki międzyfirmowe
description: Pracownik zatrudniony przez jeden podmiot prawny w organizacji może wykonywać działania dla innego podmiotu prawnego w danej organizacji. W takiej sytuacji można skorzystać z funkcji wydatek międzyfirmowy, aby przypisać koszty pracownika firmie, dla której rzeczywiście wykonano pracę.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082163"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="b8a83-104">Wydatki międzyfirmowe</span><span class="sxs-lookup"><span data-stu-id="b8a83-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8a83-105">Pracownik zatrudniony przez jeden podmiot prawny w organizacji może wykonywać działania dla innego podmiotu prawnego w danej organizacji.</span><span class="sxs-lookup"><span data-stu-id="b8a83-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="b8a83-106">W takiej sytuacji można skorzystać z funkcji wydatek międzyfirmowy, aby przypisać koszty pracownika firmie, dla której rzeczywiście wykonano pracę.</span><span class="sxs-lookup"><span data-stu-id="b8a83-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="b8a83-107">Podmiot prawny, który jest zatrudniony przez pracownika, jest nazywany firmą wypożyczającą.</span><span class="sxs-lookup"><span data-stu-id="b8a83-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="b8a83-108">Podmiot prawny, na rzecz którego pracownik ponosi koszty, nosi nazwę podmiotu pożyczającego.</span><span class="sxs-lookup"><span data-stu-id="b8a83-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="b8a83-109">Aby pracownik mógł tworzyć i składać wydatki dotyczące pracy wykonywanej w odniesieniu do innej osoby prawnej, na stronie **Parametry zarządzania wydatkami** w firmie wypożyczającej wybierz opcję **Zezwalaj na wiersze kosztów międzyfirmowych**.</span><span class="sxs-lookup"><span data-stu-id="b8a83-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="b8a83-110">Księgowanie podatku na potrzeby kosztów międzyfirmowych</span><span class="sxs-lookup"><span data-stu-id="b8a83-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8a83-111">Aby użyć grup podatku skojarzonych z wypożyczającym (źródłowym) podmiotem, zamiast podmiotu pożyczającego (docelowego) w raporcie z wydatków należy skonfigurować odpowiednią opcję w konfiguracji podatku na potrzeby księgi głównej.</span><span class="sxs-lookup"><span data-stu-id="b8a83-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="b8a83-112">Kiedy parametr księgi głównej **Podmiot prawny na potrzeby międzyfirmowego księgowania podatkowego** jest ustawiony na wartość **Źródło** i wartość **Zastosuj reguły opodatkowania** ustawiona jest na **Nie** , stosowana będzie kombinacja podatku z wypożyczającego podmiotu prawnego.</span><span class="sxs-lookup"><span data-stu-id="b8a83-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="b8a83-113">Jeśli ten sam parametr ma ustawioną wartość **Docelowy** , będzie używana kombinacja podatku dla podmiotu prawnego wypożyczającego.</span><span class="sxs-lookup"><span data-stu-id="b8a83-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="b8a83-114">W przypadku podmiotów prawnych w Stanach Zjednoczonych, gdy parametr jest ustawiony na wartość **Źródło** , to w polu **Należny podatek od sprzedaży** musi być skonfigurowana nowa strona **Grup księgowania w rejestrze**.</span><span class="sxs-lookup"><span data-stu-id="b8a83-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="b8a83-115">Silnik do księgowania użyje informacji z tego pola do prowadzania rachunków związanych z podatkami.</span><span class="sxs-lookup"><span data-stu-id="b8a83-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="b8a83-116">Zachowanie to jest spójne w przypadku wierszy wydatków zaksięgowanych z użyciem projektu lub bez niego.</span><span class="sxs-lookup"><span data-stu-id="b8a83-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
