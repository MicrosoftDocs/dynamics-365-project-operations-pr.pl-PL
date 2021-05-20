---
title: Integracja danych instalacji i konfiguracji aplikacji Project Operations
description: Ten temat zawiera informacje dotyczące ustawienia i konfigurowania mapowania podwójnego zapisu w Project Operations.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939027"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a><span data-ttu-id="cc3f8-103">Integracja danych instalacji i konfiguracji aplikacji Project Operations</span><span class="sxs-lookup"><span data-stu-id="cc3f8-103">Project Operations setup and configuration data integration</span></span>

<span data-ttu-id="cc3f8-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="cc3f8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cc3f8-105">Ten temat zawiera informacje na temat integracji podwójnego zapisu w Project Operations dla encji konfiguracji i ustawień.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-105">This topic provides information about Project Operations dual-write integration for setup and configuration entities.</span></span>

## <a name="project-contracts-contract-lines-and-projects"></a><span data-ttu-id="cc3f8-106">Kontrakty projektu, wiersze kontraktu i projekty</span><span class="sxs-lookup"><span data-stu-id="cc3f8-106">Project contracts, contract lines, and projects</span></span>

<span data-ttu-id="cc3f8-107">Kontrakty projektów, wiersze kontraktu i projekty są tworzone w Dataverse i synchronizowane z aplikacjami Finance and Operations na potrzeby dodatkowego rozliczenia.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-107">Project contracts, contract lines, and projects are created in Dataverse and synchronized to Finance and Operations apps for additional accounting.</span></span> <span data-ttu-id="cc3f8-108">Rekordy w tych encjach można tworzyć i usuwać tylko w programie Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-108">The records in these entities can be created and deleted only in Dataverse.</span></span> <span data-ttu-id="cc3f8-109">Można jednak dodać do tych rekordów w aplikacjach Finance and Operations atrybuty księgowe, takie jak domyślne ustawienia grupy podatku sprzedaży oraz rozmiary finansowe.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-109">However, accounting attributes such as sales tax group defaults and financial dimensions can be added to these records in the Finance and Operations apps.</span></span>

  ![Pojęcia integracji kontraktu projektu](./media/1ProjectContract.jpg)

<span data-ttu-id="cc3f8-111">Potencjalni klienci w sprzedaży, szanse sprzedaży i oferty są śledzone w Dataverse i te dane nie są synchronizowane z aplikacjami Finance and Operations, ponieważ z tym działaniem nie jest skojarzona żadna księgowa wartość.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-111">Sales activity leads, opportunities, and quotes are tracked in Dataverse and don't synchronize to Finance and Operations apps because there is no downstream accounting associated with this activity.</span></span>

<span data-ttu-id="cc3f8-112">Funkcja kontraktu projektu w Dataverse umożliwia utworzenie rekordu kontraktu projektu w aplikacjach Finance and Operations przy użyciu mapowania tabeli **nagłówków kontraktu projektu (salesorders)**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-112">The project contract functionality in Dataverse creates a project contract record in Finance and Operations apps using the **Project contract headers (salesorders)** table map.</span></span> <span data-ttu-id="cc3f8-113">Zapisanie kontraktu projektu w Dataverse także rozpoczyna tworzenie rekordu encji klienta kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-113">Saving a project contract in Dataverse also starts the creation of a project contract customer entity record.</span></span> <span data-ttu-id="cc3f8-114">Ten rekord jest synchronizowany z aplikacjami Finance and Operations, używając mapowania tabeli **źródła finansowania w projekcie (msdyn\_projectcontractsspbillingrules)**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-114">This record is synchronized to Finance and Operations apps using the **Project funding source (msdyn\_projectcontractssplitbillingrules)** table map.</span></span> <span data-ttu-id="cc3f8-115">Na tym mapowaniu są również synchronizowane dodatki, aktualizacje i usunięcia klientów kontraktu projektu.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-115">This map also synchronizes project contract customer additions, updates, and deletions.</span></span> <span data-ttu-id="cc3f8-116">Podział wartości procentowych rozliczania między klientów kontraktów projektów jest opanowany tylko w Dataverse i nie jest synchronizowany z aplikacjami Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-116">Split billing percentages between project contract customers are mastered only in Dataverse and not synchronized to Finance and Operations apps.</span></span>

