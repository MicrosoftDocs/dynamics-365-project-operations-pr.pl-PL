---
title: Przetwarzanie paragonów związanych z wydatkami
description: W tym temat przedstawiono informacje na temat przetwarzania paragonów za pomocą technologii OCR. Ta funkcja ma na celu usprawnienie pracy użytkownika podczas tworzenia raportów o wydatkach w Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271816"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="abf69-104">Przetwarzanie paragonów związanych z wydatkami</span><span class="sxs-lookup"><span data-stu-id="abf69-104">Expense receipt processing</span></span>

<span data-ttu-id="abf69-105">Zapis wydatków został ulepszony poprzez wprowadzenie przetwarzania paragonów za pomocą technologii OCR.</span><span class="sxs-lookup"><span data-stu-id="abf69-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="abf69-106">Ta funkcja ma na celu usprawnienie pracy użytkownika podczas tworzenia raportów o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="abf69-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="abf69-107">Kluczowe cechy i funkcje</span><span class="sxs-lookup"><span data-stu-id="abf69-107">Key features</span></span>

- <span data-ttu-id="abf69-108">System wyodrębni nazwę handlową, datę i łączną kwotę z paragonów.</span><span class="sxs-lookup"><span data-stu-id="abf69-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="abf69-109">Funkcja podejmie także próbę dopasowania niedołączonych paragonów do niedołączonych transakcji wydatkowych.</span><span class="sxs-lookup"><span data-stu-id="abf69-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="abf69-110">Użytkownicy mogą tworzyć ręcznie wprowadzone transakcje wydatkowe z paragonów.</span><span class="sxs-lookup"><span data-stu-id="abf69-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="abf69-111">Przykłady użycia</span><span class="sxs-lookup"><span data-stu-id="abf69-111">Usage examples</span></span>

<span data-ttu-id="abf69-112">Aby automatycznie dołączać paragony z uwzględnieniem transakcji kartą kredytową podczas tworzenia raportu z wydatków, należy wykonać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="abf69-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="abf69-113">Otwórz obszar roboczy **Zarządzanie wydatkami**.</span><span class="sxs-lookup"><span data-stu-id="abf69-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="abf69-114">Na karcie **Paragony** sprawdź, czy istnieją niedołączone paragony.</span><span class="sxs-lookup"><span data-stu-id="abf69-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="abf69-115">Możesz również przekazać paragony za pomocą karty **Paragony**.</span><span class="sxs-lookup"><span data-stu-id="abf69-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="abf69-116">Na karcie **Wydatki** sprawdź, czy istnieją niedołączone wydatki.</span><span class="sxs-lookup"><span data-stu-id="abf69-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="abf69-117">Zazwyczaj administrator kosztów importuje te koszty, które otrzymuje od dostawcy karty kredytowej.</span><span class="sxs-lookup"><span data-stu-id="abf69-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="abf69-118">Wybierz **Nowy raport o wydatkach**.</span><span class="sxs-lookup"><span data-stu-id="abf69-118">Select **New expense report**.</span></span> <span data-ttu-id="abf69-119">Należy pamiętać, że podczas tworzenia raportu o wydatkach mogą zostać uwzględnione zarówno koszty, jak i przychody.</span><span class="sxs-lookup"><span data-stu-id="abf69-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="abf69-120">W przypadku dodawania zarówno wydatków jak i paragonów zostanie wyzwolone automatyczne dopasowanie paragonów do wydatków.</span><span class="sxs-lookup"><span data-stu-id="abf69-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="abf69-121">W celu utworzenia wydatku lub dopasowania go do paragonu należy wykonać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="abf69-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="abf69-122">W raporcie z wydatków na karcie **Paragony** dołącz paragon, zaznaczając pole wyboru **Dodaj paragony**.</span><span class="sxs-lookup"><span data-stu-id="abf69-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="abf69-123">W obszarze przekazanego obrazu paragonu zwróć uwagę na opcję **Utwórz** i **Dopasuj**.</span><span class="sxs-lookup"><span data-stu-id="abf69-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="abf69-124">Wybierz opcję **Utwórz**, aby utworzyć ręcznie wprowadzoną transakcję wydatkową i wypełnij wartości wyodrębnione z paragonu.</span><span class="sxs-lookup"><span data-stu-id="abf69-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="abf69-125">W przypadku wybrania opcji **Dopasuj** system podejmie próbę dopasowania istniejących kosztów do paragonu.</span><span class="sxs-lookup"><span data-stu-id="abf69-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="abf69-126">Instalacja</span><span class="sxs-lookup"><span data-stu-id="abf69-126">Installation</span></span>

