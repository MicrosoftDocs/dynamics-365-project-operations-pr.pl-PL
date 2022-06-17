---
title: Szacowanie wiersza oferty projektu
description: W tym artykule przedstawiono informacje na temat sposobu tworzenia szacowanej wartości wiersza oferty dotyczącej projektu.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fd387da51da6e85e740aef529d488adcdf27c9a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912642"
---
# <a name="estimate-a-project-quote-line"></a>Szacowanie wiersza oferty projektu

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Wiersz oferty opartej na projekcie zawiera szczegółowe informacje pomocne przy szacowaniu kosztów i potencjalnego przychodu związanych z pracą mającą na celu dostarczenie danego wiersza oferty.

Aby szacować wiersz oferty oparty na projekcie, w wierszu oferty wybierz kartę **Szczegóły wiersza oferty**. Istnieją dwa sposoby tworzenia szacowań w wierszu oferty opartej na projektach:

   - Ręczne tworzenie oszacowania bezpośrednio w wierszu oferty przy użyciu szczegółów wiersza oferty. 
   - Utworzenie projektu i planu projektu, a następnie skojarzenie projektu i zadań w projekcie z wierszem oferty. Proces importowania oszacowań z planu projektu na wiersz oferty na podstawie podanych informacji zostanie włączony.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Tworzenie szacowań bezpośrednio na wierszu oferty opartej na projekcie

Aby utworzyć szacunki bezpośrednio w wierszu oferty opartej na projekcie, wykonaj następujące kroki:

1. Aby utworzyć oszacowanie w wierszu oferty opartej na projekcie, wybierz kartę **Szczegóły wiersza oferty**. Utworzony w ten sposób wiersz będzie sumować wartość cytowaną dla danego wiersza oferty. 
2. Aby utworzyć Szczegóły wiersza oferty, można wybrać nowe **Szczegóły wiersza oferty** z podsiatki **Szczegóły wierszy oferty**. Zostanie otwarty suwak szybkiego tworzenia. Poniższe pola na stronie **Wiersz oferty**.

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Opis | Szybkie tworzenie | Opis terminu konkretnego oszacowania. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Klasa transakcji | Szybkie tworzenie | Ta lista rozwijana zawiera klasy transakcji uwzględnione na karcie **Ogólne** w wierszu oferty opartej na projekcie.  | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Wybierz produkt | Szybkie tworzenie | Stosuje się, gdy klasa transakcji to **Materiał**. Możesz określić, czy ten wiersz oszacowania dotyczy produktu **Istniejącego** produktu (katalogu), czy też **Dopisane** produktu. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Produkt | Szybkie tworzenie | Identyfikator produktu z katalogu produktów. To pole jest aktywne tylko po wybraniu opcji **Istniejący** w polu **Wybierz produkt**. Identyfikator jest używany do pobierania ceny sprzedaży z cennika projektu dla oferty. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Dopisz produkt | Szybkie tworzenie | Pole tekstowe dopisania nazwy produktu. To pole jest dostępne tylko po wybraniu opcji **Dopisanie** w polu **Wybierz produkt**.| Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Rola | Szybkie tworzenie | Rola osoby, która wykona tę pracę lub poniesie ten wydatek. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Kategoria | Szybkie tworzenie | Kategoria pracy lub wydatku. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Data rozpoczęcia | Szybkie tworzenie | Data rozpoczęcia pracy. | W tym polu domyślnie wyświetlane są szczegóły wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Data zakończenia | Szybkie tworzenie | Data zakończenia pracy. | W tym polu domyślnie wyświetlane są szczegóły wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Firma zasobów | Szybkie tworzenie | Firma pozyskująca lub podmiot prawny, który ponosi te koszty i zapewnia zasoby do pracy nad tym. | Wartością domyślną są powiązane szczegóły wiersza oferty dla kosztu, który jest tworzony automatycznie i jest używany do pobierania ceny kosztu. |
| Jednostka zasobów | Szybkie tworzenie | Jednostka zaopatrzeniowa, która ponosi ten koszt i zapewnia zasoby do pracy. | Wartością domyślną są powiązane szczegóły wiersza oferty dla kosztu, który jest tworzony automatycznie i jest używany do pobierania ceny kosztu. |
| Harmonogram jednostek | Szybkie tworzenie | Grupa jednostek pracy, produktu lub wydatku. Jednostki należą do harmonogramu jednostek lub grupy jednostek. Na przykład mile i kilometry to jednostki należące do grupy jednostek opisujących odległość. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Jednostka | Szybkie tworzenie | Jednostka pracy, produkt lub wydatek. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Ilość | Szybkie tworzenie | Ilość pracy, produkt lub wydatek. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Cena jednostkowa | Szybkie tworzenie |Stawka fakturowa roli, która wykonuje pracę, cena jednostkowa produktu lub cena sprzedaży produktu lub kategorii wydatków. To pole ma wartość domyślną **Czas** na podstawie kombinacji wartości wymiarów wyceny w wierszu ceny roli cennika projektu, który obowiązuje od daty rozpoczęcia. W przypadku **Kosztów** wartość jest domyślna określana na podstawie konfiguracji ceny w danej kategorii transakcji w cenniku projektu, która obowiązuje w stosunku do daty rozpoczęcia. Jeśli w kategorii transakcji wybrana jest inna metoda kalkulacji cen niż cena jednostkowa, nie zostanie zastosowana wartość domyślna, a to pole pozostanie puste. Wartość domyślna tego pola jest oparta na pozycji cennika w **Cenniku projektu**, która obowiązuje w dniu rozpoczęcia.| Stawka kosztów roli wykonującej pracę lub koszt jednostkowy kategorii wydatków lub koszt jednostkowy produktu. Wartość domyślna **Czas** jest w oparciu o kombinację wartości wymiarów wyceny w wierszu ceny roli w cenniku własnym dołączonym do jednostki zamawiającej obowiązującej od daty rozpoczęcia. W przypadku wydatków wartość domyślna jest oparta na wierszu ceny kategorii w cenniku własnym dołączonym do jednostki zawierającej umowę, która obowiązuje od daty rozpoczęcia. Jeśli metoda wyceny dla kategorii transakcji nie jest ceną za jednostkę, nie ma wartości domyślnej i to pole jest puste. Wartość domyślna tego pola jest oparta na **Pozycji cennika**  w Cenniku projektu dołączonego do jednostki zamawiającej, która obowiązuje od daty rozpoczęcia.|
| Szacowany podatek | Szybkie tworzenie | Można ręcznie wprowadzić szacowaną kwotę podatku dla tej pracy lub kosztu. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Kwota | Szybkie tworzenie | Informacje zawarte w tym polu można wprowadzić ręcznie, jeśli pola **Ilość** oraz **Cena** pozostaną niewypełnione. Jeśli te pola nie są puste, to pole staje się dostępne tylko do odczytu i będzie obliczane jako (ilość \* cena jednostkowa) + podatek. | W tym polu nie ma wpływu zmian na dalsze etapy. |

