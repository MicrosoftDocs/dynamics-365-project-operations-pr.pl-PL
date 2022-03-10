---
title: Najważniejsze pojęcia
description: W tym temacie zamieszczono informacje o podstawowych pojęciach dotyczących zarządzania zasobami w programie Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 8e56523a9a2fbe8bc07e6d46062f4e1c20e6d2fa2244b32ff53e96d898b0086c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995099"
---
# <a name="key-concepts"></a>Najważniejsze pojęcia

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

W poniższej tabeli przedstawiono najważniejsze pojęcia używane w aplikacji Dynamics 365 Project Service Automation.

| Pojęcie                    | Definicja |
|----------------------------|------------|
| Członek zespołu projektu        | Jako element zespołu projektu członek zespołu projektu może być nazwanym zasobem, który ma rezerwacje, nazwanym zasobem, który nie ma rezerwacji, lub zasobem ogólnym. Zasoby ogólne nie mają rezerwacji, są lokalne dla projektu i nie mają ograniczeń dyspozycyjności między projektami. |
| Zasób ogólny projektu   | Symbol zastępczy zasobu, który umożliwia utworzenie zespołu i obsadzenie planu projektu bez znajomości danych nazwanego zasobu. Jako kalendarz zasobu ogólnego jest używany kalendarz projektu. Zasoby ogólne można dodawać do zespołu projektu i przypisywać do zadań. |
| Zarezerwowane godziny               | Godziny zasobu są rezerwowane ostatecznie względem projektu w celu zagwarantowania, że praca w projekcie zostanie wykonana. Zarezerwowane godziny są zużywane z łącznej dyspozycyjności zasobu. Rezerwacje są dokonywane tylko wobec zasobów nazwanych, a nie ogólnych. |
| Przypisane godziny             | Godziny zasobów są przypisywane do zadań w harmonogramie projektu. Przypisania mogą dotyczyć zasobów nazwanych lub ogólnych. Przypisania mogą być niezależne od rezerwacji. |
| Wymagane godziny             | Dyspozycyjność, która jest wymagana, ale jeszcze nie została zaspokojona przez nazwany zasób. Wymagane godziny mają zastosowanie tylko do ogólnych członków zespołu, wobec których wygenerowano wymagania zasobów. |
| Zapotrzebowanie                     | Obecne i przychodzące obciążenie pracą. W programie Project Service Automation zapotrzebowanie jest prezentowane jako wymagania zasobów lub żądania zasobów. |
| Wymaganie zasobów       | Encja służąca do przechwytywania wymaganych godzin, dat rozpoczęcia i zakończenia, umiejętności, lokalizacji geograficznych i innych wymiarów kalkulacji cen w wymaganych zasobach. Wymagania zasobów są generowane przez członków zespołu projektu albo tworzone indywidualnie. |
| Żądanie zasobu           | Encja używana jako „koperta” do przenoszenia wymagania zasobu, które musi zostać zrealizowane przez menedżera zasobów. |
| Domyślna rola zasobu      | Rola, pod którą zasób jest pogrupowany w celu obliczenia wykorzystania. Zakłada się, że zasób posiada umiejętności wymagane w roli i jest w stanie zaspokoić docelowe wykorzystanie w roli. |
| Jednostka organizacyjna zasobu | Jednostka organizacyjna, do której jest przypisany zasób. |
| Rozkład                    | Godziny zadania, wymagania lub przydziału w rozbiciu na dzienną dystrybucję. Na przykład zadanie przewidziane na pięć dni i 40 godzin można rozłożyć na 8 godzin dziennie przez pięć dni. |
| Widok Uzgadnianie        | Widok, w którym są pokazywane rezerwacje i przypisania dla każdego członka zespołu projektu. W tym widoku menedżer projektu może wyszukiwać wszelkie niezgodności między rezerwacjami i przypisaniami, a w razie stwierdzenia niezgodności podejmować działania naprawcze. |
| Godziny pracy                 | Encja służąca do identyfikowania dyspozycyjności zasobu oraz godzin pracy i wolnych. Ta encja jest również nazywana kalendarzem zasobu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]