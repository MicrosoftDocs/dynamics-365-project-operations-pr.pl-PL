---
title: Rezerwacje i przypisania
description: Ten temat zawiera informacje o różnicach między księgami zasobów a przydziałami zasobów.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008464"
---
# <a name="bookings-vs-assignments"></a>Rezerwacje i przypisania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu. Rezerwacje ostateczne zużywają dyspozycyjność zasobu. Rezerwacje reprezentują koncepcje organizacyjne dla zespołów, dzięki czemu mogą zrozumieć, w jaki sposób zasoby będą realizowane między różnymi projektami. Dynamics 365 Project Operations traktuje rezerwacje jako koncepcję na poziomie projektu. 

W przeciwieństwie do rezerwacji, przydziały to przydział zasobów do zadań projektu w harmonogramie projektu. Zasoby mogą mieć nazwy lub ogólne.  Gdy zapotrzebowanie na zasoby pochodzi z przydziałów zadań projektu, Project Operations używają konturów nakładu pracy przydziału zasobów do tworzenia konturów szczegółów zapotrzebowania na zasoby. Jednak czas, który przypisano do zasobów, nie jest zachowywany. Aktualizacje rezerwacji wynikających z wymagania zasobu nie aktualizują żadnych przypisań zasobów.

Zazwyczaj suma księgowań zasobu jest równa sumie przydziałów zasobu w jednym lub wielu zadaniach. Jednak Project Operations nie wymusza takiej zgodności. Widok **Uzgadnianie** pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.




[!INCLUDE[footer-include](../includes/footer-banner.md)]