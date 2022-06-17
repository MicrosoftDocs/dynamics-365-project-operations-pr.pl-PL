---
title: Szacowania projektu i integracja wartości rzeczywistych
description: W tym artykule przedstawiono informacje dotyczące integracji podwójnego zapisu w aplikacji Project Operations na potrzeby szacowanych i rzeczywistych wartości projektu.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914599"
---
# <a name="project-estimates-and-actuals-integration"></a>Szacowania projektu i integracja wartości rzeczywistych

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

W tym artykule przedstawiono informacje dotyczące integracji podwójnego zapisu w aplikacji Project Operations na potrzeby szacowanych i rzeczywistych wartości projektu.

## <a name="project-estimates"></a>Szacowania projektu

Szacunki dotyczące robocizny, wydatków i materiałów w ramach projektu są tworzone i przechowywane w Microsoft Dataverse oraz synchronizowane z aplikacjami finansowymi i operacyjnymi dla celów księgowych. Operacje tworzenia, aktualizacji i usuwania nie są obsługiwane przez aplikacje finansowe i operacyjne.

Do tworzenia oszacowania jest wymagana prawidłowa konfiguracja księgowości dla projektu. Projekty skojarzone z wierszami kosztów muszą mieć prawidłowy profil kosztów i przychodów zdefiniowany w regułach kosztów projektu i profilu przychodu. Aby uzyskać więcej informacji, zobacz temat [Konfigurowanie rozliczania projektów rozliczanych](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Szacowanie pracy

Szacunki robocizny są tworzone przez kierownika projektu lub kierownika zasobów, który również przypisuje ogólny lub nazwany zasób do zadania projektowego. Rekordy przypisania zasobów można przeglądać na karcie **Przypisania zasobów** na stronie **Szczegóły projektu** w Dataverse. Rekordy przypisania zasobów w rekordach Dataverse prognozy godzin w aplikacjach finansowych i operacyjnych przy użyciu encji **integracji Project Operations dla szacowania godzin (msdynresourceassignments\_)**.

   ![Integracja szacunków pracy.](./Media/DW4LaborEstimates.png)

Podwójny zapis synchronizuje rekordy przydziału zasobów do tabeli inscenizacji (**ProjCDSEstimateHoursImport**), a następnie wykorzystuje logikę biznesową do tworzenia i aktualizacji rekordów prognozy godzin (**ProjForecastEmpl**).

Księgowy projektu przegląda zapisy prognozowanych godzin utworzone w aplikacjach finansowych i operacyjnych, przechodząc do **Zarządzanie projektem i księgowość** > **Wszystkie projekty** > **Plan** > **Prognozy godzin**.

## <a name="expense-estimates"></a>Szacowanie wydatków

Szacunkowe koszty są tworzone przez menedżera projektu na karcie **Szacowanie wydatków** na stronie **Szczegóły projektu** w Dataverse. Rekordy szacowania wydatków są przechowywane w encji **Wiersz szacowania** w Dataverse. Te rekordy szacowania mają klasę transakcji, **Koszt** i są synchronizowane z rekordami prognozy wydatków w aplikacjach finansowych i operacyjnych przy użyciu encji **integracji Project Operations dla szacowania wydatków (msdynesti\_estimatelines)**.

   ![Integracja szacunków wydatków.](./Media/DW4ExpenseEstimates.png)

Podwójny zapis synchronizuje rekordy prognozy wydatków do tabeli inscenizacji **ProjCDSEstimateExpenseImport)**, a następnie wykorzystuje logikę biznesową do tworzenia i aktualizacji rekordów prognozy wydatków (**ProjForecastCost**). W wierszach szacowania są przechowywane oddzielnie rekordy szacowania sprzedaży i szacowania wydatków. Logika biznesowa w aplikacjach finansowych i operacyjnych wypełnia pojedynczy rekord prognozy wydatków, korzystając z tych szczegółów w tabeli etapowej.

Księgowy projektu może przeglądać zapisy prognozy wydatków w aplikacjach finansowych i operacyjnych, przechodząc do **Zarządzanie projektem i księgowość** > **Wszystkie projekty** > **Plan** > **Prognozy wydatków**.

## <a name="material-estimates"></a>Szacowania materiałów

Szacowanie materiałów jest tworzone przez menedżera projektu na karcie **Szacowanie materiałów** na stronie **Szczegóły projektu** w Dataverse. Rekordy szacowania materiałów są przechowywane w encji **Wiersz szacowania** w Dataverse. Te rekordy szacowania mają klasę transakcji, **Materiał** i są synchronizowane z rekordami prognozy wydatków w aplikacjach finansowych i operacyjnych przy użyciu encji **Tabela integracji projektu dla oszacowań materiałowych (msdynesti\_estimatelines)**.

   ![Integracja szacunków materiałów.](./Media/DW4MaterialEstimates.png)

