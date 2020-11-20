---
title: Tworzenie i stosowanie warunków zatrzymania płatności u dostawcy
description: W tym temacie zamieszczono informacje na temat konfigurowania i zarządzania pozostałymi warunkami zatrzymania dla płatności dostawców.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082149"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="c76c3-103">Tworzenie i stosowanie warunków zatrzymania płatności u dostawcy</span><span class="sxs-lookup"><span data-stu-id="c76c3-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="c76c3-104">Konfigurowanie warunków zatrzymania płatności u dostawcy w ramach projektu jest przydatne w momencie, gdy organizacja chce zachować część płatności dokonanych w ramach danego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c76c3-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="c76c3-105">Jeśli na przykład użytkownik chce wstrzymać płatność dla dostawcy do momentu, aż dostarczany produkt spełniać będzie oczekiwania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c76c3-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="c76c3-106">Warunki zatrzymania płatności dla dostawcy mogą być określone podczas negocjowania kontraktu dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c76c3-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="c76c3-107">Tworzenie warunków zatrzymania płatności dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="c76c3-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="c76c3-108">Istnieje możliwość wprowadzenia wartości procentowej płatności dla dostawcy na potrzeby zatrzymania oraz wartości procentowej poprzednio zatrzymanych kwot, które mają zostać zwolnione.</span><span class="sxs-lookup"><span data-stu-id="c76c3-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="c76c3-109">Kwoty na fakturach dostawców są automatycznie zatrzymywane , dopóki kontrakt nie osiągnie określonego stanu wykonania.</span><span class="sxs-lookup"><span data-stu-id="c76c3-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="c76c3-110">Po skonfigurowaniu warunków zatrzymania można stosować je do wszystkich projektów danego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c76c3-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="c76c3-111">Wykonaj poniższe kroki, aby skonfigurować warunki zatrzymywania płatności dostawcy i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="c76c3-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="c76c3-112">Przejdź do obszaru **Zarządzanie projektami i księgowanie** > **Zatrzymywanie** > **Warunki zatrzymania płatności u dostawcy**.</span><span class="sxs-lookup"><span data-stu-id="c76c3-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="c76c3-113">Wybierz opcję **Nowy** , aby dodać nowy warunek zatrzymania dla dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c76c3-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="c76c3-114">Wartość **Identyfikatora reguły** dla nowego terminu jest wprowadzana automatycznie.</span><span class="sxs-lookup"><span data-stu-id="c76c3-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="c76c3-115">Wprowadź krótki opis w polu **Opis** , a następnie na skróconej karcie **Warunki** wybierz opcję **Dodaj wiersz** w celu wprowadzenia wartości terminów dla następujących kryteriów:</span><span class="sxs-lookup"><span data-stu-id="c76c3-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="c76c3-116">**Procent dostarczonych jednostek** : wprowadź wartość procentową wykonania.</span><span class="sxs-lookup"><span data-stu-id="c76c3-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="c76c3-117">Kwoty na fakturach dostawców są automatycznie zatrzymywane , dopóki kontrakt nie będzie równy określonemu stanowi procentowego wykonania.</span><span class="sxs-lookup"><span data-stu-id="c76c3-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="c76c3-118">Na przykład po wprowadzeniu wartości 50,00 kwoty zostaną zatrzymane, dopóki projekt nie będzie ukończony w 50%.</span><span class="sxs-lookup"><span data-stu-id="c76c3-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="c76c3-119">**Procent do zatrzymania** : wprowadź wartość procentową kwoty faktury od dostawcy, która ma zostać zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="c76c3-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="c76c3-120">Na przykład wprowadzenie wartości 10,00 oznacza, że 10 procent kwoty na fakturze zostanie zatrzymane do momentu, kiedy projekt osiągnie wartość procentową wykonania ustaloną w polu **Procent dostarczonych jednostek**.</span><span class="sxs-lookup"><span data-stu-id="c76c3-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="c76c3-121">**Procent do zwolnienia** : wybierz opcję **Dodaj wiersz** , aby wprowadzić wartość procentową wszelkich poprzednio zatrzymywanych kwot do zwolnienia dla wybranego poziomu wykonania projektu.</span><span class="sxs-lookup"><span data-stu-id="c76c3-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="c76c3-122">Jeśli na różnych poziomach wykonania projektu znajduje się więcej niż jeden punkt kontrolny, dla każdej reguły zatrzymywania wprowadź osobny wiersz warunku zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="c76c3-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="c76c3-123">Każdy wiersz może określać inny procent zatrzymania i inny procent zwolnienia dla każdego określonego poziomu wykonania projektu.</span><span class="sxs-lookup"><span data-stu-id="c76c3-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="c76c3-124">Po utworzeniu warunków zatrzymania dla dostawcy, można stosować je do wszystkich warunków danego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c76c3-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="c76c3-125">Stosowanie warunków zatrzymania do projektu</span><span class="sxs-lookup"><span data-stu-id="c76c3-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="c76c3-126">Przejdź do **Zarządzania projektami i księgowania** > **Projekty** > **Wszystkie projekty** i otwórz projekt na stronie listy projektów.</span><span class="sxs-lookup"><span data-stu-id="c76c3-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="c76c3-127">Na skróconej karcie **Kontrakty z dostawcami** wybierz pozycję **Dodaj wiersz**.</span><span class="sxs-lookup"><span data-stu-id="c76c3-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="c76c3-128">W polu **Wyświetlany kod konta** wybierz jedną z następujących opcji:</span><span class="sxs-lookup"><span data-stu-id="c76c3-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="c76c3-129">**Tabela** : warunki zatrzymania dotyczące dostawcy stosuje się do jednego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c76c3-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="c76c3-130">**Grupa** : warunki zatrzymania dotyczące dostawcy stosuje się do wszystkich dostawców w grupie.</span><span class="sxs-lookup"><span data-stu-id="c76c3-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="c76c3-131">**Wszyscy** : warunki zatrzymania dotyczące dostawcy stosuje się do wszystkich dostawców.</span><span class="sxs-lookup"><span data-stu-id="c76c3-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="c76c3-132">W polu **Dostawca / Grupa dostawców** wybierz dostawcę lub grupę, do których mają mieć zastosowanie warunki zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="c76c3-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="c76c3-133">Jeśli wybrano opcję **Wszyscy** , wtedy to pole jest niedostępne.</span><span class="sxs-lookup"><span data-stu-id="c76c3-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="c76c3-134">W polu **Warunki zatrzymania dla dostawcy** wybierz warunki zatrzymania utworzone w poprzedniej procedurze.</span><span class="sxs-lookup"><span data-stu-id="c76c3-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="c76c3-135">Jeśli w projekcie zdefiniowano również warunki płatności dla dostawcy po uiszczonej opłacie (PWP) dla danego dostawcy, wprowadź procent wartości progowej dla projektu w polu **Procent wartości progowej PWP**.</span><span class="sxs-lookup"><span data-stu-id="c76c3-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="c76c3-136">Warunki zatrzymania dotyczącego dostawcy są również wyświetlane w zamówieniach zakupu tworzonych dla danego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c76c3-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>