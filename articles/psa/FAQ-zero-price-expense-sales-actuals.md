---
title: Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych wydatek sprzedaż?
description: Poniższe trzy kontrole ułatwią rozwiązanie problemu, dlaczego cena wynosi domyślnie 0 w wartościach rzeczywistych wydatek sprzedaż.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 8c2270b07b6f8765a6ec1f506fe1767a1841950b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122086"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a><span data-ttu-id="4dd33-103">Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych wydatek sprzedaż?</span><span class="sxs-lookup"><span data-stu-id="4dd33-103">Why is the price defaulting to zero on expense sales actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4dd33-104">To często zadawane pytanie dotyczy wartości rzeczywistych wydatek, gdzie klasa transakcji jest ustawiona na Wydatek, a typ transakcji to Nierozliczona sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="4dd33-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="4dd33-105">Poniższe trzy kontrole ułatwią rozwiązanie problemu, dlaczego cena (stawka rozliczania) wynosi domyślnie 0 w wartościach rzeczywistych wydatek sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="4dd33-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on expense sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-project"></a><span data-ttu-id="4dd33-106">Kontrola 1: Określ cennik sprzedaży dla projektu</span><span class="sxs-lookup"><span data-stu-id="4dd33-106">Check 1: Identify the sales price list for project</span></span>

<span data-ttu-id="4dd33-107">Znajdź projekt w polu projektu wartości rzeczywistych, a następnie przejdź na stronę projektu.</span><span class="sxs-lookup"><span data-stu-id="4dd33-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="4dd33-108">Następnie przejdź do karty Sprzedaż. Na siatce Pozycje kontraktu projektu kliknij łącze w polu Kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="4dd33-108">Then go to the Sales tab. On the Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="4dd33-109">Zostanie otwarta strona Kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="4dd33-109">The Project Contract page will open.</span></span> <span data-ttu-id="4dd33-110">Na stronie Kontrakt projektu przejdź do karty Cenniki projektu. Sprawdź, czy istnieje co najmniej jeden cennik dołączony w tym miejscu.</span><span class="sxs-lookup"><span data-stu-id="4dd33-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span>

<span data-ttu-id="4dd33-111">Jeśli żaden cennik nie został dołączony do siatki Cenniki projektu dla Kontraktu projektu wykonaj poniższe działania:</span><span class="sxs-lookup"><span data-stu-id="4dd33-111">If there is no price list attached in the Project Price Lists grid of the Project Contract do the following:</span></span>

- <span data-ttu-id="4dd33-112">Dołącz cennik do siatki Cenniki projektu.</span><span class="sxs-lookup"><span data-stu-id="4dd33-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="4dd33-113">Cenniki jakie można tu dołączyć powinny mieć pole kontekstu ustawione na Sprzedaż, a pole waluty w cenniku powinno być zgodna z polem waluty w Kontrakt projektu.</span><span class="sxs-lookup"><span data-stu-id="4dd33-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="4dd33-114">Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis wydatek, zatwierdź go, i sprawdź czy wartości rzeczywiste nierozliczonej sprzedaży ukazują prawidłową cenę.</span><span class="sxs-lookup"><span data-stu-id="4dd33-114">Once you’ve made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>
- <span data-ttu-id="4dd33-115">Jeśli istnieje jeden lub kilka cenników dołączonych w siatce Cenniki projektu dla Kontraktu projektu, przejdź do Kontroli 2.</span><span class="sxs-lookup"><span data-stu-id="4dd33-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, go to Check 2.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a><span data-ttu-id="4dd33-116">Kontrola 2: Czy którekolwiek z cenników określonych powyżej są prawidłowe dla określonej daty w wartości rzeczywistej wydatek?</span><span class="sxs-lookup"><span data-stu-id="4dd33-116">Check 2: Are any of the price lists identified above valid for the specific date of the expense actual?</span></span>

