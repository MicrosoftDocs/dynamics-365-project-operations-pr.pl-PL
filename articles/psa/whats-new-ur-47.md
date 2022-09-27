---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 47, wer. 3
description: W tym artykule przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 47, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477240"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 47, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 45, V3. Ta wersja zawiera numer kompilacji V3.10.78.8 i jest ogólnie dostępna w ramach samoobsługowej aktualizacji z lipca 2022 r.

## <a name="update-release-47"></a>Wydanie 47

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Zarządzanie zasobami**
- Zaktualizowano walidację, aby użytkownicy nie mogli wywołać wyjątku null reference podczas próby utworzenia Członka Zespołu Projektowego bez **Zasobu możliwego do zarezerwowania**.
