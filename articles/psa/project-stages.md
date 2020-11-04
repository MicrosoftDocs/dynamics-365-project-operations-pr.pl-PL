---
title: Typy etapów projektu
description: Ten temat zawiera informacje o etapach projektów.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 521bf4b3090473a603626a99fded53906b644a7a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082063"
---
# <a name="project-stage-types"></a>Typy etapów projektu 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Etapy projektu są zaprojektowane w celu odzwierciedlenia stanu projektu w miarę postępu jego realizacji. Przy użyciu dostosowań można automatycznie aktualizować etapy przepływu procesów biznesowych, Power Automate, a także rozszerzenia dodatków plug-in.

Poniższe etapy są zdefiniowane w domyślnym przepływie procesów biznesowych (BPF):

- Nowa
- Oferta
- Planowanie
- Dostarczenie
- Ukończono
- Zamknij 

## <a name="new"></a>Nowe

Podczas tworzenia projektu jego etap jest ustawiany jako **Nowy**. Jeśli projekt został utworzony z szablonu, może mieć harmonogram, oszacowanie i dane zespołu. W przeciwnym razie jest to tylko konspekt projektu, a pozostałe składniki trzeba wprowadzić.

## <a name="quote"></a>Oferta

Podczas kojarzenia projektu z ofertą lub tworzenia projektu z oferty etap projektu jest ustawiany jako **Oferta** , a szacunkowe daty rozpoczęcia i zakończenia są aktualizowane. Gdy projekt jest na etapie **Oferta** , na karcie **Sprzedaż** na stronie **Encja projektu** widać szczegóły oferty.

## <a name="plan"></a>Planowanie

Gdy wygrywasz ofertą związaną z projektem i kiedy projekt przechodzi do fazy **Kontrakt** , etap projektu zostaje aktualizowany do **Planowanie**. Gdy projekt jest na etapie **Planowanie** , na stronie **Encja projektu** są wyświetlane szczegóły kontraktu.

## <a name="deliver"></a>Dostarczenie

Po zakończeniu planowania projektu, gdy wszystko jest gotowe do rozpoczęcia projektu, menedżer projektu powinien zaktualizować etap projektu na **Dostarczenie** , aby pokazać, że projekt się rozpoczął.

## <a name="complete"></a>Ukończono 

Po zakończeniu prac w projekcie menedżer projektu może zaktualizować etap na **Ukończono**. Aktualizując etap projektu na **Ukończono** , menedżer projektu wskazuje, że praca została w całości wykonana, ale projekt nadal pozostaje otwarty, tak aby można w nim było zarejestrować wszystkie zaległe wpisy czasu lub wydatków.

## <a name="close"></a>Zamknij

Po zarejestrowaniu wszystkich transakcji w projekcie menedżer projektu może zaktualizować etap na **Zamknięto**. Odtąd nie można rejestrować żadnych transakcji, a projekt jest ustawiany jako tylko do odczytu.
