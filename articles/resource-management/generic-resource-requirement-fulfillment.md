---
title: wRealizowanie ogólnych wymagań zasobów
description: Ta temat zawiera informacje na temat rezerwowania nazwanych zasobów na potrzeby ogólnego wymagania zasobu.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279601"
---
# <a name="generic-resource-requirement-fulfillment"></a>wRealizowanie ogólnych wymagań zasobów

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Można użyć nazwanego zasobu, aby zastąpić ogólny zasób mający wymaganie zasobu.

1. Na stronie **Projekty** wybierz pozycję **Zespół**.
2. Z listy wybierz zasób ogólny, który ma wymaganie zasobu, a następnie wybierz opcję **Zarezerwuj**. Możesz też otworzyć wymaganie zasobu, a następnie wybrać przycisk **Zarezerwuj**.
3. Na stronie **Asystent planowania** wybierz nazwany zasób, który ma zostać zarezerwowany do Twojego zespołu projektu, a następnie wybierz opcję **Zarezerwuj**.

Gdy rezerwacja jest zakończona i zaspokojona przez nazwany zasób, zasób ogólny jest zastępowany nazwanym zasobem.

Również przypisania w harmonogramie zostaną zaktualizowane o nazwany zasób.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Wypełnianie roli ogólnego zasobu wieloma nazwanym zasobami
Zaspokojenie wymagania na zasób ogólny za pomocą wielu nazwanych zasobów przypomina operację przypisania jednego nazwanego zasobu. Załóżmy na przykład, że istnieje zadanie o czasie trwania pięć dni i nakładzie pracy 120 godzin. Tego zadania nie może wykonać jeden zasób pracujący na typowej ośmiogodzinnej zmianie w pięciodniowym tygodniu pracy. 

Wymaganie opiewa na 120 godzin pracy inżynieryjnej przy robotach przez pięć dni, co oznacza 24 godziny na dobę.

Jest to przykład sytuacji, kiedy do zaspokojenia żądania zasobu ogólnego potrzeba wielu nazwanych zasobów. W celu zrealizowania tego zapotrzebowania trzeba zarezerwować wiele zasobów.

Główna różnica w tym scenariuszu polega na tym, że zasób ogólny pozostaje w zespole przypisanym do zadania, a członkowie zespołu będący zarezerwowanymi zasobami nazwanymi nie są przypisywani do zadania w ramach ich standardowych obowiązków. Menedżer projektu może odpowiednio przypisać pracę do nazwanych zasobów. Widok **Uzgadnianie** może pomóc menedżerowi projektu podzielić rezerwacje między wiele zasobów i przypisać im zadanie. Nie jest to wykonywane automatycznie, ponieważ w każdym scenariuszu bardziej skomplikowanym niż ten powyżej, na przykład gdy użytkownik ma pakiet zadań składających się na wymaganie lub system musi uwzględnić sposób, w jaki Menedżer projektu zamierza dokonywać przypisań. Ponieważ system nie jest w stanie zrozumieć zamierzeń, prawdopodobnie założenia mogą być inne niż zamierzone i może wystąpić nieprawidłowy lub nieprzewidywalny rezultat. Przewidywany wynik jest taki, że zasób ogólny pozostanie przypisany do czasu, aż menedżer projektu jednoznacznie utworzyć przypisania za pomocą widoku **Uzgadnianie**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]