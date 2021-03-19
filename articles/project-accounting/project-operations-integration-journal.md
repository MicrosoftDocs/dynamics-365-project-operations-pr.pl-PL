---
title: Arkusz integracji w aplikacji Project Operations
description: Ta temat zawiera informacje na temat pracy z arkuszem integracji w Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0021147530d1aa9f82cc54ca8c92b9977c1eea2c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287251"
---
# <a name="integration-journal-in-project-operations"></a>Arkusz integracji w aplikacji Project Operations

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Wpisy czasu i wydatku tworzą **Rzeczywiste** transakcje reprezentujące praktyczny widok pracy wykonanej nad projektem. Rozwiązanie Dynamics 365 Project Operations zapewnia księgowym narzędzie do przeglądania transakcji i dostosowywania atrybutów księgowych zgodnie z potrzebami. Po zakończeniu przeglądu i dostosowań transakcje są księgowane w księgach i księdze głównej projektu. Te działania można wykonać przy użyciu arkusza **integracji Project Operations** (**Dynamics 365 Finance** > **Zarządzanie projektami i ich księgowanie** > **Arkusze** > **Arkusz integracji aplikacji Project Operations**.

![Przepływ dziennika integracji](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Utwórz rekordy w dzienniku Integracja operacji projektu

Rekordy w dzienniku integracji Project Operations są tworzone przy użyciu procesu okresowego **Import z tabeli przemieszczania**. Aby uruchomić ten proces, należy przechodząc do obszaru **Dynamics 365 Finance** > **Zarządzanie projektami i ich księgowanie** > **Okresowe** > **Integracja Project Operations** > **Import z tabeli przemieszczania**. Proces można uruchomić interakcyjnie lub skonfigurować go tak, aby uruchamiał się w tle w zależności od potrzeb.

Podczas przebiegu procesu okresowego można znaleźć wartości rzeczywiste, które nie zostały jeszcze dodane do arkusza integracji Project Operations. Zostanie utworzony wiersz dziennika dla każdej transakcji rzeczywistej.
Wiersze dziennika z grupami systemowymi jako oddzielne dzienniki na podstawie wartości wybranej w polu **Jednostka okresu w dzienniku Integracja operacji projektu** (**Finance** > **Zarządzanie projektami i ich księgowanie** > **Ustawienia** > **Zarządzanie projektem i parametry księgowe**, **Project Operations na karcie Dynamics 365 Customer Engagement**). Dopuszczalne wartości tego pola to:

  - **Dni**: wartości rzeczywiste są pogrupowane według daty transakcji. Dla każdego dnia jest tworzony osobny arkusz.
  - **Miesiące**: wartości rzeczywiste są pogrupowane według miesięcy kalendarzowych. Dla każdego miesiąca jest tworzony osobny arkusz.
  - **Lata**: wartości rzeczywiste są pogrupowane według lat kalendarzowych. Dla każdego roku jest tworzony osobny arkusz.
  - **Wszystkie**: wszystkie transakcje rzeczywiste są zawarte w tym samym arkuszu integracji. Jeśli arkusz nie jest dostępny w ramach procesu okresowego, na przykład jeśli arkusz jest w trakcie księgowania transakcji, tworzony jest nowy arkusz.

Wiersze arkusza są tworzone na podstawie wartości rzeczywistych projektu. Poniższa lista zawiera niektóre z bardziej istotnych reguł domyślnych i transformacji:

  - Każda transakcja rzeczywista projektu zawiera wiersz w arkuszu integracji Project Operations. Koszty i niezafakturowane transakcje sprzedaży na potrzeby fakturowania typu czas i materiały są przedstawione w oddzielnych wierszach.
  - Pole **Data** reprezentuje datę transakcji. Pole **Data księgowania** jest datą, kiedy transakcja jest rejestrowana w księdze głównej. Jeśli data księgowania znajduje się w [zamkniętym okresie finansowym](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), a dla parametru jest **Automatycznie ustawiana Data księgowania otwarta okresu księgi**, na karcie **Finanse** na stronie **Parametry zarządzania i księgowania projektów** system skoryguje datę księgowania transakcji na pierwszą datę w następnym otwartym okresie finansowym.
  - Pole **Załącznik** zawiera numer załącznika dla każdej transakcji rzeczywistej. Seria numerów załączników jest definiowana na karcie **Sekwencje numerów** na stronie **Parametry zarządzania projektami i parametrów księgowania**. Każdemu wierszowi przypisano nowy numer. Po zaksięgowaniu załącznika można sprawdzić, jak koszty i niezafakturowane transakcje sprzedaży są z nimi powiązane, wybierając **Pokrewne załączniki** na stronie **Transakcji załączników**.
  - Pole **Kategoria** reprezentuje transakcję projektu i wartości domyślne na podstawie kategorii transakcji dla pokrewnej wartości rzeczywistej projektu.
    - Jeśli **Kategoria transakcji** została ustawiona w wartości rzeczywistej projektu, a w danej firmie istnieje pokrewna **Kategoria projektu**, kategorią domyślną jest ta kategoria projektu.
    - Jeśli **Kategoria transakcji** nie jest ustawiona w polu wartość rzeczywista w projekcie, system użyje wartości pola **Domyślna kategoria projektu** na karcie **Project Operations w Dynamics 365 Customer Engagement** nastronie **Parametry zarządzania projektami i parametrów księgowania**.
  - Pole **Zasób** reprezentuje zasób projektu związany z daną transakcją. Zasób jest używany jako odwołanie w propozycjach faktur projektu dla klientów.
  - Domyślne pole **Kurs wymiany** na podstawie **Kurs wymiany waluty** ustawionego w Dynamics 365 Finance. Jeśli brakuje ustawienia kursu wymiany, proces okresowy **Importu z przemieszczania** nie spowoduje dodania rekordu do dziennika, a do dziennika wykonania zadania zostanie dodany komunikat o błędzie.
  - Pole **Właściwości wiersza** reprezentuje typ fakturowania w wartościach rzeczywistych projektu. Właściwości wierszy i mapowanie typów fakturowania są definiowane na karcie **Project Operations na Dynamics 365 Customer Engagement** na stronie **Parametry zarządzania projektami i parametrów księgowania**.

W wierszach arkusza integracji Project Operations można aktualizować tylko następujące atrybuty księgowe:

- **Grupa podatku fakturowania** i **Grupa podatku towaru do rozliczania**
- **Wymiary finansowe** (przy użyciu akcji **Rozdziel kwoty**)

Wiersze arkusza integracji można usunąć, jednak wszelkie niewysłane wiersze zostaną ponownie wstawione do arkusza po ponownym uruchomieniu okresowego procesu **Importowania z przemieszczania**.

Podczas księgowania arkusza integracji tworzona jest księga podrzędna projektu i transakcje księgi głównej. Są one używane w przeliczeniu na podrzędne fakturowanie klientów, rozpoznawaniu przychodów i raportowaniu finansowym.


[!INCLUDE[footer-include](../includes/footer-banner.md)]