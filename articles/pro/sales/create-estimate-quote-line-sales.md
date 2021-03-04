---
title: Szacowanie wiersza oferty opartej na projekcie
description: W tym temacie zamieszczono informacje dotyczące sposobu tworzenia oszacowania dla wiersza oferty opartej na projekcie.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 56892a134c0c739958f7f939214930631dea7420
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180385"
---
# <a name="estimating-a-project-based-quote-line"></a>Szacowanie wiersza oferty opartej na projekcie

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Wiersz oferty opartej na projekcie zawiera szczegółowe informacje pomocne przy szacowaniu kosztów i potencjalnego przychodu związanych z pracą mającą na celu dostarczenie danego wiersza oferty.

Aby oszacować wiersz oferty opartej na projekcie, w wierszu oferty opartej na projekcie wybierz kartę **Szczegóły wiersza oferty**. Istnieją dwa sposoby utworzenia oszacowania wiersza oferty opartej na projekcie:

- Ręczne tworzenie oszacowania bezpośrednio w wierszu oferty przy użyciu szczegółów wiersza oferty 
- Utworzenie projektu i planu projektu, a następnie skojarzenie projektu i zadań w projekcie z wierszem oferty. Proces importowania oszacowań z planu projektu na wiersz oferty na podstawie podanych informacji zostanie włączony.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Tworzenie szacowań bezpośrednio na wierszu oferty opartej na projekcie

Aby utworzyć oszacowanie w wierszu oferty opartej na projekcie, wybierz kartę **Szczegóły wiersza oferty**. Utworzony w ten sposób wiersz będzie sumować wartość cytowaną dla danego wiersza oferty. 

Aby utworzyć Szczegóły wiersza oferty, można wybrać nowe **+ Szczegóły wiersza oferty** z podsiatki **Szczegóły wierszy oferty**. Zostanie otwarty suwak szybkiego tworzenia. Poniższe pola w formularzu **Wiersza oferty**:

| **Pole** | **Lokalizacja** | **Opis** | **Wpływ zmian w dalszych etapach** |
| --- | --- | --- | --- |
| Opis | Szybkie tworzenie | Opis terminu konkretnego oszacowania. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Klasa transakcji | Szybkie tworzenie | Ta lista rozwijana zawiera klasy transakcji uwzględnione na karcie **Ogólne** w wierszu oferty opartej na projekcie.  | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Rola | Szybkie tworzenie | Osoba, która wykona pracę lub poniesie koszty. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Kategoria | Szybkie tworzenie | Kategoria pracy lub wydatków. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Data rozpoczęcia | Szybkie tworzenie | Data rozpoczęcia pracy. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Data zakończenia | Szybkie tworzenie | Data zakończenia pracy. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Jednostka zasobów | Szybkie tworzenie | Jednostka zasobów, która poniesie dany koszt i dostarczy zasób do pracy. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. To pole jest również używane podczas pobierania kosztu własnego. |
| Harmonogram jednostek | Szybkie tworzenie | Grupa jednostek pracy lub kosztów. Jednostki należą do harmonogramu jednostek lub grupy jednostek. Na przykład mile i kilometry to jednostki należące do grupy jednostek, które opisują odległość. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Jednostka | Szybkie tworzenie | Jednostka pracy lub kosztów. | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Ilość | Szybkie tworzenie | Ilość pracy lub kosztów | W tym polu jest domyślnie wybierana wartość Szczegółowego wiersza oferty dla automatycznie tworzonego kosztu. |
| Cena jednostkowa | Szybkie tworzenie | Stawka rozliczania dla roli wykonującej pracę lub cena sprzedaży w danej kategorii kosztów. To pole jest domyślnie ustawione na czas na podstawie kombinacji roli i jednostki zasobów znajdującej się na cenniku projektu, która obowiązuje w stosunku do daty rozpoczęcia. W przypadku kosztów, to pole zawiera domyślnie wartość ustawień ceny dla kategorii transakcji w cenniku projektowym, która obowiązuje w momencie daty rozpoczęcia. Jeśli w kategorii transakcji wybrana jest inna metoda kalkulacji cen niż cena jednostkowa, nie zostanie zastosowana wartość domyślna, a to pole pozostanie puste. | Stawka kosztów dla roli wykonującej pracę lub cena jednostkowa w danej kategorii kosztów. To pole jest domyślnie ustawione na czas na podstawie kombinacji roli i jednostki zasobów znajdującej się w cenniku jednostki kontaktującej ofertę , która obowiązuje w stosunku do daty rozpoczęcia. W przypadku kosztów, to pole zawiera domyślnie wartość ustawień ceny dla kategorii transakcji w cenniku kosztów jednostki kontraktującej, która obowiązuje w momencie daty rozpoczęcia. Jeśli w kategorii transakcji wybrana jest inna metoda kalkulacji cen niż cena jednostkowa, nie zostanie zastosowana wartość domyślna, a to pole pozostanie puste. |
| Szacowany podatek | Szybkie tworzenie | Można ręcznie wprowadzić szacowaną kwotę podatku dla tej pracy lub kosztu. | W tym polu nie ma wpływu zmian na dalsze etapy. |
| Kwota | Szybkie tworzenie | Informacje zawarte w tym polu można wprowadzić ręcznie, jeśli pola **Ilość** oraz **Cena** pozostaną niewypełnione. Jeśli te pola nie są puste, to pole staje się dostępne tylko do odczytu i będzie obliczane jako (ilość \* cena jednostkowa) + podatek. | W tym polu nie ma wpływu zmian na dalsze etapy. |

