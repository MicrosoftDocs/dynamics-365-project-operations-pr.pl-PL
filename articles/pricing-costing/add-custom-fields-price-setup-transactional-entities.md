---
title: Dodawanie wymaganych pól niestandardowych do ustawień cen i encji transakcyjnych
description: W tym temat zamieszczono informacje dotyczące sposobu dodawania wymaganych odwołań do encji, formularzy oraz widoków.
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
ms.openlocfilehash: c324e0e8797d0b6d3a06ffc2a40b787a475c49b5
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590914"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Dodawanie wymaganych pól niestandardowych do ustawień cen i encji transakcyjnych

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W tym temat założono, że wykonano procedury opisane w temacie [Tworzenie niestandardowych pól i encji, które będą użyte jako wymiary kalkulacji cen](create-custom-fields-entities-pricing-dimensions.md). Jeśli tych procedur jeszcze nie wykonano, wróć, wykonaj je, a następnie wróć do tego tematu. 

W tym temacie procedury pokazują, jak dodawać do encji i do elementów interfejsu użytkownika wymagane odwołania do pól niestandardowych, np. formularze i widoki.

## <a name="add-custom-pricing-dimension-fields"></a>Dodawanie pól wymiarów niestandardowej kalkulacji cen 
Po utworzeniu niestandardowych pól i encji kolejnym krokiem jest ustawienie w konfiguracji cen i encji transakcyjnych wszelkich niestandardowych encji lub zestawów opcji przez utworzenie pól referencyjnych. W zależności od tego, czy lista wymiarów kalkulacji cen zawiera zestaw opcji wymiarów lub wymiarów encji lub jedno i drugie, należy wykonać tylko kroki opisane w sekcji **Niestandardowe wymiary kalkulacji cen oparte na zestawie opcji** lub **Niestandardowe wymiary kalkulacji cen oparte na encji** lub jedno i drugie, odpowiednio.

### <a name="option-set-based-custom-pricing-dimensions"></a>Niestandardowe wymiary kalkulacji cen oparte na zestawie opcji
Kiedy niestandardowy wymiar kalkulacji cen jest oparty na zestawie opcji, należy dodać go jako pole do kluczowych encji. W poniższej procedurze **Lokalizacja pracy zasobu** i **Godziny pracy zasobu** są używane jako wymiary kalkulacji cen oparte na zestawach opcji. Najpierw muszą zostać dodane jako pola do encji kalkulacji cen, **Cena roli** i **Narzut na cenę dla roli**.

1. W przypadku operacji projektowych wybierz **Ustawienia** > **Rozwiązania** i kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Cena roli**.
3. Rozwiń encję **Cena roli** i wybierz **Pola**.
4. Wybierz **Nowe**, aby utworzyć nowe pole o nazwie **Lokalizacja pracy zasobu** i wybierz **Zestaw opcji** jako typ pola. 
5. Wybierz opcję **Użyj istniejącego zestaw opcji**, wybierz zostaw opcji **Lokalizacja pracy zasobu** i wybierz **Zapisz**.
6. Powtórz kroki 1-5, aby dodać to pole do encji **Narzut na cenę dla roli**. 
7. Powtórz kroki 1-5 dla zestaw opcji **Godziny pracy zasobu**.

> [!IMPORTANT]
> W przypadku dodawania pola do więcej niż jednej encji należy użyć tej samej nazwy pola we wszystkich encjach. 

> ![Dodawanie lokalizacji pracy zasobu do ceny roli](media/RWL-Field.png)

W fazach sprzedaży i szacunkowej projektu prognozy nakładu pracy wymagane do ukończenia pracy **lokalnej** i **na miejscu** w **zwykłych godzinach** i **nadgodzinach** są używane w celu oszacowania wartość oferty/projektu. Pola **Lokalizacje pracy zasobu** i **Godziny pracy zasobu** zostaną dodane do encji oszacowania, **Szczegóły wiersza oferty**, **Szczegóły wiersza umowy**, **Członek zespołu projektu** oraz **Wiersz szacowania**.

1. W przypadku operacji projektowych wybierz **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Szczegóły wiersza oferty**.
3. Rozwiń encję **Szczegóły wiersza oferty** i wybierz **Pola**.
4. Wybierz **Nowe**, aby utworzyć nowe pole o nazwie **Lokalizacja pracy zasobu** i wybierz typ pól **Zestaw opcji**. 
5. Wybierz opcję **Użyj istniejącego zestaw opcji**, wybierz **Lokalizacja pracy zasobu** i wybierz **Zapisz**.
6. Powtórz kroki 1-5, aby dodać to pole do encji **Szczegóły pozycji kontraktu projektu**, **Członek zespołu projektu** i **Wiersz szacowania**.
7. Powtórz kroki 1-6 dla zestaw opcji **Godziny pracy zasobu**. 

