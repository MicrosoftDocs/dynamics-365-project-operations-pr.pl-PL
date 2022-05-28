---
title: Zaplanuj swoją pracę w programie Microsoft Project za pomocą dodatku Project Service
description: W tym temacie zamieszczono informacje dotyczące sposobu używania dodatku programu Microsoft Project dla programu Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 1b1c9861f2a3fbb62b29ccad272dab28dc766439
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728017"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Zaplanuj swoją pracę w programie Microsoft Project za pomocą dodatku Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ułatwia planowanie i oszacowywanie projektów. Pracę można zdefiniować tak, aby koszty, wysiłek i wartość sprzedaży były jasne w momencie przedstawiania ostatecznej propozycji.  

Możesz zainstalować [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i przeprowadzać planowanie w znanym środowisku [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Użyj zaawansowanych funkcji planowania i zarządzania [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], , a następnie zaktualizuj swój plan projektu w Project Service Automation.  

> [!IMPORTANT]
> - Aby używać funkcji zarządzania dokumentami programu SharePoint do przechowywania plików programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dla projektów programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], administrator programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] będzie musiał włączyć zarządzanie dokumentami. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] jest zgodny tylko z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Pobierz i zainstaluj dodatek  
 Przygotuj swoje dane do logowania w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Informacje te będą Ci potrzebne, aby połączyć [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Korzystając z Centrum Pobierania można pobrać dodatek dla używanej wersji programu Project Service — [wer. 2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) lub [wer. 3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Wybierz łącze pobierania.  

3.  Po zakończeniu pobierania wybierz **Tak**, aby zainstalować dodatek.  

## <a name="configure-the-add-in"></a>Skonfiguruj dodatek  

1. Otwórz [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i wybierz kartę **Project Service**.  

2. Wybierz pozycję **Połącz**.  

3. Wprowadź informacje logowania, a następnie wybierz **Zaloguj się**.  

   Teraz możesz rozpocząć korzystanie z dodatku.  

## <a name="read-from-a-template"></a>Odczytać z szablonu  
 Odczytaj z szablonu, który utworzyłeś w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i skopiowałeś do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], aby rozpocząć planowanie projektów. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Utwórz szablon projektu (Project Service Automation)](../psa/create-project-template.md)  

1.  W karcie **Project Service** wybierz **Odczytaj** > **Szablon projektu Project Service Automation**.  

2.  Wybierz szablon projektu z listy, a następnie wybierz **Otwórz**.  

    > [!NOTE]
    >  Domyślnie zadania kopiowane z szablonu do Projektu są ustawiane jako ręcznie zaplanowane.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Przypisz role [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] do zasobów projektu  

1.  Otwórz projekt, a następnie wybierz wstążkę **Zadanie**.  

2. Wybierz menu **Wykres Gantta**, a następnie wybierz **Arkusz zasobów**.  

3. Na karcie Arkusz zasobów wybierz menu rozwijane **Rola usługi Project Service Automation** i wybierz rolę usługi Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Zaopatrz projekt w zasoby  

1.  Na karcie Project Service zaznacz wiersz i wybierz **Znajdź zasoby**.  

2.  Na ekranie **Zarezerwuj zasoby** wybierz zasób, którego chcesz użyć dla projektu.  

3.  Wybierz **Zarezerwuj**, a następnie wybierz **OK**.  

## <a name="publish-your-project"></a>Opublikuj projekt  
Po zakończeniu planowania projektu, następnym krokiem jest importowanie i publikowanie projektu w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projektu zostanie zaimportowany do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Zastosowano proces generowania cen i zespołu. Otwórz projekt w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aby zobaczyć, że zespół, oszacowania projektu i struktura podziału pracy zostały wygenerowane. W poniższej tabeli pokazano, gdzie można znaleźć wyniki.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Wykres Gantt**   | Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Struktura podziału pracy**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Arkusz zasobów** |   Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Członkowie zespołu projektu**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Użyj użycia**    |    Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Szacowania projektów**.     |

**Aby zaimportować i opublikować projekt**  
1. Na karcie **Project Service** przejdź do **Opublikuj** > **Nowy projekt Project Service Automation**.  

2. W oknie dialogowym **Publikuj w nowym projekcie w Project Service** wprowadź **Nazwa projektu** i wybierz **Klient**.  

3. Opcjonalnie wybierz **Połącz plan projektu z usługą Project Service Automation**, aby połączyć plik projektu z usługą Project Service Automation.  

4. Wybierz **Publikuj**.  

   Łączenie pliku Projekt z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sprawia, że plik Projekt staje się wzorcem i ustawia strukturę podziału pracy w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tylko do odczytu.  Aby wprowadzić zmiany do planu projektu, należy sporządzić je w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i opublikować jako aktualizacje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Edytuj projekt, który został importowany  
 Aby wprowadzić zmiany do planu projektu, który został zaimportowany do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], masz dwie opcje:  

