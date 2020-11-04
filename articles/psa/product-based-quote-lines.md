---
title: Wiersze ofert oparte na produktach
description: Ta temat zawiera informacje o wierszach ofert opartych na produktach.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082192"
---
# <a name="product-based-quote-lines"></a>Wiersze ofert oparte na produktach

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


W programie Dynamics 365 Project Service Automation można tworzyć wiersze ofert oparte na produktach. Wiersze ofert oparte na produktach mogą być „dopisywane” albo dotyczyć pozycji z katalogu produktów.

## <a name="product-catalog"></a>Katalog produktów

Produkty w katalogu produktów w rozwiązaniu Dynamics 365 mają domyślne jednostki i grupy jednostek. Jeśli wiele produktów ma ten sam zestaw atrybutów, można utworzyć rodzinę produktów zawierających te wspólne atrybuty. Wszystkie produkty w jednej rodzinie produktów dziedziczą ten sam zestaw atrybutów.

Na przykład firma sprzedaje licencje subskrypcyjne na różne oprogramowanie. Każdy subskrybowany program ma dwa następujące atrybuty:

- Liczba użytkowników 
- Czas trwania subskrypcji (w miesiącach)

Dobrym sposobem na prowadzenie tego typu katalogu jest utworzenie rodziny produktów o nazwie **Subskrypcja oprogramowania** , która ma atrybuty **Liczba użytkowników** i **Czas trwania subskrypcji**. Następnie można dodać poszczególne produkty, takie jak **Dynamics 365 Sales** lub **Dynamics 365 Field Service** , do rodziny produktów **Subskrypcja oprogramowania**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Dodawanie elementów katalogu produktów do oferty projektu

Strony Oferta projektu i Kontrakt projektu zawierają sekcje na dwa typy wierszy: wiersze oparte na projekcie i wiersze oparte na produktach. W przypadku wierszy opartych na produktach program Dynamics 365 dodaje elementy z katalogu produktów do oferty. Lista rozwijana w wierszu oferty lub pozycji kontraktu projektu zawiera wszystkie produkty i jednostki z cennika produktów dołączonego do oferty lub kontraktu na projekt. Można również dodawać produkty, które nie są częścią cennika produktów dołączonego do oferty.

Oprócz tego można wybierać produkty z innych cenników lub albo bezpośrednio z katalogu produktów. W przypadku wybierania produktów bezpośrednio z katalogu produktów do ustalania ceny sprzedaży produktu jest używany domyślny cennik tego produktu. Jeśli cennik domyślny nie jest określony, system ustawia cenę 0 (zero).

Jeśli wiersz oferty jest oparty na katalogu produktów, można zastąpić cenę sprzedaży bezpośrednio w wierszu oferty. Należy zwrócić uwagę, że wiersz oferty w programie Dynamics 365 ma pole **Kalkulacja cen**. Może ono przybierać dwie wartości:

- Zastąp kalkulację ceny  
- Użyj domyślnego

Jeśli w tym polu zostanie ustawiona wartość **Zastąp kalkulację ceny** , w usłudze Dynamics 365 nie jest ustawiana cena domyślna. Należy wprowadzić cenę produktu w wierszu oferty. Jeśli w tym polu zostanie ustawiona wartość **Użyj domyślnego** , w usłudze Dynamics 365 zostanie użyta domyślna cena sprzedaży, a pole zostanie zablokowane, aby zapobiec edytowaniu.

Po zainstalowaniu rozwiązania PSA domyślne ceny sprzedaży są wprowadzana w wierszach opartych na produktach w ofercie. Następnie w polu **Kalkulacja cen** jest ustawiana wartość **Zastąp kalkulację ceny** , tak aby można było edytować domyślną cenę w wierszach oferty.

> ![Konfigurowanie zastępowania kalkulacji ceny](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Współczynniki ilościowe dla produktów

Do obsługi sprzedaży produktów opartych na subskrypcji program PSA używa współczynników ilościowych. W przypadku produktów opartych na subskrypcji liczba w ofercie lub pozycji kontraktu projektu jest wyrażona liczbą użytkowników w miesiącu.

Zazwyczaj cena subskrybowanego oprogramowania jest przechowywana w katalogu jako cena za jednego użytkownika za jeden miesiąc. Można jednak używać również innych opisów czasu. W trakcie procesu sprzedaży cena w wierszu oferty to zazwyczaj cena na użytkownika na miesiąc, która została wynegocjowana i uzupełniona o rabat przez przedstawiciela handlowego z działu IT. Każda transakcja ma inną liczbę użytkowników i inną liczbę miesięcy subskrypcji. Ilość użyta do obliczenia kwoty w wierszu oferty jest iloczynem liczby użytkowników i liczby miesięcy subskrypcji.

W celu zapewnienia obsługi tego typu sprzedaży w rozwiązaniu PSA wprowadzono koncepcję współczynników ilościowych. Współczynniki ilościowe opierają się na atrybutach produktów w systemie Dynamics 365. Podczas konfigurowania konkretnych właściwości produktu program PSA umożliwia oflagowanie podzbioru tych właściwości albo wszystkich właściwości jako współczynników ilościowych.

System PSA weryfikuje, czy tylko właściwości liczbowe lub właściwości produktu mające liczbowy typ danych są flagowane jako współczynniki ilościowe. Gdy produkt, dla którego są konfigurowane współczynniki ilościowe, zostanie dodany do wiersza produktu, pole **Ilość** w wierszu oferty staje się polem tylko do odczytu. Po wprowadzeniu wartości właściwości produktu będących współczynnikami ilościowymi rozwiązanie PSA obliczy ilość w wierszu oferty.

Na przykład system Dynamics 365 może mieć następujące właściwości: 

- **Liczba użytkowników** — liczba użytkowników 
- **Liczba miesięcy** — liczba miesięcy subskrypcji
- **Kod SKU produktu** 

Właściwości **Liczba użytkowników** i **Liczba miesięcy** można oflagować jako współczynniki ilościowe, odpowiednio modyfikując właściwości wiersza produktu. 

> ![Flagowanie atrybutów Liczba użytkowników i Liczba miesięcy jako współczynników ilościowych](media/basic-guide-11.png)
 