<span data-ttu-id="4dd33-117">Aby Project Service rozważył cennik dla ceny domyślnej, ten cennik powinien być możliwy do zastosowanie w dniu wartości rzeczywistej wydatek sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="4dd33-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the expense sales actual.</span></span> <span data-ttu-id="4dd33-118">Sprawdź czy cenniki określone powyżej można zastosować:</span><span class="sxs-lookup"><span data-stu-id="4dd33-118">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="4dd33-119">Zacznij od sprawdzenia, czy data rozpoczęcia i data zakończenia na karcie Ogólne dla dołączonych cenników nie są puste.</span><span class="sxs-lookup"><span data-stu-id="4dd33-119">Start by checking if start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="4dd33-120">Jeśli daty rozpoczęcia i zakończenia w cennikach określonych powyżej są puste, zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="4dd33-120">If the start and end dates on the price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="4dd33-121">Zanotuj pole Data rozpoczęcia na wartościach rzeczywistych wydatek sprzedaż i sprawdź, czy jakiekolwiek określone cenniki można zastosować dla tej daty.</span><span class="sxs-lookup"><span data-stu-id="4dd33-121">Make a note of the start date field on your expense sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="4dd33-122">Na przykład data wartości rzeczywistej wydatek powinna mieścić się w zakresie rozpoczęcia i daty zakończenia w cenniku.</span><span class="sxs-lookup"><span data-stu-id="4dd33-122">For example, the date of the expense actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="4dd33-123">Jeśli nie istnieje cennik, który obejmuje tę datę w wartościach rzeczywistych wydatek sprzedaż, zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="4dd33-123">If there is no price list that covers that date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="4dd33-124">Zmodyfikuj daty rozpoczęcia i zakończenia cennika, aby upewnić się, że cennik obejmuje datę wartości rzeczywistej wydatek.</span><span class="sxs-lookup"><span data-stu-id="4dd33-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="4dd33-125">Jeśli istnieje jeden lub kilka cenników, które obejmują datę w wartościach rzeczywistych wydatek sprzedaż, zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="4dd33-125">If there is more than one price list that covers the date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="4dd33-126">Możesz rozwiązać ten problem, edytując daty rozpoczęcia i zakończenia cenników tak, że istnieje tylko jeden cennik, który obejmuje datę wartości rzeczywistej wydatek.</span><span class="sxs-lookup"><span data-stu-id="4dd33-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="4dd33-127">Jeśli istnieje tylko jeden cennik, który obejmuje tę datę wartości rzeczywistej wydatek, przejdź do Kontroli 3.</span><span class="sxs-lookup"><span data-stu-id="4dd33-127">If there is only one price list that covers that date of the expense actual, move to Check 3.</span></span>
<span data-ttu-id="4dd33-128">Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis wydatek, zatwierdź go, i sprawdź czy wartości rzeczywiste nierozliczonej sprzedaży ukazują prawidłową cenę.</span><span class="sxs-lookup"><span data-stu-id="4dd33-128">Once you’ve done made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a><span data-ttu-id="4dd33-129">Kontrola 3: Czy istnieje prawidłowa cena dla kategorii wydatek w odpowiednim cenniku projektu?</span><span class="sxs-lookup"><span data-stu-id="4dd33-129">Check 3: Is there a valid price for the expense category in the applicable project price list?</span></span> 

<span data-ttu-id="4dd33-130">Jeśli pomyślnie ukończyłeś Kontrolę 1 i Kontrolę 2, powinieneś posiadać już tylko jeden cennik projektu, który ma zastosowanie dla daty wartości rzeczywistej wydatek sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="4dd33-130">If you have successfully completed Check 1 and Check 2, you should now have only one project price list that is applicable for the date of the expense sales actual.</span></span> <span data-ttu-id="4dd33-131">Otwórz ten Cennik projektu i przejdź do karty Ceny kategorii. Upewnij się, że w siatce znajduje się wiersz przeznaczony dla określonej kategorii wydatków w wartościach rzeczywistych Wydatek.</span><span class="sxs-lookup"><span data-stu-id="4dd33-131">Open this Project Price List and go to the Category Prices tab. Make sure that there is a row in the grid for the specific expense category on the Expense actual.</span></span>
 
- <span data-ttu-id="4dd33-132">Jeśli nie ma wiersza, właśnie zlokalizowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="4dd33-132">If there is no row, then you have isolated the problem.</span></span> <span data-ttu-id="4dd33-133">Utwórz wiersz w siatce Cena kategorii dla kategorii na wartości rzeczywistej wydatek.</span><span class="sxs-lookup"><span data-stu-id="4dd33-133">Create a row in the Category price grid for the category on your expense actual.</span></span> <span data-ttu-id="4dd33-134">Gdy to zrobisz, ponownie utwórz wpis wydatek, zatwierdź go, i sprawdź czy wartość rzeczywista nierozliczona sprzedaż ukazuje prawidłową cenę.</span><span class="sxs-lookup"><span data-stu-id="4dd33-134">Once this is done, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 
- <span data-ttu-id="4dd33-135">Jeśli istnieje wiersz dla kategorii Wydatek w siatce Ceny kategorii, sprawdź, czy zawiera prawidłową cenę.</span><span class="sxs-lookup"><span data-stu-id="4dd33-135">If there is a row for the expense category in the category prices grid, check if it has a valid price.</span></span>

