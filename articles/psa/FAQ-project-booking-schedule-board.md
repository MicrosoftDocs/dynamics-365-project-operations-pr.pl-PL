---
title: Tworzenie rezerwacji projektu z tablicy harmonogramu
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia rezerwacji w projekcie z tablicy harmonogramu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286126"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Tworzenie rezerwacji projektu z tablicy harmonogramu

[!include [banner](../includes/psa-now-project-operations.md)]

Możesz zarezerwować zasób dla projektu bezpośrednio na karcie **Zespół** dla projektu lub wygenerować zapotrzebowanie na zasób z przydziału ogólnego członka zespołu, a następnie spełniając wygenerowane wymaganie dzięki członkowi zespołu projektu.

Możesz także zarezerwować zasób dla projektu bezpośrednio z tablicy harmonogramu. Możesz to zrobić na jeden z trzech sposobów:

- **Przeprowadź rezerwację z wygenerowanego wymagania zasobu:** możesz wygenerować wymaganie zasobu po utworzeniu zasobu ogólnego i przypisaniu zadań w ramach projektu.

- **Rezerwuj z wymagania podstawowego:** podstawowe wymagania są wyświetlane na tablicy harmonogramu na karcie **Projekt**. 

- **Przeprowadź rezerwację z nowego wymagania zasobu:** możesz utworzyć wymaganie zasobu od podstaw i skojarzyć je z projektem. W tablicy harmonogramu wymaganie zasobu jest widoczne na karcie **Otwarte wymagania**.

## <a name="book-from-a-generated-resource-requirement"></a>Przeprowadź rezerwację z wygenerowanego wymagania zasobu

Możesz utworzyć zasób ogólny i przypisać go do jednego lub wielu zadań w ramach projektu. Następnie można wygenerować wymaganie zasobu z ogólnego członka zespołu. 

1.  W tablicy harmonogramu ten zasób będzie widoczny na karcie **Otwarte wymagania**. Może zaistnieć konieczność użycia filtrów kolumny w siatce, jeśli masz wiele otwartych wymagań. 

    ![Otwórz kartę wymagań na tablicy harmonogramu](media/FAQ-Project-Booking-Schedule-Board-1.png "Zrzut ekranu ukazujący tabelę z rezerwacjami i przypisaniami")

2. Wybierz wymaganie. Karta **Znajdź dostępność** pojawi się w górnej części wybranego wiersza,
 
3. Po wybraniu karty uruchamia się tryb Asystent planowania w tablicy harmonogramu i filtruje on dostępne zasoby, które spełniają wymagania zasobu. Następnie można zarezerwować zasób.

4. Można również przeciągnąć i upuścić wybrany wiersz z dołu tablicy harmonogramu do komórki zasobu w siatce powyżej. Po upuszczeniu otworzy się panel **Utwórz rezerwację zasobu** po prawej stronie.

    Wybranie **Rezerwuj** rezerwuje zasób dla zespołu projektu.

![Panel Utwórz rezerwację zasobu](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezerwuj z wymagania podstawowego

Tworzenie projektu w Project Service powoduje automatyczne tworzenie wymagania zasobu o nazwie Wymaganie podstawowe. Jest to puste wymaganie służące do szybkiego rezerwowania zasobu z tablicy harmonogramu bez generowania wymagania czy tworzenia go od podstaw. Ponieważ wymagane jest puste, należy określić daty, a także metodę alokacji oraz godziny, jeśli ma to zastosowanie. 

1. Aby zarezerwować zasób za pomocą wymagania podstawowego, na tablicy harmonogramu wybierz kartę **Projekt**. Jeśli masz wiele projektów, być może będzie trzeba skorzystać z filtru kolumny w kolumnie **Projekt**.

   ![Filtry kolumn na tablicy harmonogramu](media/FAQ-Project-Booking-Schedule-Board-2.png "Zrzut ekranu ukazujący tabelę z rezerwacjami i przypisaniami")

2. Wybierz wymaganie, które ma tylko nazwę projektu jako nazwę i czas trwania równy zero (0).

3. Wybierz kartę **Znajdź dostępność**, która pojawia się w wierszu. To przenosi tablicę harmonogramu w tryb Asystent planowania i pokazuje dostępne zasoby, które mogą zostać zarezerwowane dla projektu.

4. Ponieważ **Wymaganie podstawowe** jest wymaganiem pustym o czasie trwania zero (0), trzeba będzie ustawić czas trwania na panelu **Utwórz rezerwację zasobu** podczas wybierania i rezerwacji zasobu.

5. Można również wybrać element **Podstawowe wymaganie projektu** w dolnej części tablicy harmonogramu i przeciągnąć oraz upuścić go na zasób, rezerwując go.
 
    Ponieważ **Wymaganie podstawowe** jest wymaganiem pustym o czasie trwania zero (0), trzeba będzie ustawić czas trwania na panelu **Utwórz rezerwację zasobu** podczas wybierania i rezerwacji zasobu.
 
    Gdy rezerwujesz zasób za pomocą elementu **Wymaganie podstawowe** na tablicy harmonogramu, dodajesz go do zespołu projektu bez żadnych przypisań.
 
## <a name="book-from-a-new-resource-requirement"></a>Przeprowadź rezerwację z nowego wymagania zasobu
Wykonaj poniższe kroki, aby zarezerwować z nowego wymagania zasobu. 

1. Przejdź do **Wymagania zasobów** i wybierz **Nowy**, aby utworzyć nowe wymaganie zasobu.

2. Na karcie **Projekt** wybierz projekt, aby skojarzyć wymaganie z projektem.
 
    W tablicy harmonogramu to nowe wymaganie jest wyświetlane jako **Wymaganie otwarte**, które możesz zrealizować.

3. Zarezerwuj zasób, aby go dodać do zespołu projektu.

4. Teraz gdy zasób jest już zarezerwowany, należy ręcznie przypisać zadania.



[!INCLUDE[footer-include](../includes/footer-banner.md)]