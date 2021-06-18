---
title: Zarządzanie projektami i rezerwacjami w kalendarzu usługi Office 365
description: Jak zarządzać projektami i rezerwacjami w kalendarzu usługi Office 365
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 575f3c94f886d12717496445d0e6357fdc01246b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000404"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Zarządzanie projektami i rezerwacjami w kalendarzu (Project Service)

> [!Note]
> PRZESTARZAŁE: Ta funkcja została uznana za przestarzałą i nie jest już dostępna.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Wyświetlaj terminy prywatne, rezerwacje pracy nad projektem i przydziały zleceń pracy dla usług Field Service za pomocą kalendarza [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Wszystko masz w jednym miejscu, więc zarządzanie dniem jest łatwe. Spotkania, terminy, rezerwacje i zadania są dostępne w kalendarzu [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Jeśli używasz [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], możesz również wprowadzić terminy prywatne w widoku wprowadzania czasu usługi Project Service. Dzięki temu menedżerowie zasobów i projektów znają Twoją dostępność dla projektów. Pozwala to również zaoszczędzić czas, ponieważ nie musisz dwukrotnie wprowadzać informacji na temat Twoich terminów prywatnych. Można po prostu importować terminy prywatne z kalendarza do widoku wprowadzania czasu Project Service.  
  
 Twój kalendarz zsynchronizuje projekt i rezerwacje zamówień roboczych od dnia dzisiejszego przez nadchodzące cztery tygodnie. To ustawienie można zmienić.  
  
 Synchronizacja jest obsługiwana tylko w jedną stronę, z PSA do kalendarza [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Synchronizację można przeprowadzić w odwrotnej kolejności. 
  
 Aby dowiedzieć się, jak używać kalendarza [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], zobacz [Kalendarz w programie Outlook w sieci Web dla firm](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Konfiguracja  
 Zanim będzie można zobaczyć rezerwacje w kalendarzu [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], musisz przeprowadzić kilka ustaleń.  
  
- Będą konieczne poświadczenia administratora globalnego [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] lub administratora systemu.  
  
- Administrator będzie musiał skonfigurować profil serwera poczty e-mail i każdy użytkownik będzie musiał skonfigurować swoją skrzynkę pocztową. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Skonfiguruj przetwarzanie wiadomości e-mail przez synchronizację na serwerze](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Włącz synchronizację dla organizacji (zadanie administratora)  
  
1.  Z menu głównego, kliknij **Ustawienia** > **Administracja**.  
  
2.  Kliknij pozycję **Ustawienia systemu**.  
  
3.  Kliknij kartę **Synchronizacja**.  
  
4.  W **Określ, czy chcesz włączyć synchronizację rezerwowania zasobów z**, zaznacz **Synchronizuj rezerwację zasobów z programem Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Włączyć synchronizację dla profilu użytkownika (zadanie użytkownika)  
  
1.  Kliknij przycisk **Ustawienia** w prawym górnym rogu ekranu.  
  
2.  Kliknij **Opcje**.  
  
3.  Kliknij kartę **Synchronizacja**.  
  
4.  W **Synchronizacja rezerwacji zasobów z programem Outlook**, zaznacz **Synchronizuj rezerwację zasobów z programem Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importuj terminy prywatne (zadanie użytkownika)  
 Można importować terminy prywatne z kalendarza do widoku wprowadzania czasu Project Service Automation.  
  
1. Otwórz kalendarz [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] i kliknij **Importuj dane**.  
  
2. Na ekranie Filtry, wybierz **Termin z Exchange** i kliknij **Zastosuj**.  
  
3. System wyciągnie terminy do widoku wpisów czasu jako sugerowane wpisy z bieżącego tygodnia. Aby dodać wpisy dla innego tygodnia, kliknij **Poprzedni** lub **Następny**.  
  
4. Wybierz termin, który chcesz dodać do widoku wpisów czasu Project Service Automation.  
  
5. W wyskakującym okienku **Wpis czasu** zaznacz odpowiednie opcje, aby przekonwertować termin na widok wpis czasu Project Service Automation.  
  
6. Kliknij przycisk **Zapisz**.  
  
### <a name="see-also"></a>Zobacz także  
 [Przewodnik dotyczący czasu, wydatków i współpracy](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]