---
title: Włącz funkcje aplikacji Project Finder Mobile
description: Włączanie funkcji aplikacji Project Finder Mobile dla Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144561"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Włącz funkcje aplikacji Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Twoje zasoby mogą korzystać z aplikacji Project Finder Mobile na telefonie z [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aby znajdować nowe projekty, nad którymi mogą pracować, lub aby aktualizować posiadane umiejętności.  
  
 Aplikacja jest dostępna na telefony [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Aby umożliwić użytkownikom przeglądanie wymagań dotyczących zasobów projektu i aktualizowanie umiejętności, w ustawieniach parametrów jednostki organizacyjnej należy wybrać opcje.
  
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
|Menedżer projektu|- Zasób zgłasza się do projektu za pomocą aplikacji Project Finder Mobile.|  
|Zasób|- Prace związane z projektem, do którego zasób się zgłosił, zostały już zrealizowane przez inny zasób.<br />- Żądanie zatwierdzenia umiejętności zostało zatwierdzone lub odrzucone.<br />- Żądanie zgłoszenia się do projektu zostało zatwierdzone lub odrzucone.|  
  
## <a name="privacy-notice"></a>Oświadczenie o ochronie prywatności  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Zobacz także  
 [Konfigurowanie zasobów](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]