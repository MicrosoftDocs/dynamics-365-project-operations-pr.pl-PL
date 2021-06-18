---
title: Zakup materiałów niemagazynowanych za pomocą oczekujących faktur od dostawcy
description: W tym temacie wyjaśniono, jak rejestrować oczekujące faktury od dostawcy.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993819"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="e16cb-103">Zakup materiałów niemagazynowanych za pomocą oczekujących faktur od dostawcy</span><span class="sxs-lookup"><span data-stu-id="e16cb-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="e16cb-104">_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_</span><span class="sxs-lookup"><span data-stu-id="e16cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e16cb-105">W związku z tym, że firma nabywa niezabezpieczone materiały dla projektu, można od razu zarejestrować koszty związane z projektem.</span><span class="sxs-lookup"><span data-stu-id="e16cb-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="e16cb-106">Na przykład Contoso Robotics US wykonuje projekt odnowienia sprzętu i potrzebuje licencji na oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="e16cb-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="e16cb-107">Te licencje można uzyskać od innych dostawców.</span><span class="sxs-lookup"><span data-stu-id="e16cb-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="e16cb-108">Korzystając z funkcji Dynamics 365 Finance, pracownik odpowiedzialny za rozrachunki z dostawcami dodaje fakturę od dostawcy i przypisuje koszty licencji bezpośrednio w ramach projektu odnowienia sprzętu.</span><span class="sxs-lookup"><span data-stu-id="e16cb-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e16cb-109">Przed użyciem funkcji opisanych w tym temacie należy przejrzeć i zastosować wymagane konfiguracje.</span><span class="sxs-lookup"><span data-stu-id="e16cb-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="e16cb-110">Aby uzyskać więcej informacji, zobacz [jak włączyć obsługę materiałów niebędących na stanie magazynowym i oczekujących na faktury dostawcy.](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="e16cb-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="e16cb-111">Publikowanie oczekującej faktury związanej z projektem</span><span class="sxs-lookup"><span data-stu-id="e16cb-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="e16cb-112">Oczekujące faktury dostawcy można zarejestrować na stronie **Oczekujące faktury dostawcy** (**Rozrachunki z dostawccami** > **Faktury** > **Oczekujące faktury od dostawców**).</span><span class="sxs-lookup"><span data-stu-id="e16cb-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="e16cb-113">Wykonaj następujące kroki, aby opublikować oczekującą fakturę od dostawcy związaną z projektem:</span><span class="sxs-lookup"><span data-stu-id="e16cb-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="e16cb-114">Wybierz opcję **Rozrachunki z dostawcami** > **Faktury** i wybierz opcję **Nowa**.</span><span class="sxs-lookup"><span data-stu-id="e16cb-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="e16cb-115">W polu **Konto faktury** wybierz dostawcę, a następnie w polu **Numer** wprowadź identyfikator faktury dostawcy.</span><span class="sxs-lookup"><span data-stu-id="e16cb-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="e16cb-116">Dodaj wiersz do faktury dostawcy i w polu **Numer pozycji** wybierz pozycję zakupioną od dostawcy, której brak w magazynie.</span><span class="sxs-lookup"><span data-stu-id="e16cb-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e16cb-117">W ramach projektu nie można rejestrować wierszy faktur dostawcy opartych na kategorii.</span><span class="sxs-lookup"><span data-stu-id="e16cb-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="e16cb-118">Dodaj ilość kupionego towaru.</span><span class="sxs-lookup"><span data-stu-id="e16cb-118">Add the quantity purchased.</span></span> <span data-ttu-id="e16cb-119">System wypełni cenę jednostkową w zależności od konfiguracji ceny produktu, którego nie ma w magazynie.</span><span class="sxs-lookup"><span data-stu-id="e16cb-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="e16cb-120">Sprawdź łączną kwotę i inne wymagane szczegóły dotyczące wiersza.</span><span class="sxs-lookup"><span data-stu-id="e16cb-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="e16cb-121">W szczegółach wiersza na karcie **Projekt** wybierz identyfikator projektu, do którego zostanie zarejestrowany element.</span><span class="sxs-lookup"><span data-stu-id="e16cb-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="e16cb-122">Opcjonalnie wybierz numer działania i zaktualizuj właściwość kategorii i wiersza projektu.</span><span class="sxs-lookup"><span data-stu-id="e16cb-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="e16cb-123">Opublikuj oczekującą fakturę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="e16cb-123">Post pending vendor invoice.</span></span> <span data-ttu-id="e16cb-124">Po zaksięgowaniu faktury system zapisuje:</span><span class="sxs-lookup"><span data-stu-id="e16cb-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="e16cb-125">Kwotę salda dostawcy.</span><span class="sxs-lookup"><span data-stu-id="e16cb-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="e16cb-126">Kwotę podatku od sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="e16cb-126">The sales tax amount.</span></span>
    - <span data-ttu-id="e16cb-127">Koszt w ramach projektu jest rejestrowany na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="e16cb-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="e16cb-128">Rzeczywista transakcja projektu w Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e16cb-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="e16cb-129">Ta transakcja jest dalej przetwarzana przy użyciu [dziennika integracji Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="e16cb-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="e16cb-130">Umieszczenie tej kwoty powoduje przeniesienie kwoty z konta integracji na konto kosztów projektu.</span><span class="sxs-lookup"><span data-stu-id="e16cb-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
