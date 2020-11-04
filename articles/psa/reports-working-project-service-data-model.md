---
title: Praca z modelem danych rozwiązania Project Service Automation
description: W tym temacie zamieszczono informacje dotyczące pracy z modelem danych.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 19e999e16a5bf6321a5a61208c8654f7870e6007
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082197"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Praca z modelem danych rozwiązania Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation rozszerza inne encje aplikacji i wprowadza własne encje w modelu danych Common Data Service. W tym temacie opisano niektóre encje, które będą spotykane podczas typowych scenariuszy raportowania PSA.

## <a name="reporting-on-opportunities"></a>Raportowanie szans sprzedaży

Project Service Automation rozszerza encję Dynamics 365 Sales **Opportunity** , dodając pola umożliwiające scenariusze oparte na projektach. Te pola są identyfikowane na podstawie nazwy schematu poprzedzonej prefiksem **msdyn\_**. Jednym nowym polem ważnym przy raportowaniu szans sprzedaży PSA jest **Typ zamówienia**. Wartość **Na podstawie pracy** dla tego pola oznacza, że szansa sprzedaży jest szansą sprzedaży PSA. Inne pola, które zostały dodane do encji, to **organizacja kontraktująca** (zawiera organizację przechowującą szansę sprzedaży) oraz **Menedżer klienta** (zawiera nazwę menedżera klienta odpowiedzialnego za szansę sprzedaży).

Encja **Wiersz szansy sprzedaży** zawiera także pola dotyczące Project Service. **Metoda rozliczania** wskazuje, czy wiersz szansy sprzedaży ma być rozliczany według czasu i materiałów, czy ceny stałej, natomiast **Projekt** przechwytuje nazwę projektu, stojącego za szansą sprzedaży. Inne pola, które mogą podlegać raportom, dotyczą kwot kosztów pozyskania i budżetu klienta dla pozycji wiersza.

## <a name="reporting-on-quotes"></a>Raportowanie ofert

PSA rozszerza encję **Oferta sprzedaży** , dodając pola związane z projektem. **Typ zamówienia** odróżnia oferty PSA od ofert nie-PSA. Wartość **Na podstawie pracy** dla tego pola oznacza, że oferta jest ofertą PSA. Inne pola, które mogą mieć znaczenie przy raportowaniu ofert PSA obejmują pola kwoty, takie jak **Koszty odpłatne** , **koszty nieodpłatne** , **Marża brutto** , **Szacowania** i **Budżet**. Inne przydatne pola pokazują, czy oferta jest opłacalna, czy zostanie zrealizowana w terminie oraz czy spełnia oczekiwaniami budżetowe klienta.

PSA rozszerza również encję **Wiersz oferty sprzedaży**. Jednym z pól, które dodaje PSA, jest **Metoda rozliczeniowa**. Wskazuje ono, jak wiersz oferty będzie rozliczany (czas i materiały czy stała cena). Inne pola, które zostały dodane do encji, przechwytują pokrewny projekt będący podstawą wiersza oferty, fakturowania, kosztu i budżetu.

PSA dodaje również nowe encje powiązane z ofertą do modelu danych Dynamics 365. Oto kilka przykładów:

- **Szczegóły wiersza oferty** – ta encja zawiera szczegóły szacowania projektu dla wiersza oferty. Ma dwa rekordy dla każdego wiersza oferty. Jeden rekordów zawiera koszt i szczegóły kosztu wiersza oferty, a drugi rekord zawiera informacje o kwocie sprzedaży i szczegółach sprzedaży dla wiersza oferty.
- **Harmonogram fakturowania wierszy oferty** – ta encja zwiera harmonogram fakturowania dla wiersza oferty. Ten harmonogram jest generowany na podstawie częstotliwości fakturowania przypisanej do wiersza oferty.
- **Punkt kontrolny wiersza oferty** – ta encja zawiera punkty kontrolne fakturowania dla wierszy oferty o stałej cenie.
- **Podział analizy wierszy oferty** – ta encja zawiera szczegóły finansowe dla wiersza oferty. Te szczegóły mogą być używane do raportowania kwot sprzedaż ofertowej i szacowanego kosztu według różnych wymiarów.

Inne encje, które PSA dodaje do ofert to **Cennik projektu wiersza oferty** , **Kategoria zasobów wiersza oferty** oraz **Kategoria transakcji wiersza oferty**.

![Diagram przedstawiający oferty, wiersz oferty i relacje projektu](media/PS-Reporting-image2.png "Diagram przedstawiający oferty, wiersz oferty i relacje projektu")