## <a name="update-prices-on-quote-line-details"></a>Aktualizowanie cen w wierszach oferty

W przypadku zmodyfikowania cen z cennika projektu dołączonego do oferty lub na liście kosztów własnych jednostki kontraktującej można wybrać opcję **Ponowne obliczenie** znajdującą się na stronie **Oferta**, aby odświeżyć ceny w poszczególnych wierszach oferty w celu odzwierciedlenia tej zmiany. Po wybraniu opcji **Ponowne obliczanie** zostanie wyświetlone ostrzeżenie informujące, że ceny w szczegółach wiersza oferty zostaną zresetowane we wszystkich wierszach oferty. Wybierz opcję **Tak**, aby odświeżyć ceny zarówno dla sprzedaży, jak i dla szczegółów wiersza oferty kosztów.

## <a name="access-quote-line-details-for-cost"></a>Dostęp do wierszy oferty w celu uzyskania dostępu do kosztów

Aby uzyskać dostęp do szczegółów linii wyceny dla kosztów, wykonaj następujące kroki:

1. Na karcie **Szczegóły wiersza oferty** zaznacz wiersz w siatce, aby włączyć akcje na pasku narzędzi podsiatki. 
2. Wybierz opcję **Wyświetl szczegóły kosztów**, aby wyświetlić powiązaną stawkę kosztów i kwotę dla danego wiersza oferty.

> [!NOTE]
> Zmiana jednostki zasobów, ilości, dat, roli lub kategorii w wierszu szczegółów oferty dotyczących kosztu spowoduje zmianę odpowiednich wartości w szczegółach wiersza oferty dotyczącej sprzedaży.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Waluta w wierszu szczegółów oferty dotyczących kosztów i sprzedaży

Waluta w szczegółach wiersza oferty dla sprzedaży jest ustawieniem domyślnym z cennika projektu, który obowiązuje od daty rozpoczęcia szczegółów wiersza oferty.

Waluta w szczegółach wiersza oferty dla kosztów domyślnych z cennika jednostki umownej oferty, która obowiązuje od daty rozpoczęcia szczegółów wiersza oferty dla kosztu.

> [!NOTE]
> Obliczenia rentowności konwertują kwotę w wierszu oferty szczegółów dotyczących kosztów i sprzedaży na walutę podstawową środowiska, aby raportować ogólną obliczoną marżę oferty. Błędy zaokrąglania walut i zmienione marginesy mogą nastąpić z powodu braku aktualnych kursów wymiany. Używaj tych obliczeń tylko w przypadku ofert projektowych, ponieważ są to przybliżone dane i nie są to rzeczywiste sprawozdania ustawowe lub inne, które wymagają większej precyzji zaokrąglania i świadomości skuteczności dat dla kursów wymiany.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
