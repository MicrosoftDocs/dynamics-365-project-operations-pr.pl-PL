---
title: Migrowanie w pełni zafakturowanych punktów kontrolnych rozliczania przy najechańczym
description: W tym artykule wyjaśniono sposób migrowania punktów kontrolnych rozliczania o stałej cenie, które zostały zafakturowane dla klienta w celu otwarcia kontraktów projektów przed datą rozpoczęcia.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028715"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrowanie w pełni zafakturowanych punktów kontrolnych rozliczania przy najechańczym

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

## <a name="scenario"></a>Scenariusz

Firma Contoso będzie hostowana w Microsoft Dynamics 365 Project Operations w przypadku scenariuszy niezabędowych. W ramach działań pochyłych zespół implementacji musi migrować otwarte kontrakty projektów ze starego systemu. Niektóre kontrakty projektów zawierają takie wiersze kontraktu, które korzystają z metody rozliczania o stałej cenie i zostały już zafakturowane częściowo klientowi końcoweowi. Zespół implementacji musi migrować te punkty kontrolnych rozliczania jako **fakturę klienta**, ponieważ muszą one zostać uwzględnione w łącznej wartości kontraktu dla celów uznawania przychodów. Nie ma to jednak wpływu na salda klientów w należnościach i na kontach ogólnych.

## <a name="solution"></a>Rozwiązanie

### <a name="prerequisites"></a>Wymagania wstępne

- Program Dynamics 365 Finance 10.0.24 lub nowszy musi zostać zainstalowany.
- Środowisko, w którym zostaną ukończone kroki migracji, musi być w trybie konserwacji. Podczas migracji punktów kontrolnych nie należy wykonywać innych działań.
- Kroki migracji należy wykonać dokładnie tak, jak to opisano w tym miejscu i mogą być używane tylko do działania przysłania. Firma Microsoft nie obsługuje innych możliwości tej funkcji.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Tworzenie nowej wersji mapy w zakresie integracji Project Operations z linią punktów kontrolnych kontraktu 

1. Upewnij się, że mapowanie celu dla encji **punktów kontrolnych wiersza umowy integracji Project Operations** jest aktualne. 

    1. W Finance przejdź do **Zarządzanie danymi** \> **encje danych** i wybierz encję **punkty kontrolne wiersza umowy integracji Project Operations**. 
    2. Wybierz **opcję Modyfikuj mapowania docelowe**. 
    3. Na stronie **mapowania przemieszczania do** celu wybierz **opcję Generowanie mapowania**, a następnie potwierdź, że chcesz wygenerować mapowanie.

2. Zatrzymaj i odśwież mapę podwójnego zapisu **punktów kontrolnych wiersza kontraktu dotyczącego integracji Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Przejdź do strony **Zarządzanie danymi** \> **Podwójny zapis**, wybierz mapowanie i otwórz jego szczegóły. 
    2. Wybierz **opcję Zatrzymaj** i poczekaj, aż system zatrzyma mapę. 
    3. Wybierz **Odśwież tabele**.

3. Dodaj mapowanie stanu transakcji.

    1. Wybierz **Dodaj mapowanie**.
    2. W nowym wierszu w kolumnie **Aplikacje finansowe i operacyjne** wybierz pole **TRANSSTATUS \[TRANSSTATUS\]**.
    3. W kolumnie **Microsoft Dataverse** wybierz stan **msdyn\_invoicestatus \[Invoice status\]**.
    4. W kolumnie **Typ mapowania** wybierz strzałkę w prawo (**\>**).
    5. W oknie dialogowym wyświetlanym w polu Kierunek **synchronizacji** wybierz opcję **Dataverse na aplikacje finansowe i operacyjne**.
    6. Wybierz pozycję **Dodaj przekształcenie**.
    7. W polu **Typ przekształcenia** wybierz **ValueMap**.
    8. Wybierz **Dodaj mapowanie wartości**.
    9. W lewym polu wpisz **4**. W prawym polu wpisz **192350001**. 
    10. Wybierz pozycję **Zapisz**, a następnie zamknij okna dialogowe.

4. Wybierz **opcję Zapisz jako**, aby zapisać wersję mapy dwueszczętowej. 
5. W okienku **Dodaj tabelę** w polu **Wydawca** wybierz opcję **Wydawca domyślny**.
6. W polu **Wersja** wprowadź wersję.
7. W polu **Opis** wprowadź notatkę na temat tej wersji mapy pochyłej. 
8. Wybierz pozycję **Zapisz**.
9. Uruchom mapę.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrowanie zafakturowanych punktów kontrolnych do środowiska Dataverse

1. W środowisku Project Operations Dataverse utwórz punkty kontrolne, których **stan faktury to Gotowy do fakturowania**. Do tego momentu nie migruj punktów kontrolnych, które nie zostały zafakturowane.

    > [!NOTE]
    > Przed rozpoczęciem migracji punktów kontrolnych rozliczania należy się upewnić, że rozmiary finansowe powiązane z linią kontraktu projektu są ustawione zgodnie z oczekiwaniami. Po zakończeniu migracji nie można edytować rozmiarów finansowych.

2. Po migracji wszystkich punktów kontrolnych należy zatrzymać następujące mapowania w trybie podwójnego zapisu:

    - Punkty kontrolne pozycji kontraktu integracji rozwiązania Project Operations (msdyn\_contractlinescheduleofvalues)
    - Wartości rzeczywiste integracji Project Operations (msdyn\_actuals)
    - Propozycja faktury za projekt V2 (faktury)

    Aby zatrzymać mapy, wykonaj następujące czynności:

    1. W Finance przejdź do strony **Zarządzanie danymi** \> **Podwójny zapis**, wybierz mapowanie i otwórz jego szczegóły.
    2. Wybierz **opcję Zatrzymaj** i poczekaj, aż system zatrzyma mapę.

3. W środowisku Project Operations Dataverse można tworzyć i potwierdzać faktury pro-do punktów kontrolnych rozliczania. 

    1. Na mapie witryny przejdź do kontraktów projektów, wybierz kontrakty, a następnie wybierz opcję **Utwórz faktury**.
    2. Po utworzeniu faktur otwórz je w menu **Faktury** na mapie witryny, a następnie wybierz polecenie **Potwierdź**.

    Ten krok powoduje utworzenie wymaganych rekordów w środowisku Dataverse. Nie ma to jednak wpływu na finanse i należności, ponieważ wymienione wcześniej mapowania podwójnego zapisu zostały zatrzymane.

4. Po potwierdzenia wszystkich fakturach zadymanych powróć wszystkie mapowania dwurdzeniowe do ich stanu początkowego.

    1. Zaktualizuj wersję mapy podwójnego zapisu **punktów kontrolnych wiersza kontraktu dotyczącego integracji Project Operations** (**msdyn\_contractlinescheduleofvalues**). 
    2. Wybierz z listy mapowanie dwue write, wybierz **wersję mapowania tabeli**, a następnie wybierz oryginalną wersję mapowania tabeli.
    3. Wybierz pozycję **Zapisz**.
    4. Uruchom ponownie następujące mapowania dwuetapowe:

        - Punkty kontrolne pozycji kontraktu integracji rozwiązania Project Operations (msdyn\_contractlinescheduleofvalues)
        - Wartości rzeczywiste integracji Project Operations (msdyn\_actuals)
        - Propozycja faktury za projekt V2 (faktury)

Punkty kontrolne zostały zmigrowane i system jest gotowy do następnych kroków w przypadku migracji.
