---
title: Zarządzanie propozycjami faktur projektu
description: Ten temat zawiera szczegółowe informacje na temat przetwarzania faktur wystawianych dla klientów za pomocą Project Operations dla scenariuszy opartych na zasobach / braku zapasów.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089284"
---
# <a name="manage-project-invoice-proposals"></a><span data-ttu-id="7f439-103">Zarządzanie propozycjami faktur projektu</span><span class="sxs-lookup"><span data-stu-id="7f439-103">Manage project invoice proposals</span></span>

<span data-ttu-id="7f439-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="7f439-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7f439-105">Propozycje faktur projektu mogą być przetwarzane przez dział rozliczeń, jeśli spełnione są następujące dwa warunki:</span><span class="sxs-lookup"><span data-stu-id="7f439-105">Project invoice proposals can be processed by your billing department when the following two conditions are met:</span></span>

  - <span data-ttu-id="7f439-106">Menedżer projektu potwierdza fakturę proforma w Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7f439-106">The Project manager confirms the proforma invoice in Microsoft Dataverse.</span></span>
  - <span data-ttu-id="7f439-107">Wszystkie nierozliczone transakcje sprzedaży i materiały zawarte na fakturze proforma są publikowane przy użyciu arkusza **integracji aplikacji Project Operations** usługi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7f439-107">All time and material unbilled sales transactions that are included in the proforma invoice are posted using the Dynamics 365 **Project Operations Integration** journal.</span></span>

<span data-ttu-id="7f439-108">Aby dokończyć propozycje faktury projektu w programie Dynamics 365 Finance, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="7f439-108">Use the following steps to complete a project invoice proposal in Dynamics 365 Finance.</span></span>

1. <span data-ttu-id="7f439-109">Przeglądanie informacji dotyczących fakturowania dotyczących transakcji czasowych i materiałowych oraz publikowane w arkuszu **integracji aplikacji Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="7f439-109">Review billing information for time and material transactions and post the **Project Operations Integration** journal.</span></span>
2. <span data-ttu-id="7f439-110">Przeglądanie informacji o fakturowaniu dla punktów kontrolnych rozliczania o stałej cenie.</span><span class="sxs-lookup"><span data-stu-id="7f439-110">Review billing information for fixed price billing milestones.</span></span>
3. <span data-ttu-id="7f439-111">Przejrzyj i sformatuj propozycję faktury za projekt.</span><span class="sxs-lookup"><span data-stu-id="7f439-111">Review and format a project invoice proposal.</span></span>
4. <span data-ttu-id="7f439-112">Księgowanie i drukowanie faktur projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-112">Post and print project invoices.</span></span>

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a><span data-ttu-id="7f439-113">Zarządzanie informacjami dotyczących fakturowania w arkuszu integracji aplikacji Project Operations</span><span class="sxs-lookup"><span data-stu-id="7f439-113">Manage billing information in the Project Operations Integration journal</span></span>

<span data-ttu-id="7f439-114">Dane rzeczywiste projektu utworzone w Dataverse są przeglądane i księgowane w Finance przez księgowego projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-114">Project actuals created in Dataverse are reviewed and posted in Finance by the Project accountant.</span></span> <span data-ttu-id="7f439-115">Aby uzyskać więcej informacji na temat pracy z arkuszem integracji, zobacz [Arkusz integracji w aplikacji Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="7f439-115">For more information about working with the Integration journal, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="7f439-116">Wartości rzeczywiste kosztów i niezafakturowane wartości rzeczywiste sprzedaży są dodawane do arkusza Integracja jako oddzielne wiersze:</span><span class="sxs-lookup"><span data-stu-id="7f439-116">Cost actuals and unbilled sales actuals are added to the Integration journal as separate lines:</span></span>

  - <span data-ttu-id="7f439-117">Cena kosztu jednostkowego i kwota kosztu rzeczywistego kosztu domyślnego z transakcji kosztu rzeczywistego projektu w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7f439-117">The unit cost price and cost amount on the Cost actual default from the project actual cost transaction in Dataverse.</span></span>
  - <span data-ttu-id="7f439-118">Jednostkowa cena sprzedaży i kwota sprzedaży w niezafakturowanej transakcji sprzedaży są domyślne z rzeczywistej niezafakturowanej transakcji sprzedaży projektu w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7f439-118">The unit sales price and sales amount on the Unbilled sales transaction defaults from the project actual unbilled sales transaction in Dataverse.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="7f439-119">Rozliczanie podatku sprzedaży</span><span class="sxs-lookup"><span data-stu-id="7f439-119">Billing sales tax</span></span>

