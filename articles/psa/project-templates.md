---
title: Szablony projektów
description: W tym temacie przedstawiono informacje na temat korzystania z szablonów projektów w celu szybkiego konfigurowania projektów.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082174"
---
# <a name="project-templates"></a>Szablony projektów 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Szablon projektu to wstępnie zdefiniowana struktura, która pomaga szybko i łatwo rozpocząć pracę nad projektem. Można użyć wstępnie zdefiniowanego szablonu w celu utworzenia nowego projektu jednym kliknięciem. Tak jak w przypadku projektów, dla szablonów projektów należy zdefiniować wymagania wstępne. Należy zdefiniować kalendarz projektu dla każdego szablonu projektu, a w organizacji muszą być wstępnie zdefiniowane role i cenniki, tak aby składniki szablonu miały użyteczne dane.

Szablon projektu zawiera trzy składniki: harmonogram, oszacowania projektu i członków zespołu projektu.

## <a name="schedule"></a>Zaplanuj

Harmonogram w szablonie projektu ma taki sam zestaw elementów, jak harmonogram w projekcie. Możesz utworzyć hierarchię zadań, powiązać role z zadaniami, zdefiniować atrybuty harmonogramu oraz ustawić zależności. Harmonogram w szablonie projektu obsługuje również tryby zadań dla każdego zadania. W związku z tym obsługuje aparat planowania. Z projektem należy skojarzyć kalendarz projektu. Podczas tworzenia harmonogramu pracy nie ma różnicy między szablonem projektu a projektem.

## <a name="project-estimates"></a>Szacowania projektu

Szacunki projektu w szablonie projektu działają tak samo, jak szacunki projektu w projekcie. Różnica polega na tym, że koszty własne i ceny sprzedaży są pobierane z domyślnych list kosztów własnych i cenników sprzedaży zdefiniowanych w parametrach.

## <a name="creating-a-project-from-a-template"></a>Tworzenie projektu na podstawie szablonu
 
Istnieje kilka sposobów utworzenia projektu na podstawie szablonu projektu:

- Podczas tworzenia projektu z oferty można wybrać szablon projektu w oknie dialogowym **Szybkie tworzenie: Projekt**.

> ![Okno dialogowe Szybkie tworzenie: Projekt](media/project-11.png)

- Podczas tworzenia projektu przez wybranie opcji **Nowy projekt** strona **Projektu** jest wyświetlana przed zapisaniem rekordu. W polu **Wybierz szablon** wybierz jeden ze wstępnie zdefiniowanych szablonów projektów istniejących w organizacji.
- Użycie opcji **Utwórz projekt na podstawie szablonu** na stronie **Encja Szablon**.

## <a name="copying-components-of-template-to-project"></a>Kopiowanie elementów szablonu do projektu

Podczas kopiowania składników szablonu projektu do projektu mogą nastąpić pewne zastąpienia, zależnie od ustawień w projekcie.

### <a name="copying-the-schedule"></a>Kopiowanie harmonogramu

Jeśli podczas kopiowania harmonogramu z szablonu projektu projekt ma inny kalendarz projektu niż szablon, godziny pracy z kalendarza projektu zostaną zastosowane do harmonogramu zadań. W ten sposób harmonogram zostanie dopasowany do kopii kalendarza projektu. Analogicznie pierwsze zadanie w harmonogramie przyjmuje datę rozpoczęcia projektu, a harmonogram pozostałej części hierarchii jest aktualizowany na podstawie czasu trwania i zależności określonych w szablonie. 

### <a name="copying-project-estimates"></a>Kopiowanie szacowań projektów 

Podczas kopiowania między wierszami szacowania projektu są aktualizowane cenniki. W przypadku listy kosztów własnych te aktualizacje bazują na jednostce będącej właścicielem projektu. Dla cennika sprzedaży bazują na odbiorcy. W projektach skojarzonych z encją sprzedaży koszt jednostkowy i ceny sprzedaży są ustalane na podstawie tych cenników.

### <a name="copying-a-project-team"></a>Kopiowanie zespołu projektu

Podczas kopiowania zespołu projektu z szablonu projektu do projektu kopiowane są zasoby ogólne wraz z umiejętnościami i poziomami biegłości zdefiniowanymi w szablonie. Przypisania zasobów ogólnych są także obsługiwane jak w szablonie projektu. Nazwane zasoby nie są obsługiwane w szablonach projektów.
