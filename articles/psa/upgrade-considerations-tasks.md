---
title: Zagadnienia dotyczące uaktualniania struktury podziału pracy
description: W tym temacie zamieszczono informacje dotyczące uaktualniania struktury podziału pracy w programie Project Service Automation z wersji 2.x do 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 5258813410c3cea015775898cc72ba1574549edd8ee0c8b7aad8c94943eb5a60
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992354"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Zagadnienia dotyczące uaktualniania struktury podziału pracy

[!include [banner](../includes/psa-now-project-operations.md)]

W tym temacie zamieszczono informacje dotyczące uaktualniania struktury podziału pracy w programie Project Service Automation z wersji 2.x do 3.x. Ten temat określa dobrą kondycję projektu w rozwiązaniu Project Service Automation (PSA), która jest niezbędna do pomyślnego uaktualnienia. Są tu również informacje o typowych sytuacjach blokowania, które spowodują niepowodzenie uaktualnienia. Aby uzyskać więcej informacji na temat definiowania zadań w projektach i ich funkcjach w harmonogramie projektu, zobacz [Harmonogramy projektów](project-creating.md).

## <a name="key-entities"></a>Kluczowe encje
Dokładna struktura podziału pracy, do której już załadowano zasoby, musi mieć następujące encje:

- [Projekt](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Zespół projektu](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Zadanie projektu](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Przypisania zasobów](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Zależność zadania projektu](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Zasoby, które można zarezerwować](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

W celu zdefiniowania struktury podziału pracy z załadowanymi zasobami należy wykonać następujące kroki:

1. Utwórz nowy projekt. Aby uzyskać więcej informacji na temat tworzenia nowego projektu, zobacz [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Utwórz jedno lub więcej zadań. Aby uzyskać więcej informacji na temat tworzenia zadania, zobacz [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Zdefiniuj zależności zadań. Aby uzyskać więcej informacji, zobacz [Zależność zadań projektu](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Przypisz członków zespołu projektu do projektu. Aby uzyskać więcej informacji, zobacz [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Przypisz członków zespołu projektu do zadań. Aby uzyskać więcej informacji, zobacz [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relacje w zespole projektu

W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:
- Wszyscy członkowie zespołu projektu muszą być skojarzeni z zasobami możliwymi do zarezerwowania.
- Wszyscy członkowie zespołu projektu muszą być skojarzeni z tym samym projektem. 

## <a name="project-task-relationships"></a>Relacje zadań projektu
W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:

- Wszystkie powiązane zadania muszą być skojarzone z tym samym projektem.
- Każde zadanie wiersza musi mieć zadanie nadrzędne.
- Każde zadanie musi mieć projekt nadrzędny.

### <a name="valid-conditions"></a>Obowiązujące warunki

- Wszystkie czasy trwania zadań muszą być większe lub równe (>=) jednej godzinie, a krótsze niż 1 800 000 minut (1250 dni).*
- Wszystkie zadania muszą mieć datę rozpoczęcia nie wcześniejszą niż 1 stycznia 2000 r.*
- Wszystkie zadania muszą mieć datę rozpoczęcia nie późniejszą niż 17 lat od bieżącego dnia.*
- Wszystkie zadania muszą mieć datę rozpoczęcia wcześniejszą niż data zakończenia lub jej równą.
- Wszystkie typy transakcji w klasyfikacjach (Wydatek, Materiał, Podatek i Czas) muszą mieć wartości w ustawieniach **Jednostka domyślna** i **Grupa jednostek**.
- Należy unikać używania formatów daty z literami.

### <a name="potential-mitigation-steps"></a>Potencjalne kroki ograniczenia ryzyka
- Użycie funkcji szukania zaawansowanego w celu zidentyfikowania zadań projektu, które nie zawierają identyfikatora projektu.
- Przy użyciu funkcji Szukanie zaawansowane można identyfikować zadania projektu, w których zaplanowany czas trwania jest większy niż > 1 800 000.
- Przed wprowadzeniem jakichkolwiek zmian w danych należy przeanalizować wszystkie dostosowania skojarzone z encją, które mogły doprowadzić do nieprawidłowego stanu danych. Te dostosowania należy rozwiązać przed kontynuowaniem jakichkolwiek aktualizacji dotyczących danych.
- W przypadku zidentyfikowanych oddzielonych zadań warto rozważyć ich usunięcie, jeśli nie są one potrzebne lub które powinny być skojarzone z poprawnym projektem nadrzędnym.
- W przypadku każdego zadania, w którym czas trwania wynosi więcej niż 1250 dni, warto rozważyć dodanie wielu zadań w celu przedstawienia łącznego czasu trwania, o ile jest to możliwe.

> [!NOTE]
> Elementy oznaczone gwiazdką (\*) mają ograniczenia wynikające z faktu, że system zarządzania relacjami z klientami (CRM) obsługuje tylko 7320 rozszerzeń cyklu. Należy pozostać poniżej tego limitu.

## <a name="resource-assignment-relationships"></a>Relacje przypisania zasobów
W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:

- Wszystkie przypisania zasobów w strukturze podziału pracy muszą być powiązane z tym samym projektem.
- Wszystkie przypisania zasobów w strukturze podziału pracy muszą być skojarzone z członkami zespołu projektu w tym samym projekcie.

### <a name="potential-mitigation-steps"></a>Potencjalne kroki ograniczenia ryzyka
- Zidentyfikuj wszystkie zadania, które nie mieszczą się poza powyższymi warunkami.  
- Wszystkie przydziały zasobów, które nie są już ważne, powinny zostać usunięte.

## <a name="project-task-dependency-relationships"></a>Relacje zależność zadań projektu
W celu zapewnienia pomyślnego uaktualnienia należy poprawnie utrzymywać następujące relacje:

- Wszystkie zależności zadań projektu muszą być powiązane z tym samym projektem.
- Zadanie może się odwoływać tylko raz do każdego elementu stanowiącego zależność.


[!INCLUDE[footer-include](../includes/footer-banner.md)]