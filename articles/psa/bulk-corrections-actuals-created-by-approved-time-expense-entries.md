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
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144966"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Korekty zbiorcze utworzone według zatwierdzonych wpisów czasu i wydatków

[!include [banner](../includes/psa-now-project-operations.md)]

Czasami może zostać wprowadzony błędnie wpis czasu lub wydatku. Na przykład konsultant może wybrać nieprawidłową datę przy tworzeniu wpisu czasu lub może poprzestawiać liczby przy wprowadzaniu wydatku. Jeśli konsultant nie może dokonać aktualizacji przesłanych wpisów, Administrator może bezpośrednio poprawić wpis w projekcie.

Do wykonania procedur opisanych w tym temacie są wymagane uprawnienia Administratora.

## <a name="correct-approved-time-entries"></a>Popraw zatwierdzone wpisy czasu     

Wykonaj poniższe kroki, aby skorygować pojedynczy lub wiele wpisów czasu projektu.

1. W obszarze **Sprzedaż** wybierz opcję **Transakcje**, a następnie wybierz opcję **Zatwierdzony czas**. 

2. Na liście **Zatwierdzony czas** znajdź i wybierz jeden lub więcej zatwierdzonych wpisów czasu, które mają zostać poprawione. Do wyszukania pokrewnych wpisów można użyć funkcji filtru. Można na przykład filtrować identyfikatory projektów i wybrać wszystkie zatwierdzone wpisy czasu z danym Identyfikatorem projektu.

3. Wybierz **Koryguj wpisy**. Zostanie automatycznie utworzony nowy arkusz korekt z przypisanym typem **Korekta czasu**. Wybrane wpisy zostaną dodane do arkusza. 

4. Na stronie **Nowy arkusz** wprowadź **Opis** arkusza korekty, a następnie wybierz kartę **Korekty wpisów czasu**.  
5. W sekcji **Nowe wartości dla wpisów czasu** w razie potrzeby zaktualizuj pola do odpowiednich informacji. Można na przykład zmienić przypisany projekt lub zasób zaksięgowany.

6. Wybierz **Podgląd**. W oknie dialogowym wybierz **OK**. Na karcie **Wiersze arkusza** można wyświetlić listę oryginalnych wartości rzeczywistych związanych z wybranymi wpisami czasu, które zostały odwrócone, i poprawione odpowiadające utworzone wiersze. Jeśli trzeba dokonać dodatkowych korekt, powtórz kroki 5 i 6. 

> [!NOTE]
> Wszystkie poprawione wartości rzeczywiste będą miały te same wartości, jak wybrane w sekcji **Nowe wartości dla wpisów czasu**.

7. Jeśli poprawki zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**. W oknie dialogowym wybierz **OK**.

8. Wróć do obszaru **Sprzedaż**, wybierz pozycję **Projekty**, a następnie otwórz projekt, dla którego zaktualizowano już te wpisy godzin. 

9. Na stronie **Projekty** na karcie **Wartości rzeczywiste** wyświetl wprowadzone zmiany. 

> [!NOTE]
> Jeśli karta **Wartości rzeczywiste** nie jest widoczna, wybierz **Pokrewne** > **Wartości rzeczywiste**.  

10. Na liście **Widok skojarzony wartości rzeczywistej** można sprawdzić, czy pierwotne wpisy czasu, które zostały cofnięte, są nadal wyświetlane na liście, podobnie jak w przypadku odpowiednich poprawionych wpisów czasu. 

Na przykład na poniższym rysunku znajdują się dwie wiersze z ilością 8,00, która zawiera na liście wartości w kolumnie Kwota. Ponadto istnieją dwa wiersze z ilością -8,00, która pokazuje kwoty kredytu w kolumnie kwota. Te korekty umożliwiają wyzerowanie ilości.

![Lista Widok skojarzony wartości rzeczywistej](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Popraw zatwierdzone wpisy wydatków

Wykonaj poniższe kroki, aby skorygować jeden lub więcej wpisów wydatków. 

1. W obszarze **Sprzedaż** w lewym okienku nawigacji w obszarze **Transakcje** wybierz pozycję **Zatwierdzone wydatki**.

2. Z listy **Zatwierdzone wydatki** wybierz projekt, który ma zostać poprawiony, a następnie wybierz pozycję **Koryguj wpisy**. Zostanie automatycznie utworzony nowy arkusz korekt z przypisanym typem **Korekta wydatku**. 

3. Na stronie **Nowy arkusz** wprowadź **Opis** poprawki i na karcie **Korekta wydatku** w sekcji **Nowe wartości dla wydatków** wybierz pola danych, które mają zostać poprawione dla wybranych wierszy wydatku. Można na przykład przypisać koszty do innego **Projektu** lub skorygować **Kategoria wydatków**, **Data wydatku** lub **Zasób, który można zarezerwować**.

4. Wybierz **Podgląd**. W oknie dialogowym wybierz **OK**. 

5. Sprawdź poprawki na karcie **Wiersze arkusza**. Można wyświetlić listę oryginalnych wartości rzeczywistych związanych z wybranymi wpisami wydatków, które zostały odwrócone, i poprawione odpowiadające utworzone wiersze.

6. Jeśli poprawione wartości zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**. W oknie dialogowym wybierz **OK.** Jeśli wartości nie są wyświetlane zgodnie z oczekiwaniami, wybierz pozycję **Anuluj**, aby powrócić do listy **Zatwierdzonych wydatków**. Powtórz kroki od 2 do 5. 

> [!NOTE]
> Wszystkie poprawione wartości rzeczywiste będą miały te same wartości, jak wybrane w sekcji **Nowe wartości dla wpisów wydatków**.

7. Po potwierdzeniu dziennika korekt wróć do projektu lub projektów, które zaktualizowałeś, aby wyświetlić zmiany.  

8. Na stronie projektu na karcie **Wartości rzeczywiste** przejrzyj **Widok skojarzony wartości rzeczywistej**. Oryginalne wpisy i poprawione wpisy są wyświetlane na liście. Na poniższym rysunku pokazano pierwotne kwoty wpisów wydatków oraz odpowiednie skorygowane wpisy kwoty wydatków. 

![Rzeczywiste_wydatki](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]