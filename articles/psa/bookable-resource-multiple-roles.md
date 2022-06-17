---
title: Szacowanie sprzedaży i kosztów projektu, gdy zasób z możliwością rezerwowania pełni wiele ról w projekcie
description: W tym artykule przedstawiono informacje na temat sposobu wykorzystania rozmiarów kalkulacji cen do obsługi kalkulacji cen i kosztów zasobu, który pełni wiele ról w projekcie.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5adaa7b83aae69c15aa268e723417172f1b56f42
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916163"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Szacowanie sprzedaży i kosztów projektu, gdy zasób z możliwością rezerwowania pełni wiele ról w projekcie 

[!include [banner](../includes/psa-now-project-operations.md)]

W firmach opartych na projektach często jeden zasób musi wypełnić wiele ról w projekcie. Każda z tych ról może mieć odmienną cenę i różny koszt, co oznacza, że czas zasobu w projekcie może mieć różny szacunek finansowy w zależności od stawek za fakturę i stawki kosztów dla poszczególnych ról. Rozwiązanie Project Service Automation zezwala na konfigurowanie wartości w rekordach członków zespołu dla nazwanego zasobu i zezwala na różne zastąpienia dla każdego zadania, do którego jest przypisany członek zespołu.

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
2. Na stronie **Szczegóły zadania** znajdź pola **Rola** i **Jednostka organizacyjna**, dodaj wartości wymagane dla zasobu, który wykona to zadanie. 

  > [!NOTE]
  > W przypadku wykonywania tych scenariuszy przy użyciu danych demonstracyjnych w programie Project Service Automation wybierz opcję **Potencjalny klient konsultingowy** dla roli oraz **Fabrikam US** jako jednostkę organizacyjną.

3. Wybierz zadanie B, a następnie wybierz **Edytuj zadanie**.
4. Na stronie **Szczegóły zadania** znajdź pola **Rola** i **Jednostka organizacyjna**, dodaj wartości wymagane dla zasobu, który wykona to zadanie. Upewnij się, że wartości w polach **Rola** i **Jednostka organizacyjna** różnią się dla zadania B od wartości dla zadania A. 

  > [!NOTE]
  > W przypadku wykonywania tych scenariuszy przy użyciu danych demonstracyjnych w programie Project Service Automation wybierz opcję **Technik sieciowy** dla roli oraz **Fabrikam US** jako jednostkę organizacyjną.

5. Zapisz i zamknij stronę **Szczegóły zadania**. 

## <a name="team-member-and-estimates-behavior"></a>Zachowanie członków zespołu i szacowań 

1. Na stronie **Szczegóły zadania** w **Członek zespołu** wybierz dwóch ogólnych członków zespołu, a następnie wybierz opcję **Generuj wymagania**. 
2. Wybierz wiersz członka zespołu do **Potencjalny klient konsultingowy** i wybierz pozycję **Rezerwuj**. Tablica harmonogramu zostanie otwarta i zostanie zarezerwowany zasób dla tego wymagania.
3. Wybierz wiersz członka zespołu do **Technik sieciowy** i wybierz pozycję **Rezerwuj**. Tablica harmonogramu zostanie otwarta i zostanie zarezerwowany ten sam zasób dla tego wymagania.

### <a name="team-member-grid"></a>Siatka członka zespołu 
Zwróć uwagę, że w siatce **członków zespołu** są usuwane dwa podstawowe rekordy członków zespołu i są one zastąpione jednym zasobem. Dla tego zasobu istnieje jeden zestaw wartości, który zawiera domyślny zestaw wartości dla **Roli** i **Jednostki organizacyjnej**.
Po rozwinięciu wiersza rekordu tego członka zespołu można wyraźnie zobaczyć przypisania da obu tych zadań w rekordzie członka zespołu. Każdy wiersz przypisania zawiera specyficzne wartości zadania dla pól **Rola** i **Jednostka organizacyjna**. 

### <a name="estimates-grid"></a>Siatka szacowań 
Kiedy przechodzisz do siatki **Szacowań**, zauważysz, że oba przypisania dotyczące tego samego zasobu będą w różny sposób wycenione.
Przypisanie zasobu w zadaniu A ma cenę ustaloną za pomocą wartości atrybutu **Rola** **Potencjalnego klienta konsultingowego**. Przypisanie tego samego zasobu w zadaniu B ma cenę ustaloną za pomocą wartości atrybutu **Rola** **Technika sieciowego**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
