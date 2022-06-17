---
title: Używanie zasobu możliwego do zarezerwowania jako wymiaru kalkulacji cen
description: Ten artykuł zawiera informacje na temat używania zasobu możliwego do zarezerwowania jako wymiaru kalkulacji cen.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c467c45885bbd8931eccc75862f537c0f46433ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914829"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Używanie zasobu możliwego do zarezerwowania jako wymiaru kalkulacji cen

 _**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_ 

Ten artykuł zawiera informacje na temat używania zasobu możliwego do zarezerwowania jako wymiaru kalkulacji cen. Jeśli strategia kalkulacji cen została skonfigurowana tak, że każdy zasób z możliwością rezerwacji musi mieć określoną cenę lub stawkę kosztów, można użyć zasobu z możliwością rezerwacji jako wymiaru kalkulacji cen.

## <a name="prerequisites"></a>Wymagania wstępne
Przed zakończeniem procedur określonych w tym artykule należy uzyskać nowe rozwiązanie dotyczące rozmiarów kalkulacji cen dla organizacji. Jeśli jeszcze tego nie zrobiono, zobacz [Tworzenie pól i encji niestandardowych](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Dodawanie pola zasobu możliwego do zarezerwowania do formularzy i widoków
Aby pole **zasobu możliwego do zarezerwowania** było widoczne w rozwiązaniu obsługującym wymiarami kalkulacji cen, należy dodać pole do wszystkich formularzy i widoków jako encję.

W poniższej tabeli wymieniono wszystkie gotowe formularze i widoki według encji. Konieczne będzie również dodanie nowego pola do dodatkowych formularzy lub widoków w encjach niestandardowych.

|   Jednostka        | Formularze   |Widoki        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roli| Informacja | - Aktywne ceny kategorii zasobów<br> - Skojarzone ceny kategorii zasobów |
|  Narzut na cenę dla roli| Informacja| - Aktywny narzut na cenę dla roli<br>- Skojarzony narzut na cenę dla roli |
|  Szczegóły wiersza oferty| - Informacje o projekcie<br>- Szybkie tworzenie projektów| - Aktywne szczegóły wierszy ofert<br>- Połączone szczegóły wierszy ofert<br>- Skojarzone szczegóły wierszy oferty |
|  Szczegóły pozycji kontraktu projektu| - Informacje o projekcie<br>- Szybkie tworzenie projektów| - Połączone szczegóły pozycji kontraktu<br>- Aktywne szczegóły pozycji kontraktu<br>- Skojarzone szczegóły pozycji kontraktu |
|  Zadanie projektu| - Informacje<br>- Nowy formularz| &nbsp; |
|  Członek zespołu projektu| - Informacje<br>- Nowy formularz| - Aktywni członkowie zespołu projektu<br>- Członkowie zespołu projektu<br>- Widok skojarzony członków zespołu projektu |
|  Wpis czasu| - Informacje<br>- Tworzenie wpisu czasu| - Moje wpisy czasu według daty<br>- Moje wpisy czasu w tym tygodniu<br>- Wpisy czasu do zatwierdzenia|
|  Wiersz arkusza| - Informacje<br>- Szybkie tworzenie| - Aktywne wiersze arkuszy<br>- Skojarzony wiersz arkusza |
|  Szczegóły wiersza faktury| - Informacje<br>- Szybkie tworzenie| - Aktywne szczegóły wierszy faktur<br>- Odpłatne transakcje faktury<br>- Uzupełniające transakcje faktury<br>- Skojarzone szczegóły wiersza faktury <br>- Nieodpłatne transakcje faktury|
|  Rzeczywiste| - Informacje<br>- Aktywne wartości rzeczywiste| Skojarzona wartość rzeczywista |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Konfigurowanie zasobu możliwego do zarezerwowania jako wymiaru kalkulacji cen
Aby skonfigurować zasób możliwy do zarezerwowania jako wymiar kalkulacji cen, wykonaj następujące kroki:

1. Wybierz kolejno pozycje **Ustawienia** > **Parametry**. 
2. Na stronie **Parametr** na karcie **Wymiary kalkulacji cen oparte na kwocie** sprawdź, czy siatka pokazuje rekordy z encji **Wymiary kalkulacji cen**. 
2. Do tej listy wymiarów kalkulacji cen dodaj element **Zasób, który można zarezerwować** jako **msdyn_bookableresource**. 
3. Wybierz wartości w obszarach **Ma zastosowanie do kosztu** i **Ma zastosowanie do kosztu**.
4. W obszarze **Typ wymiaru** wybierz wartość **Oparty na kwocie**. 
5. Wybierz priorytet kosztu i sprzedaży dla zasobu możliwego do zarezerwowania. Zazwyczaj zasób możliwy do zarezerwowania ma najwyższy priorytet, gdy jest uwzględniony jako wymiar kalkulacji cen. Ustaw priorytet na **1** (lub **0**, w zależności od sposobu, w jaki określasz priorytet), aby zagwarantować takie zachowanie.

## <a name="set-up-pricing-dimension-field-names"></a>Konfigurowanie nazw pól wymiaru kalkulacji cen

Kiedy nazwa pola wymiaru kalkulacji cen w tabeli **Cena roli** różni się od nazwy pola w którejkolwiek innej encji, gdzie jest używana cena domyślna, rekord wymiaru kalkulacji cen musi być powiadamiany o innych nazwach.  

W zasobie możliwym do zarezerwowania encja **Członkowie zespołu projektu** ma nieco inną nazwę pola niż w encji **Cena roli**: 

 - Encja **Członkowie zespołu projektu** = **msdyn_bookableresourceid**
 - Encja **Cena roli** = **msdyn_bookableresource**

Rekord wymiaru kalkulacji cen dla pola **msdyn_bookableresource** musi zostać powiadomiony o tej różnicy.

1. Kliknij dwukrotnie wiersz w siatce **Wymiary kalkulacji**, aby otworzyć stronę wymiarów obiektu **msdyn_bookableresource**.
2. Na stronie wymiarów na karcie **Pokrewne** wybierz pozycję **Nazwy pól wymiaru kalkulacji cen**.

  ![Karta Nazwy pól wymiaru kalkulacji cen.](media/PD-fieldname.png)

3. W skojarzonym widoku, który zostanie otwarty, wybierz opcję **Dodaj nową nazwę pola wymiaru kalkulacji cen**.

  ![Opcja Dodaj nową nazwę pola wymiaru kalkulacji cen.](media/Add-NewPD-fieldname.png)

  Spowoduje to otwarcie strony **Nowa nazwa pola wymiaru kalkulacji cen** dla encji **msdyn_bookableresource**. 

4. Na stronie **Nowa nazwa pola wymiaru kalkulacji cen** dodaj obiekt **msdyn_projectteam** do **nazwy logicznej encji**.
5. Dodaj obiekt **msdyn_bookableresourceid** do **nazwy pola**.

 ![Formularz Nowa nazwa pola wymiaru kalkulacji cen.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]