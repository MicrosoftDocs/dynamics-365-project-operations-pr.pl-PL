---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 40, wer. 3
description: W tym artykule przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912805"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 40, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 40, V3. Ta wersja ma numer kompilacji V3.10.61.61 i jest ogólnie dostępna za pośrednictwem samodzielnej aktualizacji w lutym 2022 r.

## <a name="update-release-40"></a>Wydanie 40

### <a name="features"></a>Funkcje
Etap 1 uaktualnienia z rozwiązania Project Service Automation do wersji Project Operations — Zespołu zostanie wydane w lutym 2022 r. dla wszystkich klientów. Aby sprawdzić uprawnienia, zobacz [Uaktualnianie rozwiązania Project Service Automation do Project Operations](upgrade-project-operations-non-stocked.md). Jeśli aplikacja nie jest wyświetlana w Wystąpieniu użytkownika w Centrum administracyjnym Power Platform, należy skontaktować się z pomocą techniczną i zażądać, aby włączyć obsługę środowiska. Żądanie musi zawierać listę identyfikatorów środowiska, dla których trzeba włączyć funkcję.

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Czas i wydatek**
- W przypadku odrzucenia lub anulowania wpisu czasu nie ma wpisu notatki. 

**Sprzedaż**

- Podczas aktualizowania szacowanych kosztów lub sprzedaży przy użyciu zainstalowanych już dodateków plug-in istnieje nieprawidłowe uprawnienia do wysyłania ładunków JSON, które nie są prawidłowe poza interfejsem użytkownika.
- Podczas aktualizowania wierszy oferty przy użyciu widoku szybkiego widoku można aktywować oferty.
