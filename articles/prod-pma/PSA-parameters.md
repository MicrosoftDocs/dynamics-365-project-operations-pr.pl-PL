---
title: Parametry integracji Project Service Automation z Finance
description: W tym temacie wyjaśniono, jak skonfigurować sposób wprowadzania danych domyślnych podczas integracji Microsoft Dynamics 365 for Project Service Automation z Microsoft Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a0cee090e0ecb306aa3bda62c79a57dfade93c0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082152"
---
# <a name="project-service-automation-integration-parameters"></a>Parametry integracji Project Service Automation z Finance

[!include[banner](../includes/banner.md)]

Na stronie **parametry integracji rozwiązania Project Service Automation** można skonfigurować sposób wprowadzania danych domyślnych podczas integracji Dynamics 365 Project Service Automation z Dynamics 365 Finance. Aby projekty zostały pomyślnie zsynchronizowane z Project Service Automation do Finance, należy skonfigurować następujące pola.

Aby otworzyć stronę **parametry integracji z Project Service Automation** , wybierz **Zarządzanie projektami i księgowanie** \> **Ustawienia** \> **Parametry integracji Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - W wersji 8,0 udostępniono integrację zadań projektu, kategorie transakcji wydatkowej, oszacowania godzin, oszacowania kosztów i blokadę funkcji.
> - Integracja danych rzeczywistych jest dostępna w wersji 8.0.1 lub nowszej.


| Zakładka                    | Pole                | Opis |
|------------------------|----------------------|-------------|
| Ogólne                | Domyślny typ projektu | Wybierz domyślny typ projektu. Jeśli projekty są synchronizowane z rozwiązania Project Service Automation, ta wartość jest używana, jeśli w szablonie integracji nie została wybrana wartość domyślna. Podczas synchronizacji pole **Typ projektu** dla nowych projektów ma ustawioną tę wartość. Jednak wartość może zostać zaktualizowana w momencie, gdy pozycje kontraktu projektu zostaną zsynchronizowane z rozwiązania Project Service Automation. |
|                        | Kategoria czasu        | Wybierz domyślną kategorię czasową. Ta wartość jest używana przy synchronizowaniu oszacowania godzinnego z rozwiązania Project Service Automation. Kiedy wartości szacunkowe godzin i godzin są synchronizowane z rozwiązania Project Service Automation, pole **Kategoria** w nowych prognozach godzin projektów w Finance ma ustawioną tę wartość. |
|                        | Kategoria opłat         | Wybierz domyślną kategorię opłat. Ta wartość jest używana, gdy wartości rzeczywiste opłat są synchronizowane z Project Service Automation. Kiedy wartości rzeczywiste opłat i godzin są synchronizowane z rozwiązania Project Service Automation, pole **Kategoria** w nowych opłatach za transakcje w Finance ma ustawioną tę wartość. |
| Domyślne ustawienia grup projektów | Typ projektu         | Kliknij pozycję **Nowy** , aby dodać wiersz, w którym można wybrać typ projektu, dla którego ma zostać ustawiona domyślna grupa projektów. Określony typ projektu może być wybierany w konfiguracji tylko raz. |
|                        | Grupa projektów        | Wybierz grupę domyślnych projektów dla wybranego typu projektu. Kiedy nowe projekty są synchronizowane z rozwiązania Project Service Automation, w polu **Grupa projektów** jest ustawiona wartość domyślna dla typu projektu, jeśli szablon integracji nie zawiera wartości domyślnej. |
| Domyślne typy fakturowania  | Typ rozliczania         | Kliknij opcję **Nowy** , aby dodać wiersz, w którym można wybrać typ rozliczenia, dla którego ustawić domyślną właściwość linii. Określony typ rozliczenia można wybrać tylko raz w konfiguracji. |
|                        | Właściwość wiersza        | Wybierz domyślną właściwość linii dla wybranego typu rozliczenia. Gdy nowe szacunki godzinowe, nowe szacunki wydatków lub nowe wartości rzeczywiste są synchronizowane z Project Service Automation, pole **Właściwości wiersz** jest ustawiane na wartość domyślną dla typu rozliczenia. |
| Blokowanie funkcjonalności  | Nie dotyczy       | Wybierz funkcję do wyłączenia w Finance dla projektów i umów, które pochodzą z Project Service Automation. Na przykład można wyłączyć możliwość edytowania umów i projektów, tworzenia struktur podziału pracy i wprowadzania grafików pracy w Finance. Pola związane z księgowością będą nadal aktywne, nawet jeśli są niedostępne przez ustawienie parametru. Domyślnie wszystkie funkcje są włączone. |
