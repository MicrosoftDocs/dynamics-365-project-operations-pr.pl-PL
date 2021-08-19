---
title: Szacowanie sprzedaży i kosztów projektu, gdy zasób z możliwością rezerwowania pełni wiele ról w projekcie
description: W tym temacie wyjaśniono, jak używać wymiarów cen do obsługi wyceny i szacowania kosztów dla zasobu, który pełni wiele ról w projekcie.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28a67e79b03dfbc38e9786350c931838ef27891a3d26787fc0334e0572528228
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990149"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Szacowanie sprzedaży i kosztów projektu, gdy zasób z możliwością rezerwowania pełni wiele ról w projekcie 

_**Ma zastosowanie do:** Project Operations dla scenariuszy opartych na zasobach/braku zapasów, wdrożenie w wersji uproszczonej — fakturowanie proforma dla transakcji i Project Operations dla scenariuszy magazynowych/opartych na produkcji_ 

W firmach opartych na projektach często jeden zasób musi pełnić wiele ról w projekcie. Każda rola może być wyceniana inaczej. Oznacza to, że czas tego samego zasobu w projekcie może uzyskać różne szacunki finansowe w zależności od rachunku i stawek kosztów dla każdej roli. Można skonfigurować wartości w rekordzie członka zespołu dla nazwanego zasobu z różnymi zastąpieniami dla każdego z zadań, do których jest przypisany członek zespołu.

W poniższym przykładzie pokazano, jak proste zastąpienie wartości umożliwia zasobowi pełnienie wielu ról w projekcie z różnymi stawkami kosztów i rozliczania.

## <a name="create-tasks"></a>Tworzenie zadań
Aby utworzyć zadania, należy dodać zadania, a także zadania zbiorcze, po czym należy przypisać zadanie przed dodaniem czasu trwania zadania. 

### <a name="add-tasks-and-summary-tasks"></a>Dodawanie zadań i zadań zbiorczych
Aby dodać zadanie, wykonaj następujące kroki.

1. Przejdź do obszaru **Projekty** i otwórz projekt, do którego chcesz dodać zadania.
2. Wybierz **Dodaj nowe zadanie**. Nazwij zadanie, a następnie naciśnij klawisz **Enter**.
3. Wprowadź nazwę kolejnego zadania, a następnie naciśnij klawisz **Enter**. Powtarzaj tę czynność, aż do wyświetlenia pełnej listy zadań.
3. Aby utworzyć wcięcia zadań w obszarze **Zadania sumaryczne**, zaznacz trzy pionowe kropki obok nazwy zadania, a następnie wybierz pozycję **Utwórz podzadanie**. 

  > [!TIP]
  > Aby zaznaczyć więcej niż jedno zadanie, zaznacz zadanie, naciśnij i przytrzymaj klawisz **Ctrl**, a następnie wybierz inne zadanie.
  >
  > Można również wybrać opcję **Promuj podzadanie**, aby przenieść zadania z obszaru **Zadania sumaryczne**.

### <a name="assign-tasks"></a>Przypisywanie zadań

Wykonaj następujące kroki, aby przypisać zadania.

1. W kolumnie **Przypisane do** dla zadania, wybierz ikonę osoby.
2. Wybierz członka zespołu z listy lub wprowadź tekst w celu wyszukania nazwy.

### <a name="add-task-duration-and-columns"></a>Dodawanie czasu trwania i kolumn zadań

Często najprostszym sposobem jest rozpoczęcie konstruowania projektu z czasem trwania. Wykonaj następujące kroki, aby dodać czas trwania zadania.

1. W kolumnie **Czas trwania** dla zadania wpisz liczbę dni, które Twoim zdaniem zajmie wykonanie zadania. Jeśli chcesz użyć innej jednostki czasu, wprowadź liczbę i wyraz **godziny**, **tygodnie** lub **miesiące**.
2. Jeśli chcesz, aby zadania były wyświetlane jako punkt kontrolny w kształcie rombu w widoku **osi czasu**, w kolumnie **Czas trwania** wprowadź **0 dni**.
3. Naciśnij klawisz **Enter**, aby przejść do pola **Czas trwania** następnego zadania i kontynuować wprowadzanie wartości czasu trwania.

  > [!NOTE]
  > Nie można wprowadzić czasu trwania dla zadań sumarycznych.

Aby podać więcej informacji, można dodać do projektu kolumny. W tym celu należy wybrać opcję **Dodaj kolumnę**. 

