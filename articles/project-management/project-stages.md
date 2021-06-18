---
title: Etapy projektu
description: W tym temacie zamieszczono informacje na temat etapów projektów, które są dostępne w Microsoft Dynamics Project operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996939"
---
# <a name="project-stages"></a>Etapy projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Etapy projektu są zaprojektowane w celu odzwierciedlenia stanu projektu w miarę postępu jego realizacji. Przy użyciu dostosowań można automatycznie aktualizować etapy przepływu procesów biznesowych, Power Automate, a także rozszerzenia dodatków plug-in.

Poniższe etapy są zdefiniowane w domyślnym przepływie procesów biznesowych:

- Nowa
- Oferta
- Plan
- Dostarczenie
- Zakończony
- Zamykanie 

## <a name="new"></a>Nowa

Podczas tworzenia projektu jego etap jest ustawiany jako **Nowy**. Jeśli projekt został utworzony z szablonu, może mieć harmonogram, oszacowanie i dane zespołu. W przeciwnym razie jest to konspekt projektu, a pozostałe składniki trzeba wprowadzić.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]