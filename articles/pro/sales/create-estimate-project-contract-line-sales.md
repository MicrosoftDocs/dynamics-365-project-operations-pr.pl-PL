---
title: Szacowanie pozycji kontraktu opartego na projekcie - wersja uproszczona
description: Ta temat zawiera informacje na temat oszacowań w pozycji kontraktu opartej na projekcie.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf7941a627375604dca778ab293756bed2536049
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858109"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Szacowanie pozycji kontraktu opartego na projekcie - wersja uproszczona

_**Zastosowane w:** Wdrażanie uproszczone — od okazji do faktury pro forma_

W Dynamics 365 Project Operations pozycja kontraktu oparta na projektach zawiera szczegółowe informacje pomocne w oszacowaniu kosztu i potencjalnego przychodu pozostałej pracy związanej z pozycjami kontraktu.

Aby oszacować pozycje kontraktu oparte na projektach, przejdź do karty **Szczegóły pozycji kontraktu** w **Pozycji kontraktu** projektu.  Istnieją dwa sposoby tworzenia oszacowania w pozycji kontraktu opartym na projekcie:

   - Aby utworzyć szacowaną bezpośrednio w pozycji kontraktu, należy ręcznie dodać szczegóły pozycji kontraktu.
   - Utworzenie projektu i planu projektu, a następnie skojarzenie projektu i zadań z pozycją kontraktu projektu. Umożliwia to proces importowania oszacowania planu projektu do pozycji kontraktu na podstawie składników zawartych w pozycji kontraktu.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Tworzenie oszacowania bezpośrednio w pozycji kontraktu opartego na projekcie

Aby utworzyć szacowanie bezpośrednio na podstawie wiersza kontraktu opartego na projekcie, wykonaj następujące kroki:

1. Przejdź do pozycji kontraktu i wybierz kartę **Szczegóły pozycji kontraktu** . Wiersze utworzone na tej karcie są sumowane i wyświetlane jako **Wartość kontraktu** dla danej **Pozycji kontraktu**. 
2. W podsiatce **Szczegóły pozycji kontraktu** wybierz pozycję **Nowe szczegóły pozycji kontraktu**. Zostanie otwarty suwak szybkiego tworzenia. Na stronie **Szczegóły wiersza kontraktu** są dostępne następujące pola.

| Pole | Lokalizacja | Opis | Wpływ zmian w dalszych etapach |
| --- | --- | --- | --- |
| **Opis** | **Szybkie tworzenie** | Opis terminu konkretnego oszacowania. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Klasa transakcji** | **Szybkie tworzenie** | Jest to lista klas transakcji zawartych na karcie **Ogólne** w wierszu kontraktu opartego na projekcie. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Wybierz produkt** | **Szybkie tworzenie** | Stosuje się, gdy klasa transakcji to **Materiał**. Możesz określić, czy ten wiersz oszacowania dotyczy produktu **Istniejącego** produktu (katalogu), czy też **Dopisane** produktu. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Produkt** | **Szybkie tworzenie** | Identyfikator produktu z katalogu produktów. To pole jest aktywne tylko po wybraniu opcji **Istniejący produkt** w polu **Wybierz produkt**. Identyfikator jest używany do pobierania ceny sprzedaży z cennika projektu dla kontraktu. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Produkt dopisany** | **Szybkie tworzenie** | Pole tekstowe służące do wprowadzania nazwy produktu. To pole jest dostępne tylko po wybraniu opcji **Dopisanie** w polu **Wybierz produkt**.| Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Rola** | **Szybkie tworzenie** | Rola osoby wykonującej prace lub korzystającej z tego wydatku. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie.|
| **Kategoria** | **Szybkie tworzenie** | Kategoria pracy lub wydatku. |Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie.|
| **Data rozpoczęcia** | **Szybkie tworzenie** | Data rozpoczęcia pracy. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Data zakończenia** | **Szybkie tworzenie** | Data zakończenia pracy. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Jednostka zasobów** | **Szybkie tworzenie** | Jednostka zaopatrzeniowa, która ponosi ten koszt i zapewnia zasoby do pracy. |Ta wartość jest wartością domyślną dla powiązanego szczegółu pozycji kontraktu dla kosztu, który jest tworzony automatycznie i jest używany do pobierania ceny kosztu. |
| **Harmonogram jednostek** | **Szybkie tworzenie** | Grupa jednostek pracy, produktu lub wydatku. Jednostki należą do harmonogramu jednostek lub grupy jednostek. Na przykład *mile* i *kilometry (kms)* to jednostki należące do grupy jednostek, które opisują odległość. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Jednostka** | **Szybkie tworzenie** | Jednostka pracy, produkt lub wydatek. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Ilość** | **Szybkie tworzenie** | Ilość pracy, produkt lub wydatek. | Ta wartość jest wartością domyślną dla powiązanych szczegółów pozycji kontraktu dla kosztów, które są tworzone automatycznie. |
| **Cena jednostkowa** | **Szybkie tworzenie** | Stawka fakturowa roli, która wykonuje pracę, cena jednostkowa produktu lub cena sprzedaży produktu lub kategorii wydatków. To pole ma wartość domyślną **Czas** na podstawie kombinacji wartości wymiarów wyceny w wierszu ceny roli cennika projektu, który obowiązuje od daty rozpoczęcia. W przypadku **Kosztów** wartość tego pola jest domyślna określana na podstawie konfiguracji ceny w danej kategorii transakcji w cenniku projektu, która obowiązuje w stosunku do daty rozpoczęcia. Jeśli w kategorii transakcji wybrana jest inna metoda kalkulacji cen niż **cena jednostkowa**, nie zostanie zastosowana wartość domyślna, a to pole pozostanie puste. Wartość domyślna tego pola jest oparta na pozycji cennika w **Cenniku projektu**, która obowiązuje w dniu rozpoczęcia.| Stawka kosztów roli wykonującej pracę lub koszt jednostkowy kategorii wydatków lub koszt jednostkowy produktu. To pole ma wartość domyślną **Czas** w oparciu o kombinację wartości wymiarów wyceny w wierszu ceny roli w cenniku własnym dołączonym do jednostki zamawiającej obowiązującej od daty rozpoczęcia. W przypadku wydatków wartość domyślna tego pola jest oparta na wierszu ceny kategorii w cenniku własnym dołączonym do jednostki umownej, która obowiązuje od daty rozpoczęcia. Jeśli w kategorii transakcji wybrana jest inna metoda kalkulacji cen niż cena jednostkowa, nie zostanie zastosowana wartość domyślna, a to pole pozostanie puste. Wartość domyślna tego pola jest oparta na **Pozycji cennika**  w Cenniku projektu dołączonego do jednostki zamawiającej, która obowiązuje od daty rozpoczęcia.|
| **Szacowany podatek** | **Szybkie tworzenie** | Szacowany podatek dla tej pracy lub wydatku. | Szacowany podatek dla tej pracy lub wydatku. |
| **Kwota** | **Szybkie tworzenie** | W tym polu można dodać wartość, jeśli pola **Ilość** i **Cena** pozostawią puste. Jeśli **ilość** i **Cena** są wypełnione, pole **Kwoty** jest przeznaczone tylko do odczytu i jest obliczane jako **(Ilość \* Cena jednostkowa) + podatek**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualizowanie cen w wierszach kontraktu