> ![Dodawanie lokalizacji pracy zasobu do Wiersza szacowania](media/RWL-Default-Value.png)

W celu dostarczenia i fakturowania ukończona praca powinna być dokładnie wyceniona, aby wybrać czy została wykonana **Lokalnie** lub **Na miejscu** i czy została ukończona w **godzinach pracy** czy w **nadgodzinach** w wartościach rzeczywistych projektu. Pola **Lokalizacja pracy zasobu** i **Godziny pracy zasobu** zostaną dodane do encji **Wpis czasu**, **Rzeczywiste**, **Szczegóły wiersza faktury** oraz **Wiersz dziennika**.

1. Wybierz **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**.
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Wpisz czasu**.
3. Rozwiń encję **Szczegóły wiersza oferty**, a następnie wybierz **Pola**.
4. Wybierz **Nowe**, aby utworzyć nowe pole o nazwie **Lokalizacja pracy zasobu** i wybierz **Zestaw opcji** jako typ pola. 
5. Wybierz opcję **Użyj istniejącego zestaw opcji**, wybierz zostaw opcji **Lokalizacja pracy zasobu** i wybierz **Zapisz**.
6. Powtórz kroki 1-5 w celu dodania tego pola do encji **Rzeczywiste**, **Szczegóły wiersza faktury** i **Wiersz dziennika**.
7. Powtórz kroki 1-6 dla zestaw opcji **Godziny pracy zasobu**. 

> ![Dodawanie lokalizacji pracy zasobu do Wpisu czasu](media/RWL-time-entry.png)

Spowoduje to ukończenie zmian schematu wymaganych dla niestandardowych wymiarów opartych na zestawie opcji.

## <a name="entity-based-custom-pricing-dimensions"></a>Niestandardowe wymiary kalkulacji cen oparte na encji

Kiedy niestandardowym wymiarem kalkulacji cen jest encja, dodasz relację 1:N między encją wymiarową i kluczowymi encjami. Kiedy użyjemy przykładu Standardowe stanowisko z góry, należy oczekiwać, że każdy pracownik będzie miał przypisany standardowe stanowisko. To będzie wymagało relacji 1:N między standardowym stanowiskiem a zasobem, który można zaksięgować albo relacji N:1, jeśli utworzono z zasobu, który można zaksięgować do standardowego stanowiska.

1. W przypadku operacji projektowych wybierz **Ustawienia** > **Rozwiązania**, a następnie kliknij dwukrotnie opcję **Wymiary kalkulacji cen \<your organization name>**. 
2. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Standardowe stanowisko**.
3. Rozwiń encję **Standardowe stanowisko** i wybierz **Relacje 1:N**.
4. Wybierz **Nowa**, aby utworzyć nową relację 1:N o nazwie **Standardowe stanowisko do Zasobu, który można zaksięgować**. Wprowadź wymagane informacje, a następnie wybierz **Zapisz**.

> ![Dodawanie standardowego stanowiska jako pola odwołania do zasobu, który można zarezerwować](media/ST-BR.png)

Standardowe stanowisko musi również zostać dodane do encji kalkulacji cen **Cena roli** oraz **Narzut na cenę dla roli**. Te dane są również uzupełniane przy użyciu relacji 1:N między encjami **Standardowe stanowisko** a **Cena roli** i encjami **Standardowe stanowisko** i **Narzut na cenę dla roli**.

1. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Standardowe stanowisko**.
2. Rozwiń encję **Standardowe stanowisko** i wybierz **Relacje 1:N**.
3. Wybierz **Nowa**, aby utworzyć nową relację 1:N o nazwie **Standardowe stanowisko do Ceny roli**. Wprowadź wymagane informacje, a następnie wybierz **Zapisz**.
4. Powtórz kroki 1–4, aby utworzyć relacje 1:N między encjami **Standardowe stanowisko** i **Narzut na cenę dla roli**,

W fazach sprzedaży i oszacowania projektu, do kalkulacji cen oferty/projektu konieczne są szacowania nakładu pracy dotyczące poszczególnych standardowych stanowisk. Oznacza to, że potrzebne są relacje 1:N ze Standardowego stanowiska do poszczególnych encji szacowania w: 

