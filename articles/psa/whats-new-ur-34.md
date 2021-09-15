---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 34, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Project Service Automation, aktualizacja 34, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323294"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 34, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie wymieniono nowe lub zmienione funkcje i poprawki programu Project Service Automation, wer. 3, aktualizacja 34. Ta wersja zawiera numer kompilacji V3.10.55.38 i jest ogólnie dostępna w ramach samoobsługowej aktualizacji z lipca 2021 r.

## <a name="update-release-34"></a>Wydanie 34

### <a name="bug-fixes"></a>Poprawki błędów
Rozwiązano następujące problemy.

**Ogólne**

- Aktualizacje kontrolowane przez wydawcę nie aktywują nowego nowoczesnego przepływu pracy zatwierdzania.
- Brakuje atrybutów **Stan docelowy** i **Typ akcji** na stronie głównej **Zestawu zatwierdzeń**.

**Czas i wydatek**

- Nie można zatwierdzić żądania wycofania przy użyciu nowoczesnego procesu zatwierdzania.
- Kopiowanie wpisów tygodniowych nie działa podczas kopiowania wpisów, które nie są związane z zalogowanym użytkownikiem.

**Planowanie projektu**

- Kontury przydziału zasobów są uszkodzone podczas importowania z dodatku pulpitu programu Microsoft Project.

**Zarządzanie zasobami**

- Podczas publikowania projektu z dodatku klienta pulpitu Microsoft Project zmienia się data zakończenia istniejących wymagań.
- Dokładność dziesiętna przekracza dwa miejsca po przecinku w oknie dialogowym potwierdzenia przedłużenia rezerwacji.

**Sprzedaż**

- Po dodaniu wiersza opartego na produkcie z istniejącym produktem do umowy dotyczącej projektu wyświetlany jest wyjątek **klucz nie znaleziony w słowniku**.
- Potencjalnych klientów nie można zakwalifikować, gdy typ zamówienia jest mapowany z potencjalnego klienta do możliwości.