W przypadku zmiany cen w cenniku projektu, które są dołączone do kontraktu lub cennika kosztów na jednostkę zamawiającą, można odświeżyć ceny w poszczególnych wierszach kontraktu w celu odzwierciedlenia zmian. Na stronie **Kontrakt** wybierz pozycję **Oblicz ponownie**. Pojawia się ostrzeżenie informujące, że ceny wszystkich pozycji kontraktu w tej umowie zostały zresetowane. Wybierz opcję **Tak**, aby odświeżyć ceny zarówno dla sprzedaży, jak i dla wierszy kontraktu kosztowego.

## <a name="access-contract-line-details-for-cost"></a>Dostęp do szczegółów wiersza kontraktu dostępu

Z poziomu karty **Szczegóły pozycji kontraktu** wybierz wiersz w siatce, aby wyświetlić niektóre akcje na pasku narzędzi w podsiatce. Pierwsza akcja na pasku narzędzi w podsiatce powoduje **Otwarcie szczegółów kosztów**. Aby wyświetlić pokrewną stawkę kosztów i kwotę dotyczącą szczegółów danego wiersza kontraktu, wybierz pozycję **Otwarcie szczegółów kosztów**. 

> [!NOTE]
> Zmiana wartości składnika reźródłem, przekroczenie jednostki, ilość, daty, rola lub kategoria w pozycji kontraktu szczegóły dotyczące **Koszt** spowoduje zmianę odpowiednich wartości w szczegółach pozycji kontraktu dotyczącej **Sprzedaży**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Waluta w wierszu kontraktu szczegóły dotyczące kosztów i sprzedaży

Szczegóły wiersza kontraktu dla **Sprzedaży** ustawiają domyślną walutę z cennika projektu, która obowiązuje od daty rozpoczęcia szczegółów wiersza kontraktu.

Szczegóły wiersza kontraktu dla **Kosztu** ustawiają domyślną walutę z cennika jednostki kontraktu, która obowiązuje od daty rozpoczęcia szczegółów wiersza kontraktu dla **Kosztu**.

Obliczenia rentowności konwertują kwoty dla szczegółów pozycji kontraktu dotyczące **Kosztów** i **Sprzedaży** w walutę podstawową środowiska, aby raportować ogólne i szacowane marginesy kontraktu.

> [!NOTE]
> Błędy zaokrąglania walut i zmienione marginesy mogą nastąpić z powodu braku aktualnych kursów wymiany. Obliczenia te należy stosować tylko w przypadku umów dotyczących projektów, ponieważ są one przybliżone i nie służą do rzeczywistych sprawozdań ustawowych lub innych, które wymagają większej precyzji zaokrąglania i świadomości skuteczności dat dla kursów wymiany.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