<span data-ttu-id="4dd33-136">Aby zrozumieć, czym jest prawidłowa cena, skorzystaj z tych metod:</span><span class="sxs-lookup"><span data-stu-id="4dd33-136">To understand what a valid price is, use these methods:</span></span>

- <span data-ttu-id="4dd33-137">Jeśli pole Metoda kalkulacji cen w wierszu Cena kategorii ustawiono na Po kosztach, to stawka jednostkowa w wartościach rzeczywistych Wydatek zostanie domyślnie ustawiona na wartość we wpisie Wydatek.</span><span class="sxs-lookup"><span data-stu-id="4dd33-137">If the Pricing Method field on the Category price line is set to At Cost, then the unit rate on your Expense sales actual will be defaulted to the value in the Expense entry.</span></span>
- <span data-ttu-id="4dd33-138">Jeśli pole Metoda kalkulacji cen w wierszu Cennik kategorii ustawiono na wartość Procent narzutu, sprawdź, czy pole Procent zostało ustawione na prawidłową wartość.</span><span class="sxs-lookup"><span data-stu-id="4dd33-138">If the Pricing Method field on the Category price line is set to Markup Percentage, then check if the Percent field is set to a valid value.</span></span> <span data-ttu-id="4dd33-139">Stawka jednostkowa na wartości rzeczywistej Wydatek jest ustawiona domyślnie po zastosowaniu tego procentu narzutu dla ceny we wpisie Wydatek.</span><span class="sxs-lookup"><span data-stu-id="4dd33-139">The unit rate on your Expense sales actual is defaulted by applying this markup percent to the price in the Expense entry.</span></span>
- <span data-ttu-id="4dd33-140">Jeśli pole Metoda kalkulacji cen w wierszu Cennik kategorii ustawiono na wartość Cena jednostkowa, sprawdź, czy pole Cena zostało ustawione na prawidłową wartość.</span><span class="sxs-lookup"><span data-stu-id="4dd33-140">If the Pricing Method field on the Category price line is set to Price per Unit, then check if the Price field is set to a valid value.</span></span> <span data-ttu-id="4dd33-141">Stawka jednostkowa na wartości rzeczywistej Wydatek zostanie ustawiona domyślnie na określoną w polu Cena kwotę w walucie.</span><span class="sxs-lookup"><span data-stu-id="4dd33-141">The unit rate on your Expense sales actual will be defaulted to the currency amount specified in the Price field.</span></span>

<span data-ttu-id="4dd33-142">Jeśli ustawienia ceny dla kategorii wydatek nie są prawidłowe, właśnie zlokalizowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="4dd33-142">If the price setup for the expense category isn't valid, then you have isolated the problem.</span></span> <span data-ttu-id="4dd33-143">Rozwiązaniem jest przeprowadzenie edycji wiersza Cena kategorii z prawidłową ceną dla kategorii wydatek zgodnie z regułami opisanymi powyżej.</span><span class="sxs-lookup"><span data-stu-id="4dd33-143">The solution is to edit the category price line with a valid price for the expense category in accordance with the rules above.</span></span> <span data-ttu-id="4dd33-144">Gdy to zrobisz, ponownie utwórz wpis wydatek, zatwierdź go, a następnie sprawdź, czy wartość rzeczywista nierozliczona sprzedaż ukazuje prawidłową cenę.</span><span class="sxs-lookup"><span data-stu-id="4dd33-144">Once you’ve done that, recreate an expense entry, approve it, and then check that the unbilled sales actual gets a valid price.</span></span>

<span data-ttu-id="4dd33-145">Jeśli nadal nie widać prawidłowej ceny na wartości rzeczywistej wydatek sprzedaż, po wykonaniu powyższych trzech kontroli prześlij zgłoszenie prośby o pomoc techniczną.</span><span class="sxs-lookup"><span data-stu-id="4dd33-145">If you still don't see a valid price on your expense sales actual after doing the three checks above, please log a support ticket.</span></span>

