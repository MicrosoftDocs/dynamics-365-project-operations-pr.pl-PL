---
title: Cenniki produktu
description: Ta temat zawiera informacje o cennikach związanych z używanych w cenach katalogowych w ofertach i kontraktach projektów.
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
ms.openlocfilehash: 702402854c0787dae0bde854c9c274f5c23c131f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119611"
---
# <a name="product-price-lists"></a>Cenniki produktu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Encje Cennik i Pozycja cennika obsługują kalkulacje cen w katalogach produktów. W większości przypadków ta funkcjonalność jest używana do wierszy opartych na katalogach w ofertach projektów i kontraktach projektów.

W przypadku wierszy opartych na projektach kontrakt reprezentuje transakcję po zdobyciu zamówienia. Ponieważ zwycięstwo jest zwykle poprzedzone procesem negocjowania, kalkulacja cen dołączana do oferty jest zawsze kopiowana w swoim aktualnym stanie do nowego cennika i dołączana do kontraktu. Nowego cennika nie można modyfikować poza zakresem kontraktu. To ograniczenie pomaga chronić kartę wynegocjowanych stawek przed wszelkimi zmianami zachodzącymi w głównym cenniku.

Produkty należy skonfigurować w taki sposób, aby miały domyślne listy kosztów i cenniki w katalogu produktów. W celu skonfigurowania domyślnych list kosztów i cenników należy użyć ceny katalogowej, kosztu standardowego i kosztu bieżącego. Domyślne ceny katalogowe są używane w wierszu oferty lub w pozycji kontraktu projektu tylko wtedy, gdy system nie może znaleźć wiersza cennika dla tego produktu w cenniku produktu ustawionym dla oferty lub kontraktu projektu.

Koszty własne w wierszach katalogu produktów można zmieniać miedzy ofertami. Ta funkcja jest ważna, ponieważ w przypadku niedokładnego śledzenia kosztów nie można ustalić zysku operacyjnego z wykonywanych projektów. Domyślnie kosztem własnym jest standardowy koszt produktu. Jednak domyślny koszt własny można aktualizować w wierszu oferty, jeśli w konkretnej ofercie istnieje inny koszt własny.

## <a name="price-list-items"></a>Pozycje cennika

Produkty z katalogu produktów można dodawać do różnych cenników. Pozycje cennika dla produktów zawsze odwołują się do określonej jednostki. Wycenę produktów figurujących na pozycjach cennika można skonfigurować jako kwotę w walucie. Alternatywnie kalkulacja ceny może być funkcją ceny katalogowej, kosztu bieżącego lub kosztu standardowego.

Program PSA obsługuje różne opcje zaokrąglania, gdy ceny są skonfigurowane jako funkcje ceny katalogowej, kosztu standardowego lub kosztu bieżącego. W odniesieniu do pozycji cenników można nie tylko stosować wiele metod kalkulacji cen i opcji zaokrąglania, ale również łączyć z nimi listy rabatów. 

Podczas tworzenia nowego cennika niestandardowego dla oferty poprzez wybranie opcji **Utwórz niestandardową kalkulację cen** na stronie **Oferta projektu** program tworzy kopię cennika, a w polu **Encja** w nagłówku nowego cennika ustawia wartość **Encja sprzedaży**. Do nazwy nowego cennika jest dołączana nazwa oferty oraz sygnatura czasowa. Nazwy nowego cennika i nazwy oferty można również używać w niestandardowych przepływach pracy w celu inicjowania dodatkowej weryfikacji i zatwierdzania ofert korzystających z niestandardowej kalkulacji cen.

 
## <a name="default-product-price-list"></a>Domyślny cennik produktów
Każdy rekord odbiorcy zawiera pole **Cennik domyślny**, w którym można określić cennik odpowiadający walucie klienta. Wartość domyślna nie jest automatycznie wprowadzana w tym polu. Jeśli istnieje umowa z konkretnym odbiorcą określająca niestandardową kalkulację cen, można użyć tego pola w celu skojarzenia cennika z tym odbiorcą.

Encje Szansa sprzedaży, Oferta i Kontrakt projektu używają następującej kolejności wprowadzania domyślnych cenników produktów. Ta sama kolejność jest stosowana w cennikach projektów.

1.  Oferta
2.  Szansa sprzedaży
3.  Klient
4.  Ustawienia globalne 

Domyślnie w polu **Produkt** w wierszu oferty znajduje się lista wszystkich aktywnych produktów z cennika produktów w ofercie. Jeśli produkt został zdezaktywowany lub jest wersją roboczą, nie jest on wymieniony na tej liście, nawet jeśli znajduje się w cenniku. 

Wiersze katalogu produktów są dodawane jako wiersze faktury w pierwszej fakturze tworzonej dla kontraktu na projekt. W fakturze w wersji roboczej te wiersze faktury można usuwać. W takim przypadku wiersze będą wyświetlane na kolejnej fakturze do momentu ich zafakturowania lub do chwili wysłania faktury do klienta. Nie można zafakturować częściowej ilości w wierszu faktury za produkt. Podczas fakturowania wierszy produktów z kontraktu na projekt są tworzone wartości rzeczywiste. Jednak te wartości rzeczywiste nie są łączone z pokrewną encją projektu. Innymi słowy pozycje kontraktu projektu oparte na produktach są niezależne od jakiegokolwiek użycia opartego na projekcie. Nie jest śledzone zużycie materiałów w projektach.
