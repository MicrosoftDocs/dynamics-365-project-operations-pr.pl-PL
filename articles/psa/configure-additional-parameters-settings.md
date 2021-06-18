---
title: Konfigurowanie ustawień dodatkowych parametrów
description: Konfigurowanie ustawień dodatkowych parametrów w Project Service
author: JohnPBurrows
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
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001124"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Konfiguruj ustawienia dodatkowych parametrów (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Po skonfigurowaniu elementów w poprzednich tematach, należy ustawić dodatkowe parametry projektów, jakie mają być używane dla Twoich projektów. Podczas pierwszej instalacji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] utworzyłeś ustawienia parametrów, aby najpierw utworzyć wszystkie rekordy wymagane dla [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Teraz nadszedł czas, aby wrócić i skonfigurować dodatkowe pola dla tych ustawień.  
  
 Musisz skonfigurować następujące ustawienia:  
  
-   Jednostka organizacyjna  
  
-   Częstotliwość faktur  
  
-   Szablon godzin pracy  
  
-   Cennik  
 
W tym kroku wskażesz również żądany typ alokacji zasobów:  
  
- **Centralny**. Tylko menedżerowie zasobów mogą przydzielać zasoby do projektów.  
  
- **Hybrydowy**. Menedżerowie zasobów, menedżerowie projektów i menedżerowie kont mogą przydzielać zasoby do projektów.  
  
 
Aby określić parametry projektu:  
  
1. Przejdź do **Project Service > Parametry**.  
  
2. Kliknij ustawienia parametrów, które chcesz skonfigurować (to utworzone podczas pierwszej instalacji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), lub kliknij **Nowe**, aby utworzyć nowe ustawienie.  
  
3. W obszarze **Ogólne**, ustaw wszystkie opcje dla parametrów Twojego projektu.  
  
4. W obszarze **Cennik** kliknij **+**, aby dodać cennik, wybierz cennik z listy rozwijanej **Cennik parametrów projektu** a następnie kliknij **Zapisz**.  
  
5. Kliknij przycisk **Zapisz** w prawym dolnym rogu ekranu.  

> [!NOTE]
> Aby usługa Project Service działała prawidłowo, musi zostać zachowany rekord parametru projektu. Ten rekord nie powinien być usuwany.

### <a name="see-also"></a>Zobacz także  
 [Konfigurowanie zasobów](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]