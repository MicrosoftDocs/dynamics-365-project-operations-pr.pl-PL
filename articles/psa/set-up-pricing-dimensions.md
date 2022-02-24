---
title: Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen
description: Ten temat zawiera informacje na temat konfigurowania niestandardowych wymiarów kalkulacji cen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150366"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Konfigurowanie pól niestandardowych jako wymiarów kalkulacji cen 

[!include [banner](../includes/psa-now-project-operations.md)]

Założono, że przed rozpoczęciem tej procedury użytkownik wykonał procedury opisane w tematach [Tworzenie niestandardowych pól i encji](create-custom-fields-entities.md) i [Dodawanie niestandardowych pól do konfiguracji cen i encji transakcyjnych](field-references.md). Jeśli tych procedur jeszcze nie wykonano, wróć, wykonaj je, a następnie wróć do tego tematu. 

Ten temat zawiera informacje na temat konfigurowania niestandardowych wymiarów kalkulacji cen. W interfejsie internetowym usługi Project Service na stronie **Parametry** karta **Wymiary kalkulacji cen oparte na kwocie** pokazuje rekordy z encji wymiaru kalkulacji cen. Domyślnie instalacja aplikacji Project Service powoduje utworzenie dwóch wierszy w siatce na tej karcie:

- **msdyn_resourcecategory** (Rola)
- **msdyn_OrganizationalUnit** (Jednostka organizacyjna)

> [!IMPORTANT]
> Nie usuwaj tych wierszy. Jeśli jednak nie są potrzebne, można je określić jako niemające zastosowania w konkretnym kontekście. W tym celu w ustawieniach **Ma zastosowanie do kosztu**, **Ma zastosowanie do sprzedaży** i **Ma zastosowanie do zakupu** należy zaznaczyć wartość **Nie**. Ustawienie w tych atrybutach wartości **Nie** ma taki sam skutek, jak wyłączenie tym polom funkcjonalności wymiarów kalkulacji cen.

Aby pole było wymiarem kalkulacji cen, musi być:

- Utworzone jako pole w encjach **Cena roli** i **Narzut na cenę dla roli**. Aby uzyskać więcej informacji na ten temat, zobacz [Dodawanie niestandardowych pól do konfiguracji cen i encji transakcyjnych](field-references.md).
- Utworzone jako wiersz w tabeli **Wymiar kalkulacji cen**. Na przykład dodaj wiersze wymiarów kalkulacji cen jak pokazano na poniższym rysunku. 

![Wiersze wymiarów kalkulacji cen opartych na kwocie](media/Amt-based-PD.png)

Zauważ, że encja Godziny pracy zasobu (**msdyn_resourceworkhours**) została dodana jako wymiar oparty na narzucie oraz dodana do siatki na karcie **Wymiar kalkulacji cen oparty na narzucie**.

![Wiersze wymiaru kalkulacji cen opartego na narzucie](media/Markup-based-PD.png)

> [!IMPORTANT]
> Każda zmiana lub dodanie danych wymiaru kalkulacji cen w tej tabeli jest rozpowszechniana do logiki biznesowej kalkulacji cen w usłudze Project Service dopiero po odświeżeniu pamięci podręcznej. Czas odświeżania pamięci podręcznej może wynosić do 10 minut. Poczekaj ten czas, aby zobaczyć zmiany w logice ustawiania domyślnych cen, które muszą wyniknąć ze zmiany danych wymiaru kalkulacji cen.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atrybuty tabeli Wymiary kalkulacji cen
W poniższych sekcjach przedstawiono informacje o różnych atrybutach istniejących w tabeli **Wymiary kalkulacji cen**.

### <a name="pricing-dimension-name"></a>Nazwa wymiaru kalkulacji cen
Ta wartość powinna być identyczna, jak nazwa schematu pola dodawanego do tabeli **Cena roli** dla niestandardowych wymiarów kalkulacji cen. Aby uzyskać więcej informacji o dodawaniu pól do tabeli **Cena roli**, zobacz [Dodawanie niestandardowych pól do konfiguracji cen i encji transakcyjnych](field-references.md).

