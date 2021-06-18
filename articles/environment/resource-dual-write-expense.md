---
title: Integracja zarządzania wydatkami
description: Ten temat zawiera informacje na temat integracji raportu wydatków w Project Operations przy użyciu podwójnego zapisu.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7fff69f062bf09fe7ceca61d951b535d2e010bfd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999999"
---
# <a name="expense-management-integration"></a>Integracja zarządzania wydatkami

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Ten temat zawiera informacje na temat integracji raportu wydatków w Project Operations [wdrożenie wszystkich wydatków](../expense/expense-overview.md) przy użyciu podwójnego zapisu.

## <a name="expense-categories"></a>Kategorie wydatków

W przypadku pełnego wdrożenia wydatków kategorie wydatków są tworzone i utrzymywane w aplikacjach Finance and Operations. Aby utworzyć nową kategorię wydatków, należy wykonać następujące kroki:

1. W Microsoft Dataverse utwórz kategorię **transakcja**. Integracja z podwójnym zapisem zsynchronizuje kategorię transakcji z aplikacjami Finance and Operations. Aby uzyskać więcej informacji, zobacz [konfigurowanie kategorii projektu](/dynamics365/project-operations/project-accounting/configure-project-categories) oraz [konfigurowanie Project Operations i konfiguracja integracji danych](resource-dual-write-setup-integration.md). W wyniku tej integracji system tworzy cztery rekordy kategorii udostępnionych w aplikacjach Finance and Operations.
2. W Finance wybierz **Zarządzanie wydatkami** > **Konfiguracja** > **Kategorie współdzielone** i wybierz kategorię współdzieloną z klasą transakcji **Wydatek**. Ustaw parametr **Może być używany wydatkach** na wartość **True** i zdefiniuj typ wydatku, który ma być używany.
3. Przy użyciu tego rekordu kategorii udostępnionej utwórz nową kategorię wydatków, przechodząc do **Zarządzanie kosztami** > **Konfiguracja** > **Kategorie wydatków** i wybierz opcję **Nowa**. Po zapisaniu rekordu podwójny zapis używa mapowania tabeli, **Kategorii wydatków integracji Project Operations — encji eksportowania (msdyn\_expensecategories)** w celu synchronizacji tego rekordu z rekordem Dataverse.

  ![Integracja kategorii wydatków](./media/DW6ExpenseCategories.png)

Kategorie wydatków w aplikacjach Finance and Operations są specyficzne dla firmy lub podmiotu prawnego. Są dostępne oddzielne, specyficzne dla podmiotu prawnego rekordy Dataverse. Kiedy kierownik projektu szacuje wydatki, nie może wybrać kategorii wydatków, które zostały utworzone dla projektu należącego do innej firmy niż ta, która jest właścicielem projektu, nad którym pracuje. 

## <a name="expense-reports"></a>Raporty z wydatków

Raporty o wydatkach są tworzone i zatwierdzone w aplikacjach Finance and Operations. Aby uzyskać więcej informacji, zobacz temat [Tworzenie i przetwarzanie raportów o wydatkach w programie Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Po zatwierdzeniu raportu wydatków przez menedżera projektu jest on publikowany w księdze głównej. W Project Operations wiersze raportu dotyczące wydatków związane z projektem są publikowane przy użyciu specjalnych reguł publikowania:

  - Koszty związane z projektem (w tym podatek niepodlegający zwrotowi) nie są natychmiast księgowane na koncie kosztów projektu w księdze głównej, lecz na koncie integracji kosztów. To konto jest skonfigurowane w **Zarządzanie projektami i księgowanie** > **Konfiguracja** > **Zarządzanie parametrami projektów i księgowania**, **Project Operations w Dynamics 365 Customer Engagement**.
  - Funkcja podwójnego zapisu synchronizuje z Dataverse za pomocą mapowania tabeli **Integrowania wydatków projektu w Project Operations z encjami eksportu (msdyn \_expenses)**.
  - Księgę pomocniczą podatków, księgę pomocniczą dostawców i inne księgowania finansowe rejestruje się odpowiednio w momencie księgowania raportu wydatków.

  ![Integracja raportów wydatków](./media/DW6ExpenseReports.png)

Po wpisie rekordu w encji **Wydatki** w Dataverse, system uruchamia zautomatyzowany proces zatwierdzania rekordu. W razie potrzeby można przejrzeć stan procesu zautomatyzowanego zatwierdzania w Dataverse, przechodząc do strony **Zaawansowane ustawienia** > **System** > **Zadania systemowe**. Po zakończeniu zatwierdzania rekordy klasy transakcji wydatków są tworzone w encji **Wartości rzeczywiste**.

Wartości rzeczywiste związane z wydatkami są następnie przetwarzane przy użyciu podwójnego zapisu tabeli mapowania **Wartości rzeczywistych integracji z Project Operations (msdyn\_actuals)**. Aby uzyskać więcej informacji, zobacz [Szacunki projektowe i wartości rzeczywiste](resource-dual-write-estimates-actuals.md).

Proces okresowy, **Import z etapów** tworzy wiersze dziennika związane z raportem wydatków w dzienniku integracji Project Operations. Domyślnym kontem rozliczeniowym jest konto integracji wydatków. Integracja z Posting powoduje wyczyszczenie salda konta dla transakcji wydatków i przeniesienie kwoty wydatku na konto kosztów projektu. System tworzy również transakcje podrzędne w ramach projektu na potrzeby fakturowania i rozpoznawania przychodów.
