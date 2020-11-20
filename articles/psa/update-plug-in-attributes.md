---
title: Aktualizowanie atrybutów dodatków plug-in w celu dołączenia nowych wymiarów kalkulacji cen
description: W tym temacie zamieszczono informacje dotyczące aktualizowania atrybutów dodatków plug-in o wymiary kalkulacji cen.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c42e5fda79d51430f4dedf46037e11c86a38c474
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121861"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="a5de3-103">Aktualizowanie atrybutów dodatków plug-in w celu dołączenia nowych wymiarów kalkulacji cen</span><span class="sxs-lookup"><span data-stu-id="a5de3-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="a5de3-104">Użytkownicy, którzy nie korzystają z funkcji sporządzania ofert i zawierania kontraktów dostępnych w programie Project Service Automation, mogą pominąć tę temat.</span><span class="sxs-lookup"><span data-stu-id="a5de3-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="a5de3-105">W tym temacie założono, że przed rozpoczęciem tej procedury użytkownik wykonał procedury opisane w tematach [Tworzenie niestandardowych pól i encji](create-custom-fields-entities.md), [Dodawanie niestandardowych pól do konfiguracji cen i encji transakcyjnych](field-references.md) oraz [Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="a5de3-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="a5de3-106">Jeśli tych procedur jeszcze nie wykonano, wróć, wykonaj je, a następnie wróć do tego tematu.</span><span class="sxs-lookup"><span data-stu-id="a5de3-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="a5de3-107">Podczas tworzenia szczegółów wiersza oferty na stronie **Wiersz oferty** dla wiersza oferty projektu system tworzy w tle dwa wiersze szacowania — jeden dla strony kosztu oszacowania i jeden dla strony sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="a5de3-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="a5de3-108">To samo dzieje się dla pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="a5de3-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="a5de3-109">Po dokonaniu zmiany w ilości lub w polu po stronie kosztu zmiana jest rozpowszechniana do strony sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="a5de3-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="a5de3-110">Jest to możliwe dzięki następującym dodatkom plug-in, które należy ponownie zarejestrować po modyfikacji wymiarów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="a5de3-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="a5de3-111">PreOperationContractLineDetailUpdate - aktualizuje obiekt **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="a5de3-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="a5de3-112">PreOperationQuoteLineDetailUpdate - aktualizuje obiekt **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="a5de3-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="a5de3-113">W poniższych krokach przedstawiono proces rejestrowania dodatków plug-in.</span><span class="sxs-lookup"><span data-stu-id="a5de3-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="a5de3-114">Otwórz narzędzie **PluginRegistrationTool** i nawiąż połączenie z wystąpieniem online.</span><span class="sxs-lookup"><span data-stu-id="a5de3-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="a5de3-115">Kliknij przycisk **Wyszukaj** i poszukaj dodatku plug-in, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="a5de3-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Zrzut ekranu drzewa wyszukiwania](media/PRT-1.png)

3. <span data-ttu-id="a5de3-117">Po znalezieniu dodatku plug-in zaznacz go, a następnie kliknij opcję **Zaznacz w formularzu głównym**.</span><span class="sxs-lookup"><span data-stu-id="a5de3-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="a5de3-118">Zaznacz krok dodatku plug-in, który chcesz zaktualizować, kliknij prawym przyciskiem myszy, a następnie wybierz opcję **Aktualizuj**.</span><span class="sxs-lookup"><span data-stu-id="a5de3-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Zrzut ekranu z dodatkiem plug-in, który ma zostać zaktualizowany](media/PRT-2.png)
 
5. <span data-ttu-id="a5de3-120">W oknie aktualizowania w atrybutach filtrowania kliknij wielokropek (**...**).</span><span class="sxs-lookup"><span data-stu-id="a5de3-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Zrzut ekranu z informacjami konfiguracyjnymi w oknie Aktualizowanie istniejącego kroku](media/PRT-3.png)
 
6. <span data-ttu-id="a5de3-122">Zaznacz pola wyboru atrybutów kalkulacji cen.</span><span class="sxs-lookup"><span data-stu-id="a5de3-122">Select the pricing attribute check boxes.</span></span>

 ![Zrzut ekranu pokazujący zaznaczenia pól wyboru atrybutów kalkulacji cen](media/PRT-4.png)

7. <span data-ttu-id="a5de3-124">Kliknij przycisk **OK**, aby zamknąć stronę, a następnie wybierz pozycję **Aktualizuj krok**.</span><span class="sxs-lookup"><span data-stu-id="a5de3-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Zrzut ekranu z widocznym przyciskiem „Aktualizuj krok”](media/PRT-5.png)
 
8. <span data-ttu-id="a5de3-126">Powtórz ten proces dla drugiego dodatku plug-in, **PreOperationQuoteLineDetail - aktualizuje obiekt msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="a5de3-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="a5de3-127">Zamknij narzędzie do rejestrowania dodatków plug-in.</span><span class="sxs-lookup"><span data-stu-id="a5de3-127">Close the plug-in registration tool.</span></span>

