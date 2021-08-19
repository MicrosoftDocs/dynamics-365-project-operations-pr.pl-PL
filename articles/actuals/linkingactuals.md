---
title: Łączenie wartości rzeczywistych z oryginalnymi rekordami
description: W tym temacie wyjaśniono, jak połączyć dane rzeczywiste z oryginalnymi rekordami, takimi jak zapis czasu, wpis wydatków lub dzienniki użycia materiałów.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991769"
---
# <a name="link-actuals-to-original-records"></a>Łączenie wartości rzeczywistych z oryginalnymi rekordami

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


W programie Dynamics 365 Project Operations *transakcja biznesowa* to abstrakcyjne pojęcie, które nie jest reprezentowane przez encję. Jednak niektóre typowe pola i procesy wykonywane na encjach zaprojektowano tak, aby korzystały z koncepcji transakcji biznesowych. Następujące podmioty używają tej koncepcji:

- Szczegóły wiersza oferty
- Szczegóły pozycji kontraktu
- Wiersze szacowania
- Wiersze arkusza
- Wartości rzeczywiste

Spośród tych encji **Szczegóły wiersza oferty**, **Szczegóły pozycji kontraktu** i **Wiersze szacowania** są mapowane na fazę oszacowania w cyklu życia projektu. Encje **Wiersze arkusza** i **Wartości rzeczywiste** są mapowane na fazę wykonywania w cyklu życia projektu.

Project Operations rozpoznaje rekordy w tych pięciu jednostkach jako transakcje biznesowe. Jedyna różnica polega na tym, że rekordy w encjach mapowanych na fazę szacowania są traktowane jako prognozy finansowe, podczas gdy rekordy w encjach mapowanych na fazę wykonywania są traktowane jako fakty finansowe, które już wystąpiły.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Pojęcia unikatowe dla transakcji biznesowych
Poniższe pojęcia są unikatowe dla koncepcji transakcji biznesowych:

- Typ transakcji
- Klasa transakcji
- Początkowy rekord transakcji
- Połączenie transakcji

### <a name="transaction-type"></a>Typ transakcji

Typ transakcji reprezentuje czas i kontekst wpływu aspektów finansowych w projekcie. Jest reprezentowany przez zestaw opcji mających następujące obsługiwane wartości w Project Operations:

  - Koszt
  - Kontrakt projektu
  - Nierozliczona sprzedaż
  - Rozliczona sprzedaż
  - Sprzedaż międzyorganizacyjna
  - Koszt jednostkowy zasobów

### <a name="transaction-class"></a>Klasa transakcji

Klasa transakcji reprezentuje różne typy kosztów ponoszonych w projektach. Jest reprezentowany przez zestaw opcji mających następujące obsługiwane wartości w Project Operations:

  - Czas
  - Wydatek
  - Materiał
  - Opłata
  - Punkt kontrolny
  - Podatek

Wartość **Punkt kontrolny** jest zwykle używana w logice biznesowej do rozliczania transakcji ze stałą ceną w Project Operations.

### <a name="transaction-origin"></a>Początkowy rekord transakcji

**Początkowy rekord transakcji** to encja przechowująca źródło pochodzenia każdej transakcji biznesowej. W miarę realizacji projektu każda transakcja biznesowa będzie skutkować kolejną transakcją biznesową, która z kolei stworzy kolejną i tak dalej. Jednostka pochodzenia transakcji jest przeznaczona do przechowywania danych o pochodzeniu każdej transakcji, aby pomóc w raportowaniu i identyfikowalności. 

### <a name="transaction-connection"></a>Połączenie transakcji

**Połączenie transakcji** to encja, która przechowuje relację między dwoma podobnymi transakcjami biznesowymi, takimi jak koszt i powiązane wartości rzeczywiste dotyczące sprzedaży, lub między wycofaniami transakcji wyzwalanymi przez działania fakturowania, takie jak potwierdzenie faktury lub korekty faktur.