<span data-ttu-id="7f439-120">Obliczenia podatku dla fakturowania są określane przez kombinację pola **Grupa podatku fakturowania** i **Grupa podatku towaru do rozliczania** dla nieunikatowego rekordu sprzedaży w wierszu arkusza **integracji aplikacji Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="7f439-120">Sales tax calculation for billing is determined by the **Billing sales tax group** and **Billing item sales tax group** field combination on an unbilled sales record on the **Project Operations Integration** journal line.</span></span> <span data-ttu-id="7f439-121">System domyślnych wartości tych pól jest oparty na ustawieniach na karcie **Finanse** na stronie **Parametry zarządzania projektami i parametrów księgowania**.</span><span class="sxs-lookup"><span data-stu-id="7f439-121">The system defaults these field values based on settings on the **Financials** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="7f439-122">**Metoda grupy podatku fakturowania** służy do określania domyślnej logiki grupy podatku fakturowania:</span><span class="sxs-lookup"><span data-stu-id="7f439-122">**Sales tax group method** determines the billing sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="7f439-123">**Projekt**: zawsze będzie domyślną grupą podatku fakturowania dla projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-123">**Project**: Will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="7f439-124">Aby przejrzeć lub zmienić domyślną grupę podatku fakturowania w projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Wszystkie projekty**.</span><span class="sxs-lookup"><span data-stu-id="7f439-124">You can review or change the default billing sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
  - <span data-ttu-id="7f439-125">**Kontrakt projektu**: zawsze będzie domyślną grupą podatku fakturowania dla kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-125">**Project contract**: Will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="7f439-126">Aby przejrzeć lub zmienić domyślną grupę podatku fakturowania w kontrakcie projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Kontrakty projektów**.</span><span class="sxs-lookup"><span data-stu-id="7f439-126">You can review or change the default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
  - <span data-ttu-id="7f439-127">**Klient**: zawsze będzie domyślną grupą podatku fakturowania dla klienta.</span><span class="sxs-lookup"><span data-stu-id="7f439-127">**Customer**: Will always default the billing sales tax group from the customer.</span></span>
  - <span data-ttu-id="7f439-128">**Wyszukiwanie**: przeszuka wszystkie powyższe encje i wybierz pierwszą dostępną wartość.</span><span class="sxs-lookup"><span data-stu-id="7f439-128">**Search**: Will search across all the above entities and select the first value available.</span></span> <span data-ttu-id="7f439-129">Wyszukiwanie rozpoczyna się od encji **Projekt**, encji **Kontrakt projektu** oraz encji **Klient**.</span><span class="sxs-lookup"><span data-stu-id="7f439-129">Search starts with the **Project** entity, then the **Project contract** entity, and finally the **Customer** entity.</span></span>

- <span data-ttu-id="7f439-130">**Metoda grupy podatku towaru** służy do określania domyślnej logiki grupy podatku towaru do rozliczenia:</span><span class="sxs-lookup"><span data-stu-id="7f439-130">**Item sales tax group method** determines the billing item sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="7f439-131">W przypadku typów transakcji dotyczących czasu, wydatków i opłat grupa podatku dla elementu rozliczeniowego będzie zawsze domyślną encja **Kategoria projektu**.</span><span class="sxs-lookup"><span data-stu-id="7f439-131">For time, expense, and fee transaction types, the billing item sales tax group will always default from the **Project category** entity.</span></span>
  - <span data-ttu-id="7f439-132">W przypadku typów transakcji materiałowych domyślne wartości grupy podatku dla pozycji rozliczeń są oparte na ustawieniu **Metody grupy podatku** w **Parametrach zarządzania projektami i księgowania**.</span><span class="sxs-lookup"><span data-stu-id="7f439-132">For material transaction types, the billing item sales tax group defaults based on the **Item sales tax group method** setting in **Project management and accounting parameters**.</span></span> <span data-ttu-id="7f439-133">Numer pozycji jest domyślnie pobiera grupę podatku dla pozycji rozliczeń dla encji **Produkt wydany**.</span><span class="sxs-lookup"><span data-stu-id="7f439-133">The item number defaults the item sales tax group from the **Released product** entity.</span></span> <span data-ttu-id="7f439-134">Kategoria domyślnie określa grupę podatków dla towaru z encji **Kategoria projektu**.</span><span class="sxs-lookup"><span data-stu-id="7f439-134">The category defaults the item sales tax group from the **Project category** entity.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="7f439-135">Wymiary finansowe</span><span class="sxs-lookup"><span data-stu-id="7f439-135">Financial dimensions</span></span>

