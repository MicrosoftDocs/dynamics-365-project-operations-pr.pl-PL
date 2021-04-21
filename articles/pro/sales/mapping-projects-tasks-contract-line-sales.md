---
title: Mapowanie projektów i zadań do pozycji kontraktu opartego na projekcie - wersja uproszczona
description: W tym temat przedstawiono informacje o dodawaniu i usuwaniu projektów i zadań do pozycji kontraktu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4737f9870904bfc7adac11b8e2aa13bb8c610ca3
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858112"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mapowanie projektów i zadań do wiersza kontraktu opartego na projekcie 

_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_

W pozycjach kontraktu opartych na projektach można zmapować określone zadania projektu do pozycji kontraktu.

Kiedy poszczególne zadania są mapowane na pozycje kontraktu, opcje metody fakturowania, opłaty, inne niż przekroczenia, a klienci zdefiniowani w pozycji kontraktu będą miały zastosowanie wyłącznie do tych zadań specjalnych.

Jeśli istnieje scenariusz, w którym jedna faza projektu, na przykład faza prototypu, to stała cena, a wszystkie pozostałe fazy to czas i materiał, można skojarzyć fazę prototypu z wszystkimi zadaniami podrzędnymi z pozycją kontraktu w tej fazie z metodą fakturowania przy stałej cenie.

Wszystkie pozostałe fazy struktury podziału prac projektu (SPP) można skojarzyć z pozycją kontraktu czasowego i na podstawie materiału.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Przypisanie pozycji kontraktu do zadań projektu

Zadania można kojarzyć z pozycjami kontraktu na karcie **Zadania płatne** na stronie **Pozycja kontraktu** lub na karcie **Rozliczanie zadań** na stronie **Projekt**.

### <a name="from-the-contract-line-page"></a>Ze strony Pozycja kontraktu

Wykonaj poniższe kroki, aby skojarzyć zadania projektu z pozycją kontraktu na karcie **Zadania płatne** na stronie **Pozycja kontraktu**.

1. Na karcie **Ogólne** pozycji kontraktu opartego na projekcie sprawdź, czy pole **Projekt** jest wypełnione.
2. W polu **Dołączone zadania** wybierz **Tylko wybrane zadania**.
3. Zapisz zmiany. Formularz zostanie odświeżony, a karta **Zadania płatne** będzie widoczna.
4. Wybierz kartę **Zadania płatne** i w podsiatce wybierz pozycję **Dodaj zadanie dotyczące pozycji kontraktu**.
5. Na stronie **Zadania dotyczące pozycji kontraktu** na liście rozwijanej **Zadania** zaznacz zadanie. 
6. Wprowadź informacje w polu **Typ fakturowania**, a następnie wybierz pozycję **Zapisz i Zamknij**. Wybrane zadanie jest skojarzone z pozycją kontraktu.

> [!NOTE]
> Nie jest to najbardziej optymalny sposób kojarzenia zadań projektu z pozycjami kontraktu. Z każdym projektem będzie konieczne ręczne skojarzenie w tym środowisku. Preferowaną metodą jest kliknięcie karty **Rozliczanie zadań** na stronie **Projekt**.

### <a name="from-the-project-page"></a>Z poziomu strony projektu

Jest to optymalna metoda kojarzenia zadań z pozycjami kontraktu. Użytkownik może wybrać wiele zadań i skojarzyć wszystkie te i zadania podrzędne z wybraną pozycją kontraktu. Wykonaj poniższe kroki, aby skojarzyć zadania z pozycją kontraktu z poziomu strony **Projektu**.

