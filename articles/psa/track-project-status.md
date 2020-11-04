---
title: Śledź stan projektu
description: Śledzenie stanu projektu w Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082098"
---
# <a name="track-a-projects-status-project-service"></a>Śledź stan projektu (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Użyj [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], aby śledzić postęp projektu klienta.  

Wraz z postępem zaangażowania etapy projektu są aktualizowane, aby odzwierciedlić etap zaangażowania:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Nowy**    | Podczas tworzenia projektu etap jest określany jako **Nowy**. Jeżeli projekt został utworzony z szablonu, na tym etapie projekt może posiadać harmonogram, szacunki i dane zespołu. W przeciwnym razie będzie to konspekt projektu i będziesz musiał ręcznie wprowadzić pozostałe elementy projektu. |
|  **Oferta**   |      Podczas kojarzenia projektu z ofertą lub tworzenia go z oferty, etap projektu jest określany jako **Oferta** , a szacunkowe daty rozpoczęcia i zakończenia są również aktualizowane. Gdy projekt jest w fazie oferty, szczegóły dotyczące ofert są wyświetlane na karcie **Sprzedaż** na stronie **Projekt**.      |
|   **Planowanie**   |                                     Gdy wygrywasz ofertę związaną z projektem, i kiedy zaangażowanie przechodzi na etap umowy, etap projektu zostaje aktualizowany do **Plan**. Szczegóły dotyczące umowy są wyświetlane na karcie **Sprzedaż** na stronie **Projekt**.                                      |
| **Zakończony** |                    Po zakończeniu pracy nad projektem można przełączyć etap na **Zakończ**. Gdy etapu projektu jest określany jako zakończony, rozumiemy, że praca została wykonana w 100%, ale projekt pozostaje otwarty przez czas oczekiwania lub do czasu zarejestrowania wpisów dotyczących wydatków.                     |
|  **Zamknij**   |           Gdy wszystkie transakcje zostały zarejestrowane w projekcie i nie spodziewasz rejestrowania żadnych innych, możesz ręcznie ustawić etap na **Zamknij**. Gdy projekt jest na etapie **Zamknij** , nie możesz zarejestrować żadnych więcej transakcji w ramach tego projektu i projektu jest w trybie tylko do odczytu.           |

## <a name="to-track-a-projects-status"></a>Aby śledzić stan projektu  

1.  Przejdź do **Project Service > Projekty**.  

2.  Kliknij projekt, nad którym chcesz pracować.  

3.  Na pasku u góry ekranu, wybierz strzałkę w dół obok nazwy projektu, a następnie kliknij **Śledzenie projektu**.  

4.  Wybierz **Śledzenie nakładu pracy** lub **Śledzenie kosztów** na liście rozwijanej powyżej listy zadań.  

5.  Kliknij dwukrotnie dowolne zadanie, aby je edytować. Możesz również przenieść lub zmienić rozmiar pasków na wykresie Gantta, aby zmienić godzinę i postęp zadania.  

### <a name="see-also"></a>Zobacz także  
 [Przewodnik menedżera projektu](../psa/project-manager-guide.md)
