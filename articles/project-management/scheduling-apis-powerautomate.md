---
title: Używanie interfejsów API harmonogramu projektu z Power Automate
description: Ten artykuł zawiera przykładowy przepływ, który korzysta z interfejsów programowania aplikacji planowania projektu (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916347"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Używanie interfejsów API harmonogramu projektu z Power Automate

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

W tym artykule opisano przepływ przykładowy, który pokazuje, jak utworzyć pełny plan projektu przy użyciu Microsoft Power Automate, jak utworzyć zestaw operacji i jak zaktualizować encję. W tym przykładzie pokazano, jak utworzyć projekt, członka zespołu projektu, zestawy operacji, zadania projektu i przypisania zasobów. W artykule wyjaśniono także sposób aktualizowania encji i wykonywania zestawu operacji.

Oto pełna lista kroków udokumentowanych w przepływie przykładowym w tym artykule:

1. [Tworzenie wyzwalacza usługi PowerApps](#1)
2. [Utwórz projekt](#2)
3. [Inicjowanie zmiennej dla członka zespołu](#3)
4. [Utwórz ogólnego członka zespołu](#4)
5. [Tworzenie zestawu opcji](#5)
6. [Tworzenie szansy zasobnika projektu](#6)
7. [Zainicjuj zmienną dla statusu łącza](#7)
8. [Zainicjuj zmienną dla liczby zadań](#8)
9. [Zainicjuj zmienną dla identyfikatora zadania projektu](#9)
10. [Do momentu](#10)
11. [Ustaw zadanie projektowe](#11)
12. [Utwórz zadanie projektu](#12)
13. [Utwórz przydział zasobów](#13)
14. [Zmniejsz zmienną](#14)
15. [Zmień nazwę zadania projektu](#15)
16. [Uruchom zestaw opcji](#16)

## <a name="assumptions"></a>Założenia

W artykule założono, że użytkownik ma podstawową wiedzę o platformie Dataverse, przepływach w chmurze i interfejsie API planowania aplikacji projektu. Więcej informacji znajduje się w dalszym obszarze [Odwołania](#references) w tym artykule.

## <a name="create-a-flow"></a>Utwórz przepływ

### <a name="select-an-environment"></a>Wybierz środowisko

Możesz utworzyć przepływ Power Automate w swoim środowisku.

1. Przejdź do <https://flow.microsoft.com> i zaloguj się za pomocą swoich poświadczeń administratora.
2. W prawym górnym rogu wybierz pozycję **Środowiska**.
3. Z listy wybierz środowisko, w którym został zainstalowany Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Tworzenie rozwiązania

Wykonaj następujące kroki, aby [utworzyć przepływ obsługujący rozwiązania](/power-automate/overview-solution-flows). Dzięki utworzeniu przepływu korzystającego z rozwiązania można łatwiej wyeksportować ten przepływ w celu jego późniejszego użycia.

1. W okienku nawigacji, wybierz **Rozwiązania**.
2. Na stronie **Rozwiązania** wybierz **Nowe rozwiązanie**.
3. W oknie dialogowym **Nowe rozwiązanie** ustaw pola, a następnie wybierz przycisk **Utwórz**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Krok 1: Utwórz wyzwalacz PowerApps

1. Na stronie **Rozwiązania** wybierz utworzone rozwiązanie, a następnie wybierz opcję **Nowy**.
2. W lewym okienku wybierz pozycję **Przepływy w chmurze** \> **Automatyzacja** \> **Przepływ w chmurze** \> **Błyskawiczne**.
3. W polu **Nazwa przepływu** wprowadź przepływ **demonstracyjny interfejsu API planowania**.
4. Z listy **wybierz sposób wyzwalania tej listy przepływu** wybierz pozycję **Power Apps**. Podczas tworzenia wyzwalania Power Apps logika należy do autora. W tym artykule pozostaw puste parametry wejściowe na potrzeby testowania.
5. Wybierz pozycję **Utwórz**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Krok 2. Tworzenie projektu

Wykonaj poniższe czynności, aby utworzyć przykładowy projekt.

1. W utworzonym przepływie wybierz **Nowy krok**.

    ![Dodanie nowego kroku.](media/newstep.png)

2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **akcji niepowiązanej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.

    ![Wybór operacji.](media/chooseactiontab.png)

3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.

![Zmiana nazwy kroku](media/renamestep.png)

4. Zmień nazwę kroku **Tworzenie projektu**.
5. W polu **Nazwa akcji** wybierz opcję **msdyn\_CreateProjectV1**.
6. W polu **msdyn\_subject** wybierz opcję **Dodaj zawartość dynamiczną**.
7. Na karcie **Wyrażenie** w polu funkcji wprowadź **Nazwę projektu — utcNow()**.
8. Zaznacz **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Krok 3: Inicjowanie zmiennej dla członka zespołu

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **zmienną inicjującą**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę **członka zespołu init**.
5. W polu **Nazwa** wpisz **TeamMemberAction**.
6. W polu **Typ** wybierz **Ciąg**.
7. W polu **Wartość** wpisz **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Krok 4: Utwórz ogólnego członka zespołu

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **akcji niepowiązanej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę kroku **Utwórz członka zespołu init**.
5. W polu **Nazwa akcji** wybierz opcję **TeamMemberAction** w **oknie dialogowym Zawartości dynamicznej**.
6. W polu **Parametry akcji** wprowadź następujące informacje o parametrze.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Oto wyjaśnienie parametrów:

    - **\@\@odata.type** – Nazwa typu encji. Na przykład wprowadź **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** — klucz podstawowy identyfikatora zespołu projektu. Ta wartość jest globalnie unikatowym identyfikatorem (GUID).   Identyfikator jest generowany na karcie wyrażenia.

    - **msdyn\_project\@odata.bind** — identyfikator projektu projektu, który jest właścicielem projektu. Wartością będzie zawartość dynamiczna pochodząca z odpowiedzi w kroku „Utwórz projekt”. Upewnij się, że wprowadź pełną ścieżkę i dodaj zawartość dynamiczną między elementami nadrzędnymi. Wymagane są cudzysłowy. Na przykład wprowadź **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Etykieta nazwy członka zespołu. Na przykład wpisz **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Krok 5: Tworzenie zestawu opcji

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **akcji niepowiązanej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę kroku **Zestaw operacji tworzenia**.
5. W polu **Nazwa akcji** wybierz akcję niestandardową **msdyn\_CreateOperationSetV1** Dataverse.
6. W polu **Opis** wpisz **ScheduleAPIDemoOperationSet**.
7. W polu **Projekt** wprowadź **/msdyn\_projects(**.
8. W oknie dialogowym **Zawartość dynamiczna** wybierz **msdyn\_CreateProjectV1Response ProjectId**.
9. W polu **Projekt** wprowadź **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Krok 6: Tworzenie szansy zasobnika projektu

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź **dodaj nowy wiersz**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę kroku **Tworzenie zasobnika**.
5. W polu **Nazwa tabeli** wybierz opcję **Zasobniki projektu**.
6. W polu **Nazwa** wpisz **ScheduleAPIDemoBucket1**.
7. W polu **Projekt** wybierz **msdyn\_CreateProjectV1Response ProjectId** w oknie dialogowym **Zawartość dynamiczna**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Krok 7: Zainicjuj zmienną dla statusu łącza

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **zmienną inicjującą**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę kroku **Init linkstatus**.
5. W polu **Nazwa** wpisz **linkstatus**.
6. W polu **Typ** wybierz **Liczba całkowita**.
7. W polu **Wartość** wpisz **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Krok 8: Zainicjuj zmienną dla liczby zadań

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **zmienną inicjującą**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę kroku **Liczba zadań**.
5. W polu **Nazwa** wpisz **liczba zadań**.
6. W polu **Typ** wybierz **Liczba całkowita**.
7. W polu **Wartość** wpisz **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Krok 9: Zainicjuj zmienną dla identyfikatora zadania projektu

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **zmienną inicjującą**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę **ProjectTaskID init**.
5. W polu **Nazwa** wpisz **liczba zadań**.
6. W polu **Typ** wybierz **Ciąg**.
7. W przypadku **pola Wartość** wprowadź wartość **guid()** w konstruktorze wyrażenia.

## <a name="step-10-do-until"></a><a id="10"></a>Krok 10: Do momentu

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź **do momentu**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. Pierwszą wartość w instrukcji warunkowej należy ustawić na **liczbę zadań** zmiennej z **okna dialogowego Zawartość dynamiczna**.
4. Ustaw warunek na **mniejszy niż równy**.
5. Drugą wartość w instrukcji warunkowej należy ustawić na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Krok 11: Ustaw zadanie projektowe

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **ustaw zmienną**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W nowym kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę **Ustaw zadanie projektu**.
5. W polu **Nazwa** wybierz **msdyn\_projecttaskid**.
6. W przypadku **pola Wartość** wprowadź wartość **guid()** w konstruktorze wyrażenia.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Krok 12: Tworzenie zadania projektu

Wykonaj te kroki, aby utworzyć zadanie projektu z unikatowym identyfikatorem należącym do bieżącego projektu i utworzonym zadaniem projektu.

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **akcji niepowiązanej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę **Utwórz zadanie projektu**.
5. W polu **Nazwa akcji** wybierz opcję **msdyn\_PssCreateV1**.
6. W polu **Encja** wprowadź następujące informacje o parametrze.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Oto wyjaśnienie parametrów:

    - **\@\@odata.type** – Nazwa typu encji. Na przykład wprowadź **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Unikatowy identyfikator tego zadania. Wartość powinna być ustawiona na zmienną dynamiczną z **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** — identyfikator projektu projektu, który jest właścicielem projektu. Wartością będzie zawartość dynamiczna pochodząca z odpowiedzi w kroku „Utwórz projekt”. Upewnij się, że wprowadź pełną ścieżkę i dodaj zawartość dynamiczną między elementami nadrzędnymi. Wymagane są cudzysłowy. Na przykład wprowadź **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – dowolna nazwa zadania.
    - **msdyn\_projectbucket\@odata.bind** – projekt zawierający zadania. Wartością będzie zawartość dynamiczna pochodząca z odpowiedzi w kroku „Utwórz zasobnik”. Upewnij się, że wprowadź pełną ścieżkę i dodaj zawartość dynamiczną między elementami nadrzędnymi. Wymagane są cudzysłowy. Na przykład wprowadź **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** — zawartość dynamiczna dla daty rozpoczęcia. Na przykład przyszłości będzie reprezentowana **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Planowana data rozpoczęcia. Na przykład przyszłości będzie reprezentowana **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – zaplanowana data zakończenia. Wybierz datę w przyszłości. Na przykład określ wartość **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Link do strony stanu. Na przykład wprowadź **"192350000"**.

7. W polu **OperationSetId** wybierz **msdyn\_CreateOperationSetV1Response** w oknie dialogowym **Zawartość dynamiczna**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Krok 13: Utwórz przydział zasobów

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **akcji niepowiązanej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę kroku **Utwórz przydział**.
5. W polu **Nazwa akcji** wybierz opcję **msdyn\_PssCreateV1**.
6. W polu **Encja** wprowadź następujące informacje o parametrze.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. W polu **OperationSetId** wybierz **msdyn\_CreateOperationSetV1Response** w oknie dialogowym **Zawartość dynamiczna**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Krok 14: Zmniejsz zmienną

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **dekrementacji zmiennej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W polu **Nazwa** wybierz **liczba zadań**.
4. W polu **Wartość** wpisz **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Krok 15: Zmień nazwę zadania projektu

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **akcji niepowiązanej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę **Zmień nazwę zadania projektu**.
5. W polu **Nazwa akcji** wybierz opcję **msdyn\_PssUpdateV1**.
6. W polu **Encja** wprowadź następujące informacje o parametrze.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. W polu **OperationSetId** wybierz **msdyn\_CreateOperationSetV1Response** w oknie dialogowym **Zawartość dynamiczna**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Krok 16: Uruchom zestaw operacji

1. W przepływie wybierz **Nowy krok**.
2. W oknie dialogowym **Wybierz operację** w polu wyszukiwania wprowadź wykonanie **akcji niepowiązanej**. Następnie na karcie **Akcje** wybierz operację z listy wyników.
3. W kroku wybierz wielokropek (**...**), a następnie wybierz **Zmień nazwę**.
4. Zmień nazwę kroku **Wykonaj operację Zestaw**.
5. W polu **Nazwa akcji** wybierz opcję **msdyn\_ExecuteOperationSetV1**.
6. W polu **OperationSetId** wybierz **msdyn\_CreateOperationSetV1Response OperationSetId** w oknie dialogowym **Zawartość dynamiczna**.

## <a name="references"></a>Odwołania

- [Omówienie sposobu integrowania przepływów Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Używanie interfejsów API harmonogramu projektu do wykonywania operacji na encji planowania](schedule-api-preview.md)
- [Omówienie przepływów chmury — Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Omówienie przepływów świadomość rozwiązania - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
