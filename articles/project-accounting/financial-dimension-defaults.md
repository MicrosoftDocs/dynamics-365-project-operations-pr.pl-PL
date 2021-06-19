---
title: Wartości domyślne wymiaru finansowego
description: Ta temat zawiera informacje na temat konfigurowania wartości domyślnych wymiarów finansowych.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013319"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="26180-103">Wartości domyślne wymiaru finansowego</span><span class="sxs-lookup"><span data-stu-id="26180-103">Financial dimension defaults</span></span>

<span data-ttu-id="26180-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="26180-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="26180-105">Aplikacja Dynamics 365 Project Operations używa struktury [wymiarów finansowych](/dynamics365/finance/general-ledger/financial-dimensions) w aplikacji Dynamics 365 Finance w celu uzyskiwania dodatkowych informacji na temat ksiąg i transakcji księgi głównej projektu.</span><span class="sxs-lookup"><span data-stu-id="26180-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="26180-106">W przypadku klienta, źródła finansowania projektu, punktu kontrolnego, pozycji kontraktu projektu lub projektu można ustawić domyślne wymiary finansowe.</span><span class="sxs-lookup"><span data-stu-id="26180-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="26180-107">Definiowanie domyślnych wymiarów finansowych dla klienta</span><span class="sxs-lookup"><span data-stu-id="26180-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="26180-108">Wartości domyślne wymiarów klientów są określane w Finance.</span><span class="sxs-lookup"><span data-stu-id="26180-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="26180-109">Wykonaj następujące kroki, aby ustawić domyślne wymiary.</span><span class="sxs-lookup"><span data-stu-id="26180-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="26180-110">W tym celu należy przejść do **Rozrachunki z odbiorcami** > **Klienci** > **Wszyscy klienci**.</span><span class="sxs-lookup"><span data-stu-id="26180-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="26180-111">Na stronie **Klienci** na karcie **Wymiary finansowe** ustaw wartości wymiarów finansowych dla określonego klienta.</span><span class="sxs-lookup"><span data-stu-id="26180-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="26180-112">Zdefiniuj domyślne wymiary finansowe dla umów dotyczących projektów</span><span class="sxs-lookup"><span data-stu-id="26180-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="26180-113">Kontrakty projektów są tworzone i konserwowane w Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="26180-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="26180-114">Atrybuty obsługi kont dla kontraktów projektów są ustawiane w module **Zarządzanie projektami i ich księgowanie** w Finance.</span><span class="sxs-lookup"><span data-stu-id="26180-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="26180-115">Ustawianie wymiarów finansowych dla źródła finansowania projektu</span><span class="sxs-lookup"><span data-stu-id="26180-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="26180-116">Przejdź do **Zarządzanie projektami i księgowanie** > **Projekty** > **Kontrakty projektu**.</span><span class="sxs-lookup"><span data-stu-id="26180-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="26180-117">Zaznacz rekord, który chcesz zaktualizować, a następnie na karcie **Kontrakt projektu** wybierz pozycję **Pokaż domyślne księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="26180-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="26180-118">Rozwiń **Pokrewne informacje** i wybierz kartę **Źródła finansowania**.</span><span class="sxs-lookup"><span data-stu-id="26180-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="26180-119">Ustaw wartości domyślne wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="26180-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="26180-120">Należy zwrócić uwagę, że wymiar finansowy jest typem domyślnym na podstawie konta klienta.</span><span class="sxs-lookup"><span data-stu-id="26180-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="26180-121">Ustawianie wymiarów finansowych dla projektu pozycji kontraktu</span><span class="sxs-lookup"><span data-stu-id="26180-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="26180-122">Przejdź do **Zarządzanie projektami i księgowanie** > **Projekty** > **Kontrakty projektu**.</span><span class="sxs-lookup"><span data-stu-id="26180-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="26180-123">Zaznacz rekord, który chcesz zaktualizować, a następnie na karcie **Kontrakt projektu** wybierz pozycję **Pokaż domyślne księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="26180-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="26180-124">Rozwiń **Pokrewne informacje** i wybierz kartę **Pozycje kontraktu**.</span><span class="sxs-lookup"><span data-stu-id="26180-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="26180-125">Ustaw wartości domyślne wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="26180-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="26180-126">Wartości domyślne wymiarów finansowych są stosowane i mogą być używane tylko z pozycjami kontraktu z ustalonymi cenami (punktów kontrolnych).</span><span class="sxs-lookup"><span data-stu-id="26180-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="26180-127">Te wartości domyślne są używane w pokrewnych transakcjach i wierszach faktur dotyczących danego projektu.</span><span class="sxs-lookup"><span data-stu-id="26180-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="26180-128">Zdefiniuj domyślne wymiary finansowe dla projektów</span><span class="sxs-lookup"><span data-stu-id="26180-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="26180-129">Kontrakty projektów są tworzone i utrzymywane w (CDS).</span><span class="sxs-lookup"><span data-stu-id="26180-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="26180-130">Atrybuty obsługi kont dla projektów są ustawiane w module **Zarządzanie projektami i ich księgowanie** w Finance.</span><span class="sxs-lookup"><span data-stu-id="26180-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="26180-131">Przejdź do **Zarządzanie projektami i księgowanie** > **Projekty** > **Wszystkie projekty**.</span><span class="sxs-lookup"><span data-stu-id="26180-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="26180-132">Zaznacz rekord, który chcesz zaktualizować, a następnie na karcie **Projekt** wybierz pozycję **Pokaż domyślne księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="26180-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="26180-133">Rozwiń **Pokrewne informacje** i wybierz kartę **Ustawienia**.</span><span class="sxs-lookup"><span data-stu-id="26180-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="26180-134">Ustaw wartości domyślne wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="26180-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="26180-135">Należy zwrócić uwagę, że wymiar finansowy jest typem domyślnym na podstawie konta klienta.</span><span class="sxs-lookup"><span data-stu-id="26180-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="26180-136">Jeśli projekt jest skojarzony z pozycją kontraktu, która ma wielu klientów kontraktów projektów, jest używany podstawowy klient z domyślnymi wymiarami finansowymi.</span><span class="sxs-lookup"><span data-stu-id="26180-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="26180-137">Domyślne wymiary finansowe projektu służą do ustawiania wartości domyślnych wierszy arkusza dla transakcji dotyczących czasu, wydatków i opłat w **Arkusz integracji aplikacji Project Operations** oraz w powiązanych wierszach faktur projektu.</span><span class="sxs-lookup"><span data-stu-id="26180-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]