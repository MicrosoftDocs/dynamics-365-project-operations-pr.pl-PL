---
title: Ustawianie zasad dotyczących wydatków
description: W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować w Microsoft Dynamics 365 Finance zasady dotyczące kosztów, których pracownicy muszą przestrzegać.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082159"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="613df-103">Ustawianie zasad dotyczących wydatków</span><span class="sxs-lookup"><span data-stu-id="613df-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="613df-104">W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować zasady, których pracownicy muszą przestrzegać.</span><span class="sxs-lookup"><span data-stu-id="613df-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="613df-105">Wprowadzenie w życie zasad dotyczących kosztów może pomóc w skutecznym zarządzaniu wydatkami.</span><span class="sxs-lookup"><span data-stu-id="613df-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="613df-106">Można na przykład ustawić zasadę dotyczącą wydatków na hotele w Nowym Jorku, która stwierdza, że koszty na dzień nie mogą być większe niż 250 USD.</span><span class="sxs-lookup"><span data-stu-id="613df-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="613df-107">Jeśli pracownik złoży raport o wydatkach lub zapotrzebowanie wyjazdowe, gdzie koszt pokoju przekroczy tę kwotę, system wyświetli</span><span class="sxs-lookup"><span data-stu-id="613df-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="613df-108">użytkownikowi informację o zasadzie i o przekroczeniu kwoty wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="613df-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="613df-109">Użytkownik może skonfigurować wiadomość wyświetlaną użytkownikowi podczas</span><span class="sxs-lookup"><span data-stu-id="613df-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="613df-110">określania zasady.</span><span class="sxs-lookup"><span data-stu-id="613df-110">define the policy.</span></span>      
        
<span data-ttu-id="613df-111">Możesz korzystać z trzech typów zasad:</span><span class="sxs-lookup"><span data-stu-id="613df-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="613df-112">Ostrzeżenie — zezwala pracownikowi na przesyłanie raportu z wydatków lub przejazdu na podróż, ale wydatek będzie zaznaczony dla wszystkich osób zatwierdzających i</span><span class="sxs-lookup"><span data-stu-id="613df-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="613df-113">na potrzeby późniejszego raportowania.</span><span class="sxs-lookup"><span data-stu-id="613df-113">for later reporting.</span></span>        

- <span data-ttu-id="613df-114">Błąd — wymaga, aby pracownik poprawił koszty w celu zapewnienia zgodności z zasadami przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.</span><span class="sxs-lookup"><span data-stu-id="613df-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="613df-115">Uzasadnienie — wymaga, aby pracownik lub kierownik wprowadził uzasadnienie przekroczenia kwoty zasady przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.</span><span class="sxs-lookup"><span data-stu-id="613df-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="613df-116">Podpowiedzi dot. zasad</span><span class="sxs-lookup"><span data-stu-id="613df-116">Policy tips</span></span>
<span data-ttu-id="613df-117">Oto kilka sugestii, które mogą pomóc podczas tworzenia nowych zasad zarządzania wydatkami.</span><span class="sxs-lookup"><span data-stu-id="613df-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="613df-118">Zasady wchodzą w życie z datą utworzenia. Oznacza to, że zasada nie będzie obowiązywała co do wydatków, które powstały przed utworzeniem zasady.</span><span class="sxs-lookup"><span data-stu-id="613df-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="613df-119">Jeśli na przykład tworzysz nową zasadę na dziś, aby wymusić maksymalne koszty posiłku w wysokości 50 USD, wówczas wszelkie istniejące koszty wprowadzone wczoraj nie będą sprawdzane względem tej zasady.</span><span class="sxs-lookup"><span data-stu-id="613df-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="613df-120">Tworząc zasadę dla kategorii wydatków, która może być wyświetlona w ramach listy elementów, należy rozważyć dodanie warunku dotyczącego typu wiersza wydatku.</span><span class="sxs-lookup"><span data-stu-id="613df-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="613df-121">Niektóre zasady, takie jak wymaganie przyjęcia paragonu, mogą nie być zrozumiałe dla wyszczególnionych wierszy i powinny być stosowane tylko w wierszu nagłówka lub w wierszu niewyszczególnionym.</span><span class="sxs-lookup"><span data-stu-id="613df-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="613df-122">Reguły zarządzania wydatkami są domyślnie oceniane względem encji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="613df-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="613df-123">Zamiast tego, w przypadku scenariuszy międzyfirmowych można skonfigurować zasadę, która będzie oceniana względem encji docelowej (encji pożyczanej).</span><span class="sxs-lookup"><span data-stu-id="613df-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="613df-124">Aby uruchomić zasady w odniesieniu do encji docelowej, należy włączyć funkcję „Oceniaj zasadę dotyczącą kosztów względem pożyczonej encji firmy” w obszarze roboczym **Zarządzanie funkcjami**.</span><span class="sxs-lookup"><span data-stu-id="613df-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="613df-125">Kiedy oceniać przestrzeganie zasad</span><span class="sxs-lookup"><span data-stu-id="613df-125">When to evaluate policies</span></span>

<span data-ttu-id="613df-126">W ramach parametrów zarządzania wydatkami można wybrać opcję oceny pod kątem przestrzegania zasad dotyczących wydatków na: podczas zapisywania wiersza lub podczas przesyłania raportu z wydatków.</span><span class="sxs-lookup"><span data-stu-id="613df-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="613df-127">W przypadku wybrania opcji oceny w trakcie zapisywania wiersza użytkownicy będą wcześniej widzieli, co należy wykonać, aby wypełnić cały raport.</span><span class="sxs-lookup"><span data-stu-id="613df-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="613df-128">Można także opóźnić ocenę przez zasadę i oszczędzić czas przeprowadzając weryfikację na samym końcu, przed przesłaniem do przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="613df-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
