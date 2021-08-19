---
title: Używanie interfejsów API harmonogramu projektu do wykonywania operacji na encji planowania
description: Ten temat zawiera informacje i przykłady dotyczące korzystania z interfejsów API harmonogramu projektu.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 55bd9020275fbb72761b45ba09294f57266b418c0e5b506ba55a2a498aff24e5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008779"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Używanie interfejsów API harmonogramu projektu do wykonywania operacji na encji planowania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

> [!IMPORTANT] 
> Niektóre lub wszystkie funkcje wymienione w tym temacie są dostępne w wersji zapoznawczej. Zawartość i funkcjonalność mogą ulec zmianie. 

## <a name="scheduling-entities"></a>Encje planowania

Interfejsy API harmonogramu projektu zapewniają możliwość wykonywania operacji tworzenia, aktualizowania i usuwania za pomocą **encji planowania**. Te jednostki są zarządzane za pomocą aparatu planowania w Project dla sieci Web. We wcześniejszych wersjach Dynamics 365 Project Operations operacje tworzenia, aktualizowania i usuwania **Encji planowania** były ograniczone.

W poniższej tabeli przedstawiono pełną listę encji harmonogramu projektu.

| Nazwa encji  | Logiczna nazwa encji |
| --- | --- |
| Project | msdyn_project |
| Zadanie projektu  | msdyn_projecttask  |
| Zależność zadania projektu  | msdyn_projecttaskdependency  |
| Przypisanie zasobu | msdyn_resourceassignment |
| Zasobnik projektu  | msdyn_projectbucket |
| Członek zespołu projektu | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet to wzorzec jednostki pracy, którego można użyć, gdy w ramach transakcji musi zostać przetworzonych kilka żądań mających wpływ na harmonogram.

## <a name="project-schedule-apis"></a>Interfejsy API harmonogramu projektu

Poniżej przedstawiono listę bieżących interfejsów API harmonogramu projektu.

- **msdyn_CreateProjectV1**: tego interfejsu API można używać do tworzenia projektu. Projekt i domyślny rozmiar projektu są tworzone natychmiast.
- **msdyn_CreateTeamMemberV1**: tego interfejsu API można używać do tworzenia członka zespołu projektu. Rekord członka zespołu jest tworzony natychmiast.
- **msdyn_CreateOperationSetV1**: ten interfejs API może być używany do planowania kilku żądań, które muszą zostać wykonane w ramach transakcji.
- **msdyn_PSSCreateV1**: tego interfejsu API można używać do tworzenia encji. Encją może być dowolna z encji planowania projektów, które obsługują operację tworzenia.
- **msdyn_PSSUpdateV1**: tego interfejsu API można używać do aktualizacji encji. Encją może być dowolna z encji planowania projektów, które obsługują operację aktualizowania.
- **msdyn_PSSDeleteV1**: tego interfejsu API można używać do usuwania encji. Encją może być dowolna z encji planowania projektów, które obsługują operację usuwania.
- **msdyn_ExecuteOperationSetV1**: ten interfejs API jest używany do wykonywania wszystkich operacji w ramach danego zestawu operacji.

## <a name="using-project-schedule-apis-with-operationset"></a>Używanie interfejsów API harmonogramu projektu z zestawem OperationSet

Ponieważ rekordy z zarówno **CreateProjectV1**, jak i **CreateTeamMemberV1** są tworzone natychmiast, tych interfejsów API nie można używać bezpośrednio w przy użyciu zestawu **OperationSet**. Interfejs API umożliwia jednak tworzenie potrzebnych rekordów, tworzenie zestawu **OperationSet**, a następnie używanie tych wstępnie utworzonych rekordów w zestawie **OperationSet**.

## <a name="supported-operations"></a>Obsługiwane operacje

