---
title: Przechwytywanie potwierdzenia za pomocą funkcji OCR
description: W tym temat przedstawiono informacje na temat przetwarzania paragonów za pomocą technologii OCR.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c7fa8a805acbf7c75edd49c4c49aa159493f525
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002024"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="577a5-103">Przechwytywanie potwierdzenia za pomocą funkcji OCR</span><span class="sxs-lookup"><span data-stu-id="577a5-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="577a5-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="577a5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="577a5-105">Zapis wydatków został ulepszony poprzez wprowadzenie przetwarzania paragonów za pomocą technologii OCR.</span><span class="sxs-lookup"><span data-stu-id="577a5-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="577a5-106">Ta funkcja ma na celu usprawnienie pracy użytkownika podczas tworzenia raportów o wydatkach.</span><span class="sxs-lookup"><span data-stu-id="577a5-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="577a5-107">Kluczowe cechy i funkcje</span><span class="sxs-lookup"><span data-stu-id="577a5-107">Key features</span></span>

- <span data-ttu-id="577a5-108">System wyodrębni nazwę handlową, datę i łączną kwotę z paragonów.</span><span class="sxs-lookup"><span data-stu-id="577a5-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="577a5-109">Podejmie także próbę dopasowania niedołączonych paragonów do niedołączonych transakcji wydatkowych.</span><span class="sxs-lookup"><span data-stu-id="577a5-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="577a5-110">Użytkownik może tworzyć ręcznie wprowadzone transakcje wydatkowe z paragonów.</span><span class="sxs-lookup"><span data-stu-id="577a5-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="577a5-111">Dołączanie paragonów do raportu o wydatkach</span><span class="sxs-lookup"><span data-stu-id="577a5-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="577a5-112">Aby automatycznie dołączać paragony z uwzględnieniem transakcji kartą kredytową podczas tworzenia raportu z wydatków, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="577a5-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="577a5-113">Otwórz obszar roboczy **Zarządzanie wydatkami**.</span><span class="sxs-lookup"><span data-stu-id="577a5-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="577a5-114">Na karcie **Paragony** sprawdź, czy istnieją niedołączone paragony.</span><span class="sxs-lookup"><span data-stu-id="577a5-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="577a5-115">Możesz również przekazać paragony za pomocą karty **Paragony**.</span><span class="sxs-lookup"><span data-stu-id="577a5-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="577a5-116">Na karcie **Wydatki** sprawdź, czy istnieją niedołączone wydatki.</span><span class="sxs-lookup"><span data-stu-id="577a5-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="577a5-117">Zazwyczaj administrator kosztów importuje te koszty, które otrzymuje od dostawcy karty kredytowej.</span><span class="sxs-lookup"><span data-stu-id="577a5-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="577a5-118">Wybierz **Nowy raport o wydatkach**.</span><span class="sxs-lookup"><span data-stu-id="577a5-118">Select **New expense report**.</span></span> <span data-ttu-id="577a5-119">Należy pamiętać, że podczas tworzenia raportu o wydatkach mogą zostać uwzględnione zarówno koszty, jak i przychody.</span><span class="sxs-lookup"><span data-stu-id="577a5-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="577a5-120">W przypadku dodawania zarówno wydatków jak i paragonów zostanie wyzwolone automatyczne dopasowanie paragonów do wydatków.</span><span class="sxs-lookup"><span data-stu-id="577a5-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="577a5-121">Tworzenie lub dopasowanie paragonów do raportu o wydatkach</span><span class="sxs-lookup"><span data-stu-id="577a5-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="577a5-122">W celu utworzenia wydatku lub dopasowania go do paragonu należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="577a5-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="577a5-123">W raporcie z wydatków na karcie **Paragony** dołącz paragon, zaznaczając pole wyboru **Dodaj paragony**.</span><span class="sxs-lookup"><span data-stu-id="577a5-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="577a5-124">W obszarze przekazanego obrazu paragonu zwróć uwagę na opcję **Utwórz** i **Dopasuj**.</span><span class="sxs-lookup"><span data-stu-id="577a5-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="577a5-125">Wybierz opcję **Utwórz**, aby utworzyć ręcznie wprowadzoną transakcję wydatkową i wypełnij wartości wyodrębnione z paragonu.</span><span class="sxs-lookup"><span data-stu-id="577a5-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="577a5-126">W przypadku wybrania opcji **Dopasuj** system podejmie próbę dopasowania istniejących kosztów do paragonu.</span><span class="sxs-lookup"><span data-stu-id="577a5-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="577a5-127">Instalacja</span><span class="sxs-lookup"><span data-stu-id="577a5-127">Installation</span></span>

