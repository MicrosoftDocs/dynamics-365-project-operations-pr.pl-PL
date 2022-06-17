---
title: Dzienniki harmonogramu projektu
description: Ten artykuł zawiera informacje i próbki, które pomogą Ci wykorzystać dzienniki harmonogramu projektu do śledzenia awarii związanych z usługą harmonogramu projektu i interfejsami API harmonogramu projektu.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923708"
---
# <a name="project-scheduling-logs"></a>Dzienniki harmonogramu projektu

_**Dotyczy:** Project Operations dla scenariuszy opartych na zasobach/nieopartych na zaopatrzeniu, wdrażanie w wersji uproszczonej — od okazji do faktury pro forma_, _Project for the Web_

Microsoft Dynamics 365 Project Operations używa [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) jako swojego podstawowego aparatu planowania. Zamiast używać standardowych interfejsów programowania aplikacji (API) Microsoft Dataverse Web, Project Operations używa nowych interfejsów API Project Scheduling do tworzenia, aktualizacji i usuwania zadań projektowych, przydziałów zasobów, zależności między zadaniami, kubełków projektowych i członków zespołów projektowych. Jednakże, gdy operacje tworzenia, aktualizacji lub usuwania są uruchamiane programowo na elementach struktury podziału pracy (WBS), mogą wystąpić błędy. Aby śledzić te błędy i historię operacji, wprowadzono dwa nowe dzienniki administracyjne: **Zestaw Operacji** oraz **Project Scheduling Service (PSS)**. Aby uzyskać dostęp do tych logów, przejdź do **Ustawień** \> **Integracja harmonogramu**.

Poniższa ilustracja przedstawia model danych dla dziennika harmonogramu projektu.

