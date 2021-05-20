---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 15, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 15, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949332"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, wydanie 15, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA). To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 15. Numer tej kompilacji to V3.10.5.28 i jest on zazwyczaj dostępny za pośrednictwem samoaktualizacji w styczniu 2020 r.

## <a name="update-release-15"></a>Wydanie 15 

### <a name="enhancements"></a>Ulepszenia

- Zarządzanie projektem

### <a name="bug-fixes"></a>Poprawki błędów

- Czas i wydatek

  - Naprawione: dodanie obsługi błędów podczas wczytywania w widoku uzgodnienia.
  - Naprawione: Centrum zasobów projektu: zmiana nazwy **kwoty** w celu zmniejszenia niejednoznaczności.
  - Naprawione: Dopasowanie widoku **kolumn wpisu czasu kopiowania**, aby zawierały typ.
  - Naprawione: czas trwania edycji czasu w widoku siatki za pomocą liczb dziesiętnych powoduje nieznane błędy w przypadku niektórych liczb.

- Zarządzanie projektem

  - Naprawione: menu rozwijane **użyj w widoku śledzenia** jest teraz rozwijane w zależności od szerokości opcji.
  - Naprawione: podczas zarządzania projektami w strefie czasowej +13 obliczenia zadań mogą wyświetlać niedokładne wyniki.
  - Naprawione: **czas zakończenia członka zespołu** został poprawiony podczas korzystania z kalendarza 24-godzinnego.
  - Naprawione: ponownie aktywowany **BPF** w formularzu głównym **msdyn_project**.
  - Naprawione: obliczenie przypisań nie ignoruje już jednego dnia.
  - Naprawione: do formularza projektu został dodany nowy transparent powiadomień, gdy strefa czasowa różni się między użytkownikiem i projektem.

- Sales

  - Naprawione: Wyszukiwanie wg kategorii oszacowania kosztów może służyć do filtrowania duplikatów.
  - Naprawione: kod w **PluginDomain.ExecuteInTryCatchBlock(..)** nie ukrywa już źródła wyjątku.
  - Naprawione: Komunikat błędu w **Wyszukiwaniu projektu** w formularzu **Wiersz oferty** nie pojawia się, gdy wprowadzono ponad 1000 projektów.
  - Naprawione: Siatka **Szacowane** dla oszacowań robocizny i oszacowań kosztów powoduje wyświetlenie poprawnego symbolu waluty.
  - Naprawione: po zaktualizowaniu PSA przez organizację z wydania 14 do wydania 15 karta **Harmonogram** nie pojawia się pusty w formularzu **Projekt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]