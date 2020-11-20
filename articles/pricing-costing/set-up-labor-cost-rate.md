---
title: Konfigurowanie stawek kosztów wykonanej pracy
description: W tym temacie zamieszczono informacje dotyczące sposobu konfigurowania kosztu wykonanej pracy w Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d17f266b6e34fc2a2743fe19fd18b15fb992ceef
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081909"
---
# <a name="set-up-labor-cost-rates"></a><span data-ttu-id="91908-103">Konfigurowanie stawek kosztów wykonanej pracy</span><span class="sxs-lookup"><span data-stu-id="91908-103">Set up labor cost rates</span></span>

<span data-ttu-id="91908-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="91908-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="91908-105">Każdy cennik ma zestaw stawek pracy (ceny ról), który jest wyrównany do treści i daty obowiązywania danego cennika.</span><span class="sxs-lookup"><span data-stu-id="91908-105">Each price list has a set of labor rates (role prices) that align with the content and date effectivity of the price list.</span></span>

1. <span data-ttu-id="91908-106">Utwórz cennik i na karcie **Ceny ról** , w podsiatce wybierz pozycję **+ Nowa cena roli**.</span><span class="sxs-lookup"><span data-stu-id="91908-106">Create a price list and on the **Role Price** tab, in the sub-grid, select **New Role**.</span></span>
2. <span data-ttu-id="91908-107">Na stronie **Szybkie tworzenie** wybierz rolę i jednostkę organizacyjną.</span><span class="sxs-lookup"><span data-stu-id="91908-107">On the **Quick Create** page, select the role and organization unit.</span></span>
3. <span data-ttu-id="91908-108">Wprowadź inne informacje w wymaganych polach.</span><span class="sxs-lookup"><span data-stu-id="91908-108">Enter any other required field information.</span></span>

<span data-ttu-id="91908-109">Poniższa tabela zawiera pola, które są istotne podczas tworzenia stawek pracy w cenniku kosztów.</span><span class="sxs-lookup"><span data-stu-id="91908-109">The following table includes some of the fields that are important when creating labor rates on a cost price list.</span></span>

