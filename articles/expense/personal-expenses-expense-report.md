---
title: Pracuj z wydatkami osobistymi na raporcie wydatków
description: Ten temat zawiera informacje o tym, jak radzić sobie z wydatkami osobistymi poniesionymi przez pracowników podczas podróży służbowych.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025697"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="6b140-103">Pracuj z wydatkami osobistymi na raporcie wydatków</span><span class="sxs-lookup"><span data-stu-id="6b140-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="6b140-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="6b140-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6b140-105">Podczas podróży służbowej pracownik może obciążać firmową kartę kredytową wydatkami osobistymi.</span><span class="sxs-lookup"><span data-stu-id="6b140-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="6b140-106">Jeśli proces nie został zdefiniowany do obsługi wydatków osobistych, proces zatwierdzania raportu z wydatków może zostać zakłócony, gdy pracownik prześle szczegółowy raport z wydatków.</span><span class="sxs-lookup"><span data-stu-id="6b140-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="6b140-107">Istnieją dwie metody pracy z wydatkami osobistymi pracownika:</span><span class="sxs-lookup"><span data-stu-id="6b140-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="6b140-108">**Płacone przez pracownika**: organizacja nie płaci kosztów osobistych, które są wyświetlane na rachunku za firmową kartę kredytową.</span><span class="sxs-lookup"><span data-stu-id="6b140-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="6b140-109">Zamiast tego pracownik opłaca wydatki bezpośrednio sprzedawcy karty kredytowej.</span><span class="sxs-lookup"><span data-stu-id="6b140-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="6b140-110">**Zapłacona przez firmę**: Twoja organizacja płaci pełny rachunek za firmową kartę kredytową, a następnie obciąża konto pracownika kosztami osobistymi.</span><span class="sxs-lookup"><span data-stu-id="6b140-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="6b140-111">Użytkownik może wybrać metodę, której dana organizacja użyje na stronie **Parametrów zarządzania wydatkami**.</span><span class="sxs-lookup"><span data-stu-id="6b140-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="6b140-112">Włącz funkcję dzielenia wydatków, gdy pole kwoty osobistej ma zdefiniowaną wartość</span><span class="sxs-lookup"><span data-stu-id="6b140-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="6b140-113">Funkcja **Włącz funkcję podzielonego wydatku, gdy pole kwoty osobistej ma zdefiniowaną wartość** dotyczy tylko raportów wydatków, które są zatwierdzane za pomocą przepływu pracy na poziomie linii.</span><span class="sxs-lookup"><span data-stu-id="6b140-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="6b140-114">Zatwierdzenie raportu odbywa się poprzez przejście do zakładki **Obsługa raportów wydatków** > **Raporty wydatków przypisane do mnie** > **Otwórz raport wydatków**.</span><span class="sxs-lookup"><span data-stu-id="6b140-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="6b140-115">Aby włączyć tę funkcję, należy przejść do **Obszary robocze** > **Zarządzanie funkcjami**, wybrać **Włącz funkcję dzielenia wydatków, gdy pole kwoty osobistej ma zdefiniowaną wartość**, a następnie wybrać **Uruchom teraz**.</span><span class="sxs-lookup"><span data-stu-id="6b140-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="6b140-116">Gdy funkcja jest włączona, linie wydatków, które korzystają z tej funkcjonalności, generują dwie linie podczas składania raportu.</span><span class="sxs-lookup"><span data-stu-id="6b140-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="6b140-117">Generowane są dwie linie, aby osoba zatwierdzająca mogła zatwierdzić każdą linię osobno.</span><span class="sxs-lookup"><span data-stu-id="6b140-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
