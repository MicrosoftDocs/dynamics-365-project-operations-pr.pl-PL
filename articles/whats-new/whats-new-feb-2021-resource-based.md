---
title: 'Nowości: luty 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów'
description: Ten temat zawiera informacje o aktualizacjach dotyczących jakości dostępnych w wersji Project Operations ze luty 2021 r. w scenariuszach dotyczących zasobów/braku zapasów.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141339"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="fce50-103">Nowości: luty 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów</span><span class="sxs-lookup"><span data-stu-id="fce50-103">What's new February 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="fce50-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="fce50-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fce50-105">Ten temat dotyczy następujących składników i wersji aplikacji Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="fce50-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="fce50-106">Project Operations w środowisku Dataverse 4.7.0.95</span><span class="sxs-lookup"><span data-stu-id="fce50-106">Project Operations on Dataverse environment 4.7.0.95</span></span>
- <span data-ttu-id="fce50-107">Zarządzanie projektami i ich księgowanie w wersji 10.0.16 środowiska Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="fce50-107">Project management and accounting in Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="fce50-108">Aktualizacje dotyczące jakości</span><span class="sxs-lookup"><span data-stu-id="fce50-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="fce50-109">Project Operations w usłudze Dataverse</span><span class="sxs-lookup"><span data-stu-id="fce50-109">Project Operations on Dataverse</span></span>