| <span data-ttu-id="91908-110">Pole</span><span class="sxs-lookup"><span data-stu-id="91908-110">Field</span></span> | <span data-ttu-id="91908-111">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="91908-111">Location</span></span> | <span data-ttu-id="91908-112">Stopień zgodności, cel i wskazówki</span><span class="sxs-lookup"><span data-stu-id="91908-112">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="91908-113">Wpływ zmian w dalszych etapach</span><span class="sxs-lookup"><span data-stu-id="91908-113">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="91908-114">Rola</span><span class="sxs-lookup"><span data-stu-id="91908-114">Role</span></span> | <span data-ttu-id="91908-115">Karta **Ogólne** i strony **Szybkie tworzenie**</span><span class="sxs-lookup"><span data-stu-id="91908-115">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="91908-116">Wybierz rolę, której dotyczy stawka kosztu.</span><span class="sxs-lookup"><span data-stu-id="91908-116">Select the role that the cost rate applies to.</span></span> | <span data-ttu-id="91908-117">Rola na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki kosztu za rolę.</span><span class="sxs-lookup"><span data-stu-id="91908-117">The role on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="91908-118">Firma zasobów</span><span class="sxs-lookup"><span data-stu-id="91908-118">Resourcing Company</span></span> | <span data-ttu-id="91908-119">Karta **Ogólne** i strony **Szybkie tworzenie**</span><span class="sxs-lookup"><span data-stu-id="91908-119">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="91908-120">Wybierz firmę lub podmiot prawny, do którego rola jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="91908-120">Select the legal entity that the role is assigned to.</span></span> <span data-ttu-id="91908-121">Na przykład deweloper z firmy Fabrikam India lub deweloper z firmy Fabrikam USA.</span><span class="sxs-lookup"><span data-stu-id="91908-121">For example, a developer from Fabrikam India or a developer from Fabrikam USA.</span></span> | <span data-ttu-id="91908-122">Firma zasobów na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki kosztu za rolę.</span><span class="sxs-lookup"><span data-stu-id="91908-122">The resourcing company on the incoming estimate or actual will be matched against this line to default the cost rate of the role.</span></span> |
| <span data-ttu-id="91908-123">Jednostka zasobów</span><span class="sxs-lookup"><span data-stu-id="91908-123">Resourcing Unit</span></span> | <span data-ttu-id="91908-124">Karta **Ogólne** i strony **Szybkie tworzenie**</span><span class="sxs-lookup"><span data-stu-id="91908-124">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="91908-125">Wybierz jednostkę organizacyjną lub wydział firmy, gdzie ta rola będzie wykorzystana.</span><span class="sxs-lookup"><span data-stu-id="91908-125">Select the organizational unit or division of the company from where this role will be used.</span></span> <span data-ttu-id="91908-126">Na przykład deweloper z działu robotyki w Fabrikam India lub deweloper z działu oprogramowania w Fabrikam USA.</span><span class="sxs-lookup"><span data-stu-id="91908-126">For example, a developer from the Robotics division of Fabrikam India or a developer from the Software division of Fabrikam USA.</span></span> | <span data-ttu-id="91908-127">Jednostka zasobów na oszacowaniu przychodzącym lub wartości rzeczywistej, dopasowana do tego wiersza domyślnej stawki kosztu za rolę.</span><span class="sxs-lookup"><span data-stu-id="91908-127">The resourcing unit on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="91908-128">Cena</span><span class="sxs-lookup"><span data-stu-id="91908-128">Price</span></span> | <span data-ttu-id="91908-129">Karta **Ogólne** i strony **Szybkie tworzenie**</span><span class="sxs-lookup"><span data-stu-id="91908-129">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="91908-130">Skonfiguruj stawkę kosztu dla połączenia jednostki zasobów i firmy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91908-130">Set up the cost rate for the role, resourcing company, and resourcing unit combination.</span></span> <span data-ttu-id="91908-131">Na przykład deweloper z firmy Fabrikam India kosztuje 1000 INR lub deweloper z firmy Fabrikam USA kosztuje 150 USD.</span><span class="sxs-lookup"><span data-stu-id="91908-131">For example, a developer from Fabrikam India costs 1000 INR or a developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="91908-132">Cena jest stawką kosztową domyślną dla każdego kosztu jednostkowego w szacowaniu przychodzącym lub wartości rzeczywistej dla klasy transakcji **Czas**.</span><span class="sxs-lookup"><span data-stu-id="91908-132">The price is the cost rate that defaults on the per unit cost of the incoming estimate or actual line for the **Time** transaction class.</span></span> |
| <span data-ttu-id="91908-133">Waluta</span><span class="sxs-lookup"><span data-stu-id="91908-133">Currency</span></span> | <span data-ttu-id="91908-134">Karta **Ogólne** i strony **Szybkie tworzenie**</span><span class="sxs-lookup"><span data-stu-id="91908-134">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="91908-135">Domyślnie wartość waluty pochodzi z waluty w nagłówku cennika kosztów, ale ta wartość może być nadpisana.</span><span class="sxs-lookup"><span data-stu-id="91908-135">By default, the currency value comes from the currency on the header of the cost price list but can be overridden.</span></span> <span data-ttu-id="91908-136">Na przykład deweloper z firmy Fabrikam India kosztuje 1000 INR.</span><span class="sxs-lookup"><span data-stu-id="91908-136">For example, a developer from Fabrikam India costs 1000 INR.</span></span> <span data-ttu-id="91908-137">Deweloper z firmy Fabrikam USA kosztuje 150 USD.</span><span class="sxs-lookup"><span data-stu-id="91908-137">A developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="91908-138">Domyślna wartość waluty każdego kosztu jednostkowego w przychodzącej wartości rzeczywistej dla klasy transakcji **Czas**.</span><span class="sxs-lookup"><span data-stu-id="91908-138">This currency defaults on the per unit cost of the incoming actual cost line for the **Time** transaction class.</span></span> <span data-ttu-id="91908-139">W przypadku oszacowania projektu wartość waluty jest konwertowana na walutę projektu i wyświetlana w widoku okresowym oszacowania.</span><span class="sxs-lookup"><span data-stu-id="91908-139">On a project estimate, the currency value is converted to the project currency and shown on the Time-phased view of the estimate.</span></span> |
| <span data-ttu-id="91908-140">Harmonogram jednostek</span><span class="sxs-lookup"><span data-stu-id="91908-140">Unit Schedule</span></span> | <span data-ttu-id="91908-141">Karta **Ogólne** i strony **Szybkie tworzenie**</span><span class="sxs-lookup"><span data-stu-id="91908-141">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="91908-142">Domyślna wartość tego harmonogramu określa czas i nie można jej zmienić, ponieważ jest ona używana do wyrażania stawek na jednostkę czasu.</span><span class="sxs-lookup"><span data-stu-id="91908-142">The unit schedule defaults to Time and can't be changed on the Role price entity because it is used express rates by units of time.</span></span> | <span data-ttu-id="91908-143">Nie ma to wpływu na podrzędne procesy.</span><span class="sxs-lookup"><span data-stu-id="91908-143">There is no downstream impact.</span></span> |
| <span data-ttu-id="91908-144">Jednostka</span><span class="sxs-lookup"><span data-stu-id="91908-144">Unit</span></span> | <span data-ttu-id="91908-145">Karta **Ogólne** i strony **Szybkie tworzenie**</span><span class="sxs-lookup"><span data-stu-id="91908-145">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="91908-146">Domyślnie wartość jednostki pochodzi z pola **Jednostka czasu** z nagłówka cennika kosztów.</span><span class="sxs-lookup"><span data-stu-id="91908-146">By default, the value comes from the **Time Unit** field on the header of the cost price list.</span></span> <span data-ttu-id="91908-147">Ta wartość może być zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="91908-147">The value can be overridden.</span></span> <span data-ttu-id="91908-148">Na przykład deweloper z firmy Fabrikam India kosztuje 1000 INR na **dzień w Indiach**.</span><span class="sxs-lookup"><span data-stu-id="91908-148">For example, a developer from Fabrikam India costs 1000 INR per **India Day**.</span></span> <span data-ttu-id="91908-149">Deweloper z firmy Fabrikam USA kosztuje 150 USD za **Dzień w USA**.</span><span class="sxs-lookup"><span data-stu-id="91908-149">A developer from Fabrikam USA costs 150 USD per **US Day**.</span></span> | <span data-ttu-id="91908-150">System używa żywany jest jednostek i dokonywana jest konwersja w jednostkach podstawowych w celu obliczenia domyślnej ceny jednostkowej dla przychodzącego oszacowania lub wiersza rzeczywistego.</span><span class="sxs-lookup"><span data-stu-id="91908-150">The system uses the system of units and conversion in base units to compute a per unit cost to calculate the default price per unit on an incoming estimate or actual line.</span></span> <span data-ttu-id="91908-151">Na przykład wartość szacunkowa wynosi 10 jednostek **Dni w Indiach** dla dewelopera z Indii, a jednostka **Dni w Indiach** jest definiowana jako 10 godzin.</span><span class="sxs-lookup"><span data-stu-id="91908-151">For example, an estimate is for 10 **India Days** worth of work for a developer from India, and the unit, **India Day** is defined as 10 hours.</span></span> <span data-ttu-id="91908-152">Przy ustalaniu kosztów w wierszu szacowania aplikacja oblicza koszt jednostkowy w szacowaniu jako: 1000 INR/10 godzin = 100 INR na godzinę, która to wartość jest konwertowana na USD i wyświetlana jako koszt jednostkowy na stronie **Oszacowania projektu**.</span><span class="sxs-lookup"><span data-stu-id="91908-152">When costing that estimate line, the application calculates the unit cost on the estimate as: 1000 INR/ 10 hours = 100 INR per hour which is converted into USD and shown as the unit cost on the **Project Estimates** page.</span></span> |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a><span data-ttu-id="91908-153">Przenieś ceny i koszty zasobów poza dział lub podmiot prawny</span><span class="sxs-lookup"><span data-stu-id="91908-153">Transfer pricing and costs for resources outside of your division or legal entity</span></span>

