---
title: Skorygowane faktury - wersja uproszczona
description: Ta temat zawiera informacje na temat pracy korekt faktur w Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176444"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="f4387-103">Skorygowane faktury - wersja uproszczona</span><span class="sxs-lookup"><span data-stu-id="f4387-103">Corrected invoices - lite</span></span>

<span data-ttu-id="f4387-104">_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_</span><span class="sxs-lookup"><span data-stu-id="f4387-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f4387-105">Potwierdzona faktura projektu może być skorygowana w celu wprowadzenia zmian lub uznań, po uprzedniej zgodzie klienta i menedżera projektu.</span><span class="sxs-lookup"><span data-stu-id="f4387-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f4387-106">Aby dokonać edycji potwierdzonej faktury, otwórz potwierdzoną fakturę i wybierz pozycję **Koryguj tę fakturę**.</span><span class="sxs-lookup"><span data-stu-id="f4387-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f4387-107">Ta opcja jest niedostępna, jeśli nie została potwierdzona faktura projektu.</span><span class="sxs-lookup"><span data-stu-id="f4387-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="f4387-108">Nowa wersja robocza faktury jest tworzona na podstawie potwierdzonej faktury.</span><span class="sxs-lookup"><span data-stu-id="f4387-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f4387-109">Wszystkie szczegóły wiersza faktury z uprzednio potwierdzonej faktury zostaną skopiowane do nowej wersji roboczej.</span><span class="sxs-lookup"><span data-stu-id="f4387-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f4387-110">Oto niektóre z najważniejszych informacji na temat nowych wierszy korygowanych faktur:</span><span class="sxs-lookup"><span data-stu-id="f4387-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f4387-111">Wszystkie ilości są aktualizowane na zero.</span><span class="sxs-lookup"><span data-stu-id="f4387-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f4387-112">Aplikacja zakłada, że wszystkie zafakturowane towary są całkowicie uznane.</span><span class="sxs-lookup"><span data-stu-id="f4387-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f4387-113">Jeśli jest to konieczne, można ręcznie zaktualizować te ilości, tak aby odpowiadały ilości zafakturowanej, a nie uznanej ilości.</span><span class="sxs-lookup"><span data-stu-id="f4387-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f4387-114">W zależności od wprowadzonej ilości program obliczy uznaną zaksięgowaną kwotę.</span><span class="sxs-lookup"><span data-stu-id="f4387-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f4387-115">Ta kwota jest odzwierciedlona w wartościach rzeczywistych tworzonych podczas potwierdzania faktury korygującej.</span><span class="sxs-lookup"><span data-stu-id="f4387-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f4387-116">W przypadku wprowadzania zmian do kwoty podatku należy wprowadzić prawidłową kwotę podatku, a nie kwotę podatku, która ma być uznana.</span><span class="sxs-lookup"><span data-stu-id="f4387-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f4387-117">Poprzednio potwierdzone pozycje kontraktu opartego na produktach nie są kopiowane.</span><span class="sxs-lookup"><span data-stu-id="f4387-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="f4387-118">Przetwarzanie korekt na fakturze projektu opartej na produkcie nie jest obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="f4387-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="f4387-119">Korekta punktów kontrolnych jest zawsze przetwarzana jako pełne uznania.</span><span class="sxs-lookup"><span data-stu-id="f4387-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="f4387-120">Jeśli klient został zafakturowany na nieprawidłową kwotę, można skorygować zatrzymanie lub zaliczkę.</span><span class="sxs-lookup"><span data-stu-id="f4387-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="f4387-121">Uzgodnienia dotyczące zatrzymań i zaliczek można skorygować, jeśli do uzgodnienia została użyta nieprawidłowa kwota względem opłat na poprzednio potwierdzonej fakturze zastosowano nieprawidłową kwotę.</span><span class="sxs-lookup"><span data-stu-id="f4387-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4387-122">Szczegóły wierszy faktury, które są korektą do innych zafakturowanych opłat, mają w polu **Korektę** ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="f4387-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="f4387-123">Na fakturach, dla których istnieją poprawione dane w wierszu faktury znajduje się pole **Wprowadzono korektę**, która ma również ustawioną wartość na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="f4387-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="f4387-124">Wartości rzeczywiste utworzone w potwierdzeniu faktury korygującej:</span><span class="sxs-lookup"><span data-stu-id="f4387-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="f4387-125">Poniżej znajdują się wartości rzeczywiste, które zostały utworzone przez aplikację na bazie korekty na podstawie operacji wykonywanych na wersji roboczej faktury korygującej przed jej potwierdzeniem.</span><span class="sxs-lookup"><span data-stu-id="f4387-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f4387-126">
                    <strong>Scenariusz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f4387-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f4387-127">
                    <strong>Wartości rzeczywiste utworzone przy potwierdzeniu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f4387-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f4387-128">Potwierdź korektę zafakturowanego zatrzymania lub zaliczki.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f4387-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-129">Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="f4387-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f4387-130">Ta kwota jest dodatnia, ponieważ powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie zafakturowania zatrzymania lub zaliczki.</span><span class="sxs-lookup"><span data-stu-id="f4387-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-131">Wartość rzeczywista wycofanych wyliczonych sprzedaży jest tworzona dla kwoty zaliczki lub zatrzymania, w celu wycofania pierwotnej zafakturowanej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="f4387-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-132">Tworzona jest nowa wartość rzeczywista zafakturowanej sprzedaży w korygowanym wierszu faktury opartym na zaliczce lub zatrzymaniu.</span><span class="sxs-lookup"><span data-stu-id="f4387-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-133">Niezafakturowana wartość sprzedaży negatywnej wartości rzeczywistej wiersza faktury opartego na zaliczce lub zatrzymaniu, która ma być używana do uzgadniania.</span><span class="sxs-lookup"><span data-stu-id="f4387-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f4387-134">Potwierdzenie korekty wcześniej uzgodnionej zaliczki lub zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="f4387-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-135">Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="f4387-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f4387-136">Ta kwota jest dodatnia i powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie poprzedniego uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="f4387-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-137">Rzeczywiste rozliczone wycofanie wartości sprzedaży za ilość znajdującą się na poprzedniej fakturze.</span><span class="sxs-lookup"><span data-stu-id="f4387-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-138">Stosowana jest nowa rozliczona wartość rzeczywista w korygowanym wierszu faktury opartym na zaliczce lub zatrzymaniu.</span><span class="sxs-lookup"><span data-stu-id="f4387-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-139">Niezafakturowana wartość sprzedaży o negatywnej wartości rzeczywistej ze skorygowanych pozostałych zaliczek lub zatrzymań, która ma być używana na późniejszych fakturach.</span><span class="sxs-lookup"><span data-stu-id="f4387-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f4387-140">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji czasowej.</span><span class="sxs-lookup"><span data-stu-id="f4387-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-141">Rozliczona sprzedaż za godziny i kwotę z oryginalnego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="f4387-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-142">Nowa nierozliczona wartość rzeczywista sprzedaży za godziny i kwotę z oryginalnego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="f4387-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f4387-143">Fakturowanie częściowego uznania transakcji czasu.</span><span class="sxs-lookup"><span data-stu-id="f4387-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-144">Rozliczona sprzedaż za godziny i kwotę z oryginalnego fakturowanego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="f4387-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-145">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna względem godzin i kwoty w edytowanym wierszu faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="f4387-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-146">Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą liczbę godzin i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="f4387-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f4387-147">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="f4387-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-148">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="f4387-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-149">Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="f4387-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f4387-150">Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="f4387-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-151">Rozliczone wycofanie sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="f4387-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-152">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z korygowanego wiersza faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="f4387-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-153">Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą ilość i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="f4387-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f4387-154">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji opłaty.</span><span class="sxs-lookup"><span data-stu-id="f4387-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-155">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.</span><span class="sxs-lookup"><span data-stu-id="f4387-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-156">Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.</span><span class="sxs-lookup"><span data-stu-id="f4387-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f4387-157">Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji opłaty.</span><span class="sxs-lookup"><span data-stu-id="f4387-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-158">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury opłaty.</span><span class="sxs-lookup"><span data-stu-id="f4387-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-159">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z wiersza faktury korygującej, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="f4387-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f4387-160">Zafakturowanie pełnego uznania uprzednio zafakturowanego punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="f4387-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-161">Rozliczona sprzedaż za kwotę z oryginalnego wiersza faktury dla punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="f4387-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f4387-162">Faktura punktu kontrolnego lub status fakturowania w pozycji kontraktu projektu są aktualizowane na **Gotowe do fakturowania**.</span><span class="sxs-lookup"><span data-stu-id="f4387-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f4387-163">Zafakturowanie częściowego uznania uprzednio zafakturowanego punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="f4387-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-164">Nieobsługiwane</span><span class="sxs-lookup"><span data-stu-id="f4387-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f4387-165">Uznania i korekty poprzednio zafakturowanego wiersza kontraktu opartego na produkcie.</span><span class="sxs-lookup"><span data-stu-id="f4387-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f4387-166">Nieobsługiwane</span><span class="sxs-lookup"><span data-stu-id="f4387-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
