---
title: Tworzenie cennika
description: Tworzenie cennika w Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 08d93ad86d782922df6b22370749628ddbdc0718
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122041"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="fc30c-103">Utwórz cennik (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fc30c-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fc30c-104">Cenniki zapewniają szablon, którego menedżerowie kont mogą używać do tworzenia projektów i ofert, i do określania kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="fc30c-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="fc30c-105">Zapewniają one listę ról i wydatków, oraz ich ceny.</span><span class="sxs-lookup"><span data-stu-id="fc30c-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="fc30c-106">Można utworzyć wiele cenników, aby obsługiwać wiele struktur cenowych przeznaczonych dla różnych regionów, w których są sprzedawane produkty, lub różnych kanałów sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="fc30c-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="fc30c-107">Jest to dobry pomysł, aby utworzyć co najmniej jeden cennik dla każdej waluty, w jakiej planujesz rozliczać się z klientami.</span><span class="sxs-lookup"><span data-stu-id="fc30c-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="fc30c-108">Aby utworzyć szacunki finansowe dla prac, które mają zostać zrealizowane, upewnij się, że każdy projekt ma zapasowy cennik kosztów i sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="fc30c-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="fc30c-109">Zdefiniuj domyślny cennik sprzedaży i kosztów, który ma zastosowanie do wszystkich projektów utworzonych w Twojej organizacji.</span><span class="sxs-lookup"><span data-stu-id="fc30c-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="fc30c-110">Cenniki opierają się na kategoriach wydatków i ról, więc przed utworzeniem cennika, upewnij się, że skonfigurowałeś już role i kategorie wydatków, które mają zostać użyte podczas tworzenia cennika.</span><span class="sxs-lookup"><span data-stu-id="fc30c-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="fc30c-111">Przejdź do **Project Service > Cennik**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="fc30c-112">Kliknij pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="fc30c-113">W **Kontekst**, wybierz, czy jest to cennik dla **Koszty**, **Zakupy**, czy **Sprzedaż**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="fc30c-114">W **Nazwa**, wprowadź nazwę cennika.</span><span class="sxs-lookup"><span data-stu-id="fc30c-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="fc30c-115">W **Waluta**, wybierz walutę, której masz zamiar użyć podczas fakturowania lub wyceny.</span><span class="sxs-lookup"><span data-stu-id="fc30c-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="fc30c-116">W **Jednostka czasu**, podaj okres czasu, którego dotyczy cena, taki jak dzień lub godzina.</span><span class="sxs-lookup"><span data-stu-id="fc30c-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="fc30c-117">W zależności od potrzeb wypełnij **Data rozpoczęcia**, **Data zakończenia**, i **Opis**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="fc30c-118">Kliknij **Zapisz**, aby utworzyć rekord i móc kontynuować jego edycję.</span><span class="sxs-lookup"><span data-stu-id="fc30c-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="fc30c-119">Aby dodać cenę roli do cennika, kliknij **+** w **Ceny ról**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="fc30c-120">W okienku **Cena roli** podaj szczegółowe informacje, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fc30c-121">W razie potrzeby kontynuuj dodawanie cen ról.</span><span class="sxs-lookup"><span data-stu-id="fc30c-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="fc30c-122">Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="fc30c-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="fc30c-123">Aby dodać cenę kategorii wydatek do cennika, kliknij **+** w **Ceny kategorii**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="fc30c-124">W okienku **Cena kategorii transakcji** podaj szczegółowe informacje, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fc30c-125">W razie potrzeby kontynuuj dodawanie cen kategorii.</span><span class="sxs-lookup"><span data-stu-id="fc30c-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="fc30c-126">Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="fc30c-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="fc30c-127">Aby dodać pozycje cennika do cennika, kliknij **+** w **Pozycje cennika**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="fc30c-128">W okienku **Pozycja cennika** podaj szczegółowe informacje, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fc30c-129">W razie potrzeby kontynuuj dodawanie pozycji cennika.</span><span class="sxs-lookup"><span data-stu-id="fc30c-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="fc30c-130">Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="fc30c-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="fc30c-131">Aby dodać relacje terytoriów do cennika, kliknij **+** w **Relacje terytoriów**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="fc30c-132">W okienku **Nowe połączenie** podaj szczegółowe informacje, a następnie kliknij **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="fc30c-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fc30c-133">W razie potrzeby kontynuuj dodawanie relacji terytoriów.</span><span class="sxs-lookup"><span data-stu-id="fc30c-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="fc30c-134">Po skończeniu kliknij **Zapisz** w prawym dolnym rogu ekranu.</span><span class="sxs-lookup"><span data-stu-id="fc30c-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fc30c-135">Zobacz także</span><span class="sxs-lookup"><span data-stu-id="fc30c-135">See Also</span></span>  
 [<span data-ttu-id="fc30c-136">Skonfiguruj Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fc30c-136">Configure Project Service Automation</span></span>](../psa/configure.md)
