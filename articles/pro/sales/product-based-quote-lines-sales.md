---
title: Omówienie wierszy oferty opartej na produkcie - wersja uproszczona
description: Ten temat zawiera informacje dotyczące pracy z wierszami ofert opartymi na produktach.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178201"
---
# <a name="product-based-quote-lines-overview---lite"></a>Omówienie wierszy oferty opartej na produkcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W Dynamics 365 Project Operations można tworzyć wiersze ofert oparte na produktach. Wiersze ofert oparte na produktach mogą być dodane ręcznie albo dotyczyć pozycji z katalogu produktów.

## <a name="product-catalog"></a>Katalog produktów

Każdy produkt w katalogu produktów ma domyślną jednostkę i grupę jednostek. Jeśli wiele produktów ma ten sam zestaw atrybutów, można utworzyć rodzinę produktów zawierających te wspólne atrybuty. 

Na przykład firma sprzedaje licencje subskrypcyjne na różne typy oprogramowania. Każdy subskrybowany program ma dwa następujące atrybuty:

- Liczba użytkowników
- Okres subskrypcji mierzony w miesiącach

Aby zachować ten typ katalogu, utwórz rodzinę produktów o nazwie **Subskrypcja oprogramowania** i dodaj liczbę użytkowników oraz czas trwania subskrypcji jako atrybuty. Następnie możesz dodać poszczególne produkty do rodziny produktów **Oprogramowanie subskrypcyjne**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Dodawanie elementów katalogu produktów do oferty projektu

Strony **Oferta projektu** i **Kontrakt projektu** zawierają sekcje: wiersze oparte na projekcie i wiersze oparte na produktach. W przypadku linii opartych na produktach lista rozwijana w wierszu oferty lub wierszu umowy dotyczącej projektu zawiera wszystkie produkty i jednostki w cenniku produktów. Można również dodawać produkty, które nie są częścią cennika produktów.

Oprócz tego można wybierać produkty z innych cenników lub bezpośrednio z katalogu produktów. W przypadku wybierania produktów bezpośrednio z katalogu produktów do ustalania ceny sprzedaży produktu jest używany domyślny cennik tego produktu. Jeśli cennik domyślny nie jest określony, system ustawia cenę zero (0).

Jeśli wiersz oferty jest oparty na katalogu produktów, można zastąpić cenę sprzedaży bezpośrednio w wierszu oferty. Wiersz oferty wpolu **Cennik** zawierający dwie dostępne wartości:

- **Zastąp Cennik**
- **Użyj domyślnej**

W przypadku wybrania opcji **Zastąp cennik** cena domyślna nie jest ustawiona. W zamian należy wprowadzić cenę produktu w wierszu oferty. W przypadku wybrania opcji **Użyj domyślnych** jest używana domyślna cena sprzedaży, a pole jest zablokowane do edycji.

Domyślne ceny sprzedaży są wprowadzana w wierszach opartych na produktach w ofercie. Następnie w polu **Kalkulacja cen** jest ustawiana wartość **Zastąp Cennik**, tak aby można było edytować domyślną cenę w wierszach oferty. Jest to zastąpienie specyficzne dla Project Operations dotyczące zachowania wierszy opartych na produkcie w rozwiązaniu Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]