### <a name="type-of-dimension"></a>Typ wymiaru
Istnieją dwa typy wymiarów kalkulacji cen:
  
  - **Wymiary oparte na kwotach**: wartości wymiarów z kontekstu wejściowego są dopasowywane do wartości wymiarów w wierszu **Cena roli**, a domyślna wartość ceny/kosztu jest pobierana bezpośrednio z tabeli **Cena roli**.
  - **Wymiary oparte na narzutach**: są to wymiary, w których usługa Project Service stosuje następujący 3-etapowy proces pozyskiwania wartości ceny/kosztu:
 
    1. Usługa Project Service dopasowuje wartości wymiarów nieopartych na narzutach z kontekstu wejściowego do wiersza Cena roli w celu wyznaczenia stawki podstawowej.
    2. Usługa Project Service dopasowuje wszystkie wartości wymiarów z kontekstu wejściowego do wiersza **Narzut na cenę dla roli** w celu wyznaczenia procenta narzutu.
    3. Usługa Project Service stosuje procent narzutu z drugiego kroku do stawki podstawowej pobranej z tabeli **Cena roli** w pierwszym kroku i w ten sposób ustala końcową cenę/koszt.
   
   Poniższa tabela ilustruje obliczanie narzutów na ceny.
  
| Rola        | Jednostka organizacyjna    |Lokalizacja pracy      |Standardowe stanowisko      |Godziny pracy zasobu      |  Narzut|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Na miejscu            |                    |Nadgodziny                 |15     |
|             | Contoso India|Lokalny             |                    |Nadgodziny                 |10     |
|             | Contoso US   |Lokalny             |                    |Nadgodziny                 |20     |


Jeśli zasób z firmy Contoso India, którego stawka podstawowa to 100 USD, pracuje na miejscu, a we wpisie czasu odnotuje 8 godzin regularnego czasu pracy i 2 godziny nadgodzin, aparat kalkulacji cen w usłudze Project Service użyje stawki podstawowej 100 dla 8 godzin i w ten sposób zarejestruje 800 USD. Dla 2 godzin nadgodzin zastosuje narzut 15% do stawki podstawowej 100 USD, uzyskując w ten sposób cenę jednostkową 115 USD i odnotowując łączny koszt 230 USD.

### <a name="applicable-to-cost"></a>Ma zastosowanie do kosztu 
Zaznaczenie wartości **Tak** oznacza, że wartość wymiaru z kontekstu wejściowego powinna być dopasowywana do wartości w encjach **Cena roli** i **Narzut na cenę dla roli** podczas pobierania stawek kosztów i narzutów.

### <a name="applicable-to-sales"></a>Ma zastosowanie do sprzedaży
Zaznaczenie wartości **Tak** oznacza, że wartość wymiaru z kontekstu wejściowego powinna być dopasowywana do wartości w encjach **Cena roli** i **Narzut na cenę dla roli** podczas pobierania stawek rozliczania i narzutów.

### <a name="applicable-to-purchase"></a>Ma zastosowanie do zakupu
Zaznaczenie wartości **Tak** oznacza, że wartość wymiaru z kontekstu wejściowego powinna być dopasowywana do wartości w encjach **Cena roli** i **Narzut na cenę dla roli** podczas pobierania ceny zakupu. Obecnie usługa Project Service nie obsługuje scenariuszy podwykonawstwa, więc to pole nie jest używane. 

### <a name="priority"></a>Priorytet
Ustawienie priorytetu wymiaru ułatwia aparatowi kalkulacji cen w usłudze Project Service wygenerowanie ceny nawet wtedy, gdy nie może znaleźć dokładnego dopasowania między wartościami wymiarów wejściowych a wartościami z tabel **Cena roli** lub **Narzut na cenę dla roli**. W tym scenariuszu usługa Project Service będzie używać wartości null dla niedopasowanych wartości wymiarów poprzez nadanie wymiarom wag w kolejności ich priorytetu.

- **Priorytet kosztu**: wartość priorytetu kosztu w wymiarze wskazuje wagę tego wymiaru podczas dopasowywania do konfiguracji kosztów własnych. Wartość pola **Priorytet kosztu** musi być unikatowa wśród wymiarów z ustawionym atrybutem **Ma zastosowanie do kosztu**.
- **Priorytet sprzedaży**: wartość priorytetu sprzedaży w wymiarze wskazuje wagę tego wymiaru podczas dopasowywania do konfiguracji cen sprzedaży lub stawek rozliczania. Wartość pola **Priorytet sprzedaży** musi być unikatowa wśród wymiarów z ustawionym atrybutem **Ma zastosowanie do sprzedaży**.
