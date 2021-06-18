---
title: Zarządzanie strefami czasowymi
description: Po utworzeniu projektu jego strefa czasowa jest oparta na strefie czasowej określonej w szablonie godziny pracy zastosowanym w programie.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997749"
---
# <a name="manage-time-zones"></a>Zarządzanie strefami czasowymi

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


## <a name="projects"></a>Projekty

Po utworzeniu projektu jego strefa czasowa jest oparta na strefie czasowej określonej w szablonie godziny pracy zastosowanym w programie. W szablonie **Projekt** daty są zawsze określane względem strefy czasowej użytkownika zalogowanego na każdej karcie, z wyjątkiem karty **Zadanie**. Podczas wyświetlania struktury podziału pracy daty będą zawsze wyświetlane w strefie czasowej projektu.

## <a name="tasks"></a>Zadania

Podczas tworzenia zadania godzina rozpoczęcia, godzina zakończenia i liczba godzin/dzień jest kontrolowana przez godziny pracy projektu. Jeśli na przykład zadanie zostanie utworzone dla projektu, którego strefa czasowa ma wartość -8 PST i ma następujące godziny pracy: 9:00 rano – 5:00 po południu od poniedziałku do piątku, każde zadanie utworzone bez przydziału będzie respektować godzinę rozpoczęcia i zakończenia w kalendarzu projektu.

## <a name="manage-resources-with-time-zones"></a>Zarządzanie zasobami za pomocą stref czasowych

Aby uzyskać dokładne i przewidywalne wyniki podczas korzystania z **Przedłużenia rezerwacja**, należy spełnić dwa podstawowe kluczowe wymagania:  

- Użytkownik musi skonfigurować strefę czasową swoich urządzeń, aby odpowiadała strefom czasowym zdefiniowanym w **ustawieniach personalizacji** systemu.
 
  ![Ustawienia strefy czasowej w systemie Windows 10](media/reconcile-assignments-03.png)

  ![Ustawienia strefy czasowej w ustawieniach personalizacji](media/reconcile-assignments-04.png)
 
- Zasób możliwy do zarezerwowania musi mieć co najmniej jedną minutę czasu pracy, który pokrywa się z rozkładem używanym do definiowania żądanego rozszerzenia. Na przykład następujące zasoby z godzinami pracy, które mieszczą się w zakresie 9:00 rano i 7:00 wieczorem. 

  ![Porównanie rozkładów zasobów](media/reconcile-assignments-05.png)

W poniższej tabeli przedstawiono:

- Szablon kalendarza projektu
- Zasób A: ten zasób ma ten sam kalendarz i znajduje się w tej samej strefie czasowej, co projekt. Godziną rozpoczęcia rezerwacji będzie 9:00.
- Zasób B: ten zasób znajduje się w innej strefie czasowej niż projekt i zaczyna pracę o 7:00 rano w swojej strefie czasowej. Jednak rezerwacje zaczynają się od godziny 9:00, która jest najwcześniejszym czasem rozpoczęcia rozkładu przydziału.
- Zasoby C i D: zasoby znajdują się w różnych strefach czasowych, różniącymi się między sobą i projektem, a ich rezerwacje zaczynają się nie wcześniej niż ich dostęp do swoich godzin rozpoczęcia.

|Encja  |Kalendarz  |
|-|-|
|Szablon kalendarza projektu   | ![kalendarz projektu](media/reconcile-assignments-06.png) |
|Zasób A  | ![Kalendarz zasobu A](media/reconcile-assignments-06.png) |
|Zasób B  |  ![Kalendarz zasobu B](media/reconcile-assignments-07.png) |
|Zasób C  |  ![Kalendarz zasobu C](media/reconcile-assignments-08.png) |
|Zasób D  | ![Kalendarz zasobu D](media/reconcile-assignments-09.png)  |
 
Po przejściu do widoku **uzgodnienia** zostaną wyświetlone przydziały zasobów i skojarzone niedobory rezerwacji.

![Uzgadnianie widoku przed rozszerzeniem](media/reconcile-assignments-10.png)

Po zastosowaniu funkcji przedłużenia rezerwacji dla każdego zasobu rezerwacje są pomyślnie przedłużane dla każdego zasobu, ponieważ godziny pracy poszczególnych zasobów pokrywają się z rozkładem niedoborów.

![Widok Uzgodnienie po rozszerzeniu rezerwacji](media/reconcile-assignments-11.png) 

Należy zwrócić uwagę, że bliższe zapoznanie się z szczegółowymi informacjami dotyczącymi rezerwacji pokazuje różnice w czasie rozpoczęcia rezerwacji. Rezerwacje zaczynają się nie wcześniej niż godzina rozpoczęcia rozkładu przydziału i nie wcześniej niż jest dostępna godzina rozpoczęcia zasobu.

![Nowe rezerwacje zasobów na tablicy harmonogramu](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]