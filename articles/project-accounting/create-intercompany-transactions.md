---
title: Tworzenie transakcji międzyfirmowych
description: W tym temacie przedstawiono informacje dotyczące sposobu tworzenia transakcji międzyfirmowych.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 88e5658c9087fdb19adce1c23bc5cad0ad0fa434
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600003"
---
# <a name="create-intercompany-transactions"></a>Tworzenie transakcji międzyfirmowych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Transakcje międzyfirmowe są transakcjami dotyczącymi czasu i wydatków z kontraktu projektu należącego do jednej firmy lub jednostki organizacyjnej, a zasoby w kontrakcie projektu stanowią część innej firmy lub jednostki organizacyjnej.

Po zatwierdzeniu transakcji międzyfirmowej są tworzone następujące transakcje rzeczywiste

| **Typ transakcji** | **Zastosowany cennik** | **Waluta transakcji** |
| --- | --- | --- |
| Koszt | Lista kosztów własnych jednostki kontraktującej | Waluta w wierszu ceny |
| Nierozliczona sprzedaż. Te elementy są tworzone tylko dla wartości rzeczywistych skojarzonych z pozycją kontraktu z typem rozliczeń, czasem i materiałem. | Cennik sprzedaży projektu kontraktu | Waluta kontraktu |
| Koszt jednostkowy zasobów | Lista kosztów własnych jednostki zasobów | Waluta w wierszu ceny |
| Sprzedaż jednostek międzyorganizacyjnych | Lista kosztów własnych jednostki kontraktującej | Waluta w wierszu ceny |

Koszt, koszt jednostkowy zasobów oraz cena i waluta transakcji sprzedaży między jednostkami organizacyjnymi są określane przez **jednostkę organizacyjną**. Jest to ważna kwestia, o której należy pamiętać podczas decydowania o strukturze firm i jednostek organizacyjnych w implementacji.

Podczas tworzenia rekordów szansy sprzedaży, oferty, kontraktu projektu i projektu weryfikuje, czy waluta jednostki kontraktującej jest zgodna z walutą rozliczeniową firmy zawierającej kontrakt. Jeśli nie są one identyczne, nie można utworzyć tych rekordów. Waluta jednostki organizacyjnej jest definiowana w aplikacji Dynamics 365 Project Operations przez przejście do pozycji **Dataverse** > **Ustawienia** > **Jednostki organizacyjne**. Walutę księgowej firmy definiuje się w programie Dynamics 365 Finance, przechodząc do **Księga główna** > **Ustawienia księgi** > **Księga**. Waluta jest synchronizowana ze środowiskiem Dataverse przy użyciu mapy podwójnego zapisu w księgach.

System tworzy wartości rzeczywiste kosztu jednostkowego zasobów oraz sprzedaży jednostki organizacyjnej w następujących sytuacjach:

  - Kiedy jednostka zasobów jest inna niż jednostka kontraktująca
  - Kiedy firma zasobów jest inna niż firma kontraktująca

Jednak tylko transakcje, w których firma kontraktowa ma inną firmę, która zawiera kontrakt, zostanie przeniesiona do środowiska Dynamics 365 Finance na dodatkową księgę.

Księgowanie wartości rzeczywistych w projekcie jest rejestrowane w arkuszu integracji aplikacji Project Operations w aplikacji Finance. W systemie są tworzone poniższe wiersze arkusza.

| **Typ transakcji** | **Podmiot prawny** | **Tworzenie transakcji projektu przy księgowaniu** | **Wartości domyślne wymiaru finansowego pobierane z** | **Domyślna grupa podatku fakturowania i grupa podatku towaru do rozliczania** |
| --- | --- | --- | --- | --- |
| Koszt | Bez dodawania do arkusza integracji | nie dotyczy | nie dotyczy | nie dotyczy |
| Nierozliczona sprzedaż | Arkusz integracji z pożyczającym podmiotem prawnym | Tak | Project | **Grupa podatku fakturowania**: na podstawie **klienta kontraktu** <br/> **Grupa podatku towaru do rozliczania**: z bieżącej kategorii projektu podmiotu prawnego w wierszu arkusza |
| Koszt jednostkowy zasobów | Arkusz integracji z podmiotem prawnym udzielającym pożyczki | Brak | Klient międzyfirmowy | **Grupa podatku fakturowania**: na podstawie **klienta międzyfirmowego** <br/> **Grupa podatku towaru do rozliczania**: z bieżącej kategorii projektu podmiotu prawnego w wierszu arkusza |
| Sprzedaż międzyorganizacyjna | Arkusz integracji z podmiotem prawnym udzielającym pożyczki | Brak | Klient międzyfirmowy | **Grupa podatku fakturowania**: na podstawie **klienta międzyfirmowego** <br/> **Grupa podatku towaru do rozliczania**: z bieżącej kategorii projektu podmiotu prawnego w wierszu arkusza |

### <a name="example-intercompany-transactions"></a>Przykład: transakcje międzyfirmowe

Molly Clark zatrudniona jako deweloper w firmie GBPM rejestruje 10 godzin pracy w ramach projektu USPM Adventure Works, co jest zatwierdzane przez menedżera projektu. Koszt pracy dewelopera w firmie GBPM wynosi 88 GBP za godzinę. Firma GBPM wystawi fakturę dla USPM na 120 USD za godzinę pracy dewelopera. USPM wystawia klientowi, czy firmie Adventure Works, fakturę na 200 USD za pracę wykonywaną przez zasób GBPM. Aby uzyskać więcej informacji, zobacz [Konfigurowanie fakturowania międzyfirmowego](configure-intercompany-invoicing.md).

