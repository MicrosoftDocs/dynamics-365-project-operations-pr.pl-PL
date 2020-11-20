---
title: Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych
description: W tym temacie przedstawiono informacje na temat sposobu rozwiązywania kosztów kosztu na szacunkach i wartościach rzeczywistych.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bad8f4b95ac5803d3f334e1b306d2a9d27a6645d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081922"
---
# <a name="resolving-cost-prices-on-estimates-and-actuals"></a><span data-ttu-id="e5da2-103">Rozwiązywanie kosztów własnych w oszacowaniach i wartościach rzeczywistych</span><span class="sxs-lookup"><span data-stu-id="e5da2-103">Resolving cost prices on estimates and actuals</span></span>

<span data-ttu-id="e5da2-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="e5da2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5da2-105">W celu rozpoznania cennika i listy kosztów własnych na potrzeby oszacowań i wartości rzeczywistych,, system używa informacji zawartych w polach **Data** , **Waluta** i **Jednostka kontraktująca** z powiązanego projektu.</span><span class="sxs-lookup"><span data-stu-id="e5da2-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date** , **Currency** , and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="e5da2-106">Po rozpoznaniu listy kosztów aplikacja rozpoznaje stawkę kosztów.</span><span class="sxs-lookup"><span data-stu-id="e5da2-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="e5da2-107">Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Czas</span><span class="sxs-lookup"><span data-stu-id="e5da2-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="e5da2-108">Szacowane wiersze dla wartości Czas odnoszą się do oferty i pozycji kontraktu oraz do przydziałów zasobów w projekcie.</span><span class="sxs-lookup"><span data-stu-id="e5da2-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="e5da2-109">Po rozwiązaniu listy cennika, system korzysta z pól **Rola** oraz **Jednostka kontraktująca** z wiersza szacowania dla czasu, w celu dopasowania do wierszy cennika ról.</span><span class="sxs-lookup"><span data-stu-id="e5da2-109">After a cost price list is resolved, the system uses the **Role** and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="e5da2-110">To dopasowanie zakłada, że używasz przygotowanych wymiarów kalkulacji cen, aby uzyskać koszty wykonanej pracy.</span><span class="sxs-lookup"><span data-stu-id="e5da2-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="e5da2-111">Jeśli system został skonfigurowany w taki sposób, aby odpowiadał polom **Rola** i **Jednostka zasobów** lub odpowiadał także tym polom, w celu pobrania pasującego cennika ról zostanie wykorzystana inna kombinacja.</span><span class="sxs-lookup"><span data-stu-id="e5da2-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit** , then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="e5da2-112">Jeśli aplikacja znajdzie wiersz ceny roli, który ma stawkę kosztu dla połączenia **Rola** oraz **Jednostką zamawiająca** , to będzie domyślna stawka kosztu.</span><span class="sxs-lookup"><span data-stu-id="e5da2-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="e5da2-113">Jeśli aplikacja nie może dopasować pól **Rola** i **Jednostka zamawiająca** , program pobiera pasujące wiersze z rolą, ale ustawiane są wartości null **Jednostki zamawiającej**.</span><span class="sxs-lookup"><span data-stu-id="e5da2-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="e5da2-114">Po dopasowaniu odpowiedniego rekordu ceny roli, stawka kosztu pobierana jest domyślnie z tego rekordu.</span><span class="sxs-lookup"><span data-stu-id="e5da2-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="e5da2-115">W przypadku skonfigurowania innej prioretyzacji **Roli** i **Jednostki zamawiającej** lub jeśli istnieją inne wymiary mające wyższy priorytet, to zachowanie odpowiednio się zmieni.</span><span class="sxs-lookup"><span data-stu-id="e5da2-115">If you configure a different prioritization of **Role** and **Resourcing Unit** , or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="e5da2-116">System pobiera rekordy cen ról wraz z wartościami odpowiadającymi poszczególnym wartościom wymiarów kalkulacji cen w kolejności według priorytetu. Wiersze, które mają wartości null dla tych wymiarów są ostatnie.</span><span class="sxs-lookup"><span data-stu-id="e5da2-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="e5da2-117">Rozpoznawanie stawek kosztów w wartościach rzeczywistych i oszacowaniach dla wiersza Wydatek</span><span class="sxs-lookup"><span data-stu-id="e5da2-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="e5da2-118">Szacowane wiersze dla wartości Wydatek odnoszą się do oferty i pozycji kontraktu dla wydatku oraz do wierszy oszacowania wydatku w projekcie.</span><span class="sxs-lookup"><span data-stu-id="e5da2-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="e5da2-119">Po rozwiązaniu listy cennika, system korzysta z połączenia pól **Kategoria** , **Firma zasobów** z wiersza szacowania dla Wydatku, w celu dopasowania do wiersza **Cena kategorii** znajdującego się w rozwiązanym cenniku.</span><span class="sxs-lookup"><span data-stu-id="e5da2-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="e5da2-120">Jeśli system znajdzie wiersz ceny kategorii, który ma stawkę kosztu dla połączenia pól **Kategoria** oraz **Jednostką zasobów** , to będzie to domyślna stawka kosztu.</span><span class="sxs-lookup"><span data-stu-id="e5da2-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="e5da2-121">Jeśli system nie może dopasować wartości **Kategoria** i **Jednostka** albo jeśli jest w stanie znaleźć pasujący wiersz cena kategorii, ale metoda kalkulacji cena nie jest ustawiona na wartość **Ceną jednostkową** , stawka kosztów jest domyślnie ustawiona na zero (0).</span><span class="sxs-lookup"><span data-stu-id="e5da2-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit** , the cost rate is defaulted to zero(0).</span></span>