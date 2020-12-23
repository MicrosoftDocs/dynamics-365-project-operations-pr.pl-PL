---
title: Aktualizowanie atrybutów dodatków plug-in przy użyciu nowych wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje dotyczące sposobu aktualizowania atrybutów dodatków plug-in o wymiary kalkulacji cen.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643231"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="d98a0-103">Aktualizowanie atrybutów dodatków plug-in przy użyciu nowych wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="d98a0-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="d98a0-104">W tym temacie zamieszczono informacje dotyczące sposobu aktualizowania atrybutów dodatków plug-in o wymiary kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="d98a0-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="d98a0-105">Ta temat ma zastosowanie wyłącznie do funkcji ofert i kontraktów w aplikacji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d98a0-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d98a0-106">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="d98a0-106">Prerequisites</span></span>
<span data-ttu-id="d98a0-107">Przed wykonaniem czynności opisanych w tym temacie należy wykonać procedury opisane w następujących tematach:</span><span class="sxs-lookup"><span data-stu-id="d98a0-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="d98a0-108">Tworzenie niestandardowych pól i encji</span><span class="sxs-lookup"><span data-stu-id="d98a0-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="d98a0-109">Dodawanie pól niestandardowych do ustawień cen i encji transakcyjnych </span><span class="sxs-lookup"><span data-stu-id="d98a0-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="d98a0-110">[Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="d98a0-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="d98a0-111">Jeśli tych procedur jeszcze nie wykonano, wykonaj je, a następnie wróć do tego tematu.</span><span class="sxs-lookup"><span data-stu-id="d98a0-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="d98a0-112">Rejestrowanie dodatku plug-in</span><span class="sxs-lookup"><span data-stu-id="d98a0-112">Register a plug-in</span></span>
<span data-ttu-id="d98a0-113">W przypadku tworzenia szczegółów wiersza oferty na stronie **Wiersz oferty** dla wiersza oferty projektu system tworzy dwa wiersze szacowania.</span><span class="sxs-lookup"><span data-stu-id="d98a0-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="d98a0-114">Jeden wiersz to szacowanie po stronie kosztów, a drugi wiersz — po stronie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="d98a0-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="d98a0-115">To samo dzieje się dla pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="d98a0-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="d98a0-116">Po dokonaniu zmiany w ilości lub w polu po stronie kosztu zmiana jest również dokonywania po stronie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="d98a0-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="d98a0-117">Jest to możliwe, ponieważ dodatki plug-in PreOperations w encjach szczegółów wiersza oferty i szczegółów wiersza kontraktu łączą określone atrybuty po stronie kosztów ze stroną sprzedaży transakcji.</span><span class="sxs-lookup"><span data-stu-id="d98a0-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="d98a0-118">Jeśli zmiany wartości wymiarów kalkulacji cen wprowadzone po stronie sprzedaży mają zostać zastosowane również po stronie kosztów, należy ponownie zarejestrować następujące dodatki plug-in po wprowadzeniu zmian wymiaru kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="d98a0-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="d98a0-119">Oto dodatki plug-in do zaktualizowania i ponownego zarejestrowania:</span><span class="sxs-lookup"><span data-stu-id="d98a0-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="d98a0-120">PreOperationContractLineDetailUpdate — **aktualizuje obiekt msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="d98a0-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="d98a0-121">PreOperationQuoteLineDetailUpdate — **aktualizuje obiekt msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="d98a0-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="d98a0-122">Wykonaj poniższe kroki, aby zaktualizować i ponownie zarejestrować dodatki plug-in.</span><span class="sxs-lookup"><span data-stu-id="d98a0-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="d98a0-123">Otwórz narzędzie **PluginRegistrationTool** i połącz się ze środowiskiem usługi Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d98a0-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="d98a0-124">Wybierz opcję **Wyszukaj** i wpisz kilka pierwszych liter dodatku plug-in, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="d98a0-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="d98a0-125">Po znalezieniu dodatku plug-in zaznacz go, a następnie wybierz opcję **Zaznacz w formularzu głównym**.</span><span class="sxs-lookup"><span data-stu-id="d98a0-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="d98a0-126">Wybierz krok **Aktualizuj obiekt msdyn_orderlinetransaction**, kliknij go prawym przyciskiem myszy, a następnie wybierz opcję **Aktualizuj**.</span><span class="sxs-lookup"><span data-stu-id="d98a0-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="d98a0-127">W oknie dialogowym **Aktualizowanie** wybierz wielokropek (**...**) w atrybutach filtrowania.</span><span class="sxs-lookup"><span data-stu-id="d98a0-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="d98a0-128">Zostanie otwarte okno atrybutów filtrowania z listę wszystkich atrybutów encji i wymiarów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="d98a0-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="d98a0-129">Zaznacz pola wyboru dla atrybutów wymiarów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="d98a0-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="d98a0-130">Wybierz przycisk **OK**, aby zamknąć stronę, a następnie wybierz pozycję **Aktualizuj krok**.</span><span class="sxs-lookup"><span data-stu-id="d98a0-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="d98a0-131">Powtórz kroki 2–7 dla drugiego dodatku plug-in, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="d98a0-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="d98a0-132">Dla tego dodatku plug-in musisz zaktualizować krok **Aktualizuj obiekt msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="d98a0-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="d98a0-133">Zamknij narzędzie **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="d98a0-133">Close **PluginRegistrationTool**.</span></span>
