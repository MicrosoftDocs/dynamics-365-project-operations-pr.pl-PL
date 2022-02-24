---
title: Cenniki produktu
description: Ta temat zawiera informacje o cennikach związanych z używanych w cenach katalogowych w ofertach i kontraktach projektów.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877503"
---
# <a name="product-price-lists"></a>Cenniki produktu

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

 W Project Operations **Cenniki produktów** i powiązane jednostki pozycji cennika obsługują funkcje wyceny produktów na podstawie oferty opartej na produkcie i wierszy umowy. W przypadku produktów używanych w projektach używane są rekordy pozycji cennika dla cenników projektów. 

Produkty należy skonfigurować w taki sposób, aby miały domyślne listy kosztów i cenniki w katalogu produktów. W celu skonfigurowania domyślnych list kosztów i cenników należy użyć ceny katalogowej, kosztu standardowego i kosztu bieżącego. Domyślne ceny katalogowe są używane w wierszu oferty lub w pozycji kontraktu projektu tylko wtedy, gdy system nie może znaleźć wiersza cennika dla tego produktu w cenniku produktu ustawionym dla oferty lub kontraktu projektu.

Koszty własne w wierszach katalogu produktów można zmieniać miedzy ofertami. Ta funkcja jest ważna, ponieważ w przypadku niedokładnego śledzenia kosztów nie można ustalić zysku operacyjnego z wykonywanych projektów. Domyślnie kosztem własnym jest standardowy koszt produktu. Jednak domyślny koszt własny można aktualizować w wierszu oferty, jeśli w konkretnej ofercie istnieje inny koszt własny.

## <a name="price-list-items"></a>Pozycje cennika

Produkty z katalogu produktów można dodawać do różnych cenników. Pozycje cennika dla produktów zawsze odwołują się do określonej jednostki. Wycenę produktów figurujących na pozycjach cennika można skonfigurować jako kwotę w walucie. Alternatywnie kalkulacja ceny może być funkcją ceny katalogowej, kosztu bieżącego lub kosztu standardowego.

Funkcja wyceny obsługuje różne opcje zaokrąglania, gdy ceny produktów są skonfigurowane jako funkcja ceny katalogowej, kosztu standardowego lub kosztu bieżącego. W odniesieniu do pozycji cenników można nie tylko stosować wiele metod kalkulacji cen i opcji zaokrąglania, ale również łączyć z nimi listy rabatów. 

 
## <a name="default-product-price-list"></a>Domyślny cennik produktów
Każdy rekord odbiorcy zawiera pole **Cennik domyślny**, w którym można określić cennik odpowiadający walucie klienta. Wartość domyślna nie jest automatycznie wprowadzana w tym polu. Jeśli istnieje umowa z konkretnym odbiorcą określająca niestandardową kalkulację cen, można użyć tego pola w celu skojarzenia cennika z tym odbiorcą.

Encje Szansa sprzedaży, Oferta i Kontrakt projektu używają następującej kolejności wprowadzania domyślnych cenników produktów. Ta sama kolejność jest stosowana w cennikach projektów.

1.  Oferta
2.  Szansa sprzedaży
3.  Klient
4.  Ustawienia globalne 

Domyślnie w polu **Produkt** w wierszu oferty znajduje się lista wszystkich aktywnych produktów z cennika produktów w ofercie. Jeśli produkt został zdezaktywowany lub jest wersją roboczą, nie jest on wymieniony na tej liście, nawet jeśli znajduje się w cenniku. 

Wiersze katalogu produktów są dodawane jako wiersze faktury w pierwszej fakturze tworzonej dla kontraktu na projekt. W fakturze w wersji roboczej te wiersze faktury można usuwać. W takim przypadku wiersze będą wyświetlane na kolejnej fakturze do momentu ich zafakturowania lub do chwili wysłania faktury do klienta. Nie można zafakturować częściowej ilości w wierszu faktury za produkt. Podczas fakturowania wierszy produktów z kontraktu na projekt są tworzone wartości rzeczywiste. Jednak te wartości rzeczywiste nie są łączone z pokrewną encją projektu. Innymi słowy pozycje kontraktu projektu oparte na produktach są niezależne od jakiegokolwiek użycia opartego na projekcie. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
