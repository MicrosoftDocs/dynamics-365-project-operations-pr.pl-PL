---
title: Korekty zbiorcze utworzone według zatwierdzonych wpisów czasu i wydatków
description: W tym temacie wyjaśniono, w jaki sposób administrator może wprowadzać pojedyncze lub zbiorcze korekty wcześniej zatwierdzonych wpisów czasu lub wydatków, jeśli rozliczenie nie jest zakończone.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082188"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="e570b-103">Korekty zbiorcze utworzone według zatwierdzonych wpisów czasu i wydatków</span><span class="sxs-lookup"><span data-stu-id="e570b-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

<span data-ttu-id="e570b-104">Czasami może zostać wprowadzony błędnie wpis czasu lub wydatku.</span><span class="sxs-lookup"><span data-stu-id="e570b-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="e570b-105">Na przykład konsultant może wybrać nieprawidłową datę przy tworzeniu wpisu czasu lub może poprzestawiać liczby przy wprowadzaniu wydatku.</span><span class="sxs-lookup"><span data-stu-id="e570b-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="e570b-106">Jeśli konsultant nie może dokonać aktualizacji przesłanych wpisów, Administrator może bezpośrednio poprawić wpis w projekcie.</span><span class="sxs-lookup"><span data-stu-id="e570b-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="e570b-107">Do wykonania procedur opisanych w tym temacie są wymagane uprawnienia Administratora.</span><span class="sxs-lookup"><span data-stu-id="e570b-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="e570b-108">Popraw zatwierdzone wpisy czasu</span><span class="sxs-lookup"><span data-stu-id="e570b-108">Correct approved time entries</span></span>     

<span data-ttu-id="e570b-109">Wykonaj poniższe kroki, aby skorygować pojedynczy lub wiele wpisów czasu projektu.</span><span class="sxs-lookup"><span data-stu-id="e570b-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="e570b-110">W obszarze **Sprzedaż** wybierz opcję **Transakcje** , a następnie wybierz opcję **Zatwierdzony czas**.</span><span class="sxs-lookup"><span data-stu-id="e570b-110">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="e570b-111">Na liście **Zatwierdzony czas** znajdź i wybierz jeden lub więcej zatwierdzonych wpisów czasu, które mają zostać poprawione.</span><span class="sxs-lookup"><span data-stu-id="e570b-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="e570b-112">Do wyszukania pokrewnych wpisów można użyć funkcji filtru.</span><span class="sxs-lookup"><span data-stu-id="e570b-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="e570b-113">Można na przykład filtrować identyfikatory projektów i wybrać wszystkie zatwierdzone wpisy czasu z danym Identyfikatorem projektu.</span><span class="sxs-lookup"><span data-stu-id="e570b-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="e570b-114">Wybierz **Koryguj wpisy**.</span><span class="sxs-lookup"><span data-stu-id="e570b-114">Select **Correct entries**.</span></span> <span data-ttu-id="e570b-115">Zostanie automatycznie utworzony nowy arkusz korekt z przypisanym typem **Korekta czasu**.</span><span class="sxs-lookup"><span data-stu-id="e570b-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="e570b-116">Wybrane wpisy zostaną dodane do arkusza.</span><span class="sxs-lookup"><span data-stu-id="e570b-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="e570b-117">Na stronie **Nowy arkusz** wprowadź **Opis** arkusza korekty, a następnie wybierz kartę **Korekty wpisów czasu**.</span><span class="sxs-lookup"><span data-stu-id="e570b-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="e570b-118">W sekcji **Nowe wartości dla wpisów czasu** w razie potrzeby zaktualizuj pola do odpowiednich informacji.</span><span class="sxs-lookup"><span data-stu-id="e570b-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="e570b-119">Można na przykład zmienić przypisany projekt lub zasób zaksięgowany.</span><span class="sxs-lookup"><span data-stu-id="e570b-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="e570b-120">Wybierz **Podgląd**.</span><span class="sxs-lookup"><span data-stu-id="e570b-120">Select **Preview**.</span></span> <span data-ttu-id="e570b-121">W oknie dialogowym wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="e570b-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="e570b-122">Na karcie **Wiersze arkusza** można wyświetlić listę oryginalnych wartości rzeczywistych związanych z wybranymi wpisami czasu, które zostały odwrócone, i poprawione odpowiadające utworzone wiersze.</span><span class="sxs-lookup"><span data-stu-id="e570b-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="e570b-123">Jeśli trzeba dokonać dodatkowych korekt, powtórz kroki 5 i 6.</span><span class="sxs-lookup"><span data-stu-id="e570b-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="e570b-124">Wszystkie poprawione wartości rzeczywiste będą miały te same wartości, jak wybrane w sekcji **Nowe wartości dla wpisów czasu**.</span><span class="sxs-lookup"><span data-stu-id="e570b-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="e570b-125">Jeśli poprawki zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="e570b-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="e570b-126">W oknie dialogowym wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="e570b-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="e570b-127">Wróć do obszaru **Sprzedaż** , wybierz pozycję **Projekty** , a następnie otwórz projekt, dla którego zaktualizowano już te wpisy godzin.</span><span class="sxs-lookup"><span data-stu-id="e570b-127">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="e570b-128">Na stronie **Projekty** na karcie **Wartości rzeczywiste** wyświetl wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="e570b-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="e570b-129">Jeśli karta **Wartości rzeczywiste** nie jest widoczna, wybierz **Pokrewne** > **Wartości rzeczywiste**.</span><span class="sxs-lookup"><span data-stu-id="e570b-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="e570b-130">Na liście **Widok skojarzony wartości rzeczywistej** można sprawdzić, czy pierwotne wpisy czasu, które zostały cofnięte, są nadal wyświetlane na liście, podobnie jak w przypadku odpowiednich poprawionych wpisów czasu.</span><span class="sxs-lookup"><span data-stu-id="e570b-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="e570b-131">Na przykład na poniższym rysunku znajdują się dwie wiersze z ilością 8,00, która zawiera na liście wartości w kolumnie Kwota.</span><span class="sxs-lookup"><span data-stu-id="e570b-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="e570b-132">Ponadto istnieją dwa wiersze z ilością -8,00, która pokazuje kwoty kredytu w kolumnie kwota.</span><span class="sxs-lookup"><span data-stu-id="e570b-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="e570b-133">Te korekty umożliwiają wyzerowanie ilości.</span><span class="sxs-lookup"><span data-stu-id="e570b-133">These corrections bring the quantity to zero.</span></span>