| Encja planowania | Utworzenie | Zaktualizuj | Delete | Ważne uwagi |
| --- | --- | --- | --- | --- |
Zadanie projektu | Tak | Tak | Tak | Brak |
| Zależność zadania projektu | Tak | Tak | | Rekordy zależności zadań projektu nie są aktualizowane. Zamiast tego można usunąć stary rekord i utworzyć nowy rekord. |
| Przypisanie zasobu | Tak | Tak | | Operacje z następującymi polami nie są obsługiwane: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**. Rekordy przypisania zasobów nie są aktualizowane. Zamiast tego można usunąć stary rekord i utworzyć nowy rekord. |
| Zasobnik projektu | Nie dotyczy | Nie dotyczy | Nie dotyczy | Domyślny domyślny rozmiar jest tworzony przy użyciu interfejsu **API CreateProjectV1**. |
| Członek zespołu projektu | Tak | Tak | Tak | Aby utworzyć operację tworzenia, użyj interfejsu API **CreateTeamMemberV1**. |
| Project | Tak | Tak | Nie dotyczy | Operacje z następującymi polami nie są obsługiwane: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**. |

Te interfejsy API można nazwać obiektami encji, które zawierają pola niestandardowe.

Właściwość numeru identyfikacyjnego jest opcjonalna. Jeśli zostanie on podany, system próbuje go użyć i zgłasza wyjątek, jeśli nie może być używany. Jeśli nie zostanie on dostarczony, system wygeneruje go.

## <a name="restricted-fields"></a>Pola ograniczone

W poniższych tabelach przedstawiono pola, których nie można **tworzyć** i **edytować**.

### <a name="project-task"></a>Zadanie projektu

| **Nazwa logiczna**                       | **Można tworzyć** | **Może edytować**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | nie             | nie               |
| msdyn_actualcost_base                  | nie             | nie               |
| msdyn_actualend                        | nie             | nie               |
| msdyn_actualsales                      | nie             | nie               |
| msdyn_actualsales_base                 | nie             | nie               |
| msdyn_actualstart                      | nie             | nie               |
| msdyn_costatcompleteestimate           | nie             | nie               |
| msdyn_costatcompleteestimate_base      | nie             | nie               |
| msdyn_costconsumptionpercentage        | nie             | nie               |
| msdyn_effortcompleted                  | nie             | nie               |
| msdyn_effortestimateatcomplete         | nie             | nie               |
| msdyn_iscritical                       | nie             | nie               |
| msdyn_iscriticalname                   | nie             | nie               |
| msdyn_ismanual                         | nie             | nie               |
| msdyn_ismanualname                     | nie             | nie               |
| msdyn_ismilestone                      | nie             | nie               |
| msdyn_ismilestonename                  | nie             | nie               |
| msdyn_LinkStatus                       | nie             | nie               |
| msdyn_linkstatusname                   | nie             | nie               |
| msdyn_msprojectclientid                | nie             | nie               |
| msdyn_plannedcost                      | nie             | nie               |
| msdyn_plannedcost_base                 | nie             | nie               |
| msdyn_plannedsales                     | nie             | nie               |
| msdyn_plannedsales_base                | nie             | nie               |
| msdyn_pluginprocessingdata             | nie             | nie               |
| msdyn_progress                         | nie             | nie (tak dla P4W) |
| msdyn_remainingcost                    | nie             | nie               |
| msdyn_remainingcost_base               | nie             | nie               |
| msdyn_remainingsales                   | nie             | nie               |
| msdyn_remainingsales_base              | nie             | nie               |
| msdyn_requestedhours                   | nie             | nie               |
| msdyn_resourcecategory                 | nie             | nie               |
| msdyn_resourcecategoryname             | nie             | nie               |
| msdyn_resourceorganizationalunitid     | nie             | nie               |
| msdyn_resourceorganizationalunitidname | nie             | nie               |
| msdyn_salesconsumptionpercentage       | nie             | nie               |
| msdyn_salesestimateatcomplete          | nie             | nie               |
| msdyn_salesestimateatcomplete_base     | nie             | nie               |
| msdyn_salesvariance                    | nie             | nie               |
| msdyn_salesvariance_base               | nie             | nie               |
| msdyn_scheduleddurationminutes         | nie             | nie               |
| msdyn_scheduledend                     | nie             | nie               |
| msdyn_scheduledstart                   | nie             | nie               |
| msdyn_schedulevariance                 | nie             | nie               |
| msdyn_skipupdateestimateline           | nie             | nie               |
| msdyn_skipupdateestimatelinename       | nie             | nie               |
| msdyn_summary                          | nie             | nie               |
| msdyn_varianceofcost                   | nie             | nie               |
| msdyn_varianceofcost_base              | nie             | nie               |

