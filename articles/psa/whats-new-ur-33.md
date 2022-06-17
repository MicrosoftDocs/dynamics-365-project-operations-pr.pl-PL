---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 33, wer. 3
description: W tym artykule przedstawiono funkcje i poprawki dostępne w programie Project Service Automation, wydanie aktualizacji 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915429"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 33, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym artykule przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation V3, wydanie aktualizacji 33. Ta wersja zawiera numer kompilacji V3.10.54.98 i jest ogólnie dostępna w ramach samoobsługowej aktualizacji z lipca 2021 r.

## <a name="update-release-33"></a>Wydanie 33

### <a name="bug-fixes"></a>Poprawki błędów

**Czas i wydatek**

Rozwiązano następujące problemy:

- Dwa zablokowane pola, **msdyn_description** i **msdyn_externaldescription**, można edytować po przesłaniu.
- Jeśli zostanie utworzony koszt niepowiązany z projektem, pojawia się komunikat o błędzie.
- Po utworzeniu wpisu czasu rola zasobu jest domyślnie ustawiana na rolę nieaktywną.
- Wiersze arkusza skojarzone z wycofanym i usuniętym wydatkiem nie są usuwane.
- W **formularzu szybkiego tworzenia wpisu czasu** zaktualizuj widok **Lista zadań projektu**, aby zmienić wyświetlaną domyślnie datę na datę rozpoczęcia zadania.
- Podczas tworzenia wpisu czasu na karcie **Pokrewne** zasobu do zarezerwowania wpis czasu jest niepoprawnie tworzony dla zalogowanego użytkownika, zamiast nadrzędnego zasobu, który można zarezerwować.
- Nowe pola zostaną dodane do okna dialogowego **zbiorczego zatwierdzania (MDD)**.

**Planowanie projektu**

Rozwiązano następujące problemy:
- Mała wydajność tworzenia projektów w przypadku stosowania szablonów godzin pracy projektu w złożonych kalendarzach.
- Gdy data rozpoczęcia jest późniejsza niż data zakończenia, w szablonie kopii szablonu projektu jest wyświetlany błąd z powodu różnic w składniku czasowym poszczególnych pól.

**Zarządzanie zasobami**

Rozwiązano następujące problemy:
- Niepoprawny parametr jest używany w zapytaniu wykorzystania zasobów i kodzie XML, co prowadzi do niepoprawnych wyników filtrowania w siatce **wykorzystania zasobów**.
- Potwierdzenie **rozszerzenia rezerwacji** powoduje wyświetlenie nieprawidłowej daty zakończenia rezerwacji.

**Sprzedaż**

Rozwiązano następujące problemy:
- Komunikat o błędzie pojawia się, jeśli cena kategorii jest tworzona z brakującymi wartościami.
- Komunikat o błędzie pojawia się w przypadku utworzenia kamienia milowego pozycji kontraktu bez wiersza zamówienia.
