---
title: Zaplanuj zasoby dla projektu
description: Planowanie zasobów dla projektu w Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754399"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planuj zasoby dla projektu (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Możesz sprawdzić dostępność zasobów, aby uzyskać ogólny pogląd stopnia zarezerwowania zasobów, lub możesz filtrować widok według umiejętności, zespołu, lokalizacji i innych opcji.  
  
Tablica harmonogramu zawiera listę zasobów i ich dostępności. Wybierz tryb wyświetlania dostępności dla **Godziny**, **Dzień**, **Tydzień**, lub **Miesiąc**.  
  
Przed skorzystaniem z tablicy harmonogramu, należy ją skonfigurować. Aby uzyskać więcej informacji, zobacz [Konfiguruj tablicę harmonogramu (Field Service lub Project Service Automation)](../field-service/configure-schedule-board.md).
  
Jeśli używasz starszej wersji, dla dostępności zasobów sprawdź [Przeglądanie dostępności zasobów](../project-service/view-resource-availability.md).  

> [!IMPORTANT]
>  Aby użyć funkcji rezerwacji tablicy harmonogramu, geokodowania i usług lokalizacji, należy włączyć mapy.  
> 
> 1. W menu głównym zaznacz **Planowanie zasobów** > **Administracja**.  
> 2. Kliknij **Parametry planowania**.  
> 3. Otwórz rekord i przewiń w dół do sekcji **Resource Scheduling Optimization**.  
> 4. W polu **Połącz z Mapy**, wybierz **Tak**.  
> 5. Zaakceptuj warunki i zapisz rekord.  
> 6. W menu głównym wybierz **Project Service** > **Tablica harmonogramu**. Istnieje kilka sposobów ręcznego planowania wymogu rezerwacji. Wybierz metodę, którą preferujesz.
  
## <a name="find-available-resources"></a>Znajdź dostępne zasoby

1.  Na liście **Wymóg rezerwacji**, kliknij prawym przyciskiem myszy na niezaplanowanej rezerwacji i wybierz jedną z następujących czynności:  
  
- Wybierz **Znajdź dostępność - Bieżące zasoby**, aby znaleźć dostępny zasób na liście na tablicy harmonogramu.  
- Wybierz **Znajdź dostępność - Wszystkie zasoby**, aby znaleźć zasób dostępny pośród zasobów w systemie  
   > [!NOTE]
   >  Gdy to zrobisz, filtry ukażą opcje wybranego wymogu rezerwacji.  
  
2. Po pojawieniu się dostępnego przedziału czasu kliknij na nim prawym przyciskiem myszy na tablicy harmonogramu i wybierz **Zarezerwuj tutaj**. Lub przeciągnij i upuść wymóg rezerwacji na dostępny przedział czasu.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Dokonaj rezerwacji zasobu w widoku dziennym i dowiedzieć się, który z zasobów wciąż można zarezerwować
  
1.  Na tablicy harmonogramu, wybierz **Tryb widoku** i wybierz **Dni**.  
  
    Pokazuje widok siatki mówiący o tym, ile godzin zasobu zostało zarezerwowane na dobę i w które dni zasób ten jest wolny.  
  
2.  Kliknij nazwę zasobu, który chcesz zerezerwować, a następnie wybierz **Zarezerwuj**.  
  
3.  W oknie dialogowym **Rezerwacja zasobu (utwórz)** wybierz projekt, dla którego chcesz zarezerwować zasób, wraz z metodą rezerwacji oraz czasem rozpoczęcia i zakończenia.  
  
4.  Kiedy skończysz, wybierz **Zarezerwuj**.  
  
## <a name="view-to-the-schedule-board"></a>Wyświetl tablicę harmonogramu
  
1.  Wybierz niezaplanowany wymóg rezerwacji z listy u dołu.  
  
2.  Przeciągnij wymóg rezerwacji do dostępnego zasobu/przedziału czasu na tablicy harmonogramu.  
  
3.  Kiedy skończysz, wybierz **Zarezerwuj**.  
  
### <a name="additional-resources"></a>Dodatkowe zasoby  
 [Przewodnik menedżera zasobów](../project-service/resource-manager-guide.md)
