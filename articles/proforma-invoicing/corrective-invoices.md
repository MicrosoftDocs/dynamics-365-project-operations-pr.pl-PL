---
title: Faktury skorygowane
description: Ten temat zawiera informacje o skorygowanych fakturach.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898094"
---
# <a name="corrected-invoices"></a><span data-ttu-id="b512f-103">Faktury skorygowane</span><span class="sxs-lookup"><span data-stu-id="b512f-103">Corrected invoices</span></span>

<span data-ttu-id="b512f-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="b512f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b512f-105">Potwierdzone faktury w PSA można korygować.</span><span class="sxs-lookup"><span data-stu-id="b512f-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="b512f-106">W przypadku edytowania potwierdzonej faktury jest tworzona wersja robocza skorygowanej faktury.</span><span class="sxs-lookup"><span data-stu-id="b512f-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="b512f-107">Ponieważ założono, że mają zostać wyzerowane wszystkie transakcje i ilości z oryginalnej faktury, ta faktura skorygowana zawiera wszystkie transakcje z oryginalnej faktury, a wszystkie jej ilości są równe 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b512f-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="b512f-108">Jeśli żadne transakcje nie wymagają korekty, można je usunąć z wersji roboczej faktury korygującej.</span><span class="sxs-lookup"><span data-stu-id="b512f-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="b512f-109">Aby odwrócić lub dokonać zwrotu tylko ilości częściowej, można edytować pole ilość w szczegółach wiersza.</span><span class="sxs-lookup"><span data-stu-id="b512f-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="b512f-110">Po otwarciu szczegółów wiersza faktury jest wyświetlana oryginalna ilość faktury.</span><span class="sxs-lookup"><span data-stu-id="b512f-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="b512f-111">Następnie można edytować bieżącą ilość na fakturze, tak aby była mniejsza lub większa niż oryginalna ilość na fakturze.</span><span class="sxs-lookup"><span data-stu-id="b512f-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="b512f-112">Po potwierdzeniu faktury korygującej oryginalna rozliczona wartość rzeczywista sprzedaży jest cofana i system tworzy nową wartość rzeczywistą rozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b512f-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="b512f-113">Jeśli ilość została zmniejszona, różnica spowoduje utworzenie nowej nierozliczonej wartości rzeczywistej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b512f-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="b512f-114">Jeśli na przykład oryginalna rozliczona sprzedaż trwała 8 godzin, a wiersz faktury korygującej ograniczył ilość do sześciu godzin, oryginalny wiersz wyliczonych transakcji jest wycofany i utworzone są dwie nowe wartości rzeczywiste:</span><span class="sxs-lookup"><span data-stu-id="b512f-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="b512f-115">Rozliczona wartość rzeczywista za sześć godzin.</span><span class="sxs-lookup"><span data-stu-id="b512f-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="b512f-116">Nierozliczona sprzedaż za pozostałe dwie godziny.</span><span class="sxs-lookup"><span data-stu-id="b512f-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="b512f-117">Ta transakcja może być rozliczona później lub oznakowana jako niepłatna, w zależności od ustaleń z klientem.</span><span class="sxs-lookup"><span data-stu-id="b512f-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>