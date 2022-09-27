---
title: Używanie interfejsów API harmonogramu projektu do wykonywania operacji na encji planowania
description: W tym artykule przedstawiono informacje i przykłady dotyczące korzystania z interfejsów API harmonogramu projektów.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541138"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Używanie interfejsów API harmonogramu projektu do wykonywania operacji na encji planowania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_


**Encje planowania**

Interfejsy API harmonogramu projektu zapewniają możliwość wykonywania operacji tworzenia, aktualizowania i usuwania za pomocą **encji planowania**. Te jednostki są zarządzane za pomocą aparatu planowania w Project dla sieci Web. We wcześniejszych wersjach Dynamics 365 Project Operations operacje tworzenia, aktualizowania i usuwania **Encji planowania** były ograniczone.

W poniższej tabeli przedstawiono pełną listę encji harmonogramu projektu.

| **Nazwa encji**         | **Logiczna nazwa encji**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Zadanie projektu            | msdyn_projecttask           |
| Zależność zadania projektu | msdyn_projecttaskdependency |
| Przypisanie zasobu     | msdyn_resourceassignment    |
| Zasobnik projektu          | msdyn_projectbucket         |
| Członek zespołu projektu     | msdyn_projectteam           |
| Listy kontrolne projektu      | msdyn_projectchecklist      |
| Etykieta projektu           | msdyn_projectlabel          |
| Zadanie projektu do etykietowania   | msdyn_projecttasktolabel    |
| Przebieg projektu          | msdyn_projectsprint         |

**OperationSet**

OperationSet to wzorzec jednostki pracy, którego można użyć, gdy w ramach transakcji musi zostać przetworzonych kilka żądań mających wpływ na harmonogram.

**Interfejsy API harmonogramu projektu**

Poniżej przedstawiono listę bieżących interfejsów API harmonogramu projektu.

| **API**                                 | opis                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Ten interfejs API służy do tworzenia projektu. Domyślne i domyślne rozmiary projektu są tworzone natychmiast.                         |
| **msdyn_CreateTeamMemberV1**            | Ten interfejs API służy do tworzenia członka projektu. Rekord członka zespołu jest tworzony natychmiast.                                  |
| **msdyn_CreateOperationSetV1**          | Ten interfejs API może być używany do planowania kilku żądań, które muszą zostać wykonane w ramach transakcji.                                        |
| **msdyn_PssCreateV1**                   | Ten interfejs API służy do tworzenia encji. Encją może być dowolna z encji planowania projektów, które obsługują operację tworzenia. |
| **msdyn_PssUpdateV1**                   | Ten interfejs API służy do aktualizacji encji. Encją może być dowolna z encji planowania projektów, które obsługują operację aktualizowania  |
| **msdyn_PssDeleteV1**                   | Ten interfejs API służy do usuwania encji. Encją może być dowolna z encji planowania projektów, które obsługują operację usuwania. |
| **msdyn_ExecuteOperationSetV1**         | Ten interfejs API jest używany do wykonywania wszystkich operacji w ramach danego zestawu operacji.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Ten interfejs API służy do aktualizacji konturu planowanej pracy w ramach Przydziału zasobów.                                                        |



**Używanie interfejsów API harmonogramu projektu z zestawem OperationSet**

Ponieważ rekordy z zarówno **CreateProjectV1**, jak i **CreateTeamMemberV1** są tworzone natychmiast, tych interfejsów API nie można używać bezpośrednio w przy użyciu zestawu **OperationSet**. Interfejs API umożliwia jednak tworzenie potrzebnych rekordów, tworzenie zestawu **OperationSet**, a następnie używanie tych wstępnie utworzonych rekordów w zestawie **OperationSet**.

**Obsługiwane operacje**

