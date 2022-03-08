---
title: Definiowanie kalendarzy projektu
description: Ten temat zawiera informacje na temat stosowania szablonu kalendarza projektu w celu śledzenia harmonogramu projektu.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 181032b27ee67591a3bb40ab080477c51c1e34a46e9aac20039e4e5df3a5ab1d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000949"
---
# <a name="define-project-calendars"></a>Definiowanie kalendarzy projektu

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

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

Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

