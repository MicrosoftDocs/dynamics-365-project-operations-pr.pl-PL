---
title: Wiersze podumowy dla produktów
description: W tym temacie wyjaśniono, jak rejestrować wiersze podumowy dla produktów i używać różnych pól do rejestrowania zakupów produktów od dostawców.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71e4a48c3d29d7ea5b015f6c6797da60001fccff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579086"
---
# <a name="subcontract-lines-for-products"></a>Wiersze podumowy dla produktów

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Podumowa w aplikacji Dynamics 365 Project Operations może mieć pozycję podumowy dla produktów. Te wiersze umożliwiają menedżerowi projektu zakup produktów od dostawców, a następnie używanie ich w zadaniach projektów.

Wykonaj następujące kroki, aby utworzyć pozycję podumowy dla produktów w aplikacji Project Operations.

1. Na stronie nawigacji wybierz pozycję **Podumowy**, a następnie otwórz podumowę, z którą chcesz pracować. 
2. Na karcie **Wiersze podumowy** wybierz opcję **+ Nowy**, aby utworzyć nowy wiersz podumowy.
3. Na stronie **Szybkie tworzenie** w polu **Klasa transakcji** wybierz opcję **Materiał** i wprowadź lub wybierz wymagane informacje dotyczące pola. 
4. Wybierz pozycję **Zapisz**.

W poniższej tabeli przedstawiono informacje o polach na stronie **szczegółów wiersza podumowy** oraz na stronie **Szybkie tworzenie**, ponieważ dotyczą one dotyczące zakupu produktów.

| Pole | Opis | Wpływ funkcjonalny|
| ----- | ----------- | ----------- |
| Imię i nazwisko/nazwa | Nazwa wiersza podumowy, który ma pomóc w identyfikacji. |Ta kolumna będzie wyświetlana jako pierwsza we wszystkich wyszukiwaniach na podstawie wierszy podumów.
| Opis | Krótki opis produktów zamawianych w ramach pozycji podumowy. | Brak |
| Typ linii | Wartość domyślna tego pola to **Na podstawie ilości**. |Brak |
| Metoda rozliczania | Jest to zestaw opcji reprezentujący dwa główne modele umów obsługiwane przez program Project Operations: **Stała cena** i **Czas i materiały**. | Na podstawie wybranej formy rozliczenia zostanie udostępniony harmonogram faktur opartych na punktach kontrolnych dla wierszy podumowy ze stałą ceną formy rozliczenia. |
| Klasa transakcji |Wartość domyślna tego pola to **Czas**. Aby utworzyć wiersze podumowy na potrzeby zakupu produktów, w polu **Klasa transakcji** ustaw opcję **Materiał**.  | Oznacza to, że wiersz podumowy jest używany do rejestrowanie zakupu produktów, które mają być użyte w projektach. |
| Wybierz produkt | Należy wybrać, czy zakupiony produkt jest zapisywany w katalogu produktów, czy jest produktem dopisanym. |Brak |
| Produkt | Wybierz aktywny produkt z katalogu. To pole jest dostępne tylko wtedy, gdy ustawienie **Wybierz produkt** ma wartość **Istniejący**. |Kombinacja **Produktu** i **Jednostki** zostanie użyta jako domyślna lub obliczona dla ceny jednostkowej dla wiersza podumowy.
| Produkt dopisany | Wprowadź nazwę produktu dopisanego. To pole jest dostępne tylko wtedy, gdy ustawienie **Wybierz produkt** ma wartość **Dopisany**.  |Cena zakupu nie zostanie automatycznie wypełniona produktami do zapisu.|
| Żądana data dostawy | Wprowadź wymaganą datę dostawy produktów.| Ta data służy także do wyboru cennika projektu z cenników projektu dołączonych do podumowy. Koszt produktu w pozycji umowy jest następnie domyślny dla danego cennika. |
| Zakontraktowana data dostawy | Wprowadź datę dostawy produktów zgodnie z ustaleniami kontraktu.  |Brak|
| Ilość zamówiona | Wprowadź ilość produktu kupowaną od dostawcy.| Będzie on używany do pokazywania ostrzeżeń, gdy menedżer projektu pobiera zbyt wiele z tej ilości.|
| Grupa jednostek | Ta wartość jest domyślnie ustawiana tylko dla produktów z katalogu. |Po wybraniu opcji **Produkt** i **Żądana data dostawy** system wybiera odpowiedni cennik na podstawie daty dostawy. W obrębie pozycji cennika są tworzone zapytania dotyczące pasującego projektu. Wartości jednostki i grupy jednostek są ustawiane jako domyślne na podstawie ustawień rekordu pozycji cennika. |
| Jednostka | Ta wartość jest ustawiana domyślnie na jednostkę ustawioną w rekordzie pozycji cennika. W razie potrzeby można zmienić tę jednostkę na inną jednostkę.| Kombinacja produktu i jednostki jest używana w celu ustawienia domyślnego ceny jednostkowej w pozycji podumowy dla istniejących produktów katalogu. |
| Cena jednostkowa | Domyślne ceny jednostkowe są stosowane na podstawie kombinacji produktów i jednostek z pozycji cennika powiązanych z cennikiem projektu, który ma zastosowanie w przypadku żądanej daty dostawy pozycji podumowy.  |Brak |
| Suma częściowa | To pole tylko do odczytu jest obliczane jako Ilość x Cena jednostkowa, jeśli w obu polach wprowadzono wartości. Jeśli pole **Ilość**, **Cena jednostkowa** lub oba te pola są puste, można wprowadzić wartość ręcznie.  |Brak |
| Podatek | Wprowadź wartość podatku. |Brak |
| Łączna kwota | To pole obliczane zawiera łączną kwotę pozycji podumowy po uwzględnieniu podatków. Wartość w tym polu jest obliczana jako Suma częściowa + Podatek. |Brak |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
