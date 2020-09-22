---
title: Etapy projektu
description: Ten temat zawiera informacje o etapach projektów.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754300"
---
# <a name="project-stages"></a>Etapy projektu 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Etapy projektu są aktualizowane w celu odzwierciedlenia stanu projektu w miarę postępu jego realizacji. Domyślny przepływ procesów biznesowych powoduje automatyczne aktualizowanie niektórych etapów projektu, podczas gdy inne etapy są aktualizowane ręcznie przez menedżera projektu. 

Poniższe etapy są zdefiniowane w domyślnym przepływie procesów biznesowych (BPF):

- Nowe
- Oferta
- Planowanie
- Dostarczenie
- Ukończono
- Zamknij 

## <a name="new"></a>Nowe

Podczas tworzenia projektu jego etap jest ustawiany jako **Nowy**. Jeśli projekt został utworzony z szablonu, może mieć harmonogram, oszacowanie i dane zespołu. W przeciwnym razie jest to tylko konspekt projektu, a pozostałe składniki trzeba wprowadzić.

## <a name="quote"></a>Oferta

Podczas kojarzenia projektu z ofertą lub tworzenia projektu z oferty etap projektu jest ustawiany jako **Oferta**, a szacunkowe daty rozpoczęcia i zakończenia są aktualizowane. Gdy projekt jest na etapie **Oferta**, na karcie **Sprzedaż** na stronie **Encja projektu** widać szczegóły oferty.

## <a name="plan"></a>Planowanie

Gdy wygrywasz ofertą związaną z projektem i kiedy projekt przechodzi do fazy **Kontrakt**, etap projektu zostaje aktualizowany do **Planowanie**. Gdy projekt jest na etapie **Planowanie**, na stronie **Encja projektu** są wyświetlane szczegóły kontraktu.

## <a name="deliver"></a>Dostarczenie

Po zakończeniu planowania projektu, gdy wszystko jest gotowe do rozpoczęcia projektu, menedżer projektu powinien zaktualizować etap projektu na **Dostarczenie**, aby pokazać, że projekt się rozpoczął.

## <a name="complete"></a>Ukończono 

Po zakończeniu prac w projekcie menedżer projektu może zaktualizować etap na **Ukończono**. Aktualizując etap projektu na **Ukończono**, menedżer projektu wskazuje, że praca została w całości wykonana, ale projekt nadal pozostaje otwarty, tak aby można w nim było zarejestrować wszystkie zaległe wpisy czasu lub wydatków.

## <a name="close"></a>Zamknij

Po zarejestrowaniu wszystkich transakcji w projekcie menedżer projektu może zaktualizować etap na **Zamknięto**. Odtąd nie można rejestrować żadnych transakcji, a projekt jest ustawiany jako tylko do odczytu.
