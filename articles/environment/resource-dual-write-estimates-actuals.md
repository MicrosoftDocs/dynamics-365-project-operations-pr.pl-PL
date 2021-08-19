---
title: Szacowania projektu i integracja wartości rzeczywistych
description: Ten temat zawiera informacje na temat integracji podwójnego zapisu w Project Operations dla oszacowań i danych rzeczywistych projektu.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006304"
---
# <a name="project-estimates-and-actuals-integration"></a>Szacowania projektu i integracja wartości rzeczywistych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat zawiera informacje na temat integracji podwójnego zapisu w Project Operations dla oszacowań i danych rzeczywistych projektu.

## <a name="project-estimates"></a>Szacowania projektu

Szacunki dotyczące robocizny, kosztów i materiałów są tworzone i utrzymywane w Microsoft Dataverse oraz synchronizowane z aplikacjami Finance and Operations w celach księgowych. Operacje tworzenia, aktualizowania i usuwania nie są obsługiwane za pośrednictwem aplikacji Finance and Operations.

Do tworzenia oszacowania jest wymagana prawidłowa konfiguracja księgowości dla projektu. Projekty skojarzone z wierszami kosztów muszą mieć prawidłowy profil kosztów i przychodów zdefiniowany w regułach kosztów projektu i profilu przychodu. Aby uzyskać więcej informacji, zobacz temat [Konfigurowanie rozliczania projektów rozliczanych](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Szacowanie pracy

Szacunki robocizny są tworzone przez kierownika projektu lub kierownika zasobów, który również przypisuje ogólny lub nazwany zasób do zadania projektowego. Rekordy przypisania zasobów można przeglądać na karcie **Przypisania zasobów** na stronie **Szczegóły projektu** w Dataverse. Rekordy przydziału zasobów w Dataverse tworzą rekordy prognozy godzin w aplikacjach Finance and Operations przy użyciu **Encji integracji Project Operations dla szacunków godzin (msdyn\_resourceassignments)**.

   ![Integracja szacunków pracy.](./Media/DW4LaborEstimates.png)

Podwójny zapis synchronizuje rekordy przydziału zasobów do tabeli inscenizacji (**ProjCDSEstimateHoursImport**), a następnie wykorzystuje logikę biznesową do tworzenia i aktualizacji rekordów prognozy godzin (**ProjForecastEmpl**).

Księgowy projektu przegląda zapisy prognozowanych godzin utworzone w aplikacjach Finance and Operations przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Plan** > **Prognozy godzin**.

## <a name="expense-estimates"></a>Szacowanie wydatków

Szacunkowe koszty są tworzone przez menedżera projektu na karcie **Szacowanie wydatków** na stronie **Szczegóły projektu** w Dataverse. Rekordy szacowania wydatków są przechowywane w encji **Wiersz szacowania** w Dataverse. Te rekordy szacowania mają klasę transakcji **Wydatek** i są synchronizowane z rekordami prognozy wydatków w aplikacjach Finance and Operations przy użyciu **Encji integracji Project Operations dla szacowania wydatków (msdyn\_estimatelines)**.

   ![Integracja szacunków wydatków.](./Media/DW4ExpenseEstimates.png)

Podwójny zapis synchronizuje rekordy prognozy wydatków do tabeli inscenizacji **ProjCDSEstimateExpenseImport)**, a następnie wykorzystuje logikę biznesową do tworzenia i aktualizacji rekordów prognozy wydatków (**ProjForecastCost**). W wierszach szacowania są przechowywane oddzielnie rekordy szacowania sprzedaży i szacowania wydatków. Logika biznesowa w aplikacjach Finance and Operations wypełnia pojedynczy rekord prognozy wydatków, korzystając z tych szczegółów w tabeli przemieszczania.

Księgowy projektu może analizować zapisy prognozowanych godzin utworzone w aplikacjach Finance and Operations przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Plan** > **Prognozy wydatków**.

## <a name="material-estimates"></a>Szacowania materiałów

Szacowanie materiałów jest tworzone przez menedżera projektu na karcie **Szacowanie materiałów** na stronie **Szczegóły projektu** w Dataverse. Rekordy szacowania materiałów są przechowywane w encji **Wiersz szacowania** w Dataverse. Te rekordy szacowania mają klasę transakcji **Materiał** i są synchronizowane z rekordami prognozy wydatków w aplikacjach Finance and Operations przy użyciu **Tabeli integracji Project Operations dla szacowania materiałów (msdyn\_estimatelines)**.

   ![Integracja szacunków materiałów.](./Media/DW4MaterialEstimates.png)

