---
title: Wstępne rezerwowanie zasobu
description: W tym temacie zamieszczono informacje dotyczące sposobu wstępnego planowania, czyli inaczej wstępnego rezerwowania, członków zespołu projektu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: cb506a519dbc490ecdd579edf1e3fa5dd0153bdb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082137"
---
# <a name="soft-book-a-resource"></a>Wstępne rezerwowanie zasobu

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Można wstępnie zaplanować lub wstępnie zarezerwować zasób dla zespołu projektu, aby pokazać, że planujesz przypisać zasób do projektu. Wstępne rezerwacje nie zużywają dostępnej dyspozycyjności zasobu, więc możesz przypisać zarezerwowanych wstępnie członków zespołu do zadań projektu. Jednak ponieważ rezerwacja wstępna nie zużywa dyspozycyjności zasobu, wciąż można przeprowadzić ostateczną rezerwację zasobu dla innych zadań w tym samym okresie. Zasoby ogólne nie mogą być rezerwowane wstępnie, a rezerwacja wstępna nie może wypełnić żądania o zasób ogólny.

Wstępnie zarezerwowani członkowie zespołu projektu są wyświetlani na karcie **Zespół** na stronie **Projekt** , z godzinami zarezerwowanymi wstępnie przedstawionymi w kolumnie **Wstępnie zarezerwowane godziny** w widoku **Nazwani członkowie zespołu**. Wstępnie zarezerwowani członkowie zespołu są również wymienieni na tablicy harmonogramu. Ponieważ zostali oni zarezerwowani wstępnie, tablica harmonogramu nie wyświetla zużycia dyspozycyjności dla tych zasobów. Zarezerwowany wstępnie czas nie pojawia się na karcie **Uzgadnianie** , nie jest też wyświetlany w polu **Rozszerz rezerwacje** na karcie **Uzgadnianie** w tablicy harmonogramu. 

Istnieją dwa sposoby przeprowadzenia rezerwacji wstępnej członka zespołu dla projektu: bezpośrednio z tablicy harmonogramu lub poprzez dodanie członka zespołu na karcie **Zespół**. 

## <a name="soft-book-from-the-schedule-board"></a>Wstępna rezerwacja z tablicy harmonogramu
Wykonaj poniższe kroki, aby wstępnie zarezerwować zasób z tablicy harmonogramu. 

1. Otwórz tablicę harmonogramu, a następnie w panelu **Wymagania dotyczące rezerwacji** wybierz kartę **Projekt**.
2. Znajdź projekt, dla którego chcesz wstępnie zarezerwować zasób. Jeśli na liście znajduje się duża liczba projektów, kliknij nagłówek kolumny **Projekt** , a następnie użyj filtru w celu wyszukania jednego lub więcej projektów.
3. Zaznacz projekt, a następnie przeciągnij i upuść go w siatce czasu zasobu.
5. W panelu **Utwórz rezerwację zasobu** dostosuj daty początkową i końcową, w polu **Stan rezerwacji** ustaw wartość **Wstępna** , a następnie ustaw godziny. 
6. Kliknij opcję **Zarezerwuj**. Zasób jest teraz widoczny na karcie **Zespół** jako zasób projektu. W widoku **Nazwany członek zespołu** zobaczysz godziny zarezerwowane wstępnie w kolumnie **Wstępnie zarezerwowane godziny**.

> [!NOTE]
> Możesz teraz przypisać wstępnie zarezerwowane godziny do zadań na karcie **Harmonogram**. Na karcie **Uzgadnianie** zasób ukazuje deficyt rezerwacji względem przypisania zadania, ponieważ karta **Uzgadnianie** uwzględnia tylko rezerwacje ostateczne. Możesz użyć funkcji **Rozszerz rezerwacje** , aby dokonać rezerwacji ostatecznej zasobu i wyeliminować deficyt rezerwacji ostatecznych dla przypisań zasobów. Będziesz musiał ręcznie anulować rezerwacje wstępne dla zasobu za pomocą **Obsługa rezerwacji**.