<span data-ttu-id="91908-154">Przedsiębiorstwa oparte na projektach często używają pracowników z różnych działów firmy lub różnych podmiotów prawnych w pracy nad projektami.</span><span class="sxs-lookup"><span data-stu-id="91908-154">In project-based companies, it's common to use employees from different legal entities or divisions on projects.</span></span> <span data-ttu-id="91908-155">Projekty mogą być wykonywane w ramach określonego podmiotu prawnego, podczas gdy pracownicy lub konsultanci pracujący nad projektem mogą pochodzić z tego samego lub innego podmiotu bądź działu. Może też istnieć połączenie tych możliwości.</span><span class="sxs-lookup"><span data-stu-id="91908-155">A project can be executed by one legal entity, but the employees or consultants that work on the project could come from the same legal entity or from a different one, or there may be a combination of both.</span></span> <span data-ttu-id="91908-156">W Dynamics 365 Project Operations podmiot prawny, który jest właścicielem usługi dostarczania projektu, jest nazywany **Firmą będącą właścicielem** , natomiast dział, któremu należy dostarczyć usługi to **Jednostka zamawiająca**.</span><span class="sxs-lookup"><span data-stu-id="91908-156">In Dynamics 365 Project Operations, the legal entity that owns the delivery of the project is the **Owning Company** and the division that owns the delivery is the **Contracting Unit**.</span></span> <span data-ttu-id="91908-157">Każdy inny podmiot prawny, który zawiera zasoby, jest zwany **Firmami zasobów** , a wydziały, które zawierają zasoby, to **Jednostki zasobów**.</span><span class="sxs-lookup"><span data-stu-id="91908-157">Other legal entities that provide resources are the **Resourcing companies** and divisions that provide resources are the **Resourcing Units**.</span></span> <span data-ttu-id="91908-158">W większości krajów firma jest zobowiązana zapewnić, że osoba lub oddział prawny, który chce skorzystać z tej osoby, obciążą firmę będącą właścicielem oraz jednostkę zamawiającą do korzystania z zasobów.</span><span class="sxs-lookup"><span data-stu-id="91908-158">In most countries, companies are required to ensure that the resourcing legal entity or division, charge the owning company and the contracting unit for the use of resources.</span></span>

