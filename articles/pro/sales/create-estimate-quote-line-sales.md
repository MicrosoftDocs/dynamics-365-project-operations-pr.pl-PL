---
title: Szacowanie wiersza oferty projektu
description: W tym artykule przedstawiono informacje na temat sposobu tworzenia szacowanej wartości wiersza oferty dotyczącej projektu.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bac3a3fa2d14c857edfb469a005406c346c8dbf6
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826001"
---
# <a name="estimate-a-project-quote-line"></a>Szacowanie wiersza oferty projektu

_**Ma zastosowanie do:** Wdrożenie uproszczone - zajmuje się fakturowaniem proforma, Project Operations dla scenariuszy opartych na zasobach / braku zapasów_

Wiersz oferty opartej na projekcie zawiera szczegółowe informacje pomocne przy szacowaniu kosztów i potencjalnego przychodu związanych z pracą mającą na celu dostarczenie danego wiersza oferty.

Aby oszacować wiersz oferty opartej na projekcie, w wierszu oferty opartej na projekcie wybierz kartę **Szczegóły wiersza oferty**. Istnieją dwa sposoby utworzenia oszacowania wiersza oferty opartej na projekcie:

- Ręczne tworzenie oszacowania bezpośrednio w wierszu oferty przy użyciu szczegółów wiersza oferty. 
- Utworzenie projektu i planu projektu, a następnie skojarzenie projektu i zadań w projekcie z wierszem oferty. Proces importowania oszacowań z planu projektu na wiersz oferty na podstawie podanych informacji zostanie włączony.

## <a name="create-estimates-directly-on-a-project-quote-line"></a>Tworzenie szacowań bezpośrednio na wierszu oferty projektu

Aby utworzyć oszacowanie w wierszu oferty opartej na projekcie, wybierz kartę **Szczegóły wiersza oferty**. Utworzony w ten sposób wiersz będzie sumować wartość cytowaną dla danego wiersza oferty. 

Aby utworzyć Szczegóły wiersza oferty, można wybrać nowe **Szczegóły wiersza oferty** z podsiatki **Szczegóły wierszy oferty**. Zostanie otwarty suwak szybkiego tworzenia. W poniższej tabeli przedstawiono szczegółowe informacje o polach na stronie **Szczegóły wiersza oferty** oraz sposób, w jaki wartości mają wpływ na funkcjonalność.

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
| Jednostka zasobów | Szybkie tworzenie | Jednostka zaopatrzeniowa, która poniesie ten koszt i zapewni zasoby do pracy nad nią. | Wartością domyślną są powiązane szczegóły wiersza oferty dla kosztu, który jest tworzony automatycznie i jest używany do pobierania ceny kosztu. |
| Harmonogram jednostek | Szybkie tworzenie | Grupa jednostek pracy, produktu lub wydatku. Jednostki należą do harmonogramu jednostek lub grupy jednostek. Na przykład mile i kilometry to jednostki należące do grupy jednostek opisujących odległość. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Jednostka | Szybkie tworzenie | Jednostka pracy, produkt lub wydatek. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Ilość | Szybkie tworzenie | Ilość pracy, produkt lub wydatek. | Ta wartość jest wartością domyślną dla powiązanych szczegółów wiersza oferty dla kosztów, które są tworzone automatycznie. |
| Cena jednostkowa | Szybkie tworzenie |Stawka fakturowa roli, która wykonuje pracę, cena jednostkowa produktu lub cena sprzedaży produktu lub kategorii wydatków. To pole ma wartość domyślną **Czas** na podstawie kombinacji wartości wymiarów wyceny w wierszu ceny roli cennika projektu, który obowiązuje od daty rozpoczęcia. W przypadku **Kosztów** wartość jest domyślna określana na podstawie konfiguracji ceny w danej kategorii transakcji w cenniku projektu, która obowiązuje w stosunku do daty rozpoczęcia. Jeśli metoda wyceny dla kategorii transakcji nie jest ceną za jednostkę, nie ma wartości domyślnej i to pole jest puste. Wartość domyślna jest oparta na pozycji cennika w **Cenniku projektu**, która obowiązuje w dniu rozpoczęcia.| Stawka kosztów roli wykonującej pracę lub koszt jednostkowy kategorii wydatków lub koszt jednostkowy produktu. To pole ma wartość domyślną **Czas** na podstawie kombinacji wartości wymiarów wyceny w wierszu ceny roli cennika projektu, który obowiązuje od daty rozpoczęcia. W przypadku **Kosztów** wartość jest domyślna określana na podstawie konfiguracji ceny w danej kategorii transakcji w cenniku projektu, która obowiązuje w stosunku do daty rozpoczęcia. Jeśli metoda wyceny dla kategorii transakcji nie jest ceną za jednostkę, nie ma wartości domyślnej i to pole jest puste. Wartość domyślna jest oparta na pozycji cennika w **Cenniku projektu**, która obowiązuje w dniu rozpoczęcia.|
| Szacowany podatek | Szybkie tworzenie | Można ręcznie wprowadzić szacowaną kwotę podatku dla tej pracy lub kosztu. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Kwota | Szybkie tworzenie | Informacje zawarte w tym polu można wprowadzić ręcznie, jeśli pola **Ilość** oraz **Cena** pozostaną niewypełnione. Jeśli te pola nie są puste, to pole staje się dostępne tylko do odczytu i będzie obliczane jako (ilość \* cena jednostkowa) + podatek. | W tym polu nie ma wpływu zmian na dalsze etapy. |


