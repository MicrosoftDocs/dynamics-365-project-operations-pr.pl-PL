---
title: Tworzenie faktur korygujących opartych na projekcie
description: Ten temat zawiera informacje o fakturach korygujących w Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788884"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="b6c74-103">Tworzenie faktur korygujących opartych na projekcie</span><span class="sxs-lookup"><span data-stu-id="b6c74-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="b6c74-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="b6c74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b6c74-105">Potwierdzona faktura projektu może być skorygowana w celu wprowadzenia zmian lub uznań, po uprzedniej zgodzie klienta i menedżera projektu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="b6c74-106">Aby dokonać edycji potwierdzonej faktury, otwórz potwierdzoną fakturę i wybierz pozycję **Koryguj tę fakturę**.</span><span class="sxs-lookup"><span data-stu-id="b6c74-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="b6c74-107">Ta opcja jest niedostępna, jeśli nie została potwierdzona faktura projektu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="b6c74-108">Nowa wersja robocza faktury jest tworzona na podstawie potwierdzonej faktury.</span><span class="sxs-lookup"><span data-stu-id="b6c74-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="b6c74-109">Wszystkie szczegóły wiersza faktury z uprzednio potwierdzonej faktury zostaną skopiowane do nowej wersji roboczej.</span><span class="sxs-lookup"><span data-stu-id="b6c74-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="b6c74-110">Poniżej przedstawiono kilka kluczowych punktów, które pomogą Ci lepiej zrozumieć szczegóły linii na nowej skorygowanej fakturze:</span><span class="sxs-lookup"><span data-stu-id="b6c74-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="b6c74-111">Wszystkie ilości są aktualizowane na zero.</span><span class="sxs-lookup"><span data-stu-id="b6c74-111">All quantities are updated to zero.</span></span> <span data-ttu-id="b6c74-112">Zakłada się, że wszystkie zafakturowane pozycje są w pełni zaksięgowane.</span><span class="sxs-lookup"><span data-stu-id="b6c74-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="b6c74-113">Jeśli jest to konieczne, można ręcznie zaktualizować te ilości, tak aby odpowiadały ilości zafakturowanej, a nie uznanej ilości.</span><span class="sxs-lookup"><span data-stu-id="b6c74-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="b6c74-114">W zależności od wprowadzonej ilości program obliczy uznaną zaksięgowaną kwotę.</span><span class="sxs-lookup"><span data-stu-id="b6c74-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="b6c74-115">Ta kwota jest odzwierciedlona w wartościach rzeczywistych tworzonych podczas potwierdzania faktury korygującej.</span><span class="sxs-lookup"><span data-stu-id="b6c74-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="b6c74-116">W przypadku wprowadzania zmian do kwoty podatku należy wprowadzić prawidłową kwotę podatku, a nie kwotę podatku, która ma być uznana.</span><span class="sxs-lookup"><span data-stu-id="b6c74-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="b6c74-117">Korekta punktów kontrolnych jest zawsze przetwarzana jako pełne uznania.</span><span class="sxs-lookup"><span data-stu-id="b6c74-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="b6c74-118">Jeśli klient został zafakturowany na nieprawidłową kwotę, można skorygować zatrzymanie lub zaliczkę.</span><span class="sxs-lookup"><span data-stu-id="b6c74-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="b6c74-119">Uzgodnienia dotyczące zatrzymań i zaliczek można skorygować, jeśli do uzgodnienia została użyta nieprawidłowa kwota względem opłat na poprzednio potwierdzonej fakturze zastosowano nieprawidłową kwotę.</span><span class="sxs-lookup"><span data-stu-id="b6c74-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6c74-120">Szczegóły wiersza faktury, które są poprawiane w innych już zafakturowanych opłatach, mają w polu **Korekta** ustawioną wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="b6c74-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="b6c74-121">Na fakturach, dla których istnieją poprawione dane w wierszu faktury znajduje się pole **Wprowadzono korektę**, która ma również ustawioną wartość na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="b6c74-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="b6c74-122">Wartości rzeczywiste utworzone w potwierdzeniu faktury korygującej</span><span class="sxs-lookup"><span data-stu-id="b6c74-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="b6c74-123">W poniższej tabeli przedstawiono wartości rzeczywiste, które są tworzone po potwierdzenia faktury korekcyjnej.</span><span class="sxs-lookup"><span data-stu-id="b6c74-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="b6c74-124">
                    <strong>Scenariusz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6c74-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="b6c74-125">
                    <strong>Wartości rzeczywiste utworzone przy potwierdzeniu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6c74-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="b6c74-126">Potwierdź korektę zafakturowanego zatrzymania lub zaliczki.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6c74-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-127">Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="b6c74-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b6c74-128">Ta kwota jest dodatnia, ponieważ powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie zafakturowania zatrzymania lub zaliczki.</span><span class="sxs-lookup"><span data-stu-id="b6c74-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-129">Wartość rzeczywista wycofanych wyliczonych sprzedaży jest tworzona dla kwoty zaliczki lub zatrzymania, w celu wycofania pierwotnej zafakturowanej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="b6c74-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-130">Tworzona jest nowa wartość rzeczywista zafakturowanej sprzedaży w korygowanym wierszu faktury opartym na zaliczce lub zatrzymaniu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-131">Niezafakturowana wartość sprzedaży negatywnej wartości rzeczywistej wiersza faktury opartego na zaliczce lub zatrzymaniu, która ma być używana do uzgadniania.</span><span class="sxs-lookup"><span data-stu-id="b6c74-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="b6c74-132">Potwierdzenie korekty wcześniej uzgodnionej zaliczki lub zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="b6c74-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-133">Wycofanie nierozliczonej sprzedaży zaliczki lub zatrzymania, która zostały utworzone na potrzeby uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="b6c74-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b6c74-134">Ta kwota jest dodatnia i powoduje anulowanie ujemnych wartości, które zostały utworzone w momencie poprzedniego uzgodnienia.</span><span class="sxs-lookup"><span data-stu-id="b6c74-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-135">Rzeczywiste rozliczone wycofanie wartości sprzedaży za ilość znajdującą się na poprzedniej fakturze.</span><span class="sxs-lookup"><span data-stu-id="b6c74-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-136">Stosowana jest nowa rozliczona wartość rzeczywista w korygowanym wierszu faktury opartym na zaliczce lub zatrzymaniu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-137">Niezafakturowana wartość sprzedaży o negatywnej wartości rzeczywistej ze skorygowanych pozostałych zaliczek lub zatrzymań, która ma być używana na późniejszych fakturach.</span><span class="sxs-lookup"><span data-stu-id="b6c74-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6c74-138">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji czasowej.</span><span class="sxs-lookup"><span data-stu-id="b6c74-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-139">Rozliczona sprzedaż za godziny i kwotę z oryginalnego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-140">Nowa nierozliczona wartość rzeczywista sprzedaży za godziny i kwotę z oryginalnego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b6c74-141">Fakturowanie częściowego uznania transakcji czasu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-142">Rozliczona sprzedaż za godziny i kwotę z oryginalnego fakturowanego wiersza faktury dla czasu.</span><span class="sxs-lookup"><span data-stu-id="b6c74-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-143">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna względem godzin i kwoty w edytowanym wierszu faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="b6c74-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-144">Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą liczbę godzin i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="b6c74-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6c74-145">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="b6c74-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-146">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="b6c74-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-147">Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="b6c74-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b6c74-148">Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji wydatkowej.</span><span class="sxs-lookup"><span data-stu-id="b6c74-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-149">Rozliczone wycofanie sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla wydatku.</span><span class="sxs-lookup"><span data-stu-id="b6c74-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-150">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z korygowanego wiersza faktury, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="b6c74-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-151">Nowa nierozliczona wartość rzeczywista sprzedaży, która jest odpłatna za pozostałą ilość i kwotę po odjęciu skorygowanych wartości w szczegółach wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="b6c74-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6c74-152">Zafakturowanie pełnego uznania uprzednio zafakturowanej transakcji opłaty.</span><span class="sxs-lookup"><span data-stu-id="b6c74-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-153">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.</span><span class="sxs-lookup"><span data-stu-id="b6c74-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-154">Nowa nierozliczona wartość aktualna sprzedaży na ilość i kwotę z oryginalnego fakturowanego wiersza faktury dla opłaty.</span><span class="sxs-lookup"><span data-stu-id="b6c74-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6c74-155">Zafakturowanie częściowego uznania uprzednio zafakturowanej transakcji opłaty.</span><span class="sxs-lookup"><span data-stu-id="b6c74-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-156">Wycofana rozliczona sprzedaż za ilość i kwotę z oryginalnego fakturowanego wiersza faktury opłaty.</span><span class="sxs-lookup"><span data-stu-id="b6c74-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-157">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest odpłatna dla ilości i kwoty z wiersza faktury korygującej, wycofanie tego i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="b6c74-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b6c74-158">Zafakturowanie pełnego uznania uprzednio zafakturowanego punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="b6c74-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-159">Rozliczona sprzedaż za kwotę z oryginalnego wiersza faktury dla punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="b6c74-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="b6c74-160">Stan faktury w punktów kontrolnych jest aktualizowany z <b>Zaksięgowano fakturę dla klienta</b> do <b>Przygotowane do fakturowania</b>.</span><span class="sxs-lookup"><span data-stu-id="b6c74-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b6c74-161">Zafakturowanie częściowego uznania uprzednio zafakturowanego punktu kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="b6c74-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6c74-162">Nieobsługiwane</span><span class="sxs-lookup"><span data-stu-id="b6c74-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
