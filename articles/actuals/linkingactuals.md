---
title: Pochodzenia transakcji — łączenie wartości rzeczywistych ze źródłem
description: W tym artykule wyjaśniono, w jaki sposób pojęcie pochodzenia transakcji jest używane do łączenia wartości rzeczywistych z oryginalnymi rekordami źródłowymi, na przykład do wprowadzania czasu, wprowadzania wydatków lub dzienników użycia materiałów.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921315"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Pochodzenia transakcji — łączenie wartości rzeczywistych ze źródłem

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rekordy pochodzenia transakcji są tworzone w celu połączenia wartości rzeczywistych ze źródłem, takich jak wpisy czasu, wpisy kosztów, dzienniki użycia materiałów i faktury projektu.

W następującym przykładzie przedstawiono typowy sposób przetwarzania wpisów czasu w cyklu życia projektu w rozwiązaniu Project Operations.

> ![Przetwarzanie całych czasu w Project Operations.](media/basic-guide-17.png)
 
1. Przesłanie wpisu czasu powoduje utworzenie dwóch wierszy arkusza: jednego dla kosztu i jednego dla nierozliczonej sprzedaży.
2. Końcowe zatwierdzenie wpisu czasu powoduje utworzenie dwóch wartości rzeczywistych: jednej dla kosztu i jednej dla nierozliczonej sprzedaży.
3. Kiedy użytkownik tworzy fakturę projektu, transakcja wiersza faktury jest tworzona przy użyciu danych z wartości rzeczywistej nierozliczonej sprzedaży.
4. Po potwierdzeniu faktury są tworzone dwie nowe wartości rzeczywiste: wycofanie nierozliczonej sprzedaży i wartość rzeczywista rozliczonej sprzedaży.

Każde zdarzenie w tym przepływie pracy przetwarzania wyzwala tworzenie rekordów w encji Pochodzenie transakcji, aby pomóc w tworzeniu śladu relacji między tymi rekordami, które są tworzone w zakresie wpisu czasu, wiersza dziennika, danych rzeczywistych i szczegółów wiersza faktury.

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
| Identyfikator GUID faktury korygującej      | Faktura                  | Identyfikator GUID nowej wartości rzeczywistej nierozliczonej sprzedaży    | Rzeczywiste                            |                          |


Na poniższym rysunku pokazano łącza tworzone między wartościami rzeczywistymi i ich źródłami podczas różnych zdarzeń przy użyciu przykładowych wpisów czasu w Project Operations.

> ![Jak wartości rzeczywiste są łączone z rekordami źródłowymi w Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