![Lista Widok skojarzony wartości rzeczywistej](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="e570b-135">Popraw zatwierdzone wpisy wydatków</span><span class="sxs-lookup"><span data-stu-id="e570b-135">Correct approved expense entries</span></span>

<span data-ttu-id="e570b-136">Wykonaj poniższe kroki, aby skorygować jeden lub więcej wpisów wydatków.</span><span class="sxs-lookup"><span data-stu-id="e570b-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="e570b-137">W obszarze **Sprzedaż** w lewym okienku nawigacji w obszarze **Transakcje** wybierz pozycję **Zatwierdzone wydatki**.</span><span class="sxs-lookup"><span data-stu-id="e570b-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="e570b-138">Z listy **Zatwierdzone wydatki** wybierz projekt, który ma zostać poprawiony, a następnie wybierz pozycję **Koryguj wpisy**.</span><span class="sxs-lookup"><span data-stu-id="e570b-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="e570b-139">Zostanie automatycznie utworzony nowy arkusz korekt z przypisanym typem **Korekta wydatku**.</span><span class="sxs-lookup"><span data-stu-id="e570b-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="e570b-140">Na stronie **Nowy arkusz** wprowadź **Opis** poprawki i na karcie **Korekta wydatku** w sekcji **Nowe wartości dla wydatków** wybierz pola danych, które mają zostać poprawione dla wybranych wierszy wydatku.</span><span class="sxs-lookup"><span data-stu-id="e570b-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="e570b-141">Można na przykład przypisać koszty do innego **Projektu** lub skorygować **Kategoria wydatków** , **Data wydatku** lub **Zasób, który można zarezerwować**.</span><span class="sxs-lookup"><span data-stu-id="e570b-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="e570b-142">Wybierz **Podgląd**.</span><span class="sxs-lookup"><span data-stu-id="e570b-142">Select **Preview**.</span></span> <span data-ttu-id="e570b-143">W oknie dialogowym wybierz **OK**.</span><span class="sxs-lookup"><span data-stu-id="e570b-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="e570b-144">Sprawdź poprawki na karcie **Wiersze arkusza**. Można wyświetlić listę oryginalnych wartości rzeczywistych związanych z wybranymi wpisami wydatków, które zostały odwrócone, i poprawione odpowiadające utworzone wiersze.</span><span class="sxs-lookup"><span data-stu-id="e570b-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="e570b-145">Jeśli poprawione wartości zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**.</span><span class="sxs-lookup"><span data-stu-id="e570b-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="e570b-146">W oknie dialogowym wybierz **OK.**</span><span class="sxs-lookup"><span data-stu-id="e570b-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="e570b-147">Jeśli wartości nie są wyświetlane zgodnie z oczekiwaniami, wybierz pozycję **Anuluj** , aby powrócić do listy **Zatwierdzonych wydatków**.</span><span class="sxs-lookup"><span data-stu-id="e570b-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="e570b-148">Powtórz kroki od 2 do 5.</span><span class="sxs-lookup"><span data-stu-id="e570b-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="e570b-149">Wszystkie poprawione wartości rzeczywiste będą miały te same wartości, jak wybrane w sekcji **Nowe wartości dla wpisów wydatków**.</span><span class="sxs-lookup"><span data-stu-id="e570b-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="e570b-150">Po potwierdzeniu dziennika korekt wróć do projektu lub projektów, które zaktualizowałeś, aby wyświetlić zmiany.</span><span class="sxs-lookup"><span data-stu-id="e570b-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="e570b-151">Na stronie projektu na karcie **Wartości rzeczywiste** przejrzyj **Widok skojarzony wartości rzeczywistej**.</span><span class="sxs-lookup"><span data-stu-id="e570b-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="e570b-152">Oryginalne wpisy i poprawione wpisy są wyświetlane na liście.</span><span class="sxs-lookup"><span data-stu-id="e570b-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="e570b-153">Na poniższym rysunku pokazano pierwotne kwoty wpisów wydatków oraz odpowiednie skorygowane wpisy kwoty wydatków.</span><span class="sxs-lookup"><span data-stu-id="e570b-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Rzeczywiste_wydatki](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
