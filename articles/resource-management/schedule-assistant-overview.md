---
title: Omówienie asystenta planowania
description: W tym temacie zamieszczono informacje dotyczące pracy z asystentem planowania zasobów w celu ich rezerwowania.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125641"
---
# <a name="schedule-assistant-overview"></a>Omówienie asystenta planowania

_**Ma zastosowanie do:** Project Operations dotyczące scenariuszy z zasobami i zasobami niemagazynowanymi, lekkiego wdrażania — od transakcji do fakturowania proforma_

Asystent planowania jest używany do rezerwowania zasobów na podstawie wymagań określonych przez menedżera projektu. Asystent planowania opiera się na parametrach zawartych w wymaganiu zasobu w celu wyszukania danego zasobu. Asystent planowania rekomenduje zasoby spełniające odpowiednie wymagania, takie jak czas i potrzebne umiejętności.

Po zidentyfikowaniu odpowiednich zasobów, menedżer zasobów lub menedżer projektu może dokonać jego rezerwacji na zadania.

## <a name="prerequisites"></a>Wymagania wstępne

Asystent planowania jest częścią rozwiązania Universal Resource Scheduling. To rozwiązanie jest dołączone i instalowane wraz z Dynamics 365 Project Operations, Dynamics 365 Field Service i Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Dopasowywanie wymagań i zasobów

Zapotrzebowanie wygenerowanego zasobu jest oparte na szczegółach, takich jak:

-   Charakterystyki
-   Role
-   Jednostki biznesowe
-   Preferencje dotyczące zasobu
-   Rozkłady nakładów
-   Strefa czasowa

Asystent planowania używa tych szczegółów do filtrowania zasobów.

## <a name="launch-the-schedule-assistant"></a>Uruchom asystenta planowania

Istnieją dwa sposoby uruchamiania asystenta planowania. W przypadku korzystania z trybu hybrydowego w siatce członków zespołu można wybrać dowolnego członka zespołu z niezrealizowanym wymaganiem dotyczącym zasobów, a następnie wybrać opcję **Rezerwacja**. W przypadku korzystania z trybu centralnego menedżer zasobów znajduje i wybiera zasób.

## <a name="schedule-assistant-filters"></a>Filtr asystenta planowania

Po uruchomieniu asystenta planowania szczegóły dotyczące wymagania zasobu są wyświetlane jako filtrowane wartości w lewym okienku. Wyniki może dostosować menedżer zasobów lub menedżer projektu, dopasowując filtry w celu zaspokojenia potrzeb planowania.

W okienku filtru są wyświetlane opcje związane z pracą, w tym:

-   Data rozpoczęcia i zakończenia pracy
-   Charakterystyki
-   Role
-   Jednostki organizacyjne
-   Firma zasobów
-   Typy zasobów
-   Preferowane zasoby