<span data-ttu-id="577a5-128">Aby wykorzystać te zaawansowane funkcje wydatkowe, należy zainstalować dodatek usługi zarządzania wydatkami (Expense Management Service) dla programu Microsoft Dynamics 365 Finance i włączyć funkcje w wystąpieniu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="577a5-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="577a5-129">Użytkownik może uzyskać dostęp do dodatku z poziomu projektu, korzystając z Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="577a5-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="577a5-130">Zaloguj się do programu LCS i otwórz wybrane środowisko.</span><span class="sxs-lookup"><span data-stu-id="577a5-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="577a5-131">Wybierz pozycję **Wszystkie szczegóły**.</span><span class="sxs-lookup"><span data-stu-id="577a5-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="577a5-132">Wybierz opcję **Zachowaj** lub przewiń w dół do skróconej karty **Dodatków środowiskowych**.</span><span class="sxs-lookup"><span data-stu-id="577a5-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="577a5-133">Wybierz opcję **Zainstaluj nowy dodatek**.</span><span class="sxs-lookup"><span data-stu-id="577a5-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="577a5-134">Wybierz **Expense Management Service**.</span><span class="sxs-lookup"><span data-stu-id="577a5-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="577a5-135">Postępuj zgodnie z instrukcjami zawartymi w przewodniku po instalacji i zgódź się na warunki.</span><span class="sxs-lookup"><span data-stu-id="577a5-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="577a5-136">Wybierz **Zainstaluj**.</span><span class="sxs-lookup"><span data-stu-id="577a5-136">Select **Install**.</span></span>

<span data-ttu-id="577a5-137">W obszarze **Zarządzanie funkcjami** włącz następujące funkcje:</span><span class="sxs-lookup"><span data-stu-id="577a5-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="577a5-138">Przebudowane raporty wydatków</span><span class="sxs-lookup"><span data-stu-id="577a5-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="577a5-139">Automatycznie dopasuj koszty i utwórz wydatek z paragonu</span><span class="sxs-lookup"><span data-stu-id="577a5-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="577a5-140">Po włączeniu tych funkcji zostaną wykonane następujące akcje:</span><span class="sxs-lookup"><span data-stu-id="577a5-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="577a5-141">Istniejący obszar roboczy **Zarządzanie wydatkami** zostanie zastąpiony nowym obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="577a5-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="577a5-142">Dodawany jest nowy element menu z widocznością pola wydatku.</span><span class="sxs-lookup"><span data-stu-id="577a5-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="577a5-143">W dalszym ciągu można otworzyć stronę **Raportów wydatków**, przechodząc do **Zarządzania wydatkami > Moje wydatki > Raporty dotyczące wydatków**.</span><span class="sxs-lookup"><span data-stu-id="577a5-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="577a5-144">Przepływy pracy i wszelkie zatwierdzenia wciąż przenoszą użytkownika na stronę istniejących raportów z wydatków.</span><span class="sxs-lookup"><span data-stu-id="577a5-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="577a5-145">Paragony będą przetwarzane za pośrednictwem Microsoft Azure Cognitive Services, a metadane zostaną wyodrębnione i dodane.</span><span class="sxs-lookup"><span data-stu-id="577a5-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="577a5-146">Dodana jest opcja umożliwiająca utworzenie raportu z wydatków, który zawiera dopasowanie do niedołączonych paragonów.</span><span class="sxs-lookup"><span data-stu-id="577a5-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="577a5-147">Opcja dodana do raportów z wydatków umożliwia utworzenie wiersza wydatku na podstawie paragonu lub podjęcie próby dopasowania istniejącego paragonu do istniejącego wiersza wydatku.</span><span class="sxs-lookup"><span data-stu-id="577a5-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="577a5-148">Często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="577a5-148">Frequently asked questions</span></span>

<span data-ttu-id="577a5-149">**Czy firma Microsoft używa moich danych w swoich modelach?**</span><span class="sxs-lookup"><span data-stu-id="577a5-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="577a5-150">Nie, firma Microsoft opracowała ogólny model uczenia maszynowego na potrzeby usługi przetwarzania paragonów.</span><span class="sxs-lookup"><span data-stu-id="577a5-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="577a5-151">Ten model nie jest oparty na analizie przesyłanych przez użytkowników paragonów.</span><span class="sxs-lookup"><span data-stu-id="577a5-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="577a5-152">**Gdzie jest udostępniona ta funkcja i gdzie można przetwarzać dane?**</span><span class="sxs-lookup"><span data-stu-id="577a5-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="577a5-153">Obecnie obsługiwana lokalizacja to Stany Zjednoczone.</span><span class="sxs-lookup"><span data-stu-id="577a5-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="577a5-154">**Gdzie przesyłane są moje paragony?**</span><span class="sxs-lookup"><span data-stu-id="577a5-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="577a5-155">W celu wyodrębnienia danych, Finance kontaktuje się z usługami Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="577a5-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="577a5-156">Cognitive Services zachowają kopie otrzymanego paragonu przez maksymalnie 24 godziny, w czasie których trwać będzie przetwarzanie.</span><span class="sxs-lookup"><span data-stu-id="577a5-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="577a5-157">Po zakończeniu przetwarzania usługi Cognitive Services usuną paragon.</span><span class="sxs-lookup"><span data-stu-id="577a5-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="577a5-158">Paragony są przechowywane w usłudze Finance.</span><span class="sxs-lookup"><span data-stu-id="577a5-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="577a5-159">Aby uzyskać więcej informacji, zobacz temat [Włączanie funkcji rozumienia paragonów korzystając z nowej funkcji dostępnej w Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="577a5-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
