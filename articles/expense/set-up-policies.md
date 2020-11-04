---
title: Definiowanie zasad wydatków
description: W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować zasady dotyczące kosztów, których pracownicy muszą przestrzegać.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082082"
---
# <a name="define-expense-policies"></a><span data-ttu-id="1960b-103">Definiowanie zasad wydatków</span><span class="sxs-lookup"><span data-stu-id="1960b-103">Define expense policies</span></span>

<span data-ttu-id="1960b-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="1960b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1960b-105">W przypadku wprowadzania i przesyłania raportów o wydatkach i wniosków wyjazdowych można zdefiniować zasady, których pracownicy muszą przestrzegać.</span><span class="sxs-lookup"><span data-stu-id="1960b-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="1960b-106">Wprowadzenie w życie zasad dotyczących kosztów może pomóc w skutecznym zarządzaniu wydatkami.</span><span class="sxs-lookup"><span data-stu-id="1960b-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="1960b-107">Można na przykład ustawić zasadę dotyczącą wydatków na hotele w Nowym Jorku, która stwierdza, że koszty na dzień nie mogą być większe niż 250 USD.</span><span class="sxs-lookup"><span data-stu-id="1960b-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="1960b-108">Jeśli pracownik złoży raport o wydatkach lub zapotrzebowanie wyjazdowe, gdzie koszt pokoju przekroczy tę kwotę, system wyświetli</span><span class="sxs-lookup"><span data-stu-id="1960b-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="1960b-109">użytkownikowi informację o zasadzie i o przekroczeniu kwoty wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="1960b-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="1960b-110">Użytkownik może skonfigurować wiadomość wyświetlaną użytkownikowi podczas</span><span class="sxs-lookup"><span data-stu-id="1960b-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="1960b-111">określania zasady.</span><span class="sxs-lookup"><span data-stu-id="1960b-111">define the policy.</span></span>      
        
<span data-ttu-id="1960b-112">Możesz korzystać z trzech typów zasad:</span><span class="sxs-lookup"><span data-stu-id="1960b-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="1960b-113">**Ostrzeżenie** : Zezwala pracownikowi na przesyłanie raportu z wydatków lub przejazdu na podróż, ale wydatek będzie zaznaczony dla wszystkich osób zatwierdzających i</span><span class="sxs-lookup"><span data-stu-id="1960b-113">**Warning** : Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="1960b-114">na potrzeby późniejszego raportowania.</span><span class="sxs-lookup"><span data-stu-id="1960b-114">for later reporting.</span></span>        

- <span data-ttu-id="1960b-115">**Błąd** : wymaga, aby pracownik poprawił koszty w celu zapewnienia zgodności z zasadami przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.</span><span class="sxs-lookup"><span data-stu-id="1960b-115">**Error** : Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="1960b-116">**Uzasadnienie** : wymaga, aby pracownik lub kierownik wprowadził uzasadnienie przekroczenia kwoty zasady przed przesłaniem raportu z wydatków lub wniosku wyjazdowego.</span><span class="sxs-lookup"><span data-stu-id="1960b-116">**Justification** : Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="1960b-117">Podpowiedzi dot. zasad</span><span class="sxs-lookup"><span data-stu-id="1960b-117">Policy tips</span></span>
<span data-ttu-id="1960b-118">Oto kilka sugestii, które mogą pomóc podczas tworzenia nowych zasad zarządzania wydatkami:</span><span class="sxs-lookup"><span data-stu-id="1960b-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="1960b-119">Zasady wchodzą w życie z datą utworzenia. Oznacza to, że zasady nie będą obowiązywały co do wydatków, które powstały przed utworzeniem zasady.</span><span class="sxs-lookup"><span data-stu-id="1960b-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="1960b-120">Załóżmy na przykład, że użytkownik utworzył nowe zasady dziś w celu wyegzekwowania maksymalnego kosztu posiłku w wys. 50 USD.</span><span class="sxs-lookup"><span data-stu-id="1960b-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="1960b-121">Wszelkie istniejące koszty wprowadzone wczoraj nie będą sprawdzane względem tej zasady.</span><span class="sxs-lookup"><span data-stu-id="1960b-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="1960b-122">Tworząc zasadę dla kategorii wydatków, która może być wyświetlona w ramach listy elementów, należy rozważyć dodanie warunku dotyczącego typu wiersza wydatku.</span><span class="sxs-lookup"><span data-stu-id="1960b-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="1960b-123">Niektóre zasady, na przykład wymaganie paragonu, mogą nie mieć zastosowania względem list elementów.</span><span class="sxs-lookup"><span data-stu-id="1960b-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="1960b-124">W tym przypadku zasada ma zastosowanie tylko względem wiersza nagłówka lub wiersza bez pozycji.</span><span class="sxs-lookup"><span data-stu-id="1960b-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="1960b-125">Reguły zarządzania wydatkami są domyślnie oceniane względem encji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="1960b-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="1960b-126">Zamiast tego, w przypadku scenariuszy międzyfirmowych można skonfigurować zasadę, która będzie oceniana względem encji docelowej (encji pożyczanej).</span><span class="sxs-lookup"><span data-stu-id="1960b-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="1960b-127">Aby uruchomić zasady w odniesieniu do encji docelowej, należy włączyć funkcję **Oceniaj zasadę dotyczącą kosztów względem pożyczonej encji firmy** w obszarze roboczym **Zarządzanie funkcjami**.</span><span class="sxs-lookup"><span data-stu-id="1960b-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="1960b-128">Kiedy oceniać przestrzeganie zasad</span><span class="sxs-lookup"><span data-stu-id="1960b-128">When to evaluate policies</span></span>

<span data-ttu-id="1960b-129">W ramach parametrów zarządzania wydatkami można wybrać opcję oceny pod kątem przestrzegania zasad dotyczących wydatków na: podczas zapisywania wiersza lub podczas przesyłania raportu z wydatków.</span><span class="sxs-lookup"><span data-stu-id="1960b-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="1960b-130">W przypadku wybrania opcji oceny w trakcie zapisywania wiersza użytkownicy będą wcześniej widzieli, co należy wykonać, aby wypełnić cały raport.</span><span class="sxs-lookup"><span data-stu-id="1960b-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="1960b-131">Można także opóźnić ocenę przez zasadę i oszczędzić czas przeprowadzając weryfikację na samym końcu, przed przesłaniem do przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="1960b-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