<span data-ttu-id="cc3f8-117">Po utworzeniu umowy projektowej w Dataverse, księgowy projektu może zaktualizować atrybuty księgowe dla tej umowy projektowej w aplikacjach Finance and Operations przechodząc do **zarządzanie projektem i księgowość** > **Kontrakty projektu** > **Ustawienie** > **Pokaż domyślne wartości księgowe**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-117">After a project contract is created in Dataverse, the project accountant can update the accounting attributes for this project contract in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**.</span></span> <span data-ttu-id="cc3f8-118">Księgowy może przejrzeć operacyjne atrybuty umowy projektowej, takie jak żądana data dostawy i kwota umowy, wybierając identyfikator umowy projektowej w aplikacji Finance and Operations, która otwiera powiązany rekord umowy projektowej w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-118">The accountant can review operational project contract attributes, such as requested delivery date and contract amount by selecting the project contract ID in Finance and Operations apps which opens the related project contract record in Dataverse.</span></span>

<span data-ttu-id="cc3f8-119">Encja projektu jest synchronizowana z aplikacjami Finance and Operations, używając mapowania tabeli **Projektów V2 (msdyn\_** projects).</span><span class="sxs-lookup"><span data-stu-id="cc3f8-119">The project entity is synchronized to Finance and Operations apps using the **Projects V2 (msdyn\_projects)** table map.</span></span> <span data-ttu-id="cc3f8-120">Konto klienta projektu może:</span><span class="sxs-lookup"><span data-stu-id="cc3f8-120">The project accountant can:</span></span>

  - <span data-ttu-id="cc3f8-121">Przejrzyj projekty w aplikacjach Finance and Operations, przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-121">Review projects in Finance and Operations apps by going to **Project management and accounting** > **All projects**.</span></span> 
  - <span data-ttu-id="cc3f8-122">Aktualizuj atrybuty księgowe projektu w aplikacjach Finance and Operations, przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Konfigurowanie** > **Pokaż domyślne ustawienia księgowe**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-122">Update accounting attributes for the project in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Set up** > **Show default accounting**.</span></span>  
  - <span data-ttu-id="cc3f8-123">Przejrzyj atrybuty operacyjne projektu, takie jak szacowane daty rozpoczęcia i zakończenia, wybierając identyfikator projektu w aplikacjach Finance and Operations, które otwierają rekord pokrewny projektu w chmurze w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-123">Review operational project attributes, such as estimated start and end dates, by selecting the project ID in Finance and Operations apps which opens the related project record in Dataverse.</span></span>

<span data-ttu-id="cc3f8-124">Projekt jest skojarzony z kontraktem projektu za pośrednictwem encji **Wiersz kontraktu projektu**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-124">A project is associated with a project contract through the **Project contract line** entity.</span></span>

<span data-ttu-id="cc3f8-125">Wiersze kontraktu projektu w Dataverse umożliwiają utworzenie zasady rozliczania w aplikacjach Finance and Operations przy użyciu mapowania tabeli **Wierszy kontraktu projektu (salesordersdetails)**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-125">Project contract lines in Dataverse creates a project contract billing rule in Finance and Operations apps using the **Project contract lines (salesorderdetails)** table map.</span></span> <span data-ttu-id="cc3f8-126">Metoda rozliczania definiuje typ reguły rozliczania kontraktu projektu w aplikacjach Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="cc3f8-126">The billing method defines the project contract billing rule type in Finance and Operations apps:</span></span>

  - <span data-ttu-id="cc3f8-127">Wiersze kontraktu projektu z metodą rozliczania czasu i materiałów tworzą regułę rozliczania typu czas i materiał.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-127">Project contract lines with a billing method of time and material create a billing rule of time and material type.</span></span>
  - <span data-ttu-id="cc3f8-128">Linie kontraktowe metody rozliczeń wg stałej ceny tworzą regułę rozliczeń wg etapów.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-128">Fixed price billing method contract lines create a milestone billing rule.</span></span>

