---
title: Omówienie rozpoznawania przychodów
description: W tym temacie zamieszczono informacje dotyczące rozpoznawania przychodów w aplikacji Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531512"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="e36a1-103">Omówienie rozpoznawania przychodów</span><span class="sxs-lookup"><span data-stu-id="e36a1-103">Revenue recognition overview</span></span>

<span data-ttu-id="e36a1-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="e36a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e36a1-105">W aplikacji Dynamics 365 Project Operations zasady rozpoznawania przychodów różnią się w zależności od wybranej metody fakturowania dla projektu lub części projektu.</span><span class="sxs-lookup"><span data-stu-id="e36a1-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="e36a1-106">W tym temacie zamieszczono informacje dotyczące rozpoznawania przychodów w aplikacji Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e36a1-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="e36a1-107">Transakcje rozliczane za pomocą metody rozliczania transakcji czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="e36a1-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="e36a1-108">Funkcje rozpoznawania kosztów i przychodów są połączone.</span><span class="sxs-lookup"><span data-stu-id="e36a1-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="e36a1-109">Koszt transakcji i sprzedaż nierozliczona są księgowane przy użyciu [arkusza integracja aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="e36a1-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="e36a1-110">Koszty projektu i profil przychodów określają, czy nierozliczone transakcje sprzedaży są księgowane w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="e36a1-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="e36a1-111">Jeśli wybrano pozycję **Przychód naliczony**, system używa kont **Wartość sprzedaży PWT** i **Wartość sprzedaży naliczonego przychodu** podczas księgowania.</span><span class="sxs-lookup"><span data-stu-id="e36a1-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="e36a1-112">Poniżej znajduje się przykład tej metody.</span><span class="sxs-lookup"><span data-stu-id="e36a1-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="e36a1-113">Typ transakcji</span><span class="sxs-lookup"><span data-stu-id="e36a1-113">Transaction type</span></span> | <span data-ttu-id="e36a1-114">Obciążenie/uznanie</span><span class="sxs-lookup"><span data-stu-id="e36a1-114">Debit/Credit</span></span> | <span data-ttu-id="e36a1-115">Kwota</span><span class="sxs-lookup"><span data-stu-id="e36a1-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="e36a1-116">Wartość sprzedaży PWT</span><span class="sxs-lookup"><span data-stu-id="e36a1-116">WIP Sales value</span></span> | <span data-ttu-id="e36a1-117">Obciążenie</span><span class="sxs-lookup"><span data-stu-id="e36a1-117">Debit</span></span> | <span data-ttu-id="e36a1-118">100</span><span class="sxs-lookup"><span data-stu-id="e36a1-118">100</span></span> |
  | <span data-ttu-id="e36a1-119">Wartość sprzedaży naliczonego przychodu</span><span class="sxs-lookup"><span data-stu-id="e36a1-119">Accrued revenue sales value</span></span> | <span data-ttu-id="e36a1-120">Uznanie</span><span class="sxs-lookup"><span data-stu-id="e36a1-120">Credit</span></span> | <span data-ttu-id="e36a1-121">100</span><span class="sxs-lookup"><span data-stu-id="e36a1-121">100</span></span> |

- <span data-ttu-id="e36a1-122">Przychód jest rozpoznawany podczas fakturowania.</span><span class="sxs-lookup"><span data-stu-id="e36a1-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="e36a1-123">System używa konta **Zafakturowany przychód** podczas księgowania.</span><span class="sxs-lookup"><span data-stu-id="e36a1-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="e36a1-124">Poniżej znajduje się przykład tej metody.</span><span class="sxs-lookup"><span data-stu-id="e36a1-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="e36a1-125">Typ transakcji</span><span class="sxs-lookup"><span data-stu-id="e36a1-125">Transaction type</span></span> | <span data-ttu-id="e36a1-126">Obciążenie/uznanie</span><span class="sxs-lookup"><span data-stu-id="e36a1-126">Debit/Credit</span></span> | <span data-ttu-id="e36a1-127">Kwota</span><span class="sxs-lookup"><span data-stu-id="e36a1-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="e36a1-128">Saldo klienta</span><span class="sxs-lookup"><span data-stu-id="e36a1-128">Customer balance</span></span> | <span data-ttu-id="e36a1-129">Obciążenie</span><span class="sxs-lookup"><span data-stu-id="e36a1-129">Debit</span></span> | <span data-ttu-id="e36a1-130">120</span><span class="sxs-lookup"><span data-stu-id="e36a1-130">120</span></span> |
  | <span data-ttu-id="e36a1-131">Podatek do zapłacenia</span><span class="sxs-lookup"><span data-stu-id="e36a1-131">Sales tax payable</span></span> | <span data-ttu-id="e36a1-132">Uznanie</span><span class="sxs-lookup"><span data-stu-id="e36a1-132">Credit</span></span> | <span data-ttu-id="e36a1-133">20</span><span class="sxs-lookup"><span data-stu-id="e36a1-133">20</span></span> |
  | <span data-ttu-id="e36a1-134">Zafakturowany przychód</span><span class="sxs-lookup"><span data-stu-id="e36a1-134">Invoiced Revenue</span></span> | <span data-ttu-id="e36a1-135">Uznanie</span><span class="sxs-lookup"><span data-stu-id="e36a1-135">Credit</span></span> | <span data-ttu-id="e36a1-136">100</span><span class="sxs-lookup"><span data-stu-id="e36a1-136">100</span></span> |

- <span data-ttu-id="e36a1-137">Jeśli przychód został naliczony podczas księgowania sprzedaży nierozliczonej, system wycofa przychód naliczony przy fakturowaniu.</span><span class="sxs-lookup"><span data-stu-id="e36a1-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="e36a1-138">Typ transakcji</span><span class="sxs-lookup"><span data-stu-id="e36a1-138">Transaction type</span></span> | <span data-ttu-id="e36a1-139">Obciążenie/uznanie</span><span class="sxs-lookup"><span data-stu-id="e36a1-139">Debit/Credit</span></span> | <span data-ttu-id="e36a1-140">Kwota</span><span class="sxs-lookup"><span data-stu-id="e36a1-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="e36a1-141">Wartość sprzedaży PWT</span><span class="sxs-lookup"><span data-stu-id="e36a1-141">WIP Sales value</span></span> | <span data-ttu-id="e36a1-142">Uznanie</span><span class="sxs-lookup"><span data-stu-id="e36a1-142">Credit</span></span> | <span data-ttu-id="e36a1-143">100</span><span class="sxs-lookup"><span data-stu-id="e36a1-143">100</span></span> |
  | <span data-ttu-id="e36a1-144">Wartość sprzedaży naliczonego przychodu</span><span class="sxs-lookup"><span data-stu-id="e36a1-144">Accrued revenue sales value</span></span> | <span data-ttu-id="e36a1-145">Obciążenie</span><span class="sxs-lookup"><span data-stu-id="e36a1-145">Debit</span></span> | <span data-ttu-id="e36a1-146">100</span><span class="sxs-lookup"><span data-stu-id="e36a1-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="e36a1-147">Transakcje rozliczane za pomocą metody rozliczania transakcji o stałej cenie</span><span class="sxs-lookup"><span data-stu-id="e36a1-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="e36a1-148">Funkcje rozpoznawania kosztów i przychodów są rozdzielone.</span><span class="sxs-lookup"><span data-stu-id="e36a1-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="e36a1-149">Koszt transakcji jest księgowany przy użyciu [arkusza integracja aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="e36a1-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="e36a1-150">Nierozliczone transakcje sprzedaży nie są tworzone.</span><span class="sxs-lookup"><span data-stu-id="e36a1-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="e36a1-151">Przychód można rozpoznać podczas fakturowania, jeśli koszty projektu i profil przychodów mają **zasadę używaną do obliczeń wykonania projektu** ustawioną na **Brak PWT**.</span><span class="sxs-lookup"><span data-stu-id="e36a1-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="e36a1-152">Używaj tej metody tylko dla krótkoterminowych, prostych projektów.</span><span class="sxs-lookup"><span data-stu-id="e36a1-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="e36a1-153">Przychody można rozpoznać przy użyciu szacowanych przychodów o stałej cenie za pomocą metody **Kontrakt ukończony** lub **Procent ukończenia — rozpoznawanie przychodów**.</span><span class="sxs-lookup"><span data-stu-id="e36a1-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e36a1-154">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="e36a1-154">Additional resources</span></span>
[<span data-ttu-id="e36a1-155">Konfigurowanie księgowania projektów do zafakturowania (artykuł)</span><span class="sxs-lookup"><span data-stu-id="e36a1-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="e36a1-156">Szacowane projekty przychodów o stałej cenie</span><span class="sxs-lookup"><span data-stu-id="e36a1-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="e36a1-157">Zarządzanie szacowaniami przychodów</span><span class="sxs-lookup"><span data-stu-id="e36a1-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="e36a1-158">Metody dotyczące kosztów wykonania</span><span class="sxs-lookup"><span data-stu-id="e36a1-158">Cost to complete methods</span></span>](cost-complete-methods.md)
