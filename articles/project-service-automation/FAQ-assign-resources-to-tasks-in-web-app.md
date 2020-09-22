---
title: Jak przypisać zasób, który można zarezerwować, do zadania w aplikacji sieci Web
description: Przegląd sposobów przypisywania zasobów możliwych do zarezerwowania.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754422"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Jak przypisać zasób, który można zarezerwować do zadania w aplikacji sieci Web (aplikacja Project Service, v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Istnieją dwa sposoby przypisywania zasobu do zadania w Project Service. Możesz rezerwować zasób jako członek zespołu, a następnie przypisać go do zadania. Lub możesz też utworzyć ogólnego członka zespołu za pośrednictwem przypisywania roli na zadaniach, wygenerować zespół, a następnie spełnić związane z nim wymagania za pomocą zasobu nazwanego.

Należy zauważyć, że jeśli chcesz przypisać zasób, który można zarezerwować do zadania, członek zespołu zasobu, który można zarezerwować musi posiadać wystarczającą ilość dostępnych rezerwacji. Stan rezerwacji musi być określony jako Typ zatwierdzenia Zarezerwowano ostatecznie a Stan Zatwierdzono. Jeśli nie ma wystarczającej liczby rezerwacji dla zasobu, Project Service usuwa przypisania i wyświetla następujący komunikat o błędzie:

*Nie można przypisać zasobu do zadania - Następujące zasoby nie mają zarezerwowanej wystarczającej liczby godzin dla tego projektu*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Zarezerwuj zasób jako członek zespołu, a następnie przypisz zasób do zadania

Dzięki tej metodzie dodajesz zasób do zespołu projektu, a następnie przypisujesz zadania do zasobu w harmonogramie projektu. Oto, jak to zrobić:
1.  W siatce Członek zespołu dodaj nowego członka zespołu, wybierając **Nowy**.
2.  Na ekranie Szybkie tworzenie członków zespołu wybierz nazwę zasobu, który można zarezerwować, i ustaw rolę.
3.  Wybierz daty **Od** i **Do**.

    > [!div class="mx-imgBorder"] 
    > ![Zrzut ekranu składnika Dodawanie członka zespołu](media/FAQ-Resources-to-Tasks2-1.png "Zrzut ekranu składnika Dodawanie członka zespołu")
 
4.  Wybierz jedną z następujących metod alokacji, aby zarezerwować zasób:
    - **Pełna dyspozycyjność** rezerwuje pełną dyspozycyjność zasobu dla określonych dat Od/Do.
    - **Dyspozycyjność procentowa** rezerwuje zasób procentowo dla dyspozycyjności zasobu dla określonych dat Od/Do.
    - **Według godzin — rozłóż równomiernie** rezerwuje zasób na określoną liczbą godzin, rozkładając je równomiernie w ciągu dnia dla określonych dat Od/Do.
    - **Według godzin — Najwięcej na początku** rezerwuje zasób na określoną liczbą godzin, kładąc nacisk na godziny początkowe w ciągu dnia dla określonych dat Od/Do.

    Nie wybieraj **Brak**, ponieważ ta metoda dodaje zasób do zespołu, ale nie tworzy żadnych rezerwacji, które absorbują dyspozycyjność zasobu.
5.  Wybierz pozycję **Zapisz**.

    Należy zauważyć, że godziny rezerwacji muszą pokrywać nakład pracy i zakres dat zadań, które można przypisać do tego zasobu. Jeśli nie są one zgodne, nie możesz przypisać zasobu do zadania.

6.  Na strukturze podziału pracy (SPP) dla zadania kliknij listę rozwijaną komórki zasobu. Następnie: 

    1. Wybierz **Dodaj**.
    2. Wybierz listę rozwijaną w obszarze **Zasoby** i wybierz dodanego powyżej członka zespołu.
    3. Wybierz pozycję **OK**. Członek zespołu teraz jest przypisany do zadania.

    > [!div class="mx-imgBorder"] 
    > ![Zrzut ekranu dotyczący dodawania zasobów z SPP](media/FAQ-Resources-to-Tasks2-2.png "Zrzut ekranu dotyczący dodawania zasobów z SPP")
 
Na siatce członków zespołu zobaczysz sumę godzin przypisanych do zasobu w obszarze Przypisane godziny. Będzie on mniejsza od liczby godzin zarezerwowanych dla zasobu lub równa z nią. 

> [!div class="mx-imgBorder"] 
> ![Zrzut ekranu z przypisanymi godzinami dla zasobu](media/FAQ-Resources-to-Tasks2-3.png "Zrzut ekranu z przypisanymi godzinami dla zasobu")
 
