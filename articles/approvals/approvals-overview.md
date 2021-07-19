---
title: Omówienie zatwierdzeń
description: Ta temat zawiera informacje na temat pracy z zatwierdzeniami w Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368669"
---
# <a name="approvals-overview"></a><span data-ttu-id="c25ef-103">Omówienie zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="c25ef-103">Approvals overview</span></span>

<span data-ttu-id="c25ef-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="c25ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c25ef-105">Informacje dotyczące czasu, wydatków i materiałów są przepływem pracy zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="c25ef-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="c25ef-106">Po zatwierdzeniu wpisów transakcje są rejestrowane w wartościach rzeczywistych lub czasu zaksięgowanych w harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="c25ef-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="c25ef-107">Przepływ pracy zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="c25ef-107">Approvals workflow</span></span>
<span data-ttu-id="c25ef-108">Podczas tworzenia i przesyłania wpisu czasu, wydatków lub zużycia materiałów tworzony jest rekord zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="c25ef-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="c25ef-109">Osoba zatwierdzająca projekt lub menedżer przegląda i zatwierdza wpis.</span><span class="sxs-lookup"><span data-stu-id="c25ef-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="c25ef-110">Jeśli wpis dotyczy projektu, dane rzeczywiste zostaną utworzone po jego zatwierdzeniu.</span><span class="sxs-lookup"><span data-stu-id="c25ef-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="c25ef-111">Pozwala to na śledzenie kosztów i rozliczania fakturowania.</span><span class="sxs-lookup"><span data-stu-id="c25ef-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="c25ef-112">Zatwierdzanie wpisu</span><span class="sxs-lookup"><span data-stu-id="c25ef-112">Approve an entry</span></span>
<span data-ttu-id="c25ef-113">Strona **Zatwierdzenia** umożliwia przełączanie się między różnymi widokami, dzięki czemu można przeglądać różne typy zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="c25ef-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="c25ef-114">Przejdź do strony **Zatwierdzanie** i wybierz opcję **Koszty**, **Czas**, **Użycie materiałów** lub **Wycofania**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="c25ef-115">Przejrzyj każde zatwierdzenie i wybierz te, które chcesz zatwierdzić.</span><span class="sxs-lookup"><span data-stu-id="c25ef-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="c25ef-116">Wybierz przycisk **Zatwierdź**, aby zatwierdzić wybrane wpisy.</span><span class="sxs-lookup"><span data-stu-id="c25ef-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="c25ef-117">System przetwarza te wpisy i tworzy wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="c25ef-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="c25ef-118">Odrzucanie wpisu</span><span class="sxs-lookup"><span data-stu-id="c25ef-118">Reject an entry</span></span>
<span data-ttu-id="c25ef-119">Jako osoba zatwierdzająca, być może będziesz musiał przesłać wpis z powrotem do użytkownika w celu dokonania poprawek.</span><span class="sxs-lookup"><span data-stu-id="c25ef-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="c25ef-120">Przejdź do strony **Zatwierdzenia** i wybierz wpis, który chcesz odrzucić.</span><span class="sxs-lookup"><span data-stu-id="c25ef-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="c25ef-121">Wybierz pozycję **Odrzuć**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-121">Select **Reject**.</span></span>
3. <span data-ttu-id="c25ef-122">Opcjonalnie dodaj komentarz w oknie dialogowym **Komentarze odrzucenia**, aby poinformować użytkownika, dlaczego wpis jest odrzucany.</span><span class="sxs-lookup"><span data-stu-id="c25ef-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="c25ef-123">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-123">Select **OK**.</span></span> <span data-ttu-id="c25ef-124">Wpis zostanie zwrócony użytkownikowi.</span><span class="sxs-lookup"><span data-stu-id="c25ef-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="c25ef-125">Anuluj zatwierdzenie</span><span class="sxs-lookup"><span data-stu-id="c25ef-125">Cancel approval</span></span>
<span data-ttu-id="c25ef-126">W niektórych przypadkach może być konieczne anulowanie uprzednio zatwierdzonego wpisu.</span><span class="sxs-lookup"><span data-stu-id="c25ef-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="c25ef-127">Anulowanie uprzednio zatwierdzonego wpisu będzie miało wpływ na finanse.</span><span class="sxs-lookup"><span data-stu-id="c25ef-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="c25ef-128">Zatwierdzanie próśb o wycofanie</span><span class="sxs-lookup"><span data-stu-id="c25ef-128">Approving recall requests</span></span>
<span data-ttu-id="c25ef-129">W niektórych przypadkach konsultant może potrzebować przypomnieć wcześniej zatwierdzony wpis.</span><span class="sxs-lookup"><span data-stu-id="c25ef-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="c25ef-130">Anulowanie uprzednio zatwierdzonego wpisu będzie miało wpływ na finanse.</span><span class="sxs-lookup"><span data-stu-id="c25ef-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="c25ef-131">Osoba zatwierdzająca projekt musi zatwierdzić wycofanie w celu cofnięcia transakcji w danych rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="c25ef-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="c25ef-132">Określenie osób zatwierdzających projekt</span><span class="sxs-lookup"><span data-stu-id="c25ef-132">Specify Project approvers</span></span>
<span data-ttu-id="c25ef-133">Każdy projekt ma wielu członków zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="c25ef-133">Each project has a number of project team members.</span></span> <span data-ttu-id="c25ef-134">Użytkownik może określić, którzy członkowie zespołu mogą zatwierdzać projekty.</span><span class="sxs-lookup"><span data-stu-id="c25ef-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="c25ef-135">Przejdź na stronę **Projekty** i otwórz projekt z listy.</span><span class="sxs-lookup"><span data-stu-id="c25ef-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="c25ef-136">Na karcie **Zespół** wybierz członka zespołu, który będzie osobą zatwierdzającą w projekcie, a następnie wybierz pozycję **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="c25ef-137">Ustaw pole **Osoba zatwierdzająca w projekcie** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="c25ef-138">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-138">Select **Save**.</span></span>
5. <span data-ttu-id="c25ef-139">Powtórz kroki od 2 do 4, aby dodać kolejne osoby.</span><span class="sxs-lookup"><span data-stu-id="c25ef-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="c25ef-140">Konfigurowanie menedżera użytkownika</span><span class="sxs-lookup"><span data-stu-id="c25ef-140">Configure the user's manager</span></span>

1. <span data-ttu-id="c25ef-141">Przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="c25ef-142">Wybierz użytkownika, któremu chcesz przypisać menedżera i w obszarze **Informacje o organizacji** wybierz menedżera z listy.</span><span class="sxs-lookup"><span data-stu-id="c25ef-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="c25ef-143">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c25ef-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