## <a name="soft-book-on-the-team-tab"></a>Rezerwacja wstępna na karcie Zespół

Możesz dodać członków zespołu bezpośrednio na karcie **Zespół** , a następnie zmienić ich stan rezerwacji z **Ostateczna** na **Wstępna** za pomocą **Obsługa rezerwacji**. Po dodaniu członka zespołu w ten sposób rezerwacja będzie zawsze rezerwacją ostateczną, chyba że wybierzesz metodę alokacji jako **Brak**.

Aby korzystać z tej metody, należy wykonać następujące kroki:

1. Na stronie **Projekt** na karcie **Zespół** kliknij opcję **Nowy**.
2. Wybierz zasób, który można zarezerwować, rolę oraz daty Od/Do.
3. Wybierz metodę przydziału inną niż **Brak**.
4. Wybierz pozycję **Zapisz**. Zobaczysz zasób na siatce i godziny w kolumnie **Ostatecznie zarezerwowane godziny**.
5. Obsługuj rezerwacje zasobu, wybierając **Obsługa rezerwacji**.
6. Po otwarciu tablicy harmonogramu rozwiń zasób, aby wyświetlić dla niego rezerwacje. Zobaczysz rezerwację wskazaną jako **Ostateczna**.
7. Kliknij prawym przyciskiem myszy rezerwację, a następnie w obszarze **Zmień stan** wybierz kolejno opcje **Zarezerwuj wstępnie** \> **Wstępna**. Stan rezerwacji to teraz **Wstępna**.
8. Po zamknięciu tablicy harmonogramu zobaczysz, że godziny dla zasobu zostały przeniesione z kolumny **Godziny zarezerwowane ostatecznie** do **Godziny zarezerwowane wstępnie** na siatce karty **Zespół** w widoku **Nazwani członkowie zespołu**.

> [!NOTE]
> Gdy korzystasz z **Obsługa rezerwacji** , aby zmienić stan z **Ostateczna** na **Wstępna** , to jeśli ostatecznie zarezerwujesz zasób dla zespołu, a następnie przypiszesz temu zasobowi zadania, przypisania zadań do zasobu zostaną zachowane. Na karcie **Uzgadnianie** zasób będzie jednak posiadał deficyt rezerwacji, ponieważ tylko rezerwacje ostateczne są brane pod uwagę podczas uzgodnień rezerwacja a przypisanie. Możesz użyć funkcji **Rozszerz rezerwacje** na karcie **Uzgadnianie** , aby dokonać rezerwacji ostatecznej zasobu i wyeliminować deficyt rezerwacji ostatecznych dla przypisań zasobów. Będzie trzeba anulować rezerwacje wstępne dla zasobu za pomocą **Obsługa rezerwacji**.

Gdy jesteś gotowy, aby zmienić zasób członka zespołu zarezerwowany wstępnie na członka zespołu zarezerwowanego ostatecznie, wykonaj następujące czynności:

1. Na tablicy harmonogramu rozwiń zasób, aby wyświetlić dla niego rezerwacje. Zobaczysz rezerwację oznaczoną jako **Wstępna**.
2. Kliknij prawym przyciskiem myszy rezerwację, a następnie w obszarze **Zmień stan** wybierz kolejno opcje **Zarezerwuj ostatecznie** \> **Ostateczna**. Stan rezerwacji to teraz **Ostateczna**.
3. Po zamknięciu tablicy harmonogramu, powrocie do projektu i otwarciu karty **Zespół** zobaczysz, że godziny dla zasobu zostały przeniesione z kolumny **Godziny zarezerwowane wstępnie** do kolumny **Godziny zarezerwowane ostatecznie** na karcie **Zespół** w widoku **Nazwani członkowie zespołu**. Jeśli zasób został przypisany do zadań, nie będą one już ukazywać deficytu rezerwacji na karcie **Uzgadnianie** , gdyż ich rezerwacje są już rezerwacjami ostatecznymi.

