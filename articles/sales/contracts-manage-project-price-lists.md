---
title: Zarządzanie cennikami projektu w kontraktach projektu
description: Ta temat zawiera informacje na temat zarządzania cennikami projektu przy kontraktach dotyczących projektów.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858576"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="1ea78-103">Zarządzanie cennikami projektu w kontraktach projektu</span><span class="sxs-lookup"><span data-stu-id="1ea78-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="1ea78-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="1ea78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1ea78-105">Kontrakty projektów w rozwiązaniu Dynamics 365 Project Operations są projektowane tak, aby obsługiwały w kontrakcie wiele efektywnych cenników sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="1ea78-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="1ea78-106">W operacjach projektu istnieje nowa encja skojarzona o nazwie **Cenniki projektu**.</span><span class="sxs-lookup"><span data-stu-id="1ea78-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="1ea78-107">Ta encja jest relacją typu jeden-do-wielu z kontraktem dotyczącym projektu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="1ea78-108">Cenniki projektu służą do wyceny transakcji dotyczących czasu, materiałów i wydatków w projekcie.</span><span class="sxs-lookup"><span data-stu-id="1ea78-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="1ea78-109">Gdy kontrakt ma co najmniej jeden cennik projektu, cenniki te służą do wyceny czasu, materiałów, szacunków kosztów i wartości rzeczywistych dotyczących projektów, które są skojarzone z kontraktem za pośrednictwem wiersza kontraktu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="1ea78-110">Jeśli w umowie dotyczącej projektu nie ma cenników projektu, zostanie wyświetlony komunikat ostrzegawczy, że nie ma cenników projektu, a Twoje szacunki, rzeczywiste prace projektowe, materiały i zarejestrowane wydatki nie zostaną wycenione.</span><span class="sxs-lookup"><span data-stu-id="1ea78-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="1ea78-111">Nie będzie ceny na wartości sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="1ea78-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="1ea78-112">Kojarzenie i odkojarzenie cennika projektu względem kontraktu dotyczącego projektu</span><span class="sxs-lookup"><span data-stu-id="1ea78-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="1ea78-113">Utwórz lub skojarz konkretny cennik w celu oszacowania pracy, materiałów i wydatków związanych z projektem</span><span class="sxs-lookup"><span data-stu-id="1ea78-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="1ea78-114">W kontrakcie projektu wybierz kartę **Cenniki projektów**.</span><span class="sxs-lookup"><span data-stu-id="1ea78-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="1ea78-115">W podsiatce wybierz pozycję **+ Dodaj nowy Cennik projektu**.</span><span class="sxs-lookup"><span data-stu-id="1ea78-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="1ea78-116">Na suwaku **Szybkie tworzenie** wybierz cennik.</span><span class="sxs-lookup"><span data-stu-id="1ea78-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="1ea78-117">Lista rozwijana zawiera listę wszystkich cenników, dla których ustawiono zestawienie **Sprzedaż**, w którym waluta na cenniku odpowiada walucie zawartej w kontrakcie.</span><span class="sxs-lookup"><span data-stu-id="1ea78-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="1ea78-118">Wprowadź opis skojarzenia z cennikiem projektu, wybierz pozycję **Zapisz**, a następnie zamknij suwak **Szybkie tworzenie**.</span><span class="sxs-lookup"><span data-stu-id="1ea78-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="1ea78-119">Utworzenie skojarzenia cennika projektu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="1ea78-120">Powtórz kroki 1-4, aby skojarzyć z kontraktem projektu więcej niż jeden cennik projektu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="1ea78-121">Utwórz wiele cenników projektów tylko wtedy, gdy masz różne daty obowiązywania w każdym z powiązanych cenników projektów.</span><span class="sxs-lookup"><span data-stu-id="1ea78-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="1ea78-122">Project Operations nie obsługują nakładania się obowiązywania dat cenników projektu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="1ea78-123">Jeśli istnieje wiele cenników projektu dotyczących transakcji z określonym terminem, cena w tej transakcji będzie domyślnie równa zero.</span><span class="sxs-lookup"><span data-stu-id="1ea78-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="1ea78-124">Usuń powiązanie cennika projektu</span><span class="sxs-lookup"><span data-stu-id="1ea78-124">Remove a project price list association</span></span>

