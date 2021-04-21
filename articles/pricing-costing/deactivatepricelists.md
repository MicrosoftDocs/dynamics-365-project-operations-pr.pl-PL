---
title: Dezaktywowanie cenników
description: W temat wyjaśniono sposób dezaktywowania lub usuwania niewykorzystanych lub starych cenników.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701960"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="efdb1-103">Dezaktywowanie cenników</span><span class="sxs-lookup"><span data-stu-id="efdb1-103">Deactivate price lists</span></span> 

<span data-ttu-id="efdb1-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="efdb1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="efdb1-105">Aby usunąć stare lub nieużywane cenniki z Dynamics 365 Project Operations, należy wykonać dwa kroki.</span><span class="sxs-lookup"><span data-stu-id="efdb1-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="efdb1-106">Usuń lub usuń cennik z określonych stron.</span><span class="sxs-lookup"><span data-stu-id="efdb1-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="efdb1-107">Zdezaktywowanie lub usunięcie cennika z listy Aktywne cenniki na stronie **Cenniki**.</span><span class="sxs-lookup"><span data-stu-id="efdb1-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="efdb1-108">Aby całkowicie usunąć cennik, należy wykonać oba kroki.</span><span class="sxs-lookup"><span data-stu-id="efdb1-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="efdb1-109">Samo wykonanie kroku 2, czyli bezpośredniego usunięcia lub dezaktywacji cennika z widoku Aktywne cenniki, nie jest wystarczające.</span><span class="sxs-lookup"><span data-stu-id="efdb1-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="efdb1-110">Musisz również usunąć powiązanie tego cennika ze wszystkich miejsc wymienionych w kroku 1.</span><span class="sxs-lookup"><span data-stu-id="efdb1-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="efdb1-111">Usuń cennik z określonych stron</span><span class="sxs-lookup"><span data-stu-id="efdb1-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="efdb1-112">Aby usunąć cennik z programu Project Operations, przejdź do następujących stron:</span><span class="sxs-lookup"><span data-stu-id="efdb1-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="efdb1-113">Strona **Parametry projektu** > karta **Cenniki**</span><span class="sxs-lookup"><span data-stu-id="efdb1-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="efdb1-114">Strona **Jednostka organizacyjna** > Siatka **Cenniki**</span><span class="sxs-lookup"><span data-stu-id="efdb1-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="efdb1-115">Strona **Konto** > Siatka **Cenniki projektu**</span><span class="sxs-lookup"><span data-stu-id="efdb1-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="efdb1-116">Strona **Oferty projektu** > Siatka **Cenniki projektu**: Dotyczy to wszystkich aktywnych ofert projektu.</span><span class="sxs-lookup"><span data-stu-id="efdb1-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="efdb1-117">Strona **Kontrakty projektów** > Siatka **Cenniki projektu**: Dotyczy to wszystkich aktywnych kontraktów projektu.</span><span class="sxs-lookup"><span data-stu-id="efdb1-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="efdb1-118">Dla każdej strony należy wybrać cennik do usunięcia, a następnie wybrać opcję **Usuń**.</span><span class="sxs-lookup"><span data-stu-id="efdb1-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="efdb1-119">Usuń lub dezaktywuj cennik na stronie Cenniki</span><span class="sxs-lookup"><span data-stu-id="efdb1-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="efdb1-120">Aby usunąć cennik z aktywnych cenników, wybierz **Sprzedaż** > **Klienci** > **Cenniki**.</span><span class="sxs-lookup"><span data-stu-id="efdb1-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="efdb1-121">Wybierz cenniki, które chcesz usunąć, i naciśnij **Usuń**.</span><span class="sxs-lookup"><span data-stu-id="efdb1-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="efdb1-122">Jeśli do cennika przywołano jakiekolwiek istniejące transakcje, nie będzie można go usunąć.</span><span class="sxs-lookup"><span data-stu-id="efdb1-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="efdb1-123">W takim przypadku możesz dezaktywować cennik, aby nie pojawiał się w żadnych widokach.</span><span class="sxs-lookup"><span data-stu-id="efdb1-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="efdb1-124">Aby dezaktywować cennik, ponownie go zaznacz, a następnie wybierz opcję **Dezaktywuj**.</span><span class="sxs-lookup"><span data-stu-id="efdb1-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