![Model danych dla dzienników harmonogramu projektu.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operacja Ustaw dziennik

Dziennik Zestaw operacji śledzi wykonanie zestawu operacji, który jest używany do uruchamiania jednej lub wielu operacji tworzenia, aktualizacji lub usuwania w partii na projektach, zadaniach projektu, przydziałach zasobów, zależnościach zadań, kubełkach projektu lub członkach zespołu projektowego. Pole **Operacja w stanie** przedstawia ogólny stan zestawu operacji. Szczegóły dotyczące ładunku użytecznego zbioru operacji są przechwytywane w powiązanych rekordach szczegółów zbioru operacji.

### <a name="operation-set"></a>Zestaw operacji

Poniższa tabela przedstawia pola związane z encją **Operation Set**.

| Nazwa schematu            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Data/czas, kiedy zestaw operacji został zakończony lub zakończony niepowodzeniem.                                                | CompletedOn            |
| msdyn_correlationid   | Wartość **correlationId** wniosku.                                                                  | CorrelationId          |
| msdyn_description     | Opis zestawu operacji.                                                                        | Description            |
| msdyn_executedon      | Data/czas uruchomienia rekordu.                                                                       | Data wykonania            |
| msdyn_operationsetId  | Unikalny identyfikator instancji encji.                                                                   | OperationSet           |
| msdyn_Project         | Projekt, który jest związany z zestawem operacji.                                                            | Project                |
| msdyn_projectid       | Wartość **projectId** wniosku.                                                                      | Identyfikator ProjectId (przestarzałe) |
| msdyn_projectName     | Nie dotyczy.                                                                                              | Nie dotyczy         |
| msdyn_PSSErrorLog     | Unikalny identyfikator dziennika błędów usługi harmonogramowania projektu, który jest powiązany z zestawem operacji. | Dziennik błędów usługi PSS          |
| msdyn_PSSErrorLogName | Nie dotyczy.                                                                                              | Nie dotyczy         |
| msdyn_status          | Stan zestawu operacyjnego.                                                                             | Status                 |
| msdyn_statusName      | Nie dotyczy.                                                                                              | Nie dotyczy         |
| msdyn_useraadid       | Identyfikator obiektu Azure Active Directory (Azure AD) użytkownika, do którego należy to żądanie.                     | UserAADID              |

### <a name="operation-set-detail"></a>Szczegóły zestawu operacyjnego

Poniższa tabela przedstawia pola związane z encją **Szczegóły Operation Set**.

| Nazwa schematu                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializowane pola Dataverse dla żądania.                                            | CdsPayload            |
| msdyn_entityname           | Nazwa encji dla tego żądania.                                                     | EntityName            |
| msdyn_httpverb             | Metoda żądania.                                                                         | Czasownik HTTP (przestarzałe) |
| msdyn_httpverbName         | Nie dotyczy.                                                                             | Nie dotyczy        |
| msdyn_operationset         | Unikalny identyfikator zestawu operacji, do którego należy rekord.                      | OperationSet          |
| msdyn_operationsetdetailId | Unikalny identyfikator instancji encji.                                                  | Szczegół OperationSet   |
| msdyn_operationsetName     | Nie dotyczy.                                                                             | Nie dotyczy        |
| msdyn_operationtype        | Typ operacji szczegółu zestawu operacji.                                             | OperationType         |
| msdyn_operationtypeName    | Nie dotyczy.                                                                             | Nie dotyczy        |
| msdyn_psspayload           | Zserializowane pola usługi harmonogramowania projektu dla tego żądania.                           | PssPayload            |
| msdyn_recordid             | Identyfikator rekordu żądania.                                                       | Identyfikator rekordu             |
| msdyn_requestnumber        | Automatycznie wygenerowany numer, który identyfikuje kolejność, w jakiej zostały otrzymane zgłoszenia. | Numer żądania        |

## <a name="project-scheduling-service-error-logs"></a>Dzienniki błędów usługi harmonogramowania projektu

Dzienniki błędów usługi Harmonogramowanie projektu rejestrują błędy, które występują, gdy usługa Harmonogramowanie projektu próbuje wykonać operację **Zapisz** lub **Otwórz**. Istnieją trzy obsługiwane scenariusze, w których generowane są te dzienniki:

- Działania inicjowane przez użytkownika kończą się krytycznym niepowodzeniem (np. zadanie nie może zostać utworzone z powodu brakujących uprawnień).
- Serwis planowania projektu nie może programowo tworzyć, aktualizować, usuwać ani wykonywać żadnych innych operacji kaskadowych na encji.
- Użytkownik doświadcza błędów, gdy nie udaje się otworzyć rekordu (na przykład, gdy otwierany jest projekt lub aktualizowane są informacje o członku zespołu).

### <a name="project-scheduling-service-log"></a>Dziennik usługi planowania projektów

W poniższej tabeli przedstawiono pola, które są zawarte w dzienniku usługi harmonogramowania projektu.

| Nazwa schematu          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stos wywołań wyjątku.                                               | Stos wywołań     |
| msdyn_correlationid | Identyfikator korelacji błędu.                                               | CorrelationId  |
| msdyn_errorcode     | Pole, które służy do przechowywania kodu błędu Dataverse lub kodu błędu HTTP. | Kod błędu     |
| msdyn_HelpLink      | Link do publicznej dokumentacji Pomocy.                                       | Link do Pomocy      |
| msdyn_log           | Dziennik z usługi Project Scheduling Service.                                   | Dziennik            |
| msdyn_project       | Projekt, który jest powiązany z dziennikiem błędów.                             | Project        |
| msdyn_projectName   | Nazwa projektu, w którym będzie przechowywany ładunek zestawu operacji. | Nie dotyczy |
| msdyn_psserrorlogId | Unikalny identyfikator instancji encji.                                     | Dziennik błędów usługi PSS  |
| msdyn_SessionId     | Identyfikator sesji projektu.                                                        | Identyfikator sesji     |

## <a name="error-log-cleanup"></a>Czyszczenie dziennika błędów

Domyślnie zarówno dzienniki błędów usługi harmonogramowania projektu, jak i dziennik zestawu operacji mogą być czyszczone co 90 dni. Wszelkie zapisy starsze niż 90 dni zostaną usunięte. Jednak zmieniając wartość pola **msdyn_StateOperationSetAge** na stronie **Parametry projektu**, administratorzy mogą ustawić zakres czyszczenia tak, aby mieścił się w przedziale od 1 do 120 dni. Istnieje kilka metod zmiany tej wartości:

- Dostosuj encję **Parametr projektu**, poprzez utworzenie własnej strony i dodanie pola **Stale Operations Set Age**.
- Użyj kodu klienta, który korzysta z zestawu programistycznego [WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Użyj kodu Service SDK, który wykorzystuje metodę Xrm SDK **updateRecord** (odniesienie do API klienta) w aplikacjach opartych na modelu. Power Apps zawiera opis i obsługiwane parametry metody **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
