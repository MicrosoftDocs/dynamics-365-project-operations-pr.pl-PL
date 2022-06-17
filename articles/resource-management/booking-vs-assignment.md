---
title: Rezerwacje i przypisania
description: W tym artykule podane są informacje na temat różnic między rezerwacjami zasobów a przypisaniami zasobów.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918601"
---
# <a name="bookings-vs-assignments"></a>Rezerwacje i przypisania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rezerwacje to ostateczne lub wstępne przydzielenie zasobów do projektu. Rezerwacje ostateczne zużywają dyspozycyjność zasobu. Rezerwacje reprezentują koncepcje organizacyjne dla zespołów, dzięki czemu mogą zrozumieć, w jaki sposób zasoby będą realizowane między różnymi projektami. Dynamics 365 Project Operations traktuje rezerwacje jako koncepcję na poziomie projektu. 

W przeciwieństwie do rezerwacji, przydziały to przydział zasobów do zadań projektu w harmonogramie projektu. Zasoby mogą mieć nazwy lub ogólne.  Gdy zapotrzebowanie na zasoby pochodzi z przydziałów zadań projektu, Project Operations używają konturów nakładu pracy przydziału zasobów do tworzenia konturów szczegółów zapotrzebowania na zasoby. Jednak czas, który przypisano do zasobów, nie jest zachowywany. Aktualizacje rezerwacji wynikających z wymagania zasobu nie aktualizują żadnych przypisań zasobów.

Zazwyczaj suma księgowań zasobu jest równa sumie przydziałów zasobu w jednym lub wielu zadaniach. Jednak Project Operations nie wymusza takiej zgodności. Widok **Uzgadnianie** pokazuje menedżerowi projektu miejsca, w których rezerwacje i przypisania zasobów są niezgodne.




[!INCLUDE[footer-include](../includes/footer-banner.md)]