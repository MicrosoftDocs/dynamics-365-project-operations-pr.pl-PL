---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 42, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589209"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 42, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 42, wer. 3. Ta wersja ma numer kompilacji V3.10.73.61 i zazwyczaj jest dostępna za pośrednictwem samoaktualizacji w kwietniu 2022 r.

## <a name="update-release-42"></a>Wydanie 42

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Czas i wydatek**

- W przypadku odrzucenia arkusza czasu użytkownik, który go odrzucił, jest niepoprawnie identyfikowany jako **System**.
- Podczas importowania wpisów czasu brakuje wartości **Kategoria zasobu**.
- Osoby zatwierdzające projekt mogą zatwierdzać przesłane projekty, jeśli ich uprawnienia nie mają specjalnie ustawionej dla nich ustawienia **Może zatwierdzić**.

**Sprzedaż**

- Gdy wartości rzeczywiste są rejestrowane w zadaniach nie root, koszty rzeczywiste są niepoprawnie agregowane.
