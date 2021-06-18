---
title: Integracja danych instalacji i konfiguracji aplikacji Project Operations
description: Ten temat zawiera informacje dotyczące ustawienia i konfigurowania mapowania podwójnego zapisu w Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001079"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integracja danych instalacji i konfiguracji aplikacji Project Operations

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat zawiera informacje na temat integracji podwójnego zapisu w Project Operations dla encji konfiguracji i ustawień.

## <a name="project-contracts-contract-lines-and-projects"></a>Kontrakty projektu, wiersze kontraktu i projekty

Kontrakty projektów, wiersze kontraktu i projekty są tworzone w Dataverse i synchronizowane z aplikacjami Finance and Operations na potrzeby dodatkowego rozliczenia. Rekordy w tych encjach można tworzyć i usuwać tylko w programie Dataverse. Można jednak dodać do tych rekordów w aplikacjach Finance and Operations atrybuty księgowe, takie jak domyślne ustawienia grupy podatku sprzedaży oraz rozmiary finansowe.

  ![Pojęcia integracji kontraktu projektu](./media/1ProjectContract.jpg)

Potencjalni klienci w sprzedaży, szanse sprzedaży i oferty są śledzone w Dataverse i te dane nie są synchronizowane z aplikacjami Finance and Operations, ponieważ z tym działaniem nie jest skojarzona żadna księgowa wartość.

Funkcja kontraktu projektu w Dataverse umożliwia utworzenie rekordu kontraktu projektu w aplikacjach Finance and Operations przy użyciu mapowania tabeli **nagłówków kontraktu projektu (salesorders)**. Zapisanie kontraktu projektu w Dataverse także rozpoczyna tworzenie rekordu encji klienta kontraktu projektu. Ten rekord jest synchronizowany z aplikacjami Finance and Operations, używając mapowania tabeli **źródła finansowania w projekcie (msdyn\_projectcontractsspbillingrules)**. Na tym mapowaniu są również synchronizowane dodatki, aktualizacje i usunięcia klientów kontraktu projektu. Podział wartości procentowych rozliczania między klientów kontraktów projektów jest opanowany tylko w Dataverse i nie jest synchronizowany z aplikacjami Finance and Operations.

Po utworzeniu umowy projektowej w Dataverse, księgowy projektu może zaktualizować atrybuty księgowe dla tej umowy projektowej w aplikacjach Finance and Operations przechodząc do **zarządzanie projektem i księgowość** > **Kontrakty projektu** > **Ustawienie** > **Pokaż domyślne wartości księgowe**. Księgowy może przejrzeć operacyjne atrybuty umowy projektowej, takie jak żądana data dostawy i kwota umowy, wybierając identyfikator umowy projektowej w aplikacji Finance and Operations, która otwiera powiązany rekord umowy projektowej w Dataverse.

Encja projektu jest synchronizowana z aplikacjami Finance and Operations, używając mapowania tabeli **Projektów V2 (msdyn\_** projects). Konto klienta projektu może:

  - Przejrzyj projekty w aplikacjach Finance and Operations, przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty**. 
  - Aktualizuj atrybuty księgowe projektu w aplikacjach Finance and Operations, przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Konfigurowanie** > **Pokaż domyślne ustawienia księgowe**.  
  - Przejrzyj atrybuty operacyjne projektu, takie jak szacowane daty rozpoczęcia i zakończenia, wybierając identyfikator projektu w aplikacjach Finance and Operations, które otwierają rekord pokrewny projektu w chmurze w Dataverse.

Projekt jest skojarzony z kontraktem projektu za pośrednictwem encji **Wiersz kontraktu projektu**.

Wiersze kontraktu projektu w Dataverse umożliwiają utworzenie zasady rozliczania w aplikacjach Finance and Operations przy użyciu mapowania tabeli **Wierszy kontraktu projektu (salesordersdetails)**. Metoda rozliczania definiuje typ reguły rozliczania kontraktu projektu w aplikacjach Finance and Operations:

  - Wiersze kontraktu projektu z metodą rozliczania czasu i materiałów tworzą regułę rozliczania typu czas i materiał.
  - Linie kontraktowe metody rozliczeń wg stałej ceny tworzą regułę rozliczeń wg etapów.