<span data-ttu-id="cc3f8-129">Linie umów projektowych mogą być przeglądane przez księgowego projektu w aplikacji Finance and Operations poprzez przejście do **Zarządzanie projektem i księgowość** > **Kontrakty projektowe** > **Ustawianie** > **Pokaż domyślne księgowanie**, a następnie przegląd szczegółów na zakładce **Linie umów**. Na tej zakładce księgowy może również ustawić domyślne wymiary finansowe dla linii umów rozliczanych metodą stałej ceny.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-129">Project contract lines can be reviewed by the project accountant in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**, and reviewing the details on the **Contract lines** tab. The accountant can also set default financial dimensions for the fixed price billing method contract lines on this tab.</span></span>

## <a name="billing-milestones"></a><span data-ttu-id="cc3f8-130">Punkty kontrolne rozliczenia</span><span class="sxs-lookup"><span data-stu-id="cc3f8-130">Billing milestones</span></span>

<span data-ttu-id="cc3f8-131">Wiersze kontraktu projektu przy użyciu metody rozliczania o stałej cenie są zafakturowane za pośrednictwem punktów kontrolnych rozliczania.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-131">Project contract lines using the fixed price billing method are invoiced through billing milestones.</span></span> <span data-ttu-id="cc3f8-132">Punkty kontrolne rozliczania są synchronizowane z transakcjami konta projektu w aplikacjach Finance and Operations przy użyciu mapowania tabeli **punktów kontrolnych integracji Project Operations z linią kontraktów (msdyn\_contractlinescheduleofvalues)**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-132">Billing milestones are synchronized to project on-account transactions in Finance and Operations apps by using the **Project Operations integration contract line milestones (msdyn\_contractlinescheduleofvalues)** table map.</span></span>

  ![Integracja punktów kontrolnych rozliczenia](./media/2Milestones.jpg)

<span data-ttu-id="cc3f8-134">Księgowy może przeglądać transakcje konta i dostosowywać atrybuty księgowe tych transakcji, przechodząc do **Zarządzanie projektami i księgowość** > **Kontrakty projektów** > **Zarządzanie** > **Transakcje na rachunku** lub **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Zarządzanie** > **Transakcje na rachunku**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-134">The accountant can review on-account transactions and adjust the accounting attributes for those transactions by going to **Project management and accounting** > **Project contracts** > **Maintain** > **On-account transactions** or **Project management and accounting** > **All projects** > **Maintain** > **On-account transactions**.</span></span>

<span data-ttu-id="cc3f8-135">Podczas pierwszego tworzenia etapu rozliczeniowego dla danej linii kontraktowej projektu, system automatycznie tworzy projekt estymacji przychodów w stałej cenie dla projektu powiązanego z tą linią kontraktową.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-135">When you first create a billing milestone for a given project contract line, the system automatically creates a fixed price revenue estimate project for the project associated with this contract line.</span></span> <span data-ttu-id="cc3f8-136">Projekty szacowania przychodów o stałej cenie można przeglądać, przechodząc do **Zarządzania projektami i księgowości** > **Projekty dotyczące prognozy dochodów po stałej cenie**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-136">Fixed-price revenue estimate projects can be reviewed by going to **Project management and accounting** > **Fixed-price revenue estimate projects**.</span></span>

### <a name="project-tasks"></a><span data-ttu-id="cc3f8-137">Zadania projektu</span><span class="sxs-lookup"><span data-stu-id="cc3f8-137">Project tasks</span></span>