- Otwórz plik główny i edytuj go w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Odłącz plik i edytuj go bezpośrednio w Project Service. Domyślnie, projekt, który został przekazany z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] jest zablokowany i może być edytowany tylko w programie Project. Aby edytować plik w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], pliku musi być odłączony.  

### <a name="edit-in-pn_microsoft_project"></a>Edytuj w aplikacji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Z menu głównego, wybierz **Project Service** > **Projekty**.  

2. Z listy projektów otwórz ten, który został utworzony w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Wybierz **Otwórz w MS Project** ze Wstążki. Otworzy to połączony plik główny w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Odłącz plik i edytuj go w Usłudze [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Z menu głównego, wybierz **Project Service** > **Projekty**.  

2. Z listy projektów otwórz ten, który został utworzony w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Wybierz **Odłącz od MS Project** ze wstążki.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Przekazywanie pliku programu Project do programu SharePoint lub usługi Office Groups  
 Możesz przesłać plik programu Project do programu SharePoint i znaleźć go w sekcji Dokumenty związane dla Twojego projektu programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Administrator musi skonfigurować zarządzanie dokumentami programu SharePoint i włączyć je dla encji Project. 

 Możesz również przesłać plik Projekt do [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jeśli masz skonfigurowane grupy Office.

### <a name="upload-a-file-for-sharepoint"></a>Przekazywanie pliku do programu SharePoint  

1. Z menu głównego, wybierz **Project Service** > **Przekaż**.  

2. Wybierz **Do dokumentów projektu usługi Project Service Automation**.  

3. W oknie dialogowym **Włącz Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** wybierz **Tak** lub **Nie**.  

   - Po wybraniu **Tak** będziesz w stanie wybrać przycisk **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** w Project Service Automation i uruchomić [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] oraz załadować plik programu Project z biblioteki dokumentów SharePoint.  

   - Jeśli wybierzesz opcję **Nie**, łącze **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nie będzie działać.  

4. Plik [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] można znaleźć w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenty** dla danego projektu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Przekaż plik dla grup usługi Office  

1. Z menu głównego, wybierz **Project Service** > **Przekaż**.  

2. Wybierz **Do dokumentów projektu usługi Project Service Automation**.  

3. W oknie dialogowym **Włącz Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** wybierz **Tak** lub **Nie**.  

   - Po wybraniu **Tak** będziesz w stanie wybrać przycisk **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** w Project Service Automation i uruchomić [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] oraz załadować plik programu Project z biblioteki dokumentów SharePoint.  

   - Jeśli wybierzesz opcję **Nie**, łącze **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nie będzie działać.  

4. Plik [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] można znaleźć w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenty** dla danego projektu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Opublikuj projekt jako szablon  
 Można zapisać projekt i użyć go ponownie, zapisując go jako szablon projektu w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Szablony projektów to nadające się do wielokrotnego użytku plany projektów w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Aby uzyskać więcej informacji, zobacz [Tworzenie szablonu projektu (Project Service Automation)](../psa/create-project-template.md). 

1. Na karcie **Project Service** przejdź do **Opublikuj** > **Nowy szablon projektu Project Service Automation**.  

2. W oknie dialogowym **Publikuj w nowym projekcie w szablonie Project Service** wprowadź **Nazwa szablonu projektu**.  

3. Opcjonalnie wybierz **Połącz plan projektu z usługą Project Service Automation**, aby połączyć plik projektu z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Wybierz **Publikuj**.  

Łączenie pliku Projekt z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sprawia, że plik Projekt staje się wzorcem i ustawia strukturę podziału pracy w szablonie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tylko do odczytu.  Aby wprowadzić zmiany do planu projektu, należy sporządzić je w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i opublikować jako aktualizacje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Odczytywanie harmonogramu załadowanych zasobów

Podczas odczytywania projektu z rozwiązania Project Service Automation kalendarz zasobu nie jest synchronizowany z klientem stacjonarnym. Jeśli występują różnice między czasami trwania i pracą lub zakończeniem zadań, prawdopodobnie jest to spowodowane tym, że w przypadku zasobów i klienta stacjonarnego nie ma tego samego kalendarza szablonu godzin pracy zastosowanego do projektu.


## <a name="data-synchronization"></a>Synchronizacja danych
Tabele w tej sekcji zawierają informacje o synchronizacji danych encji między programem Project Service Automation a dodatkiem pulpitu programu Microsoft Project.

### <a name="project-task-entity-table"></a>Tabela encji Zadanie projektu
W poniższej tabeli przedstawiono sposób synchronizowania danych encji zadania projektu między programem Project Service Automation a dodatkiem plug-in Microsoft Project dla komputerów stacjonarnych.

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Zadanie projektu | Termin wykonania | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Szacowany nakład pracy | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Identyfikator klienta programu MS Project | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Zadanie nadrzędne | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Project | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Zadanie projektu | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Nazwa zadania projektu | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Jednostka zasobów (przestarzałe w wersji 3.0) | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Zaplanowany czas trwania | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Data rozpoczęcia | Zsynchronizowany | Niezsynchronizowane |
| Zadanie projektu | Identyfikator SPP | Zsynchronizowany | Niezsynchronizowane |

### <a name="team-member-entity-table"></a>Tabela encji Członka zespołu
W poniższej tabeli przedstawiono sposób synchronizacji danych encji członka zespołu między programem Project Service Automation i oprogramowaniem Micros

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Członek zespołu | Identyfikator klienta programu MS Project | Zsynchronizowany | Niezsynchronizowane |
| Członek zespołu | Nazwa stanowiska | Zsynchronizowany | Niezsynchronizowane |
| Członek zespołu | projekt | Zsynchronizowany | Zsynchronizowany |
| Członek zespołu | Zespół projektu | Zsynchronizowany | Zsynchronizowany |
| Członek zespołu | Jednostka zasobów | Niezsynchronizowane | Zsynchronizowany |
| Członek zespołu | Rola | Niezsynchronizowane | Zsynchronizowany |
| Członek zespołu | Godziny pracy | Niezsynchronizowane | Niezsynchronizowane |

### <a name="resource-assignment-entity-table"></a>Tabela encji Przydział zasobów
W poniższej tabeli przedstawiono sposób synchronizacji danych encji przydziału zasobów między programem Project Service Automation i oprogramowaniem Micros

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Przypisanie zasobu | Od daty | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | godzin(y) | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | Identyfikator klienta programu MS Project | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | Zaplanowana praca | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | Project | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | Zespół projektu | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | Przypisanie zasobu | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | Zadanie | Zsynchronizowany | Niezsynchronizowane |
| Przypisanie zasobu | Do daty | Zsynchronizowany | Niezsynchronizowane |

### <a name="project-task-dependencies-entity-table"></a>Tabela encji Zależności zadań projektu
W poniższej tabeli przedstawiono sposób synchronizacji danych encji Zależności zadań projektu między programem Project Service Automation i oprogramowaniem Micros

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Zależności zadań projektu | Zależność zadania projektu | Zsynchronizowany | Niezsynchronizowane |
| Zależności zadań projektu | Typ łącza | Zsynchronizowany | Niezsynchronizowane |
| Zależności zadań projektu | Zadanie poprzedzające | Zsynchronizowany | Niezsynchronizowane |
| Zależności zadań projektu | Project | Zsynchronizowany | Niezsynchronizowane |
| Zależności zadań projektu | Zadanie następujące | Zsynchronizowany | Niezsynchronizowane |

### <a name="additional-resources"></a>Dodatkowe zasoby
 [Przewodnik menedżera projektu](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
