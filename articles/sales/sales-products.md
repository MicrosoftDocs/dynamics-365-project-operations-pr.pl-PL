---
title: Produkty
description: Ta temat zawiera informacje o katalogu produktów, za pomocą którego można dostarczać klientom informacje o produktach i cenach oferowanych przez organizację.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121276"
---
# <a name="products"></a>Produkty

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Produkty są podstawą Twojej firmy. Katalog produktów w Dynamics 365 Sales Professional jest zbiorem produktów i informacji o ich cenach. Ułatw swoim przedstawicielom handlowym zwiększanie sprzedaży poprzez szybkie tworzenie katalogu produktów.

## <a name="add-a-product"></a>Dodawanie produktu

1.  Upewnij się, że przypisano Cię do roli zabezpieczeń Menedżer Sales Professional lub Administrator systemu, aby móc dodawać produkty w Dynamics 365 Sales Professional.
2.  Na mapie witryny w obszarze **Konfiguruj**, wybierz **Produkty**.
3.  Wybierz pozycję **Dodaj produkt** i wypełnij następujące informacje:

    -  **Nazwa/nazwisko**
    -  **Identyfikator produktu**
    -  **Nadrzędny**: Wybierz nadrzędną rodzinę produktów dla produktu. Jeśli tworzysz produkt podrzędny w rodzinie produktów, nazwa nadrzędnej rodziny produktów zostaną wypełniona w tym miejscu. Nie można tego zmienić po zapisaniu rekordu.
    -  **Ważne od**/**Ważne do**: Określ okres ważności pakietu produktu wybierając daty **Ważne od** i **Ważne do**.
    -  **Grupa jednostek**: Wybierz grupę jednostek. Grupa jednostek jest zbiorem różnych jednostek, w jakich produkt jest sprzedawany, i definiuje, jak poszczególne elementy są grupowane w większe ilości. Na przykład podczas dodawania nasion jako produktu mogłeś utworzyć grupę jednostek o nazwie „Nasiona” i zdefiniować jej jednostkę podstawową jako „paczka”.
    -  **Jednostka domyślna**: Wybierz najpopularniejszą jednostkę, w jakiej będzie sprzedawany produkt. Jednostki to ilości lub wielkości, w jakich sprzedajesz swoje produkty. Na przykład jeśli dodajesz nasiona jako produkt, możesz je sprzedawać w paczkach, pudłach oraz paletach. Każda z tych jednostek staje się jednostką produktu. Jeśli nasiona są najczęściej sprzedawane w paczkach, wybierz to jako jednostkę.
    -  **Domyślny cennik**: Jeśli produkt jest nowy, to pole jest polem tylko do odczytu. Przed wybraniem cennika domyślnego należy wypełnić wszystkie wymagane pola, a następnie zapisać rekord. Chociaż cennik domyślny nie jest wymagany, po zapisaniu rekordu produktu warto ustawić cennik domyślny dla każdego produktu. Jeśli rekord klienta nie zawiera cennika, aplikacja Sales może użyć cennika domyślnego do generowania ofert, zamówień i faktur.
    -  **Obsługiwane miejsca dziesiętne**: Musisz wprowadzić liczbę całkowitą z zakresu od 0 do 5. Jeśli produktu nie można dzielić na części ułamkowe, wpisz wartość 0. Dokładność pola **Ilość** w rekordzie oferty, zamówienia lub zafakturowanego produktu jest sprawdzana dla wartości w tym polu, jeśli produkt nie posiada skojarzonego cennika.
    -  **Temat**: Powiąż produkt z tematem. Tematów można używać do podziału produktów na kategorie oraz do filtrowania raportów.

4.  Wybierz pozycję **Zapisz**.
5.  Przejdź do karty **Dodatkowe informacje**. W sekcji **Pozycja cennika** wybierz ikonę **Więcej poleceń**, a następnie wybierz **Dodaj nową pozycję cennika**.
7.  Na karcie **Dodatkowe informacje**, w sekcji **Relacje produktów** wybierz ikonę **Więcej poleceń**, a następnie wybierz **Dodaj nową relację produktu**.
8.  W formularzu **Nowa relacja produktu**, wpisz następujące informacje szczegółowe, a na pasku poleceń wybierz **Zapisz i Zamknij**:

    -   **Powiązany produkt**: Wybierz produkt, który chcesz dodać jako produkt pokrewny do istniejącego rekordu produktu, nad którym pracujesz.
    -   **Typ relacji sprzedaży**: Wybierz, czy chcesz dodać produkt jako produkt droższy, produkt powiązany, akcesorium lub zamiennik.
    -   **Kierunek**: Określ, czy relacja między produktami będzie jednokierunkowa czy dwukierunkowa. Po wybraniu opcji Jednokierunkowa, produkt wybrany w **Produkt porewny** pojawi się jako zalecenie dla istniejącego produktu, ale nie odwrotnie.

9.  W formularzu produktu wybierz **Zapisz**.

## <a name="import-products"></a>Importowanie produktów

Korzystając z szablonów importu, można przenosić zbiorcze dane produktu do Dynamics 365 Sales.

## <a name="revise-a-product"></a>Poprawianie produktu

Zachowaj aktualność magazynu produktów poprzez szybkie poprawianie właściwości produktów zgodnie z wymaganiami, a następnie ponowne publikowanie informacji, dzięki czemu przedstawiciele handlowi zawsze zobaczą najnowsze zmiany w zapasach.

1.  Upewnij się, że przypisano Cię do jednej z następujących ról zabezpieczeń — Administrator systemu, Konfigurator systemu, Dyrektor ds. sprzedaży, Wiceprezes ds. sprzedaży, Wiceprezes ds. marketingu lub Prezes zarządu — bądź dysponujesz równoważnymi uprawnieniami.
2.  Na mapie witryny, wybierz **Produkty**.
3.  Otwórz aktywny produkt, który chcesz zmodyfikować, a następnie na pasku poleceń wybierz **Popraw**.
4.  W oknie dialogowym **Potwierdź poprawienie** wybierz **Potwierdź**. Spowoduje to zmianę stanu produktu na **Do poprawki**.
5.  Po zakończeniu wprowadzania zmian na pasku poleceń wybierz **Publikuj**.

    > [!TIP]
    > Aby odwrócić zmiany i kontynuować pracę z ostatnią aktywną wersją produktu, wybierz opcję **Przywróć**. To zmieni stan produktu z powrotem na **Aktywny**.

## <a name="clone-a-product"></a>Klonowanie produktu 

Podczas tworzenia nowego produktu oszczędź czas, klonując istniejący obiekt. Tworzy się wtedy kopia oryginalnego rekordu ze wszystkimi szczegółami, z wyjątkiem nazwy i identyfikatora.

1.  Upewnij się, że przypisano Cię do jednej z następujących ról zabezpieczeń — Administrator systemu, Konfigurator systemu, Dyrektor ds. sprzedaży, Wiceprezes ds. sprzedaży, Wiceprezes ds. marketingu lub Prezes zarządu — bądź dysponujesz równoważnymi uprawnieniami.
2.  Na mapie witryny, wybierz **Produkty**.
3.  Wybierz rekord produktu, który chcesz sklonować, i na pasku poleceń wybierz **Klonuj**. Pojawia się okno dialogowe potwierdzenia.
4.  Wybierz pozycję **Potwierdź**.

Otwiera się nowy rekord produktu z takimi samymi szczegółami jak oryginalny rekord, z wyjątkiem nazwy i identyfikatora.

## <a name="retire-a-product"></a>Wycofywanie produktu 

Jeśli Twoja organizacja nie sprzedaje już produktu, wycofaj go, tak aby nie był już dostępny dla przedstawicieli handlowych.

1.  Upewnij się, że przypisano Cię do roli zabezpieczeń Administrator systemu lub Menedżer Sales Professional bądź dysponujesz równoważnymi uprawnieniami.
2.  Na mapie witryny, wybierz **Produkty**.
3.  Otwórz aktywny produkt, który chcesz wycofać, a następnie na pasku poleceń wybierz **Wycofaj**.
4.  W oknie dialogowym **Potwierdź wycofanie** wybierz **Potwierdź**.


## <a name="delete-a-product"></a>Usuń produkt

Aby przestać sprzedawać produkt, usuń go.

> [!IMPORTANT]
> Nie istnieje możliwość odzyskania usuniętego rekordu.

1.  Upewnij się, że przypisano Cię do roli zabezpieczeń Administrator systemu lub Menedżer Sales Professional bądź dysponujesz równoważnymi uprawnieniami.
2.  Na mapie witryny, wybierz **Produkty**.
3.  Wybierz rekord produktu, który chcesz usunąć, i na pasku poleceń wybierz **Usuń**.
4.  W oknie dialogowym **Potwierdź usunięcie** wybierz **Kontynuuj**.
 
 ## <a name="quantity-factors-for-products"></a>Współczynniki ilościowe dla produktów

Do obsługi sprzedaży produktów opartych na subskrypcji można użyć współczynników ilościowych. W przypadku produktów opartych na subskrypcji liczba w ofercie lub pozycji kontraktu projektu jest wyrażona liczbą użytkowników w miesiącu.

Zazwyczaj cena subskrybowanego oprogramowania jest przechowywana w katalogu jako cena za jednego użytkownika za jeden miesiąc. Można jednak używać również innych opisów czasu. W trakcie procesu sprzedaży cena w wierszu oferty to zazwyczaj cena na użytkownika na miesiąc, która została wynegocjowana i uzupełniona o rabat przez przedstawiciela handlowego z działu IT. Każda transakcja ma inną liczbę użytkowników i inną liczbę miesięcy subskrypcji. Ilość użyta do obliczenia kwoty w wierszu oferty jest iloczynem liczby użytkowników i liczby miesięcy subskrypcji.

Współczynniki ilościowe opierają się na atrybutach produktów. Podczas konfigurowania konkretnych właściwości produktu można oznaczyć podzbiór tych właściwości albo wszystkich właściwości jako współczynników ilościowych.

System weryfikuje, czy tylko właściwości liczbowe lub właściwości produktu mające liczbowy typ danych są flagowane jako współczynniki ilościowe. Gdy produkt, dla którego są konfigurowane współczynniki ilościowe, zostanie dodany do wiersza produktu, pole **Ilość** w wierszu oferty staje się polem tylko do odczytu. Po wprowadzeniu wartości właściwości produktu będących współczynnikami ilościowymi rozwiązanie obliczy ilość w wierszu oferty.

Jeśli na przykład istnieją następujące właściwości: 

- **Liczba użytkowników**: liczba użytkowników 
- **Liczba miesięcy**: liczba miesięcy subskrypcji
- **Kod SKU produktu** 

Właściwości **Liczba użytkowników** i **Liczba miesięcy** można oflagować jako współczynniki ilościowe, odpowiednio modyfikując właściwości wiersza produktu. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]