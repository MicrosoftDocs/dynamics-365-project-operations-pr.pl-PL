---
title: Kalkulacja cen w katalogu produktów
description: W tym temacie przedstawiono informacje na temat sposobu funkcjonowania aparatu kalkulacji cen w katalogu produktów w programie Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 3fb9b51d58cbe3b0db6dad902461b90ac04cc42f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151221"
---
# <a name="product-catalog-pricing"></a>Kalkulacja cen w katalogu produktów 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Encje Cennik i Pozycja cennika obsługują kalkulacje cen w katalogach produktów. W większości przypadków ta funkcjonalność jest używana do wierszy opartych na katalogach w ofertach projektów i kontraktach projektów.

W przypadku wierszy opartych na projektach kontrakt reprezentuje transakcję po zdobyciu zamówienia. Ponieważ zwycięstwo jest zwykle poprzedzone procesem negocjowania, kalkulacja cen dołączana do oferty jest zawsze kopiowana w swoim aktualnym stanie do nowego cennika i dołączana do kontraktu. Nowego cennika nie można modyfikować poza zakresem kontraktu. To ograniczenie pomaga chronić kartę wynegocjowanych stawek przed wszelkimi zmianami zachodzącymi w głównym cenniku.

Produkty należy skonfigurować w taki sposób, aby miały domyślne listy kosztów i cenniki w katalogu produktów. W celu skonfigurowania domyślnych list kosztów i cenników należy użyć ceny katalogowej, kosztu standardowego i kosztu bieżącego. Domyślne ceny katalogowe są używane w wierszu oferty lub w pozycji kontraktu projektu tylko wtedy, gdy system nie może znaleźć wiersza cennika dla tego produktu w cenniku produktu ustawionym dla oferty lub kontraktu projektu.

Koszty własne w wierszach katalogu produktów można zmieniać miedzy ofertami. Ta funkcja jest ważna, ponieważ w przypadku niedokładnego śledzenia kosztów nie można ustalić zysku operacyjnego z wykonywanych projektów. Domyślnie kosztem własnym jest standardowy koszt produktu. Jednak domyślny koszt własny można aktualizować w wierszu oferty, jeśli w konkretnej ofercie istnieje inny koszt własny.

## <a name="price-list-items"></a>Pozycje cennika

Produkty z katalogu produktów można dodawać do różnych cenników. Pozycje cennika dla produktów zawsze odwołują się do określonej jednostki. Wycenę produktów figurujących na pozycjach cennika można skonfigurować jako kwotę w walucie. Alternatywnie kalkulacja ceny może być funkcją ceny katalogowej, kosztu bieżącego lub kosztu standardowego.

Program PSA obsługuje różne opcje zaokrąglania, gdy ceny są skonfigurowane jako funkcje ceny katalogowej, kosztu standardowego lub kosztu bieżącego. W odniesieniu do pozycji cenników można nie tylko stosować wiele metod kalkulacji cen i opcji zaokrąglania, ale również łączyć z nimi listy rabatów. 

> ![Dodawanie produktów z katalogu do różnych cenników](media/basic-guide-16.png)

Podczas tworzenia nowego cennika niestandardowego dla oferty poprzez wybranie opcji **Utwórz niestandardową kalkulację cen** na stronie **Oferta projektu** program PSA tworzy kopię cennika, a w polu **Encja** w nagłówku nowego cennika ustawia wartość **Encja sprzedaży**. Do nazwy nowego cennika jest dołączana nazwa oferty oraz sygnatura czasowa. Nazwy nowego cennika i nazwy oferty można również używać w niestandardowych przepływach pracy w celu inicjowania dodatkowej weryfikacji i zatwierdzania ofert korzystających z niestandardowej kalkulacji cen.

 
## <a name="default-product-price-list"></a>Domyślny cennik produktów
Każdy rekord odbiorcy zawiera pole **Cennik domyślny**, w którym można określić cennik odpowiadający walucie klienta. W usłudze PSA wartość domyślna nie jest automatycznie wprowadzana w tym polu. Jeśli istnieje umowa z konkretnym odbiorcą określająca niestandardową kalkulację cen, można użyć tego pola w celu skojarzenia cennika z tym odbiorcą.

Encje Szansa sprzedaży, Oferta i Kontrakt projektu używają następującej kolejności wprowadzania domyślnych cenników produktów. Ta sama kolejność jest stosowana w cennikach projektów.

1.  Oferta
2.  Szansa sprzedaży
3.  Klient
4.  Ustawienia globalne dla PSA

Domyślnie w polu **Produkt** w wierszu oferty znajduje się lista wszystkich aktywnych produktów z cennika produktów w ofercie. Jeśli produkt został zdezaktywowany lub jest wersją roboczą, nie jest on wymieniony na tej liście, nawet jeśli znajduje się w cenniku. 

Wiersze katalogu produktów są dodawane jako wiersze faktury w pierwszej fakturze tworzonej dla kontraktu na projekt. W fakturze w wersji roboczej te wiersze faktury można usuwać. W takim przypadku wiersze będą wyświetlane na kolejnej fakturze do momentu ich zafakturowania lub do chwili wysłania faktury do klienta. W rozwiązaniu PSA nie można zafakturować częściowej ilości w wierszu faktury za produkt. Podczas fakturowania wierszy produktów z kontraktu na projekt są tworzone wartości rzeczywiste. Jednak te wartości rzeczywiste nie są łączone z pokrewną encją projektu. Innymi słowy pozycje kontraktu projektu oparte na produktach są niezależne od jakiegokolwiek użycia opartego na projekcie. Program PSA nie śledzi zużycia materiałów w projektach.


[!INCLUDE[footer-include](../includes/footer-banner.md)]