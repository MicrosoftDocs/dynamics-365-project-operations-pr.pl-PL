---
title: Transakcje biznesowe
description: Ten temat zawiera informacje o transakcjach biznesowych.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7c1fd7046783b98b7c2e823b2c2eb8bbdfb232fc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583358"
---
# <a name="business-transactions"></a>Transakcje biznesowe

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

W programie Dynamics 365 Project Service Automation *transakcja biznesowa* to abstrakcyjne pojęcie, które nie jest reprezentowane przez żadną encję. Jednak niektóre typowe pola i procesy wykonywane na encjach zaprojektowano tak, aby korzystały z koncepcji transakcji biznesowych. To abstrakcyjne pojęcie jest używane w następujących encjach:

- Szczegóły wiersza oferty
- Szczegóły pozycji kontraktu
- Wiersze szacowania
- Wiersze arkusza
- Wartości rzeczywiste

Spośród tych encji Szczegóły wiersza oferty, Szczegóły pozycji kontraktu i Wiersze szacowania są mapowane na fazę oszacowania w cyklu życia projektu. Encje Wiersze arkusza i Wartości rzeczywiste są mapowane na fazę wykonywania w cyklu życia projektu.

Rozwiązanie PSA traktuje rekordy w tych pięciu encjach jako transakcje biznesowe. Jedyna różnica polega na tym, że rekordy w encjach mapowanych na fazę szacowania są traktowane jako prognozy finansowe, podczas gdy rekordy w encjach mapowanych na fazę wykonywania są traktowane jako fakty finansowe, które już wystąpiły.

Aby uzyskać więcej informacji, zobacz [Szacunki](estimates.md) i [Wartości rzeczywiste](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Pojęcia unikatowe dla transakcji biznesowych
Poniższe pojęcia są unikatowe dla koncepcji transakcji biznesowych:

- Typ transakcji
- Klasa transakcji
- Początkowy rekord transakcji
- Połączenie transakcji

### <a name="transaction-type"></a>Typ transakcji

Typ transakcji reprezentuje czas i kontekst wpływu aspektów finansowych w projekcie. Jest reprezentowany przez zestaw opcji mających następujące obsługiwane wartości w rozwiązaniu PSA:
- Koszt
- Kontrakt projektu
- Nierozliczona sprzedaż
- Rozliczona sprzedaż
- Sprzedaż międzyorganizacyjna
- Koszt jednostkowy zasobów

### <a name="transaction-class"></a>Klasa transakcji

Klasa transakcji reprezentuje różne typy kosztów ponoszonych w projektach. Jest reprezentowany przez zestaw opcji mających następujące obsługiwane wartości w rozwiązaniu PSA:

- Time
- Wydatek
- Materiał
- Opłata
- Punkt kontrolny
- Podatek

Wartość **Punkt kontrolny** jest zwykle używana w logice biznesowej do rozliczania transakcji ze stałą ceną w rozwiązaniu PSA.

### <a name="transaction-origin"></a>Początkowy rekord transakcji

Początkowy rekord transakcji to encja przechowująca źródło pochodzenia każdej transakcji biznesowej. W miarę wykonywania projektu każda transakcja biznesowa spowoduje powstanie innej transakcji biznesowej, która z kolei stworzy następną i tak dalej. Encja Początkowy rekord transakcji została zaprojektowana w celu przechowywania danych o pochodzeniu każdej transakcji, aby ułatwić raportowanie i śledzenie. 

### <a name="transaction-connection"></a>Połączenie transakcji

Połączenie transakcji to encja, która przechowuje relację między dwoma podobnymi transakcjami biznesowymi, takimi jak koszt i powiązane wartości rzeczywiste dotyczące sprzedaży, lub między wycofaniami transakcji wyzwalanymi przez działania fakturowania, takie jak potwierdzenie faktury lub korekty faktur.

Łącznie encje Początkowy rekord transakcji i Połączenie transakcji ułatwiają śledzenie relacji między transakcjami biznesowymi i działaniami, które spowodowały utworzenie określonej transakcji biznesowej.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Przykład: Jak encja Początkowy rekord transakcji współpracuje z encją Połączenie transakcji

W następującym przykładzie przedstawiono typowy sposób przetwarzania wpisów czasu w cyklu życia projektu w rozwiązaniu PSA.

> ![Wpisy przetwarzania czasu w cyklu życia w usłudze Project Service.](media/basic-guide-17.png)
 
1. Przesłanie wpisu czasu powoduje utworzenie dwóch wierszy arkusza: jednego dla kosztu i jednego dla nierozliczonej sprzedaży.
2. Końcowe zatwierdzenie wpisu czasu powoduje utworzenie dwóch wartości rzeczywistych: jednej dla kosztu i jednej dla nierozliczonej sprzedaży.
3. Kiedy użytkownik tworzy fakturę projektu, transakcja wiersza faktury jest tworzona przy użyciu danych z wartości rzeczywistej nierozliczonej sprzedaży. 
4. Po potwierdzeniu faktury są tworzone dwie nowe wartości rzeczywiste: wycofanie nierozliczonej sprzedaży i wartość rzeczywista rozliczonej sprzedaży.

Każde z tych zdarzeń wyzwala tworzenie rekordów w encjach Początkowy rekord transakcji i Połączenie transakcji w celu ułatwienia śledzenia relacji między tymi rekordami, które są tworzone we wpisie czasu, wierszu arkusza, wartościach rzeczywistych i szczegółach wiersza faktury.

W poniższej tabeli przedstawiono rekordy w encji Początkowy rekord transakcji dla poprzedniego przepływu pracy.

| Zdarzenie                        | Rekord początkowy                   | Typ rekordu początkowego                       | Transakcja                       | Typ transakcji         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Przesłanie wpisu czasu        | Identyfikator GUID rekordu wpisu czasu   | Wpis czasu                        | Identyfikator GUID rekordu wiersza arkusza (koszt)   | Wiersz arkusza             |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID rekordu wiersza arkusza (sprzedaż)  | Wiersz arkusza                      |                          |
| Zatwierdzenie czasu                | Identyfikator GUID rekordu wiersza arkusza | Wiersz arkusza                      | Identyfikator GUID rekordu nierozliczonej sprzedaży        | Wartość rzeczywista                   |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID rekordu nierozliczonej sprzedaży        | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wiersza arkusza     | Wiersz arkusza             | Identyfikator GUID rekordu wartości rzeczywistej kosztu           | Wartość rzeczywista                            |                          |
| Identyfikator GUID rekordu wpisu czasu       | Wpis czasu               | Identyfikator GUID rekordu wartości rzeczywistej kosztu           | Wartość rzeczywista                            |                          |
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

W poniższej tabeli przedstawiono rekordy w encji Połączenie transakcji dla poprzedniego przepływu pracy.

| Zdarzenie                          | Transakcja 1                 | Rola transakcji 1 | Typ transakcji 1           | Transakcja 2                | Rola transakcji 2 | Typ transakcji 2 |
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