| **Encja planowania**   | **Utworzenie** | **Update** | **Delete** | **Ważne uwagi**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zadanie projektu            | Tak        | Tak        | Tak        | Pola **Progres**, **EffortCompleted** i **EffortRemaining** można edytować w Project for the Web, ale nie można ich edytować w Project Operations.                                                                                                                                                                                             |
| Zależność zadania projektu | Tak        | Nie.         | Tak        | Rekordy zależności zadań projektu nie są aktualizowane. Zamiast tego można usunąć stary rekord i utworzyć nowy rekord.                                                                                                                                                                                                                                 |
| Przypisanie zasobu     | Tak        | Tak\*      | Tak        | Operacje z następującymi polami nie są obsługiwane: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**. Rekordy przypisania zasobów nie są aktualizowane. Zamiast tego można usunąć stary rekord i utworzyć nowy rekord. Do aktualizacji konturów Przydziału zasobów udostępniono osobny interfejs API. |
| Zasobnik projektu          | Tak        | Tak        | Tak        | Domyślny domyślny rozmiar jest tworzony przy użyciu interfejsu **API CreateProjectV1**. W wersji 16. aktualizacji dodano obsługę tworzenia i usuwania zasobników projektów.                                                                                                                                                                                                   |
| Członek zespołu projektu     | Tak        | Tak        | Tak        | Aby utworzyć operację tworzenia, użyj interfejsu API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Tak        | Tak        |            | Operacje z następującymi polami nie są obsługiwane: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.                                                                                       |
| Listy kontrolne projektu      | Tak        | Tak        | Tak        |                                                                                                                                                                                                                                                                                                                                                         |
| Etykieta projektu           | Nie.         | Tak        | Nie.         | Nazwy etykiet można zmieniać. Ta funkcja jest dostępna tylko w programie Project for the Web                                                                                                                                                                                                                                                                      |
| Zadanie projektu do etykietowania   | Tak        | Nie.         | Tak        | Ta funkcja jest dostępna tylko w programie Project for the Web                                                                                                                                                                                                                                                                                                  |
| Przebieg projektu          | Tak        | Tak        | Tak        | Pole **Początek** musi mieć datę wcześniejszą niż pole **Zakończenie**. Sprinty dotyczące tego samego projektu nie mogą się na siebie nakładać. Ta funkcja jest dostępna tylko w programie Project for the Web                                                                                                                                                                    |




Właściwość numeru identyfikacyjnego jest opcjonalna. Jeśli zostanie on podany, system próbuje go użyć i zgłasza wyjątek, jeśli nie może być używany. Jeśli nie zostanie on dostarczony, system wygeneruje go.

**Ograniczenia i znane problemy**

Oto lista ograniczeń i znanych problemów:

-   Interfejsy API harmonogramu projektu mogą być używane tylko przez **użytkowników z licencją programu Microsoft Project**. Nie mogą z nich korzystać:
    -   Użytkownicy aplikacji
    -   Użytkownicy systemowi
    -   Użytkownicy integracyjni
    -   Inni użytkownicy, którzy nie mają wymaganej licencji
-   Każdy **OperationSet** może mieć maksymalnie 100 operacji.
-   Każdy użytkownik może mieć otwartych maksymalnie 10 **OperationSets**.
-   Project Operations obsługuje obecnie maksymalnie 500 wszystkich zadań w projekcie.
-   Każda operacja aktualizacji konturu przypisania zasobów jest liczona jako jedna operacja.
-   Każda lista zaktualizowanych konturów może zawierać maksymalnie 100 odcinków czasu.
-   Obecnie nie są dostępne dzienniki błędów i stanu niepowodzenia **OperationSet**.
-   W ramach jednego projektu można przeprowadzić maksymalnie 400 sprintów.
-   [Limity i ograniczenia projektów i zadań](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Etykiety są obecnie dostępne tylko w Project for the Web.

**Obsługa błędów**

-   Aby przejrzeć błędy wygenerowane z zestawów operacji, przejdź do strony **Ustawienia** \> **Harmonogram integracji** \> **Zestawy operacji**.
-   Aby przejrzeć błędy wygenerowane przez usługę harmonogramu projektów, przejdź do pozycji **Ustawienia** \> **Integracja harmonogramu** \> **Dzienniki błędów PSS**.

**Edycja konturów przypisania zasobów**

W przeciwieństwie do wszystkich innych interfejsów API planowania projektu, które aktualizują encję, interfejs API konturu przydziału zasobów jest odpowiedzialny wyłącznie za aktualizację pojedynczego pola, msdyn_plannedwork, w pojedynczej encji, msydn_resourceassignment.

Podany tryb harmonogramu to:

-   **stałe jednostki**
-   Kalendarz projektu to 9-5p to 9-5 pst, poniedziałek, wtorek, czwartek, piątek (NIE MA PRACY W ŚRODĘ)
-   i kalendarz zasobów to od 9 do 1p PST od poniedziałku do piątku

To zadanie jest na jeden tydzień, cztery godziny dziennie. Dzieje się tak dlatego, że kalendarz zasobów działa w godzinach 9-1 PST, czyli cztery godziny dziennie.

| &nbsp;     | Zadanie | Data rozpoczęcia | Data zakończenia  | Ilość | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 pracownik |  T1  | 6/13/2022  | 6/17/2022 | 20       | 100         | 100         | 100         | 100         | 100         |

Na przykład, jeśli chcesz, aby w tym tygodniu pracownik pracował tylko trzy godziny dziennie i miał jedną godzinę na inne zadania.

#### <a name="updatedcontours-sample-payload"></a>Przykładowa zawartość UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Jest to zadanie po uruchomieniu interfejsu API Update Contour Schedule.

| &nbsp;     | Zadanie | Data rozpoczęcia | Data zakończenia  | Ilość | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 pracownik | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Przykładowy scenariusz**

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

** Więcej przykładów

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