<span data-ttu-id="91908-159">Na przykład firma Fabrikam Corporation musi zagwarantować, że firma Fabrikam India-Robotics wynegocjowała stawkę kosztów z Fabrikam US-Robotics lub Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="91908-159">For example, the Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate card with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="91908-160">Deweloper z Fabrikam India pobiera 100 USD, gdy jest wypożyczony do Fabrikam US-Robotics, ale 150 USD gdy jest wypożyczony do Fabrikam U-Robotics.</span><span class="sxs-lookup"><span data-stu-id="91908-160">A developer from Fabrikam India-Robotic charges $100 when lent to Fabrikam US-Robotics and $150 when lent to Fabrikam U-Robotics.</span></span>

### <a name="set-up-costs-for-outside-resources"></a><span data-ttu-id="91908-161">Konfigurowanie kosztów zasobów zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="91908-161">Set up costs for outside resources</span></span>

1. <span data-ttu-id="91908-162">Utwórz cennik o nazwie, *stawki kosztów US Fabrikam-Robotics* , a następnie ustaw obowiązujące daty.</span><span class="sxs-lookup"><span data-stu-id="91908-162">Create a cost price list called, *Fabrikam US-Robotics cost rates* and set a date effective range.</span></span>
2. <span data-ttu-id="91908-163">Korzystając z informacji zawartych w tabeli można ustawić stawki na liście kosztów.</span><span class="sxs-lookup"><span data-stu-id="91908-163">In the cost price list, set up rates using information from the following table.</span></span> 

