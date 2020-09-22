---
title: Zmiany w zarządzaniu zasobami (Project Service Automation wer. 3.x)
description: Ten temat zawiera informacje o zmianach w obszarze Zarządzanie zasobami.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754343"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Zmiany w zarządzaniu zasobami (Project Service Automation wer. 3.x)

Sekcje tego tematu zawierają informacje o zmianach wprowadzonych w obszarze Zarządzanie zasobami w programie Dynamics 365 Project Service Automation w wersji 3.x.

## <a name="project-estimates"></a>Szacowania projektu

Szacunki projektu już nie opierają się na encji **msdyn\_projecttask** (**Zadanie projektu**), ale na encji **msdyn\_resourceassignment** (**Przypisanie zasobu**). Przypisania zasobów stały się „źródłem prawdziwych informacji” dla aparatów planowania zadań i kalkulacji cen.

## <a name="line-tasks"></a>Zadania wierszy

W programie PSA 3.x funkcjonalność zadań wierszy została wycofana. Obecnie przypisania wskazują całe zadanie, a nie poszczególne wiersze zadania.

W poniższym przykładzie pokazano, jak zadanie o nazwie „Zadanie testowe” jest przypisywane członkom zespołu A i B w starszych wersjach programu PSA i w wersji PSA 3.x.

- **Przed wersją PSA 3.x:**

    - Zadanie testowe

        - Zadanie testowe — zadanie wiersza 1

            - Przypisanie do osoby A

        - Zadanie testowe — zadanie wiersza 2

            - Przypisanie do osoby B

- **PSA 3.x:**

    - Zadanie testowe

        - Przypisanie do osoby A
        - Przypisanie do osoby B

## <a name="unassigned-assignment"></a>Nieprzydzielone przypisanie

W programie PSA 3.x nieprzydzielone przypisanie to takie, które zostało przypisane do członka zespołu **NULL** i zasobu **NULL**. Nieprzydzielone przypisania mogą występować w różnych scenariuszach:

- Jeśli zadanie zostało utworzone, ale nie zostało jeszcze przypisane żadnemu członkowi zespołu, zawsze jest tworzone nieprzydzielone przypisanie. 
- Jeśli wszystkie osoby przypisane do zadania zostaną usunięte, dla tego zadania zostanie ponownie utworzone nieprzydzielone przypisanie.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Pola planowania w encji Zadanie projektu

Pola w encji **msdyn\_projecttask** zostały wycofane lub przeniesione do encji **msdyn\_resourceassignment** albo są obecnie przywoływane przez encję **msdyn\_projectteam** (**Członek zespołu projektu**).

| Wycofane pole w encji msdyn\_projecttask (Zadanie projektu) | Nowe pole w encji msdyn\_resourceassignment (Przypisanie zasobu) | Komentarz |
|---|---|---|
| msdyn\_assignedresources | Brak | |
| msdyn\_assignedteammembers | Brak | |
| msdyn\_numberofresources | Brak | |
| msdyn\_scheduledhours | Brak | |
| msdyn\_effortcontour | msdyn\_plannedwork | Zmieniła się struktura danych formatu JavaScript Object Notation (JSON) przechowywana w polu. |

## <a name="schedule-contour"></a>Rozkład harmonogramu

Rozkład harmonogramu jest przechowywany w polu **Zaplanowana praca** (**msdyn\_plannedwork**) każdej encji **Przypisanie zasobu** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktura

Nowa struktura rozkładu harmonogramu składa się z elastycznych fragmentów czasu, które są definiowane dla każdego dnia harmonogramu. Każdy fragment czasu ma następujące właściwości:

- **Początek** — początek godzin pracy w dniu, zgodnie z kalendarzem projektu.
- **Koniec** — koniec godzin pracy w dniu, zgodnie z kalendarzem projektu.
- **Godziny** — liczba godzin przypisana do dnia.

**Przykład**

W tym przykładzie jest używany kalendarz projektu, w którym dzień roboczy trwa od 9.00 do 17.00 w strefie czasowej UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Planowanie automatyczne i ręczne

Jeśli zadanie jest planowane automatycznie, system stara się zmieścić jak najwięcej godzin na początku i czas trwania zadania może wtedy zostać skrócony.

**Przykład**

Poniższe zadanie zostało zaplanowane automatycznie na 18 godzin w ciągu trzech dni (od 3 grudnia 2018 r. do 5 grudnia 2018 r.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Jeśli zadanie jest planowane ręcznie, godziny są rozmieszczane równo między wszystkie dni.

**Przykład**

Poniższe zadanie zostało zaplanowane ręcznie na 18 godzin w ciągu trzech dni (od 3 grudnia 2018 r. do 5 grudnia 2018 r.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Jednostka przypisania

Funkcjonalność jednostki przypisania została wycofana w programie PSA 3.x. Godziny nakładu pracy zadania są obecnie równo dzielone w ciągu dnia między wszystkie przypisane zasoby.

**Przykład**

W tym przykładzie zadanie zostało przypisane do dwóch zasobów i automatycznie zaplanowane na 36 godzin w ciągu trzech dni (od 3 grudnia 2018 r. do 5 grudnia 2018 r.).

- Przypisanie 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Przypisanie 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Wymiary kalkulacji cen

W programie PSA 3.x pola wymiaru kalkulacji cen specyficzne dla zasobów (takie jak **Rola** i **Jednostka organizacyjna**) zostały usunięte z encji **msdyn\_projecttask**. Te pola można teraz pobrać od odpowiedniego członka zespołu projektu (**msdyn\_projectteam**) w przypisaniu zasobu (**msdyn\_resourceassignment**) podczas generowania oszacowań projektu. Do encji **msdyn\_projectteam** dodano nowe pole **msdyn\_organizationalunit**.

| Wycofane pole w encji msdyn\_projecttask (Zadanie projektu) | Pola z encji msdyn\_projectteam (Członek zespołu projektu) używane w zamian |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Rozkłady

Pola rozkładu kalkulacji cen i szacowania zostały wycofane z encji **msdyn\_projecttask**. Zostały przeniesione do encji **msdyn\_resourceassignment**.

| Wycofane pole w encji msdyn\_projecttask (Zadanie projektu) | Nowe pole w encji msdyn\_resourceassignment (Przypisanie zasobu) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Następujące pola zostały dodane do encji **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

W encji **msdyn\_projecttask** nie zmieniono następujących pól kosztu ani sprzedaży planowanych, rzeczywistych i pozostałych:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
