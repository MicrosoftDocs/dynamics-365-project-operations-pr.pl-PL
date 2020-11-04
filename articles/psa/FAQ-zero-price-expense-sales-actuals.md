---
title: Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych wydatek sprzedaż?
description: Poniższe trzy kontrole ułatwią rozwiązanie problemu, dlaczego cena wynosi domyślnie 0 w wartościach rzeczywistych wydatek sprzedaż.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5840bda4f74c720bfcdc7f4e84c8f22e0c6163ec
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082032"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych wydatek sprzedaż?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

To często zadawane pytanie dotyczy wartości rzeczywistych wydatek, gdzie klasa transakcji jest ustawiona na Wydatek, a typ transakcji to Nierozliczona sprzedaż. Poniższe trzy kontrole ułatwią rozwiązanie problemu, dlaczego cena (stawka rozliczania) wynosi domyślnie 0 w wartościach rzeczywistych wydatek sprzedaż.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Kontrola 1: Określ cennik sprzedaży dla projektu

Znajdź projekt w polu projektu wartości rzeczywistych, a następnie przejdź na stronę projektu. Następnie przejdź do karty Sprzedaż. Na siatce Pozycje kontraktu projektu kliknij łącze w polu Kontrakt projektu. Zostanie otwarta strona Kontrakt projektu. Na stronie Kontrakt projektu przejdź do karty Cenniki projektu. Sprawdź, czy istnieje co najmniej jeden cennik dołączony w tym miejscu.

Jeśli żaden cennik nie został dołączony do siatki Cenniki projektu dla Kontraktu projektu wykonaj poniższe działania:

- Dołącz cennik do siatki Cenniki projektu. Cenniki jakie można tu dołączyć powinny mieć pole kontekstu ustawione na Sprzedaż, a pole waluty w cenniku powinno być zgodna z polem waluty w Kontrakt projektu. Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis wydatek, zatwierdź go, i sprawdź czy wartości rzeczywiste nierozliczonej sprzedaży ukazują prawidłową cenę.
- Jeśli istnieje jeden lub kilka cenników dołączonych w siatce Cenniki projektu dla Kontraktu projektu, przejdź do Kontroli 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Kontrola 2: Czy którekolwiek z cenników określonych powyżej są prawidłowe dla określonej daty w wartości rzeczywistej wydatek?

Aby Project Service rozważył cennik dla ceny domyślnej, ten cennik powinien być możliwy do zastosowanie w dniu wartości rzeczywistej wydatek sprzedaż. Sprawdź czy cenniki określone powyżej można zastosować:

- Zacznij od sprawdzenia, czy data rozpoczęcia i data zakończenia na karcie Ogólne dla dołączonych cenników nie są puste. Jeśli daty rozpoczęcia i zakończenia w cennikach określonych powyżej są puste, zidentyfikowałeś problem. 
- Zanotuj pole Data rozpoczęcia na wartościach rzeczywistych wydatek sprzedaż i sprawdź, czy jakiekolwiek określone cenniki można zastosować dla tej daty. Na przykład data wartości rzeczywistej wydatek powinna mieścić się w zakresie rozpoczęcia i daty zakończenia w cenniku. 
    - Jeśli nie istnieje cennik, który obejmuje tę datę w wartościach rzeczywistych wydatek sprzedaż, zidentyfikowałeś problem. Zmodyfikuj daty rozpoczęcia i zakończenia cennika, aby upewnić się, że cennik obejmuje datę wartości rzeczywistej wydatek. 
    - Jeśli istnieje jeden lub kilka cenników, które obejmują datę w wartościach rzeczywistych wydatek sprzedaż, zidentyfikowałeś problem. Możesz rozwiązać ten problem, edytując daty rozpoczęcia i zakończenia cenników tak, że istnieje tylko jeden cennik, który obejmuje datę wartości rzeczywistej wydatek. 
    - Jeśli istnieje tylko jeden cennik, który obejmuje tę datę wartości rzeczywistej wydatek, przejdź do Kontroli 3.
Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis wydatek, zatwierdź go, i sprawdź czy wartości rzeczywiste nierozliczonej sprzedaży ukazują prawidłową cenę.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Kontrola 3: Czy istnieje prawidłowa cena dla kategorii wydatek w odpowiednim cenniku projektu? 

Jeśli pomyślnie ukończyłeś Kontrolę 1 i Kontrolę 2, powinieneś posiadać już tylko jeden cennik projektu, który ma zastosowanie dla daty wartości rzeczywistej wydatek sprzedaż. Otwórz ten Cennik projektu i przejdź do karty Ceny kategorii. Upewnij się, że w siatce znajduje się wiersz przeznaczony dla określonej kategorii wydatków w wartościach rzeczywistych Wydatek.
 
- Jeśli nie ma wiersza, właśnie zlokalizowałeś problem. Utwórz wiersz w siatce Cena kategorii dla kategorii na wartości rzeczywistej wydatek. Gdy to zrobisz, ponownie utwórz wpis wydatek, zatwierdź go, i sprawdź czy wartość rzeczywista nierozliczona sprzedaż ukazuje prawidłową cenę. 
- Jeśli istnieje wiersz dla kategorii Wydatek w siatce Ceny kategorii, sprawdź, czy zawiera prawidłową cenę.

Aby zrozumieć, czym jest prawidłowa cena, skorzystaj z tych metod:

- Jeśli pole Metoda kalkulacji cen w wierszu Cena kategorii ustawiono na Po kosztach, to stawka jednostkowa w wartościach rzeczywistych Wydatek zostanie domyślnie ustawiona na wartość we wpisie Wydatek.
- Jeśli pole Metoda kalkulacji cen w wierszu Cennik kategorii ustawiono na wartość Procent narzutu, sprawdź, czy pole Procent zostało ustawione na prawidłową wartość. Stawka jednostkowa na wartości rzeczywistej Wydatek jest ustawiona domyślnie po zastosowaniu tego procentu narzutu dla ceny we wpisie Wydatek.
- Jeśli pole Metoda kalkulacji cen w wierszu Cennik kategorii ustawiono na wartość Cena jednostkowa, sprawdź, czy pole Cena zostało ustawione na prawidłową wartość. Stawka jednostkowa na wartości rzeczywistej Wydatek zostanie ustawiona domyślnie na określoną w polu Cena kwotę w walucie.

Jeśli ustawienia ceny dla kategorii wydatek nie są prawidłowe, właśnie zlokalizowałeś problem. Rozwiązaniem jest przeprowadzenie edycji wiersza Cena kategorii z prawidłową ceną dla kategorii wydatek zgodnie z regułami opisanymi powyżej. Gdy to zrobisz, ponownie utwórz wpis wydatek, zatwierdź go, a następnie sprawdź, czy wartość rzeczywista nierozliczona sprzedaż ukazuje prawidłową cenę.

Jeśli nadal nie widać prawidłowej ceny na wartości rzeczywistej wydatek sprzedaż, po wykonaniu powyższych trzech kontroli prześlij zgłoszenie prośby o pomoc techniczną.