- **zczegóły wiersza oferty**
- **Szczegóły pozycji kontraktu projektu**
- **Członek zespołu projektu**
- **Wiersz szacowania**

5. Powtórz kroki 1-5, aby utworzyć relacje 1:N z encji **Standardowe stanowisko** do encji **Szczegóły wiersza oferty**, **Szczegóły pozycji kontraktu projektu**, **Członek zespołu projektu** oraz **Wiersz szacowania**.

> ![Dodawanie standardowego stanowiska jako pola odwołania do wiersza szacowania](media/ST-Estimate-Line.png)

  W fazach dostarczania i fakturowania praca wykonana przez każde standardowe stanowisko musi być dokładnie wyceniona w wartościach rzeczywistych projektu. To oznacza, że musi być relacja 1:N z encji **Standardowe stanowisko** do encji **Wpis czasu**, **Rzeczywiste**, **Szczegóły wiersza faktury** oraz **Wiersz arkusza**.

6. Powtórz kroki 1-6, aby utworzyć relacje 1:N z encji **Standardowe stanowisko** do encji **Wpis czasu**, **Rzeczywiste**, **Szczegóły wiersza faktury** oraz **Wiersz arkusza**.

> ![Dodawanie standardowego stanowiska jako pola odwołania do wpisu czasu](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Konfigurowanie ustawiania domyślnych wartości wymiaru przy użyciu funkcji mapowania platformy
W przypadku encji Wpis czasu pomocne jest, kiedy system domyślnie ustawia ustawienie standardowe stanowisko na Wpis czas z Zasobu, który można zarezerwować, który rejestruje wpis czasu. Wykonaj poniższe kroki, aby dodać mapowania do relacji 1:N z encji **Zasób, który można zarezerwować** do encji **Wpis czasu**.

1. W Eksploratorze rozwiązań w lewym okienku nawigacji kliknij pozycję **Encje > Standardowe stanowisko**.
2. Rozwiń encję **Standardowe stanowisko** i wybierz **Relacje 1:N**.
3. Kliknij dwukrotnie pozycję **zasób z możliwością rezerwacji do wpisu czasu**. Na stronie **Relacja** wybierz **Użyj mapowań pól**. 
4. Wybierz **Nowy**, aby utworzyć nowe mapowanie między polem **Standardowe stanowisko** w encji **Zasób, który można zarezerwować** a polem odwołania **Standardowe stanowisko** w encji **Wpis czasu**. 

> ![Skonfiguruj mapowanie pól, aby zezwolić na domyślne używanie wpisu czasu jako standardowego tytułu w zasobie, który można zarezerwować.](media/ST-Mapping2.png)

Spowoduje to ukończenie zmian schematu wymaganych dla niestandardowych wymiarów opartych na encji.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Dodawanie niestandardowych pól do formularzy, widoków i reguł biznesowych

Po wprowadzeniu wszystkich wymaganych zmian schematu kolejne kroki polegają na ustawieniu, aby pola były widoczne w interfejsie użytkownika przez dodanie pól do formularzy i widoków.

1. Otwórz formularz lub widok. W prawym okienku nawigacji zaznacz pole i przeciągnij je na kanwę formularza. 
2. W przypadku edytowania widoku użyj prawego okienka nawigacji, wybierz **Dodaj pola**, a następnie w oknie dialogowym **Lista pól** wybierz wymagane pola i wybierz **OK**.

Poniższa tabela zawiera wyczerpującą listę gotowych formularzy i widoków, wyszczególnionych według encji, które należy zaktualizować o te pola. Jeśli którekolwiek dodatkowe widoki lub formularze w dostosowaniach korzystają z tych encji, należy dodać nowe pola również do nich.

| Jednostka        | Formularz, które wymagają nowego pola   |Widoki, które wymagają nowego pola      |
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

Pola niestandardowe mogą być również dodawane w regułach biznesowych w zależności od zdefiniowanych opcji. Jednym z wbudowanych przykładów jest wprowadzenie reguły **możliwość edycji wpisu czasu na podstawie stanu**. Ta reguła określa, które pola muszą być zablokowane, gdy wpis czasu będzie mieć stan, który nie jest edytowalny, np. **Zatwierdzony**. Dodaj pola do tej reguły biznesowej, aby były zablokowane do edycji, kiedy wpis czasu ma status inny niż **Wersja robocza** lub **Zwrócony**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]