---
title: Użyj dodatku Project Service, aby zaplanować pracę w programie Microsoft Project | MicrosoftDocs
description: W tym temacie zamieszczono informacje dotyczące sposobu dodawania, konfigurowania i używania dodatku programu Microsoft Project dla programu Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: ccebf1439f49092b23da5b4fc2ebb4fc484de4dd17c870eea9fe37b00fbb3689
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005314"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Użyj dodatku Project Service Automation do planowania pracy w programie Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ułatwia planowanie i oszacowywanie projektów. Pracę można zdefiniować tak, aby koszty, wysiłek i wartość sprzedaży były jasne w momencie przedstawiania ostatecznej propozycji.  

 Teraz możesz zainstalować [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i przeprowadzać planowanie w znanym środowisku [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Użyj zaawansowanych funkcji planowania i zarządzania [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], , a następnie zaktualizuj swój plan projektu w Project Service Automation.  

> [!IMPORTANT]
> - Aby używać funkcji zarządzania dokumentami programu SharePoint do przechowywania plików programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dla projektów programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], administrator programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] będzie musiał włączyć zarządzanie dokumentami. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] jest zgodny tylko z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Pobierz i zainstaluj dodatek  
 Przygotuj swoje dane do logowania w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Informacje te będą Ci potrzebne, aby połączyć [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Korzystając z Centrum Pobierania można pobrać dodatek dla używanej wersji programu Project Service — [wer. 2.X](https://go.microsoft.com/fwlink/?linkid=828268) lub [wer. 3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Kliknij łącze pobierania.  

3.  Po zakończeniu pobierania kliknij **Tak**, aby zainstalować dodatek.  

## <a name="configure-the-add-in"></a>Skonfiguruj dodatek  

1. Otwórz [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i kliknij kartę **Project Service**.  

2. Kliknij **Połącz**.  

3. Wprowadź informacje logowania, a następnie kliknij **Zaloguj się**.  

   Teraz możesz rozpocząć korzystanie z dodatku.  

## <a name="read-from-a-template"></a>Odczytać z szablonu  
 Odczytaj z szablonu, który utworzyłeś w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i skopiowałeś do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], aby rozpocząć planowanie projektów. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Utwórz szablon projektu (Project Service Automation)](../psa/create-project-template.md)  

1.  W karcie **Project Service** kliknij **Odczytaj** > **Szablon projektu Project Service Automation**.  

2.  Wybierz szablon projektu z listy, a następnie kliknij **Otwórz**.  

    > [!NOTE]
    >  Domyślnie zadania kopiowane z szablonu do Projektu są ustawiane jako ręcznie zaplanowane.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Przypisz role [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] do zasobów projektu  

1.  Otwórz projekt, a następnie kliknij wstążkę **Zadanie**.  

2.  Kliknij menu **Wykres Gantta**, a następnie wybierz **Arkusz zasobów**.  

3.  Na karcie Arkusz zasobów kliknij menu rozwijane **Rola usługi Project Service Automation** i wybierz rolę usługi Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Zaopatrz projekt w zasoby  

1.  Na karcie Project Service zaznacz wiersz i kliknij **Znajdź zasoby**.  

2.  Na ekranie **Zarezerwuj zasoby** wybierz zasób, którego chcesz użyć dla projektu.  

3.  Kliknij **Zarezerwuj**, a następnie kliknij **OK**.  

## <a name="publish-your-project"></a>Opublikuj projekt  
Po zakończeniu planowania projektu, następnym krokiem jest importowanie i publikowanie projektu w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projektu zostanie zaimportowany do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Zastosowano proces generowania cen i zespołu. Otwórz projekt w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aby zobaczyć, że zespół, oszacowania projektu i struktura podziału pracy zostały wygenerowane. W poniższej tabeli pokazano, gdzie można znaleźć wyniki:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Wykres Gantt**   | Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Struktura podziału pracy**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Arkusz zasobów** |   Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Członkowie zespołu projektu**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Użyj użycia**    |    Importuje do ekranu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Szacowania projektów**.     |

**Aby zaimportować i opublikować projekt**  
1. W karcie **Project Service** kliknij **Opublikuj** > **Nowy projekt Project Service Automation**.  

2. W oknie dialogowym **Publikuj w nowym projekcie w Project Service** wprowadź **Nazwa projektu** i wybierz **Klient**.  

3. Opcjonalnie zaznacz **Połącz plan projektu z usługą Project Service Automation**, aby połączyć plik projektu z usługą Project Service Automation.  

4. Kliknij przycisk **Publikuj**.  

   Łączenie pliku Projekt z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sprawia, że plik Projekt staje się wzorcem i ustawia strukturę podziału pracy w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tylko do odczytu.  Aby wprowadzić zmiany do planu projektu, należy sporządzić je w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i opublikować jako aktualizacje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Edytuj projekt, który został importowany  
 Aby wprowadzić zmiany do planu projektu, który został zaimportowany do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], masz dwie opcje:  

