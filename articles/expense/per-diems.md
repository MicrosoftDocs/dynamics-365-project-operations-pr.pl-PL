---
title: Każdego dnia
description: Ta temat zawiera informacje na temat reguł na dzień, które są używane w zarządzaniu wydatkami.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128521"
---
# <a name="per-diems"></a><span data-ttu-id="6cbb7-103">Każdego dnia</span><span class="sxs-lookup"><span data-stu-id="6cbb7-103">Per diems</span></span>

<span data-ttu-id="6cbb7-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="6cbb7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="6cbb7-105">Stawka dzienna jest przyznawana pracownikowi, który podróżuje do pracy.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="6cbb7-106">W przypadku zarządzania wydatkami można tworzyć reguły na diety dzienne dla różnych typów podróży.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="6cbb7-107">Stawki dzienne mogą być oparte na porze roku, miejscu podróży lub obydwu tych danych.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="6cbb7-108">Podczas tworzenia reguły diety dziennej można określić, że procent stawki diety będzie wstrzymany, jeśli pracownik otrzymuje dodatkowe posiłki lub usługi.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="6cbb7-109">Można również ustawić minimalną i maksymalną liczbę godzin, w przypadku których stawka dzienna może być zastosowana do kosztów podróży pracownika.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="6cbb7-110">Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="6cbb7-110">Configuration</span></span> 

1. <span data-ttu-id="6cbb7-111">Aby dodać lokalizacje diety, przejdź do **Ustawienia** > **Obliczeń i kody** > **Lokalizacje diety na dzień**.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="6cbb7-112">W przypadku każdej z dodanych wcześniej lokalizacji wybierz stawkę diety i walutę, która obowiązuje między określoną datą początkową i końcową dla hotelu, dań i innych kosztów.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="6cbb7-113">Stawki za diety i waluty konfiguruje się w obszarze **Konfigurowanie** > **Obliczenia i kody** > **Stawki na dzień**.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="6cbb7-114">Na stronie **Lokalizacje z dietą na dzień** skonfiguruj warstwy stawek diet na dzień.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="6cbb7-115">Poziomy stawki diety na dzień umożliwiają zdefiniowanie procentowego podziału dziennego wydatku na hotel, posiłki i inne koszty.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="6cbb7-116">Aby określić redukcję procentową za śniadanie, obiad lub kolację, należy zaktualizować pola na stronie **Parametry zarządzania wydatkami** na karcie **Na dzień**.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="6cbb7-117">Prześlij koszty przy użyciu diety na dzień</span><span class="sxs-lookup"><span data-stu-id="6cbb7-117">Submit expenses using per diem</span></span>
<span data-ttu-id="6cbb7-118">Aby przesyłać wydatki umożliwiające korzystanie z diet na dzień, należy skorzystać z kategorii wydatków **Na dzień** podczas tworzenia raportu z wydatków.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="6cbb7-119">Wprowadź **Datę diety na dzień**, **Datę końcową diety na dzień** i **Lokalizację diety na dzień**.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="6cbb7-120">Kwota będzie obliczana na podstawie stawek diety na dzień dla wybranej lokalizacji, a redukcja za posiłki będzie obliczana na podstawie warstw stawek diety.</span><span class="sxs-lookup"><span data-stu-id="6cbb7-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
