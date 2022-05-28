---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 39, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588749"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 39, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 39, wer. 3. Numer tej kompilacji to V3.10.60.170 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2022 r.

## <a name="update-release-39"></a>Wydanie 39

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Ogólne**

- W mapce witryny w przypadku tłumaczenia arabskiego wprowadzono kilka udoskonaleń.

**Zarządzanie projektem**

- Błąd występuje, gdy menedżer projektu jest zmieniany na użytkownika, który już jest członkiem zespołu projektu.

**Sprzedaż**

- Właściciel cennika kontraktu **projektu jest niepoprawny** podczas automatycznego tworzenia cennika. 
- Efekt efektności daty dla cennika nie jest honorowany po zastosowaniu cennika do parametru projektu.
- Jednostka kontraktu może nie mieć poprawnej wartości domyślnej podczas edytowania dwóch osobnych ofert.
