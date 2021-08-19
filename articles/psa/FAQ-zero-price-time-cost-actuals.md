---
title: Dlaczego cena domyślna wynosi zero w wartościach rzeczywistych czas koszt?
description: Rozwiązywanie problemu, dlaczego cena domyślna wynosi 0 w wartościach rzeczywistych czas koszt.
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
ms.openlocfilehash: e1f81268c894e2ff5d607d8008876c84f7eafdf05f8b1f3212263a5dfa89b69d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996989"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Dlaczego cena domyślna wynosi zero w wartościach rzeczywistych czas koszt?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

To często zadawane pytanie dotyczy wartości rzeczywistych, gdzie klasa transakcji jest ustawiona na Czas a typ transakcji to Koszt. Poniższe trzy kontrole ułatwią rozwiązanie problemu, dlaczego cena wynosi domyślnie 0 w wartościach rzeczywistych koszt czasu.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Kontrola 1: Określ listę kosztów własnych dla projektu

Znajdź projekt w polu projektu wartości rzeczywistych, a następnie przejdź na stronę projektu. Kliknij łącze jednostki kontraktującej w polu. Na stronie Jednostka kontraktująca sprawdź, czy jednostka kontraktująca posiada cennik w siatce kosztów własnych.

Jeśli istnieje więcej niż jeden cennik, zidentyfikowałeś problem. Usługa Project Service obsługuje tylko jeden cennik dla jednostki organizacyjnej. Usuń wszystkie cenniki z tej encji i zostaw tylko jeden cennik dołączony w siatce Koszt własny jednostki organizacyjnej.

Jeśli żaden cennik nie jest dołączony do jednostki organizacyjnej, sporządź notatkę o walucie jednostki organizacyjnej. Przejdź do usługi Project Service, a następnie do Parametry i otwórz kartę Cenniki. Sprawdź, czy istnieją cenniki z kontekstem ustawionym na Koszt i walutę, która odpowiada walucie jednostki organizacyjnej.
 
Jeśli nie istnieją cenniki, które spełniają te kryteria, znalazłeś problem. Upewnij się, że posiadasz co najmniej jeden cennik, którego kontekst ustawiono na Koszt, i którego waluta odpowiada walucie jednostki organizacyjnej.

Jeśli istnieje więcej niż jeden cennik zgodny z tymi kryteriami, czytaj dalej ten dokument, aby przeprowadzić więcej kontroli.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Kontrola 2: Czy którekolwiek z cenników określonych powyżej są prawidłowe dla określonej daty wartości rzeczywistych czas koszt?

Aby Project Service rozważył cennik dla ceny domyślnej, ten cennik powinien być możliwy do zastosowania w dniu wartości rzeczywistej czasu koszt. Sprawdź czy cenniki określone powyżej można zastosować:

- Sprawdź, czy data rozpoczęcia i zakończenia na karcie Ogólne dla dołączonych cenników nie są puste. Jeśli daty rozpoczęcia i zakończenia w cennikach określonych powyżej są puste, zidentyfikowałeś problem. 
- Zanotuj pole daty rozpoczęcia na wartościach rzeczywistych czas koszt i sprawdź, czy jakiekolwiek określone cenniki można zastosować dla tej daty. Na przykład data wartości rzeczywistej czas koszt powinna mieścić się w zakresie rozpoczęcia i daty zakończenia w cenniku. 
    - Jeśli nie istnieje cennik, który obejmuje tę datę w wartościach rzeczywistych czas koszt, zidentyfikowałeś problem. Zmodyfikuj daty rozpoczęcia i zakończenia cennika, aby upewnić się, że cennik obejmuje datę wartości rzeczywistej czas koszt. 
    - Jeśli istnieje jeden lub kilka cenników, które obejmują datę w wartościach rzeczywistych czas koszt, zidentyfikowałeś problem. Możesz rozwiązać ten problem, edytując daty rozpoczęcia i zakończenia cenników tak, że istnieje tylko jeden cennik, który obejmuje datę wartości rzeczywistej czas koszt. 
    - Jeśli istnieje tylko jeden cennik, który obejmuje datę wartości rzeczywistej czas koszt, przejdź do następnej kontroli w dokumencie.
Po wprowadzeniu niezbędnych poprawek ponownie utwórz wpis godziny, zatwierdź go, i sprawdź czy wartości rzeczywiste czas koszt ukazują prawidłową cenę.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Kontrola 3: Czy istnieje cena w cenniku dla rozmiarów kalkulacji cen w wartościach rzeczywistych czas koszt?

Jeśli pomyślnie ukończyłeś Kontrolę 1 i Kontrolę 2, powinieneś posiadać już tylko jeden cennik, który ma zastosowanie dla daty wartości rzeczywistej czas koszt. Otwórz ten Cennik i przejdź do karty Ceny ról. Upewnij się, że w siatce znajduje się wiersz przeznaczony dla wymiarów kalkulacji cen w wartościach rzeczywistych czas koszt.

Jeśli nie istnieje wiersz w siatce ceny roli dla kalkulacji cen na wartości rzeczywistej czas koszt, właśnie zidentyfikowałeś problem. Utwórz wiersz w siatce Ceny ról dla rozmiarów kalkulacji cen na wartości rzeczywistej czas koszt. Gdy to skończysz, ponownie utwórz wpis czasu, zatwierdź go, i sprawdź czy wartości rzeczywiste czas koszt ukazują prawidłową cenę.
 
Jeśli nadal nie widać prawidłowej ceny na wartości rzeczywistej czas koszt, po wykonaniu powyższych trzech kontroli prześlij zgłoszenie prośby o pomoc techniczną.





[!INCLUDE[footer-include](../includes/footer-banner.md)]