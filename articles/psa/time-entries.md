---
title: Tworzenie wpisów czasu
description: W tym temacie zamieszczono informacje dotyczące tworzenia wpisów czasu.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 0d0e21d0964788564d3db9173c3a0b3378cd0049b4455a23ccc1bccd1c21d9e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990419"
---
# <a name="create-time-entries"></a>Tworzenie wpisów czasu

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

W poprzednich wersjach programu Dynamics 365 Project Service Automation wpisy czasu były wprowadzane tygodniowo. W wersji 3 rozwiązania Project Service Automation wpisy czasu są wprowadzane codziennie. Jednak po utworzeniu kilku wpisów czasu można je tworzyć lub kopiować zbiorczo.

## <a name="create-a-time-entry"></a>Tworzenie wpisu czasu

Aby utworzyć wpis czasu, wykonaj następujące czynności.

1. Na stronie **Wpisy czasu** kliknij przycisk **Nowy**.
2. W oknie dialogowym **Szybkie tworzenie: Wpis czasu** wprowadź czas trwania wpisu czasu w minutach, godzinach lub dniach. Czas trwania musi być wprowadzony w następującym formacie: *x* minut, *x* godzin lub *x* dni. Godziny i dni można również wprowadzać jako wartości dziesiętne, na przykład *x,x* godzin lub *x,x* dni.
3. Wybierz typ wpisu czasu oraz projekt, dla którego wprowadzasz ten wpis czasu.
4. W polu **Zadanie projektu** znajdź zadanie dla tego wpisu czasu.

    > [!NOTE]
    > W przypadku tworzenia wpisu czasu dla zadania, które nie jest przypisane do użytkownika, w polu **Zadanie projektu** kliknij przycisk **Wyszukaj**, wybierz pozycję **Zmień widok**, a następnie wybierz pozycję **Wszystkie aktywne zadania projektu**, a zostanie wyświetlona lista wszystkich zadań.

5. Wprowadź opis, jeśli jest wymagany, a następnie wybierz pozycję **Zapisz i zamknij**.

Po utworzeniu i zapisaniu wpisu czasu można go edytować w siatce wpisów czasu. Siatka wpisów czasu obsługuje dwa formaty:

- Wpisy czasu można wprowadzać w formacie **gg:mm**. Ten format jest następnie konwertowany na godziny i ułamki.
- Godziny i ułamki można wprowadzać bezpośrednio.

Zauważ, że ułamki godziny nie są minutami. Innymi słowy zapis 1,5 godziny oznacza 1 godzinę i 30 minut. Ta sama reguła ma zastosowanie do ułamków dnia. Jeden dzień to 24 godziny, a 0,5 dnia oznacza 12 godzin.

## <a name="bulk-create-time-entries"></a>Zbiorcze tworzenie wpisów czasu

Po utworzeniu kilku wpisów czasu można je kopiować i w ten sposób tworzyć dodatkowe wpisy czasu zbiorczo.

1. Na stronie **Wpisy czasu** kliknij przycisk **Kopiuj tydzień**.
2. W grupie pól **Z okresu** w polach **Data rozpoczęcia** i **Data zakończenia** zdefiniuj zakres dat, z którego mają zostać skopiowane wpisy czasu.
3. W grupie pól **Do okresu** w polu **Data rozpoczęcia** określ dzień, dla którego mają zostać utworzone wpisy czasu.
4. Kliknij przycisk **Kopiuj**, aby utworzyć kopię wpisów czasu odpowiadających dniu tygodnia określonemu w grupie pól **Do okresu**. Na przykład wpis czasu dla poniedziałku poprzedniego tygodnia jest kopiowany do poniedziałku tygodnia określonego w grupie pól **Do okresu**.

## <a name="import-data-for-time-entries"></a>Importowanie danych dla wpisów czasu

Można importować dane z rezerwacji projektów i przypisań. Podczas importowania danych można określić zakres dat dla rezerwacji, które mają zostać zaimportowane, a następnie jawnie wybrać rezerwacje, które mają zostać utworzone jako wpisy czasu **Wersja robocza**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Funkcje grupowania według, sortowania, wyszukiwania i filtrowania

Wpisy czasu można grupować i filtrować według wymiarów określonych w kolumnach. W polu **Grupuj według** wybierz wymiar, który ma być używany do filtrowania wpisów czasu. Przy użyciu strzałek sortowania w nagłówkach kolumn można również sortować rekordy wpisów czasu w porządku rosnącym lub malejącym. Ponadto można wyświetlać lub ukrywać wpisy, klikając przycisk **Filtruj** w nagłówkach kolumn, a następnie w polu **Wyszukaj** wprowadzając tekst, który ma być używany do wyszukiwania wpisów czasu według nazwy projektu, zadania projektu, godziny wpisu lub zasobu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]