---
title: Konfigurowanie integracji z kartą kredytową
description: W tym temacie wyjaśniono, jak pracować z transakcjami kartą kredytową związanymi z wydatkami.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001842"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="bc809-103">Konfigurowanie integracji z kartą kredytową</span><span class="sxs-lookup"><span data-stu-id="bc809-103">Set up credit card integration</span></span>

<span data-ttu-id="bc809-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="bc809-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bc809-105">Transakcje związane z kartą kredytową związane z wydatkami można skonfigurować w taki sposób, aby były automatycznie importowane w harmonogramie cyklicznym.</span><span class="sxs-lookup"><span data-stu-id="bc809-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="bc809-106">Można także importować transakcje ręcznie, zależnie od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="bc809-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="bc809-107">Transakcje kartą kredytową są importowane za pośrednictwem obiektu danych o nazwie transakcje kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="bc809-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="bc809-108">Importowanie transakcji kartą kredytową</span><span class="sxs-lookup"><span data-stu-id="bc809-108">Import credit card transactions</span></span>

<span data-ttu-id="bc809-109">Aby zaimportować transakcje kartą kredytową, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="bc809-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="bc809-110">Na stronie **Transakcje kartą kredytową** wybierz opcję **Import transakcji**.</span><span class="sxs-lookup"><span data-stu-id="bc809-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="bc809-111">W przypadku korzystania z zarządzania danymi po raz pierwszy, przed kontynuowaniem system musi zaktualizować listę encji danych.</span><span class="sxs-lookup"><span data-stu-id="bc809-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="bc809-112">W polu **Nazwa** wprowadź unikatowy opis zadania importu.</span><span class="sxs-lookup"><span data-stu-id="bc809-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="bc809-113">W polu **Format danych źródłowych** wybierz format pliku zawierającego transakcje kartą kredytową do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="bc809-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="bc809-114">Wybierz opcję **Prześlij**, a następnie znajdź i wybierz plik do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="bc809-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="bc809-115">Po przekazaniu pliku należy sprawdzić poprawność mapowania pliku transakcji kartą kredytową i kolumnę obiektu dane transakcji kartą kredytową, wybierając łącze **Mapa widoku** na kafelku.</span><span class="sxs-lookup"><span data-stu-id="bc809-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="bc809-116">Jeśli występują błędy mapowania lub konieczne będzie jego zmodyfikowanie, można to zrobić na karcie **Wizualizacja** lub **Szczegóły mapowania**.</span><span class="sxs-lookup"><span data-stu-id="bc809-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="bc809-117">W celu zautomatyzowania transakcji kartą kredytową wybierz opcję **Utwórz cykliczne zadanie danych**.</span><span class="sxs-lookup"><span data-stu-id="bc809-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="bc809-118">Następnie można ustawić cykliczność definiującą częstotliwość importowania transakcji kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="bc809-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="bc809-119">Kiedy skończysz, wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc809-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="bc809-120">Aby zaimportować wybrany plik teraz, wybierz pozycję **Importuj**.</span><span class="sxs-lookup"><span data-stu-id="bc809-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="bc809-121">Jeśli podczas importu wystąpią błędy, możesz przejrzeć dziennik wykonywania lub dane przemieszczania, aby zobaczyć błędy, które należy naprawić, aby zapewnić pomyślny import.</span><span class="sxs-lookup"><span data-stu-id="bc809-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="bc809-122">Jeśli chcesz zaimportować więcej niż jeden format pliku, musisz utworzyć osobne zadania importu dla każdego typu formatu.</span><span class="sxs-lookup"><span data-stu-id="bc809-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="bc809-123">Ponowne przypisywanie transakcji kartą kredytową dla zakończonych pracowników</span><span class="sxs-lookup"><span data-stu-id="bc809-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="bc809-124">Po zakończeniu rekordu pracownika, jego konto Active Directory Domain Services (AD DS) jest wyłączane.</span><span class="sxs-lookup"><span data-stu-id="bc809-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="bc809-125">Jednakże mogą istnieć aktywne transakcje kartą, które nadal trzeba rozliczyć lub zwrócić.</span><span class="sxs-lookup"><span data-stu-id="bc809-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="bc809-126">Na stronie **Transakcje kartą kredytową** możesz ponownie przypisać pracownika do dowolnej transakcji kartą kredytową, w przypadku której powiązany pracownik został zwolniony.</span><span class="sxs-lookup"><span data-stu-id="bc809-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="bc809-127">Wybierz jedną lub kilka transakcji kartą kredytową, a następnie wybierz opcję **Ponowne przypisanie transakcji**.</span><span class="sxs-lookup"><span data-stu-id="bc809-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="bc809-128">Następnie można wybrać innego pracownika, do którego ma zostać przypisana transakcja kartą kredytową.</span><span class="sxs-lookup"><span data-stu-id="bc809-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="bc809-129">Po zmianie przypisania transakcji kartą kredytową można ją wybrać z poziomu raportu z wydatków i zapłacić korzystając z normalnego procesu zwrotu kosztu wydatków.</span><span class="sxs-lookup"><span data-stu-id="bc809-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="bc809-130">Usuwanie transakcji kartą kredytową</span><span class="sxs-lookup"><span data-stu-id="bc809-130">Delete credit card transactions</span></span> 

<span data-ttu-id="bc809-131">Czasami po zaimportowaniu transakcji kartą kredytową niektóre transakcje mogą wymagać usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bc809-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="bc809-132">Może tak być, jeśli transakcje są duplikatami lub ponieważ dane mogą być niedokładne.</span><span class="sxs-lookup"><span data-stu-id="bc809-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="bc809-133">Administratorzy mogą używać funkcji **Usuwanie transakcji kart kredytowych**, aby wybierać i usuwać transakcje kartą kredytową, które **nie są dołączone** do raportu wydatków.</span><span class="sxs-lookup"><span data-stu-id="bc809-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="bc809-134">Przejdź do **Zadania okresowe** > **Usuń transakcje kartą kredytową**.</span><span class="sxs-lookup"><span data-stu-id="bc809-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="bc809-135">Wybierz opcję **Filtruj** i podaj informacje służące do identyfikacji uwzględnianych rekordów.</span><span class="sxs-lookup"><span data-stu-id="bc809-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="bc809-136">Wybierz **OK**, aby usunąć rekordy.</span><span class="sxs-lookup"><span data-stu-id="bc809-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
