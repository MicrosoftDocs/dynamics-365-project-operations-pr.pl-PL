---
title: Tworzenie i potwierdzanie arkuszy korekcyjnych
description: W tym temacie zamieszczono informacje dotyczące tworzenia i potwierdzania arkusza korekcyjnego.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582816"
---
# <a name="create-and-confirm-correction-journals"></a>Tworzenie i potwierdzanie arkuszy korekcyjnych

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Czasami wpisany czas lub koszt może zostać wprowadzony niepoprawnie. Na przykład konsultant może wybrać nieprawidłową datę podczas tworzenia wpisu czasu lub wybrać zły projekt po wprowadzeniu wydatku. Jeśli konsultant nie może zaktualizować przesłanych wpisów, administrator końcowy może bezpośrednio poprawić wartości rzeczywiste projektu.

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

 
## <a name="correct-approved-expense-entries"></a>Popraw zatwierdzone wpisy wydatków

Wykonaj poniższe kroki, aby skorygować jeden lub więcej wpisów wydatków. 

1. W obszarze **Sprzedaż** w lewym okienku nawigacji w obszarze **Transakcje** wybierz pozycję **Zatwierdzone wydatki**.

2. Z listy **Zatwierdzone wydatki** wybierz projekt, który ma zostać poprawiony, a następnie wybierz pozycję **Koryguj wpisy**. Zostanie automatycznie utworzony nowy arkusz korekt z przypisanym typem **Korekta wydatku**. 

3. Na stronie **Nowy arkusz** wprowadź **Opis** poprawki i na karcie **Korekta wydatku** w sekcji **Nowe wartości dla wydatków** wybierz pola danych, które mają zostać poprawione dla wybranych wierszy wydatku. Można na przykład przypisać koszty do innego **Projektu** lub skorygować **Kategoria wydatków**, **Data wydatku** lub **Zasób, który można zarezerwować**.

4. Wybierz **Podgląd**. W oknie dialogowym wybierz **OK**. 

5. Sprawdź poprawki na karcie **Wiersze arkusza**. Można wyświetlić listę oryginalnych wartości rzeczywistych związanych z wybranymi wpisami wydatków, które zostały odwrócone, i poprawione odpowiadające utworzone wiersze.

6. Jeśli poprawione wartości zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**. W oknie dialogowym wybierz **OK.** Jeśli wartości nie są wyświetlane zgodnie z oczekiwaniami, wybierz pozycję **Anuluj**, aby powrócić do listy **Zatwierdzonych wydatków**. Powtórz kroki od 2 do 5. 

7. Po potwierdź zmianę, wróć do projektu lub projektów, które zostały zaktualizowane w celu wyświetlenia zmian.

8. Na stronie projektu na karcie **Wartości rzeczywiste** przejrzyj listę **Rzeczywisty widok skojarzony**. Oryginalne wpisy i poprawione wpisy są wyświetlane na liście.


## <a name="correct-approved-material-usage-logs"></a>Prawidłowe dzienniki użycia materiałów zatwierdzonych

Wykonaj poniższe kroki, aby poprawić jeden lub więcej wpisów dziennika użycia materiałów.

1. W obszarze **Sprzedaż** w lewym okienku nawigacji w obszarze **Transakcje** wybierz opcję **Wartości rzeczywiste**.

2. Na liście **Wartości** rzeczywiste użyj filtrów kolumn do wybrania klasy transakcji **Materiały**, tak aby wyświetlane są tylko wartości rzeczywiste dla materiałów. Użyj innych filtrów kolumn w celu dalszego ograniczenia wyświetlanych wartości rzeczywistych. Po znalezienie żądanego zestawu wartości rzeczywistych wybierz wartości rzeczywiste, a następnie wybierz opcję **Popraw pozycje**. Nowa poprawka jest tworzona automatycznie, a do pisania zostanie przypisany typ poprawki **materiałowej**.

3. Na stronie **Nowa strona główna** w polu **Opis** wprowadź opis poprawki. Następnie na karcie **Poprawianie materiałów** w sekcji **Nowe wartości** dla materiałów wybierz pola danych, które mają być poprawne dla wybranych wierszy materiałów. Można na przykład przypisać materiał do innego projektu lub poprawić produkt, datę materiałów lub podwykonawcę.

4. Wybierz **Podgląd**. W następnym oknie dialogowym wybierz **OK**.

5. Na karcie **Wiersze arkusza** sprawdź poprawki. Można wyświetlić listę oryginalnych wartości rzeczywistych powiązanych z wybranymi wpisami materiałów, które zostały wycofane, oraz poprawione odpowiednie wiersze, które zostały utworzone.

6. Jeśli poprawione wartości zostaną wyświetlone w sposób oczekiwany, wybierz opcję **Potwierdź**. W następnym oknie dialogowym wybierz **OK**. Jeśli wartości nie są oczekiwane, wybierz opcję **Anuluj**, aby powrócić do **listy Wartości rzeczywiste**. Następnie powtórz kroki od 2 do 5.

7. Po potwierdź zmianę, wróć do projektu lub projektów, które zostały zaktualizowane w celu wyświetlenia zmian.

8. Na stronie projektu na karcie **Wartości rzeczywiste** przejrzyj listę **Rzeczywisty widok skojarzony**. Oryginalne wpisy i poprawione wpisy są wyświetlane na liście.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
