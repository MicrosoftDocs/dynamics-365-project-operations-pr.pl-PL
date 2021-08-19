---
title: Tworzenie szablonu godzin pracy
description: W tym temacie opisano tworzenie szablonu godzin pracy w Project Service.
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987404"
---
# <a name="create-a-work-hours-template-project-service"></a>Twórz szablon godzin pracy (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Aby utworzyć projekt i zarządzać nim, należy zastosować do projektu szablon kalendarza. W szablonie kalendarza są następujące atrybuty projektu:

- Godziny pracy, w tym godzina rozpoczęcia i zakończenia
- Dni robocze
- Wyjątki kalendarzowe, np. dni niepracujące

Szablon kalendarza zastosowany do projektu jest kopią szablonu kalendarza zdefiniowanego w ustawieniach organizacji.

> [!NOTE]
> W przypadku zmiany szablonu kalendarza te zmiany nie są przenoszone na godziny pracy projektu. Aby zmienić godziny pracy projektu, należy zastosować nowy szablon.

Aby utworzyć szablon kalendarza dla organizacji, należy spełnić dwa najważniejsze wymagania:

- Definiować wymagane godziny pracy szablonu przy użyciu nowego lub istniejącego zasobu, który można zarezerwować.
- Utworzyć nowy szablon kalendarza i skojarzyć szablon z zasobem, który można zarezerwować.

**Określenie godzin pracy — szablon**

1. Wybierz kolejno opcje **Zasoby** \> **Zasoby**.
2. Utwórz nowy zasób, do który chcesz się odwoływać w szablonie kalendarza lub wybierz istniejący zasób.
3. Wybierz kartę **Godziny pracy** zasobu i wykonaj instrukcje z [Ustawianie godzin pracy dla zasobu](/dynamics365/field-service/set-work-hours-resource.md) w celu skonfigurowania reguł kalendarza.

**Utwórz nowy szablon kalendarza**

1. Wybierz kolejno opcje **Ustawienia** \> **Szablon kalendarza**.
2. Wybierz opcję **Nowy** i wprowadź nazwę, opis i zasób szablonu.


> [!NOTE]
> Kiedy do zasobu odwołuje się szablon kalendarza, kopia kalendarza zasobu jest skojarzona z szablonem kalendarza. Jeśli godziny pracy skopiowanego szablonu ulegną zmianie, zmiany te nie zostaną przeniesione do szablonu kalendarza.


### <a name="see-also"></a>Zobacz także  
 [Ustawianie zasobów](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