- Otwórz plik główny i edytuj go w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Odłącz plik i edytuj go bezpośrednio w Project Service. Domyślnie, projekt, który został przekazany z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] jest zablokowany i może być edytowany tylko w programie Project. Aby edytować plik w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], pliku musi być odłączony.  

### <a name="edit-in-pn_microsoft_project"></a>Edytuj w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Z menu głównego, kliknij **Project Service** > **Projekty**.  

2. Z listy projektów otwórz ten, który został utworzony w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Kliknij **Otwórz w MS Project** ze Wstążki. Otworzy to połączony plik główny w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Odłącz plik i edytuj go w Usłudze [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Z menu głównego, kliknij **Project Service** > **Projekty**.  

2. Z listy projektów otwórz ten, który został utworzony w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Kliknij **Odłącz od MS Project** ze wstążki.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Przekazywanie pliku programu Project do programu SharePoint lub usługi Office Groups  
 Możesz przesłać plik programu Project do programu SharePoint i znaleźć go w sekcji Dokumenty związane dla Twojego projektu programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Administrator musi skonfigurować zarządzanie dokumentami programu SharePoint i włączyć je dla encji Project. 

 Możesz również przesłać plik Projekt do [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jeśli masz skonfigurowane grupy Office.

### <a name="upload-a-file-for-sharepoint"></a>Przekazywanie pliku do programu SharePoint  

1. Z menu głównego, kliknij **Project Service** > **Przekaż**.  

2. Wybierz **Do dokumentów projektu usługi Project Service Automation**.  

3. W oknie dialogowym **Włącz Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, wybierz **Tak** lub **Nie**.  

   - Po kliknięciu **Tak** będziesz w stanie wybrać przycisk **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** w Project Service Automation, uruchomić [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] oraz załadować plik programu Project z biblioteki dokumentów SharePoint.  

   - Po kliknięciu **Nie** łącze dla przycisku **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nie będzie działać.  

4. Plik [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] można znaleźć w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenty** dla danego projektu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Przekaż plik dla grup usługi Office  

1. Z menu głównego, kliknij **Project Service** > **Przekaż**.  

2. Wybierz **Do dokumentów projektu usługi Project Service Automation**.  

3. W oknie dialogowym **Włącz Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, wybierz **Tak** lub **Nie**.  

   - Po kliknięciu **Tak** będziesz w stanie wybrać przycisk **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** w Project Service Automation, uruchomić [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] oraz załadować plik programu Project z biblioteki dokumentów SharePoint.  

   - Po kliknięciu **Nie** łącze dla przycisku **Otwórz w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nie będzie działać.  

4. Plik [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] można znaleźć w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenty** dla danego projektu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Opublikuj projekt jako szablon  
 Można zapisać projekt i użyć go ponownie, zapisując go jako szablon projektu w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Szablony projektów to nadające się do wielokrotnego użytku plany projektów w [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Utwórz szablon projektu (Project Service Automation)](../psa/create-project-template.md)  

1. W karcie **Project Service** kliknij **Opublikuj** > **Nowy szablon usługi Project Service Automation**.  

2. W oknie dialogowym **Publikuj w nowym projekcie w szablonie Project Service** wprowadź **Nazwa szablonu projektu**.  

3. Opcjonalnie zaznacz **Połącz plan projektu z usługą Project Service Automation**, aby połączyć plik programu Project z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Kliknij przycisk **Publikuj**.  

Łączenie pliku Projekt z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sprawia, że plik Projekt staje się wzorcem i ustawia strukturę podziału pracy w szablonie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tylko do odczytu.  Aby wprowadzić zmiany do planu projektu, należy sporządzić je w [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i opublikować jako aktualizacje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Odczytywanie harmonogramu załadowanych zasobów

Podczas odczytywania projektu z rozwiązania Project Service Automation kalendarz zasobu nie jest synchronizowany z klientem stacjonarnym. Jeśli występują różnice między czasami trwania i pracą lub zakończeniem zadań, prawdopodobnie jest to spowodowane tym, że w przypadku zasobów i klienta stacjonarnego nie ma tego samego kalendarza szablonu godzin pracy zastosowanego do projektu.


## <a name="data-synchronization"></a>Synchronizacja danych

W poniższej tabeli przedstawiono sposób synchronizowania danych między programem Project Service Automation a dodatkiem plug-in Microsoft Project dla komputerów stacjonarnych.

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Zadanie projektu | Termin | ● | - |
| Zadanie projektu | Szacowany nakład pracy | ● | - |
| Zadanie projektu | Identyfikator klienta programu MS Project | ● | - |
| Zadanie projektu | Zadanie nadrzędne | ● | - |
| Zadanie projektu | Project | ● | - |
| Zadanie projektu | Zadanie projektu | ● | - |
| Zadanie projektu | Nazwa zadania projektu | ● | - |
| Zadanie projektu | Jednostka zasobów (przestarzałe w wersji 3.0) | ● | - |
| Zadanie projektu | Zaplanowany czas trwania | ● | - |
| Zadanie projektu | Data rozpoczęcia | ● | - |
| Zadanie projektu | Identyfikator SPP | ● | - |

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Członek zespołu | Identyfikator klienta programu MS Project | ● | - |
| Członek zespołu | Nazwa stanowiska | ● | - |
| Członek zespołu | projekt | ● | ● |
| Członek zespołu | Zespół projektu | ● | ● |
| Członek zespołu | Jednostka zasobów | - | ● |
| Członek zespołu | Rola | - | ● |
| Członek zespołu | Godziny pracy | Nie zsynchronizowano | Nie zsynchronizowano |

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Przypisanie zasobu | Od daty | ● | - |
| Przypisanie zasobu | godzin(y) | ● | - |
| Przypisanie zasobu | Identyfikator klienta programu MS Project | ● | - |
| Przypisanie zasobu | Zaplanowana praca | ● | - |
| Przypisanie zasobu | Project | ● | - |
| Przypisanie zasobu | Zespół projektu | ● | - |
| Przypisanie zasobu | Przypisanie zasobu | ● | - |
| Przypisanie zasobu | Zadanie | ● | - |
| Przypisanie zasobu | Do daty | ● | - |

| **Encja** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Zależności zadań projektu | Zależność zadania projektu | ● | - |
| Zależności zadań projektu | Typ łącza | ● | - |
| Zależności zadań projektu | Zadanie poprzedzające | ● | - |
| Zależności zadań projektu | Project | ● | - |
| Zależności zadań projektu | Zadanie następujące | ● | - |

### <a name="see-also"></a>Zobacz także  
 [Przewodnik menedżera projektu](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]