| <span data-ttu-id="91908-164">Rola</span><span class="sxs-lookup"><span data-stu-id="91908-164">Role</span></span> | <span data-ttu-id="91908-165">Firma zasobów</span><span class="sxs-lookup"><span data-stu-id="91908-165">Resourcing Company</span></span> | <span data-ttu-id="91908-166">Jednostka zasobów</span><span class="sxs-lookup"><span data-stu-id="91908-166">Resourcing Unit</span></span> | <span data-ttu-id="91908-167">Stawka kosztów</span><span class="sxs-lookup"><span data-stu-id="91908-167">Cost rate</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="91908-168">Developer</span><span class="sxs-lookup"><span data-stu-id="91908-168">Developer</span></span> | <span data-ttu-id="91908-169">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="91908-169">Fabrikam India</span></span> | <span data-ttu-id="91908-170">Fabrikam India-Robotics</span><span class="sxs-lookup"><span data-stu-id="91908-170">Fabrikam India-Robotics</span></span> | <span data-ttu-id="91908-171">100 USD</span><span class="sxs-lookup"><span data-stu-id="91908-171">$100</span></span> |
| <span data-ttu-id="91908-172">Developer</span><span class="sxs-lookup"><span data-stu-id="91908-172">Developer</span></span> | <span data-ttu-id="91908-173">Fabrikam Philippines</span><span class="sxs-lookup"><span data-stu-id="91908-173">Fabrikam Philippines</span></span> | <span data-ttu-id="91908-174">Fabrikam Philippines-Robotics</span><span class="sxs-lookup"><span data-stu-id="91908-174">Fabrikam Philippines-Robotics</span></span> | <span data-ttu-id="91908-175">90 USD</span><span class="sxs-lookup"><span data-stu-id="91908-175">$90</span></span> |
| <span data-ttu-id="91908-176">Developer</span><span class="sxs-lookup"><span data-stu-id="91908-176">Developer</span></span> | <span data-ttu-id="91908-177">Fabrikam US</span><span class="sxs-lookup"><span data-stu-id="91908-177">Fabrikam US</span></span> | <span data-ttu-id="91908-178">Fabrikam US-Robotics</span><span class="sxs-lookup"><span data-stu-id="91908-178">Fabrikam US-Robotics</span></span> | <span data-ttu-id="91908-179">150 USD</span><span class="sxs-lookup"><span data-stu-id="91908-179">$150</span></span> |

3. <span data-ttu-id="91908-180">Dołącz tą listę kosztów do jednostki organizacyjnej Fabrikam US-Robotics.</span><span class="sxs-lookup"><span data-stu-id="91908-180">Attach this cost price list to the Fabrikam US-Robotics organization unit.</span></span>

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a><span data-ttu-id="91908-181">Konfigurowanie kalkulacji cen z przeniesienia dla zasobu w odpowiedniej walucie</span><span class="sxs-lookup"><span data-stu-id="91908-181">Set up transfer pricing for a resource in the appropriate currency</span></span> 

<span data-ttu-id="91908-182">W przypadku Project Operations cena zasobu może zostać ustawiona w dowolnej walucie.</span><span class="sxs-lookup"><span data-stu-id="91908-182">In Project Operations, resource pricing can be set up in any currency.</span></span> <span data-ttu-id="91908-183">Domyślnie waluta zawiera wartość, która znajduje się w nagłówku cennika, ale można ją zmienić.</span><span class="sxs-lookup"><span data-stu-id="91908-183">The currency defaults to what is on the price list header, but can be changed.</span></span>

<span data-ttu-id="91908-184">Korzystając z przykładu dotyczącego konfiguracji ceny przeniesienia, można zmienić informacje na następujące:</span><span class="sxs-lookup"><span data-stu-id="91908-184">Using the example for transfer price set up, the information could be changed to:</span></span>

<span data-ttu-id="91908-185">Firma Fabrikam Corporation musi zagwarantować, że firma Fabrikam India-Robotics wynegocjowała stawkę kosztów z Fabrikam US-Robotics lub Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="91908-185">Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="91908-186">Deweloper z Fabrikam India kosztuje 5000 INR, gdy jest wypożyczony do Fabrikam US-Robotics, ale 5500 INR gdy jest wypożyczony do Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="91908-186">A developer from Fabrikam India-Robotics costs 5000 INR when lent to Fabrikam US-Robotics and 5500 INR when lent to Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="91908-187">W liście cenników dla Fabrikam US-Robotics, stawki kosztów mogą być wyrażone w następujących postaciach:</span><span class="sxs-lookup"><span data-stu-id="91908-187">In the cost price list for Fabrikam US-Robotics, cost rates can be expressed as:</span></span>

