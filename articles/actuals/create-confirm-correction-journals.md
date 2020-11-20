---
title: Tworzenie i potwierdzanie arkuszy korekcyjnych
description: W tym temacie zamieszczono informacje dotyczące tworzenia i potwierdzania arkusza korekcyjnego.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127777"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="2e713-103">Tworzenie i potwierdzanie arkuszy korekcyjnych</span><span class="sxs-lookup"><span data-stu-id="2e713-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="2e713-104">_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_</span><span class="sxs-lookup"><span data-stu-id="2e713-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e713-105">Czasami może zostać wprowadzony błędnie wpis czasu lub wydatku.</span><span class="sxs-lookup"><span data-stu-id="2e713-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="2e713-106">Na przykład konsultant może wybrać nieprawidłową datę przy tworzeniu wpisu czasu lub może poprzestawiać liczby przy wprowadzaniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="2e713-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="2e713-107">Jeśli konsultant nie może dokonać aktualizacji przesłanych wpisów, Administrator może bezpośrednio poprawić wpis w projekcie.</span><span class="sxs-lookup"><span data-stu-id="2e713-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="2e713-108">Do wykonania procedur opisanych w tym temacie są wymagane uprawnienia Administratora.</span><span class="sxs-lookup"><span data-stu-id="2e713-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="2e713-109">Popraw zatwierdzone wpisy czasu</span><span class="sxs-lookup"><span data-stu-id="2e713-109">Correct approved time entries</span></span>     

<span data-ttu-id="2e713-110">Wykonaj poniższe kroki, aby skorygować pojedynczy lub wiele wpisów czasu projektu.</span><span class="sxs-lookup"><span data-stu-id="2e713-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="2e713-111">W obszarze **Sprzedaż** wybierz opcję **Transakcje**, a następnie wybierz opcję **Zatwierdzony czas**.</span><span class="sxs-lookup"><span data-stu-id="2e713-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="2e713-112">Na liście **Zatwierdzony czas** znajdź i wybierz jeden lub więcej zatwierdzonych wpisów czasu, które mają zostać poprawione.</span><span class="sxs-lookup"><span data-stu-id="2e713-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="2e713-113">Do wyszukania pokrewnych wpisów można użyć funkcji filtru.</span><span class="sxs-lookup"><span data-stu-id="2e713-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="2e713-114">Można na przykład filtrować identyfikatory projektów i wybrać wszystkie zatwierdzone wpisy czasu z danym Identyfikatorem projektu.</span><span class="sxs-lookup"><span data-stu-id="2e713-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="2e713-115">Wybierz **Koryguj wpisy**.</span><span class="sxs-lookup"><span data-stu-id="2e713-115">Select **Correct entries**.</span></span> <span data-ttu-id="2e713-116">Zostanie automatycznie utworzony nowy arkusz korekt z przypisanym typem **Korekta czasu**.</span><span class="sxs-lookup"><span data-stu-id="2e713-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="2e713-117">Wybrane wpisy zostaną dodane do arkusza.</span><span class="sxs-lookup"><span data-stu-id="2e713-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="2e713-118">Na stronie **Nowy arkusz** wprowadź **Opis** arkusza korekty, a następnie wybierz kartę **Korekty wpisów czasu**.</span><span class="sxs-lookup"><span data-stu-id="2e713-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="2e713-119">W sekcji **Nowe wartości dla wpisów czasu** w razie potrzeby zaktualizuj pola do odpowiednich informacji.</span><span class="sxs-lookup"><span data-stu-id="2e713-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="2e713-120">Można na przykład zmienić przypisany projekt lub zasób zaksięgowany.</span><span class="sxs-lookup"><span data-stu-id="2e713-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="2e713-121">Wybierz **Podgląd**.</span><span class="sxs-lookup"><span data-stu-id="2e713-121">Select **Preview**.</span></span> <span data-ttu-id="2e713-122">W oknie dialogowym wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e713-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="2e713-123">Na karcie **Wiersze arkusza** można wyświetlić listę oryginalnych wartości rzeczywistych związanych z wybranymi wpisami czasu, które zostały odwrócone, i poprawione odpowiadające utworzone wiersze.</span><span class="sxs-lookup"><span data-stu-id="2e713-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="2e713-124">Jeśli trzeba dokonać dodatkowych korekt, powtórz kroki 5 i 6.</span><span class="sxs-lookup"><span data-stu-id="2e713-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="2e713-125">Wszystkie poprawione wartości rzeczywiste będą miały te same wartości, jak wybrane w sekcji **Nowe wartości dla wpisów czasu**.</span><span class="sxs-lookup"><span data-stu-id="2e713-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="2e713-126">Jeśli poprawki zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="2e713-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="2e713-127">W oknie dialogowym wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e713-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="2e713-128">Wróć do obszaru **Sprzedaż**, wybierz pozycję **Projekty**, a następnie otwórz projekt, dla którego zaktualizowano już te wpisy godzin.</span><span class="sxs-lookup"><span data-stu-id="2e713-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="2e713-129">Na stronie **Projekty** na karcie **Wartości rzeczywiste** wyświetl wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="2e713-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="2e713-130">Jeśli karta **Wartości rzeczywiste** nie jest widoczna, wybierz **Pokrewne** > **Wartości rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="2e713-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="2e713-131">Na liście **Widok skojarzony wartości rzeczywistej** można sprawdzić, czy pierwotne wpisy czasu, które zostały cofnięte, są nadal wyświetlane na liście, podobnie jak w przypadku odpowiednich poprawionych wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="2e713-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="2e713-132">Na przykład na poniższym rysunku znajdują się dwie wiersze z ilością 8,00, która zawiera na liście wartości w kolumnie Kwota.</span><span class="sxs-lookup"><span data-stu-id="2e713-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="2e713-133">Ponadto istnieją dwa wiersze z ilością -8,00, która pokazuje kwoty kredytu w kolumnie kwota.</span><span class="sxs-lookup"><span data-stu-id="2e713-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="2e713-134">Te korekty umożliwiają wyzerowanie ilości.</span><span class="sxs-lookup"><span data-stu-id="2e713-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="2e713-135">Popraw zatwierdzone wpisy wydatków</span><span class="sxs-lookup"><span data-stu-id="2e713-135">Correct approved expense entries</span></span>

