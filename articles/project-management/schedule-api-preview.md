---
title: Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania
description: To temat zawiera informacje i przykłady dotyczące korzystania z interfejsów API planowania.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868142"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Użyj interfejsów API harmonogramu, aby wykonywać operacje na jednostkach planowania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

> [!IMPORTANT] 
> Niektóre lub wszystkie funkcje wymienione w tym temacie są dostępne w wersji zapoznawczej. Zawartość i funkcjonalność mogą ulec zmianie. 

## <a name="scheduling-entities"></a>Encje planowania

Harmonogramy API zapewniają możliwość tworzenia, aktualizowania i usuwania operacji z **Encje planowania**. Te jednostki są zarządzane za pomocą aparatu planowania w Project dla sieci Web. We wcześniejszych wersjach Dynamics 365 Project Operations operacje tworzenia, aktualizowania i usuwania **Encji planowania** były ograniczone.

W poniższej tabeli przedstawiono pełną listę **Encje planowania**.

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

## <a name="schedule-apis"></a>Planowanie interfejsów API

Poniżej przedstawiono listę bieżących interfejsów API planowania.

- **msdyn_CreateProjectV1**: tego interfejsu API można używać do tworzenia projektu. Projekt i domyślny rozmiar projektu są tworzone natychmiast.
- **msdyn_CreateTeamMemberV1**: tego interfejsu API można używać do tworzenia członka zespołu projektu. Rekord członka zespołu jest tworzony natychmiast.
- **msdyn_CreateOperationSetV1**: ten interfejs API może być używany do planowania kilku żądań, które muszą zostać wykonane w ramach transakcji.
- **msdyn_PSSCreateV1**: tego interfejsu API można używać do tworzenia encji. Może to być dowolny z obiektów planowania obsługujący operację tworzenia.
- **msdyn_PSSUpdateV1**: tego interfejsu API można używać do aktualizacji encji. Może to być dowolny z obiektów planowania obsługujący operację aktualizacji.
- **msdyn_PSSDeleteV1**: tego interfejsu API można używać do usuwania encji. Może to być dowolny z obiektów planowania obsługujący operację usuwania.
- **msdyn_ExecuteOperationSetV1**: ten interfejs API jest używany do wykonywania wszystkich operacji w ramach danego zestawu operacji.

## <a name="using-schedule-apis-with-operationset"></a>Używanie interfejsów API harmonogramu z zestawem OperationSet

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

## <a name="limitations-and-known-issues"></a>Ograniczenia i znane problemy
Oto lista ograniczeń i znanych problemów:

- Interfejsy API planowania mogą być używane tylko przez **Użytkowników z licencją programu Microsoft Project**. Nie mogą z nich korzystać:
    - Użytkownicy aplikacji
    - Użytkownicy systemowi
    - Użytkownicy integracyjni
    - Inni użytkownicy, którzy nie mają wymaganej licencji
- Każdy **OperationSet** może mieć maksymalnie 100 operacji.
- Każdy użytkownik może mieć otwartych maksymalnie 10 **OperationSets**.
- Project Operations obsługuje obecnie maksymalnie 500 wszystkich zadań w projekcie.
- Obecnie nie są dostępne dzienniki błędów i stanu niepowodzenia **OperationSet**.
- Harmonogram interfejsów API jest w publicznej wersji zapoznawczej. Używanie tych interfejsów API w środowisku produkcyjnym nie jest obsługiwane przez firmę Microsoft.

## <a name="sample-scenario"></a>Przykładowy scenariusz

W tym scenariuszu zostanie utworzyć projekt, członka zespołu, cztery zadania i dwa przypisania zasobów. Następnie należy zaktualizować jedno zadanie, zaktualizować projekt, usunąć jedno zadanie, usunąć jedno przypisanie zasobów i utworzyć zależność zadania.

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Więcej przykładów

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
