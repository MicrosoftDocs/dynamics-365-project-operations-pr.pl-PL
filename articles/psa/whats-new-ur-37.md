---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 37, V3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593487"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 37, V3. Ta wersja ma numer kompilacji V3.10.58.120 i jest ogólnie dostępna po samodzielnej aktualizacji w listopadzie 2021 r.

## <a name="update-release-37"></a>Wydanie 37

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Czas i wydatek**
- Użytkownicy nie mogą usunąć wpisu czasu przez wyczyszczenie komórki.
- Widok **Moje nieudane zatwierdzenie** zawiera tylko zatwierdzenie projektu o stanie **Przesłane**.

**Zarządzanie projektem**
- Użytkownicy otrzymują błąd wyjątku odwołania o wartości null podczas otwierania projektu w dodatku Microsoft Desktop, jeśli nazwa stanowiska członka zespołu projektu jest pusta.
- Nie ma przycisku **Zapisz** na stronie **Zadanie projektu**, więc użytkownicy nie mogą zapisywać zmian w rekordach zadań.
- Użytkownicy nie mogą usunąć projektu, z zadaniem skojarzonym z ofertą, która ma stan **Wygrana**.

**Sprzedaż**
- Pole **Waluta** na stronie **Projekt** zostało zaktualizowane, aby odpowiadało walucie zastosowanego szablonu.
- Koszt jest obliczany niepoprawnie dla zadań, które mają wiele walut.