## <a name="update-prices-on-quote-line-details"></a>Aktualizowanie cen w wierszach oferty

W przypadku zmodyfikowania cen z cennika projektu dołączonego do oferty lub na liście kosztów własnych jednostki kontraktującej można wybrać opcję **Ponowne obliczenie** znajdującą się na stronie **Oferta**, aby odświeżyć ceny w poszczególnych wierszach oferty w celu odzwierciedlenia tej zmiany. Po wybraniu opcji **Oblicz ponownie** zostanie wyświetlone ostrzeżenie, które informuje tym, że ceny w wierszach oferty zostaną zresetowane. Wybierz opcję **Tak**, aby odświeżyć ceny zarówno dla sprzedaży, jak i dla szczegółów wiersza oferty kosztów.

## <a name="access-quote-line-details-for-cost"></a>Dostęp do wierszy oferty w celu uzyskania dostępu do kosztów

Z poziomu karty **Szczegóły wiersza oferty** wybierz wiersz w siatce, aby włączyć niektóre akcje na pasku narzędzi w podsiatce. Pierwsza akcja na pasku narzędzi w podsiatce po wybraniu szczegółów wiersza oferty powoduje **Otwórz szczegóły kosztu**. Wybierz opcję **Wyświetl szczegóły kosztów**, aby wyświetlić powiązaną stawkę kosztów i kwotę dla danego wiersza oferty.

> [!NOTE]
> Zmiana jednostki zasobów, ilości, dat, roli lub kategorii w wierszu szczegółów oferty dotyczących kosztu spowoduje zmianę odpowiednich wartości w szczegółach wiersza oferty dotyczącej sprzedaży.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Waluta w wierszu szczegółów oferty dotyczących kosztów i sprzedaży

Waluta w wierszu szczegółów oferty dotyczącym sprzedaży zmienia się z wartości znajdującej się w cenniku projektowym, która może zostać zastosowana od daty rozpoczęcia wiersza szczegółów oferty.

Waluta w wierszu szczegółów oferty dotyczącym kosztu zmienia się z wartości znajdującej się w cenniku jednostki kontraktującej ofertę, która może zostać zastosowana od daty rozpoczęcia wiersza szczegółów oferty dla kosztu.

Obliczenia rentowności konwertują kwotę w wierszu oferty szczegółów dotyczących kosztów i sprzedaży na walutę podstawową środowiska, aby raportować ogólną obliczoną marżę oferty.

Może to doprowadzić do błędów procesów zaokrąglania waluty i zmiany marży z powodu braku aktualnych kursów wymiany. Te obliczenia w ofertach projektów winny być używane tylko jako przybliżenia, gdyż nie są rzeczywistymi, ustawowymi lub innymi typami sprawozdawczości, które wymagają wyższego poziomu dokładności zaokrąglania i świadomości terminu ważności kursów wymiany.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]