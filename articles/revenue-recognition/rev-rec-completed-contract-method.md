---
title: Zarządzanie szacowaniami przychodów
description: W tym artykule przedstawiono informacje na temat sposobu pracy z szacowania przychodów dla projektów.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 051535ce8dd4997a923b1511d242638361076979
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928491"
---
# <a name="manage-revenue-estimates"></a>Zarządzanie szacowaniami przychodów

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Możesz tworzyć, obliczać, księgować, cofać lub eliminować szacowania przychodów. Można to zrobić ręcznie lub za pomocą procesu okresowego. W tym artykule przedstawiono informacje na temat sposobu pracy z szacowania przychodów dla projektów.

### <a name="manage-revenue-estimates-manually"></a>Ręczne zarządzanie szacowaniami przychodów

Na stronie projektu szacowania przychodów o stałej cenie lub na stronie **Zapytanie o oszacowanie** (**Zarządzanie projektami i księgowanie** > **Raporty i zapytania** > **Zapytania i raporty dotyczące szacowań**) wybierz pozycję **Szacowania**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Zarządzanie szacowaniami przychodów przy użyciu procesu okresowego

Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Okresowe** > **Szacowania** i wybierz odpowiedni proces.

## <a name="create-a-revenue-estimate"></a>Tworzenie szacowania przychodów

Wykonaj następujące kroki, aby utworzyć szacowanie przychodów. 

1. Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Okresowe** > **Szacowania**.
2. Wybierz **Nowy**. Na stronie **Tworzenie szacowania** wybierz następujące parametry:

   - **Kod okresu**: Ten kod wskazuje, jak często szacowania są księgowane.
   - **Data szacowania**: data przetwarzania szacowania.
   - **Ciągłe**: zaznacz to pole wyboru, aby tworzyć szacowania tylko wtedy, gdy szacowania zostały zaksięgowane w poprzednim okresie lub jeśli szacowanie jest pierwszym utworzonym szacowaniem. Jeśli to pole nie jest zaznaczone, szacowania są tworzone, nawet jeśli nie zostały zaksięgowane w poprzednim okresie.
   - **Metoda kosztu wykonania**: zdefiniuj sposób szacowania pozostałej pracy projektowej. Aby uzyskać więcej informacji, zobacz [Metoda kosztu wykonania](cost-complete-methods.md).
   - **Metoda wykonania**: wybierz metodę wykonania spośród następujących opcji:
     - **Automatycznie**: procent wykonania jest obliczany automatycznie, na podstawie wierszy kosztów uwzględnionych w obliczeniach. Szablon kosztu definiuje wiersze kosztu do uwzględnienia.
     - **Ręcznie**: procent wykonania jest równy procentowi wykonania dla ostatniego oszacowania. Po utworzeniu szacowania można zmienić opcję **Obliczanie ręczne** na stronie **Szacowania**.
     - **Z szablonu kosztów**: połączenie metod automatycznych i ręcznych. Ta opcja jest ustawiana jako automatyczna lub ręczna, w zależności od wartości domyślnej w szablonie kosztu.
   - **Model prognozy**: wybierz model prognozy dla szacowania.
   - **Wydrukuj listę oszacowań**: utwórz i pokaż listę szacowań. Lista zawiera stan bieżącej funkcji. W raporcie można wydrukować ostrzeżenia dotyczące szacowania. Następujące warunki powodują, że ostrzeżenia pojawiają się na liście szacowań:
     - Procent wykonania większy niż 100 procent.
     - Procent wykonania mniejszy niż zero procent.
     - Kwota ujemna w kolumnie **Do wykonania**.
     - Szacowanie bez odpowiedniej kwoty kontraktu.
     - Szacowanie bez dołączonego szacowania kosztów.
   - **Pokaż dziennik informacyjny**: wybierz tę opcję, aby otrzymać komunikat zawierający informacje o szacowanych projektach, które zostały przetworzone podczas uruchamiania zadania.


## <a name="post-wip-or-accruals"></a>Księgowanie PWT lub naliczeń

Ocenione szacowania są utrzymywane, zmniejszane lub zwiększane. Następnie można zaksięgować PWT podczas pracy przy użyciu zasad oceny **kontraktu ukończonego** lub zaksięgować naliczenia podczas pracy z zasadami oceny **Procent ukończenia**.
  
Stan okresu szacowania zmienia się z **Utworzono** na **Zaksięgowano**.

## <a name="reverse-wip-or-accruals"></a>Odwracanie PWT lub naliczeń

Użyj opcji odwracania, aby uznać już zaksięgowane PWT lub naliczenia, a następnie utworzyć szacowania dla okresu.

> [!NOTE]
> Aby odwrócić okres, który znajduje się między innymi okresami, odwróć niezbędne okresy szacowania, a następnie ponownie je zaksięguj. Ponieważ wszystkie kolejne okresy zależą od szacowań z poprzedniego okresu, nie pomijaj żadnych okresów.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Eliminowanie szacowania projektu i kończenie projektu

Ostatnim krokiem w procesie szacowania jest wyeliminowanie szacowania projektu i zakończenie projektu o stałej cenie, gdy procent ukończenia osiągnie 100 procent.

Po uruchomieniu eliminacji występują następujące sytuacje:

- W przypadku projektu o stałej cenie z ukończonym kontraktem wartości PWT są czyszczone z kont bilansów i księgowane na kontach zysków i strat.
- W przypadku projektu o stałej cenie z procentem ukończenia naliczenia są usuwane z kont zysków i strat.

Szacowanie zmienia stan na **Wyeliminowane**.

> [!NOTE]
> W szczególnych przypadkach wartość procentowa może przekraczać 100 procent. W takim przypadku należy zmniejszyć procent ukończenia przy użyciu opcji **Ustaw metodę kosztu wykonania na zero**, aby osiągnąć 100 procent.

## <a name="reverse-elimination"></a>Wycofanie eliminacji

1. Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Okresowe** > **Szacowania** > **Wycofanie eliminacji**. 
2. W okienku akcji na karcie **Proces** w grupie **Obsługa** wybierz pozycję **Szacuj**. 
3. Wybierz pozycję **Wycofanie eliminacji**.

Ta strona służy do wycofywania wszystkich eliminacji z określoną datą szacowania i stanem szacowania **Wyeliminowane**. Stan transakcji zmienia się po wybraniu odpowiednich pól.

Spowoduje to również automatyczną zmianę stanu projektu na **W trakcie przetwarzania**, jeśli etap projektu jest ustawiony na ukończenie. Stan szacowania okresu projektu zmienia się z powrotem na **Zaksięgowane**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]