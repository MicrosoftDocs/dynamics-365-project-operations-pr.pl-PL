---
title: Zestawy zatwierdzenia
description: Ten temat zawiera informacje na temat zestawu zatwierdzeń, wniosków i podzbiorów tych operacji.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116884"
---
# <a name="approval-sets"></a><span data-ttu-id="27269-103">Zestawy zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="27269-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="27269-104">Zestawy zatwierdzeń grupują żądania zatwierdzenia w mniejsze podzbiory operacji.</span><span class="sxs-lookup"><span data-stu-id="27269-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="27269-105">Takie grupowanie pozwala na przetwarzanie zatwierdzeń w kolejności według Projektu oraz umożliwia ponawianie prób i sekwencjonowanie.</span><span class="sxs-lookup"><span data-stu-id="27269-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="27269-106">Grupowanie poprawia niezawodność i identyfikowalność przetwarzania zatwierdzeń w przypadku dużych ilości zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="27269-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="27269-107">Zestawy zatwierdzeń wskazują ogólny stan przetwarzania powiązanych z nimi rekordów.</span><span class="sxs-lookup"><span data-stu-id="27269-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="27269-108">Po przetworzeniu rekordu zatwierdzenia przy użyciu zestawu zatwierdzeń, rekord zostaje przeniesiony z **Zatwierdzony** do **Zatwierdzony** i zostaje usunięty z zestawu zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="27269-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="27269-109">Jeśli zapis nie powiedzie się podczas przekazywania go do zatwierdzenia, zapis pozostaje w statusie **Przesłany**, a zestaw zatwierdzający jest oznaczony jako nieudany.</span><span class="sxs-lookup"><span data-stu-id="27269-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="27269-110">Zestaw zatwierdzający rejestruje komunikat błędu o niepowodzeniu.</span><span class="sxs-lookup"><span data-stu-id="27269-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="27269-111">Przetwarzanie zatwierdzeń i zestawów zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="27269-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="27269-112">Zatwierdzenia oczekujące w kolejce do przetwarzania widoczne są w widoku **Opracowywanie zatwierdzeń**.</span><span class="sxs-lookup"><span data-stu-id="27269-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="27269-113">System próbuje przetworzyć wszystkie wpisy wiele razy asynchronicznie, w tym ponowić próbę zatwierdzenia, jeśli poprzednie próby zakończyły się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="27269-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="27269-114">Pole **Próby zatwierdzenia ogółem** określa ilość prób, które pozostały do przetworzenia zestawu, zanim zostanie on oznaczony jako nieudany.</span><span class="sxs-lookup"><span data-stu-id="27269-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="27269-115">Nieudane zatwierdzenia i zestawy zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="27269-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="27269-116">Widok **Nieudane zatwierdzenia** zawiera listę wszystkich zatwierdzeń, które wymagają interwencji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="27269-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="27269-117">Otwórz dzienniki powiązanych zestawów zatwierdzeń, aby zidentyfikować przyczynę niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="27269-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="27269-118">Wybranie opcji **Ponów próbę** dodaje wartość do licznika prób zestawu zatwierdzeń, przywraca zestawowi zatwierdzeń status **Przetwarzanie** i próbuje przetworzyć pozostałe rekordy.</span><span class="sxs-lookup"><span data-stu-id="27269-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="27269-119">Konfiguracja zestawów zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="27269-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="27269-120">Włączanie funkcji Zestawów zatwierdzających</span><span class="sxs-lookup"><span data-stu-id="27269-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="27269-121">Przed włączeniem funkcji Zestawy zatwierdzeń należy sprawdzić, czy nie są aktualnie przetwarzane żadne zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="27269-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="27269-122">Przejdź na stronę **Parametry projektu** i wybierz **Kontrola właściwości** > **Włącz nowe zatwierdzenia**.</span><span class="sxs-lookup"><span data-stu-id="27269-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="27269-123">Wyłączanie funkcji Zestawów zatwierdzających</span><span class="sxs-lookup"><span data-stu-id="27269-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="27269-124">Przed wyłączeniem funkcji Zestawy zatwierdzeń należy sprawdzić, czy nie są aktualnie przetwarzane żadne zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="27269-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="27269-125">Przejdź na stronę **Parametry projektu** i wybierz **Kontrola właściwości** > **Wyłącz nowe zatwierdzenia**.</span><span class="sxs-lookup"><span data-stu-id="27269-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="27269-126">Konfiguracja progu asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="27269-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="27269-127">Podczas tworzenia zestawów zatwierdzeń przetwarzanie przechodzi na drugi plan, gdy wybrana liczba rekordów do zatwierdzenia przekroczy wskazany próg.</span><span class="sxs-lookup"><span data-stu-id="27269-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="27269-128">Użyj pola **Próg asynchroniczności**, aby ustalić, czy przetwarzanie zatwierdzeń ma się odbywać synchronicznie czy asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="27269-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="27269-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="27269-129">Valid values are:</span></span>

  - <span data-ttu-id="27269-130">Zero: Wszystkie żądania powinny być przetwarzane asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="27269-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="27269-131">Wartość większa od zera: Zatwierdzenia są przetwarzane asynchronicznie tylko wtedy, gdy przesłana liczba zatwierdzeń przekracza tę wartość.</span><span class="sxs-lookup"><span data-stu-id="27269-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