Aby uzyskać więcej informacji, zobacz [Tworzenie projektu](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Konfigurowanie roli i jednostki organizacyjnej dla ogólnego członka zespołu projektu
Wykonaj następujące kroki, aby skonfigurować rolę i jednostkę organizacyjną dla ogólnego członka zespołu.

1. Na stronie **Zadania** wybierz wiersz **Zadanie** dla **zadania A**. 
2. W obszarze **Przypisane do** wybierz pozycję **Dodaj zasób ogólny**. Spowoduje to otwarcie strony **szybkiego tworzenia członków zespołu**.
3. Na stronie **Szybkie tworzenie członków zespołu** określ atrybuty ogólnego członka zespołu, który będzie mógł wykonać to zadanie.
4. Wybierz odpowiednią rolę i jednostkę organizacyjną, a następnie wybierz pozycję **Zapisz i zamknij**. Ogólny członek zespołu zostaje utworzony i przypisany do tego zadania. 
5. Powtórz kroki 1–4 dla **Zadania B**. **Zadanie B** musi mieć jednak mieć inną rolę i jednostkę organizacyjną przypisaną do ogólnego członka zespołu niż **Zadanie A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Konfigurowanie roli i jednostki organizacyjnej dla zadania projektu
Wykonaj następujące kroki, aby skonfigurować rolę i jednostkę organizacyjną dla zespołu.

1. Po utworzeniu **zadania A** wybierz zadanie, a następnie wybierz ikonę **i**, aby otworzyć okienko **szczegółów zadania**. 
2. W okienku **szczegółów zadania** przewiń w dół i wybierz opcję **Wyświetl szczegóły**, aby otworzyć stronę **szczegółów zadania**.
3. Na stronie **szczegółów zadania** w polach **Rola** i **Jednostka organizacyjna** dodaj wartości, które są wymagane do wykonania tego zadania dla zasobu. 

  > [!NOTE]
  > Jeśli ten scenariusz zostanie zrealizowany przy użyciu danych pokazowych aplikacji Project Operations, wybierz pozycję **Lider ds. konsultingu** jako rolę, a następnie opcję **Fabrikam US** jako jednostkę organizacyjną.

4. Wybierz pozycję **Zadanie B**, a następnie wybierz zadanie.
5. Wybierz ikonę **i**, aby otworzyć okienko **szczegółów zadania**. 
6. W okienku **szczegółów zadania** przewiń w dół i wybierz opcję **Wyświetl szczegóły**, aby otworzyć stronę **szczegółów zadania**.
7. Na stronie **szczegółów zadania** w polach **Rola** i **Jednostka organizacyjna** dodaj wartości, które są wymagane w przypadku zasobu, który ma wykonać to zadanie. Wartości w polach **Rola** i **Jednostka organizacyjna** dla **Zadania B** muszą być inne niż w przypadku **zadania A**. 

  > [!NOTE]
  > Jeśli ten scenariusz zostanie zrealizowany przy użyciu danych pokazowych aplikacji Project Operations, wybierz pozycję **Technik sieciowy** jako rolę, a następnie opcję **Fabrikam US** jako jednostkę organizacyjną.

8. Zapisz i zamknij stronę **Szczegóły zadania**. 

## <a name="team-member-and-estimates-behavior"></a>Zachowanie członków zespołu i szacowań 
Aby zrozumieć zachowanie dotyczące siatki **członków zespołu** i oszacowań, należy wykonać następujące kroki.

1. W siatce **członków zespołu** wybierz dwóch ogólnych członków zespołu, a następnie wybierz opcję **Generuj zapotrzebowania**. Wygeneruje to wymagania zasobu. 
2. Wybierz wiersz członka zespołu dla roli **Lider ds. konsultingu**, a następnie wybierz pozycję **Rezerwuj**. Jest otwierana tablica harmonogramu z listą zasobów. Wybierz zasób, a następnie wybierz opcję **Rezerwuj** w celu zarezerwowania zasobu zgodnie z tym zapotrzebowaniem.
3. Wybierz wiersz członka zespołu dla roli **Technik sieciowy**, a następnie wybierz pozycję **Rezerwuj**. Jest otwierana tablica harmonogramu z listą zasobów. Wybierz ten sam zasób co powyżej, a następnie wybierz opcję **Rezerwuj** w celu zarezerwowania zasobu zgodnie z tym zapotrzebowaniem.

### <a name="team-member-grid"></a>Siatka członka zespołu 

W siatce **członków zespołu** dwa rekordy ogólnych członków zespołu są usuwane i zastępowane tylko jednym zasobem. Istnieje jeden zestaw wartości dla tego zasobu, który jest domyślnym zestawem wartości dla pól **Rola** i **Jednostka organizacyjna**.

Po rozwinięciu wiersza dla rekordu należącego do danego członka zespołu mogą zostać wyświetlone unikatowe przydziały rekordu członka zespołu dotyczące obu zadań. Każdy wiersz przypisania zawiera specyficzne wartości zadania dla pól **Rola** i **Jednostka organizacyjna**. 

### <a name="estimates-grid"></a>Siatka szacowań 

W siatce **szacowań** obydwa przypisania dotyczące tego samego zasobu są wyceniane w różny sposób. Przypisanie zasobu w **zadaniu A** ma cenę ustaloną za pomocą wartości atrybutu **Rola** o wartości **Lider ds. konsultingu**. Przypisanie tego samego zasobu w **zadaniu B** ma cenę ustaloną za pomocą wartości atrybutu **Rola** o wartości **Technik sieciowy**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]