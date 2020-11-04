---
title: Importowanie i zarządzanie transakcjami kartami kredytowymi
description: W tym temat przedstawiono sposób importu i utrzymywania transakcji kartą kredytową związanych z wydatkami. Te transakcje można skonfigurować w taki sposób, aby były automatycznie importowane w harmonogramie cyklicznym, lub mogą też w razie potrzeby zostać zaimportowane ręcznie.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082165"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="e129c-104">Importowanie i zarządzanie transakcjami kartami kredytowymi</span><span class="sxs-lookup"><span data-stu-id="e129c-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e129c-105">Transakcje związane z kartą kredytową związane z wydatkami można skonfigurować w taki sposób, aby były automatycznie importowane w harmonogramie cyklicznym.</span><span class="sxs-lookup"><span data-stu-id="e129c-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="e129c-106">Można także importować transakcje ręcznie, zależnie od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="e129c-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="e129c-107">Transakcje kartą kredytową są importowane za pośrednictwem obiektu danych o nazwie transakcje kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="e129c-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="e129c-108">Aby uzyskać więcej informacji o encjach danych, zobacz [Encje danych](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="e129c-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="e129c-109">Importowanie transakcji kartą kredytową</span><span class="sxs-lookup"><span data-stu-id="e129c-109">Import credit card transactions</span></span>

1. <span data-ttu-id="e129c-110">Na stronie **Transakcje kartą kredytową** wybierz opcję **Import transakcji**.</span><span class="sxs-lookup"><span data-stu-id="e129c-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="e129c-111">W przypadku korzystania z zarządzania danymi po raz pierwszy, przed kontynuowaniem system musi zaktualizować listę encji danych.</span><span class="sxs-lookup"><span data-stu-id="e129c-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="e129c-112">W polu **Nazwa** wprowadź unikatowy opis zadania importu.</span><span class="sxs-lookup"><span data-stu-id="e129c-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="e129c-113">W polu **Format danych źródłowych** wybierz format pliku zawierającego transakcje kartą kredytową do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="e129c-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="e129c-114">Wybierz opcję **Prześlij** , a następnie znajdź i wybierz plik do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="e129c-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="e129c-115">Po przekazaniu pliku należy sprawdzić poprawność mapowania pliku transakcji kartą kredytową i kolumnę obiektu dane transakcji kartą kredytową, wybierając łącze **Mapa widoku** na kafelku.</span><span class="sxs-lookup"><span data-stu-id="e129c-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="e129c-116">Jeśli występują błędy mapowania lub konieczne będzie jego zmodyfikowanie, można to zrobić na karcie **Wizualizacja** lub **Szczegóły mapowania**.</span><span class="sxs-lookup"><span data-stu-id="e129c-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="e129c-117">W celu zautomatyzowania transakcji kartą kredytową wybierz opcję **Utwórz cykliczne zadanie danych**.</span><span class="sxs-lookup"><span data-stu-id="e129c-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="e129c-118">Następnie można ustawić cykliczność definiującą częstotliwość importowania transakcji kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="e129c-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="e129c-119">Kiedy skończysz, wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="e129c-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="e129c-120">Aby zaimportować wybrany plik teraz, wybierz pozycję **Importuj**.</span><span class="sxs-lookup"><span data-stu-id="e129c-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="e129c-121">Jeśli podczas importowania wystąpią błędy, można wyświetlić dziennik wykonywania lub dane przemieszczania, aby zobaczyć błędy, które należy rozwiązać w celu zagwarantowania pomyślnego zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="e129c-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="e129c-122">Jeśli zachodzi konieczność zaimportowania więcej niż jednego formatu pliku, należy utworzyć osobne zadania importu dla każdego typu formatu.</span><span class="sxs-lookup"><span data-stu-id="e129c-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="e129c-123">Ponowne przypisywanie transakcji kartą kredytową dla zakończonych pracowników</span><span class="sxs-lookup"><span data-stu-id="e129c-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="e129c-124">Po zakończeniu rekordu pracownika, jego konto Active Directory Domain Services (AD DS) jest wyłączane.</span><span class="sxs-lookup"><span data-stu-id="e129c-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="e129c-125">Jednakże mogą istnieć aktywne transakcje kartą, które nadal trzeba rozliczyć lub zwrócić.</span><span class="sxs-lookup"><span data-stu-id="e129c-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="e129c-126">Na stronie **Transakcji kartą kredytową** można przypisać pracownika do dowolnej transakcji kartą kredytową, nawet pracownika, który już nie jest zatrudniony.</span><span class="sxs-lookup"><span data-stu-id="e129c-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="e129c-127">Wybierz jedną lub kilka transakcji kartą kredytową, a następnie wybierz opcję **Ponowne przypisanie transakcji**.</span><span class="sxs-lookup"><span data-stu-id="e129c-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="e129c-128">Następnie można wybrać innego pracownika, do którego ma zostać przypisana transakcja kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="e129c-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="e129c-129">Po zmianie przypisania transakcji kartą kredytową można ją wybrać z poziomu raportu z wydatków i zapłacić korzystając z normalnego procesu zwrotu kosztu wydatków.</span><span class="sxs-lookup"><span data-stu-id="e129c-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
