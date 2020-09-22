---
title: Dlaczego cena domyślna wynosi zero w wartościach rzeczywistych czas koszt?
description: Rozwiązywanie problemu, dlaczego cena domyślna wynosi 0 w wartościach rzeczywistych czas koszt.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754430"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="aa92b-103">Dlaczego cena domyślna wynosi zero w wartościach rzeczywistych czas koszt?</span><span class="sxs-lookup"><span data-stu-id="aa92b-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aa92b-104">To często zadawane pytanie dotyczy wartości rzeczywistych, gdzie klasa transakcji jest ustawiona na Czas a typ transakcji to Koszt.</span><span class="sxs-lookup"><span data-stu-id="aa92b-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="aa92b-105">Poniższe trzy kontrole ułatwią rozwiązanie problemu, dlaczego cena wynosi domyślnie 0 w wartościach rzeczywistych koszt czasu.</span><span class="sxs-lookup"><span data-stu-id="aa92b-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="aa92b-106">Kontrola 1: Określ listę kosztów własnych dla projektu</span><span class="sxs-lookup"><span data-stu-id="aa92b-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="aa92b-107">Znajdź projekt w polu projektu wartości rzeczywistych, a następnie przejdź na stronę projektu.</span><span class="sxs-lookup"><span data-stu-id="aa92b-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="aa92b-108">Kliknij łącze jednostki kontraktującej w polu.</span><span class="sxs-lookup"><span data-stu-id="aa92b-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="aa92b-109">Na stronie Jednostka kontraktująca sprawdź, czy jednostka kontraktująca posiada cennik w siatce kosztów własnych.</span><span class="sxs-lookup"><span data-stu-id="aa92b-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="aa92b-110">Jeśli istnieje więcej niż jeden cennik, zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="aa92b-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="aa92b-111">Usługa Project Service obsługuje tylko jeden cennik dla jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="aa92b-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="aa92b-112">Usuń wszystkie cenniki z tej encji i zostaw tylko jeden cennik dołączony w siatce Koszt własny jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="aa92b-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="aa92b-113">Jeśli żaden cennik nie jest dołączony do jednostki organizacyjnej, sporządź notatkę o walucie jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="aa92b-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="aa92b-114">Przejdź do usługi Project Service, a następnie do Parametry i otwórz kartę Cenniki. Sprawdź, czy istnieją cenniki z kontekstem ustawionym na Koszt i walutę, która odpowiada walucie jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="aa92b-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="aa92b-115">Jeśli nie istnieją cenniki, które spełniają te kryteria, znalazłeś problem.</span><span class="sxs-lookup"><span data-stu-id="aa92b-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="aa92b-116">Upewnij się, że posiadasz co najmniej jeden cennik, którego kontekst ustawiono na Koszt, i którego waluta odpowiada walucie jednostki organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="aa92b-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="aa92b-117">Jeśli istnieje więcej niż jeden cennik zgodny z tymi kryteriami, czytaj dalej ten dokument, aby przeprowadzić więcej kontroli.</span><span class="sxs-lookup"><span data-stu-id="aa92b-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="aa92b-118">Kontrola 2: Czy którekolwiek z cenników określonych powyżej są prawidłowe dla określonej daty wartości rzeczywistych czas koszt?</span><span class="sxs-lookup"><span data-stu-id="aa92b-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="aa92b-119">Aby Project Service rozważył cennik dla ceny domyślnej, ten cennik powinien być możliwy do zastosowania w dniu wartości rzeczywistej czasu koszt.</span><span class="sxs-lookup"><span data-stu-id="aa92b-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="aa92b-120">Sprawdź czy cenniki określone powyżej można zastosować:</span><span class="sxs-lookup"><span data-stu-id="aa92b-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="aa92b-121">Sprawdź, czy data rozpoczęcia i zakończenia na karcie Ogólne dla dołączonych cenników nie są puste.</span><span class="sxs-lookup"><span data-stu-id="aa92b-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="aa92b-122">Jeśli daty rozpoczęcia i zakończenia w cennikach określonych powyżej są puste, zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="aa92b-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="aa92b-123">Zanotuj pole daty rozpoczęcia na wartościach rzeczywistych czas koszt i sprawdź, czy jakiekolwiek określone cenniki można zastosować dla tej daty.</span><span class="sxs-lookup"><span data-stu-id="aa92b-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="aa92b-124">Na przykład data wartości rzeczywistej czas koszt powinna mieścić się w zakresie rozpoczęcia i daty zakończenia w cenniku.</span><span class="sxs-lookup"><span data-stu-id="aa92b-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="aa92b-125">Jeśli nie istnieje cennik, który obejmuje tę datę w wartościach rzeczywistych czas koszt, zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="aa92b-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="aa92b-126">Zmodyfikuj daty rozpoczęcia i zakończenia cennika, aby upewnić się, że cennik obejmuje datę wartości rzeczywistej czas koszt.</span><span class="sxs-lookup"><span data-stu-id="aa92b-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="aa92b-127">Jeśli istnieje jeden lub kilka cenników, które obejmują datę w wartościach rzeczywistych czas koszt, zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="aa92b-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="aa92b-128">Możesz rozwiązać ten problem, edytując daty rozpoczęcia i zakończenia cenników tak, że istnieje tylko jeden cennik, który obejmuje datę wartości rzeczywistej czas koszt.</span><span class="sxs-lookup"><span data-stu-id="aa92b-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="aa92b-129">Jeśli istnieje tylko jeden cennik, który obejmuje datę wartości rzeczywistej czas koszt, przejdź do następnej kontroli w dokumencie.</span><span class="sxs-lookup"><span data-stu-id="aa92b-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="aa92b-130">Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis godziny, zatwierdź go, i sprawdź czy wartości rzeczywiste czas koszt ukazują prawidłową cenę.</span><span class="sxs-lookup"><span data-stu-id="aa92b-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="aa92b-131">Kontrola 3: Czy istnieje cena w cenniku dla rozmiarów kalkulacji cen w wartościach rzeczywistych czas koszt?</span><span class="sxs-lookup"><span data-stu-id="aa92b-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="aa92b-132">Jeśli pomyślnie ukończyłeś Kontrolę 1 i Kontrolę 2, powinieneś posiadać już tylko jeden cennik, który ma zastosowanie dla daty wartości rzeczywistej czas koszt.</span><span class="sxs-lookup"><span data-stu-id="aa92b-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="aa92b-133">Otwórz ten Cennik i przejdź do karty Ceny ról. Upewnij się, że w siatce znajduje się wiersz przeznaczony dla wymiarów kalkulacji cen w wartościach rzeczywistych czas koszt.</span><span class="sxs-lookup"><span data-stu-id="aa92b-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="aa92b-134">Jeśli nie istnieje wiersz w siatce ceny roli dla kalkulacji cen na wartości rzeczywistej czas koszt, właśnie zidentyfikowałeś problem.</span><span class="sxs-lookup"><span data-stu-id="aa92b-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="aa92b-135">Utwórz wiersz w siatce Ceny ról dla rozmiarów kalkulacji cen na wartości rzeczywistej czas koszt.</span><span class="sxs-lookup"><span data-stu-id="aa92b-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="aa92b-136">Gdy to skończysz, ponownie utwórz wpis czasu, zatwierdź go, i sprawdź czy wartości rzeczywiste czas koszt ukazują prawidłową cenę.</span><span class="sxs-lookup"><span data-stu-id="aa92b-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="aa92b-137">Jeśli nadal nie widać prawidłowej ceny na wartości rzeczywistej czas koszt, po wykonaniu powyższych trzech kontroli prześlij zgłoszenie prośby o pomoc techniczną.</span><span class="sxs-lookup"><span data-stu-id="aa92b-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



