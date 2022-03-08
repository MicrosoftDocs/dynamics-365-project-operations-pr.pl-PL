---
title: Zagadnienia dotyczące uaktualniania — Microsoft Dynamics 365 Project Service Automation z wersji 2.x lub 1.x do wersji 3
description: W tym temat zamieszczono informacje na temat zagadnień, które należy wziąć pod uwagę podczas uaktualniania programu Project Service Automation w wersji 2.x lub 1.x do wersji 3.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 19d6d312c7cedd2d7b9b5649452b85dd24fae761
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082092"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Zagadnienia dotyczące uaktualniania — PSA z wersji 2.x lub 1.x do wersji 3.x
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation i Field service
Zarówno Dynamics 365 Project Service Automation, jak i Dynamics 365 Field Service używają rozwiązania Universal Resourcing Scheduling (URS) dla planowania zasobów. Jeśli w danym wystąpieniu jest dostępne zarówno rozwiązanie Project Service Automation, jak i Field Service, należy zaplanować uaktualnianie obu rozwiązań do najnowszej wersji (wersja 3 x w przypadku Project Service Automation, wersja 8.x w przypadku Field Service). Uaktualnianie Project Service Automation lub Field Service spowoduje zainstalowanie najnowszej wersji programu URS, co oznacza, że niespójne zachowanie będzie możliwe, jeśli rozwiązania Project Service Automation i Field Service w tym samym wystąpieniu nie zostaną uaktualnione do najnowszej wersji.

## <a name="resource-assignments"></a>Przypisania zasobów
W programie Project Service Automation w wersji 2 i w wersji 1 przydziały zadań były przechowywane jako zadania podrzędne (nazywane również zadaniami wierszowymi) w **Encji zadanie** **i pośrednio powiązane z encją przydziału zasobu**. Zadanie wiersza było widoczne w wyskakującym okienku przypisań w strukturze podziału pracy (SPP).

![Zadania związane z wierszami w SPP w programie Project Service Automation w wersji 2 i wersji 1](media/upgrade-line-task-01.png)

W wersji 3 programu Project Service Automation wprowadzono zmiany w schemacie przypisywania zasobów, które można zarezerwować. Zadanie wierszowe nie zostało zastąpione i istnieje bezpośrednia relacja 1:1 między zadaniem w **encji zadanie** a członkiem zespołu w encji **przydział zasobu**. Zadania przypisywane członkom zespołu projektu są obecnie przechowywane bezpośrednio w encji przydział zasobu.  

Te zmiany wpływają na uaktualnianie istniejących projektów, które mają przydziały zasobów dla nazwanych zasobów i zasobów ogólnych w zespole projektu. W tym temacie przedstawiono kwestie, które należy wziąć pod uwagę podczas uaktualniania do wersji 3. 

### <a name="tasks-assigned-to-named-resources"></a>Zadania przypisane do nazwanych zasobów
Przy użyciu encji zadania podstawowego zadania w wersji 2 i w wersji 1 zezwalały członkom zespołu na przedstawianie roli innej niż ich domyślna zdefiniowana rola. Na przykład Hanna Krawczyk z domyślnie przypisaną rolą Menedżer programu można było przypisać do zadania z rolą dewelopera. W wersji 3 rola nazwanego członka zespołu jest zawsze domyślna, więc każde zadanie, do którego jest przypisana Hanna Krawczyk, używa jej domyślnej roli Menedżer programu.

Jeśli do zadania przypisano zasób poza rolą domyślną w wersji 2 i w wersji 1, podczas uaktualniania, nazwany zasób zostanie przypisany do domyślnej roli dla wszystkich przypisań zadania bez względu na przypisanie roli w wersji 2. Spowoduje to rozbieżności w obliczonych oszacowaniach z wersji 2 lub wersji 1 do wersji 3, ponieważ oszacowania są obliczane na podstawie roli zasobu, a nie przypisanego zadania. Na przykład w wersji 2 przypisano dwa zadania do Bogumiły Kowalczyk. Rolą zadania wierszowego dla zadania 1 jest Deweloper, a dla zadania 2 — Menedżer programu. Bogumiła Kowalczyk ma domyślną rolę menedżera programu.

