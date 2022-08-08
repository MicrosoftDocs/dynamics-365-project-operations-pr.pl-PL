---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 45, V3
description: W tym artykule przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169163"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 45, V3. Ta wersja zawiera numer kompilacji V3.10.76.168 i jest ogólnie dostępna w ramach samoobsługowej aktualizacji z lipca 2022 r.

## <a name="update-release-45"></a>Wydanie 45

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Sprzedaż**

- Użytkownicy nie mogą pomyślnie tworzyć faktur po próbie utworzenia faktury bez nierozliczonej sprzedaży, jeśli przeglądają również to samo wystąpienie strony i nie odświeżają jej.

**Czas i wydatek**

- Po włączeniu funkcji Modern Approvals i zatwierdzeniu wycofanego zatwierdzenia projektu etap rejestrowania jest niepoprawnie aktualizowany do **Zatwierdzone żądanie prośby o zatwierdzenie**.
- Gdy nowoczesne zatwierdzanie jest włączone, a Cloud Flows jest nieaktywne, proces zatwierdzania nie kończy się pomyślnie, a przesyłający lub zatwierdzający użytkownicy nie są powiadamiani.
