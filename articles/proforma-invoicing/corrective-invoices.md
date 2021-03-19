---
title: Faktury skorygowane
description: Ten temat zawiera informacje o skorygowanych fakturach.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287836"
---
# <a name="corrected-invoices"></a><span data-ttu-id="f0539-103">Faktury skorygowane</span><span class="sxs-lookup"><span data-stu-id="f0539-103">Corrected invoices</span></span>

<span data-ttu-id="f0539-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="f0539-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f0539-105">Potwierdzone faktury w PSA można korygować.</span><span class="sxs-lookup"><span data-stu-id="f0539-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="f0539-106">W przypadku edytowania potwierdzonej faktury jest tworzona wersja robocza skorygowanej faktury.</span><span class="sxs-lookup"><span data-stu-id="f0539-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="f0539-107">Ponieważ założono, że mają zostać wyzerowane wszystkie transakcje i ilości z oryginalnej faktury, ta faktura skorygowana zawiera wszystkie transakcje z oryginalnej faktury, a wszystkie jej ilości są równe 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f0539-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="f0539-108">Jeśli żadne transakcje nie wymagają korekty, można je usunąć z wersji roboczej faktury korygującej.</span><span class="sxs-lookup"><span data-stu-id="f0539-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="f0539-109">Aby odwrócić lub dokonać zwrotu tylko ilości częściowej, można edytować pole ilość w szczegółach wiersza.</span><span class="sxs-lookup"><span data-stu-id="f0539-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="f0539-110">Po otwarciu szczegółów wiersza faktury jest wyświetlana oryginalna ilość faktury.</span><span class="sxs-lookup"><span data-stu-id="f0539-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="f0539-111">Następnie można edytować bieżącą ilość na fakturze, tak aby była mniejsza lub większa niż oryginalna ilość na fakturze.</span><span class="sxs-lookup"><span data-stu-id="f0539-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="f0539-112">Po potwierdzeniu faktury korygującej oryginalna rozliczona wartość rzeczywista sprzedaży jest cofana i system tworzy nową wartość rzeczywistą rozliczonej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="f0539-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="f0539-113">Jeśli ilość została zmniejszona, różnica spowoduje utworzenie nowej nierozliczonej wartości rzeczywistej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="f0539-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="f0539-114">Jeśli na przykład oryginalna rozliczona sprzedaż trwała 8 godzin, a wiersz faktury korygującej ograniczył ilość do sześciu godzin, oryginalny wiersz wyliczonych transakcji jest wycofany i utworzone są dwie nowe wartości rzeczywiste:</span><span class="sxs-lookup"><span data-stu-id="f0539-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="f0539-115">Rozliczona wartość rzeczywista za sześć godzin.</span><span class="sxs-lookup"><span data-stu-id="f0539-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="f0539-116">Nierozliczona sprzedaż za pozostałe dwie godziny.</span><span class="sxs-lookup"><span data-stu-id="f0539-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="f0539-117">Ta transakcja może być rozliczona później lub oznakowana jako niepłatna, w zależności od ustaleń z klientem.</span><span class="sxs-lookup"><span data-stu-id="f0539-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]