1. W aplikacji Project Operations przejdź do obszaru **Zasoby** i na liście wybierz **Molly Clark**. Na karcie **Planowanie**, w polu **Firma** wybierz **GBPM**.
2. Przejdź do pozycji **Sprzedaż** > **Klienci** i wybierz opcję **Nowy**, aby utworzyć nowy rekord klienta dla firmy Adventure Works.
    1. Ustaw firmę na **USPM**.
    2. Ustaw **typ relacji** na **Klient**.
    3. Wybierz pozycję **Grupa klientów 10 — krajowa**.
    4. Ustaw walutę na **USD**.
    5. Zapisz rekord.
3. Wybierz kolejno **Sprzedaż** > **Kontrakty projektu** i utwórz nowy kontrakt dotyczący firmy Adventure Works.
    1. Ustaw firmę będącą właścicielem na **USPM**, a jednostkę kontraktującą na **Contoso Robotics US**.
    2. Wybierz opcję Adventure Works jako klienta.
    3. Wybierz cennik produktów i zapisz rekord.
    4. Na karcie **Pozycje kontraktu** utwórz nową pozycję kontraktu. Ustaw dowolną nazwę i wybierz pozycję **Czas i materiały** jako metodę rozliczania.
    5. Utwórz nowy projekt i skojarz go z tą pozycją kontraktu.
4. Zaloguj się jako zasób **Molly Clark**. Przejdź do pozycji **Projekty** > **Wpisy czasu** i utwórz wpis czasu dla projektu Adventure Works.
5. Zaloguj się jako menedżer projektu. Wybierz opcję **Projekty** > **Zatwierdzenia** i zatwierdź transakcję wpisu czasu zarejestrowaną przez Molly Clark.
6. Przejdź do projektu Adventure Works i wybierz **Pokrewne** > **Wartości rzeczywiste**. Zostaną utworzone następujące transakcje dotyczące wartości rzeczywistych.

| **Typ transakcji** | **Cena** | **Waluta transakcji** | **Kwota** |
| --- | --- | --- | --- |
| Koszt | 120 | USD | 1200 |
| Nierozliczona sprzedaż | 200 | USD | 2000 |
| Koszt jednostkowy zasobów | 88 | GBP | 880 |
| Sprzedaż jednostki międzyorganizacyjnej | 120 | USD | 1200 |

7. Zaloguj się jako osoba zajmującą się księgowością USPM. Otwórz wystąpienie Project Operations w aplikacji Finance i wybierz firmę **USPM**. 
8. Przejdź do obszaru **Zarządzanie projektami i księgowanie** > **Okresowe** > **Project Operations w aplikacji Customer Engagement** > **Importowanie z przemieszczania** i wybierz opcję uruchomienia procesu okresowego. Ten proces okresowy spowoduje wypełnienie arkusza integracji aplikacji Project Operations.
9. Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Arkusze** > **Arkusz integracji Project Operations** i przejrzyj wiersze arkusza. W systemie jest tworzony następujący wiersz.

    | **Typ transakcji** | **Cena** | **Waluta transakcji** | **Kwota** |
    | --- | --- | --- | --- |
    | Nierozliczona sprzedaż | 200 | USD | 2000 |

    Jeśli system jest skonfigurowany w taki sposób, aby naliczony był przychód z danego projektu, są księgowane następujące elementy:

    - Debet: projekt — wartość sprzedaży PWT 200 USD
    - Kredyt: projekt — przychód naliczony 200 USD

    Ta niezafakturowana sprzedaż jest już gotowa do fakturowania. Faktura dla klienta firmy Adventure Works może być księgowana finansowo, gdy okaże się to potrzebne.

10. Zaloguj się jako osoba zajmującą się księgowością w **GBPM**. Otwórz wystąpienie Project Operations w aplikacji Finance i otwórz firmę **GBPM**. 
11. Przejdź do strony **Zarządzanie projektami i rozliczeniami** > **Okresowe** > **Integracja Project Operations** > **Importowanie z tabeli przemieszczania** i uruchom proces okresowy w celu wypełnienia dziennika integracji Project Operations.
12. Przejdź do pozycji **Zarządzanie projektami i księgowanie** > **Arkusze** > **Arkusz integracji Project Operations** i przejrzyj wiersze. W systemie są tworzone następujące wiersze.

    | **Typ transakcji** | **Cena** | **Waluta transakcji** | **Kwota** |
    | --- | --- | --- | --- |
    | Koszt jednostkowy zasobów | 88 | GBP | 880 |
    | Sprzedaż jednostki międzyorganizacyjnej | 120 | USD | 1200 |

    Księgowanie tych rekordów spowoduje powstanie następujących transakcji załącznika:

    - Debet: koszt projektu 88 GBP
    - Kredyt: alokacja płac 88 GBP

    Jeśli system jest skonfigurowany w taki sposób, aby naliczony był przychód międzyfirmowy, są księgowane następujące elementy:

    - Debet: projekt — wartość sprzedaży PWT 120 USD
    - Kredyt: projekt — przychód naliczony 120 USD

    System jest teraz gotowy do utworzenia międzyfirmowej faktury dla klienta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
