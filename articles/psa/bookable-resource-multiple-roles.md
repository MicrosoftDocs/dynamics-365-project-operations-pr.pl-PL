---
title: Szacowanie sprzedaży projektu i kosztów, gdy zasób udostępniany wypełnia wiele ról w projekcie
description: W tym temat przedstawiono informacje na temat sposobu, w jaki można użyć wymiarów kalkulacji cen do obsługi kalkulacji cen i wycen zasobu, który wypełnia wiele ról w projekcie.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082064"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Szacowanie sprzedaży projektu i kosztów, gdy zasób udostępniany wypełnia wiele ról w projekcie 

Przedsiębiorstwa oparte na projektach często muszą dysponować jednym zasobem, aby wykonywać wiele ról w projekcie. Każda z tych ról może mieć odmienną cenę i różny koszt, co oznacza, że czas zasobu w projekcie może mieć różny szacunek finansowy w zależności od stawek za fakturę i stawki kosztów dla poszczególnych ról. Rozwiązanie Project Service Automation zezwala na konfigurowanie wartości w rekordach członków zespołu dla nazwanego zasobu i zezwala na różne zastąpienia dla każdego zadania, do którego jest przypisany członek zespołu.

W poniższym przykładzie wyjaśniono, jak to proste zastąpienie tej wartości umożliwia zasobowi korzystanie z wielu ról w projekcie z różnymi stawkami kosztów i fakturowania.

## <a name="create-tasks"></a>Tworzenie zadań
Utwórz dwa zadania projektu, każde dla 40 godzin, zadanie a i zadanie B. Wybierz zadanie A jako poprzednik zadania B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Skonfiguruj rolę i jednostkę organizacyjną dla ogólnego członka zespołu projektu

1. Na stronie **harmonogram** wybierz wiersz **zadania** dla zadania A. 
2. W polu **zasoby** listy rozwijanej wybierz pozycję **Utwórz**.
3. Na stronie **Szybkie tworzenie członków zespołu** określ atrybuty ogólnego członka zespołu, który będzie mógł wykonać to zadanie.
4. Wybierz odpowiednią rolę i jednostkę organizacyjną, a następnie wybierz pozycję **Zapisz i zamknij**. Ogólny członek zespołu zostaje utworzony i przypisany do tego zadania. 

Powtórz te kroki dla zadania B i upewnij się, że rola i jednostka organizacyjna w ogólnym członku zespołu utworzonym dla zadania B są inna niż dla zadania A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Skonfiguruj rolę i jednostkę organizacyjną dla zadania projektu

1. Po utworzeniu zadania A wybierz zadanie, a następnie wybierz pozycję **Edytuj zadanie**.
2. Na stronie **Szczegóły zadania** znajdź pola **Rola** i **Jednostka organizacyjna** , dodaj wartości wymagane dla zasobu, który wykona to zadanie. 

  > [!NOTE]
  > W przypadku wykonywania tych scenariuszy przy użyciu danych demonstracyjnych w programie Project Service Automation wybierz opcję **Potencjalny klient konsultingowy** dla roli oraz **Fabrikam US** jako jednostkę organizacyjną.

3. Wybierz zadanie B, a następnie wybierz **Edytuj zadanie**.
4. Na stronie **Szczegóły zadania** znajdź pola **Rola** i **Jednostka organizacyjna** , dodaj wartości wymagane dla zasobu, który wykona to zadanie. Upewnij się, że wartości pól **Rola** i **Jednostka organizacyjna** różnią się między zadaniem B i zadaniem A. 

  > [!NOTE]
  > W przypadku wykonywania tych scenariuszy przy użyciu danych demonstracyjnych w programie Project Service Automation wybierz opcję **Technik sieciowy** dla roli oraz **Fabrikam US** jako jednostkę organizacyjną.

5. Zapisz i zamknij stronę **Szczegóły zadania**. 

## <a name="team-member-and-estimates-behaviour"></a>Członek zespołu i oszacowania zachowania 

1. Na stronie **Szczegóły zadania** w **Członek zespołu** wybierz dwóch ogólnych członków zespołu, a następnie wybierz opcję **Generuj wymagania**. Wygeneruje to wymagania zasobu. 
2. Wybierz wiersz członka zespołu do **Potencjalny klient konsultingowy** i wybierz pozycję **Rezerwuj**. Tablica harmonogramu zostanie otwarta i zostanie zarezerwowany zasób dla tego wymagania.
3. Wybierz wiersz członka zespołu do **Technik sieciowy** i wybierz pozycję **Rezerwuj**. Tablica harmonogramu zostanie otwarta i zostanie zarezerwowany ten sam zasób dla tego wymagania.

### <a name="team-member-grid"></a>Siatka członka zespołu 
Zwróć uwagę, że w siatce **członków zespołu** są usuwane dwa podstawowe rekordy członków zespołu i są one zastąpione jednym zasobem. Dla tego zasobu istnieje jeden zestaw wartości, który zawiera domyślny zestaw wartości dla **Roli** i **Jednostki organizacyjnej**.
Po rozwinięciu wiersza rekordu tego członka zespołu można wyraźnie zobaczyć przypisania da obu tych zadań w rekordzie członka zespołu. Każdy wiersz przypisania zawiera specyficzne wartości zadania dla **Roli** i **Jednostki organizacyjnej**. 

### <a name="estimates-grid"></a>Siatka szacowań 
Kiedy przechodzisz do siatki **Szacowań** , zauważysz, że oba przypisania dotyczące tego samego zasobu będą w różny sposób wycenione.
Przypisanie zasobu w zadaniu A ma cenę ustaloną za pomocą wartości atrybutu **Rola** **Potencjalnego klienta konsultingowego**. Przypisanie tego samego zasobu w zadaniu B ma cenę ustaloną za pomocą wartości atrybutu **Rola** **Technika sieciowego**.





