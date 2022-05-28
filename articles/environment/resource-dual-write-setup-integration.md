---
title: Integracja danych instalacji i konfiguracji aplikacji Project Operations
description: Ten temat zawiera informacje dotyczące ustawienia i konfigurowania mapowania podwójnego zapisu w Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586909"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integracja danych instalacji i konfiguracji aplikacji Project Operations

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat zawiera informacje na temat integracji podwójnego zapisu w Project Operations dla encji konfiguracji i ustawień.

## <a name="project-contracts-contract-lines-and-projects"></a>Kontrakty projektu, wiersze kontraktu i projekty

Umowy projektowe, linie kontraktowe i projekty są tworzone w Dataverse i synchronizowane z aplikacjami finansowymi i operacyjnymi w celu dodatkowego księgowania. Rekordy w tych encjach można tworzyć i usuwać tylko w programie Dataverse. Jednak atrybuty księgowe, takie jak domyślne grupy podatku od sprzedaży i wymiary finansowe, można dodać do tych rekordów w aplikacjach finansowych i operacyjnych.

  ![Pojęcia integracji kontraktu projektu.](./media/1ProjectContract.jpg)

Potencjalni klienci działań sprzedaży, szanse sprzedaży i oferty są śledzone w Dataverse i nie są synchronizowane z aplikacjami finansowymi i operacyjnymi, ponieważ z tymi działaniami nie jest związana żadna księgowość.

Funkcja umowy projektowej w Dataverse tworzy rekord umowy projektowej w aplikacjach finansowych i operacyjnych przy użyciu mapy tabeli **Nagłówki umów projektowych (zamówienia sprzedaży)**. Zapisanie kontraktu projektu w Dataverse także rozpoczyna tworzenie rekordu encji klienta kontraktu projektu. Ten rekord jest synchronizowany z aplikacjami finansowymi i operacyjnymi za pomocą mapy tabeli **Źródło finansowania projektu (msdyn\_projectcontractssplitbillingbrules)**. Na tym mapowaniu są również synchronizowane dodatki, aktualizacje i usunięcia klientów kontraktu projektu. Podział procentowy rozliczeń między klientów kontraktu projektowego jest dostępny tylko w Dataverse i nie jest synchronizowany z aplikacjami finansowymi i operacyjnymi.

Po utworzeniu umowy dotyczącej projektu w Dataverse księgowy projektu może zaktualizować atrybuty księgowe dla tej umowy w aplikacjach finansowych i operacyjnych, przechodząc do **Zarządzanie projektami i księgowość** > **Umowy dotyczące projektów** > **Konfiguracja** > **Pokaż domyślną księgowość**. Księgowy może przejrzeć atrybuty operacyjne umowy projektowej, takie jak żądana data dostawy i kwota umowy, wybierając identyfikator umowy projektowej w aplikacjach finansowych i operacyjnych, co powoduje otwarcie powiązanego rekordu umowy projektowej w Dataverse.

Encja projektu jest synchronizowana z aplikacjami finansowymi i operacyjnymi przy użyciu mapowania tabeli **projektów V2 (msdyn\_projects)**. Konto klienta projektu może:

  - Przejrzyj projekty w aplikacjach finansowych i operacyjnych, przechodząc do **Zarządzanie projektami i księgowość** > **Wszystkie projekty**. 
  - Zaktualizuj atrybuty księgowe dla projektu w aplikacjach finansowych i operacyjnych, przechodząc do **Zarządzanie projektem i księgowość** > **Wszystkie projekty** > **Ustaw** > **Pokaż domyślną księgowość**.  
  - Przejrzyj atrybuty operacyjne projektu, takie jak szacowane daty rozpoczęcia i zakończenia, wybierając identyfikator projektu w aplikacjach finansowych i operacyjnych, które otwierają powiązany rekord projektu w chmurze Dataverse.

Projekt jest skojarzony z kontraktem projektu za pośrednictwem encji **Wiersz kontraktu projektu**.

Linie umowy projektowej w Dataverse tworzy regułę rozliczania umowy projektowej w aplikacjach finansowych o operacyjnych przy użyciu mapy tabeli **Project contract lines (salesorderdetails)**. Metoda rozliczania definiuje typ reguły rozliczania kontraktu projektu w aplikacjach finansowych i operacyjnych:

  - Wiersze kontraktu projektu z metodą rozliczania czasu i materiałów tworzą regułę rozliczania typu czas i materiał.
  - Linie kontraktowe metody rozliczeń wg stałej ceny tworzą regułę rozliczeń wg etapów.