Łącznie encje **Początkowy rekord transakcji** i **Połączenie transakcji** ułatwiają śledzenie relacji między transakcjami biznesowymi i działaniami, które spowodowały utworzenie określonej transakcji biznesowej.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Przykład: Jak encja Początkowy rekord transakcji współpracuje z encją Połączenie transakcji

W następującym przykładzie przedstawiono typowy sposób przetwarzania wpisów czasu w cyklu życia projektu w rozwiązaniu Project Operations.

> ![Wpisy przetwarzania czasu w cyklu życia w usłudze Project Service.](media/basic-guide-17.png)
 
1. Przesłanie wpisu czasu tworzy dwa wiersze arkusza: jeden wiersz dla kosztów i jeden dla niezafakturowanej sprzedaży.
2. Ostateczne zatwierdzenie wpisu czasu tworzy dwie wartości rzeczywiste: jedną rzeczywistą dla kosztów i jedną rzeczywistą dla sprzedaży niezafakturowanej.
3. Podczas tworzenia nowej faktury za projekt transakcja wiersza faktury jest tworzona przy użyciu danych z faktycznej sprzedaży niezafakturowanej. 
4. Po potwierdzeniu faktury tworzone są dwie nowe wartości rzeczywiste: faktyczne wycofanie sprzedaży niezafakturowanej i faktyczna sprzedaż zafakturowana.

Każde z tych zdarzeń powoduje utworzenie rekordu w encjach **Początkowy rekord transakcji** i **Połączenie transakcji**. Te nowe rekordy pomagają w tworzeniu historii relacji między rekordami, które są tworzone między zapisami czasu, wierszami arkusza, wartościami rzeczywistymi i szczegółami wiersza faktury.

W poniższej tabeli przedstawiono rekordy w encji **Początkowy rekord transakcji** dla poprzedniego przepływu pracy.

| Wydarzenie                        | Pochodzenie                   | Typ rekordu początkowego                       | Transakcja                       | Typ transakcji         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Przesłanie wpisu czasu        | Identyfikator GUID rekordu wpisu czasu   | Wpis czasu                        | Identyfikator GUID rekordu wiersza arkusza (koszt)   | Wiersz arkusza             |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID rekordu wiersza arkusza (sprzedaż)  | Wiersz arkusza                      |                          |
| Zatwierdzenie czasu                | Identyfikator GUID rekordu wiersza arkusza | Wiersz arkusza                      | Identyfikator GUID rekordu nierozliczonej sprzedaży        | Wartość rzeczywista                   |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID rekordu nierozliczonej sprzedaży        | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID rekordu wartości rzeczywistej kosztu           | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID rekordu wartości rzeczywistej kosztu           | Rzeczywiste                            |                          |
| Tworzenie faktury             | Identyfikator GUID rekordu wpisu czasu   | Wpis czasu                        | Identyfikator GUID transakcji wiersza faktury     | Transakcja wiersza faktury |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID transakcji wiersza faktury     | Transakcja wiersza faktury          |                          |
| Potwierdzenie faktury         | Identyfikator GUID wiersza faktury        | Wiersz faktury                      | Identyfikator GUID rekordu rozliczonej sprzedaży          | Wartość rzeczywista                   |
| Identyfikator GUID faktury                 | Faktura                  | Identyfikator GUID rekordu rozliczonej sprzedaży          | Wartość rzeczywista                            |                          |
| Identyfikator GUID szczegółów wiersza faktury     | Szczegóły wiersza faktury      | Identyfikator GUID rekordu rozliczonej sprzedaży          | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID rekordu rozliczonej sprzedaży          | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID rekordu rozliczonej sprzedaży          | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID wycofania nierozliczonej sprzedaży      | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID wycofania nierozliczonej sprzedaży      | Wartość rzeczywista                            |                          |
| Korekta faktury w wersji roboczej     | Identyfikator GUID szczegółów wiersza starej faktury             | Transakcja wiersza faktury          | Identyfikator GUID szczegółów wiersza faktury korygującej               | Transakcja wiersza faktury |
| Identyfikator GUID starego wiersza                  | Wiersz faktury             | Identyfikator GUID szczegółów wiersza faktury korygującej               | Transakcja wiersza faktury          |                          |
| Identyfikator GUID starej faktury             | Faktura                  | Identyfikator GUID szczegółów wiersza faktury korygującej               | Transakcja wiersza faktury          |                          |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID szczegółów wiersza faktury korygującej               | Transakcja wiersza faktury          |                          |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID szczegółów wiersza faktury korygującej               | Transakcja wiersza faktury          |                          |
| Potwierdzona korekta faktury | Identyfikator GUID szczegółów wiersza starej faktury             | Transakcja wiersza faktury          | Identyfikator GUID wycofanej wartości rzeczywistej sprzedaży | Wartość rzeczywista                   |
| Identyfikator GUID starego wiersza                  | Wiersz faktury             | Identyfikator GUID wycofanej wartości rzeczywistej sprzedaży | Wartość rzeczywista                            |                          |
| Identyfikator GUID starej faktury             | Faktura                  | Identyfikator GUID wycofanej wartości rzeczywistej sprzedaży | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID wycofanej wartości rzeczywistej sprzedaży | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID wycofanej wartości rzeczywistej sprzedaży | Wartość rzeczywista                            |                          |
| Identyfikator GUID szczegółów wiersza starej faktury                 | Transakcja wiersza faktury | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |
| Identyfikator GUID starego wiersza                  | Wiersz faktury             | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |
| Identyfikator GUID starej faktury             | Faktura                  | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |
| Identyfikator GUID szczegółów wiersza faktury korygującej          | Transakcja wiersza faktury | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |
| Identyfikator GUID wiersza faktury korygującej           | Wiersz faktury             | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |
| Identyfikator GUID faktury korygującej      | Faktura                  | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Wartość rzeczywista                            |                          |