### <a name="project-task-dependency"></a>Zależność zadania projektu

| **Nazwa logiczna**              | **Można tworzyć** | **Może edytować** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | nie             | nie           |
| msdyn_linktypename            | nie             | nie           |
| msdyn_predecessortask         | tak            | nie           |
| msdyn_predecessortaskname     | tak            | nie           |
| msdyn_project                 | tak            | nie           |
| msdyn_projectname             | tak            | nie           |
| msdyn_projecttaskdependencyid | tak            | nie           |
| msdyn_successortask           | tak            | nie           |
| msdyn_successortaskname       | tak            | nie           |

### <a name="resource-assignment"></a>Przypisanie zasobu

| **Nazwa logiczna**             | **Można tworzyć** | **Może edytować** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | tak            | nie           |
| msdyn_bookableresourceidname | tak            | nie           |
| msdyn_bookingstatusid        | nie             | nie           |
| msdyn_bookingstatusidname    | nie             | nie           |
| msdyn_committype             | nie             | nie           |
| msdyn_committypename         | nie             | nie           |
| msdyn_effort                 | nie             | nie           |
| msdyn_effortcompleted        | nie             | nie           |
| msdyn_effortremaining        | nie             | nie           |
| msdyn_finish                 | nie             | nie           |
| msdyn_plannedcost            | nie             | nie           |
| msdyn_plannedcost_base       | nie             | nie           |
| msdyn_plannedcostcontour     | nie             | nie           |
| msdyn_plannedsales           | nie             | nie           |
| msdyn_plannedsales_base      | nie             | nie           |
| msdyn_plannedsalescontour    | nie             | nie           |
| msdyn_plannedwork            | nie             | nie           |
| msdyn_projectid              | tak            | nie           |
| msdyn_projectidname          | nie             | nie           |
| msdyn_projectteamid          | nie             | nie           |
| msdyn_projectteamidname      | nie             | nie           |
| msdyn_start                  | nie             | nie           |
| msdyn_taskid                 | nie             | nie           |
| msdyn_taskidname             | nie             | nie           |
| msdyn_userresourceid         | nie             | nie           |

### <a name="project-team-member"></a>Członek zespołu projektu

| **Nazwa logiczna**                                 | **Można tworzyć** | **Może edytować** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | nie             | nie           |
| msdyn_creategenericteammemberwithrequirementname | nie             | nie           |
| msdyn_deletestatus                               | nie             | nie           |
| msdyn_deletestatusname                           | nie             | nie           |
| msdyn_effort                                     | nie             | nie           |
| msdyn_effortcompleted                            | nie             | nie           |
| msdyn_effortremaining                            | nie             | nie           |
| msdyn_finish                                     | nie             | nie           |
| msdyn_hardbookedhours                            | nie             | nie           |
| msdyn_hours                                      | nie             | nie           |
| msdyn_markedfordeletiontimer                     | nie             | nie           |
| msdyn_markedfordeletiontimestamp                 | nie             | nie           |
| msdyn_msprojectclientid                          | nie             | nie           |
| msdyn_percentage                                 | nie             | nie           |
| msdyn_requiredhours                              | nie             | nie           |
| msdyn_softbookedhours                            | nie             | nie           |
| msdyn_start                                      | nie             | nie           |

### <a name="project"></a>Project