## <a name="reporting-on-project-contracts"></a>Raportowanie dotyczące kontraktów projektów

PSA rozszerza encję **Zamówienie** sprzedaży używaną podczas rejestrowania kontraktów projektów. Dodaj ważne nowe pole **Typ zamówienia** , które identyfikuje kontrakt jako kontrakt projektu PSA a nie zamówienie sprzedaży. Wartość **Na podstawie pracy** dla tego pola oznacza, że zamówienie jest kontraktem projektu PSA. Inne nowe pola dodane do encji **Zamówienie** zawierają szczegółowe informacje na temat kosztów, stanu kontraktu PSA oraz organizacji, która jest właścicielem kontraktu.

PSA rozszerza również encję **Wiersz zamówienia sprzedaży**. Wśród dodawanych pól znajdują się pola, w których jest śledzona metoda rozliczeniowa (czas i materiały lub cena ustalona), kwoty budżetu klienta praz projekt podstawowy.

PSA dodaje również nowe encje zaprojektowane z myślą o kontraktach projektów. Oto kilka przykładów:

- **Szczegóły pozycji kontraktu projektu** – ta encja zawiera szczegóły poziomu wiersza, które są zestawiane z kwotą wiersza kontraktu. Mogą one być tak szczegółowe, jak pozycje generowane na podstawie harmonogramu projektu na poziomie zadania.
- **Harmonogram fakturowania pozycji kontraktu** – ta encja zawiera harmonogram rozliczeniowy generowany na podstawie częstotliwości fakturowania przypisanej do wiersza kontraktu.
- **Punkt kontrolny kontraktu** – ta encja zawiera punkty kontrolne pozycji kontraktu, które są rozliczane na podstawie ustalonej ceny.

Inne encje, które PSA dodaje do kontraktu to **Cennik projektu pozycji kontraktu projektu** , **Kategoria zasobów pozycji kontraktu projektu** oraz **Kategoria transakcji pozycji kontraktu projektu**.

![Diagram przedstawiający zamówienie, wiersz zamówienia i relacje projektu](media/PS-Reporting-image3.png "Diagram przedstawiający zamówienie, wiersz zamówienia i relacje projektu")

## <a name="reporting-on-projects"></a>Raportowanie dotyczące projektów

Encja **Projekty** i encje z nią związane mogą występować tylko w PSA. Encja **Projekt** jest encją najwyższego poziomu używaną do przechwytywania pracy i kosztu operacji. Oto lista pokrewnych encji:

- **Członek zespołu projektu** – ta encja zawiera szczegóły dotyczące zasobów, które można zarezerwować, które są przypisane do projektu. Te zasoby mogą być ogólnymi zasobami, które można zarezerwować, lub mogą być nazwanymi zasobami, które można zarezerwować, które są wprowadzane przez menedżera projektu lub generowane z poziomu harmonogramu projektu.
- **Zadanie projektu** – ta encja zawiera zadania wchodzące w skład planu lub harmonogramu projektu.
- **Przypisanie zasobu** – ta encja zawiera przydział zadania dla zasobu, który można zarezerwować.
- **Wymaganie zasobów** – ta encja zawiera wymagania dla dowolnych wszystkich członków zespołu zasobów ogólnych.
- **Szacowanie** i **Wiersz szacowania** – te encje mają relację nagłówek/wiersz i zawierają oszacowania wydatków dla projektu. Szacowania zadań są przechowywane w encji **Szacowanie zasobu**.

![Diagram przedstawiający wymagania zasobu, wiersz zamówienia i relacje projektu](media/PS-Reporting-image4.png "Diagram przedstawiający wymagania zasobu, wiersz zamówienia i relacje projektu")

## <a name="reporting-on-resources"></a>Raportowanie zasobów

Zasoby projektu używają encji **Zasób, który można zarezerwować** z Universal Resource Scheduling (URS), które są użytkowane wspólnie z innymi aplikacjami, takimi jak Microsoft Dynamics 365 Field Service. Oto lista encji, których możesz musieć użyć podczas raportowania zasobów projektu:

- **Zasób, który można zaksięgować** – ta encja reprezentuje użytkownika, kontakt, zasób ogólny, konto, grupę lub sprzęt używany w zespole projektu.
- **Charakterystyki zasobów, które można zarezerwować** — ta encja zawiera umiejętności, certyfikaty lub wykształcenie zasobu. Charakterystyki mogą mieć wartości rankingu definiowane przez modelu oceny.
- **Kategoria zasobów, które można zarezerwować** – ta encja reprezentuje rolę zasobu, który można zarezerwować.
- **Rezerwacje zasobów, które można zarezerwować** – ta encja reprezentuje czas, który jest rezerwowany w projektach dla zasobu. Każda rezerwacja zawiera zarówno encję nagłówka, jak i encje wiersze, a każdy wiersz ma stan odpowiadający stanowi rezerwacji.

