---
title: Omówienie pozycji kontraktu opartego na produkcie - wersja uproszczona
description: Ta temat zawiera informacje o wierszach kontraktów opartych na produktach.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369749"
---
# <a name="product-based-contract-lines-overview---lite"></a>Omówienie pozycji kontraktu opartego na produkcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W programie Dynamics 365 Project Operations można tworzyć pozycje kontraktu oparte na produktach. Wiersze kontraktów oparte na produktach mogą być ręcznie tworzone albo dotyczyć pozycji z katalogu produktów.

## <a name="product-catalog"></a>Katalog produktów

Produkty w katalogu produktów mają domyślne jednostki i grupy jednostek. Jeśli wiele produktów ma ten sam zestaw atrybutów, można utworzyć rodzinę produktów zawierających te wspólne atrybuty. Wszystkie produkty w jednej rodzinie produktów dziedziczą ten sam zestaw atrybutów.

Na przykład firma sprzedaje licencje subskrypcyjne na różne typy oprogramowania. Każdy subskrybowany program ma dwa następujące atrybuty:

- Liczba użytkowników
- Czas trwania subskrypcji (w miesiącach)

Aby zachować katalog tego typu, należy utworzyć rodzinę produktów z nazwą **Oprogramowanie subskrypcyjne**. Dodaj atrybuty, **liczbę użytkowników** i **Czas trwania subskrypcji** do rodziny produktów. Następnie należy dodać poszczególne produkty do rodziny produktów **Oprogramowania subskrypcyjnego**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Dodawanie elementów katalogu produktów do kontraktu projektu

Kontrakty projektu dwa typy wierszy: wiersze oparte na projekcie i wiersze oparte na produktach. Wiersze oparte na produktach zawierają wszystkie produkty i jednostki z cennika produktów w kontrakcie. Można również dodawać produkty, które nie są częścią cennika produktów dołączonego do kontraktu.

Użytkownik może wybrać produkty z innych cenników lub bezpośrednio z katalogu produktów. W przypadku wybierania produktów bezpośrednio z katalogu produktów do ustalania ceny sprzedaży produktu jest używany domyślny cennik tego produktu. Jeśli cennik domyślny nie jest określony, system ustawia cenę 0 (zero).

Jeśli wiersz kontraktu jest oparty na katalogu produktów, można zastąpić cenę sprzedaży bezpośrednio w wierszu oferty. Pozycja kontraktu zawiera pole **Cennik** i dwie wartości:

- **Zastąp kalkulację ceny**
- **Użyj domyślnego**

Jeśli w polu **Kalkulacja cen** zostanie ustawiona wartość **Zastąp kalkulację ceny**, nie jest ustawiana cena domyślna. Wprowadź cenę produktu w pozycji kontraktu projektu. Jeśli pole ma **Używać wartości domyślnych**, jest używana domyślna cena sprzedaży i nie można edytować pola.

Po zainstalowaniu rozwiązania Project Operations domyślne ceny sprzedaży są wprowadzane w wierszach opartych na produktach w kontrakcie. Następnie w polu **Kalkulacja cen** jest ustawiana wartość **Zastąp kalkulację ceny**, tak aby można było edytować domyślną cenę w wierszach kontraktu. Jest to opcja zastąpienia dostępna w Project Operations dla wierszy opartych na produkcie w Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]