---
title: Interpretacja stanu projektu
description: Ten temat zawiera informacje o stanie przypisania do projektów w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 47d71b945a2d5e7aa41d2ac3731ac4a5d3051ce279229794e31c9673f688130e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997034"
---
# <a name="understand-project-status"></a>Interpretacja stanu projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


Sekcja **Stan** na stronie **Encja projektu** zawiera podsumowanie stanu środowiska projektu na podstawie kosztów i nakładu pracy.


## <a name="status-summary-fields"></a>Pola podsumowania stanu

- Pole **stan całkowitego projektu** jest polem edytowalnym, które zawiera ogólny stan projektu. Pole to korzysta z kodowania kolorów, takiego jak kolor zielony, żółty i czerwony, aby wskazywać większe ryzyko. 
- Pole **Komentarze** umożliwia menedżerowi projektu wprowadzenie określonych komentarzy dotyczących stanu. 
- Pole **Stan zaktualizowany dnia** jest edytowalny. Wartość w tym polu to znacznik czasowy wskazujący, że stan został ostatnio zaktualizowany.
- Pola **Wydajność planowania** i **Wydajność kosztów** są ustawiane na podstawie siatki śledzenia. Jeśli odchylenie względem harmonogramu i kosztu dla węzła głównego w widoku **śledzenia nakładu** pracy jest dodatnie, te pola są zaktualizowane na **Wyprzedza**. Kiedy Odchylenie względem harmonogramu i kosztu dla węzła głównego są ujemne,te pola otrzymają wartość **Opóźnienie**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]