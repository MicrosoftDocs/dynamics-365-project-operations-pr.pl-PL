---
title: Faktury korygujące oparte na projektach
description: Ten temat zawiera informacje o tym, jak tworzyć i potwierdzać faktury korygujące oparte na projektach w Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867054"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="5ea1a-103">Faktury korygujące oparte na projektach</span><span class="sxs-lookup"><span data-stu-id="5ea1a-103">Corrective project-based invoices</span></span>

<span data-ttu-id="5ea1a-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="5ea1a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5ea1a-105">Potwierdzona faktura projektu może być skorygowana w celu wprowadzenia zmian lub uznań, po uprzedniej zgodzie klienta i menedżera projektu.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="5ea1a-106">Aby dokonać edycji potwierdzonej faktury, otwórz potwierdzoną fakturę i wybierz pozycję **Koryguj tę fakturę**.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ea1a-107">Ten wybór nie jest dostępny, chyba że faktura za projekt zostanie potwierdzona lub faktura oparta na projekcie zawiera zaliczki lub zaliczki lub uzgodnienia zaliczek lub zaliczek.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="5ea1a-108">Nowa wersja robocza faktury jest tworzona na podstawie potwierdzonej faktury.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="5ea1a-109">Wszystkie szczegóły wiersza faktury z uprzednio potwierdzonej faktury zostaną skopiowane do nowej wersji roboczej.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="5ea1a-110">Oto niektóre z najważniejszych informacji na temat nowych wierszy korygowanych faktur:</span><span class="sxs-lookup"><span data-stu-id="5ea1a-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="5ea1a-111">Wszystkie ilości są aktualizowane na zero.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-111">All quantities are updated to zero.</span></span> <span data-ttu-id="5ea1a-112">Dynamics 365 Project Operations zakłada, że wszystkie zafakturowane pozycje są w pełni zaksięgowane.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="5ea1a-113">Jeśli jest to konieczne, można ręcznie zaktualizować te ilości, tak aby odpowiadały ilości zafakturowanej, a nie uznanej ilości.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="5ea1a-114">W zależności od wprowadzonej ilości program obliczy uznaną zaksięgowaną kwotę.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="5ea1a-115">Ta kwota jest odzwierciedlona w wartościach rzeczywistych tworzonych podczas potwierdzania faktury korygującej.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="5ea1a-116">W przypadku wprowadzania zmian do kwoty podatku należy wprowadzić prawidłową kwotę podatku, a nie kwotę podatku, która ma być uznana.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="5ea1a-117">Korekta punktów kontrolnych jest zawsze przetwarzana jako pełne uznania.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="5ea1a-118">W przypadku szczegółów wiersza faktury, które są korektami innych już zafakturowanych opłat, pole **Korekta** ma ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="5ea1a-119">W przypadku faktur, które mają skorygowane szczegóły wiersza faktury, pole **Ma korekty** ma ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="5ea1a-120">Wartości rzeczywiste tworzone po potwierdzeniu faktury korygującej</span><span class="sxs-lookup"><span data-stu-id="5ea1a-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="5ea1a-121">W poniższej tabeli przedstawiono wartości rzeczywiste, które są tworzone po potwierdzenia faktury korekcyjnej.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="5ea1a-122">
                    <strong>Scenariusz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ea1a-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="5ea1a-123">
                    <strong>Wartości rzeczywiste utworzone przy potwierdzeniu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5ea1a-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ea1a-124">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji czasowej.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-125">Rozliczona sprzedaż za godziny i kwotę z oryginalnego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-126">Nowa nierozliczona wartość rzeczywista sprzedaży za godziny i kwotę z oryginalnego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5ea1a-127">Fakturowanie częściowego uznania transakcji czasu.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-128">Rozliczona sprzedaż za godziny i kwotę z oryginalnego fakturowanego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-129">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna względem godzin i kwoty w edytowanym wierszu faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-130">Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą liczbę godzin i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ea1a-131">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-132">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-133">Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5ea1a-134">Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-135">Rozliczone wycofanie sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-136">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z korygowanego wiersza faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-137">Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą ilość i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ea1a-138">Fakturowanie pełnego kredytu z poprzednio zafakturowanej transakcji materiałowej.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-139">Fakturowane wycofanie sprzedaży dla ilości i kwoty w szczegółach wiersza oryginalnej faktury dla materiału.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-140">Nowa niezafakturowana sprzedaż rzeczywista dla ilości i kwoty w szczegółach wiersza oryginalnej faktury dla materiału.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5ea1a-141">Fakturowanie częściowego kredytu przy istotnej transakcji.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-142">Wycofanie sprzedaży zafakturowanej dla ilości i kwoty zafakturowanej dla szczegółów wiersza oryginalnej faktury dla materiału.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-143">Nowa niezafakturowana rzeczywista sprzedaż, która jest obciążana za ilość i kwotę w edytowanych szczegółach wiersza faktury, ich odwrócenie i równoważna faktyczna fakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-144">Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą ilość i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ea1a-145">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji opłaty.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-146">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-147">Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5ea1a-148">Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji opłaty.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-149">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury opłaty.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-150">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z wiersza faktury korygującej, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5ea1a-151">Zafakturowanie pełnego uznania uprzednio zafakturowanego punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-152">Rozliczona sprzedaż za kwotę z oryginalnego wiersza faktury dla punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="5ea1a-153">Stan faktury w punktów kontrolnych jest aktualizowany z <b>Zaksięgowano fakturę dla klienta</b> do <b>Przygotowane do fakturowania</b>.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5ea1a-154">Zafakturowanie częściowego uznania uprzednio zafakturowanego punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5ea1a-155">Ten scenariusz nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="5ea1a-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
