---
title: Połączenia transakcji — łączenie wartości rzeczywistych różnych typów transakcji
description: W temat wyjaśniono, w jaki sposób połączenie transakcji jest używane do łączenia wartości rzeczywistych różnych typów w celu śledzenia rentowności, backlogu fakturowania i rozliczania w stosunku do niezliczeniu przychodów.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580791"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Połączenia transakcji — łączenie wartości rzeczywistych różnych typów transakcji

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Rekordy połączeń transakcyjnych są tworzone w celu łączenia danych rzeczywistych różnych typów, takich jak czas, wydatki lub zmiany zużycia materiałów w ich cyklu życia od etapu wyceny lub przedsprzedaży do etapu umowy, zatwierdzeń i/lub wycofań, fakturowania i potencjalnie fakturowania kredytowego lub korygującego .

W następującym przykładzie przedstawiono typowy sposób przetwarzania wpisów czasu w cyklu życia projektu w rozwiązaniu Project Operations.

> ![Przetwarzanie całych czasu w Project Operations.](media/basic-guide-17.png)

Przetwarzanie wpisów czasu w cyklu życia rozwiązania Project Operations przebiega według następujących kroków: 

1. Przesłanie wpisu czasu powoduje utworzenie dwóch wierszy arkusza: jednego dla kosztu i jednego dla nierozliczonej sprzedaży. 
2. Końcowe zatwierdzenie wpisu czasu powoduje utworzenie dwóch wartości rzeczywistych: jednej dla kosztu i jednej dla nierozliczonej sprzedaży. Te dwa wartości rzeczywiste są łączone przy użyciu połączeń transakcji.
3. Kiedy użytkownik tworzy fakturę projektu, transakcja wiersza faktury jest tworzona przy użyciu danych z wartości rzeczywistej nierozliczonej sprzedaży.
4. Po potwierdzeniu faktury są tworzone dwie nowe wartości rzeczywiste: wycofanie nierozliczonej sprzedaży i wartość rzeczywista rozliczonej sprzedaży. Niezwiązane wyniki sprzedaży i oryginalna wartość rzeczywista sprzedaży nieudniwertowanych są połączone za pomocą cofania połączeń transakcji. Sprzedaż zaległych i oryginalne wartości rzeczywiste sprzedaży nielimiowane są również połączone w celu pokazania łączy między tym, co było już zaległych lub przychodów w toku (WIP) z przychodem już zaległym.   

Każde zdarzenie w przepływie pracy przetwarzania powoduje wyzwolenie tworzenia rekordów w tabeli **połączenia transakcji**. Pomaga to w budowaniu śledzenia relacji relacje między rekordami tworzonymi w czasie, wierszem daty, wartościami rzeczywistymi i szczegółami wiersza faktury.

W poniższej tabeli przedstawiono rekordy w encji **Połączenie transakcji** dla poprzedniego przepływu pracy.

|Zdarzenie                   |Transakcja 1                 |Rola transakcji 1 |Typ transakcji 1       |Transakcja 2          |Rola transakcji 2 |Typ transakcji 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Przesłanie wpisu czasu   |Identyfikator GUID wiersza arkusza (sprzedaż)     |Nierozliczona sprzedaż |msdyn_journalline            |Identyfikator GUID wiersza arkusza (koszt)     |Koszt            |msdyn_journalline  |
|Zatwierdzenie czasu           |Identyfikator GUID nierozliczonej wartości rzeczywistej (sprzedaż)  |Nierozliczona sprzedaż |msdyn_actual                 |Identyfikator GUID wartości rzeczywistej kosztu (koszt)       |Koszt            |msdyn_actual       |
|Tworzenie faktury        |Identyfikator GUID szczegółów wiersza faktury      |Rozliczona sprzedaż   |msdyn_invoicelinetransaction |Identyfikator GUID wartości rzeczywistej nierozliczonej sprzedaży   |Nierozliczona sprzedaż  |msdyn_actual       |
|Potwierdzenie faktury    |Identyfikator GUID wycofania wartości rzeczywistej         |Wycofywanie      |msdyn_actual                 |Identyfikator GUID pierwotnej nierozliczonej sprzedaży |Oryginalna        |msdyn_actual       |
|                        |Identyfikator GUID rozliczonej sprzedaży             |Rozliczona sprzedaż   |msdyn_actual                 |Identyfikator GUID wartości rzeczywistej nierozliczonej sprzedaży   |Nierozliczona sprzedaż  |msdyn_actual       |
|Korekta faktury w wersji roboczej |Identyfikator GUID transakcji wiersza faktury|Zastąpienie      |msdyn_invoicelinetransaction |Identyfikator GUID rozliczonej sprzedaży            |Oryginalna        |msdyn_actual       |
|Potwierdzanie korekty faktury|Identyfikator GUID wycofania rozliczonej sprzedaży  |Wycofywanie      |msdyn_actual                 |Identyfikator GUID rozliczonej sprzedaży            |Oryginalna        |msdyn_actual       |
|                        |Nowy identyfikator GUID sprzedaży bez faktur |Zastąpienie            |msdyn_actual                 |Identyfikator GUID rozliczonej sprzedaży            |Oryginalna        |msdyn_actual       |


Na poniższej ilustracji przedstawiono łącza utworzone między różnymi typami wartości rzeczywistych podczas różnych wydarzeń na przykładzie wpisów czasu w rozwiązaniu Project Operations.

> ![Jak są ze sobą połączone wartości rzeczywiste różnych typów w Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
