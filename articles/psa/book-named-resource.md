---
title: Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów
description: Ta temat zawiera informacje o rezerwowaniu nazwanych zasobów na potrzeby ogólnego wymagania zasobu.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145115"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezerwowanie nazwanych zasobów z poziomu wymagań zasobów

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Można użyć nazwanego zasobu, aby zastąpić ogólny zasób mający wymaganie zasobu.

1. W usłudze Project Service Automation (PSA) na stronie **Projekty** kliknij kartę **Zespół**.
2. Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie kliknij opcję **Zarezerwuj**. Możesz też otworzyć wymaganie zasobu, a następnie kliknąć przycisk **Zarezerwuj**.


![Rezerwowanie ogólnego członka zespołu](media/RM-how-to-14.png)


3. Na stronie **Asystent planowania** wybierz nazwany zasób, który ma zostać zarezerwowany do Twojego zespołu projektu, a następnie kliknij opcję **Zarezerwuj**.

![Rezerwowanie ogólnego członka zespołu przy użyciu Asystenta planowania](media/RM-how-to-15.png)

Gdy rezerwacja jest zakończona i zaspokojona przez nazwany zasób, zasób ogólny jest zastępowany nazwanym zasobem.

![Nazwany członek zespołu zastępujący ogólnego członka zespołu](media/RM-how-to-16.png)

Również przypisania w harmonogramie zostaną zaktualizowane o nazwany zasób.

![Nazwany członek zespołu projektu przypisany do zadań projektu](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Wypełnianie roli ogólnego zasobu wieloma nazwanym zasobami
Zaspokojenie wymagania na zasób ogólny za pomocą wielu nazwanych zasobów przypomina operację przypisania jednego nazwanego zasobu. Załóżmy na przykład, że istnieje zadanie o czasie trwania pięć dni i nakładzie pracy 120 godzin. Tego zadania nie może wykonać jeden zasób pracujący na typowej ośmiogodzinnej zmianie w pięciodniowym tygodniu pracy. 

![Zadanie wymagające 120 godzin pracy przez pięć dni](media/RM-how-to-21.png)

Wymaganie opiewa na 120 godzin pracy inżynieryjnej przy robotach przez pięć dni, co oznacza 24 godziny na dobę.

![Wymaganie na dzień](media/RM-how-to-22.png)

Jest to przykład sytuacji, kiedy do zaspokojenia żądania zasobu ogólnego potrzeba wielu nazwanych zasobów. W celu zrealizowania tego zapotrzebowania trzeba zarezerwować wiele zasobów.

![Rezerwowanie wielu zasobów w celu zaspokojenia wymagania](media/RM-how-to-23.png)

Główna różnica w tym scenariuszu polega na tym, że zasób ogólny pozostaje w zespole przypisanym do zadania, a członkowie zespołu będący zarezerwowanymi zasobami nazwanymi nie są przypisywani do zadania w ramach ich standardowych obowiązków. Menedżer projektu może odpowiednio przypisać pracę do nazwanych zasobów. Widok **Uzgadnianie** może pomóc menedżerowi projektu podzielić rezerwacje między wiele zasobów i przypisać im zadanie. Nie jest to wykonywane automatycznie, ponieważ w każdym scenariuszu bardziej skomplikowanym niż ten powyżej, na przykład gdy użytkownik ma pakiet zadań składających się na wymaganie, system musi uwzględnić sposób, w jaki Menedżer projektu zamierza dokonywać przypisań. Ponieważ system nie jest w stanie zrozumieć zamierzeń, założenia mogą być inne niż zamierzania i może wystąpić nieprawidłowy lub nieprzewidywalny rezultat. Przewidywany wynik jest taki, że zasób ogólny pozostanie przypisany do czasu, aż menedżer projektu jednoznacznie utworzyć przypisania za pomocą widoku **Uzgadnianie**.