Linie umów projektowych mogą być przeglądane przez księgowego projektu w aplikacji Finance and Operations poprzez przejście do **Zarządzanie projektem i księgowość** > **Kontrakty projektowe** > **Ustawianie** > **Pokaż domyślne księgowanie**, a następnie przegląd szczegółów na zakładce **Linie umów**. Na tej zakładce księgowy może również ustawić domyślne wymiary finansowe dla linii umów rozliczanych metodą stałej ceny.

## <a name="billing-milestones"></a>Punkty kontrolne rozliczenia

Wiersze kontraktu projektu przy użyciu metody rozliczania o stałej cenie są zafakturowane za pośrednictwem punktów kontrolnych rozliczania. Punkty kontrolne rozliczania są synchronizowane z transakcjami konta projektu w aplikacjach Finance and Operations przy użyciu mapowania tabeli **punktów kontrolnych integracji Project Operations z linią kontraktów (msdyn\_contractlinescheduleofvalues)**.

  ![Integracja punktów kontrolnych rozliczenia](./media/2Milestones.jpg)

Księgowy może przeglądać transakcje konta i dostosowywać atrybuty księgowe tych transakcji, przechodząc do **Zarządzanie projektami i księgowość** > **Kontrakty projektów** > **Zarządzanie** > **Transakcje na rachunku** lub **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Zarządzanie** > **Transakcje na rachunku**.

Podczas pierwszego tworzenia etapu rozliczeniowego dla danej linii kontraktowej projektu, system automatycznie tworzy projekt estymacji przychodów w stałej cenie dla projektu powiązanego z tą linią kontraktową. Projekty szacowania przychodów o stałej cenie można przeglądać, przechodząc do **Zarządzania projektami i księgowości** > **Projekty dotyczące prognozy dochodów po stałej cenie**.

### <a name="project-tasks"></a>Zadania projektu

Zadania projektu są synchronizowane z aplikacjami Finance and Operations za pośrednictwem tabeli zadań projektu **(msdyn\_projecttasks)** wyłącznie dla celów referencyjnych. Operacje tworzenia, aktualizowania i usuwania nie są obsługiwane za pośrednictwem aplikacji Finance and Operations.

  ![Integracja zadań projektowych](./media/3Tasks.jpg)

## <a name="project-resources"></a>Zasoby projektu

Encja **Role zasobów projektu** jest synchronizowana z aplikacjami Finance and Operations, używając **Role zasobów projektowych dla wszystkich firm (bookableresourcecategories)** tylko dla celów referencyjnych. Ponieważ role zasobów w Dataverse nie są specyficzne dla firmy, system automatycznie tworzy w aplikacjach Finance and Operations rekordy odpowiednich ról zasobów specyficznych dla firmy dla wszystkich podmiotów prawnych uwzględnianych w zakresie integracji podwójnego zapisu.

![Integracja ról zasobów](./media/5Resources.jpg)

Zasoby projektu w Project Operations są utrzymywane w Dataverse i nie są synchronizowane z aplikacjami Finance and Operations.

### <a name="transaction-categories"></a>Kategorie transakcji

Kategorie transakcji są zachowywane w Dataverse i synchronizowane z aplikacjami Finance and Operations przy użyciu kategorii transakcji projektu **(msdyn\_transactioncategories)**. Po zsynchronizowaniu rekordu kategorii transakcji system automatycznie tworzy cztery rekordy kategorii udostępnionych. Każdy rekord odpowiada typowi transakcji w aplikacjach Finance and Operations i łączy je z rekordem kategorii transakcji.

![Integracja kategorii transakcji](./media/4TransactionCategories.jpg)

Korzystanie z kategorii transakcji do szacowania i wartości rzeczywistych wymaga, aby księgowy projektu lub systemowy administrator utworzył odpowiednie kategorie projektu w każdym podmiocie prawnym. Aby uzyskać więcej informacji, zobacz [Konfigurowanie kategorii projektu](../project-accounting/configure-project-categories.md).
