---
title: Wersje map podwójnego zapisu aplikacji Project Operations
description: Ten temat zawiera listę wymaganych map podwójnego zapisu w Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939025"
---
# <a name="project-operations-dual-write-map-versions"></a>Wersje map podwójnego zapisu aplikacji Project Operations

_**Zastosowane do:** Project Operations dla zasobów/scenariuszy nieopartych na zaopatrzeniu_

Użycie Dynamics 365 Project Operations do scenariuszy z zasobami w magazynie/niemagazynowanymi wymaga uruchomienia w środowisku zestawu map podwójnego zapisu. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Wymagane mapy: Rozwiązanie aranżacji podwójnego zapisu

Następujące mapy są wymaganymi warunkami wstępnymi dla rozwiązania Project Operations. Pamiętaj, aby uruchomić mapowania wymienione w poniższej tabeli oraz dowolne mapowania tabel pokrewnych w środowisku.

| Mapowanie tabeli | Synchronizacja początkowa |
| --- | --- |
| Księga (msdyn_ledgers) | Wymaga wstępnej synchronizacji mapy tabeli i wszystkich wymagań wstępnych. Wzorzec dla synchronizacji początkowej to aplikacje Finance and Operations. |
| Firmy (cdm_companies) | Niewymagane. System wypełnia tę encję automatycznie, gdy środowiska są połączone przy użyciu funkcji podwójnego zapisu. |
| Klienci V3 (accounts) | Nie jest wymagane do inicjowania obsługi. |
| Vendors V2 (msdyn_vendors) | Nie jest wymagane do inicjowania obsługi. |

1. Z listy map wybierz mapowanie Księga **(msdyn\_ledgers)** ze wszystkimi wymaganiami wstępnymi i zaznacz pole wyboru **Synchronizacja początkowa**. W polu **Główny dla początkowej synchronizacji** wybierz **aplikacje Finance and Operations** zarówno dla mapy księgi głównej, jak i dla wszystkich map warunkowych. Wybierz **Uruchom**.

![Synchronizacja mapowania księgi](media/DW6.png)

1. Wykonaj te same kroki dla wszystkich pozostałych map tabel wymienionych w powyższej tabeli. Podczas uruchamiania tych map nie zaznaczaj pola wyboru **Synchronizacja początkowa**.

## <a name="project-operations-dual-write-maps"></a>Project Operations — mapy podwójnego zapisu

Następujące mapy są wymaganymi warunkami wstępnymi dla rozwiązania Project Operations.

| **Mapowanie encji** | **Najnowsza wersja** | **Synchronizacja początkowa** |
| --- | --- | --- |
| Encja integrująca dla transakcji projektu relacje (msdyn\_transactionconnections) | 1.0.0.0 | Nie jest wymagane do inicjowania obsługi. |
| Nagłówki kontraktów projektów (sales orders) | 1.0.0.1 | Nie jest wymagane do inicjowania obsługi. |
| Pozycje kontraktu w projekcie (salesorderdetails) | 1.0.0.0 | Nie jest wymagane do inicjowania obsługi. |
| Źródło danych projektu (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Nie jest wymagane do inicjowania obsługi. |
| Tabela integracji Project Operations dla szacowania materiałów (msdyn\_estimatelines) | 1.0.0.0 | Nie jest wymagane do inicjowania obsługi. |
| Propozycje faktury projektu V2 (invoices) | 1.0.0.2 | Nie jest wymagane do inicjowania obsługi. |
| Wartości rzeczywiste integracji Project Operations (msdyn_actuals) | 1.0.0.14 | Nie jest wymagane do inicjowania obsługi. |
| Punkty kontrolne pozycji kontraktu w integracji Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Nie jest wymagane do inicjowania obsługi. |
| Encja integracji Project Operations na potrzeby oszacowania kosztów (msdyn_estimateslines) | 1.0.0.2 | Nie jest wymagane do inicjowania obsługi. |
| Encja integracji Project Operations na potrzeby oszacowania godzinowego (msdyn_resourceassignments) | 1.0.0.5 | Nie jest wymagane do inicjowania obsługi. |
| Encja integracji kategorii wydatków projektowych Project Operations (msdyn_expensecategories) | 1.0.0.2 | Nie jest wymagane do inicjowania obsługi. |
| Encja integracji wydatków projektowych Project Operations (msdyn_expenses) | 1.0.0.2 | Nie jest wymagane do inicjowania obsługi. |
| Integracja w Project Operations encji eksportu faktury dostawcy projektu (msdyn_projectvendorinvoices) | 1.0.0.0 | Nie jest wymagane do inicjowania obsługi. |
| Integracja w Project Operations encji eksportu wiersza faktury dostawcy projektu (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Nie jest wymagane do inicjowania obsługi. |
| Role zasobów projektu dla wszystkich firm (bookableresourcecategories) | 1.0.0.1 | Wymaga wstępnej synchronizacji mapowania tabeli w celu zsynchronizowania ról zasobów Menedżer projektu i Członek zespołu, które zostały uzupełnione w środowisku usługi Dynamics 365 Dataverse podczas inicjowania obsługi administracyjnej. Dataverse jest głównym źródłem początkowej synchronizacji. |
| Zadania projektu (msdyn_projecttasks) | 1.0.0.4 | Nie jest wymagane do inicjowania obsługi. |
| Kategorie transakcji projektu (msdyn_transactioncategories) | 1.0.0.0 | Nie jest wymagane do inicjowania obsługi. |
| Projekty V2 (msdyn_projects) | 1.0.0.1 | Nie jest wymagane do inicjowania obsługi. |

Wykonaj następujące kroki, aby uruchomić wymienione mapowania.

1. Włącz role zasobów projektu dla **wszystkich firm (bookableresourcecategories)**, ponieważ to mapowanie wymaga początkowej synchronizacji. W polu **Główny dla początkowej synchronizacji** wybierz usługę **Common Data Service**. 

 ![Synchronizacja mapowania tabeli ról zasobów](media/6ResourceInitialSync.jpg)

 Przed przejściem do następnego kroku poczekaj, aż stan mapy zmieni się na **Uruchomione**.

2. Wybierz wszystkie pozostałe wymagane mapowania. Można filtrować je na liście mapy podwójnego zapisu, używając słowa kluczowego **Projekt** w wyszukiwaniu w prawym górnym rogu. Możesz zaznaczyć wszystkie mapy, a następnie uruchomić. Aby uzyskać więcej informacji, zobacz temat [Zarządzanie wieloma mapowaniami tabel](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Pamiętaj, aby włączyć i uruchomić pokrewne mapowania encji.

### <a name="project-operations-dual-write-map-versions"></a>Wersje map podwójnego zapisu aplikacji Project Operations

Zawsze uruchamiaj najnowszą wersję mapy w środowisku użytkownika. Niektóre funkcje i możliwości mogą nie działać poprawnie, jeśli istnieje któryś z następujących warunków:

- Mapowanie nie jest aktywowane.
- Najnowsza wersja mapy nie jest aktywowana. 
- Powiązane mapowania tabel nie są aktywowane.

Aktywną wersję mapy można zobaczyć w kolumnie **Wersja** na stronie **Zapis podwójny**. Aby uaktywnić nową wersję mapy, należy wybrać **Wersję mapowania tabeli**, a następnie zapisać wybraną wersję po wybraniu najnowszej wersji. Jeśli dostosowałeś niestandardową mapę tabeli, będziesz musiał ponownie zastosować zmiany. Więcej informacji: [Zarządzanie cyklem życia aplikacji](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
