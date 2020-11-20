---
title: Włącz funkcje aplikacji Project Finder Mobile
description: Włączanie funkcji aplikacji Project Finder Mobile dla Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132976"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Włącz funkcje aplikacji Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Twoje zasoby mogą korzystać z aplikacji Project Finder Mobile na telefonie z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aby znajdować nowe projekty, nad którymi mogą pracować, lub aby aktualizować posiadane umiejętności.  
  
 Aplikacja jest dostępna na telefony [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Należy ustawić kilka opcji w ustawieniach parametrów dla Twojego jednostki organizacyjnej, aby zezwolić użytkownikom na wyświetlanie wymagań związanych z zasobami dla projektów oraz na aktualizowanie ich umiejętności.  
  
> [!NOTE]
>  Aplikacja Project Finder Mobile działa tylko z [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], nie działa na urządzeniach lokalnych.  
  
1. Przejdź do **Project Service > Parametry**.  
  
2. Kliknij ustawienia parametrów, których chcesz używać dla umożliwienia funkcji aplikacji Project Finder Mobile.  
  
3. W obszarze **Ogólne** ustaw **Wymagania dotyczące zasobów są widoczne dla zasobów** na **Tak**.  
  
4. Ustaw **Zezwalaj na aktualizowanie umiejętności przez zasób** na **Tak**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   To ustawienie globalne. Menedżerowie projektów mogą określić, czy pojedynczy projekt będzie widoczny na stronie **Zespół projektu** tego projektu.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Powiadomienia e-mail  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wysyła wiadomości e-mail dotyczące żądań zasobów do następujących adresatów w następujących godzinach:  
  
|Odbiorca|Wydarzenie|  
|---------------|-----------|  
|Menedżer projektu|-   Kiedy zasób zgłasza się do projektu za pomocą aplikacji Project Finder Mobile.|  
|Zasób|-   Kiedy prace związane z projektem, do którego zasób się zgłosił, zostały już zrealizowane przez inny zasób.<br />-   Kiedy żądanie zatwierdzenia umiejętności zostało zatwierdzone lub odrzucone.<br />-   Kiedy żądanie zgłoszenia się do projektu zostało zatwierdzone lub odrzucone.|  
  
## <a name="privacy-notice"></a>Zasady zachowania poufności informacji  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Zobacz także  
 [Konfigurowanie zasobów](../psa/set-up-resources.md)