![Wiele ról przypisanych do jednego zasobu](media/upgrade-multiple-roles-02.png)

Z uwagi na fakt, że role Deweloper i Menedżer programu różnią się, koszty i oszacowania sprzedaży są następujące:

![Oszacowania kosztów dla ról zasobów](media/upggrade-cost-estimates-03.png)

![Oszacowania sprzedaży dla ról zasobów](media/upgrade-sales-estimates-04.png)

Po uaktualnieniu do wersji 3 zadania wierszy są zastępowane przydziałami zasobów na zadanie członka zespołu zasobu możliwego do zarezerwowania. Przypisanie będzie używać domyślnej roli zasobu możliwego do zarezerwowania. W poniższym rysunku Bogumiła Kowalczyk, która ma rolę Menedżer programu, jest zasobem.

![Przypisania zasobów](media/resource-assignment-v2-05.png)

Ponieważ oszacowania są oparte na domyślnej roli zasobu, oszacowania dotyczące sprzedaży i kosztów mogą ulec zmianie. Należy zauważyć, że na poniższym rysunku nie jest już widoczna rola **dewelopera**, ponieważ jest ona obecnie pobierana z roli domyślnej zasobu możliwego do zarezerwowania.

![Szacowana wartość sprzedaży dla ról domyślnych](media/resource-assignment-cost-estimate-06.png)
![Szacowana wartość sprzedaży dla ról domyślnych](media/resource-assignment-sales-estimate-07.png)

Po zakończeniu uaktualniania można dokonać edycji roli członka zespołu i zmienić przypisaną wartość domyślną. Jeśli jednak użytkownik zmieni rolę członka zespołu, będzie ona modyfikowana we wszystkich przydzielonych zadaniach, ponieważ członkowie zespołu nie mogą mieć przydzielonych wielu ról w wersji 3.

![Aktualizowanie roli zasobu](media/resource-role-assignment-08.png)

Ma to także zastosowanie w przypadku zadań wiersza, które przypisano do nazwanych zasobów, gdy użytkownik zmieni jednostkę organizacyjną zasobu z domyślnej na inną. Po zakończeniu uaktualniania wersji 3 przypisanie będzie używać domyślnej jednostki organizacyjnej zasobu zamiast zestawu określonego w zadaniu wierszowym.

### <a name="tasks-assigned-to-generic-resources"></a>Zadania przypisane do zasobów ogólnych
W wersji 2 i w wersji 1 można ustawić rolę i jednostkę organizacyjną dla zadania, a następnie użyć funkcji **generowania zespołu** w celu utworzenia zasobów ogólnych na podstawie atrybutów ustawionych dla zadania. W wersji 3 są tworzeni ogólni członkowie zespołu z rolą i jednostką organizacyjną, a następnie zostają przypisani do zadania.

W wersji 2 i w wersji 1 projekty z zasobami ogólnymi mogą znajdować się w dwóch stanach lub mogą się mieszać na poziomie zadania. Na przykład możliwe są następujące scenariusze:

- Zadania z ustawionymi rolami i jednostkami organizacyjnymi, ale nie wygenerowano przypisania zasobu powiązanego.
- Zadania mające przydziały ogólnych członków zespołu, które były przypisywane przez utworzenie zasobu ogólnego przy użyciu funkcji **generowania zespołu**.

Zaleca się, aby przed rozpoczęciem uaktualnienia utworzyć ponownie zespół dla każdego projektu, który ma zadania przydzielone do zasobów ogólnych lub który nie ma jeszcze uruchomionego procesu generowania zespołu.

