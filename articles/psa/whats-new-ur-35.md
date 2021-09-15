---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 35, wer. 3
description: W tym temacie przedstawiono funkcje i poprawki, które są dostępne w programie Microsoft Dynamics 365 Project Service Automation, aktualizacja 35, wer. 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473278"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Nowości i zmiany w aplikacji Project Service Automation, wydanie 35, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Z zadowoleniem informujemy, że jest to najnowsza aktualizacja aplikacji Microsoft Dynamics 365 Project Service Automation. To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. Jest ona kompatybilna z Dynamics 365 9.x. Aby dokonać aktualizacji do tego wydania, należy odwiedzić stronę Centrum administracyjnego dla rozwiązań Dynamics 365 online i zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie Project Service Automation, wydanie aktualizacji 35, wer. 3. Ta wersja ma numer kompilacji wersji V3.10.56.110 i zazwyczaj jest dostępna za pośrednictwem samodzielnej aktualizacji z września 2021 r.

## <a name="update-release-35"></a>Wydanie 35

### <a name="bug-fixes"></a>Poprawki błędów

Rozwiązano następujące problemy.

**Czas i wydatek**

- Osoba zatwierdzająca projekt otrzymuje komunikat o błędzie uprawnienia do odczytu w przypadku zatwierdzania wpisów wydatków za pośrednictwem roli **Osoba zatwierdzająca projekt**.
- Osoba zatwierdzająca projekt otrzymuje komunikat o błędzie uprawnienia do zapisu w **msdyn_projectapproval** w przypadku anulowania zatwierdzonego wpisu czasu za pośrednictwem roli **Osoba zatwierdzająca projekt**.
- Po wybraniu opcji **Kopiuj tydzień** we wpisie godziny w rozwiązaniu Dynamics 365 dla telefonu — moduł aplikacji Centrum zasobów projektu pojawia się następujący błąd: „...\OfficeProductivity_RibbonRules.js.map: błąd HTTP: kod stanu 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE”.
- Zasady **ponownych prób** automatycznie zatwierdzają wpisy, które wcześniej zostały odrzucone.
- Siatka podrzędna **Zestawy zatwierdzeń** zawiera akcje wstążki niemożliwe do zastosowania.
- Brak ikon dla elementów **Zadanie projektu** i **Rola zasobu** w encji **Wpis czasu**.
- Podczas importowania przypisań zasobów zaimportowane wpisy czasu nie mają poprawnego czasu trwania dla przypisań utworzonych w ramach zadań trybu ręcznego.
- Opcja **Usuń** nie jest wyświetlana na stronie **Wyszukiwanie zaawansowane rekordów wpisów czasu**.
- Opcja **Zapisz** nie jest wyświetlana na stronie **informacji dotyczących wpisu czasu**. Ten problem uniemożliwia zapisanie zmian po zamknięciu strony.

**Planowanie projektu**

- Siatki **Przypisanie zasobu** i **Uzgadnianie zasobów** nie sortują alfabetycznie pogrupowanych atrybutów.
- Nie można utworzyć zadań, jeśli zachowanie daty jest dostosowane do opcji **Tylko data**.

**Zarządzanie zasobami**

- Jeśli zainstalowano aplikację Dynamics 365 Field Service i program Project Service Automation, problemy z nadmiarowymi warstwami występują, gdy ze stroną główną skojarzono opcję **Widok skojarzony wymagania zasobu**.
- Dwukrotne kliknięcie pozycji **Zapisz** w oknie dialogowym **Szybkie tworzenie członka zespołu** uniemożliwia utworzenie wymagania zasobu.

**Sprzedaż**

- Po usunięciu zadania skojarzonego z ofertą o stanie **Wykorzystano** jest zgłaszany wyjątek.