Linie umów projektu mogą być przeglądane przez księgowego projektu w aplikacjach finansowych i operacyjnych poprzez przejście do **Zarządzanie projektem i księgowość** > **Kontrakty projektu** > **Ustawianie** > **Pokaż domyślne księgowanie** i przejrzenie szczegółów na karcie **Linie umów**. Na tej karcie księgowy może również ustawić domyślne wymiary finansowe dla linii umów rozliczanych metodą stałej ceny.

## <a name="billing-milestones"></a>Punkty kontrolne rozliczenia

Wiersze kontraktu projektu przy użyciu metody rozliczania o stałej cenie są zafakturowane za pośrednictwem punktów kontrolnych rozliczania. Punkty kontrolne rozliczeń są synchronizowane z transakcjami na koncie w aplikacjach finansowych i operacyjnych przy użyciu mapy tabeli **punkty kontrolne wiersza kontraktu Project Operations Integration (msdyn\_contractlinescheduleofvalues)**.

  ![Integracja punktów kontrolnych rozliczenia.](./media/2Milestones.jpg)

Księgowy może przeglądać transakcje konta i dostosowywać atrybuty księgowe tych transakcji, przechodząc do **Zarządzanie projektami i księgowość** > **Kontrakty projektów** > **Zarządzanie** > **Transakcje na rachunku** lub **Zarządzanie projektami i księgowość** > **Wszystkie projekty** > **Zarządzanie** > **Transakcje na rachunku**.

Podczas pierwszego tworzenia etapu rozliczeniowego dla danej linii kontraktowej projektu, system automatycznie tworzy projekt estymacji przychodów w stałej cenie dla projektu powiązanego z tą linią kontraktową. Projekty szacowania przychodów o stałej cenie można przeglądać, przechodząc do **Zarządzania projektami i księgowości** > **Projekty dotyczące prognozy dochodów po stałej cenie**.

### <a name="project-tasks"></a>Zadania projektu

Zadania projektowe są zsynchronizowane z aplikacjami finansowymi i operacyjnymi za pośrednictwem **Zadania projektowe (msdyn\_projecttasks)** mapa tabeli tylko do celów referencyjnych. Tworzenie, aktualizowanie i usuwanie operacji nie jest obsługiwane przez aplikacje finansowe i operacyjne.

  ![Integracja zadań projektowych.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Zasoby projektu

Podmiot **Role zasobów projektu** jest zsynchronizowany z aplikacjami finansowymi i operacyjnymi za pomocą mapy tabeli **Role zasobów projektu dla wszystkich firm (bookableresourcecategories)** tylko do celów referencyjnych. Ponieważ role zasobów w Dataverse nie są specyficzne dla firmy, system automatycznie tworzy odpowiednie rekordy ról zasobów specyficznych dla firmy w aplikacjach finansowych i operacyjnych dla wszystkich osób prawnych objętych zakresem integracji podwójnego zapisu.

![Integracja ról zasobów.](./media/5Resources.jpg)

Zasoby projektu w Project Operations są utrzymywane w Dataverse i nie są synchronizowane z aplikacjami finansowymi i operacyjnymi.

### <a name="transaction-categories"></a>Kategorie transakcji

Kategorie transakcji są przechowywane w Dataverse i synchronizowane z aplikacjami finansowymi i operacyjnymi za pomocą mapy tabelarycznej **Kategorie transakcji projektu (msdyn\_transactioncategories)**. Po zsynchronizowaniu rekordu kategorii transakcji system automatycznie tworzy cztery rekordy kategorii udostępnionych. Każdy rekord odpowiada typowi transakcji w aplikacjach finansowych i operacyjnych i łączy je z rekordem kategorii transakcji.

![Integracja kategorii transakcji.](./media/4TransactionCategories.jpg)

Korzystanie z kategorii transakcji do szacowania i wartości rzeczywistych wymaga, aby księgowy projektu lub systemowy administrator utworzył odpowiednie kategorie projektu w każdym podmiocie prawnym. Aby uzyskać więcej informacji, zobacz [Konfigurowanie kategorii projektu](../project-accounting/configure-project-categories.md).