W przypadku zadań przypisanych ogólnym członkom zespołu wygenerowanym podczas **generowania zespołu** aktualizacja pozostawi zasób ogólny w zespole i pozostawi przypisanie do ogólnego członka zespołu. Zaleca się wygenerowanie wymagania zasobu dla ogólnego członka zespołu po aktualizacji, ale przed zarezerwowaniem lub przesłaniem żądania zasobu. Spowoduje to zachowanie wszystkich przydziałów jednostek organizacyjnych ogólnych członków zespołu innych niż kontraktująca jednostka organizacyjna projektu.

Na przykład w Projekcie Z kontraktującą jednostką organizacyjną jest Contoso US. W planie projektu do zadań testowania w fazie implementacji przypisano role doradców technicznych, a przypisaną jednostką organizacyjną jest Contoso India.

![Przypisanie organizacyjne fazy implementacji](media/org-unit-assignment-09.png)

Po zakończeniu fazy implementacji zadanie testowe integracji jest przypisywane do doradcy technicznego, ale organizacja jest ustawiona jako Contoso US.  

![Przypisanie organizacyjne zadania testowania integracji](media/org-unit-generate-team-10.png)

Po wygenerowaniu zespołu dla projektu system tworzy dwóch ogólnych członków zespołu z powodu różnych jednostek organizacyjnych tych zadań. Konsultant techniczny 1 zostanie przypisany do zadania w Contoso India, a Konsultant techniczny 2 zostanie przypisany do zadania w Contoso US.  

![Wygenerowani ogólni członkowie zespołu](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> W programie Project Service Automation w wersji 2 i wersji 1 członek zespołu nie utrzymuje jednostki organizacyjnej, która jest przechowywana w zadaniu wierszowym.

![Zadania wierszowe w wersji 2 i wersji 1 w programie Project Service Automation](media/line-tasks-12.png)

Jednostkę organizacyjną można wyświetlić w widoku oszacowania. 

![Oszacowania dotyczące jednostki organizacyjnej](media/org-unit-estimates-view-13.png)
 
Po zakończeniu uaktualniania jednostka organizacyjna w zadaniu wiersza odpowiadającemu ogólnemu członkowi zespołu jest dodawana do członka zespołu ogólnego, a zadanie wierszowe jest usuwane. Z tego powodu zaleca się, aby przed uaktualnieniem utworzyć lub ponownie wygenerować zespół dla każdego projektu, który zawiera zasoby ogólne.

W przypadku zadań przydzielonych do roli w jednostce organizacyjnej innej niż jednostka organizacyjna kontraktująca i zespół nie został wygenerowany, uaktualnianie spowoduje utworzenie ogólnego członka zespołu dla roli, ale będzie używana jednostka kontraktująca projektu dla jednostki organizacyjnej członka zespołu. Odwołując się do przykładu z Projektem Z, oznacza to, że kontraktująca jednostka organizacyjna Contoso US i zadania testowania planu projektu w fazie implementacji mają przypisaną rolę konsultanta technicznego z jednostką organizacyjną przypisaną do Contoso India. Zadanie testowe integracji zakończone po fazie implementacji zostało przypisane do roli konsultanta technicznego. Jednostka organizacyjna to Contoso US, a zespół nie został wygenerowany. Uaktualnianie spowoduje utworzenie jednego ogólnego członka zespołu, konsultanta technicznego, z przypisanymi godzinami wszystkich trzech zadań oraz jednostką organizacyjną Contoso US, czyli kontraktującą jednostką organizacyjną danego projektu.   
 
Zmiana domyślnych ustawień w różnych jednostkach organizacyjnych zasobów dla niewygenerowanych członków zespołu jest powodem, dla którego zalecamy wygenerowanie lub ponowne wygenerowanie zespołu dla każdego projektu, zawierającego zasoby ogólne przed uaktualnieniem, aby nie utracić przypisań jednostki organizacyjnej.

