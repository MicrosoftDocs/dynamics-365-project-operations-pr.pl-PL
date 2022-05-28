---
title: Jak przeprowadzić wstępną rezerwację zasobów w aplikacji w wersji 2.x?
description: W tym artykule opisano sposób wstępnego rezerwowania członków zespołu projektu za pomocą rozwiązania Project Service.
author: JohnPBurrows
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
ms.openlocfilehash: 472529c146fbb5e7a4540676c880cabd4ab1a32b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585207"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Jak wstępnie zarezerwować zasoby w aplikacji sieci Web (aplikacja Project Service, wersja 2.x)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Można wstępnie zaplanować lub wstępnie zarezerwować zasób dla zespołu projektu, aby pokazać, że planujesz przypisać zasób do projektu. Wstępne rezerwacje nie zużywają dostępnej dyzpozycyjności zasobu. Wstępnie zarezerwowani członkowie zespołu nie mogą być przypisywani do zadań projektu. Tylko zasoby ze stanem Zarezerwowano ostatecznie i Typ zatwierdzenie Zatwierdzone można przypisywać do zadań (przy założeniu, że zapewniają wystarczającą liczbę godzin niezbędną dla pokrycia zadania).

Wstępnie zarezerwowani członkowie zespołu projektu są wyświetlani w siatce Członek zespołu z godzinami rezerwacji wstępnej wyświetlanymi w kolumnie Rezerwacja wstępna. Są oni również widoczni na tablicy harmonogramu. Ponownie, nie oznaczają zużycia dyspozycyjności, gdyż rezerwacja wstępna nie zużywa dyspozycyjności zasobu.

Istnieją trzy sposoby przeprowadzenia rezerwacji wstępnej członka zespołu dla projektu za pomocą rozwiązania Project Service w wersji 2.x. Można przeprowadzić wstępną rezerwację za pomocą tablicy harmonogramu, użyć funkcji Obsługa rezerwacji lub utworzyć zasób ogólny. Te metody zostały opisane poniżej.

## <a name="soft-book-with-the-schedule-board"></a>Wstępna rezerwacja za pomocą tablicy harmonogramu

Aby przeprowadzić wstępną rezerwację za pomocą tablicy harmonogramu wykonaj następujące kroki: 
1. Otwórz tablicę harmonogramu.
2. Wybierz kartę Projekt w dolnej części panelu Wymagania dotyczące rezerwacji tablicy harmonogramu.
3. Znajdź odpowiedni projekt, dla którego chcesz przeprowadzić wstępną rezerwację zasobu. Jeśli posiadasz wiele projektów, kliknij nagłówek kolumny Projektu i skorzystaj z filtru, aby znaleźć projekt.
4. Kliknij projekt, a następnie przeciągnij i upuść go w siatce czasu zasobu.
5. Spowoduje to otwarcie panelu Utwórz rezerwację zasobu po prawej stronie. Dostosuj daty rozpoczęcia i zakończenia, wybierz Stan rezerwacji jak Wstępny i określ godziny. 
6. Kliknij Zarezerwuj.
7. Wróć do projektu, zasób jest teraz wyświetlany jako członek zespołu z godzinami zarezerwowanymi wstępnie w kolumnie Zarezerwuj wstępnie.

Należy zauważyć, że nie można przypisać ich do zadań w strukturze podziału pracy (SPP), ponieważ zasoby muszą być zarezerwowane ostatecznie dla zespołu, aby można je było przypisać.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Przeprowadź wstępną rezerwację przy użyciu funkcji Obsługa rezerwacji

