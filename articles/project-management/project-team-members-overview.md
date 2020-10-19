---
title: Członkowie zespołu projektu
description: W tym temacie zamieszczono informacje dotyczące pracy z informacjami dotyczącymi członków zespołu projektu, ich atrybutami i planowaniem.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908449"
---
# <a name="project-team-members"></a>Członkowie zespołu projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Członkiem zespołu projektu są uczestnicy projektu, którzy pracują nad zakończeniem projektu. Celem siatki członków zespołu jest prezentacja listy nazwanych zasobów pracujących nad zadaniem oraz ogólnych członków zespołu, którzy są na razie elementem zastępczym, a dopiero później staną się członkami zespołu.

W siatce członków zespołu menedżer projektu i inni uczestnicy projektu mogą sprawdzić, kto został przypisany do projektu. Użytkownicy mogą również wyświetlać podsumowanie swoich rezerwacji, planowanego wysiłku oraz przydziałów poszczególnych zasobów. Siatka członków zespołu umożliwia menedżerom projektu zdefiniowanie wymagań dotyczących zasobów dla ogólnych członków zespołu oraz zarządzanie rezerwacjami istniejących członków zespołu.

W poniższej tabeli przedstawiono kluczowe atrybuty dla członka zespołu projektu.

| Nazwa pola          | Opis                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metoda alokacji        | Metoda alokacji używana do księgowania zasobów w projekcie.                                                                         |
| Typ rozliczeń             | Określ, czy członek zespołu jest zaklasyfikowany jako możliwy do rozliczenia.                                                                                                                                       |
| Zasób, który można zarezerwować        | Zasób, który można zarezerwować, wybrany w celu zastąpienia zasobu ogólnego.                                                                                                                   |
| Stan usuwania            | Stan usunięcia członka zespołu w celu śledzenia, jeśli zostało wysłane żądanie usunięcia do PSS i czy PSS pomyślnie wyśle odpowiedź z powrotem i w oczekiwanym oknie czasu. |
| Łączny nakład pracy (godziny)     | Suma nakładów pracy członka zespołu w przypisanych mu zadaniach.                                                                                                                         |
| Wykonany nakład pracy (godziny) | Śledzenie zakończonego nakładu pracy członka zespołu w przypisanych mu zadaniach.                                                                                           |
| Pozostały nakład pracy (godziny) | Śledzenie niezakończonego nakładu pracy członka zespołu w przypisanych mu zadaniach.                                                                                    |
| Zakończenie                   | Data zakończenia przynależności do zespołu zasobów.                                                                                                                                            |
| Ostatecznie zarezerwowane godziny        | Ostateczna liczba godzin zarezerwowana dla członka zespołu.                                                                                                                                                                |
| Nazwa stanowiska            | Nazwa używana do identyfikowania zasobu ogólnego.                                                                                                                                   |
| Jednostka zasobów          | Jednostka organizacyjna zasobu wykonującego pracę.                                                                                                                      |
| Osoba zatwierdzająca projekt         | Określ, czy członek zespołu może zatwierdzać czas i wydatki.                                                                                                                     |
| Wymagane godziny           | Wymagane godziny członka zespołu z wymagania członka zespołu.                                                                                                                       |
| Rola                     | Rola, jaką członek zespołu będzie pełnił w danym zespole.                                                                                                                                |
| Opis stanowiska     | Wprowadź opis roli tego członka zespołu.                                                                                                                             |
| Wstępnie zarezerwowane godziny        | Wstępna liczba godzin zarezerwowana dla członka zespołu.                                                                                                                                                                 |
| Rozpoczęcie                    | Data rozpoczęcia przynależności do zespołu zasobów.                                                                                                                                          |

Z poziomu siatki członków zespołu można wykonać następujące czynności:

- **Rezerwacja**: dla organizacji, które korzystają z hybrydowej metody rezerwacji, akcja rezerwacji pozwoli użytkownikom na zaksięgowanie nazwanego zasobu na podstawie wymagań wygenerowanych przez ogólnego członka zespołu
- **Generowanie wymagania**: Ta akcja powoduje wygenerowanie wymagania.
- **Określ wzorzec**: zezwala menedżerom projektu na dostosowywanie przypisań wymagań zasobów na poziomie szczegółowym. Menedżerowie projektów mogą korygować konkretne potrzeby projektu w sytuacjach, w których przydział domyślny nie pasuje.
- **Wyślij prośbę**: dla organizacji korzystających z centralnej metody rezerwowania.
- **Edycja**: atrybuty członków zespołu mogą być edytowane wraz z jednostką organizacyjną, rolą i nazwą pozycji.
- **Utrzymywanie rezerwacji**: Kiedy rezerwacje zasobów muszą zostać zaktualizowane, można zachować rezerwacje, dzięki czemu menedżer projektu może dostosować:

    - Rozpoczęcie
    - Zakończenie
    - Całkowite przydziały nakładów

- **Nowe**: oprócz dodawania zasobów bezpośrednio z poziomu harmonogramu menedżerowie projektów mogą dodawać nowych nazwanych lub ogólnych członków zespołu z siatki członków zespołu.
- **Usuń**: wybranie jednego lub wielu członków zespołu powoduje, że menedżer projektu może usunąć zasoby, które już nie biorą udziału w projekcie. Usunięcie członka zespołu spowoduje również usunięcie wszystkich skojarzonych przypisań zasobów i anulowanie wszystkich istniejących rezerwacji.
