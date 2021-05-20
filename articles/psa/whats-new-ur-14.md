---
title: Nowości i zmiany w aplikacji Project Service Automation, wydanie 14, wer. 3
description: W tym temacie przedstawiono informacje na temat nowości w aktualizacji usługi Project Service Automation, wydanie 14, wer. 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 1d0aeb4684ae04d8774a31a51664ceb84307b10d
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949405"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, wydanie 14, wer. 3

[!include [banner](../includes/psa-now-project-operations.md)]

Mamy przyjemność przedstawić najnowszą aktualizację dotyczącą aplikacji Dynamics 365 Project Service Automation (PSA). To wydanie obejmuje znaczną poprawę jakości, wydajności i użyteczności. To wydanie jest zgodne z systemem Dynamics 365 9.x. Aby zaktualizować do tej wersji, odwiedź Centrum administracyjne programu Dynamics 365 online i przejdź na stronę rozwiązań, aby zainstalować aktualizację. By uzyskać więcej informacji, zobacz [Instalowanie, aktualizowanie lub usuwanie preferowanego rozwiązania](/power-platform/admin/install-remove-preferred-solution).

W tym temacie przedstawiono funkcje i poprawki, które są nowe lub zostały zmienione w programie PSA, wer. 3, aktualizacja 14. Numer tej kompilacji to 3.10.4.21 i jest on dostępny w następującym harmonogramie:

- **Powszechne udostępnienie (samoaktualizacja):** styczeń 2020
- **Automatyczna aktualizacja:** luty 2020

## <a name="update-release-14"></a>Wydanie 14

### <a name="enhancements"></a>Ulepszenia

- Sales

     - Wartości pól niestandardowych z **Szczegóły wiersza oferty** są kopiowane do **Szczegóły wiersza kontraktu projektu** podczas aktualizowania oferty do **Zamknięta jako wykorzystana**.
     - Potwierdzone projekty można **Zamknąć jako utracone**.

- Zarządzanie zasobami

     - Podczas rozszerzania rezerwacji użytkownicy będą proszeni o potwierdzenie, aby podsumować wyniki rezerwacji i podać łącze do obsługi rezerwacji.


### <a name="bug-fixes"></a>Poprawki błędów

- Czas i wydatek

     - Poprawione: udoskonalony sposób pracy użytkownika, jeśli użytkownik nie wybrał żadnych wpisów do skorygowania.

- Zarządzanie zasobami

     - Stałe: wielokrotna rezerwacja zasobu przepełnia nazwę rezerwowanego zasobu.

- Sales

     - Ustalone: Łączna cena sprzedaży nie jest obliczana, dopóki użytkownik nie wprowadzi kosztu własnego dla oszacowania kosztów projektu.
     - Naprawione: zamknięcie oferty jako **wykorzystanej** kończy się niepowodzeniem, jeśli skojarzony kontrakt dotyczący projektu nie znajduje się w stanie **roboczym**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]