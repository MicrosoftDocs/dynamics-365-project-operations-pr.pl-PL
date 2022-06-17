---
title: Interpretacja stanu projektu
description: Ten artykuł zawiera informacje dotyczące stanów przypisywanych do projektów aplikacji Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 86cb60b634b62af23f39720c0452dca82ff3ad26
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923615"
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