![Diagram przedstawiający możliwe do zaksięgowania relacje charakterystyk zasobów](media/PS-Reporting-image5.png "Diagram przedstawiający możliwe do zaksięgowania relacje charakterystyk zasobów")

## <a name="reporting-on-actual-transactions"></a>Raportowanie rzeczywistych transakcji

Po zatwierdzeniu grafiku lub wydatku albo zafakturowaniu kontraktu w PSA transakcja biznesowa jest rejestrowana w encji **Rzeczywiste**. Ta encja może służyć jako podstawa do niemal wszystkich raportów związanych z finansami w PSA. Encja **Rzeczywiste** zawiera koszty i transakcje sprzedaży dotyczące danego zdarzenia biznesowego. Zawiera również wiele przydatnych atrybutów.

Pracując z encją **Rzeczywiste** , ważne jest, aby rozumieć, jakie transakcje są zarejestrowane w encji i kiedy są one rejestrowane. Oto typowy przepływ pracy z wpisami czasu (przepływ encji wydatków jest podobny):

1. Po zapisaniu wpisu czasu w encji **Rzeczywiste** nie są tworzone żadne rekordy.
2. Po przesłaniu wpisu czasu w encji **Rzeczywiste** nie są tworzone żadne rekordy.
3. Po zatwierdzeniu wpisu czasu, tworzony jest jeden rekord w encji **Rzeczywiste** i może zostać utworzony również drugi rekord. Pierwszy rekord zawiera koszty wpisu czasu. Drugi rekord zawiera niezafakturowane kwoty sprzedaży wpisu czasu. Drugi rekord jest uzależniony od tego, czy projekt ma przypisanego klienta, ofertę lub pozycję kontraktu.

    | Data dokumentu | Typ transakcji | Klasa transakcji | Klient         | Contract   | Zasób     | Rola zasobu | Typ rozliczania | Ilość | Cena jednostkowa | Kwota |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Koszt             | Time              | Alpine ski house | Alpine CRM | Bogumiła Kowalczyk | Menedżer projektu   | Odpłatne   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Nierozliczona sprzedaż   | Time              | Alpine ski house | Alpine CRM | Bogumiła Kowalczyk | Menedżer projektu   | Odpłatne   | 8.0      | 100.00     | 800.00 |

    Te dwa rekordy są odrębne, ale są ze sobą powiązane. Nie są ani obciążeniami ani uznaniami.

4. Jeśli z projektem jest skojarzony kontrakt, po zafakturowaniu wpisu czasu, są tworzone dwa kolejne rekordy w encji **Rzeczywiste**. W pierwszej kolejności tworzona jest ujemna kwota dla niezafakturowanej sprzedaży. Ten rekord zasadniczo odwraca niezafakturowaną sprzedaż. Następnie tworzona jest transakcja dla zafakturowanej sprzedaży. I znów, rekordy te są odrębne ale pokrewne i nie są ani obciążeniami ani uznaniami.

    | Data dokumentu | Typ transakcji | Klasa transakcji | Klient         | Contract   | Zasób     | Rola zasobu | Typ rozliczania | Ilość | Cena jednostkowa | Kwota   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Nierozliczona sprzedaż   | Time              | Alpine ski house | Alpine CRM | Bogumiła Kowalczyk | Menedżer projektu   | Odpłatne   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Rozliczona sprzedaż     | Time              | Alpine ski house | Alpine CRM | Bogumiła Kowalczyk | Menedżer projektu   | Odpłatne   | 8.0      | 100.00     | 800.00   |

Encja **Początkowy rekord transakcji** rejestruje źródło rekordu **Rzeczywiste** , a encja **Połączenie transakcji** rejestruje pokrewne rekordy dla rekordu **Rzeczywiste**. Ponadto rekord **Rzeczywiste** zawiera odwołania do projektu, kontraktu projektu (zamówienia), zasobu, który można zarezerwować oraz klienta.

![Diagram przedstawiający połączenie transakcji, źródło i rzeczywistą relacje](media/PS-Reporting-image6.png "Diagram przedstawiający połączenie transakcji, źródło i rzeczywistą relacje")