Aby przeprowadzić wstępną rezerwację za pomocą funkcji Obsługa rezerwacji postępuj zgodnie z poniższą procedurą:
1. Na siatce członków zespołu kliknij Nowy.
2. Wybierz zasób, który można zarezerwować, rolę, od/do.
3. Wybierz metodę przydziału inną niż Brak:
- Pełna dyspozycyjność
- Dyspozycyjność procentowa
- Według godzin, Rozłóż równomiernie
- Według godzin, Najwięcej na początku
4. Kliknij opcję Zapisz. Zobaczysz zasób na siatce zespołu i ich godzin wskazane jako Ostateczne.
5. Obsługuj rezerwacje zasobu, klikając Obsługa rezerwacji.
6. Po otwarciu tablicy harmonogramu, rozwiń zasób, aby wyświetlić dla niego rezerwacje. Zobaczysz rezerwację wskazaną jako Ostateczne.
7. Kliknij prawym przyciskiem myszy rezerwację, w obszarze Zmień stan, wybierz Zarezerwuj wstępnie, a następnie Wstępne. Stan rezerwacji to teraz Wstępne.
8. Po zamknięciu tablicy harmonogramu, zobaczysz, że godziny dla zasobu zostały zmienione z Ostateczne na Wstępne w siatce członków zespołu.
Zauważ, że jeśli ostatecznie zarezerwujesz zasób dla zespołu, a następnie przypiszesz zadania w SPP, jeśli skorzystasz z Obsługa rezerwacji, aby zmienić stan z Ostateczne na Wstępne, zostaną usunięte przydziały z zadań dla tego zasobu, ponieważ tylko zasoby zarezerwowane ostatecznie mogą zostać przypisane do zadań.

## <a name="soft-book-by-creating-a-generic-resource"></a>Przeprowadź rezerwację wstępną tworząc zasób ogólny

Możesz utworzyć rezerwację wstępną generując członka zespołu zasobów ogólnych, zgodnie z tablicą harmonogramu lub Żądaniem zasobów i zmieniając typ podczas rezerwacji.
Aby to zrobić, skorzystaj z następującej procedury:

1. W SPP projektu przypisz role do zadań, dla których chcesz wygenerować członków zespołu.
2. Kliknij Generuj zespół projektu.
3. Na siatce członków zespołu projektu wybierz zasób ogólny i kliknij Zarezerwuj.
4. W tablicy harmonogramu wybierz zasób, który chcesz zarezerwować.
5. W panelu Utwórz rezerwację zasobu tablicy harmonogramu zmień stan rezerwacji na Wstępny.
6. Kliknij Zarezerwuj lub Zarezerwuj i Zakończ.

Po zamknięciu tablicy harmonogramu, zobaczysz wybrany zasób dodany do zespołu z wstępnie zarezerwowanymi godzinami, a także przypisane godziny. Zobaczysz także, że zasób ogólny pozostaje na zespole jako wskaźnik, że zadania przypisano do wstępnie zarezerwowanego członka zespołu.

Gdy jesteś gotowy, aby zmienić zasób członka zespołu zarezerwowany wstępnie na członka zespołu zarezerwowanego ostatecznie, aby można było przypisać ich do zadań, wykonaj następujące czynności:

1. Wybierz ten zasób, a następnie kliknij Obsługa rezerwacji.
2. Po otwarciu tablicy harmonogramu, rozwiń zasób, aby wyświetlić dla niego rezerwacje. Zobaczysz rezerwację oznaczoną jako Wstępne.
3. Kliknij prawym przyciskiem myszy rezerwację, w obszarze Zmień stan, wybierz Zarezerwuj ostatecznie, a następnie Ostateczne. Stan rezerwacji to teraz Ostateczne.
4. Po zamknięciu tablicy harmonogramu, zobaczysz, że godziny dla zasobu zostały zmienione z Wstępne na Ostateczne w siatce członków zespołu. Możesz teraz przypisać zasób do zadań (pod warunkiem, że godziny zarezerwowane ostatecznie są zgodne z godzinami nakładu pracy zadania dla przypisania). Należy zauważyć, że jeśli przeprowadziłeś kroki realizacji zasobu ogólnego w punkcie #3 opisane powyżej, gdy zmieniasz stan rezerwacji zasobu z Zarezerwowane wstępnie na Zarezerwowane ostatecznie, członek zespołu jest usuwany z zespołu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