- <span data-ttu-id="1ea78-125">Wybierz Cennik projektu i wybierz pozycję **Usuń cennik projektu kontraktu** w podsiatce.</span><span class="sxs-lookup"><span data-stu-id="1ea78-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="1ea78-126">Cennik jest usuwany z cenników projektu dotyczących danego kontraktu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="1ea78-127">Sam cennik nie zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="1ea78-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="1ea78-128">Usuwany jest tylko skojarzeny z kontraktem.</span><span class="sxs-lookup"><span data-stu-id="1ea78-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="1ea78-129">Konfigurowanie automatycznej konfiguracji domyślnej cenników projektu na kontrakcie</span><span class="sxs-lookup"><span data-stu-id="1ea78-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="1ea78-130">Cennik projektu można ustawić jako cennik domyślny dla projektu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="1ea78-131">Ta konfiguracja zapewnia, że wszystkie umowy w Twojej organizacji zawsze zaczynają się od standardowego cennika projektu dla tego okresu cenowego.</span><span class="sxs-lookup"><span data-stu-id="1ea78-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="1ea78-132">Konfigurowanie ustawień domyślnych organizacyjnych dla cenników projektu</span><span class="sxs-lookup"><span data-stu-id="1ea78-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="1ea78-133">Wybierz kolejno pozycje **Ustawienia** > **Ogólne** i **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="1ea78-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="1ea78-134">Na stronie lista **Aktywnych parametrów** wybierz rekord, kliknij go dwukrotnie, aby go otworzyć.</span><span class="sxs-lookup"><span data-stu-id="1ea78-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="1ea78-135">Kiedy klikasz dwukrotnie opcję, upewnij się, że nie klikasz wartości pola, która jest hiperłączem.</span><span class="sxs-lookup"><span data-stu-id="1ea78-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="1ea78-136">Na stronie **Aktywne parametry** wybierz kartę **Cennik**. W podsiatce jest widoczna lista domyślnych cenników.</span><span class="sxs-lookup"><span data-stu-id="1ea78-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="1ea78-137">Jest to lista kosztów standardowych i cenników sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="1ea78-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="1ea78-138">Dla każdej sprzedawanej waluty w programie jest dostępna lista cen **Sprzedaży** zawierająca wartość domyślną na wszystkich kontraktach tworzonych dla klientów, którzy są transakcją w tej walucie.</span><span class="sxs-lookup"><span data-stu-id="1ea78-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="1ea78-139">Konfigurowanie cennika konkretnego klienta</span><span class="sxs-lookup"><span data-stu-id="1ea78-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="1ea78-140">Po wynegocjowaniu głównej umowy cenowej z klientami można również skonfigurować cenniki projektów dla konkretnych klientów.</span><span class="sxs-lookup"><span data-stu-id="1ea78-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="1ea78-141">Wybierz kolejno pozycje **Sprzedaż** > **Klienci**.</span><span class="sxs-lookup"><span data-stu-id="1ea78-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="1ea78-142">Z listy aktywnych klientów wybierz klienta, dla którego jest Cennik specjalny.</span><span class="sxs-lookup"><span data-stu-id="1ea78-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="1ea78-143">Wybierz rekord klienta, który ma go otworzyć, a następnie wybierz kartę **Cenniki projektu**. W podsiatce jest wyświetlona lista cenników projektu specyficzna dla danego klienta.</span><span class="sxs-lookup"><span data-stu-id="1ea78-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="1ea78-144">W tym miejscu utwórz nowe skojarzenie cennika, aby dysponować cennikiem określonym dla tego klienta.</span><span class="sxs-lookup"><span data-stu-id="1ea78-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="1ea78-145">Niestandardowa kalkulacja cen w kontrakcie dotyczącym projektu</span><span class="sxs-lookup"><span data-stu-id="1ea78-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="1ea78-146">Po utworzeniu organizacji i domyślnych cenników projektu dla konkretnego klienta kontrakty projektów zostaną utworzone automatycznie za pomocą tych skojarzeń z cennikami projektu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="1ea78-147">Jednak cenniki projektu zawarte w kontrakcie projektu są zawsze kopiowane z datą i nazwą kontraktu dodaną do nich.</span><span class="sxs-lookup"><span data-stu-id="1ea78-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="1ea78-148">Menedżerowie kont i projektów mogą następnie rozpocząć edycję cen w tych kopiach.</span><span class="sxs-lookup"><span data-stu-id="1ea78-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="1ea78-149">Te zmienione ceny będą dotyczyć wyłącznie tego kontraktu dotyczącego projektu.</span><span class="sxs-lookup"><span data-stu-id="1ea78-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
