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
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278881"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="eecad-103">Omówienie rozpoznawania przychodów</span><span class="sxs-lookup"><span data-stu-id="eecad-103">Revenue recognition overview</span></span>

<span data-ttu-id="eecad-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="eecad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eecad-105">W aplikacji Dynamics 365 Project Operations zasady rozpoznawania przychodów różnią się w zależności od wybranej metody fakturowania dla projektu lub części projektu.</span><span class="sxs-lookup"><span data-stu-id="eecad-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="eecad-106">W tym temacie zamieszczono informacje dotyczące rozpoznawania przychodów w aplikacji Project Operations.</span><span class="sxs-lookup"><span data-stu-id="eecad-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="eecad-107">Transakcje rozliczane za pomocą metody rozliczania transakcji czasu i materiałów</span><span class="sxs-lookup"><span data-stu-id="eecad-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="eecad-108">Funkcje rozpoznawania kosztów i przychodów są połączone.</span><span class="sxs-lookup"><span data-stu-id="eecad-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="eecad-109">Koszt transakcji i sprzedaż nierozliczona są księgowane przy użyciu [arkusza integracja aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="eecad-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="eecad-110">Koszty projektu i profil przychodów określają, czy nierozliczone transakcje sprzedaży są księgowane w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="eecad-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="eecad-111">Jeśli wybrano pozycję **Przychód naliczony**, system używa kont **Wartość sprzedaży PWT** i **Wartość sprzedaży naliczonego przychodu** podczas księgowania.</span><span class="sxs-lookup"><span data-stu-id="eecad-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="eecad-112">Poniżej znajduje się przykład tej metody.</span><span class="sxs-lookup"><span data-stu-id="eecad-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="eecad-113">Typ transakcji</span><span class="sxs-lookup"><span data-stu-id="eecad-113">Transaction type</span></span> | <span data-ttu-id="eecad-114">Obciążenie/uznanie</span><span class="sxs-lookup"><span data-stu-id="eecad-114">Debit/Credit</span></span> | <span data-ttu-id="eecad-115">Kwota</span><span class="sxs-lookup"><span data-stu-id="eecad-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="eecad-116">Wartość sprzedaży PWT</span><span class="sxs-lookup"><span data-stu-id="eecad-116">WIP Sales value</span></span> | <span data-ttu-id="eecad-117">Obciążenie</span><span class="sxs-lookup"><span data-stu-id="eecad-117">Debit</span></span> | <span data-ttu-id="eecad-118">100</span><span class="sxs-lookup"><span data-stu-id="eecad-118">100</span></span> |
  | <span data-ttu-id="eecad-119">Wartość sprzedaży naliczonego przychodu</span><span class="sxs-lookup"><span data-stu-id="eecad-119">Accrued revenue sales value</span></span> | <span data-ttu-id="eecad-120">Uznanie</span><span class="sxs-lookup"><span data-stu-id="eecad-120">Credit</span></span> | <span data-ttu-id="eecad-121">100</span><span class="sxs-lookup"><span data-stu-id="eecad-121">100</span></span> |

- <span data-ttu-id="eecad-122">Przychód jest rozpoznawany podczas fakturowania.</span><span class="sxs-lookup"><span data-stu-id="eecad-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="eecad-123">System używa konta **Zafakturowany przychód** podczas księgowania.</span><span class="sxs-lookup"><span data-stu-id="eecad-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="eecad-124">Poniżej znajduje się przykład tej metody.</span><span class="sxs-lookup"><span data-stu-id="eecad-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="eecad-125">Typ transakcji</span><span class="sxs-lookup"><span data-stu-id="eecad-125">Transaction type</span></span> | <span data-ttu-id="eecad-126">Obciążenie/uznanie</span><span class="sxs-lookup"><span data-stu-id="eecad-126">Debit/Credit</span></span> | <span data-ttu-id="eecad-127">Kwota</span><span class="sxs-lookup"><span data-stu-id="eecad-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="eecad-128">Saldo klienta</span><span class="sxs-lookup"><span data-stu-id="eecad-128">Customer balance</span></span> | <span data-ttu-id="eecad-129">Obciążenie</span><span class="sxs-lookup"><span data-stu-id="eecad-129">Debit</span></span> | <span data-ttu-id="eecad-130">120</span><span class="sxs-lookup"><span data-stu-id="eecad-130">120</span></span> |
  | <span data-ttu-id="eecad-131">Podatek do zapłacenia</span><span class="sxs-lookup"><span data-stu-id="eecad-131">Sales tax payable</span></span> | <span data-ttu-id="eecad-132">Uznanie</span><span class="sxs-lookup"><span data-stu-id="eecad-132">Credit</span></span> | <span data-ttu-id="eecad-133">20</span><span class="sxs-lookup"><span data-stu-id="eecad-133">20</span></span> |
  | <span data-ttu-id="eecad-134">Zafakturowany przychód</span><span class="sxs-lookup"><span data-stu-id="eecad-134">Invoiced Revenue</span></span> | <span data-ttu-id="eecad-135">Uznanie</span><span class="sxs-lookup"><span data-stu-id="eecad-135">Credit</span></span> | <span data-ttu-id="eecad-136">100</span><span class="sxs-lookup"><span data-stu-id="eecad-136">100</span></span> |