Podwójny zapis synchronizuje rekordy szacowania materiałów do tabeli inscenizacji **ProjForecastSalesImpor**, a następnie wykorzystuje logikę biznesową do tworzenia i aktualizacji rekordów prognozy Elementu (**ForecastSales**). W wierszach szacowania są przechowywane oddzielnie rekordy szacowania sprzedaży i szacowania wydatków. Logika biznesowa w aplikacjach Finance and Operations wypełnia pojedynczy rekord prognozy Element, korzystając z tych szczegółów w tabeli przemieszczania.

Księgowy projektu może analizować zapisy prognozowanych elemetów utworzone w aplikacjach Finance and Operations przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Plan** > **Prognozy elementów**.

## <a name="project-actuals"></a>Wartości rzeczywiste projektu

Wartości rzeczywiste projektu są tworzone w Dataverse na podstawie czasu, wydatków, materiałów i działań dotyczących fakturowania. W tej encji Dataverse są przechwytywane wszystkie atrybuty operacyjne tych transakcji, w tym ilość, cena kosztów, cena sprzedaży i projekt. Aby uzyskać więcej informacji, zobacz [Wartości rzeczywiste](../actuals/actuals-overview.md). Wartości rzeczywiste są synchronizowane z aplikacjami Finance and Operations przy użyciu podwójnego zapisu mapowania tabeli w ramach **Wartości rzeczywistych Project Operations (msdyn\_actuals)** dla późniejszego księgowania.

   ![Integracja wartości rzeczywistych.](./Media/DW4Actuals.png)

Mapowanie tabeli **Integracji wartości rzeczywistych Project Operations** synchronizuje wszystkie rekordy z encji **Wartości rzeczywiste** w Dataverse z atrybutem **Pomiń synchronizację (tylko do użytku wewnętrznego)** ustawionym na wartość **False**. Ta wartość atrybutu jest ustawiana w Dataverse automatycznie podczas tworzenia rekordu. Przykłady, w których ten atrybut ma wartość **True**:

  - Wartości rzeczywiste kosztu projektu dla transakcji międzyfirmowych. Aby uzyskać więcej informacji, zobacz temat [Tworzenie transakcji międzyfirmowych](../project-accounting/create-intercompany-transactions.md). Zapisy te są pomijane, ponieważ system odtwarza rzeczywisty koszt projektu w aplikacjach Finance and Operations w momencie zaksięgowania faktury sprzedawcy wewnątrz firmy.
  - Negatywny zapis sprzedaży niefakturowanej tworzony w momencie potwierdzenia faktury proforma. Rekordy te są pomijane, ponieważ księga pomocnicza projektu w aplikacjach Finance and Operations nie odwraca niefakturowanego rekordu sprzedaży przy fakturowaniu, lecz zmienia status na całkowicie zafakturowany.

Mapa tabeli podwójnego zapisu synchronizuje rekordy wartości rzeczywistych z tabelą etapu **ProjCDSActualsImport**. Rekordy te są przetwarzane przez proces okresowy **Import z tabeli etapu** podczas tworzenia linii dziennika integracji Project Operations oraz linii propozycji faktur projektowych. Aby uzyskać więcej informacji, zobacz temat [Integracja dziennika w Project Operations](../project-accounting/project-operations-integration-journal.md).

W Dataverse są również przechwytywane łącza między rzeczywistymi transakcjami w encji **Połączenie transakcji**. Aby uzyskać więcej informacji, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](../actuals/linkingactuals.md). Powiązania pomiędzy rzeczywistymi transakcjami są również synchronizowane z aplikacjami Finance and Operations za pomocą mapy tabel podwójnego zapisu **Encja integracji dla relacji transakcyjnych projektu (msdyn\_transactionconnections)**. Rekordy te są używane przez proces okresowy **Import z tabeli etapu** podczas tworzenia linii dziennika integracji Project Operations oraz linii propozycji faktur projektowych.

Zaksięgowanie dziennika integracji Project Operations i oferty faktury projektu powoduje wyzwolenie aktualizacji w odpowiednich rekordach tabeli etapu **ProjCDSActualsImport**. W systemie są przechwytywane i rejestrowane następujące atrybuty księgowe dla transakcji rzeczywistych:

- Kwota w walucie księgowej
- Kurs wymiany
- Numer załącznika
- Kwota podatku

Tabela mapowania **Integracji wartości rzeczywistych Project Operations** aktualizuje odpowiednie rekordy wartości rzeczywistych w Dataverse tymi informacjami.
