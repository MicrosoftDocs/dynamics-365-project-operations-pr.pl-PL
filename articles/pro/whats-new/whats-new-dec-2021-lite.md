---
title: Co nowego w grudniu 2021 r. — Project Operations — wersja uproszczona
description: To temat zawiera informacje o aktualizacjach jakości dostępnych w wydaniu Project Operations — wersja uproszczona w grudniu 2021 r.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585391"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Co nowego w grudniu 2021 r. — Project Operations — wersja uproszczona

_Zastosowane do: Wdrażanie uproszczone — od okazji do faktury pro forma_

Ten temat dotyczy następujących składników i wersji oprogramowania Microsoft Dynamics 365 Project Operations:

- Project Operations w środowisku Dataverse w wersji 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funkcje uwzględnione w tym wydaniu

### <a name="subcontract-management"></a>Zarządzanie podumowami 

- [Podwykonawstwo — członkowie zespołu projektu](../subcontracting/subcontracting-project-team-members.md): menedżer projektu może tworzyć nazwanych lub ogólnych członków zespołu z podumowami i pozycjami podumowy, co wpłynie na obsadzanie i szacowanie.
- [Opcje podwykonawstwa dla członków zespołu projektu](../subcontracting/subcon-options.md): podczas podejmowania decyzji o obsadzeniu dla ogólnych lub nazwanych członków zespołu projektu menedżer projektu może przeglądać istniejące podumowy lub tworzyć nowe podumowy dla co najmniej jednego członka zespołu projektu. 
- [Szacowanie kosztów przypisań zasobów w ramach podwykonawstwa](../subcontracting/costing-subcon-ra.md): szacowanie kosztów projektu uwzględnia przypisania zasobów podwykonawców i wycenia jej przy użyciu cenników zakupu skojarzonych z podumowami. 
- [Konfigurowanie tablicy harmonogramu do wyświetlania dyspozycyjności pracowników kontraktowych i podwykonawców](../subcontracting/configure-sb-subcon.md): można teraz skonfigurować tablicę harmonogramu w aplikacji Project Operations, aby wyszukać i zasugerować typ pracownika kontraktowego dla zasobów z możliwością rezerwowania oraz dyspozycyjności podwykonawców i pracowników. Ta konfiguracja może być stosowana podczas wyszukiwania zasobów w kontekście obsadzania dla określonego wymagania projektu lub podczas wyszukiwania poza kontekstem wymagania projektu.
- [Osadzanie projektu na podstawie dyspozycyjności pracowników kontraktowych i podwykonawców](../subcontracting/staffing-cw.md): pracownicy kontraktów mogą teraz być rezerwowani w projektach korzystających z środowisk tablicy harmonogramu.
- [Rejestrowanie czasu, wydatków i użycia materiałów w przypadku składników podwykonawców](../subcontracting/recording-subcon-actuals.md): pracownicy kontraktowi mogą rejestrować czas i koszty, a członkowie zespołu projektu mogą również rejestrować użycie materiałów zakupionych w ramach podumowy dla projektu. Spowoduje to rejestrowanie dokładnych kosztów projektów, w których jest wykorzystywana zakupiona dyspozycyjność lub materiały.
- [Przejścia stanu podumowy](../subcontracting/subcon-states.md): podumowy można potwierdzać w celu zakończenia negocjacji z dostawcą, zamykać w celu wskazania zakończenia dostawy lub anulować w celu wskazania zakończenia kontraktu z dostawcą przed zakończeniem dostawy.

### <a name="task-planning"></a>Planowanie zadań
- Usprawnione rozwiązywanie problemów dla administratorów systemów. Gdy użytkownik nie może otworzyć projektu, administrator może przejrzeć błędy niezwiązane z licencjami generowane przez rozwiązanie Project for the Web w [dziennikach planowania projektu](../../project-management/schedule-api-logs.md).
- [Używanie list kontrolnych zadań w rozwiązaniu Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). W rozwiązaniu Microsoft Project for the Web można dodać do zadania listę kontrolną, aby śledzić określone pozycji.

## <a name="quality-updates"></a>Aktualizacje dotyczące jakości

| **Obszar funkcji** | **Numer referencyjny** | **Aktualizacja dotycząca jakości** |
| --- | --- | --- |
| Planowanie i śledzenie | 2392596 | Interfejsy API planowania umożliwiają obecnie aktualizacje pól **Pozostały nakład pracy**, **Wykonany nakład pracy** i **% wykonania**. |
| Planowanie i śledzenie | 2478497 | Pola **Numer działania** i **Identyfikator zadania** w interfejsach API planowania mogą być puste, ponieważ system wypełni je przy użyciu automatycznego numerowania.|
| Czas i wydatek | 2468135 | Liczba operacji zatwierdzania zostanie zmniejszona z pięciu do trzech. |
| Czas i wydatek | 2468188 | Rozwiązano problem z tekstem dziennika przekraczającym maksymalną długość w atrybucie **notetext** encji **adnotacja**. |