| **Nazwa logiczna**                       | **Można tworzyć** | **Może edytować** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | nie             | nie           |
| msdyn_actualexpensecost_base           | nie             | nie           |
| msdyn_actuallaborcost                  | nie             | nie           |
| msdyn_actuallaborcost_base             | nie             | nie           |
| msdyn_actualsales                      | nie             | nie           |
| msdyn_actualsales_base                 | nie             | nie           |
| msdyn_contractlineproject              | tak            | nie           |
| msdyn_contractorganizationalunitid     | tak            | nie           |
| msdyn_contractorganizationalunitidname | tak            | nie           |
| msdyn_costconsumption                  | nie             | nie           |
| msdyn_costestimateatcomplete           | nie             | nie           |
| msdyn_costestimateatcomplete_base      | nie             | nie           |
| msdyn_costvariance                     | nie             | nie           |
| msdyn_costvariance_base                | nie             | nie           |
| msdyn_duration                         | nie             | nie           |
| msdyn_effort                           | nie             | nie           |
| msdyn_effortcompleted                  | nie             | nie           |
| msdyn_effortestimateatcompleteeac      | nie             | nie           |
| msdyn_effortremaining                  | nie             | nie           |
| msdyn_finish                           | tak            | tak          |
| msdyn_globalrevisiontoken              | nie             | nie           |
| msdyn_islinkedtomsprojectclient        | nie             | nie           |
| msdyn_islinkedtomsprojectclientname    | nie             | nie           |
| msdyn_linkeddocumenturl                | nie             | nie           |
| msdyn_msprojectdocument                | nie             | nie           |
| msdyn_msprojectdocumentname            | nie             | nie           |
| msdyn_plannedexpensecost               | nie             | nie           |
| msdyn_plannedexpensecost_base          | nie             | nie           |
| msdyn_plannedlaborcost                 | nie             | nie           |
| msdyn_plannedlaborcost_base            | nie             | nie           |
| msdyn_plannedsales                     | nie             | nie           |
| msdyn_plannedsales_base                | nie             | nie           |
| msdyn_progress                         | nie             | nie           |
| msdyn_remainingcost                    | nie             | nie           |
| msdyn_remainingcost_base               | nie             | nie           |
| msdyn_remainingsales                   | nie             | nie           |
| msdyn_remainingsales_base              | nie             | nie           |
| msdyn_replaylogheader                  | nie             | nie           |
| msdyn_salesconsumption                 | nie             | nie           |
| msdyn_salesestimateatcompleteeac       | nie             | nie           |
| msdyn_salesestimateatcompleteeac_base  | nie             | nie           |
| msdyn_salesvariance                    | nie             | nie           |
| msdyn_salesvariance_base               | nie             | nie           |
| msdyn_scheduleperformance              | nie             | nie           |
| msdyn_scheduleperformancename          | nie             | nie           |
| msdyn_schedulevariance                 | nie             | nie           |
| msdyn_taskearlieststart                | nie             | nie           |
| msdyn_teamsize                         | nie             | nie           |
| msdyn_teamsize_date                    | nie             | nie           |
| msdyn_teamsize_state                   | nie             | nie           |
| msdyn_totalactualcost                  | nie             | nie           |
| msdyn_totalactualcost_base             | nie             | nie           |
| msdyn_totalplannedcost                 | nie             | nie           |
| msdyn_totalplannedcost_base            | nie             | nie           |


## <a name="limitations-and-known-issues"></a>Ograniczenia i znane problemy
Oto lista ograniczeń i znanych problemów:

- Interfejsy API harmonogramu projektu mogą być używane tylko przez **użytkowników z licencją programu Microsoft Project.** Nie mogą z nich korzystać:
    - Użytkownicy aplikacji
    - Użytkownicy systemowi
    - Użytkownicy integracyjni
    - Inni użytkownicy, którzy nie mają wymaganej licencji
- Każdy **OperationSet** może mieć maksymalnie 100 operacji.
- Każdy użytkownik może mieć otwartych maksymalnie 10 **OperationSets**.
- Project Operations obsługuje obecnie maksymalnie 500 wszystkich zadań w projekcie.
- Obecnie nie są dostępne dzienniki błędów i stanu niepowodzenia **OperationSet**.
- [Limity i ograniczenia projektów i zadań](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Obsługa błędów

   - Aby przejrzeć błędy wygenerowane z zestawów operacji, przejdź do strony **Ustawienia** \> **Harmonogram integracji** \> **Zestawy operacji**.
   - Aby przejrzeć błędy wygenerowane przez usługę harmonogramu projektów, przejdź do pozycji **Ustawienia** \> **Integracja harmonogramu** \> **Dzienniki błędów PSS**.

## <a name="sample-scenario"></a>Przykładowy scenariusz

W tym scenariuszu zostanie utworzyć projekt, członka zespołu, cztery zadania i dwa przypisania zasobów. Następnie należy zaktualizować jedno zadanie, zaktualizować projekt, usunąć jedno zadanie, usunąć jedno przypisanie zasobów i utworzyć zależność zadania.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Więcej przykładów

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
