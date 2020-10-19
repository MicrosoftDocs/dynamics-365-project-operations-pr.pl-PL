---
title: Omówienie zatwierdzeń
description: Ta temat zawiera informacje na temat pracy z zatwierdzeniami w Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961179"
---
# <a name="approvals-overview"></a><span data-ttu-id="c9973-103">Omówienie zatwierdzeń</span><span class="sxs-lookup"><span data-stu-id="c9973-103">Approvals overview</span></span>

<span data-ttu-id="c9973-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="c9973-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c9973-105">Przepływy pracy i czasu są przenoszone do etapu zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="c9973-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="c9973-106">Po zatwierdzeniu wpisów transakcje są rejestrowane w wartościach rzeczywistych lub czasu zaksięgowanych w harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="c9973-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="c9973-107">Przepływ pracy zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="c9973-107">Approvals workflow</span></span>
<span data-ttu-id="c9973-108">Podczas tworzenia i przesyłania wpisu godziny lub wydatku zostaje utworzony wpis zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="c9973-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="c9973-109">Osoba zatwierdzająca lub menedżer projektu przegląda i zatwierdza Twój wpis.</span><span class="sxs-lookup"><span data-stu-id="c9973-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="c9973-110">Jeśli wpis jest powiązany z projektem, to po jego zatwierdzeniu zostaną utworzone wartości rzeczywiste.</span><span class="sxs-lookup"><span data-stu-id="c9973-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="c9973-111">Pozwala to na śledzenie kosztów i rozliczania fakturowania.</span><span class="sxs-lookup"><span data-stu-id="c9973-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="c9973-112">Zatwierdzanie wpisu</span><span class="sxs-lookup"><span data-stu-id="c9973-112">Approve an entry</span></span>
<span data-ttu-id="c9973-113">Formularz **Zatwierdzania** umożliwia przełączanie między różnymi widokami, dzięki czemu można wyświetlać różne typy zatwierdzeń.</span><span class="sxs-lookup"><span data-stu-id="c9973-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="c9973-114">Przejdź do formularza **Zatwierdzenia** i wybierz **Koszty**, **Czas** lub **Odwołania**.</span><span class="sxs-lookup"><span data-stu-id="c9973-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="c9973-115">Przejrzyj każde zatwierdzenie i wybierz te, które chcesz zatwierdzić.</span><span class="sxs-lookup"><span data-stu-id="c9973-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="c9973-116">Wybierz przycisk **Zatwierdź**, aby zatwierdzić wybrane wpisy.</span><span class="sxs-lookup"><span data-stu-id="c9973-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="c9973-117">System będzie przetwarzać te wpisy i tworzyć wartości rzeczywiste lub rezerwację.</span><span class="sxs-lookup"><span data-stu-id="c9973-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="c9973-118">Odrzucanie wpisu</span><span class="sxs-lookup"><span data-stu-id="c9973-118">Reject an entry</span></span>
<span data-ttu-id="c9973-119">Jako osoba zatwierdzająca, być może będziesz musiał przesłać wpis z powrotem do użytkownika w celu dokonania poprawek.</span><span class="sxs-lookup"><span data-stu-id="c9973-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="c9973-120">Przejdź do formularza **Zatwierdzanie** i wybierz wpis do odrzucenia.</span><span class="sxs-lookup"><span data-stu-id="c9973-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="c9973-121">Wybierz pozycję **Odrzuć**.</span><span class="sxs-lookup"><span data-stu-id="c9973-121">Select **Reject**.</span></span>
3. <span data-ttu-id="c9973-122">Opcjonalne — dodaj komentarz w oknie dialogowym **Powód odrzucenia**, aby użytkownik wiedział, dlaczego dane wpis został odrzucony.</span><span class="sxs-lookup"><span data-stu-id="c9973-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="c9973-123">Wybierz pozycję **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9973-123">Select **OK**.</span></span> <span data-ttu-id="c9973-124">Wpis zostanie zwrócony użytkownikowi.</span><span class="sxs-lookup"><span data-stu-id="c9973-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="c9973-125">Odwołanie wpisów</span><span class="sxs-lookup"><span data-stu-id="c9973-125">Recall entries</span></span>
<span data-ttu-id="c9973-126">W pewnym momencie może zaistnieć konieczność odwołania złożonego wpisu.</span><span class="sxs-lookup"><span data-stu-id="c9973-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="c9973-127">Jeśli wpis nie został zatwierdzony, będzie on natychmiast zwrócony.</span><span class="sxs-lookup"><span data-stu-id="c9973-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="c9973-128">Zatwierdzony wpis może jednak mieć istotny wpływ materialny.</span><span class="sxs-lookup"><span data-stu-id="c9973-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="c9973-129">Aby zatwierdzić odwołanie w celu wystornowania transakcji w wartościach rzeczywistych, osoba zatwierdzająca projekt jest zobowiązana do zaakceptowania odwołania.</span><span class="sxs-lookup"><span data-stu-id="c9973-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="c9973-130">Określenie osób zatwierdzających projekt</span><span class="sxs-lookup"><span data-stu-id="c9973-130">Specify Project approvers</span></span>
<span data-ttu-id="c9973-131">Każdy projekt ma wielu członków zespołu projektu.</span><span class="sxs-lookup"><span data-stu-id="c9973-131">Each project has a number of project team members.</span></span> <span data-ttu-id="c9973-132">Użytkownik może określić, którzy członkowie zespołu mogą zatwierdzać projekty.</span><span class="sxs-lookup"><span data-stu-id="c9973-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="c9973-133">W tym celu należy przejść do formularza **Projekty** i otworzyć projekt z listy.</span><span class="sxs-lookup"><span data-stu-id="c9973-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="c9973-134">Na karcie **Zespół** wybierz członka zespołu, który będzie osobą zatwierdzającą w projekcie, a następnie wybierz pozycję **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="c9973-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="c9973-135">Ustaw pole **Osoba zatwierdzająca w projekcie** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="c9973-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="c9973-136">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c9973-136">Select **Save**.</span></span>
5. <span data-ttu-id="c9973-137">Powtórz kroki od 2 do 4, aby dodać kolejne osoby.</span><span class="sxs-lookup"><span data-stu-id="c9973-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="c9973-138">Konfigurowanie menedżera użytkownika</span><span class="sxs-lookup"><span data-stu-id="c9973-138">Configure the user's manager</span></span>

1. <span data-ttu-id="c9973-139">Przejdź do **Ustawienia** > **Zabezpieczenia** > **Użytkownicy**.</span><span class="sxs-lookup"><span data-stu-id="c9973-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="c9973-140">Wybierz użytkownika, któremu chcesz przypisać menedżera i w obszarze **Informacje o organizacji** wybierz menedżera z listy.</span><span class="sxs-lookup"><span data-stu-id="c9973-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="c9973-141">Wybierz pozycję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c9973-141">Select **Save**.</span></span>