- <span data-ttu-id="eecad-137">Jeśli przychód został naliczony podczas księgowania sprzedaży nierozliczonej, system wycofa przychód naliczony przy fakturowaniu.</span><span class="sxs-lookup"><span data-stu-id="eecad-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="eecad-138">Typ transakcji</span><span class="sxs-lookup"><span data-stu-id="eecad-138">Transaction type</span></span> | <span data-ttu-id="eecad-139">Obciążenie/uznanie</span><span class="sxs-lookup"><span data-stu-id="eecad-139">Debit/Credit</span></span> | <span data-ttu-id="eecad-140">Kwota</span><span class="sxs-lookup"><span data-stu-id="eecad-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="eecad-141">Wartość sprzedaży PWT</span><span class="sxs-lookup"><span data-stu-id="eecad-141">WIP Sales value</span></span> | <span data-ttu-id="eecad-142">Uznanie</span><span class="sxs-lookup"><span data-stu-id="eecad-142">Credit</span></span> | <span data-ttu-id="eecad-143">100</span><span class="sxs-lookup"><span data-stu-id="eecad-143">100</span></span> |
  | <span data-ttu-id="eecad-144">Wartość sprzedaży naliczonego przychodu</span><span class="sxs-lookup"><span data-stu-id="eecad-144">Accrued revenue sales value</span></span> | <span data-ttu-id="eecad-145">Obciążenie</span><span class="sxs-lookup"><span data-stu-id="eecad-145">Debit</span></span> | <span data-ttu-id="eecad-146">100</span><span class="sxs-lookup"><span data-stu-id="eecad-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="eecad-147">Transakcje rozliczane za pomocą metody rozliczania transakcji o stałej cenie</span><span class="sxs-lookup"><span data-stu-id="eecad-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="eecad-148">Funkcje rozpoznawania kosztów i przychodów są rozdzielone.</span><span class="sxs-lookup"><span data-stu-id="eecad-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="eecad-149">Koszt transakcji jest księgowany przy użyciu [arkusza integracja aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="eecad-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="eecad-150">Nierozliczone transakcje sprzedaży nie są tworzone.</span><span class="sxs-lookup"><span data-stu-id="eecad-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="eecad-151">Przychód można rozpoznać podczas fakturowania, jeśli koszty projektu i profil przychodów mają **zasadę używaną do obliczeń wykonania projektu** ustawioną na **Brak PWT**.</span><span class="sxs-lookup"><span data-stu-id="eecad-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="eecad-152">Używaj tej metody tylko dla krótkoterminowych, prostych projektów.</span><span class="sxs-lookup"><span data-stu-id="eecad-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="eecad-153">Przychody można rozpoznać przy użyciu szacowanych przychodów o stałej cenie za pomocą metody **Kontrakt ukończony** lub **Procent ukończenia — rozpoznawanie przychodów**.</span><span class="sxs-lookup"><span data-stu-id="eecad-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eecad-154">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="eecad-154">Additional resources</span></span>
[<span data-ttu-id="eecad-155">Konfigurowanie księgowania projektów do zafakturowania (artykuł)</span><span class="sxs-lookup"><span data-stu-id="eecad-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="eecad-156">Szacowane projekty przychodów o stałej cenie</span><span class="sxs-lookup"><span data-stu-id="eecad-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="eecad-157">Zarządzanie szacowaniami przychodów</span><span class="sxs-lookup"><span data-stu-id="eecad-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="eecad-158">Metody dotyczące kosztów wykonania</span><span class="sxs-lookup"><span data-stu-id="eecad-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]