<span data-ttu-id="2e713-136">Wykonaj poniższe kroki, aby skorygować jeden lub więcej wpisów wydatków.</span><span class="sxs-lookup"><span data-stu-id="2e713-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="2e713-137">W obszarze **Sprzedaż** w lewym okienku nawigacji w obszarze **Transakcje** wybierz pozycję **Zatwierdzone wydatki**.</span><span class="sxs-lookup"><span data-stu-id="2e713-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="2e713-138">Z listy **Zatwierdzone wydatki** wybierz projekt, który ma zostać poprawiony, a następnie wybierz pozycję **Koryguj wpisy**.</span><span class="sxs-lookup"><span data-stu-id="2e713-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="2e713-139">Zostanie automatycznie utworzony nowy arkusz korekt z przypisanym typem **Korekta wydatku**.</span><span class="sxs-lookup"><span data-stu-id="2e713-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="2e713-140">Na stronie **Nowy arkusz** wprowadź **Opis** poprawki i na karcie **Korekta wydatku** w sekcji **Nowe wartości dla wydatków** wybierz pola danych, które mają zostać poprawione dla wybranych wierszy wydatku.</span><span class="sxs-lookup"><span data-stu-id="2e713-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="2e713-141">Można na przykład przypisać koszty do innego **Projektu** lub skorygować **Kategoria wydatków**, **Data wydatku** lub **Zasób, który można zarezerwować**.</span><span class="sxs-lookup"><span data-stu-id="2e713-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="2e713-142">Wybierz **Podgląd**.</span><span class="sxs-lookup"><span data-stu-id="2e713-142">Select **Preview**.</span></span> <span data-ttu-id="2e713-143">W oknie dialogowym wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e713-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="2e713-144">Sprawdź poprawki na karcie **Wiersze arkusza**. Można wyświetlić listę oryginalnych wartości rzeczywistych związanych z wybranymi wpisami wydatków, które zostały odwrócone, i poprawione odpowiadające utworzone wiersze.</span><span class="sxs-lookup"><span data-stu-id="2e713-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="2e713-145">Jeśli poprawione wartości zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="2e713-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="2e713-146">W oknie dialogowym wybierz **OK.**</span><span class="sxs-lookup"><span data-stu-id="2e713-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="2e713-147">Jeśli wartości nie są wyświetlane zgodnie z oczekiwaniami, wybierz pozycję **Anuluj**, aby powrócić do listy **Zatwierdzonych wydatków**.</span><span class="sxs-lookup"><span data-stu-id="2e713-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="2e713-148">Powtórz kroki od 2 do 5.</span><span class="sxs-lookup"><span data-stu-id="2e713-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="2e713-149">Wszystkie poprawione wartości rzeczywiste będą miały te same wartości, jak wybrane w sekcji **Nowe wartości dla wpisów wydatków**.</span><span class="sxs-lookup"><span data-stu-id="2e713-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="2e713-150">Po potwierdzeniu dziennika korekt wróć do projektu lub projektów, które zaktualizowałeś, aby wyświetlić zmiany.</span><span class="sxs-lookup"><span data-stu-id="2e713-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="2e713-151">Na stronie projektu na karcie **Wartości rzeczywiste** przejrzyj **Widok skojarzony wartości rzeczywistej**.</span><span class="sxs-lookup"><span data-stu-id="2e713-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="2e713-152">Oryginalne wpisy i poprawione wpisy są wyświetlane na liście.</span><span class="sxs-lookup"><span data-stu-id="2e713-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="2e713-153">Na poniższym rysunku pokazano pierwotne kwoty wpisów wydatków oraz odpowiednie skorygowane wpisy kwoty wydatków.</span><span class="sxs-lookup"><span data-stu-id="2e713-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


