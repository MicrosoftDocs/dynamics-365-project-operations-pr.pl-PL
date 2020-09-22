---
title: Używanie kategorii transakcji jako wymiaru kalkulacji cen
description: Ten temat zawiera informacje na temat używania kategorii transakcji jako wymiaru kalkulacji cen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754396"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Używanie kategorii transakcji jako wymiaru kalkulacji cen
W tym temacie pokazano, jak używać kategorii transakcji w roli wymiaru kalkulacji cen. Jeśli przed rozpoczęciem pracy jeszcze nie utworzono rozwiązania do zarządzania wymiarami kalkulacji cen, trzeba je utworzyć. Jeśli istnieje już rozwiązanie do zarządzania wymiarami kalkulacji cen, można wprowadzić w nim zmiany. Jeśli w organizacji nie utworzono nowego rozwiązania do zarządzania wymiarami kalkulacji cen, należy wykonać procedury opisane w temacie [Tworzenie niestandardowych pól i encji](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Dodawanie kategorii transakcji do formularzy i widoków
Aby kategoria transakcji była widoczna w interfejsie użytkownika w rozwiązaniu do zarządzania wymiarami kalkulacji cen, należy przejść przez wszystkie formularze i widoki kluczowych encji oraz dodać te pola do formularzy i widoków tych encji.
Poniższa tabela zawiera wyczerpującą listę gotowych formularzy i widoków, wyszczególnionych według encji, które należy zaktualizować o te pola. Jeśli którekolwiek dodatkowe widoki lub formularze w dostosowaniach korzystają z tych encji, należy dodać nowe pola również do nich.

|  Encja        | Formularze     |Widoki        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roli|• Informacja |• Aktywne ceny kategorii zasobów<br> • Widok skojarzony ceny kategorii zasobów|
|  Narzut na cenę dla roli|• Informacja|• Aktywny narzut na cenę dla roli<br>• Widok skojarzony narzutu na cenę dla roli|
|  Szczegóły wiersza oferty|• Informacje o projekcie<br>• Szybkie tworzenie projektów|• Aktywne szczegóły wierszy ofert<br>• Połączone szczegóły wierszy ofert<br>• Widok skojarzony szczegółów wierszy oferty|
|  Szczegóły pozycji kontraktu projektu|• Informacje o projekcie<br>• Szybkie tworzenie projektów|• Połączone szczegóły pozycji kontraktu<br>• Aktywne szczegóły pozycji kontraktu<br>• Widok skojarzony szczegółów pozycji kontraktu|
|  Członek zespołu projektu|• Informacja<br>• Nowy formularz|• Aktywni członkowie zespołu projektu<br>• Członkowie zespołu projektu<br>• Widok skojarzony członków zespołu projektu|
|  Wpis czasu|• Informacja<br>• Utwórz wpis czasu|• Moje wpisy czasu według daty<br>• Moje wpisy czasu w tym tygodniu<br>• Wpisy czasu do zatwierdzenia|
|  Wiersz arkusza|• Informacja<br>• Szybkie tworzenie|• Aktywne wiersze arkuszy<br>• Widok skojarzony wiersza arkusza|
|  Szczegóły wiersza faktury|• Informacja<br>• Szybkie tworzenie|• Aktywne szczegóły wierszy faktur<br>• Odpłatne transakcje faktury<br>• Uzupełniające transakcje faktury<br>• Widok skojarzony szczegółów wiersza faktury<br>• Nieodpłatne transakcje faktury|
|  Wartość rzeczywista|• Informacja<br>• Aktywne wartości rzeczywiste|• Widok skojarzony wartości rzeczywistej|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Konfigurowanie kategorii transakcji jako wymiaru kalkulacji cen

1. W interfejsie internetowym wybierz kolejno opcje **Project Service** > **Ustawienia** > **Parametry**. 
2. Na stronie **Parametry** na karcie **Wymiary kalkulacji cen oparte na kwocie** zwróć uwagę, że siatka na karcie pokazuje rekordy z encji **Wymiary kalkulacji cen**.
3. Dodaj pozycję **Kategoria transakcji** do tej listy, a w polach **Ma zastosowanie do kosztu** i **Ma zastosowanie do sprzedaży** ustaw wartość **Tak**.
4. W polu **Typ wymiaru** zaznacz opcję **Oparty na kwocie**, a następnie dla ustawienia **Kategoria transakcji** wybierz priorytet dotyczący kosztu i sprzedaży.
