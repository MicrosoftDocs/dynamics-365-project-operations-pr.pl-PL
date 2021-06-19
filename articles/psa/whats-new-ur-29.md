---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 29, wer. V3
description: W tym temacie wymieniono funkcje i poprawki, które są dostępne w aktualizacji Project Service Automation, wydanie 29, wersja V3.
author: ruhercul
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010484"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie aktualizacji 29, wer. V3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność ogłosić najnowszą aktualizację aplikacji Project Service Automation dla Dynamics 365. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź centrum administracyjne Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

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