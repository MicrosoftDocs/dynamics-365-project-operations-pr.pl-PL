---
title: Zapytanie dotyczące środków federalnych
description: Ten temat zawiera informacje na temat zapytania dotyczącego środków federalnych.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288977"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="ea56e-103">Zapytanie dotyczące środków federalnych</span><span class="sxs-lookup"><span data-stu-id="ea56e-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea56e-104">Zgodnie z dyrektywą A-133 Urzędu zarządzania i budżetu, agencje, które otrzymują fundusze federalne, podlegają obowiązkom przeprowadzenia audytu, które są również określane jako pojedyncze kontrole.</span><span class="sxs-lookup"><span data-stu-id="ea56e-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="ea56e-105">Proces audytu jest wykorzystywany w celu cyklicznego tworzenia sprawozdań na temat dochodów i wydatków w ramach grantów federalnych.</span><span class="sxs-lookup"><span data-stu-id="ea56e-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="ea56e-106">Część raportu dotyczącego pojedynczego audytu zawiera zestawienie wydatków w ramach środków federalnych (SEFA).</span><span class="sxs-lookup"><span data-stu-id="ea56e-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="ea56e-107">Zestawienie wydatków w ramach środków federalnych zawiera katalog Federalnej pomocy krajowej (CFDA), tytuł i numer, numer grantu, rok przyznania, nazwę agencji Federalnej, która dostarcza fundusze, oraz nazwę jednostki przekazującej dane.</span><span class="sxs-lookup"><span data-stu-id="ea56e-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="ea56e-108">Zapytanie dotyczy określonego okresu.</span><span class="sxs-lookup"><span data-stu-id="ea56e-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="ea56e-109">Zazwyczaj ten okres jest taki sam, jak okres sprawozdania finansowego, czyli rok obrachunkowy.</span><span class="sxs-lookup"><span data-stu-id="ea56e-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="ea56e-110">Zapytanie dotyczy także grantów z przewidywanymi datami realizacji w wybranym zakresie.</span><span class="sxs-lookup"><span data-stu-id="ea56e-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="ea56e-111">Kolumna **Przyznająca agencja** w zapytaniu wskazuje klienta grantu lub, w ramach grantu przekazywanego, agencję przyznającą grant.</span><span class="sxs-lookup"><span data-stu-id="ea56e-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="ea56e-112">W przypadku grantu przekazywanego, kolumna **Agencja przekazująca** wskazuje klienta grantu.</span><span class="sxs-lookup"><span data-stu-id="ea56e-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="ea56e-113">Jeśli grant jest inny niż przekazywany, kolumna **Agencja przekazująca** jest pusta.</span><span class="sxs-lookup"><span data-stu-id="ea56e-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="ea56e-114">Konfiguracja klastrów CFDA</span><span class="sxs-lookup"><span data-stu-id="ea56e-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="ea56e-115">Konieczne jest skonfigurowanie klastrów CFDA, które mogą być skojarzone z numerami CFDA w zapytaniu dotyczącym zestawienia wydatków w ramach środków federalnych.</span><span class="sxs-lookup"><span data-stu-id="ea56e-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="ea56e-116">Wybierz kolejno pozycje **Zarządzanie projektami i księgowanie \> Konfiguracja \> Granty \> Katalog klastrów federalnej pomocy krajowej**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="ea56e-117">Aby utworzyć nowy klastr CFDA wybierz opcję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="ea56e-118">Wprowadź nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ea56e-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="ea56e-119">Wybierz **Zapisz**, aby zapisać zmiany.</span><span class="sxs-lookup"><span data-stu-id="ea56e-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="ea56e-120">Konfigurowanie numerów CFDA</span><span class="sxs-lookup"><span data-stu-id="ea56e-120">Set up CFDA numbers</span></span>

