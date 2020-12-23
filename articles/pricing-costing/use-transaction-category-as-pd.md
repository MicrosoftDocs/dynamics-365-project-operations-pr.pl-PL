---
title: Używanie kategorii transakcji jako wymiaru kalkulacji cen
description: Ten temat zawiera informacje na temat sposobu używania pola kategorii transakcji jako wymiaru kalkulacji cen.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514012"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Używanie kategorii transakcji jako wymiaru kalkulacji cen


_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


W tym temacie wyjaśniono, jak używać pola **Kategoria transakcji** jako wymiaru kalkulacji cen. 

## <a name="prerequisites"></a>Wymagania wstępne
Przed wykonaniem procedur z tego tematu musisz mieć nowe rozwiązanie do obsługi wymiarów kalkulacji cen dla organizacji. Jeśli jeszcze tego nie zrobiono, zobacz [Tworzenie pól i encji niestandardowych jako wymiarów kalkulacji cen](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Dodawanie pola Kategoria transakcji do formularzy i widoków
Aby pole **kategorii transakcji** było widoczne w rozwiązaniu obsługującym wymiarami kalkulacji cen, należy dodać pole do wszystkich formularzy i widoków jako encję.

W poniższej tabeli wymieniono wszystkie gotowe formularze i widoki według encji. Konieczne będzie również dodanie nowego pola do dodatkowych formularzy lub widoków w encjach niestandardowych.

|  Jednostka        | Formularze     |Widoki        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roli| Informacja |- Aktywne ceny kategorii zasobów<br> - Skojarzone ceny kategorii zasobów |
|  Narzut na cenę dla roli| Informacja|- Aktywny narzut na cenę dla roli<br>- Skojarzony narzut na cenę dla roli |
|  Szczegóły wiersza oferty|- Informacje o projekcie<br>- Szybkie tworzenie projektów| - Aktywne szczegóły wierszy ofert<br>- Połączone szczegóły wierszy ofert<br>- Skojarzone szczegóły wierszy oferty |
|  Szczegóły pozycji kontraktu projektu|- Informacje o projekcie<br>- Szybkie tworzenie projektów|- Połączone szczegóły pozycji kontraktu<br>- Aktywne szczegóły pozycji kontraktu<br>- Skojarzone szczegóły pozycji kontraktu |
|  Zadanie projektu|- Informacje<br>- Nowy formularz| &nbsp; |
|  Członek zespołu projektu|- Informacje<br>- Nowy formularz|- Aktywni członkowie zespołu projektu<br>- Członkowie zespołu projektu<br>- Skojarzeni członkowie zespołu projektu |
|  Wpis czasu|- Informacje<br>- Tworzenie wpisu czasu|- Moje wpisy czasu według daty<br>- Moje wpisy czasu w tym tygodniu<br>- Wpisy czasu do zatwierdzenia|
|  Wiersz arkusza|- Informacje<br>- Szybkie tworzenie|- Aktywne wiersze arkuszy<br>- Skojarzony wiersz arkusza|
|  Szczegóły wiersza faktury|- Informacje<br>- Szybkie tworzenie|- Aktywne szczegóły wierszy faktur<br>- Odpłatne transakcje faktury<br>- Uzupełniające transakcje faktury<br>- Skojarzone szczegóły wiersza faktury <br>- Nieodpłatne transakcje faktury|
|  Rzeczywiste|- Informacje<br>- Aktywne wartości rzeczywiste| Skojarzona wartość rzeczywista |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Konfigurowanie pola kategorii transakcji jako wymiaru kalkulacji cen

1. Wybierz kolejno pozycje **Ustawienia** > **Parametry**. 
2. Na stronie **Parametry** na karcie **Wymiary kalkulacji cen oparte na kwocie** sprawdź, czy siatka pokazuje rekordy z encji **Wymiary kalkulacji cen**.
3. Dodaj pozycję **Kategoria transakcji** do tej listy, a w polach **Ma zastosowanie do kosztu** i **Ma zastosowanie do sprzedaży** ustaw wartość **Tak**.
4. W polu **Typ wymiaru** zaznacz opcję **Oparty na kwocie**, a następnie dla ustawienia **Kategoria transakcji** wybierz priorytet powiązany z kosztem i sprzedażą.