W poniższej tabeli przedstawiono rekordy w encji **Połączenie transakcji** dla poprzedniego przepływu pracy.

| Wydarzenie                          | Transakcja 1                 | Rola transakcji 1 | Typ transakcji 1           | Transakcja 2                | Rola transakcji 2 | Typ transakcji 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Przesłanie wpisu czasu          | Identyfikator GUID wiersza arkusza (sprzedaż)     | Nierozliczona sprzedaż     | msdyn_journalline            | Identyfikator GUID wiersza arkusza (koszt)     | Koszt               | msdyn_journalline  |
| Zatwierdzenie czasu                  | Identyfikator GUID nierozliczonej wartości rzeczywistej (sprzedaż)  | Nierozliczona sprzedaż     | msdyn_actual                 | Identyfikator GUID wartości rzeczywistej kosztu (koszt)       | Koszt               | msdyn_actual       |
| Tworzenie faktury               | Identyfikator GUID szczegółów wiersza faktury      | Rozliczona sprzedaż       | msdyn_invoicelinetransaction | Identyfikator GUID wartości rzeczywistej nierozliczonej sprzedaży   | Nierozliczona sprzedaż     | msdyn_actual       |
| Potwierdzenie faktury           | Identyfikator GUID wycofania wartości rzeczywistej         | Wycofywanie          | msdyn_actual                 | Identyfikator GUID pierwotnej nierozliczonej sprzedaży | Oryginalna           | msdyn_actual       |
| Identyfikator GUID rozliczonej sprzedaży              | Rozliczona sprzedaż                  | msdyn_actual       | Identyfikator GUID wartości rzeczywistej nierozliczonej sprzedaży   | Nierozliczona sprzedaż               | msdyn_actual       |                    |
| Korekta faktury w wersji roboczej       | Identyfikator GUID transakcji wiersza faktury | Zastąpienie          | msdyn_invoicelinetransaction | Identyfikator GUID rozliczonej sprzedaży            | Oryginalna           | msdyn_actual       |
| Potwierdzanie korekty faktury     | Identyfikator GUID wycofania rozliczonej sprzedaży    | Wycofywanie          | msdyn_actual                 | Identyfikator GUID rozliczonej sprzedaży            | Oryginalna           | msdyn_actual       |
| Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży | Zastąpienie                     | msdyn_actual       | Identyfikator GUID rozliczonej sprzedaży            | Oryginalna                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
