---
title: Szablony projektów
description: W tym artykule przedstawiono informacje na temat korzystania z szablonów projektów w celu szybkiego konfigurowania projektów.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 03cccf8f0201d82db57e52dc1175fcf9a7812a53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930883"
---
# <a name="project-templates"></a>Szablony projektów 

[!include [banner](../includes/psa-now-project-operations.md)]

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

> ![Okno dialogowe Szybkie tworzenie: Projekt.](media/project-11.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
