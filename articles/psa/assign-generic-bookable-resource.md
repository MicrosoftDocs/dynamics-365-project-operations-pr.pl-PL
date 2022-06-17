---
title: Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i zespołu projektu
description: Ten artykuł zawiera informacje o rezerwowaniu ogólnych zasobów dla zadań i zespołów projektów.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9f67ab7381747e5d780f8b0024dd98ae8420d05f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923569"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Przypisywanie ogólnego zasobu możliwego do zarezerwowania do zadania i generowanie wymagań zasobów 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Oprócz rezerwowania i przypisywania nazwanych lub rzeczywistych zasobów do projektu można również przypisywać zasoby ogólne do zadań projektu. Te zasoby mogą służyć jako zastępcze dla zasobów nazwanych, dopóki użytkownik nie będzie gotowy do obsadzenia projektu nazwanymi zasobami. 

1. W usłudze Project Service Automation (PSA) otwórz stronę **Projekt** na karcie **Harmonogram** wprowadź nazwę stanowiska ogólnego zasobu w komórce **Zasób** w harmonogramie. Alternatywnie w komórce kliknij ikonę **Zasób**, aby otworzyć selektora zasobów, a następnie wpisz nazwę zasobu ogólnego, który ma zostać utworzony.

![Tworzenie i przypisywanie ogólnego członka zespołu.](media/RM-how-to-9.png)

Spowoduje to otwarcie panelu **Szybkie tworzenie: Członek zespołu projektu**. 

2. Wprowadź rolę i jednostkę organizacyjną członka zespołu będącego zasobem ogólnym, a następnie kliknij przycisk **Zapisz**.

![Szybkie tworzenie ogólnego członka zespołu.](media/RM-how-to-10.png)

3. Po utworzeniu nowego członka zespołu będącego zasobem ogólnym zostanie on przypisany do zadania. Możesz nadal przypisywać ten zasób ogólny do innych zdań w harmonogramie.

![Przypisywanie istniejącego ogólnego członka zespołu do zadań.](media/RM-how-to-11.png)

4. Po przypisaniu ogólnego zasobu można wygenerować wymaganie zasobu i je zrealizować poprzez bezpośrednie zarezerwowanie albo przesyłając żądanie zasobu do menedżera zasobów.

![Generowanie wymagania dla ogólnego członka zespołu.](media/RM-how-to-12.png)

W siatce członków zespołu można nie tylko używać selektora zasobów, jak wspomniano powyżej, ale również dodawać zasoby ogólne bezpośrednio. Zasoby zostaną dodane z wymaganiami zasobów opartymi na datach początkowych i końcowych oraz metodzie alokacji określonej w panelu **Szybkie tworzenie: Członek zespołu projektu**.

Widać różnicę, jeśli dodasz ogólnego członka zespołu bezpośrednio, a następnie przypiszesz mu więcej zadań, niż ma on wymaganych godzin do pokrycia. Kliknij opcję **Generuj wymaganie**, aby ponownie wygenerować wymaganie w celu zrównoważenia wymaganych godzin z przypisaniem.

Możesz także kliknąć łącze **Wymaganie zasobów** w siatce zespołu, aby otworzyć wymaganie i dodać umiejętności, preferowane zasoby itd.

![Wymaganie zasobu.](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
