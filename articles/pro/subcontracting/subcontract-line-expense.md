---
title: Pozycje podumowy dla kategorii wydatków
description: W tym temacie wyjaśniono, jak rejestrować wiersze podumowy dla wydatków i używać różnych pól do rejestrowania zakupu czasu od dostawców.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9eba8b70aeb98389515ee679e4bfb1426736ee2c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591693"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Pozycje podumowy dla kategorii wydatków

[!include [banner](../../includes/dataverse-preview.md)]

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

Podumowa w aplikacji Dynamics 365 Project Operations może mieć wiersz dla kategorii podatków. Wiersze podumowy dla kategorii wydatków umożliwiają menedżerowi projektu zakup kategorii usług lub produktów od dostawców, za które opłaty można naliczać w ramach projektu.

Aby utworzyć pozycję podumowy dla kategorii wydatków w aplikacji Project Operations, wykonaj poniższe kroki.

1. W okienku nawigacji wybierz pozycję **Podumowy** i otwórz podumowę, z którą chcesz pracować.
2. Na karcie **Wiersze podumowy** wybierz opcję **+ Nowy**, aby utworzyć nowy wiersz.
3. Na stronie **Szybkie tworzenie** w polu **Klasa transakcji** wybierz opcję **Wydatek** i wprowadź lub wybierz wymagane informacje dotyczące innych pól.

W poniższej tabeli przedstawiono informacje o polach na stronie szczegółów **wiersza podumowy** oraz na stronie **Szybkie tworzenie**.

| **Pole** | **Opis** | **Wpływ funkcjonalny** |
| --- | --- | --- |
| Imię i nazwisko/nazwa | Nazwa wiersza podumowy, który ma pomóc w identyfikacji. | Ta kolumna będzie wyświetlana jako pierwsza we wszystkich wyszukiwaniach na podstawie wierszy podumów. |
| Opis | Krótki opis kategorii wydatków zakupionych w wierszu podumowy. | Brak |
|Typ linii | Wartość domyślna tego pola to **Na podstawie ilości**. |Brak |
| Metoda rozliczania | Jest to zestaw opcji reprezentujący dwa główne modele umów obsługiwane przez program Project Operations: **Stała cena** i **Czas i materiały**. | Po wybraniu metody rozliczania stałej ceny dla wierszy podumów zostanie udostępniony harmonogram faktur opartych na punktach kontrolnych. |
| Klasa transakcji | Wartość domyślna tego pola to **Czas**. Aby utworzyć wiersze podumowy na potrzeby zakupu produktów, w polu **Klasa transakcji** ustaw opcję **Wydatek**.  | Oznacza to, że wiersz podumowy jest używany do rejestrowanie zakupu kategorii wydatków, które mają być użyte w projektach. |
| Kategoria transakcji | Pokazuje listę aktywnych kategorii transakcji w systemie. |Brak |
| Żądane rozpoczęcie | Wprowadź datę, do kiedy kategorie zakupu muszą być dostępne od dostawcy. | Żądany początek służy do wyboru cennika projektu z cenników projektu dołączonych do podumowy. Koszt kategorii w wierszu podumowy pochodzi z tego cennika. |
| Żądane zakończenie | Wprowadź datę, kiedy kategorie zakupu nie są już potrzebne. | Będzie on używany do pokazywania ostrzeżeń, gdy menedżer projektu kojarzy ten wiersz podumowy z określonymi oszacowaniami wydatków w projekcie, które są wymagane po tej dacie. |
| Ilość zamówiona | Ilość kategorii zakupionych od dostawcy. | Będzie on używany do pokazywania ostrzeżeń, gdy menedżer projektu pobiera zbyt wiele z tej ilości.|
| Grupa jednostek | Ta wartość domyślna jest oparta na domyślnej grupie jednostek ustawionej dla wybranej kategorii. |Brak |
| Jednostka | Ta wartość domyślna jest oparta na domyślnej jednostce ustawionej dla wybranej kategorii.  | Kombinacja **Kategorii** i **Jednostki** zostanie użyta jako domyślna lub obliczona dla ceny jednostkowej dla wiersza podumowy.  |
| Cena jednostkowa | Domyślna wartość wykorzystuje kombinację **Kategorii** i **Jednostki** z cen kategorii powiązanych z cennikiem projektu, która ma zastosowanie do żądanego początku wiersza podumowy. |Brak |
| Suma częściowa | Jest to pole tylko do odczytu obliczane jako cena jednostkowa X ilość, jeśli wprowadzono zarówno wartość jednostkową, jak i ilość. Jeśli jedno lub oba pola są puste, można wprowadzić wartość w tym polu. |Brak |
| Podatek | Wprowadź kwotę podatku. |Brak |
| Łączna kwota | Łączna kwota pozycji podumowy z uwzględnieniem podatku. To pole jest obliczane jako Suma częściowa + Podatek. |Brak |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
