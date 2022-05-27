---
title: Interpretacja stanu projektu
description: Ten temat zawiera informacje o stanie przypisania do projektów w rozwiązaniu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9efa6135bbaa98f8968e09fcf38c9dd4fde84fe4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578905"
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