<span data-ttu-id="ea56e-121">Konieczne jest skonfigurowanie numerów CFDA, które będą dodane do grantów i zawarte w zapytaniu dotyczącym zestawienia wydatków w ramach środków federalnych.</span><span class="sxs-lookup"><span data-stu-id="ea56e-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="ea56e-122">Wybierz kolejno pozycje **Zarządzanie projektami i księgowanie \> Konfiguracja \> Granty \> Numery katalogu federalnej pomocy krajowej**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="ea56e-123">Wybierz opcję **Nowy**, aby nadać numer CFDA.</span><span class="sxs-lookup"><span data-stu-id="ea56e-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="ea56e-124">W kolumnie **Liczba** wprowadź numer CFDA.</span><span class="sxs-lookup"><span data-stu-id="ea56e-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="ea56e-125">Naciśnij klawisz **Tab**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="ea56e-126">W kolumnie **Opis** wprowadź tytuł CFDA.</span><span class="sxs-lookup"><span data-stu-id="ea56e-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="ea56e-127">Naciśnij klawisz **Tab**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="ea56e-128">Opcjonalnie: w polu **Klaster programów** dodaj odpowiedni klaster CFDA.</span><span class="sxs-lookup"><span data-stu-id="ea56e-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="ea56e-129">Wybierz **Zapisz**, aby zapisać zmiany.</span><span class="sxs-lookup"><span data-stu-id="ea56e-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="ea56e-130">Konfigurowanie grantów na potrzeby sporządzania raportów na temat zestawień wydatków w ramach środków federalnych</span><span class="sxs-lookup"><span data-stu-id="ea56e-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="ea56e-131">W tym celu należy przejść do obszaru **Zarządzanie projektami i księgowanie \> Granty \> Granty** oraz wybrać istniejący grant.</span><span class="sxs-lookup"><span data-stu-id="ea56e-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="ea56e-132">Na skróconej karcie **Konfiguracja** w polu **Katalog federalnej pomocy krajowej** przypisz numer CFDA.</span><span class="sxs-lookup"><span data-stu-id="ea56e-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="ea56e-133">Numer CFDA określa raportowany klaster CFDA.</span><span class="sxs-lookup"><span data-stu-id="ea56e-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="ea56e-134">Na skróconej karcie **Informacje kontaktowe** FastTab wprowadź informacje dotyczące podmiotu udzielającego grant, wykonując następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="ea56e-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="ea56e-135">W polu **Klient grantu** wprowadź klienta, który jest odpowiedzialny za grant.</span><span class="sxs-lookup"><span data-stu-id="ea56e-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="ea56e-136">W przypadku istniejącego grantu te informacje mogą być już wprowadzane.</span><span class="sxs-lookup"><span data-stu-id="ea56e-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="ea56e-137">Wskazuje, czy dany klient jest fundatorem.</span><span class="sxs-lookup"><span data-stu-id="ea56e-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="ea56e-138">Jeśli dany klient jest fundatorem, pole **Przekazanie** powinno być czyste.</span><span class="sxs-lookup"><span data-stu-id="ea56e-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="ea56e-139">Jeśli fundatorem jest inny klient, a klient grantu jest odpowiedzialny za wydanie i śledzenie funduszy, pole **Przekazanie** powinno być zaznaczone.</span><span class="sxs-lookup"><span data-stu-id="ea56e-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="ea56e-140">Jeśli wybrano pole **Przekazanie** w poprzednim kroku, w polu **Agencja przyznająca grant** wprowadź klienta, który przekazał grant.</span><span class="sxs-lookup"><span data-stu-id="ea56e-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="ea56e-141">Agencja przyznająca grant i klient grantu nie może być tym samym podmiotem.</span><span class="sxs-lookup"><span data-stu-id="ea56e-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="ea56e-142">Oto przykład grantu przekazanego:</span><span class="sxs-lookup"><span data-stu-id="ea56e-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="ea56e-143">Rząd federalny finansuje projekt infrastrukturalny w danym stanie.</span><span class="sxs-lookup"><span data-stu-id="ea56e-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="ea56e-144">Rząd federalny przyznaje środki do wydania stanowi.</span><span class="sxs-lookup"><span data-stu-id="ea56e-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="ea56e-145">W tym przypadku rząd federalny to organizacja przyznająca grant, a stan jest klientem grantu.</span><span class="sxs-lookup"><span data-stu-id="ea56e-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="ea56e-146">Po pierwszym włączeniu funkcji początkowe numery CFDA będą wprowadzane przy użyciu istniejących numerów dla grantów.</span><span class="sxs-lookup"><span data-stu-id="ea56e-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="ea56e-147">Wyłączenie grantów z raportów SEFA w zależności od typu grantu</span><span class="sxs-lookup"><span data-stu-id="ea56e-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="ea56e-148">Wybierz pozycje **Zarządzanie projektami i księgowanie \> Konfiguracja \> Granty \> Typy grantów**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="ea56e-149">Na skróconej karcie **Informacje domyślne** zaznacz pole **Wyklucz z zapytania dotyczącego zestawienia wydatków w ramach środków federalnych**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="ea56e-150">Wybierz **Zapisz**, aby zapisać zmiany.</span><span class="sxs-lookup"><span data-stu-id="ea56e-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="ea56e-151">Uruchamianie zapytania dotyczącego środków federalnych</span><span class="sxs-lookup"><span data-stu-id="ea56e-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="ea56e-152">Przejdź do **Zarządzanie projektami i księgowanie \> Zapytania i raporty \> Zapytanie grantowe \> Zapytanie dotyczące wydatków w ramach środków federalnych**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="ea56e-153">W sekcji **Parametry** postępuj zgodnie z poniższymi krokami:</span><span class="sxs-lookup"><span data-stu-id="ea56e-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="ea56e-154">W polu **Zakres da** wybierz kod interwału dat.</span><span class="sxs-lookup"><span data-stu-id="ea56e-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="ea56e-155">Można też określić interwał daty w polach **Data od** oraz **Data do**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="ea56e-156">Opcjonalnie: aby uwzględnić w zapytaniu tylko transakcje zafakturowane jako przychód , należy ustawić opcję **Dołącz tylko rozliczone przychody** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="ea56e-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="ea56e-157">Kolumny</span><span class="sxs-lookup"><span data-stu-id="ea56e-157">Columns</span></span>

