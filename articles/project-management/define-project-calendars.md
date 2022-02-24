---
title: Definiowanie kalendarzy projektu
description: Ten temat zawiera informacje na temat stosowania szablonu kalendarza projektu w celu śledzenia harmonogramu projektu.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981313"
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
3. Wybierz kartę **Godziny pracy** zasobu i wykonaj instrukcje z [Ustawianie godzin pracy dla zasobu](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) w celu skonfigurowania reguł kalendarza.

**Utwórz nowy szablon kalendarza**

1. Wybierz kolejno opcje **Ustawienia** \> **Szablon kalendarza**.
2. Wybierz opcję **Nowy** i wprowadź nazwę, opis i zasób szablonu.

> [!NOTE]
> Kiedy do zasobu odwołuje się szablon kalendarza, kopia kalendarza zasobu jest skojarzona z szablonem kalendarza. Jeśli godziny pracy skopiowanego szablonu ulegną zmianie, zmiany te nie zostaną przeniesione do szablonu kalendarza.

Szablon pracy można teraz skojarzyć z szablonem kalendarza projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

