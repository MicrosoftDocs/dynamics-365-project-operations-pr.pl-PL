---
title: Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych czas sprzedaż?
description: Rozwiązywanie problemu, dlaczego ceny domyślnie wynoszą 0 w wartościach rzeczywistych czas sprzedaż.
author: rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 4cfa7c7a7c13c00e6f8411b7eae4d5abd1aaa7ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576513"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Dlaczego ceny domyślnie wynoszą zero w wartościach rzeczywistych czas sprzedaż?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

To często zadawane pytanie dotyczy wartości rzeczywistych, gdzie klasa transakcji jest ustawiona na Czas a typ transakcji to Nierozliczona sprzedaż. Poniższe trzy kontrole ułatwią rozwiązanie problemu, dlaczego cena (stawka rozliczania) wynosi domyślnie 0 w wartościach rzeczywistych czas sprzedaż.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Kontrola 1: Określ listę cen sprzedaży dla projektu

Znajdź projekt w polu projektu wartości rzeczywistych, a następnie przejdź na stronę projektu. Następnie przejdź do karty Sprzedaż a w siatce Pozycje kontraktu projektu, kliknij łącze w polu Kontrakt projektu. Zostanie otwarta strona Kontrakt projektu. Na stronie Kontrakt projektu przejdź do karty Cenniki projektu. Sprawdź, czy istnieje co najmniej jeden cennik dołączony w tym miejscu. Jeśli żadna lista cen nie została dołączona do siatki Cenniki projektu dla Kontraktu projektu, właśnie zidentyfikowałeś problem. Dołącz cennik do siatki Cenniki projektu. Cenniki jakie można tu dołączyć powinny mieć pole kontekstu ustawione na Sprzedaż, a pole waluty w cenniku powinno być zgodna z polem waluty w Kontrakt projektu. Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis godziny, zatwierdź go, i sprawdź czy wartości rzeczywiste nierozliczonej sprzedaży ukazują prawidłową cenę. 

Jeśli istnieje jeden lub kilka cenników dołączonych w siatce Cenniki projektu dla Kontraktu projektu, przejdź do następnej kontroli w dokumencie.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Kontrola 2: Czy którekolwiek z cenników określonych powyżej są prawidłowe dla określonej daty wartości rzeczywistych czas sprzedaż?

Aby Project Service rozważył cennik dla ceny domyślnej, ten cennik powinien być możliwy do zastosowanie w dniu wartości rzeczywistej czas sprzedaż. Sprawdź czy cenniki określone powyżej można zastosować:
- Sprawdź, czy data rozpoczęcia i zakończenia na karcie Ogólne dla dołączonych cenników nie są puste. Jeśli daty rozpoczęcia i zakończenia w cennikach określonych powyżej są puste, zidentyfikowałeś problem. 
- Zanotuj pole Data rozpoczęcia na wartościach rzeczywistych czas sprzedaż i sprawdź, czy jakiekolwiek określone cenniki można zastosować dla tej daty. Na przykład data wartości rzeczywistej czas sprzedaż powinna mieścić się w zakresie rozpoczęcia i daty zakończenia w cenniku. 
    - Jeśli nie istnieje cennik, który obejmuje tę datę w wartościach rzeczywistych czas sprzedaż, właśnie zidentyfikowałeś problem. Zmodyfikuj daty rozpoczęcia i zakończenia cennika, aby upewnić się, że cennik obejmuje datę wartości rzeczywistej czas sprzedaż. 
    - Jeśli istnieje jeden lub kilka cenników, które obejmują datę w wartościach rzeczywistych czas sprzedaż, właśnie zidentyfikowałeś problem. Możesz rozwiązać ten problem, edytując daty rozpoczęcia i zakończenia cenników tak, że istnieje tylko jeden cennik, który obejmuje datę wartości rzeczywistej czas sprzedaż. 
    - Jeśli istnieje tylko jeden cennik, który obejmuje tę datę wartości rzeczywistej czas sprzedaż, przejdź do kontroli 3.
Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis godziny, zatwierdź go, i sprawdź czy wartość rzeczywista czas sprzedaż ukazuje prawidłową cenę.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Kontrola 3: Czy istnieje cena w cenniku dla rozmiarów kalkulacji cen na wartości rzeczywistej czas sprzedaż?

Jeśli pomyślnie ukończyłeś Kontrolę 1 i Kontrolę 2, powinieneś posiadać już tylko jeden cennik, który ma zastosowanie dla daty wartości rzeczywistej czas sprzedaż. Otwórz ten Cennik i przejdź do karty Ceny ról. Upewnij się, że w siatce znajduje się wiersz przeznaczony dla wymiarów kalkulacji cen w wartościach rzeczywistych Czas sprzedaż.

Jeśli nie ma wiersza w siatce cena roli dla rozmiarów kalkulacji cen na wartości rzeczywistej czas sprzedaż, właśnie zlokalizowałeś problem. Utwórz wiersz w siatce Ceny ról dla rozmiarów kalkulacji cen na wartości rzeczywistej czas koszt. Gdy to skończysz, ponownie utwórz wpis czasu, zatwierdź go, i sprawdź czy wartość rzeczywista czas koszt ukazuje prawidłową cenę.

Jeśli nadal nie widać prawidłowej ceny na wartości rzeczywistej czas sprzedaż, po wykonaniu powyższych trzech kontroli prześlij zgłoszenie prośby o pomoc techniczną. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
