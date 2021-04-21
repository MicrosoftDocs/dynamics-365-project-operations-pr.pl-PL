---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 29, wer. V3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 29, wersja V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664656"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 29, wer. V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

W tym temacie wymieniono funkcje i poprawki, które są nowe lub zmienione w programie Project Service Automation V3, aktualizacja wydanie 29. Ta wersja ma numer kompilacji V3.10.47.7 i jest ogólnie dostępna za pośrednictwem samodzielnej aktualizacji w lutym 2021 r.

## <a name="update-release-29"></a>Wydanie 29

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:

- Użytkownicy nie widzą godzin pracy zalogowanych w dniach wolnych od pracy w siatce wprowadzania czasu.
- Zatwierdzone zapisy wydatków mogą być edytowane w siatce.

**Zarządzanie projektem**

Rozwiązano następujące problemy:

- Brak logiki sprawdzania poprawności, w celu upewnienia się, że godziny nakładu pracy przypisania zasobów nie mogą być ujemne.
- Akcja niestandardowa **AssignResourcesForTask** aktualizuje wszystkie pola, a nie tylko zmienione pola.
- Podczas kopiowania projektu w środowisku z dodatkami lub przepływami pracy, które są zarejestrowane w zdarzeniu **CreateProject**, atrybut **msdyn_bulkgenerationstatus** nie jest aktualizowany, jeśli **CopyWBSToProject** nie powiedzie się.
- Po rozwinięciu kalendarza projektu dni robocze nie są sortowane w kolejności rosnącej, co powoduje niepowodzenie niektórych aktualizacji zadań projektu.
- Zmiana menedżera projektu w istniejącym projekcie wyzwala logikę domyślnego działania jednostki organizacyjnej.

**Sprzedaż**

Rozwiązano następujące problemy:

- Karta **Wydajność kontraktu** na stronie **Kontrakt** nie powiedzie się podczas inicjowania, gdy nie ma żadnych pozycji kontraktu.
