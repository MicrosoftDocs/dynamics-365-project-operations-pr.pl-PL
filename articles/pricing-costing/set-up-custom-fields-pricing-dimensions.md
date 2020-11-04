---
title: Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen
description: Ten temat zawiera informacje na temat konfiguracji niestandardowych wymiarów kalkulacji cen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 087950c9639a95868a20d71286dfad4437555108
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082007"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Założono, że przed rozpoczęciem tej procedury użytkownik wykonał procedury opisane w tematach [Tworzenie niestandardowych pól i encji](create-custom-fields-entities-pricing-dimensions.md) i [Dodawanie wymaganych niestandardowych pól do konfiguracji cen i encji transakcyjnych](add-custom-fields-price-setup-transactional-entities.md). Jeśli tych procedur jeszcze nie wykonano, wróć, wykonaj je, a następnie wróć do tego tematu. 

Ten temat zawiera informacje na temat konfigurowania niestandardowych wymiarów kalkulacji cen. Na stronie **Parametry** na karcie **Wymiary kalkulacji cen oparte na kwocie** zwróć uwagę, że pokazywane są encje wymiarów kalkulacji cen. Na tej karcie domyślnie istnieją dwa wiersze siatki:

- **msdyn_resourcecategory** (Rola)
- **msdyn_OrganizationalUnit** (Jednostka organizacyjna)

> [!IMPORTANT]
> Nie usuwaj tych wierszy. Jeśli jednak nie są potrzebne, można je określić jako niemające zastosowania w konkretnym kontekście. W tym celu w ustawieniach **Ma zastosowanie do kosztu** , **Ma zastosowanie do sprzedaży** i **Ma zastosowanie do zakupu** należy zaznaczyć wartość **Nie**. Ustawienie w tych atrybutach wartości **Nie** ma taki sam skutek, jak wyłączenie tym polom funkcjonalności wymiarów kalkulacji cen.

Aby pole było wymiarem kalkulacji cen, musi być:

- Utworzone jako pole w encjach **Cena roli** i **Narzut na cenę dla roli**. Aby uzyskać więcej informacji na ten temat, zobacz [Dodawanie niestandardowych pól do konfiguracji cen i encji transakcyjnych](add-custom-fields-price-setup-transactional-entities.md).
- Utworzone jako wiersz w tabeli **Wymiar kalkulacji cen**. Na przykład dodaj wiersze wymiarów kalkulacji cen jak pokazano na poniższym rysunku. 

Godziny pracy zasobu ( **msdyn_resourceworkhours** ) została dodana jako wymiar oparty na narzucie oraz dodana do siatki na karcie **Wymiar kalkulacji cen oparty na narzucie**.

> [!IMPORTANT]
> Każda zmiana lub dodanie danych wymiaru kalkulacji cen w tej tabeli jest rozpowszechniana do logiki biznesowej kalkulacji cen w usłudze dopiero po odświeżeniu pamięci podręcznej. Czas odświeżania pamięci podręcznej może wynosić do 10 minut. Poczekaj ten czas, aby zobaczyć zmiany w logice ustawiania domyślnych cen, które muszą wyniknąć ze zmiany danych wymiaru kalkulacji cen.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atrybuty tabeli Wymiary kalkulacji cen
W poniższych sekcjach przedstawiono informacje o różnych atrybutach istniejących w tabeli **Wymiary kalkulacji cen**.

