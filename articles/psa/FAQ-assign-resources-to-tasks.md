---
title: Przypisywanie zasobu do zadania
description: W tym temacie zamieszczono informacje dotyczące sposobu przypisywania zasobów do zadań.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150006"
---
# <a name="assign-a-resource-to-a-task"></a>Przypisywanie zasobu do zadania

[!include [banner](../includes/psa-now-project-operations.md)]

Istnieją trzy sposoby przypisywania zasobu do zadania w programie Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Zarezerwuj zasób jako członek zespołu, a następnie przypisz zasób do zadania

Możesz dodać zasób do zespołu projektu, a następnie przypisać zasób do zadań w harmonogramie projektu.

1. Na karcie **Członek zespołu** dodaj nowego członka zespołu, wybierając **Nowy**. 

2. Otworzy się panel **Szybkie tworzenie członków zespołu**, gdzie można wybrać nazwę zasobu, który można zarezerwować, i ustawić rolę. 

    Wybierz jedną z następujących metod alokacji, aby zarezerwować zasób:

    - **Pełna dyspozycyjność** rezerwuje pełną dyspozycyjność zasobu dla określonych dat Od/Do.
    - **Dyspozycyjność procentowa** rezerwuje zasób procentowo dla dyspozycyjności zasobu dla określonych dat Od/Do.
    - **Według godzin — rozłóż równomiernie** rezerwuje zasób na określoną liczbą godzin, rozkładając je równomiernie w ciągu dnia dla określonych dat Od i Do.
    - **Według godzin — Najwięcej na początku** rezerwuje zasób na określoną liczbą godzin, kładąc nacisk na godziny początkowe w ciągu dnia dla określonych dat Od/Do.
    - **Brak** dodaje zasób do zespołu, ale nie tworzy żadnych rezerwacji, które absorbują ich dyspozycyjność.

3. W siatce **Harmonogram** dla zadania wybierz ikonę **Zasób** w komórce zasobu, a następnie w obszarze **Członkowie zespołu** wybierz członka zespołu, który został właśnie dodany. 

> [!NOTE]
> Na kartach **Członek zespołu** i **Uzgadnianie** zasób ukazuje zarezerwowane i przypisane godziny. Godziny powinny, ale nie muszą być takie same, ponieważ rezerwacje i przypisania nie są ściśle powiązane. Karta **Uzgadnianie** przedstawia szczegóły, gdy są one inne, np. jeśli przypiszesz do zasobu więcej godzin, niż zarezerwowano. W razie potrzeby można skorygować informacje, rozszerzając rezerwacje zasobu albo zmieniając przypisanie.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Tworzenie ogólnego członka zespołu za pośrednictwem przypisania zadania

Podczas tworzenia ogólnego członka zespołu poprzez przypisanie zadania tworzysz zasób zastępczy lub zasób ogólny, który opisuje cechy zasobu nazwanego, który ma ostatecznie pracować nad zadaniami. Następnie generujesz wymaganie (lub przesyłasz zgłoszenie korzystające z tego wymagania), które jest używane do wyszukiwania i rezerwowania nazwanego zasobu.

1. W siatce **Harmonogram** dla zadania wybierz ikonę **Zasób** w komórce zasobu.

2. Wpisz nazwę, jaka ma stać się nazwą zasobu zastępczego. Na przykład Menedżer programu.

3. Kliknij przycisk **Utwórz**, a następnie w polu **Szybkie tworzenie członka zespołu projektu** ustaw rolę zasobu ogólnego.

4. Możesz nadal przypisywać zadania do tego zasobu zastępczego, wybierając zasób w oknie **Selektor zasobów** dla zadania. Są one wyświetlane w obszarze **Członkowie zespołu**.

5. Po zakończeniu przypisywania zasobu ogólnego wybierz zasób ogólny na karcie **Zespół**, a następnie wybierz opcję **Generuj wymaganie**, aby utworzyć wymaganie zasobu dla zasobu ogólnego.

6. Wybierz **Zarezerwuj** dla zasobu ogólnego. Następnie możesz użyć tablicy harmonogramu, aby wyszukać i zarezerwować zasób. Można również przesłać wymagań do spełnienia przez Menedżera zasobów.

7. Gdy zasób ogólny jest zrealizowany przez zasób nazwany, zasób ogólny jest usuwany z zespołu a przypisania zadań dla zasobu ogólnego są przypisywane do zasobu nazwanego, który zrealizował wymaganie zasobu dla zasobu ogólnego.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Przypisywanie nazwanego zasobu z listy wszystkich zasobów, które można zarezerwować

Możesz użyć pola wyszukiwania w oknie **Selektor zasobów**, aby wyszukać wszystkie zasoby możliwe do zarezerwowania i przypisać je do zadania.

Zasoby przypisane w ten sposób zostaną dodane do zespołu bez żadnych rezerwacji. Jest to sposób podobny do dodawania członka zespołu i wybierania opcji Brak jako metody alokacji. Zasoby będą wyświetlane na kartach **Zespół** i **Uzgadnianie** jako zasoby z przydziałami i deficytem rezerwacji. Zarezerwuj je, jeśli chcesz użyć ich dostępności.

1. W siatce **Harmonogram** dla zadania wybierz ikonę **Zasób** w komórce zasobu.

2. Zacznij wpisywać nazwę. Wyniki wyszukiwania nazwy są wyświetlane w oknie **Selektor zasobów** w obszarze **Inne zasoby**.

3. Zaznacz zasób, który chcesz przypisać do zadania.



[!INCLUDE[footer-include](../includes/footer-banner.md)]