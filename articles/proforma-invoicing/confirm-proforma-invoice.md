---
title: Potwierdzenie faktury proforma
description: Ta temat zawiera informacje na temat potwierdzania faktury proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081857"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="54dbe-103">Potwierdzenie faktury proforma</span><span class="sxs-lookup"><span data-stu-id="54dbe-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="54dbe-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="54dbe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="54dbe-105">Po potwierdzeniu faktury pro forma stan faktury projektu ustawiony zostanie na **Potwierdzenie**.</span><span class="sxs-lookup"><span data-stu-id="54dbe-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="54dbe-106">Po potwierdzeniu faktura staje się dostępna tylko w trybie do odczytu.</span><span class="sxs-lookup"><span data-stu-id="54dbe-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="54dbe-107">Faktura może zostać skorygowana tylko wtedy, gdy istnieją zwroty lub kredytowanie zainicjowane przez klienta albo gdy faktura zostanie oznaczona jako zapłacona.</span><span class="sxs-lookup"><span data-stu-id="54dbe-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="54dbe-108">Poniższa tabela zawiera listę wartości rzeczywistych tworzonych przez system.</span><span class="sxs-lookup"><span data-stu-id="54dbe-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="54dbe-109">Te wartości rzeczywiste są tworzone przy wykonywaniu pewnych operacji na wersji roboczej faktury projektu przed jej potwierdzeniem.</span><span class="sxs-lookup"><span data-stu-id="54dbe-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="54dbe-110">
                    <strong>Scenariusz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54dbe-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="54dbe-111">
                    <strong>Wartości rzeczywiste utworzone przy potwierdzeniu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54dbe-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54dbe-112">Fakturowanie transakcji czasowej bez żadnych zmian w stosunku do wersji roboczej faktury.</span><span class="sxs-lookup"><span data-stu-id="54dbe-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-113">Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="54dbe-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-114">Wycofanie rozliczonej kwoty rzeczywistej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="54dbe-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="54dbe-115">Fakturowanie transakcji godzinowej, która została edytowana w celu zmniejszenia ilości.</span><span class="sxs-lookup"><span data-stu-id="54dbe-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-116">Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="54dbe-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-117">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu godzin i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="54dbe-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-118">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałych godzin i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="54dbe-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54dbe-119">Fakturowanie transakcji godzinowej, która została edytowana w celu zwiększenia ilości.</span><span class="sxs-lookup"><span data-stu-id="54dbe-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-120">Wycofanie nierozliczonej sprzedaży za godziny i kwotę w oryginalnym zatwierdzeniu czasu.</span><span class="sxs-lookup"><span data-stu-id="54dbe-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-121">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu godzin i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="54dbe-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54dbe-122">Fakturowanie transakcji wydatkowej bez żadnych zmian w stosunku do wersji roboczej faktury.</span><span class="sxs-lookup"><span data-stu-id="54dbe-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-123">Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="54dbe-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-124">Rozliczona wartość rzeczywista sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="54dbe-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="54dbe-125">Fakturowanie transakcji wydatkowej, która została edytowana w celu zmniejszenia ilości.</span><span class="sxs-lookup"><span data-stu-id="54dbe-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-126">Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="54dbe-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-127">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="54dbe-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-128">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest nie pobierana z powodu pozostałej ilości i kwoty po odliczeniu skorygowanych wartości w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="54dbe-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54dbe-129">Fakturowanie transakcji wydatkowej, która została edytowana w celu zwiększenia ilości.</span><span class="sxs-lookup"><span data-stu-id="54dbe-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-130">Wycofanie nierozliczonej sprzedaży za ilość i kwotę w oryginalnym zatwierdzeniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="54dbe-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-131">Nowa nierozliczona kwota rzeczywista sprzedaży, która jest pobierana z powodu ilości i kwoty w edytowanym wierszu faktury, wycofanie rzeczywistej niezafakturowanej sprzedaży i odpowiadającą jej rzeczywista zafakturowana sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="54dbe-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54dbe-132">Fakturowanie opłaty.</span><span class="sxs-lookup"><span data-stu-id="54dbe-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-133">Wycofanie nierozliczonej sprzedaży za kwotę opłaty w oryginalnym wierszu arkusza.</span><span class="sxs-lookup"><span data-stu-id="54dbe-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-134">Rozliczona wartość rzeczywista sprzedaży za ilość i kwotę w oryginalnym wierszu arkusza opłaty.</span><span class="sxs-lookup"><span data-stu-id="54dbe-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="54dbe-135">Wystawianie fakturowania punktów kontrolnych.</span><span class="sxs-lookup"><span data-stu-id="54dbe-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="54dbe-136">Rozliczona rzeczywista sprzedaż dla kwoty punktów kontrolnych w oryginalnym punktach kontrolnych pozycji kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="54dbe-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