## <a name="update-prices-on-quote-line-details"></a>Aktualizowanie cen w wierszach oferty

Jeśli zmieniłeś ceny w cenniku projektu dołączonym do oferty lub w cenniku kosztów jednostki zamawiającej, możesz wybrać opcję **Oblicz ponownie** na stronie **Oferta**, aby odświeżyć ceny w poszczególnych wierszach oferty, aby odzwierciedlić tę zmianę. Po wybraniu opcji **Ponowne obliczanie** zostanie wyświetlone ostrzeżenie informujące, że ceny w szczegółach wiersza oferty zostaną zresetowane we wszystkich wierszach oferty. Wybierz opcję **Tak**, aby odświeżyć ceny zarówno dla sprzedaży, jak i dla szczegółów wiersza oferty kosztów.

## <a name="access-quote-line-details-for-cost"></a>Dostęp do wierszy oferty w celu uzyskania dostępu do kosztów

Z poziomu karty **Szczegóły wiersza oferty** wybierz wiersz w siatce, aby włączyć niektóre akcje na pasku narzędzi w podsiatce. Pierwsza akcja na pasku narzędzi w podsiatce po wybraniu szczegółów wiersza oferty powoduje **Otwórz szczegóły kosztu**. Wybierz opcję **Wyświetl szczegóły kosztów**, aby wyświetlić powiązaną stawkę kosztów i kwotę dla danego wiersza oferty.

> [!NOTE]
> Zmiana jednostki zasobów, ilości, dat, roli lub kategorii w wierszu szczegółów oferty dotyczących kosztu spowoduje zmianę odpowiednich wartości w szczegółach wiersza oferty dotyczącej sprzedaży.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Waluta w wierszu szczegółów oferty dotyczących kosztów i sprzedaży

Waluta w wierszu szczegółów oferty dotyczącym sprzedaży zmienia się z wartości znajdującej się w cenniku projektowym, która może zostać zastosowana od daty rozpoczęcia wiersza szczegółów oferty.

Waluta w wierszu szczegółów oferty dotyczącym kosztu zmienia się z wartości znajdującej się w cenniku jednostki kontraktującej ofertę, która może zostać zastosowana od daty rozpoczęcia wiersza szczegółów oferty dla kosztu.

Obliczenia rentowności konwertują kwotę w wierszu oferty szczegółów dotyczących kosztów i sprzedaży na walutę podstawową środowiska, aby raportować ogólną obliczoną marżę oferty.

> [!UWAGA Błędy zaokrąglania walut i zmienione marginesy mogą nastąpić z powodu braku aktualnych kursów wymiany. Obliczenia te należy stosować tylko w przypadku umów dotyczących projektów, ponieważ są one przybliżone i nie służą do rzeczywistych sprawozdań ustawowych lub innych, które wymagają większej precyzji zaokrąglania i świadomości skuteczności dat dla kursów wymiany.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