<span data-ttu-id="7f439-136">Wymiary finansowe dla niezafakturowanych rekordów sprzedaży w arkuszu **Integracja Project Operations** domyślnie z encji **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="7f439-136">The financial dimensions for unbilled sales records in the **Project Operations Integration** journal default from the **Project** entity.</span></span> <span data-ttu-id="7f439-137">Wymiary finansowe można przejrzeć i dostosować, wybierając opcję **Dystrybuuj kwoty**.</span><span class="sxs-lookup"><span data-stu-id="7f439-137">Financial dimensions can be reviewed and adjusted by selecting **Distribute Amounts**.</span></span> <span data-ttu-id="7f439-138">Jeśli potrzebujesz zmienić wymiary finansowe niezafakturowanego rekordu sprzedaży po zaksięgowaniu arkusza integracji, ale przed potwierdzeniem faktury Proforma, przejdź do **Wszystkie projekty** > **Zarządzaj** > **Transakcje zaksięgowane**, wybierz transakcję, a następnie wybierz **Proces** > **Koryguj Księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="7f439-138">If you need to change the financial dimensions of the unbilled sales record after the Integration journal is posted but before the Proforma invoice is confirmed, go to **All Projects** > **Manage** > **Posted transactions**, select the transaction, and then select **Process** > **Adjust accounting**.</span></span>

### <a name="exchange-rates"></a><span data-ttu-id="7f439-139">Kursy wymiany</span><span class="sxs-lookup"><span data-stu-id="7f439-139">Exchange rates</span></span>

<span data-ttu-id="7f439-140">Niezafakturowana waluta transakcji w Dataverse jest używana jako waluta transakcji w Finance i konwertowana na walutę księgową firmy przy użyciu kursów wymiany zdefiniowanych w Finance.</span><span class="sxs-lookup"><span data-stu-id="7f439-140">Unbilled transaction currency in Dataverse is used as transaction currency in Finance and converted to company's accounting currency using exchange rates defined in Finance.</span></span>


## <a name="manage-the-financial-attributes-of-billing-milestones"></a><span data-ttu-id="7f439-141">Zarządzanie atrybutami finansowymi punktów kontrolnych rozliczania</span><span class="sxs-lookup"><span data-stu-id="7f439-141">Manage the financial attributes of billing milestones</span></span> 