1. Na karcie **Ogólne** pozycji kontraktu opartego na projekcie sprawdź, czy pole **Projekt** jest wypełnione.
2. W polu **Dołączone zadania** wybierz **Tylko wybrane zadania**.
3. Zapisz pozycję kontraktu opartego na projekcie. Formularz zostanie odświeżony, a karta **Zadania płatne** będzie widoczna. Wystarczy tylko do celów związanych z weryfikacją.
4. Na karcie **Ogólne** pozycji kontraktu opartego na projekcie sprawdź, pole **Projekt** i wybierz link do projektu.
5. Na stronie **Projekt** wybierz kartę **Ustawienia fakturowania zadań**.
6. Istnieją dwie siatki. Jedna siatka jest dotycząca pozycji kontraktu mających zastosowanie do całego projektu. Druga siatka ma zastosowanie do konfiguracji fakturowania konkretnego zadania. W drugiej siatce wybierz jedno lub więcej zadań, a następnie wybierz pozycję **Skojarz pozycje kontraktu**.
7. Na stronie dialogu, który zostanie otwarty, wybierz pozycja kontraktu z listy rozwijanej.
8. Użyj listy rozwijanej **Typ fakturowania**, aby oznaczyć zadania jako odpłatne lub niepłatne.
9. Zaznacz pole wyboru, aby określić, czy skojarzenie powinno również zawierać zadania podrzędne zaznaczonych zadań. Zaznaczenie tego pola wyboru powoduje również skojarzenie z zadaniami podrzędnymi zaznaczonych zadań w pozycji kontraktu.
10. Wybierz **OK**, aby zamknąć okno dialogowe.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Usuń skojarzenia zadań z linii umowy opartych na projekcie

### <a name="from-the-contract-line-page"></a>Ze strony pozycja kontraktu

Wykonaj poniższe kroki, aby anulować skojarzenie zadania projektu z pozycją kontraktu na karcie **Zadania płatne** na stronie **Pozycja kontraktu**.

1. Na karcie **Zadania płatne** wybierz pozycję **Usuń zadanie w wierszu kontraktu**.
2. Komunikat ostrzegawczy oznacza, że usunięcie tego skojarzenia może skutkować wycofaniem wartości rzeczywistych zanotowanych wcześniej dla zadania. Kliknij przycisk **OK** w dialogu, aby usunąć skojarzenie między zadaniem a pozycją kontraktu opartego na projektach. 

> [!NOTE]
> Nie powoduje usunięcia zadania z projektu. Zamiast tego jest usuwane powiązanie zadania z pozycji kontraktu opartej na projektach.

### <a name="from-the-project-page"></a>Z poziomu strony projektu

Jest to bardziej optymalne rozwiązanie w przypadku usuwania skojarzeń zadań z pozycji kontraktowych. Możesz wybrać wiele zadań i usunąć skojarzenie wszystkich z nich i ich zadań podrzędnych z wybranej pozycji kontraktu. Wykonaj następujące kroki, aby usunąć skojarzenie zadań z pozycji kontraktu.

1. Na karcie **Ogólne** pozycji kontraktu opartego na projekcie sprawdź, pole **Projekt** i wybierz link do projektu.
2. Na stronie **Projekt** wybierz kartę **Ustawienia fakturowania zadań**.
3. Na stronie znajdują się dwie siatki. Jedna siatka jest przeznaczona dla pozycji kontraktu mających zastosowanie do całego projektu, a drugi jest stosowana do konfigurowania fakturowania poszczególnych zadań. W drugiej siatce wybierz jedno lub więcej zadań, a następnie wybierz pozycję **Anuluj skojarzenie pozycje kontraktu**.
4. Na stronie dialogu, który zostanie otwarty, wybierz pozycja kontraktu z listy rozwijanej.
5. Zaznacz pole wyboru, aby wskazać, czy skojarzenie powinno również zostać usunięte z wszelkich zadań podrzędnych wybranych zadań. Zaznaczenie tego pola spowoduje również odłączenie zadań podrzędnych wybranych zadań z linii kontraktu.
6. Wybierz pozycję **OK**. Komunikat ostrzegawczy oznacza, że usunięcie tego skojarzenia może skutkować wycofaniem wartości rzeczywistych zanotowanych wcześniej dla zadania. Kliknij przycisk **OK** w oknie ostrzeżenia, aby usunąć skojarzenie między zadaniem a pozycją kontraktu opartego na projektach.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
