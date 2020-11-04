---
title: Tworzenie przypisanych zasobów
description: W tym temacie zamieszczono informacje dotyczące tworzenia ogólnych i nazwanych przydziałów zasobów.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081925"
---
# <a name="create-resource-assignments"></a>Tworzenie przypisanych zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Przydział zasobu jest bezpośrednim skojarzeniem członka zespołu projektu z zadaniem węzła liścia. W tym temacie zamieszczono informacje dotyczące różnych sposobów przypisywania zasobów.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Tworzenie ogólnego członka zespołu za pośrednictwem przypisania zadania


W trakcie tworzenia ogólnego członka zespołu za pomocą przydziału zadania, można utworzyć symbol zastępczy lub zasób ogólny. Ten zasób ogólny opisuje cechy nazwanego zasobu, który ma być ostatecznie wykorzystany do pracy nad zadaniami. Następnie generujesz wymaganie (lub przesyłasz zgłoszenie korzystające z tego wymagania), które jest używane do wyszukiwania i rezerwowania nazwanego zasobu.

1. W siatce Harmonogram dla zadania wybierz ikonę Zasób w komórce **zasobu**.
2. Wpisz nazwę, jaka ma stać się nazwą zasobu zastępczego. Na przykład Menedżer programu.
3. Kliknij przycisk **Utwórz** , a następnie w polu **Szybkie tworzenie członka zespołu projektu** ustaw rolę zasobu ogólnego.
4. Dalej przypisuj zadania do tego zasobu zastępczego, wybierając zasób w oknie **Selektor zasobów** dla zadania. Zasoby są wyświetlane w obszarze **Członkowie zespołu**.
5. Po zakończeniu przypisywania zasobu ogólnego wybierz zasób ogólny na karcie **Zespół** , wybierz zasób ogólny, a następnie wybierz opcję **Generuj wymaganie** , aby utworzyć wymaganie zasobu dla zasobu ogólnego.
6. Wybierz **Zarezerwuj** dla zasobu ogólnego, a w następnym kroku będziesz mógł użyć tablicy Harmonogramu, aby wyszukać i zarezerwować rzeczywisty zasób. Można również przesłać wymagań do spełnienia przez Menedżera zasobów.
7. Kiedy zasób ogólny zostanie całkowicie zrealizowany (częściowe wypełnienie zasobów nie będzie skutkować przypisaniem zasobu) za pomocą nazwanego zasobu, zasób ogólny jest usuwany z zespołu. Przydziały zadania dla zasobu ogólnego są przypisywane do zasobu nazwanego, który spełnił zapotrzebowanie na zasoby zasobu ogólnego.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Przypisywanie nazwanego zasobu z listy wszystkich zasobów, które można zarezerwować

Możesz użyć pola wyszukiwania w oknie **Selektor zasobów** , aby wyszukać wszystkie zasoby możliwe do zarezerwowania i przypisać je do zadania węzła liścia. Zasoby przypisane w ten sposób zostaną dodane do zespołu bez żadnych rezerwacji. Jest to sposób podobny do dodawania członka zespołu i wybierania opcji **Brak** jako metody alokacji. Zasoby będą wyświetlane na kartach **Zespół** , **Uzgadnianie** , oraz **Przypisanie zasobów** jako zasoby z przydziałami i deficytem rezerwacji. Zarezerwuj je, jeśli chcesz użyć ich dostępności.

1. Z siatki zadań, tablicy lub osi czasu przejdź do komórki **Przypisane do**.
2. W polu wyszukiwania rozpocznij wpisywanie nazwy. Wyniki wyszukiwania nazwy są wyświetlane w oknie **Selektor zasobów** w obszarze **Inne zasoby**.
3. Wybierz zasób, który chcesz przypisać do zadania, lub wybierz nazwę zasobu w obszarze **Innych zasobów zespołu**.