### <a name="pricing-dimension-name"></a>Nazwa wymiaru kalkulacji cen
Ta wartość powinna być identyczna, jak nazwa schematu pola dodawanego do tabeli **Cena roli** dla niestandardowych wymiarów kalkulacji cen. Aby uzyskać więcej informacji o dodawaniu pól do tabeli **Cena roli** , zobacz [Dodawanie niestandardowych pól do konfiguracji cen i encji transakcyjnych](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Typ wymiaru
Istnieją dwa typy wymiarów kalkulacji cen:
  
  - **Wymiary oparte na kwotach** : wartości wymiarów z kontekstu wejściowego są dopasowywane do wartości wymiarów w wierszu **Cena roli** , a domyślna wartość ceny/kosztu jest pobierana bezpośrednio z tabeli **Cena roli**.
  - **Wymiary oparte na narzutach** : są to wymiary, w których zastosowany jest następujący 3-etapowy proces pozyskiwania wartości ceny/kosztu:
 
    1. Dopasowanie wartości wymiarów nieopartych na narzutach z kontekstu wejściowego do wiersza Cena roli w celu wyznaczenia stawki podstawowej.
    2. Dopasowanie wszystkich wartości wymiarów z kontekstu wejściowego do wiersza **Narzut na cenę dla roli** w celu wyznaczenia procenta narzutu.
    3. Zastosowanie procentowego narzutu z drugiego kroku do stawki podstawowej pobranej z tabeli **Cena roli** w pierwszym kroku i w ten sposób ustalenie końcowej ceny/kosztu.
   
   Poniższa tabela ilustruje obliczanie narzutów na ceny.
  
| Rola        | Jednostka organizacyjna    |Lokalizacja pracy      |Standardowe stanowisko      |Godziny pracy zasobu      |  Narzut|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Na miejscu            |                    |Nadgodziny                 |15     |
|             | Contoso India|Lokalny             |                    |Nadgodziny                 |10     |
|             | Contoso US   |Lokalny             |                    |Nadgodziny                 |20     |


Jeśli zasób z firmy Contoso India, którego stawka podstawowa to 100 USD, pracuje na miejscu, a we wpisie czasu odnotuje 8 godzin regularnego czasu pracy i 2 godziny nadgodzin, aparat kalkulacji cen użyje stawki podstawowej 100 dla 8 godzin i w ten sposób zarejestruje 800 USD. Dla 2 godzin nadgodzin zastosuje narzut 15% do stawki podstawowej 100 USD, uzyskując w ten sposób cenę jednostkową 115 USD i odnotowując łączny koszt 230 USD.

### <a name="applicable-to-cost"></a>Ma zastosowanie do kosztu 
Zaznaczenie wartości **Tak** oznacza, że wartość wymiaru z kontekstu wejściowego powinna być dopasowywana do wartości w encjach **Cena roli** i **Narzut na cenę dla roli** podczas pobierania stawek kosztów i narzutów.

### <a name="applicable-to-sales"></a>Ma zastosowanie do sprzedaży
Zaznaczenie wartości **Tak** oznacza, że wartość wymiaru z kontekstu wejściowego powinna być dopasowywana do wartości w encjach **Cena roli** i **Narzut na cenę dla roli** podczas pobierania stawek rozliczania i narzutów.

### <a name="applicable-to-purchase"></a>Ma zastosowanie do zakupu
Zaznaczenie wartości **Tak** oznacza, że wartość wymiaru z kontekstu wejściowego powinna być dopasowywana do wartości w encjach **Cena roli** i **Narzut na cenę dla roli** podczas pobierania ceny zakupu. Scenariusze podwykonawców nie są obsługiwane, więc to pole nie jest używane. 

### <a name="priority"></a>Priorytet
Ustawienie priorytetu wymiaru ułatwia aparatowi kalkulacji cen wygenerowanie ceny nawet wtedy, gdy nie może znaleźć dokładnego dopasowania między wartościami wymiarów wejściowych a wartościami z tabel **Cena roli** lub **Narzut na cenę dla roli**. W tym scenariuszu usługa będzie używać wartości null dla niedopasowanych wartości wymiarów poprzez nadanie wymiarom wag w kolejności ich priorytetu.

- **Priorytet kosztu** : wartość priorytetu kosztu w wymiarze wskazuje wagę tego wymiaru podczas dopasowywania do konfiguracji kosztów własnych. Wartość pola **Priorytet kosztu** musi być unikatowa wśród wymiarów z ustawionym atrybutem **Ma zastosowanie do kosztu**.
- **Priorytet sprzedaży** : wartość priorytetu sprzedaży w wymiarze wskazuje wagę tego wymiaru podczas dopasowywania do konfiguracji cen sprzedaży lub stawek rozliczania. Wartość pola **Priorytet sprzedaży** musi być unikatowa wśród wymiarów z ustawionym atrybutem **Ma zastosowanie do sprzedaży**.