<span data-ttu-id="abf69-127">Ta funkcja działa wraz z funkcją **Przebudowane raporty wydatków** w celu uproszczenia pracy z wydatkami.</span><span class="sxs-lookup"><span data-stu-id="abf69-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="abf69-128">Ta funkcja jest dostępna tylko dla środowisk w warstwie 2 +, które są piaskownicami lub produkcją.</span><span class="sxs-lookup"><span data-stu-id="abf69-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="abf69-129">Aby wykorzystać te zaawansowane funkcje wydatkowe, należy zainstalować dodatek usługi zarządzania wydatkami (Expense Management Service) dla programu Microsoft Dynamics 365 Finance i włączyć funkcje w wystąpieniu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="abf69-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="abf69-130">Użytkownik może uzyskać dostęp do dodatku z poziomu projektu, korzystając z Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="abf69-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="abf69-131">Zaloguj się do programu LCS i otwórz wybrane środowisko.</span><span class="sxs-lookup"><span data-stu-id="abf69-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="abf69-132">Wybierz pozycję **Wszystkie szczegóły**.</span><span class="sxs-lookup"><span data-stu-id="abf69-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="abf69-133">Wybierz opcję **Zachowaj** lub przewiń w dół do skróconej karty **Dodatków środowiskowych**.</span><span class="sxs-lookup"><span data-stu-id="abf69-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="abf69-134">Wybierz opcję **Zainstaluj nowy dodatek**.</span><span class="sxs-lookup"><span data-stu-id="abf69-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="abf69-135">Wybierz **Expense Management Service**.</span><span class="sxs-lookup"><span data-stu-id="abf69-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="abf69-136">Postępuj zgodnie z instrukcjami zawartymi w przewodniku po instalacji i zgódź się na warunki.</span><span class="sxs-lookup"><span data-stu-id="abf69-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="abf69-137">Wybierz **Zainstaluj**.</span><span class="sxs-lookup"><span data-stu-id="abf69-137">Select **Install**.</span></span>

<span data-ttu-id="abf69-138">W obszarze **Zarządzanie funkcjami** włącz następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="abf69-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="abf69-139">Przebudowane raporty wydatków</span><span class="sxs-lookup"><span data-stu-id="abf69-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="abf69-140">Automatycznie dopasuj koszty i utwórz wydatek z paragonu</span><span class="sxs-lookup"><span data-stu-id="abf69-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="abf69-141">Po włączeniu tych funkcji zostaną wykonane następujące akcje:</span><span class="sxs-lookup"><span data-stu-id="abf69-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="abf69-142">Istniejący obszar roboczy **Zarządzanie wydatkami** zostanie zastąpiony nowym obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="abf69-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="abf69-143">Dodawany jest nowy element menu z widocznością pola wydatku.</span><span class="sxs-lookup"><span data-stu-id="abf69-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="abf69-144">W dalszym ciągu można otworzyć stronę **Raportów wydatków**, przechodząc do **Zarządzania wydatkami > Moje wydatki > Raporty dotyczące wydatków**.</span><span class="sxs-lookup"><span data-stu-id="abf69-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="abf69-145">Przepływy pracy i wszelkie zatwierdzenia wciąż przenoszą użytkownika na stronę istniejących raportów z wydatków.</span><span class="sxs-lookup"><span data-stu-id="abf69-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="abf69-146">Paragony będą przetwarzane za pośrednictwem Microsoft Azure Cognitive Services, a metadane zostaną wyodrębnione i dodane.</span><span class="sxs-lookup"><span data-stu-id="abf69-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="abf69-147">Dodana jest opcja umożliwiająca utworzenie raportu z wydatków, który zawiera dopasowanie do niedołączonych paragonów.</span><span class="sxs-lookup"><span data-stu-id="abf69-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="abf69-148">Opcja dodana do raportów z wydatków umożliwia utworzenie wiersza wydatku na podstawie paragonu lub podjęcie próby dopasowania istniejącego paragonu do istniejącego wiersza wydatku.</span><span class="sxs-lookup"><span data-stu-id="abf69-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="abf69-149">Aby uzyskać więcej informacji na temat funkcji Przebudowanych raporty wydatków, zobacz [Przebudowane raporty wydatków](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="abf69-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="abf69-150">Często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="abf69-150">Frequently asked questions</span></span>

<span data-ttu-id="abf69-151">**Czy firma Microsoft używa moich danych w swoich modelach?**</span><span class="sxs-lookup"><span data-stu-id="abf69-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="abf69-152">Nie, firma Microsoft opracowała ogólny model uczenia maszynowego na potrzeby usługi przetwarzania paragonów.</span><span class="sxs-lookup"><span data-stu-id="abf69-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="abf69-153">Ten model nie jest oparty na analizie przesyłanych przez użytkowników paragonów.</span><span class="sxs-lookup"><span data-stu-id="abf69-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="abf69-154">**Gdzie jest udostępniona ta funkcja i gdzie można przetwarzać dane?**</span><span class="sxs-lookup"><span data-stu-id="abf69-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="abf69-155">Obecnie obsługiwana lokalizacja to Stany Zjednoczone.</span><span class="sxs-lookup"><span data-stu-id="abf69-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="abf69-156">**Gdzie przesyłane są moje paragony?**</span><span class="sxs-lookup"><span data-stu-id="abf69-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="abf69-157">W celu wyodrębnienia danych, Finance kontaktuje się z usługami Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="abf69-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="abf69-158">Cognitive Services zachowają kopie otrzymanego paragonu przez maksymalnie 24 godziny, w czasie których trwać będzie przetwarzanie.</span><span class="sxs-lookup"><span data-stu-id="abf69-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="abf69-159">Po zakończeniu przetwarzania usługi Cognitive Services usuną paragon.</span><span class="sxs-lookup"><span data-stu-id="abf69-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="abf69-160">Paragony są przechowywane w usłudze Finance.</span><span class="sxs-lookup"><span data-stu-id="abf69-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="abf69-161">Aby uzyskać więcej informacji, zobacz temat [Włączanie funkcji rozumienia paragonów korzystając z nowej funkcji dostępnej w Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="abf69-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]