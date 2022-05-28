---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 41, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580929"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 41, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 41, wer. 3. Numer tej kompilacji to V3.10.62.162 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w marcu 2022 r.

## <a name="update-release-41"></a>Wydanie 41

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Zarządzanie projektem**
- Podczas próby utworzenia projektu na podstawie szablonu, który jest oparty na projekcie utworzonym za pomocą dodatku na komputery stacjonarne, wyświetlany jest następujący błąd: „Weryfikacja pola Planowana praca przydziału zasobów: data końcowa każdego wycinka czasu przydziału zasobów nie może być wcześniejsza niż jego początkowa Data".

**Czas i wydatek**
- Podczas próby usunięcia wpisu czasu wyświetlany jest następujący komunikat o błędzie „Wystąpił nieoczekiwany błąd z kodu ISV”.

**Sprzedaż**
- Podczas tworzenia faktury dla punktu kontrolnego stałej ceny pola **Opis** i **Opis zewnętrzny** nie są wypełniane. 
