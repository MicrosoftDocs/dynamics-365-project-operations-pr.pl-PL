---
title: Tworzenie i potwierdzanie arkuszy korekcyjnych
description: W tym temacie zamieszczono informacje dotyczące tworzenia i potwierdzania arkusza korekcyjnego.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896969"
---
# <a name="create-and-confirm-correction-journals"></a>Tworzenie i potwierdzanie arkuszy korekcyjnych

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

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