| <span data-ttu-id="fce50-110">**Obszar funkcji**</span><span class="sxs-lookup"><span data-stu-id="fce50-110">**Feature Area**</span></span> | <span data-ttu-id="fce50-111">**Numer referencyjny**</span><span class="sxs-lookup"><span data-stu-id="fce50-111">**Reference number**</span></span> | <span data-ttu-id="fce50-112">**Aktualizacja dotycząca jakości**</span><span class="sxs-lookup"><span data-stu-id="fce50-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fce50-113">**Rozliczenia i ceny**</span><span class="sxs-lookup"><span data-stu-id="fce50-113">**Billing and Pricing**</span></span> | <span data-ttu-id="fce50-114">2053736</span><span class="sxs-lookup"><span data-stu-id="fce50-114">2053736</span></span> | <span data-ttu-id="fce50-115">Szczegółowe informacje o wierszu faktury są teraz dostępne, przechodząc do **Faktura** > **Pokrewne informacje**.</span><span class="sxs-lookup"><span data-stu-id="fce50-115">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="fce50-116">**Rozliczenia i ceny**</span><span class="sxs-lookup"><span data-stu-id="fce50-116">**Billing and Pricing**</span></span> | <span data-ttu-id="fce50-117">2122613</span><span class="sxs-lookup"><span data-stu-id="fce50-117">2122613</span></span> | <span data-ttu-id="fce50-118">Akcje **Aktywowanie** i **Dezaktywowanie** zostały usunięte z encji skojarzenia **Cennik**.</span><span class="sxs-lookup"><span data-stu-id="fce50-118">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="fce50-119">**Rozliczenia i ceny**</span><span class="sxs-lookup"><span data-stu-id="fce50-119">**Billing and Pricing**</span></span> | <span data-ttu-id="fce50-120">2128606</span><span class="sxs-lookup"><span data-stu-id="fce50-120">2128606</span></span> | <span data-ttu-id="fce50-121">Rozwiązano problem **ullReferenceException** w dodatku plug-in **GetEferenceatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="fce50-121">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="fce50-122">**Wdrażanie i konfiguracja**</span><span class="sxs-lookup"><span data-stu-id="fce50-122">**Deployment and configuration**</span></span> | <span data-ttu-id="fce50-123">2139346</span><span class="sxs-lookup"><span data-stu-id="fce50-123">2139346</span></span> | <span data-ttu-id="fce50-124">Rozwiązano problem z importowaniem niezaimportowanego rozwiązania **Dynamics365ProjectOperationsDualWrite**.</span><span class="sxs-lookup"><span data-stu-id="fce50-124">Resolved the issue with importing unmanaged **Dynamics365ProjectOperationsDualWrite** solution.</span></span> |
| <span data-ttu-id="fce50-125">**Wdrażanie i konfiguracja**</span><span class="sxs-lookup"><span data-stu-id="fce50-125">**Deployment and configuration**</span></span> | <span data-ttu-id="fce50-126">2140569</span><span class="sxs-lookup"><span data-stu-id="fce50-126">2140569</span></span> | <span data-ttu-id="fce50-127">Rozwiązanie projektu nie może być zainstalowane w środowiskach Dataverse Teams.</span><span class="sxs-lookup"><span data-stu-id="fce50-127">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="fce50-128">**Wdrażanie i konfiguracja**</span><span class="sxs-lookup"><span data-stu-id="fce50-128">**Deployment and configuration**</span></span> | <span data-ttu-id="fce50-129">2086991</span><span class="sxs-lookup"><span data-stu-id="fce50-129">2086991</span></span> | <span data-ttu-id="fce50-130">Ograniczone dostosowywanie lokalizacji zasobów sieci Web.</span><span class="sxs-lookup"><span data-stu-id="fce50-130">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="fce50-131">**Zarządzanie szansami sprzedaży**</span><span class="sxs-lookup"><span data-stu-id="fce50-131">**Opportunity Management**</span></span> | <span data-ttu-id="fce50-132">2136794</span><span class="sxs-lookup"><span data-stu-id="fce50-132">2136794</span></span> | <span data-ttu-id="fce50-133">Wyświetl poprawny komunikat o błędzie, gdy nie powiedzie się proces **Potwierdź fakturę** lub **Oznacz fakturę jako zapłaconą**.</span><span class="sxs-lookup"><span data-stu-id="fce50-133">Display the correct error message when the **Confirm invoice** or **Mark invoice as paid** processes fail.</span></span> |
| <span data-ttu-id="fce50-134">**Zarządzanie szansami sprzedaży**</span><span class="sxs-lookup"><span data-stu-id="fce50-134">**Opportunity Management**</span></span> | <span data-ttu-id="fce50-135">2139330</span><span class="sxs-lookup"><span data-stu-id="fce50-135">2139330</span></span> | <span data-ttu-id="fce50-136">Zmiana menedżera projektu w projekcie nie może zresetować firmy, która jest właścicielem, do wartości domyślnej.</span><span class="sxs-lookup"><span data-stu-id="fce50-136">Changing the Project manager on a project must not reset the owning company back to the default value.</span></span> |
| <span data-ttu-id="fce50-137">**Zarządzanie szansami sprzedaży**</span><span class="sxs-lookup"><span data-stu-id="fce50-137">**Opportunity Management**</span></span> | <span data-ttu-id="fce50-138">2146376</span><span class="sxs-lookup"><span data-stu-id="fce50-138">2146376</span></span> | <span data-ttu-id="fce50-139">Skorygowana kwota podatku w kwocie niepodlegającej obciążeniu jest tworzona z potwierdzenia faktury.</span><span class="sxs-lookup"><span data-stu-id="fce50-139">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="fce50-140">**Planowanie i śledzenie projektu**</span><span class="sxs-lookup"><span data-stu-id="fce50-140">**Project Planning and Tracking**</span></span> | <span data-ttu-id="fce50-141">2099879</span><span class="sxs-lookup"><span data-stu-id="fce50-141">2099879</span></span> | <span data-ttu-id="fce50-142">Wdrożenie środowiska Dataverse musi utworzyć domyślną kategorię transakcji z identyfikatorem statycznym i nie może losowo wygenerować jednej kategorii dla każdego środowiska.</span><span class="sxs-lookup"><span data-stu-id="fce50-142">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="fce50-143">**Planowanie i śledzenie projektu**</span><span class="sxs-lookup"><span data-stu-id="fce50-143">**Project Planning and Tracking**</span></span> | <span data-ttu-id="fce50-144">2128577</span><span class="sxs-lookup"><span data-stu-id="fce50-144">2128577</span></span> | <span data-ttu-id="fce50-145">Naprawiono uprawnienia użytkownika usługi Project Service, aby zaktualizować kategorię transakcji w przypisaniu zasobu.</span><span class="sxs-lookup"><span data-stu-id="fce50-145">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="fce50-146">**Planowanie i śledzenie projektu**</span><span class="sxs-lookup"><span data-stu-id="fce50-146">**Project Planning and Tracking**</span></span> | <span data-ttu-id="fce50-147">2164035</span><span class="sxs-lookup"><span data-stu-id="fce50-147">2164035</span></span> | <span data-ttu-id="fce50-148">Rozwiązano problemy z funkcją **Kopiowanie projektu**.</span><span class="sxs-lookup"><span data-stu-id="fce50-148">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="fce50-149">**Wpis czasu**</span><span class="sxs-lookup"><span data-stu-id="fce50-149">**Time entry**</span></span> | <span data-ttu-id="fce50-150">2129161</span><span class="sxs-lookup"><span data-stu-id="fce50-150">2129161</span></span> | <span data-ttu-id="fce50-151">Stosuje się bardziej ścisłe ograniczenia, aby zagwarantować, że użytkownicy nie mogą zmienić ani zaktualizować wpisu czasu przesłanego lub zatwierdzonego.</span><span class="sxs-lookup"><span data-stu-id="fce50-151">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="fce50-152">**Wpis czasu**</span><span class="sxs-lookup"><span data-stu-id="fce50-152">**Time entry**</span></span> | <span data-ttu-id="fce50-153">2103572</span><span class="sxs-lookup"><span data-stu-id="fce50-153">2103572</span></span> | <span data-ttu-id="fce50-154">Zatwierdzenie przez czas wpisów czasu, które nie dotyczącą projektu, nie może być szukane przez rolę osoby zatwierdzającej projekt.</span><span class="sxs-lookup"><span data-stu-id="fce50-154">Time approval for non-project time entries must not be looking for project approver role.</span></span> |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a><span data-ttu-id="fce50-155">Omówienie zarządzania projektami i księgowania w Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="fce50-155">Project management and accounting in Dynamics 365 Finance</span></span> 

