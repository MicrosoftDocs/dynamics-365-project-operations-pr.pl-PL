---
title: Zapytanie dotyczące środków federalnych
description: Ten temat zawiera informacje na temat zapytania dotyczącego środków federalnych.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d0cc3db3fd05fa809f707b15a50380753ac8f9f779f45c13f707321d2b0e0841
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007249"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Zapytanie dotyczące środków federalnych

[!include [banner](../includes/banner.md)]

Zgodnie z dyrektywą A-133 Urzędu zarządzania i budżetu, agencje, które otrzymują fundusze federalne, podlegają obowiązkom przeprowadzenia audytu, które są również określane jako pojedyncze kontrole. Proces audytu jest wykorzystywany w celu cyklicznego tworzenia sprawozdań na temat dochodów i wydatków w ramach grantów federalnych. Część raportu dotyczącego pojedynczego audytu zawiera zestawienie wydatków w ramach środków federalnych (SEFA).

Zestawienie wydatków w ramach środków federalnych zawiera katalog Federalnej pomocy krajowej (CFDA), tytuł i numer, numer grantu, rok przyznania, nazwę agencji Federalnej, która dostarcza fundusze, oraz nazwę jednostki przekazującej dane. Zapytanie dotyczy określonego okresu. Zazwyczaj ten okres jest taki sam, jak okres sprawozdania finansowego, czyli rok obrachunkowy.

Zapytanie dotyczy także grantów z przewidywanymi datami realizacji w wybranym zakresie. Kolumna **Przyznająca agencja** w zapytaniu wskazuje klienta grantu lub, w ramach grantu przekazywanego, agencję przyznającą grant. W przypadku grantu przekazywanego, kolumna **Agencja przekazująca** wskazuje klienta grantu. Jeśli grant jest inny niż przekazywany, kolumna **Agencja przekazująca** jest pusta.

## <a name="set-up-the-cfda-clusters"></a>Konfiguracja klastrów CFDA

Konieczne jest skonfigurowanie klastrów CFDA, które mogą być skojarzone z numerami CFDA w zapytaniu dotyczącym zestawienia wydatków w ramach środków federalnych.

1. Wybierz kolejno pozycje **Zarządzanie projektami i księgowanie \> Konfiguracja \> Granty \> Katalog klastrów federalnej pomocy krajowej**.
2. Aby utworzyć nowy klastr CFDA wybierz opcję **Nowy**.
3. Wprowadź nazwę klastra.
4. Wybierz **Zapisz**, aby zapisać zmiany.

## <a name="set-up-cfda-numbers"></a>Konfigurowanie numerów CFDA

Konieczne jest skonfigurowanie numerów CFDA, które będą dodane do grantów i zawarte w zapytaniu dotyczącym zestawienia wydatków w ramach środków federalnych.

1. Wybierz kolejno pozycje **Zarządzanie projektami i księgowanie \> Konfiguracja \> Granty \> Numery katalogu federalnej pomocy krajowej**.
2. Wybierz opcję **Nowy**, aby nadać numer CFDA.
3. W kolumnie **Liczba** wprowadź numer CFDA.
4. Naciśnij klawisz **Tab**.
5. W kolumnie **Opis** wprowadź tytuł CFDA.
6. Naciśnij klawisz **Tab**.
7. Opcjonalnie: w polu **Klaster programów** dodaj odpowiedni klaster CFDA.
8. Wybierz **Zapisz**, aby zapisać zmiany.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Konfigurowanie grantów na potrzeby sporządzania raportów na temat zestawień wydatków w ramach środków federalnych

1. W tym celu należy przejść do obszaru **Zarządzanie projektami i księgowanie \> Granty \> Granty** oraz wybrać istniejący grant.
2. Na skróconej karcie **Konfiguracja** w polu **Katalog federalnej pomocy krajowej** przypisz numer CFDA. Numer CFDA określa raportowany klaster CFDA.
3. Na skróconej karcie **Informacje kontaktowe** FastTab wprowadź informacje dotyczące podmiotu udzielającego grant, wykonując następujące kroki:

    1. W polu **Klient grantu** wprowadź klienta, który jest odpowiedzialny za grant. W przypadku istniejącego grantu te informacje mogą być już wprowadzane.
    2. Wskazuje, czy dany klient jest fundatorem. Jeśli dany klient jest fundatorem, pole **Przekazanie** powinno być czyste. Jeśli fundatorem jest inny klient, a klient grantu jest odpowiedzialny za wydanie i śledzenie funduszy, pole **Przekazanie** powinno być zaznaczone.

4. Jeśli wybrano pole **Przekazanie** w poprzednim kroku, w polu **Agencja przyznająca grant** wprowadź klienta, który przekazał grant. Agencja przyznająca grant i klient grantu nie może być tym samym podmiotem.

Oto przykład grantu przekazanego:

Rząd federalny finansuje projekt infrastrukturalny w danym stanie. Rząd federalny przyznaje środki do wydania stanowi. W tym przypadku rząd federalny to organizacja przyznająca grant, a stan jest klientem grantu.

> [!NOTE] 
> Po pierwszym włączeniu funkcji początkowe numery CFDA będą wprowadzane przy użyciu istniejących numerów dla grantów.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Wyłączenie grantów z raportów SEFA w zależności od typu grantu

1. Wybierz pozycje **Zarządzanie projektami i księgowanie \> Konfiguracja \> Granty \> Typy grantów**.
2. Na skróconej karcie **Informacje domyślne** zaznacz pole **Wyklucz z zapytania dotyczącego zestawienia wydatków w ramach środków federalnych**.
3. Wybierz **Zapisz**, aby zapisać zmiany.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Uruchamianie zapytania dotyczącego środków federalnych

1. Przejdź do **Zarządzanie projektami i księgowanie \> Zapytania i raporty \> Zapytanie grantowe \> Zapytanie dotyczące wydatków w ramach środków federalnych**.
2. W sekcji **Parametry** postępuj zgodnie z poniższymi krokami:

    1. W polu **Zakres da** wybierz kod interwału dat. Można też określić interwał daty w polach **Data od** oraz **Data do**.
    2. Opcjonalnie: aby uwzględnić w zapytaniu tylko transakcje zafakturowane jako przychód , należy ustawić opcję **Dołącz tylko rozliczone przychody** na **Tak**.

## <a name="columns"></a>Kolumny

Zapytanie dotyczące środków federalnych zawiera następujące kolumny:

- Nazwa klastra katalogu federalnej pomocy krajowej
- Agencja udzielająca grantu
- Agencja przekazująca
- Nazwa grantu
- Identyfikator grantu
- Identyfikator przyznania grantu
- Katalog federalnej pomocy krajowej
- Paragony
- Wydatki


[!INCLUDE[footer-include](../includes/footer-banner.md)]