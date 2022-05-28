---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 43, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710042"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 43, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest on zgodny z usługą Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 43, wer. 3. Ta wersja ma numer kompilacji wer. V3.10.74.200 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w maju 2022 r.

## <a name="update-release-43"></a>Wydanie 43

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.


**Czas i wydatek**

- Importowanie wpisów czasu z rezerwacji lub przypisań zasobów nie jest zachowywane odwołanie do pokrewnego zasobu, który można zarezerwować.
- Po rozwinięciu siatki wprowadzania czasu do pełnego ekranu nawigacja po siatce przy użyciu klawisza tabulatora nie działa.
- W przypadku przesyłania wpisu czasu utworzonego przez innego użytkownika pole **Przesłane** przez jest niepoprawnie wypełniane przy użyciu użytkownika, który utworzył arkusz czasowy.
