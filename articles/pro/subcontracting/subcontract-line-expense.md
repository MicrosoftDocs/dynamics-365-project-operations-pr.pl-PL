---
title: Pozycje podumowy dla kategorii wydatków
description: W tym temacie wyjaśniono, jak rejestrować wiersze podumowy dla wydatków i używać różnych pól do rejestrowania zakupu czasu od dostawców.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323834"
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

| **Pole** |  **Opis** |
| ----------| ---------------- |
| Imię i nazwisko/nazwa | Nazwa wiersza podumowy. |
| Opis | Krótki opis kategorii usług lub produktów zakupionych w ramach wiersza podumowy. |
| Typ linii | Wartość domyślna tego pola to **Na podstawie ilości**.  |
| Metoda rozliczania | Nazwa rozliczania wiersza podumowy. W oparciu o metodę rozliczania wiersza dla metody rozliczania o stałej cenie jest dostępny harmonogram faktur oparty na punktach kontrolnych.  |
| Klasa transakcji | Wartość domyślna tego pola to **Czas**. Aby utworzyć wiersze podumowy na potrzeby zakupu produktów, w polu **Klasa transakcji** ustaw opcję **Wydatek**. Ta wartość pola oznacza, że pozycja podumowy jest używana do rejestrowania zakupu kategorii produktów lub usług do użycia w projektach. |
| Kategoria transakcji | Wybierz kategorię transakcji. |
| Żądane rozpoczęcie | Data, dla której kategorie zakupu muszą być dostępne od dostawcy. Żądana data rozpoczęcia służy do wyboru cennika projektu z cenników projektu dołączonych do podumowy. Koszt kategorii w pozycji umowy jest następnie domyślny dla danego cennika. |
| Żądane zakończenie | Data, od kiedy kategorie zakupu nie są już potrzebne. Ta data wymaga ostrzeżenia, gdy menedżer projektu skojarzy tę pozycję podumowy z określonymi szacowaniami wydatków w projektach przypadających po tej dacie. |
| Ilość zamówiona | Ilość kategorii kupowana od dostawcy. Jeśli menedżer projektu przekroczy kupowaną ilość, pojawi się ostrzeżenie.  |
| Grupa jednostek | Ta wartość pola jest ustawiana domyślnie na podstawie domyślnej grupy jednostek ustawionej dla wybranej kategorii. |
| Jednostka | Ta wartość pola jest ustawiana domyślnie na podstawie domyślnej jednostki ustawionej dla wybranej kategorii. Kombinacja kategorii i jednostki jest używana w celu ustawienia domyślnej ceny jednostkowej w pozycji podumowy. |
| Cena jednostkowa | Domyślna wartość pola ceny jednostkowej pochodzi z kombinacji kategorii i jednostki z cen kategorii powiązanych z cennikiem projektu, który ma zastosowanie w przypadku żądanego rozpoczęcia pozycji podumowy.  |
| Suma częściowa | To pole tylko do odczytu jest automatycznie obliczane jako cena jednostkowa ilości, jeśli zostanie wprowadzona zarówno wartość ilości, jak i cena jednostkowa. Jeśli dowolne lub oba pola są puste, można ręcznie wprowadzić wartość tego pola.  |
| Podatek | Wprowadź kwotę podatku.  |
| Łączna kwota | Łączna kwota pozycji podumowy z uwzględnieniem podatku. To pole jest obliczane jako suma częściowa + podatek.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
