---
title: Konfigurowanie integracji z kartą kredytową
description: W tym temat przedstawiono sposób importu i utrzymywania transakcji kartą kredytową związanych z wydatkami.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c7971204b485ee7cb222cd9cffdfdfde93dcf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081975"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="013a5-103">Konfigurowanie integracji z kartą kredytową</span><span class="sxs-lookup"><span data-stu-id="013a5-103">Set up credit card integration</span></span>

<span data-ttu-id="013a5-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="013a5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="013a5-105">Transakcje związane z kartą kredytową związane z wydatkami można skonfigurować w taki sposób, aby były automatycznie importowane w harmonogramie cyklicznym.</span><span class="sxs-lookup"><span data-stu-id="013a5-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="013a5-106">Można także importować transakcje ręcznie, zależnie od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="013a5-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="013a5-107">Transakcje kartą kredytową są importowane za pośrednictwem obiektu danych o nazwie transakcje kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="013a5-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="013a5-108">Importowanie transakcji kartą kredytową</span><span class="sxs-lookup"><span data-stu-id="013a5-108">Import credit card transactions</span></span>

1. <span data-ttu-id="013a5-109">Na stronie **Transakcje kartą kredytową** wybierz opcję **Import transakcji**.</span><span class="sxs-lookup"><span data-stu-id="013a5-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="013a5-110">W przypadku korzystania z zarządzania danymi po raz pierwszy, przed kontynuowaniem system musi zaktualizować listę encji danych.</span><span class="sxs-lookup"><span data-stu-id="013a5-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="013a5-111">W polu **Nazwa** wprowadź unikatowy opis zadania importu.</span><span class="sxs-lookup"><span data-stu-id="013a5-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="013a5-112">W polu **Format danych źródłowych** wybierz format pliku zawierającego transakcje kartą kredytową do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="013a5-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="013a5-113">Wybierz opcję **Prześlij** , a następnie znajdź i wybierz plik do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="013a5-113">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="013a5-114">Po przekazaniu pliku należy sprawdzić poprawność mapowania pliku transakcji kartą kredytową i kolumnę obiektu dane transakcji kartą kredytową, wybierając łącze **Mapa widoku** na kafelku.</span><span class="sxs-lookup"><span data-stu-id="013a5-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="013a5-115">Jeśli występują błędy mapowania lub konieczne będzie jego zmodyfikowanie, można to zrobić na karcie **Wizualizacja** lub **Szczegóły mapowania**.</span><span class="sxs-lookup"><span data-stu-id="013a5-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="013a5-116">W celu zautomatyzowania transakcji kartą kredytową wybierz opcję **Utwórz cykliczne zadanie danych**.</span><span class="sxs-lookup"><span data-stu-id="013a5-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="013a5-117">Następnie można ustawić cykliczność definiującą częstotliwość importowania transakcji kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="013a5-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="013a5-118">Kiedy skończysz, wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="013a5-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="013a5-119">Aby zaimportować wybrany plik teraz, wybierz pozycję **Importuj**.</span><span class="sxs-lookup"><span data-stu-id="013a5-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="013a5-120">Jeśli podczas importowania wystąpią błędy, można wyświetlić dziennik wykonywania lub dane przemieszczania, aby zobaczyć błędy, które należy rozwiązać w celu zagwarantowania pomyślnego zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="013a5-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="013a5-121">Jeśli zachodzi konieczność zaimportowania więcej niż jednego formatu pliku, należy utworzyć osobne zadania importu dla każdego typu formatu.</span><span class="sxs-lookup"><span data-stu-id="013a5-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="013a5-122">Ponowne przypisywanie transakcji kartą kredytową dla zakończonych pracowników</span><span class="sxs-lookup"><span data-stu-id="013a5-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="013a5-123">Po zakończeniu rekordu pracownika, jego konto Active Directory Domain Services (AD DS) jest wyłączane.</span><span class="sxs-lookup"><span data-stu-id="013a5-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="013a5-124">Jednakże mogą istnieć aktywne transakcje kartą, które nadal trzeba rozliczyć lub zwrócić.</span><span class="sxs-lookup"><span data-stu-id="013a5-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="013a5-125">Na stronie **Transakcji kartą kredytową** można przypisać pracownika do dowolnej transakcji kartą kredytową, nawet pracownika, który już nie jest zatrudniony.</span><span class="sxs-lookup"><span data-stu-id="013a5-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="013a5-126">Wybierz jedną lub kilka transakcji kartą kredytową, a następnie wybierz opcję **Ponowne przypisanie transakcji**.</span><span class="sxs-lookup"><span data-stu-id="013a5-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="013a5-127">Następnie można wybrać innego pracownika, do którego ma zostać przypisana transakcja kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="013a5-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="013a5-128">Po zmianie przypisania transakcji kartą kredytową można ją wybrać z poziomu raportu z wydatków i zapłacić korzystając z normalnego procesu zwrotu kosztu wydatków.</span><span class="sxs-lookup"><span data-stu-id="013a5-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