Jeśli zadanie, które próbujesz przypisać do zasobu rozpoczyna się dacie zakończenia rezerwacji zasobów, zasób nie będzie widoczny na liście rozwijanej.

Należy zauważyć, że można przypisać zasób do większej liczny godzin niż godziny zarezerwowane jeśli zasób posiada jeszcze nieprzypisaną dyspozycyjność. W tym przypadku zasób będzie tylko częściowo przypisany do ich rezerwacji. Można wyświetlić te pozostałe godziny nieprzypisane do zadań dodając kolumnę Nieobsadzone godziny do struktury podziału pracy.

Jeśli zasoby są przypisane do zarezerwowanych godzin (liczba godzin dla nich zarezerwowanych równa się liczbie przypisanych do nich godzin), pojawi się komunikat o błędzie podczas próby przypisania do nich kolejnych zadań:

*Nie można przypisać zasobu do zadania - Następujące zasoby nie mają zarezerwowanej wystarczającej liczby godzin dla tego projektu.*

Ponadto domyślny członek zespołu menedżera projektu, który jest dodawany do zespołu podczas tworzenia projektu jest dodawany bez żadnych rezerwacji i nie można go przypisać do żadnego zadania. Nie będą oni widoczni na liście rozwijanej zasobów dla zadań.

Jeśli chcesz przypisać ten zasób, musisz ich usunąć z zespołu, a następnie ponownie dodaj za pomocą metody alokacji innej niż Brak. Są oni dodawani do zespołu podczas tworzenia projektu, aby projekt miał domyślnie co najmniej jedną osobę zatwierdzającą.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Utwórz ogólnego członka zespołu za pomocą przypisania roli do zadania

Ta metoda sprawia, że zasoby mają odpowiednią ilość rezerwacji dla zadań. Po pierwsze tworzysz symbol zastępczy lub zasób ogólny, który opisuje cechy zasobu nazwanego, który ma ostatecznie pracować na zadaniach, tworząc zespół po przypisaniu ról do zadań. Oto, jak to zrobić:

1. Na strukturze podziału pracy wybierz zadanie.
2. Wybierz ikonę listy rozwijanej **Rola przypisana** w komórce zasobów.
3. Wybierz listę rozwijaną **Rola** i wybierz rolę dla zasobu ogólnego.
4. Wybierz pozycję **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Zrzut ekranu dotyczący użycia SPP do dodawania zasobów](media/FAQ-Resources-to-Tasks2-4.png "Zrzut ekranu dotyczący użycia SPP do dodawania zasobów")
 
Po zakończeniu przypisywania ról do zadań w SPP, wybierz **Wygeneruj zespół projektu**. Usługa Project Service tworzy minimalną liczbę ogólnych członków zespołu, w oparciu o role, korzystając z jednostek organizacyjnych i kalendarza projektu agregując przypisania zadań.

> [!div class="mx-imgBorder"] 
> ![Zrzut ekranu z generowaniem zespołu projektu](media/FAQ-Resources-to-Tasks2-5.png "Zrzut ekranu z generowaniem zespołu projektu")
 
Na siatce Członek zespołu zobaczysz zasoby typu Zasób ogólny z nazwą roli i stanowiska. Jeśli dwa zasoby są potrzebne dla roli, aby zakończyć pracę, funkcja Generuj zespół tworzy dwóch członków zespołu i używa nazwy stanowiska, aby odróżnić ich od siebie.

> [!div class="mx-imgBorder"] 
> ![Zrzut ekranu pokazujący dodawanie dwóch zasobów ogólnych](media/FAQ-Resources-to-Tasks2-6.png "Zrzut ekranu pokazujący dodawanie dwóch zasobów ogólnych")
 
Można otworzyć bazowe wymagania zasobu dla ogólnego członka zespołu, wybierając łącze w obszarze Wymaganie zasobów.

> [!div class="mx-imgBorder"] 
> ![Zrzut ekranu przedstawiający otwieranie bazowego wymagania zasobu](media/FAQ-Resources-to-Tasks2-7.png "Zrzut ekranu przedstawiający otwieranie bazowego wymagania zasobu")

Wybierz **Zarezerwuj** dla zasobu ogólnego, a w następnym kroku będziesz mógł użyć tablicy harmonogramu, aby wyszukać i zarezerwować rzeczywisty zasób. Można również przesłać wymagania do spełnienia przez menedżera zasobu wybierając **Prześlij żądanie**.

Gdy zasób ogólny jest zrealizowany przez zasób nazwany, zasób ogólny jest usuwany z zespołu a przypisania zadań dla zasobu ogólnego są przypisywane do zasobu nazwanego, który zrealizował wymaganie zasobu dla zasobu ogólnego.
 

