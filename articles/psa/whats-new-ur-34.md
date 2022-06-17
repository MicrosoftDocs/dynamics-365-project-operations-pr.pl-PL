---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 34, wer. 3
description: W tym artykule przedstawiono funkcje i poprawki dostępne w programie Project Service Automation, wydanie aktualizacji 34, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928675"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 34, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation V3, wydanie aktualizacji 34. Ta wersja zawiera numer kompilacji V3.10.55.38 i jest ogólnie dostępna w ramach samoobsługowej aktualizacji z lipca 2021 r.

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
