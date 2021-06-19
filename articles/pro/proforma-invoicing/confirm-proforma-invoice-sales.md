---
title: Potwierdzenie faktury proforma projektu
description: Ten temat zawiera informacje na temat potwierdzania faktur projektu proforma w Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004139"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="6df1c-103">Potwierdzenie faktury proforma projektu</span><span class="sxs-lookup"><span data-stu-id="6df1c-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="6df1c-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="6df1c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6df1c-105">Po potwierdzeniu faktury pro forma stan faktury projektu ustawiony zostanie na **Potwierdzenie**.</span><span class="sxs-lookup"><span data-stu-id="6df1c-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="6df1c-106">Po potwierdzeniu faktura staje się dostępna tylko w trybie do odczytu.</span><span class="sxs-lookup"><span data-stu-id="6df1c-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="6df1c-107">Odtąd fakturę można skorygować tylko wtedy, gdy występują jakiekolwiek korekty lub uznanie zainicjowane przez klienta.</span><span class="sxs-lookup"><span data-stu-id="6df1c-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="6df1c-108">Poniższa tabela zawiera listę wartości rzeczywistych tworzonych przez system.</span><span class="sxs-lookup"><span data-stu-id="6df1c-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="6df1c-109">Te wartości rzeczywiste są tworzone przy wykonywaniu pewnych operacji na wersji roboczej faktury projektu przed jej potwierdzeniem.</span><span class="sxs-lookup"><span data-stu-id="6df1c-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="6df1c-110">
                    <strong>Scenariusz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6df1c-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="6df1c-111">
                    <strong>Wartości rzeczywiste utworzone przy potwierdzeniu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6df1c-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-112">Fakturowanie płatności opartej na zatrzymaniu lub zaliczce</span><span class="sxs-lookup"><span data-stu-id="6df1c-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-113">Wartość rzeczywista sprzedaży fakturowanej typu <strong>Zatrzymanie</strong>, tworzony dla zaliczki lub zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="6df1c-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-114">Niewykorzystana wartość sprzedaży niepodlegającej kwocie ujemnej zatrzymania lub wcześniejszej, która ma być używana do uzgadniania.</span><span class="sxs-lookup"><span data-stu-id="6df1c-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-115">Po pełnym uzgodnieniu z zamówieniem lub zaliczką na fakturze.</span><span class="sxs-lookup"><span data-stu-id="6df1c-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-116">Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="6df1c-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6df1c-117">Ta kwota jest dodatnia, ponieważ powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie zafakturowania zatrzymania lub zaliczki.</span><span class="sxs-lookup"><span data-stu-id="6df1c-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-118">Rzeczywista rozliczona wartość sprzedaży za ilość znajdującą się na tej fakturze.</span><span class="sxs-lookup"><span data-stu-id="6df1c-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6df1c-119">Po częściowym uzgodnieniu z zamówieniem lub zaliczką na fakturze.</span><span class="sxs-lookup"><span data-stu-id="6df1c-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-120">Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="6df1c-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6df1c-121">Ta kwota jest dodatnia, ponieważ powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie zafakturowania zatrzymania lub zaliczki.</span><span class="sxs-lookup"><span data-stu-id="6df1c-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-122">Rzeczywista rozliczona wartość sprzedaży za ilość znajdującą się na tej fakturze.</span><span class="sxs-lookup"><span data-stu-id="6df1c-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-123">Kwota ujemna nierozliczonej sprzedaży pozostałej zaliczki lub zatrzymania, która zostanie użyta podczas uzgodnienia na przyszłych fakturach.</span><span class="sxs-lookup"><span data-stu-id="6df1c-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-124">Fakturowanie transakcji czasowej bez żadnych zmian w stosunku do wersji roboczej faktury.</span><span class="sxs-lookup"><span data-stu-id="6df1c-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-125">Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="6df1c-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-126">Wycofanie rozliczonej kwoty rzeczywistej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="6df1c-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6df1c-127">Fakturowanie transakcji godzinowej, która została edytowana w celu zmniejszenia ilości.</span><span class="sxs-lookup"><span data-stu-id="6df1c-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-128">Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="6df1c-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-129">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu godzin i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-130">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałych godzin i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-131">Fakturowanie transakcji godzinowej, która została edytowana w celu zwiększenia ilości.</span><span class="sxs-lookup"><span data-stu-id="6df1c-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-132">Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="6df1c-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-133">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu godzin i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-134">Fakturowanie transakcji wydatkowej bez żadnych zmian w stosunku do wersji roboczej faktury.</span><span class="sxs-lookup"><span data-stu-id="6df1c-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-135">Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="6df1c-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-136">Rozliczona wartość rzeczywista sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku</span><span class="sxs-lookup"><span data-stu-id="6df1c-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6df1c-137">Fakturowanie transakcji wydatkowej, która została edytowana w celu zmniejszenia ilości.</span><span class="sxs-lookup"><span data-stu-id="6df1c-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-138">Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="6df1c-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-139">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-140">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałej ilości i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-141">Fakturowanie transakcji wydatkowej, która została edytowana w celu zwiększenia ilości.</span><span class="sxs-lookup"><span data-stu-id="6df1c-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-142">Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="6df1c-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-143">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-144">Fakturowanie istotnej transakcji bez żadnych zmian w wersji roboczej faktury.</span><span class="sxs-lookup"><span data-stu-id="6df1c-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-145">Niezafakturowane wycofanie sprzedaży dla ilości i kwoty w pierwotnym zatwierdzeniu wykorzystania materiału.</span><span class="sxs-lookup"><span data-stu-id="6df1c-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-146">Faktyczna sprzedaż zafakturowana dla ilości i kwoty na pierwotnym zatwierdzeniu wykorzystania materiału.</span><span class="sxs-lookup"><span data-stu-id="6df1c-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6df1c-147">Fakturowanie transakcji materiałowej, która została edytowana w celu zmniejszenia ilości.</span><span class="sxs-lookup"><span data-stu-id="6df1c-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-148">Niezafakturowane wycofanie sprzedaży dla ilości i kwoty w pierwotnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="6df1c-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-149">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-150">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałej ilości i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-151">Fakturowanie transakcji materiałowej, która została edytowana w celu zwiększenia ilości.</span><span class="sxs-lookup"><span data-stu-id="6df1c-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-152">Niezafakturowane wycofanie sprzedaży dla ilości i kwoty w pierwotnym zatwierdzeniu wykorzystania materiału.</span><span class="sxs-lookup"><span data-stu-id="6df1c-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-153">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="6df1c-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6df1c-154">Fakturowanie opłaty.</span><span class="sxs-lookup"><span data-stu-id="6df1c-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-155">Wycofanie nierozliczonej sprzedaży za kwotę opłaty w oryginalnym wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="6df1c-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-156">Rozliczona wartość rzeczywista sprzedaży za ilość i kwotę w oryginalnym wierszu arkusza opłaty.</span><span class="sxs-lookup"><span data-stu-id="6df1c-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6df1c-157">Wystawianie fakturowania punktów kontrolnych.</span><span class="sxs-lookup"><span data-stu-id="6df1c-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-158">Rozliczona rzeczywista sprzedaż dla kwoty punktów kontrolnych w oryginalnym punktach kontrolnych pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="6df1c-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6df1c-159">Fakturowanie pozycji kontraktu opartych na produkcie.</span><span class="sxs-lookup"><span data-stu-id="6df1c-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6df1c-160">Rozliczona wartość rzeczywista za wiersz produktu wraz z ilością i kwotą przychodzącą z pozycji kontraktu opartej na produkcie.</span><span class="sxs-lookup"><span data-stu-id="6df1c-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