<span data-ttu-id="cc3f8-138">Zadania projektu są synchronizowane z aplikacjami Finance and Operations za pośrednictwem tabeli zadań projektu **(msdyn\_projecttasks)** wyłącznie dla celów referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-138">Project tasks are synchronized to Finance and Operations apps through the **Project tasks (msdyn\_projecttasks)** table map for reference purposes only.</span></span> <span data-ttu-id="cc3f8-139">Operacje tworzenia, aktualizowania i usuwania nie są obsługiwane za pośrednictwem aplikacji Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-139">Creating, updating, and deleting operations isn't supported through Finance and Operations apps.</span></span>

  ![Integracja zadań projektowych](./media/3Tasks.jpg)

## <a name="project-resources"></a><span data-ttu-id="cc3f8-141">Zasoby projektu</span><span class="sxs-lookup"><span data-stu-id="cc3f8-141">Project resources</span></span>

<span data-ttu-id="cc3f8-142">Encja **Role zasobów projektu** jest synchronizowana z aplikacjami Finance and Operations, używając **Role zasobów projektowych dla wszystkich firm (bookableresourcecategories)** tylko dla celów referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-142">The **Project resource roles** entity is synchronized to Finance and Operations apps using the **Project resource roles for all companies (bookableresourcecategories)** table map for reference purposes only.</span></span> <span data-ttu-id="cc3f8-143">Ponieważ role zasobów w Dataverse nie są specyficzne dla firmy, system automatycznie tworzy w aplikacjach Finance and Operations rekordy odpowiednich ról zasobów specyficznych dla firmy dla wszystkich podmiotów prawnych uwzględnianych w zakresie integracji podwójnego zapisu.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-143">Because resource roles in Dataverse are not company-specific, the system automatically creates respective company-specific resource roles records in Finance and Operations apps automatically for all legal entities included into dual-write integration scope.</span></span>

![Integracja ról zasobów](./media/5Resources.jpg)

<span data-ttu-id="cc3f8-145">Zasoby projektu w Project Operations są utrzymywane w Dataverse i nie są synchronizowane z aplikacjami Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-145">Project resources in Project Operations are maintained in Dataverse and aren't synchronized to Finance and Operations apps.</span></span>

### <a name="transaction-categories"></a><span data-ttu-id="cc3f8-146">Kategorie transakcji</span><span class="sxs-lookup"><span data-stu-id="cc3f8-146">Transaction categories</span></span>

<span data-ttu-id="cc3f8-147">Kategorie transakcji są zachowywane w Dataverse i synchronizowane z aplikacjami Finance and Operations przy użyciu kategorii transakcji projektu **(msdyn\_transactioncategories)**.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-147">Transaction categories are maintained in Dataverse and synchronized to Finance and Operations apps using the **Project transaction categories (msdyn\_transactioncategories)** table map.</span></span> <span data-ttu-id="cc3f8-148">Po zsynchronizowaniu rekordu kategorii transakcji system automatycznie tworzy cztery rekordy kategorii udostępnionych.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-148">After the transaction category record is synchronized, the system automatically creates four shared category records.</span></span> <span data-ttu-id="cc3f8-149">Każdy rekord odpowiada typowi transakcji w aplikacjach Finance and Operations i łączy je z rekordem kategorii transakcji.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-149">Each record corresponds to a transaction type in Finance and Operations apps and links them to the transaction category record.</span></span>

![Integracja kategorii transakcji](./media/4TransactionCategories.jpg)

<span data-ttu-id="cc3f8-151">Korzystanie z kategorii transakcji do szacowania i wartości rzeczywistych wymaga, aby księgowy projektu lub systemowy administrator utworzył odpowiednie kategorie projektu w każdym podmiocie prawnym.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-151">Using transaction categories for estimates and actuals requires the project accountant or system administrator to create corresponding project categories in every legal entity.</span></span> <span data-ttu-id="cc3f8-152">Aby uzyskać więcej informacji, zobacz [Konfigurowanie kategorii projektu](../project-accounting/configure-project-categories.md).</span><span class="sxs-lookup"><span data-stu-id="cc3f8-152">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md).</span></span>