<span data-ttu-id="7f439-142">Wiersze kontraktu dotyczącego projektu korzystające z metody fakturowania ze stałą ceną są fakturowane za pośrednictwem [punktach kontrolnych z ustalonymi cenami](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span><span class="sxs-lookup"><span data-stu-id="7f439-142">Project contract lines using the fixed price billing method are invoiced through [Fixed price milestones](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span></span> <span data-ttu-id="7f439-143">Księgowy projektu może przeglądać etapy rozliczeń w programie Finance, przechodząc do **Zarządzanie projektami i księgowanie** > **Wszystkie projekty** > **Zarządzaj** > **Transakcje dotyczące klienta**.</span><span class="sxs-lookup"><span data-stu-id="7f439-143">The Project accountant can review billing milestones in Finance by going to **Project management and accounting** > **All projects** > **Manage** > **On-account transactions**.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="7f439-144">Rozliczanie podatku sprzedaży</span><span class="sxs-lookup"><span data-stu-id="7f439-144">Billing sales tax</span></span>

<span data-ttu-id="7f439-145">Wartości **Grupa podatków** i **Grupa podatku towaru** są domyślnie ustawione na podstawie ustawień, gdy nowy punkt kontrolny fakturowania jest tworzony w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7f439-145">The **Sales tax group** and **Item sales tax group**  values default from the settings when a new billing milestone is created in Dataverse.</span></span> <span data-ttu-id="7f439-146">System domyślnie ustawia wartości w tych polach na podstawie ustawień na karcie **Finanse** na stronie **parametrach zarządzania projektami i księgowania**.</span><span class="sxs-lookup"><span data-stu-id="7f439-146">The system defaults the values to these fields based on settings on the **Financial** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="7f439-147">**Metoda grupy podatku fakturowania** określa domyślną logikę **Grupy rozliczenia podatków**:</span><span class="sxs-lookup"><span data-stu-id="7f439-147">**Sales tax group method** determines the defaulting logic of the **Billing sales tax group**:</span></span>

    - <span data-ttu-id="7f439-148">**Projekt** zawsze będzie domyślną grupą podatku fakturowania dla projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-148">**Project** will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="7f439-149">Aby przejrzeć lub zmienić domyślną grupę podatku w projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Wszystkie projekty**.</span><span class="sxs-lookup"><span data-stu-id="7f439-149">You can review or change the default sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
    - <span data-ttu-id="7f439-150">**Kontrakt projektu** zawsze będzie domyślną grupą podatku fakturowania dla kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-150">**Project contract** will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="7f439-151">Aby przejrzeć lub zmienić domyślną grupę podatku fakturowania w kontrakcie projekcie, wybierz opcję **Pokaż domyślne księgowanie** na stronie **Kontrakty projektów**.</span><span class="sxs-lookup"><span data-stu-id="7f439-151">You can review or change default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
    - <span data-ttu-id="7f439-152">**Klient** zawsze będzie domyślną grupą podatku fakturowania dla klienta.</span><span class="sxs-lookup"><span data-stu-id="7f439-152">**Customer** will always default to the billing sales tax group from the customer.</span></span>
    - <span data-ttu-id="7f439-153">**Wyszukiwanie**:przeszuka wszystkie powyższe encje na tej liście i wybierz pierwszą dostępną wartość.</span><span class="sxs-lookup"><span data-stu-id="7f439-153">**Search** will search across all the entities in this list and select the first value available.</span></span> <span data-ttu-id="7f439-154">Wyszukiwanie rozpoczyna się od encji **Projekt**, encji **Kontrakt projektu** oraz encji **Klient**.</span><span class="sxs-lookup"><span data-stu-id="7f439-154">Search starts with the **Project** entity, then the **Project contract** entity, and then the **Customer** entity.</span></span>

- <span data-ttu-id="7f439-155">**Grupa podatku produktu o stałej cenie punktów kontrolnych** jest używana, aby domyślna wartość pola wynosiła **Grupa podatku towaru do rozliczania**.</span><span class="sxs-lookup"><span data-stu-id="7f439-155">**Fixed price milestone item sales tax group** is used to default the value to the **Item sales tax group** field.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="7f439-156">Wymiary finansowe</span><span class="sxs-lookup"><span data-stu-id="7f439-156">Financial dimensions</span></span>

<span data-ttu-id="7f439-157">Domyślne wymiary finansowe dla punktu kontrolnego fakturowania ze stałą ceną są ustawiane w wierszach umowy dotyczącej projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-157">Default financial dimensions for the fixed price billing milestone are set on Project contract lines.</span></span> <span data-ttu-id="7f439-158">Wybierz pozycję **Kontrakty projektów** > **Pokaż domyślne księgowanie**, a na karcie **Wiersze kontraktu** wybierz **wiersz umowy cenowej**, a następnie ustaw wartości wymiarów finansowych, których chcesz użyć jako domyślnych.</span><span class="sxs-lookup"><span data-stu-id="7f439-158">Go to **Project contracts** > **Show default accounting** and on the **Contract lines** tab, select **price contract line**, then set the financial dimension values that you want to use as the default.</span></span>

<span data-ttu-id="7f439-159">Księgowy projektu może edytować informacje o podatku od sprzedaży i wymiarach finansowych w punktach kontrolnych faktur do momentu utworzenia propozycji faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-159">The Project accountant can edit the sales tax and financial dimensions information on invoice milestones up until the Project invoice proposal is created.</span></span>


## <a name="create-project-invoice-proposals"></a><span data-ttu-id="7f439-160">Utwórz propozycje faktur za projekt</span><span class="sxs-lookup"><span data-stu-id="7f439-160">Create project invoice proposals</span></span>

<span data-ttu-id="7f439-161">Oferty na fakturę projektu można przejrzeć w module **Zarządzanie projektami i księgowanie**, przechodząc do **Faktury projektu** > **Propozycje faktur projektu**.</span><span class="sxs-lookup"><span data-stu-id="7f439-161">Project invoice proposals can be reviewed in the **Project management and accounting** module by going to **Project invoices** > **Project invoice proposals**.</span></span>

<span data-ttu-id="7f439-162">Nagłówek propozycji faktury projektu jest tworzony w Finance, gdy faktura Proforma jest potwierdzana w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7f439-162">The Project invoice proposal header is created in Finance when the Proforma invoice is confirmed in Dataverse.</span></span> <span data-ttu-id="7f439-163">Aby ułatwić uzgodnienie, system ustawia numer propozycji faktury za projekt w programie Finance na taki sam numer, jak identyfikator faktury Proforma w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7f439-163">For easier reconciliation, the system sets the Project invoice proposal number in Finance to the same number as the Proforma invoice ID in Dataverse.</span></span> <span data-ttu-id="7f439-164">Ponieważ faktury Proforma niekoniecznie są potwierdzane w tej samej kolejności, w jakiej są tworzone, sekwencja numerów propozycji faktury projektu w programie Finance musi zezwalać na zmiany w coraz niższych i wyższych numerach.</span><span class="sxs-lookup"><span data-stu-id="7f439-164">Because Proforma invoices are not necessarily confirmed in the same order they are created, the Project invoice proposal number sequence in Finance must allow for changes to lower and higher numbers.</span></span> <span data-ttu-id="7f439-165">Skonfiguruj sekwencje numerów, korzystając z następujących kroków:</span><span class="sxs-lookup"><span data-stu-id="7f439-165">Configure number sequences using the following steps:</span></span>

1. <span data-ttu-id="7f439-166">W Finance przejdź do **Administracja organizacji** > **Sekwencje numerów** > **Sekwencje numerów**.</span><span class="sxs-lookup"><span data-stu-id="7f439-166">In Finance, go to **Organization Administration** > **Number sequences** > **Number sequences**.</span></span>
2. <span data-ttu-id="7f439-167">W filtrze **Obszar** wybierz opcję **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="7f439-167">In the **Area** filter, select **Projects**.</span></span>
3. <span data-ttu-id="7f439-168">W filtrze **Odwołania** wybierz opcję **Propozycja faktury**.</span><span class="sxs-lookup"><span data-stu-id="7f439-168">In the **Reference** filter, select **Invoice proposal**.</span></span>
4. <span data-ttu-id="7f439-169">Pole **Firma** umożliwia filtrowanie poszczególnych firm, dla których włączono integrację Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7f439-169">Use the **Company** field to filter each legal entity with Project Operations Dataverse integration enabled.</span></span>
5. <span data-ttu-id="7f439-170">Otwórz **Szczegóły sekwencji numerów** i na karcie **Ogólne**:</span><span class="sxs-lookup"><span data-stu-id="7f439-170">Open **Number Sequence details** and on the **General** tab set:</span></span>

    - <span data-ttu-id="7f439-171">**Zezwalaj na zmiany użytkownika: Do niższej liczby** = **Tak**</span><span class="sxs-lookup"><span data-stu-id="7f439-171">**Allow user changes: To a lower number** = **Yes**</span></span>
    - <span data-ttu-id="7f439-172">**Zezwalaj na zmiany użytkownika: Do wyższej liczby** = **Tak**</span><span class="sxs-lookup"><span data-stu-id="7f439-172">**Allow user changes: To a higher number** = **Yes**</span></span>

<span data-ttu-id="7f439-173">Wiersze propozycji faktury projektu są dodawane przez system przy użyciu procesu okresowego **Import z tabeli przemieszczania** (**Zarządzanie projektami i księgowanie** > **Okresowe** > **Integracja Project Operations** > **Import z tabeli przemieszczania**).</span><span class="sxs-lookup"><span data-stu-id="7f439-173">Project invoice proposal lines are added by the system using the periodic process **Import from staging table** (**Project management and accounting** > **Periodic** > **Project Operations integration** > **Import from staging table**).</span></span> <span data-ttu-id="7f439-174">Ten proces można uruchomić ręcznie lub przy użyciu harmonogramu okresowego.</span><span class="sxs-lookup"><span data-stu-id="7f439-174">This process can be run manually or by using a periodic schedule.</span></span> <span data-ttu-id="7f439-175">System nie doda wierszy do dokumentu propozycji faktury, dopóki wszystkie wiersze nie będą gotowe do zafakturowania.</span><span class="sxs-lookup"><span data-stu-id="7f439-175">The system won't add lines to the invoice proposal document until all the lines are ready to be invoiced.</span></span> <span data-ttu-id="7f439-176">Transakcje czasowe i materiałowe są gotowe do zafakturowania tylko wtedy, gdy są zaksięgowane przy użyciu arkusza **Integracja Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="7f439-176">Time and material transactions are ready to be invoiced only when they are posted using the **Project Operations Integration** journal.</span></span>

## <a name="format-and-print-invoice-proposals"></a><span data-ttu-id="7f439-177">Formatowanie i drukowanie propozycji faktur</span><span class="sxs-lookup"><span data-stu-id="7f439-177">Format and print invoice proposals</span></span>

<span data-ttu-id="7f439-178">Księgowy projektu może dostosować wydruk faktury za projekt, korzystając z propozycji faktury **Formatowanie propozycji faktury** oraz funkcji zarządzania drukowaniem.</span><span class="sxs-lookup"><span data-stu-id="7f439-178">The Project accountant can customize a project invoice printout by using the **Format invoice proposal** page and print management capabilities.</span></span>

### <a name="format-invoice-proposals"></a><span data-ttu-id="7f439-179">Formatowanie propozycji faktur</span><span class="sxs-lookup"><span data-stu-id="7f439-179">Format invoice proposals</span></span>

<span data-ttu-id="7f439-180">Strona **Formatowanie ofert faktur** umożliwia wyświetlanie niestandardowych transakcji grupowania na fakturze projektu klienta.</span><span class="sxs-lookup"><span data-stu-id="7f439-180">The **Format invoice proposals** page allows custom grouping transactions to display in the customer project invoice.</span></span>

1. <span data-ttu-id="7f439-181">Na stronie **Propozycje faktury projektu** wybierz opcję **Drukuj** > **Formatowanie propozycji faktur**.</span><span class="sxs-lookup"><span data-stu-id="7f439-181">On the **Project invoice proposal** page, select **Print** > **Format invoice proposal**.</span></span>
2. <span data-ttu-id="7f439-182">Wybierz opcję **Nowy**, aby utworzyć nowe grupowanie dla wydruku faktury Projektu.</span><span class="sxs-lookup"><span data-stu-id="7f439-182">Select **New** to create a new grouping for the Project invoice printout.</span></span>
3. <span data-ttu-id="7f439-183">W polu **Szczegóły/Podsumowanie** wybierz opcje dotyczące tego grupowania:</span><span class="sxs-lookup"><span data-stu-id="7f439-183">In the **Detail/Summary** field, select options for this grouping:</span></span>

    - <span data-ttu-id="7f439-184">Wybierz opcję **Szczegóły**, aby wydrukować szczegóły transakcji na fakturze klienta.</span><span class="sxs-lookup"><span data-stu-id="7f439-184">Select **Detail** to print the transaction details of the customer invoice.</span></span>
    - <span data-ttu-id="7f439-185">Wybierz opcję **Podsumowanie**, aby wydrukować podsumowanie transakcji na fakturze klienta.</span><span class="sxs-lookup"><span data-stu-id="7f439-185">Select **Summary** to print the transaction summary of the customer invoice.</span></span>

> [!NOTE]
> <span data-ttu-id="7f439-186">Wybór w polu **Szczegóły/Podsumowanie** na stronie **Formatowanie propozycji faktury** zastępuje opcję wybraną w polu **IFormat faktury** na stronie **Propozycje faktur**, aby wydrukować szczegółową fakturę lub fakturę podsumowania.</span><span class="sxs-lookup"><span data-stu-id="7f439-186">The selection in the **Detail/Summary** field on the **Format invoice proposal** page overrides the option selected in the **Invoice format** field on the **Invoice proposals** page to print a detailed invoice or a summarized invoice.</span></span>

- <span data-ttu-id="7f439-187">Wybierz wiersze transakcji, które chcesz uwzględnić w tej sekcji na karcie **Dostępne transakcje** i wybierz opcję **Uwzględnij transakcje**, aby przenieść je na kartę **Wybrane transakcje**.</span><span class="sxs-lookup"><span data-stu-id="7f439-187">Select the transaction lines to include in this section on the **Available transactions** tab and select **Include transactions** to move them to the **Selected transactions** tab.</span></span>
- <span data-ttu-id="7f439-188">Wybierz opcję **Przenieś w górę** i **Przenieś w dół**, aby zmienić kolejność sekcji.</span><span class="sxs-lookup"><span data-stu-id="7f439-188">Select **Move up** and **Move down** to change the order of the sections.</span></span>
- <span data-ttu-id="7f439-189">Wybierz **Podgląd wydruku**, aby wyświetlić podgląd sformatowanych faktur.</span><span class="sxs-lookup"><span data-stu-id="7f439-189">Select **Print preview** to preview formatted invoice.</span></span>

### <a name="print-management"></a><span data-ttu-id="7f439-190">Zarządzanie drukowaniem</span><span class="sxs-lookup"><span data-stu-id="7f439-190">Print management</span></span>

<span data-ttu-id="7f439-191">Zarządzanie drukowaniem wykorzystuje różne pliki raportów do drukowania, określania miejsc docelowych i dostosowywania tekstu stopki faktury.</span><span class="sxs-lookup"><span data-stu-id="7f439-191">Print management uses different report files to print, specify destinations, and customize footer text for the invoice.</span></span> <span data-ttu-id="7f439-192">Zarządzanie drukowaniem można skonfigurować na poziomie modułu, jednak ustawienia te można zastąpić dla konkretnego klienta, umowy lub propozycji faktury.</span><span class="sxs-lookup"><span data-stu-id="7f439-192">Print management can be set up at the module level, however these settings can be overridden for a specific customer, contract, or invoice proposal.</span></span> <span data-ttu-id="7f439-193">Aby uzyskać dostęp do tej funkcji na stronie **Propozycji fakturowania projektu**, wybierz **Drukuj** > **Zarządzanie drukowaniem**.</span><span class="sxs-lookup"><span data-stu-id="7f439-193">To access this function on the **Project invoice proposal** page, select **Print** > **Print management**.</span></span>

<span data-ttu-id="7f439-194">Konfiguracja zarządzania drukowaniem jest wyświetlana jako widok drzewa, w którym na każdym poziomie węzła są wyświetlane dokumenty dostępne do dostosowania.</span><span class="sxs-lookup"><span data-stu-id="7f439-194">Print management setup is displayed as a tree view, where each node level displays the available documents to adjust.</span></span> <span data-ttu-id="7f439-195">Możesz przypisać niestandardowe wydruki na poziomie modułu, klienta, umowy lub dokumentu propozycji faktury.</span><span class="sxs-lookup"><span data-stu-id="7f439-195">You can assign custom printouts at the module, customer, contract, or invoice proposal document level.</span></span> <span data-ttu-id="7f439-196">Aby zmodyfikować wydruk oryginalnego dokumentu, rozwiń żądany węzeł i wybierz **Oryginalny element**.</span><span class="sxs-lookup"><span data-stu-id="7f439-196">To modify the original document printout, expand the desired node and select **Original item**.</span></span> <span data-ttu-id="7f439-197">W polu **Format raportu** wybierz format raportu, który ma być używany do drukowania.</span><span class="sxs-lookup"><span data-stu-id="7f439-197">In the **Report format** field, select the report format to be used for printing.</span></span> <span data-ttu-id="7f439-198">Możesz użyć niestandardowych formatów raportów, używając [struktury zarządzania dokumentami biznesowymi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span><span class="sxs-lookup"><span data-stu-id="7f439-198">You can use custom report formats by using [Business Document Management framework](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span></span>

## <a name="post-invoice-proposals"></a><span data-ttu-id="7f439-199">Księgowanie propozycji faktur</span><span class="sxs-lookup"><span data-stu-id="7f439-199">Post invoice proposals</span></span>

<span data-ttu-id="7f439-200">Po przejrzeniu i edycji faktury, a wiersze propozycji faktury są zadowalające, sprawdź sumy faktur i podatek.</span><span class="sxs-lookup"><span data-stu-id="7f439-200">After the invoice has been reviewed and edited, and the invoice proposal lines are satisfactory, check the invoice totals and sales tax.</span></span> <span data-ttu-id="7f439-201">W grupie **Szczegóły** wybierz opcję **Sumy**, a następnie wybierz opcję **Zaksięguj** w celu zafakturowania faktury.</span><span class="sxs-lookup"><span data-stu-id="7f439-201">In the **Details** group, select **Totals** and then select **Post** to post the invoice.</span></span>

<span data-ttu-id="7f439-202">Aby wyświetlić fakturę przed opublikowaniem, wyczyść pole wyboru **Księgowanie**.</span><span class="sxs-lookup"><span data-stu-id="7f439-202">To view the invoice before posting, clear the **Posting** check box.</span></span> <span data-ttu-id="7f439-203">**Pro forma** zostanie wydrukowane na fakturze, aby zaznaczyć, że jest to faktura przykładowa.</span><span class="sxs-lookup"><span data-stu-id="7f439-203">**Pro forma** will be printed on the invoice to signify it is a sample invoice.</span></span> <span data-ttu-id="7f439-204">Aby wydrukować fakturę, zaznacz pole wyboru **Wydrukuj fakturę**.</span><span class="sxs-lookup"><span data-stu-id="7f439-204">To print the invoice, select the **Print invoice** check box.</span></span>

<span data-ttu-id="7f439-205">Oprócz strony **Propozycja faktury** można także wystawić propozycję faktury, uruchamiając zadanie okresowe **Księgowanie propozycji faktur**.</span><span class="sxs-lookup"><span data-stu-id="7f439-205">In addition to the **Invoice proposal** page, invoice proposals can also be posted by running the periodic job, **Post invoice proposals**.</span></span> <span data-ttu-id="7f439-206">Aby znaleźć to zadanie, przejdź do **Zarządzanie projektami i księgowanie** > **Okresowe** > **Faktury projektów** > **Zaksięguj propozycje faktur**.</span><span class="sxs-lookup"><span data-stu-id="7f439-206">To find this job, go to **Project management and accounting** > **Periodic** > **Project invoices** > **Post invoice proposals**.</span></span>

<span data-ttu-id="7f439-207">Ta strona zawiera wszystkie propozycje faktur, które są gotowe do zaksięgowania.</span><span class="sxs-lookup"><span data-stu-id="7f439-207">This page shows all the invoice proposals that are ready for posting.</span></span> <span data-ttu-id="7f439-208">Ofertę na fakturę można zaplanować, wybierając opcję **Partia**.</span><span class="sxs-lookup"><span data-stu-id="7f439-208">You can schedule posting invoice proposals by selecting **Batch**.</span></span> <span data-ttu-id="7f439-209">Ustaw parametr **Przetwarzanie wsadowe** na wartość **Tak** i ustaw cykl przetwarzania wsadowego, wybierając opcję **Cykl**.</span><span class="sxs-lookup"><span data-stu-id="7f439-209">Set the **Batch processing parameter** to **Yes** and set the recurrence of batch processing by selecting **Recurrence**.</span></span>