<span data-ttu-id="ea56e-158">Zapytanie dotyczące środków federalnych zawiera następujące kolumny:</span><span class="sxs-lookup"><span data-stu-id="ea56e-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="ea56e-159">Nazwa klastra katalogu federalnej pomocy krajowej</span><span class="sxs-lookup"><span data-stu-id="ea56e-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="ea56e-160">Agencja udzielająca grantu</span><span class="sxs-lookup"><span data-stu-id="ea56e-160">Grantor agency</span></span>
- <span data-ttu-id="ea56e-161">Agencja przekazująca</span><span class="sxs-lookup"><span data-stu-id="ea56e-161">Pass-through agency</span></span>
- <span data-ttu-id="ea56e-162">Nazwa grantu</span><span class="sxs-lookup"><span data-stu-id="ea56e-162">Grant name</span></span>
- <span data-ttu-id="ea56e-163">Identyfikator grantu</span><span class="sxs-lookup"><span data-stu-id="ea56e-163">Grant ID</span></span>
- <span data-ttu-id="ea56e-164">Identyfikator przyznania grantu</span><span class="sxs-lookup"><span data-stu-id="ea56e-164">Grant application ID</span></span>
- <span data-ttu-id="ea56e-165">Katalog federalnej pomocy krajowej</span><span class="sxs-lookup"><span data-stu-id="ea56e-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="ea56e-166">Paragony</span><span class="sxs-lookup"><span data-stu-id="ea56e-166">Receipts</span></span>
- <span data-ttu-id="ea56e-167">Wydatki</span><span class="sxs-lookup"><span data-stu-id="ea56e-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]