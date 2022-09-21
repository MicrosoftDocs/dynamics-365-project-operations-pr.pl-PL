---
title: Zmiany funkcji od Project Service Automation do Project Operations
description: Ten artykuł zawiera omówienie zmian funkcji z rozwiązania Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459940"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Zmiany funkcji od Project Service Automation do Project Operations

Uaktualnienie z wersji Dynamics 365 Project Service Automation do Dynamics 365 Project Operations Lite zostanie dostarczone na trzech etapach. Ten artykuł zawiera informacje na temat głównych zmian, których można się spodziewać po zakończeniu uaktualniania.

| Dostarczanie uaktualnienia | Faza 1 <br>(Styczeń 2022) | Faza 2 <br>(Listopad 2022) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Brak zależności od struktury podziału pracy (WBS) dla projektów. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS jest uwzględniony w aktualnie obsługiwanych limitach Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS poza obecnie obsługiwanymi limitami Project Operations, w tym obsługa klienta pulpitu programu Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Zarządzanie projektem

Najważniejsze zmiany, jakie odczuje użytkownik, to obszar planowania projektów. Project Operations to nowe, nowocześniej dostępne środowisko do zarządzania strukturą struktury podziału pracy (WBS) dzięki wykorzystaniu funkcji planowania dostarczanych przez [program Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Różnice w funkcjach planowania

W poniższej tabeli można podsumować różnice między Project Service Automation a Project Operations.

|  Planowanie     |   Project Operations   |   Pomoc medyczna   |
|-----------------|------------------------|---------|
| Szablony projektu — możliwość definiowania i stosowania szablonów projektów podczas tworzenia projektu  |  &nbsp;    | :heavy_check_mark: |
| Integracja struktury organizacyjnej prac nad projektem z klientem stacjonarnym   |    &nbsp;  | :heavy_check_mark: |
| Ograniczenia — rozpocznij nie wcześniej niż, zakończ nie później niż  | :heavy_check_mark: |   &nbsp;  |
| Punkty kontrolne — Zadania z zerowym czasem trwania   | :heavy_check_mark:  |  &nbsp;  |
| Zadania oparte na zasobach będą respektować dostępność przypisanych zasobów   | :heavy_check_mark: |  &nbsp;    |
| Edytowanie etapami — edytowanie planów i praca z dnia na dzień   |   &nbsp;  | :heavy_check_mark: |
| Automatyczne/ręczne planowanie — użycie aparatu planowania projektów do automatycznego lub ręcznego planowania zadań |  &nbsp; | :heavy_check_mark:  |
| Edytowanie dużych projektów bezpośrednio w interfejsie użytkownika: Nie ma ograniczenia rozmiaru planów, które można edytować  | Ograniczenie do 500 zadań  | :heavy_check_mark:       |
| Procent realizacji — Oznacz postęp zadania   | :heavy_check_mark:  |  &nbsp;  |
| [Tryby harmonogramu projektu](../project-management/scheduling-modes.md) — projektu należy zdefiniować jako stałe jednostki, stały nakład pracy lub stały czas trwania | :heavy_check_mark: | &nbsp; |
| Oś czasu — tworzenie i dostosowywanie widoku osi czasu w celu wizualizacji szczegółów harmonogramu i komunikowania się z interesariuszami. | :heavy_check_mark:  | &nbsp; |
| Zadania oparte na nakładach pracy — obsługa aparatu planowania planowania zadań w sposób oparty na działaniach  | :heavy_check_mark:  | &nbsp; |
| **Okno dialogowe** Informacje o zadaniu — Zapisywanie szczegółów zadania przy użyciu okna dialogowego | :heavy_check_mark:  |  &nbsp;  |
| Przeciągnij i upuść — zadania zaznaczane wiele osób i modyfikowanie ich pozycji w SPP | :heavy_check_mark: | &nbsp;  |
| Elastyczne widoki widoków zadań — definiowanie bardziej ziarnistych widoków atrybutów zadań   | :heavy_check_mark:  | &nbsp; |
| Sortowanie i filtrowanie SPP  | :heavy_check_mark:  | &nbsp; |
| Widok kaskadowy w celu realizacji projektu bez wydychanych obrazów  | :heavy_check_mark:   | &nbsp; |
| Widok osi czasu — interakcyjny wykres tt używany do wizualizacji i edycji SPP   | :heavy_check_mark:  | &nbsp; |
| Skróty klawiaturowe — używanie skrótów klawiaturowych do typowych operacji, takich jak wcięcie lub wstawianie  | :heavy_check_mark:  |  &nbsp; |
| Cofnij wieloetapowy — wykonywanie analizy typu what-if, aby w pełni zrozumieć wpływ zmian przez cofnięcie i ponowne wykonywanie całego zestawu operacji | :heavy_check_mark: | &nbsp; |
| Wytnij/Kopiuj/Wklej — Współpracuj przy opracowywaniu harmonogramu, kopiując i wklejając szczegóły harmonogramu między aplikacjami  | :heavy_check_mark: | &nbsp; |
| Listy kontrolne zadań — dodawanie do zadania maksymalnie 20 pozycji listy kontrolnej   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planowanie projektu

Strona **Projekt** w Project Operations zawiera dużą liczbę **różnic w porównaniu ze stroną Projekt** w automatyzacji usługi Project Service Automation.

Następujące akcje zostały usunięte ze strony **Projekty** w ramach uaktualniania 1 etapu:

  - **Otwórz w programie MS Project**
  - **Utwórz szablon**
  - **Odłącz od programu MS Project**

Strona **Projekt** w Project Operations zawiera następujące nowe karty.

- **Szacowania materiałów**
- **Ustawienie rozliczeń zadań**

Karta **Stan** została usunięta, a **pole Stan** znajduje się teraz na karcie **Podsumowanie** w trybie planowania projektu.

   ![Aktualizacje strony Projekt.](media/projectform.png)

Nazwa **karty** Harmonogram została zmieniona **na karta Zadanie**. W aplikacji Project for the Web są dostępne nowe funkcje planowania projektów.

   ![Karta Nowe zadania projektu.](media/tasktab.png)

## <a name="scheduling-modes"></a>Tryby planowania

Project Operations wprowadzono nową funkcję — tryby [planowania](../project-management/scheduling-modes.md). Wszystkie istniejące projekty rozwiązania Project Service Automation będą domyślnie mieć wartość **Stały czas trwania** w Project Operations. Domyślną wartością nowych projektów można jednak zarządzać, przechodząc do **Ustawienia** > **Parametry** > **Parametr** > **Tryb planowania**.

   ![Ustawienia parametru Projekt dla trybu Harmonogram.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Ograniczenia planowania projektu

Project Operations są wykonywane na platformie Project for the Web i są wykonywane wszystkie operacje planowania projektów. Project for the Web zarządza strukturą podziału pracy przy użyciu ograniczeń określonych w poniższej tabeli.

| **Pole**                                          | **Limit**             |
|----------------------------------------------------|-----------------------|
| Maksymalna łączna liczba zadań projektu                  | 500                   |
| Maksymalny całkowity czas trwania projektu               | 3650 dni (10 lat)  |
| Maksymalne całkowite zasoby na projekt              | 300                   |
| Maksymalna łączna liczba linków (tylko następca) dla projektu | 600                   |
| Maksymalna łączna liczba pól niestandardowych dla projektu          | 10                    |
| Maksymalny poziom hierarchii                            | 10 poziomów             |
| Maksymalna liczba linków (następca + poprzednik)            | 20                    |
| Maksymalny czas trwania zadania podczas realizacji                      | 1250 dni             |
| Maksymalny czas trwania zadania podsumowującego                 | 3650 dni (10 lat)  |
| Maksymalne zasoby przypisane do zadania               | 20 zasobów          |
| Obsługiwany zakres dat dla zadania                    | 1/1/2000 - 31/12/2149 |
| Pozycje listy kontrolnej                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Rozszerzanie i opracowywanie planowania projektów

Po uaktualnieniu do Project Operations należy użyć interfejsów API planowania projektów do wykonywania operacji tworzenia, aktualizowania i usuwania dla następujących encji:

|   Nazwa encji           |   Logiczna nazwa encji       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Zadanie projektu            | msdyn_projecttask           |
| Zależność zadania projektu | msdyn_projecttaskdependency |
| Przypisanie zasobu     | msdyn_resourceassignment    |
| Zasobnik projektu          | msdyn_projectbucket         |
| Członek zespołu projektu     | msdyn_projectteam           |

Jeśli obecnie są dostępne dostosowania dotyczące tych encji, [zobacz interfejsy API](../project-management/schedule-api-preview.md) harmonogramu projektów w celu wykonywania operacji z encji planowania wytycznymi dotyczących implementacji.

## <a name="data-model-changes"></a>Zmiany modelu danych

W ramach 1. etapu uaktualnienia istnieją zmiany w modelu danych. Te zmiany to głównie zmiany pól w istniejących encji. Na etapie 1 encje, **msydn_project** i **msdyn_projectteam** są ponowną modyfikacją dostosowań. 

> [!IMPORTANT]
> Ta sekcja będzie uaktualniana o dodatkowe encje na etapie przyszłego uaktualniania.

Poniższe pola zostały zastąpione nowymi polami.

|   Jednostka          |   Stara nazwa logiczna   |   Nowa nazwa logiczna    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Dodano następujące pola.

|   Jednostka          |   Nazwa logiczna                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Pokazuje agregację rzeczywistych obrotów opłat w projekcie. Wyłącznie do użytku w Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Pokazuje sumę rzeczywistych kosztów materiałów w projekcie. Wyłącznie do użytku w Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Pokazuje agregację rzeczywistych obrotów materiałowych w projekcie. Wyłącznie do użytku w Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Linia kontraktu powiązana z tym projektem. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | To jest wewnętrzne pole systemowe używane do **Kopiuj projekt** powiązanego z identyfikatorem korelacji. Wyłącznie do użytku w Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | To jest wewnętrzne pole systemowe używane do **Kopiuj projekt** powiązanego z identyfikatorem sesji. Wyłącznie do użytku w Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Ostatnia synchronizacja xRM Globalnego tokenu poprawki z usługi planowania projektów. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokument programu Microsoft Project należący do projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Suma planowanych kosztów materiałów w projekcie. Wyłącznie do użytku w Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Suma planowanych sprzedaży materiałów w projekcie. Wyłącznie do użytku w Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program, z którym jest powiązany ten projekt. |
| msdyn_project     | msdyn_quotelineproject                       | Wiersz wyceny powiązany z tym projektem. |
| msdyn_project     | msdyn_replaylogheader                        | Nagłówek dzienników powtórek. |
| msdyn_project     | msdyn_schedulemode                           | Domyślny tryb planowania używany do wszystkich zadań w projekcie.  |
| msdyn_project     | msdyn_taskearlieststart                      | Najwcześniejsza data rozpoczęcia któregokolwiek zadania w projekcie.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Pokazuje członka zespołu projektu, z którego został skopiowany ten członek zespołu projektu. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Wskaż, czy utworzyć wymaganie zasobu dla nowo utworzonego ogólnego członka zespołu.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status usunięcia członka zespołu, który ma być śledzony, czy żądanie usunięcia zostało wysłane do usługi planowania projektu i czy pomyślnie odeśle odpowiedź z powrotem w oczekiwanym przedziale czasowym. |
| msdyn_projectteam | msdyn_effortcompleted                        | Rejestruje nakład pracy członka zespołu w przypisanych mu zadaniach. |
| msdyn_projectteam | msdyn_effortremaining                        | Śledzi wysiłek, który członek zespołu musi jeszcze wykonać w ramach swoich zadań. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Okres oczekiwania, od kiedy członek zespołu wysyła żądanie usuwania do usługi planowania projektów do momentu, gdy członek zespołu zostanie w rzeczywistości usunięty Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Sygnatura czasowa do zarejestrowania, kiedy żądanie usunięcia członka zespołu jest wysyłane do usługi planowania projektu. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Pokazuje członka zespołu projektu, z którego został skopiowany ten członek zespołu projektu.  |

## <a name="project-templates"></a>Szablony projektów

Project Operations nie obsługują szablonów projektów. Można jednak replikować wiele podstawowych funkcji przy użyciu interfejsu [API kopii projektu](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Obsługa dodatków stacjonarnych

Pomoc techniczna dodatku Pulpit programu Microsoft Project nie będzie dostępna na pierwszych dwóch etapach uaktualniania. W etapie 3 klienci, którzy mają projekty większe niż obsługiwane obecnie ograniczenia programu Project for the Web, będą mogli używać dodatku stacjonarnego.

## <a name="editing-resource-assignment-contours"></a>Edytowanie przypisań do zasobów

Możliwość edytowania konturów przydziału zasobów będzie dostępna, gdy dostępna będzie faza 2 aktualizacji.

## <a name="billing-and-pricing"></a>Rozliczenia i ceny

W programie Project Operations dodano następujące nowe funkcje. Funkcje te można addyować z natury i nie mają one wpływu na model danych rozwiązania Project Service Automation.

- [Rejestrowanie użycia materiałów w projektach i zadaniach projektów](../material/material-usage-log.md)
- [Zarządzanie podumowami](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrakty oparte na zaliczkach i zatrzymaniach](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontraktowanie nieprzekraczalnego stanu i weryfikacji](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Rozliczenia oparte na zadaniach](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Przestarzałe składniki

W poniższych tabelach przedstawiono wszystkie przestarzałe pola, które zostały przeniesione do przestarzałego rozwiązania składników po uaktualnieniu. Więcej informacji i łącze do rozwiązania można znaleźć w części [Dynamics 365 Project Service Automation 3x to Project Operations 4x przestarzałe składniki](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Pola                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