<span data-ttu-id="fce50-156">Aby uzyskać więcej informacji o zarządzaniu projektami i księgowością w Dynamics 365 Finance, zobacz [Nowości: styczeń 2021 r. — Project Operations dla scenariuszy dotyczących zasobów/braku zapasów](whats-new-jan-2021-resource-based.md).</span><span class="sxs-lookup"><span data-stu-id="fce50-156">For more information about Project management and accounting in Dynamics 365 Finance, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>


## <a name="regulatory-updates"></a><span data-ttu-id="fce50-157">Aktualizacje dotyczące regulacji</span><span class="sxs-lookup"><span data-stu-id="fce50-157">Regulatory updates</span></span>

<span data-ttu-id="fce50-158">Aby uzyskać więcej informacji na temat aktualizacji dotyczących aplikacji Finance and Operations, zobacz artykuł dotyczący [Aktualizacje dotyczące regulacji](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span><span class="sxs-lookup"><span data-stu-id="fce50-158">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="fce50-159">Innym sposobem uzyskania informacji o aktualizacjach regulacyjnych jest zalogowanie się do Lifecycle Services (LCS) i wyświetlenie planowanych aktualizacji prawnych za pomocą narzędzia do wyszukiwania problemów.</span><span class="sxs-lookup"><span data-stu-id="fce50-159">Another way to learn about regulatory updates is to sign in to Lifecycle Services (LCS) and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="fce50-160">Funkcja wyszukiwanie problemów umożliwia wyszukiwanie według kraju, typu funkcji oraz wydania.</span><span class="sxs-lookup"><span data-stu-id="fce50-160">Issue search lets you search by country, type of feature, and release.</span></span>