---
title: Interpretacja stanu projektu
description: W tym temacie zamieszczono informacje statusie przypisanym do projektu w Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081884"
---
# <a name="understand-project-status"></a>Interpretacja stanu projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


 **Sekcja stan** na stronie **Encja projektu** zawiera podsumowanie stanu środowiska projektu na podstawie kosztów i nakładu pracy.


## <a name="status-summary-fields"></a>Pola podsumowania stanu

- Pole **Stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu. Pole to korzysta z kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko. 
- Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu. 
- Wyświetlany w polu **Stan zaktualizowany** nie jest edytowalny. Wartość w tym polu to znacznik czasowy wskazujący, że stan został ostatnio zaktualizowany.
- Pola **Wydajność planowania** oraz **Wydajność kosztów** są ustawiane na podstawie siatki śledzenia. Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu pracy** jest dodatnie, pola te zostaną zaktualizowane do **mieści się**. Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne,te pola otrzymają wartość **nie mieści się**.
