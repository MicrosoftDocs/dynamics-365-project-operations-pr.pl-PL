---
title: Tworzenie przypisanych zasobów
description: W tym artykule przedstawiono informacje o tworzeniu przypisań zasobów ogólnych i nazwanych.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812007"
---
# <a name="create-resource-assignments"></a>Tworzenie przypisanych zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Przydział zasobu jest bezpośrednim skojarzeniem członka zespołu projektu z zadaniem węzła liścia. Ten artykuł zawiera informacje na temat różnych sposobów przypisywania zasobów.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Tworzenie ogólnego członka zespołu za pośrednictwem przypisania zadania


W trakcie tworzenia ogólnego członka zespołu za pomocą przydziału zadania, można utworzyć symbol zastępczy lub zasób ogólny. Ten zasób ogólny opisuje cechy nazwanego zasobu, który ma być ostatecznie wykorzystany do pracy nad zadaniami. Następnie generujesz wymaganie (lub przesyłasz zgłoszenie korzystające z tego wymagania), które jest używane do wyszukiwania i rezerwowania nazwanego zasobu.

1. W siatce Harmonogram dla zadania wybierz ikonę Zasób w komórce **zasobu**.
2. Wpisz nazwę, jaka ma stać się nazwą zasobu zastępczego. Na przykład Menedżer programu.
3. Kliknij przycisk **Utwórz**, a następnie w polu **Szybkie tworzenie członka zespołu projektu** ustaw rolę zasobu ogólnego.
4. Dalej przypisuj zadania do tego zasobu zastępczego, wybierając zasób w oknie **Selektor zasobów** dla zadania. Zasoby są wyświetlane w obszarze **Członkowie zespołu**.
5. Po zakończeniu przypisywania zasobu ogólnego wybierz zasób ogólny na karcie **Zespół**, wybierz zasób ogólny, a następnie wybierz opcję **Generuj wymaganie**, aby utworzyć wymaganie zasobu dla zasobu ogólnego.
6. Wybierz **Zarezerwuj** dla zasobu ogólnego, a w następnym kroku będziesz mógł użyć tablicy Harmonogramu, aby wyszukać i zarezerwować rzeczywisty zasób. Można również przesłać wymagań do spełnienia przez Menedżera zasobów.
7. Gdy ogólny zasób jest w pełni zrealizowany z nazwanym zasobem, ogólny zasób jest usuwany z zespołu. (Częściowe wypełnienie zasobów nie będzie skutkować przypisaniem zasobu.) Przypisania zadania dla zasobu ogólnego są przypisane do nazwanego zasobu, który spełnij wymagania zasabu dla zasobu ogólnego.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Przypisywanie nazwanego zasobu z listy wszystkich zasobów, które można zarezerwować

Możesz użyć pola wyszukiwania w oknie **Selektor zasobów**, aby wyszukać wszystkie zasoby możliwe do zarezerwowania i przypisać je do zadania węzła liścia. Zasoby przypisane w ten sposób zostaną dodane do zespołu bez żadnych rezerwacji. Jest to sposób podobny do dodawania członka zespołu i wybierania opcji **Brak** jako metody alokacji. Zasoby będą wyświetlane na kartach **Zespół**, **Uzgadnianie**, oraz **Przypisanie zasobów** jako zasoby z przydziałami i deficytem rezerwacji. Zarezerwuj je, jeśli chcesz użyć ich dostępności.

1. Z siatki zadań, tablicy lub osi czasu przejdź do komórki **Przypisane do**.
2. W polu wyszukiwania rozpocznij wpisywanie nazwy. Wyniki wyszukiwania nazwy są wyświetlane w oknie **Selektor zasobów** w obszarze **Inne zasoby**.
3. Wybierz zasób, który chcesz przypisać do zadania, lub wybierz nazwę zasobu w obszarze **Innych zasobów zespołu**.

## <a name="editing-resource-assignment-contours"></a>Edytowanie przypisań do zasobów

Domyślnie, gdy zasoby są przypisywane do zadania w harmonogramie, ich nakłady są liniowo dystrybuowane do każdego zasobu na podstawie godzin pracy tego zasobu i trybu harmonogramu projektu. Menedżer projektu może użyć siatki przypisywania zasobów w celu uściślenia szacowania nakładów pracy każdego zasobu przypisanego do jednego lub wielu zadań na różnych skalach czasu. Funkcja ta ułatwia menedżerom projektów tworzenie bardziej dokładnych szacowań kosztów i sprzedaży, które są oparte na przypisaniach zasobów, które są generowane, gdy zasób jest przypisany do zadania. Dodatkowo menedżerowie projektów mogą łatwiej odzwierciedlić zapotrzebowanie na zasoby wymagane do budowania popytu w wymaganiach zasobów.

### <a name="navigation"></a>Nawigacja

Aby uzyskać dostęp do siatki edycji konturów, menedżer projektu najpierw wybiera kartę **Zadania** na stronie głównej projektu, a następnie wybiera kartę **Przypisania**.

![Karta Przypisania na karcie Zadania głównej strony projektu.](media/AssignmentGrid.png)

Siatka obsługuje dwa sposoby grupowania: **grupowanie według zasobu** i **grupowanie według zadania**. W przeciwieństwie do widoku siatki, kolumn nie można konfigurować. Jedyne widoczne kolumny to **Przypisane do**, **Nazwa zadania**, **Początek przypisania**, **Zakończenie przypisania** i **Nakład pracy przypisania**.

Kiedy siatka jest początkowo renderowana, rozpoczyna się ona od najwcześniejszego przypisania. Jeśli harmonogram nie zawiera przypisań, które mają nakład pracy, siatka będzie pusta i nie będzie niczego renderować.

![Pusta siatka przypisania.](media/emptyassignmentgrid.png)

Aby wyświetlić widoki konturów i różne skale czasowe, dostępna jest także siatka przypisywania zasobów tylko do odczytu oraz siatka uzgadniania zasobu.

### <a name="resource-calendars"></a>Kalendarze zasobu

Możliwość edycji konturu w określonym dniu jest regulowane przez dni robocze zasobu, co jest odzwierciedlane w kalendarzu. Jeśli komórka jest wyłączona dla danego zasobu, ten zasób nie ma w tym okresie dni roboczych.

Konturów zasobu mogą wykraczać poza bieżące daty rozpoczęcia i zakończenia przypisanego zadania. Jeśli data zakończenia zadania zostanie zaktualizowana w taki sposób, aby nastąpi ona po najnowszej dacie zakończenia zadania lub najwcześniejszej dacie rozpoczęcia zadania, data zakończenia lub data rozpoczęcia zadania zostaną odpowiednio zmienione. Jeśli jednak przypisanie zostanie zaktualizowane w taki sposób, że jest ono wcześniejsze niż data rozpoczęcia zadania połączonego z zadaniem, aktualizacja zakończy się niepowodzeniem, ponieważ przypisanie spowoduje uruchomienie zadania przed jego zakończeniem i takie zachowanie nie jest obecnie obsługiwane.

### <a name="co-authoring"></a>Współtworzenie

Zmiany w siatce przypisania zasobów są automatycznie odzwierciedlane we wszystkich skojarzonych widokach, w tym w wykresie, osi czasu, tablicy i widokach siatki. Jeśli projekt jest przeglądany jednocześnie przez wielu użytkowników, zmiany wprowadzone przez jednego użytkownika zostaną odzwierciedlone w siatce. I odwrotnie, zmiany wprowadzone w siatce przypisania zasobów będą wyświetlane dla wszystkich innych użytkowników wyświetlających projekt w tej samej sesji.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