Podwójny zapis synchronizuje rekordy szacowania materiałów do tabeli inscenizacji **ProjForecastSalesImpor**, a następnie wykorzystuje logikę biznesową do tworzenia i aktualizacji rekordów prognozy Elementu (**ForecastSales**). W wierszach szacowania są przechowywane oddzielnie rekordy szacowania sprzedaży i szacowania wydatków. Logika biznesowa w aplikacjach finansowych i operacyjnych wypełnia pojedynczy rekord prognozy pozycji, korzystając z tych szczegółów w tabeli etapowej.

Księgowy projektu może przeglądać zapisy prognozy pozycji w aplikacjach finansowych i operacyjnych, przechodząc do **Zarządzanie projektem i księgowość** > **Wszystkie projekty** > **Plan** > **Prognozy pozycji**.

## <a name="project-actuals"></a>Wartości rzeczywiste projektu

Wartości rzeczywiste projektu są tworzone w Dataverse na podstawie czasu, wydatków, materiałów i działań dotyczących fakturowania. W tej encji Dataverse są przechwytywane wszystkie atrybuty operacyjne tych transakcji, w tym ilość, cena kosztów, cena sprzedaży i projekt. Aby uzyskać więcej informacji, zobacz [Wartości rzeczywiste](../actuals/actuals-overview.md). Zapisy rzeczywiste są synchronizowane z aplikacjami finansowymi i operacyjnymi przy użyciu mapy tabeli podwójnego zapisu, **wartości rzeczywistych integracji Project Operations (msdynactuals\_)** w celu dalszego księgowania.

   ![Integracja wartości rzeczywistych.](./Media/DW4Actuals.png)

Mapowanie tabeli **Integracji wartości rzeczywistych Project Operations** synchronizuje wszystkie rekordy z encji **Wartości rzeczywiste** w Dataverse z atrybutem **Pomiń synchronizację (tylko do użytku wewnętrznego)** ustawionym na wartość **False**. Ta wartość atrybutu jest ustawiana w Dataverse automatycznie podczas tworzenia rekordu. Przykłady, w których ten atrybut ma wartość **True**:

  - Wartości rzeczywiste kosztu projektu dla transakcji międzyfirmowych. Aby uzyskać więcej informacji, zobacz temat [Tworzenie transakcji międzyfirmowych](../project-accounting/create-intercompany-transactions.md). Rekordy te są pomijane, ponieważ system odtwarza rzeczywisty koszt projektu w aplikacjach finansowych i operacyjnych w momencie zaksięgowania faktury sprzedawcy wewnętrznego.
  - Negatywny zapis sprzedaży niefakturowanej tworzony w momencie potwierdzenia faktury proforma. Rekordy te są pomijane, ponieważ księga pomocnicza projektu w aplikacjach finansowych i operacyjnych nie odwraca niefakturowanego rekordu sprzedaży w momencie wystawiania faktury, lecz zmienia status na całkowicie zafakturowany.

Mapa tabeli podwójnego zapisu synchronizuje rekordy wartości rzeczywistych z tabelą etapu **ProjCDSActualsImport**. Rekordy te są przetwarzane przez proces okresowy **Import z tabeli etapu** podczas tworzenia linii dziennika integracji Project Operations oraz linii propozycji faktur projektowych. Aby uzyskać więcej informacji, zobacz temat [Integracja dziennika w Project Operations](../project-accounting/project-operations-integration-journal.md).

W Dataverse są również przechwytywane łącza między rzeczywistymi transakcjami w encji **Połączenie transakcji**. Aby uzyskać więcej informacji, zobacz temat [Łączenie wartości rzeczywistych z oryginalnymi rekordami](../actuals/linkingactuals.md). Powiązania między rzeczywistymi transakcjami są również synchronizowane z aplikacjami finansowymi i operacyjnymi za pomocą mapy tabeli z podwójnym zapisem, **encji Integracja dla transakcji projektu relacje (msdyn\_transactionconnections)**. Rekordy te są używane przez proces okresowy **Import z tabeli etapu** podczas tworzenia linii dziennika integracji Project Operations oraz linii propozycji faktur projektowych.

Zaksięgowanie dziennika integracji Project Operations i oferty faktury projektu powoduje wyzwolenie aktualizacji w odpowiednich rekordach tabeli etapu **ProjCDSActualsImport**. W systemie są przechwytywane i rejestrowane następujące atrybuty księgowe dla transakcji rzeczywistych:

- Kwota w walucie księgowej
- Kurs wymiany
- Numer załącznika
- Kwota podatku

Tabela mapowania **Integracji wartości rzeczywistych Project Operations** aktualizuje odpowiednie rekordy wartości rzeczywistych w Dataverse tymi informacjami.