| <span data-ttu-id="91908-188">Rola</span><span class="sxs-lookup"><span data-stu-id="91908-188">Role</span></span> | <span data-ttu-id="91908-189">Firma zasobów</span><span class="sxs-lookup"><span data-stu-id="91908-189">Resourcing Company</span></span> | <span data-ttu-id="91908-190">Koszt</span><span class="sxs-lookup"><span data-stu-id="91908-190">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="91908-191">Developer</span><span class="sxs-lookup"><span data-stu-id="91908-191">Developer</span></span> | <span data-ttu-id="91908-192">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="91908-192">Fabrikam India</span></span> | <span data-ttu-id="91908-193">5000 INR</span><span class="sxs-lookup"><span data-stu-id="91908-193">5000 INR</span></span> |
| <span data-ttu-id="91908-194">Developer</span><span class="sxs-lookup"><span data-stu-id="91908-194">Developer</span></span> | <span data-ttu-id="91908-195">Fabrikam US</span><span class="sxs-lookup"><span data-stu-id="91908-195">Fabrikam US</span></span> | <span data-ttu-id="91908-196">115 USD</span><span class="sxs-lookup"><span data-stu-id="91908-196">115 USD</span></span> |

<span data-ttu-id="91908-197">W liście cenników dla Fabrikam UK-Robotics, stawki kosztów mogą być wyrażone w następujących postaciach poniżej:</span><span class="sxs-lookup"><span data-stu-id="91908-197">In the cost price list for Fabrikam UK-Robotics, cost rates can be expressed below:</span></span>

| <span data-ttu-id="91908-198">Rola</span><span class="sxs-lookup"><span data-stu-id="91908-198">Role</span></span> | <span data-ttu-id="91908-199">Firma zasobów</span><span class="sxs-lookup"><span data-stu-id="91908-199">Resourcing company</span></span> | <span data-ttu-id="91908-200">Koszt</span><span class="sxs-lookup"><span data-stu-id="91908-200">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="91908-201">Developer</span><span class="sxs-lookup"><span data-stu-id="91908-201">Developer</span></span> | <span data-ttu-id="91908-202">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="91908-202">Fabrikam India</span></span> | <span data-ttu-id="91908-203">5500 INR</span><span class="sxs-lookup"><span data-stu-id="91908-203">5500 INR</span></span> |
| <span data-ttu-id="91908-204">Developer</span><span class="sxs-lookup"><span data-stu-id="91908-204">Developer</span></span> | <span data-ttu-id="91908-205">Fabrikam UK</span><span class="sxs-lookup"><span data-stu-id="91908-205">Fabrikam UK</span></span> | <span data-ttu-id="91908-206">115 GBP</span><span class="sxs-lookup"><span data-stu-id="91908-206">115 GBP</span></span> |

<span data-ttu-id="91908-207">Lista kosztów własnych może udostępniać stawki pracy w wielu walutach.</span><span class="sxs-lookup"><span data-stu-id="91908-207">The cost price list can provide labor rates in multiple currencies.</span></span> <span data-ttu-id="91908-208">Podczas generowania oszacowania kosztów projektu są one konwertowane na walutę projektu i wyświetlane dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="91908-208">When generating a cost estimate on the project, Project Operations will convert these cost rates into the project currency and display it to the user.</span></span> <span data-ttu-id="91908-209">Po zatwierdzeniu wpisu czasu i utworzeniu kosztu wartości rzeczywistej koszt rzeczywisty jest wyceniany w walucie odpowiadającej tej pozycji z wiersza z ceną z listy cenników.</span><span class="sxs-lookup"><span data-stu-id="91908-209">When a time entry is approved and a cost actual is created, the cost actual is priced in the currency of that matching role price line on the cost price list.</span></span> <span data-ttu-id="91908-210">Koszt rzeczywisty czasu w pojedynczym projekcie może być rejestrowany w wielu walutach.</span><span class="sxs-lookup"><span data-stu-id="91908-210">Cost actuals for time on a single project can be recorded in multiple currencies.</span></span> <span data-ttu-id="91908-211">Jednak podczas zestawiania lub podsumowywania rzeczywistych kosztów wykonanej pracy na poziomie projektu Project Operations wykonają konwersję wszystkich kosztów pracy na walutę projektu, która może być wyświetlana przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="91908-211">However, when rolling up or summarizing the actual labor costs at the project level, Project Operations will convert all labor cost amounts into the project currency, which the user can view.</span></span>